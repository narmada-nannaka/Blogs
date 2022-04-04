## How to run Forefront Identity Manager (FIM) PowerShell cmdlets

If you have been working with the outdated Microsoft's Forefront Identity Manager (FIM), there will come a point where you will have to run some of the PowerShell commands from a non-FIM machine. This blog post shares the automated script you can use to register the FIM libraries. 

```
d:
cd c:\utilities
set-alias installutil $env:windir\Microsoft.NET\Framework64\v2.0.50727\installutil
installutil .\Microsoft.ResourceManagement.Automation.dll
installutil .\Microsoft.ResourceManagement.dll
Set-location "c:\utilities"
[System.Reflection.Assembly]::Load("System.EnterpriseServices, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a")
$publish = New-Object System.EnterpriseServices.Internal.Publish
$publish.GacInstall("c:\utilities\Microsoft.ResourceManagement.dll")
$publish.GacInstall$publish.GacInstall("c:\utilities\Microsoft.ResourceManagement.Automation.dll")
``` 

Note: It is critical that you are loading the correct versions of your libraries depending on your machine OS version. 

The above script is for a 64-bit machine, for a 32-bit you should update the set-alias command to refer to C:\Windows\Microsoft.NET\Framework\v2.0.50727\installutil

Once the above script is run, you should be able to load the pssnap-in by running the following command: 

```add-pssnapin FIMAutomation
``` 

The above command will load the modules and from here you should be good to run the FIM-related cmdlets from your PowerShell.

#Thank you for Reading - Let's Connect!
Enjoy my blog? For more such awesome blog articles - follow, subscribe and let's connect.

