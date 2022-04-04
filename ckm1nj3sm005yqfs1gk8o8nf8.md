## How to run the chmod400 command on Windows

Have you attempted to connect to an EC2 instance from your machine? If so, you will know that the secure connection can only be established after running the chmod400 command on the security key pair file. The downside, there is no chmod command utility in Windows like we do in macOS, Linux, and other Unix-like operating systems. 

So, this post will detail an alternative - a PowerShell script that can be run to SSH to an EC2 instance from Windows OS and it does an equivalent job to the chmod400 command. 

## What does the chmod400 command do to a file or folder?

The command when run on the security key pair file basically removes all access to the file and gives only the current user read permission. So, when connecting to an EC2 instance, we are making sure no one has "write" access to the security key pair file. This is a mandatory requirement to connect to the EC2 instance safely. 

If running from MacOs or Linux, the command will be like:

```
$ chmod 400 securityfile.txt
``` 

The updated file permissions will look something like this:

|         | User | Group | Other |
|---------|------|-------|-------|
| **Read  **  | Yes  | No    | No    |
| **Write **  | No   | No    | No    |
| **Execute **| No   | No    | No    |

## chmod400 on Windows

The chmod command utility is not supported on windows. There are other ways to apply for the same file permissions. One way is to right-click to the file properties, security tab and then clicking on the Advanced button. In this dialog, you will have to disable inheritance and then remove access to all users except for the current user.  All these steps sound very tedious and if you consider doing it multiple times on different security key pair files to connect to different EC2 instances, it sounds un-productive!

So, here comes the magic script that does all that. But before you run the script make sure OpenSSH.Client and OpenSSH.Server are installed on your machine. These two are required to run the SSH command and can be found from this [link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse). Also, Powershell should have Microsoft.Powershell.Security Module installed. This script makes use of some of the cmdlets from this module.

### Powershell script

```
#NOTE:  Update the below parameters with your EC2 details before running this script.

#Parameters for Running the script
[string] $keyFile = "C:\AWS\ec2KeyPair.pem"
[string] $publicip = "ec2-user@XX.xXX.xXX.xxX" #update the public ip address here

#view the security key file permissions
Write-Host "Current ACL permissions to the security file:"
Get-Acl $keyFile | fl

#add current user with read control to the security file
$acl = Get-Acl $keyFile
$uName = [System.Security.Principal.WindowsIdentity]::GetCurrent().Name

$accessRule = New-Object System.Security.AccessControl.FileSystemAccessRule($uName,"Read","Allow")
$acl.SetAccessRule($accessRule)
$acl | Set-Acl $keyFile

#Delete inherited permissions
$acl.SetAccessRuleProtection($true,$false)
$acl | Set-Acl $keyFile

Write-Host "ACL Permissions after disabling inheritance and adding full control access to current user:"
Get-Acl $keyFile | fl

# ssh to the ec2-instance
ssh -i $keyFile $publicip
``` 

Copy the above script and update the parameters section with the location of your security key pair file and EC2 instance IP address. Once the file is saved, you just run the script. See, it is that simple and reduces running through multiple steps. 


### Thank you for Reading - Let's Connect!
Enjoy my blog? For more such awesome blog articles - follow, subscribe and let's connect.


