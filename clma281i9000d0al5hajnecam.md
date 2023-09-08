---
title: "Is AWS Really Safe? A Security Overview"
seoTitle: "AWS Security: Is It Truly Safe?"
seoDescription: "Examine AWS security, shared responsibility, infrastructure protection for cloud data safety and addressing customer concerns"
datePublished: Fri Sep 08 2023 03:50:53 GMT+0000 (Coordinated Universal Time)
cuid: clma281i9000d0al5hajnecam
slug: is-aws-really-safe-a-security-overview
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1694128555353/40bdcc9b-4720-44cc-9497-78f9af9b428b.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1694144964758/4ca32893-e0de-4cdd-911f-5fd90c59229a.png
tags: aws, security, cloud-computing, securityawareness, solutionarchitect

---

Recently, I attended a role-playing interview that was extremely interesting. One of the questions involved meeting an existing AWS customer, who, during our chat, voiced concerns about the security of their cloud. I delved into the topic of securing their cloud data. After a few questions, I realized the customer's concern was focused on the security of AWS infrastructure. So, here is my fresh take on this:

AWS has been named the leader in Cloud Infrastructure and Platform Services (CIPS) by [Gartner](https://aws.amazon.com/blogs/aws/aws-named-as-a-leader-in-the-2022-gartner-cloud-infrastructure-platform-services-cips-magic-quadrant-for-the-12th-consecutive-year/) for 12 consecutive years. Now, that's a huge achievement that validates AWS is at the forefront of operational excellence in securing its cloud infrastructure. This is backed by over [300 cloud security tools](https://aws.amazon.com/security/?nc1=f_cc) and the [testimonials](https://aws.amazon.com/compliance/testimonials/) of its most sensitive customers. All this sounds great, but what exactly does this mean, and how does it translate to an AWS cloud being secure?

This all sounds good, but what exactly does AWS do to secure the cloud, and how? To understand this, we need to delve into the [AWS Shared Security Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/). According to this model, it is clear that AWS takes sole ownership of securing the infrastructure supporting the cloud. This includes all hardware, AWS global infrastructure - regions, availability zones, and edge locations.

![Figure 1: AWS Security Responsibility Model](https://d1.awsstatic.com/security-center/Shared_Responsibility_Model_V2.59d1eccec334b366627e9295b304202faf7b899b.jpg align="center")

AWS Region consists of a collection of Availability Zones (AZ), [with at least 3 AZs per region](https://aws.amazon.com/about-aws/global-infrastructure/?p=ngi&loc=1). If we look at this from an infrastructure perspective, each region is a cluster of data centres, and each group of logical data centres is defined as an availability zone. Multiple lines of proprietary high-speed fibre networks run between every availability zone, so we can treat the group of AZs as a single area. For those interested in learning more about AWS regions and which ones to choose for your project or account, read my insights [here](https://narmadanannaka.com/how-to-choose-your-aws-region).

So, back to the question of how one knows if their cloud infrastructure is secure. In simpler words, let's take an EC2 instance, which is nothing but a virtual machine hosted on a physical machine in a data centre somewhere in the world. The customer raises concerns that the resources are on a shared infrastructure. It is very unlikely one can pinpoint the specific hardware on which the EC2 instance virtual machine is running. Because the shared infrastructure context is broader - we are talking about a specific AZ. According to our definition above, that is a group of logical data centres located within a region. This could be one or more data centres in distinct locations.

On top of this obscurity, AWS provides several [security capabilities and services](https://d1.awsstatic.com/whitepapers/Security/Intro_to_AWS_Security.pdf):

* All connections throughout the AWS global infrastructure (AWS Regions and AZs) are automatically encrypted, and the connections are secured.
    
* The spread of AWS infrastructure throughout the world limits the surface area for any [DDoS](https://aws.amazon.com/shield/ddos-attack-protection/) attacks. Additionally, AWS is known for surviving one of the largest DDoS attacks, [targeting 2.3 Tbps requests](https://aws-shield-tlr.s3.amazonaws.com/2020-Q1_AWS_Shield_TLR.pdf).
    
* AWS resources can be isolated into a logical virtual network that can be defined by the customer, also known as the [Amazon Virtual Private Cloud](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) (Amazon VPC). This is secured through built-in network firewalls.
    
* Connectivity options within the network or outside the network provide options for private or dedicated connections.
    

On top of the general cloud infrastructure, any software installed to support the computing, storage, database, and networking (serverless) facilities is secured by AWS through automatic software updates and security patching.

# **Thank you for Reading - Let's Connect!**

Enjoy my blog? For more such awesome blog articles - follow, subscribe and let's connect.