---
title: "Azure Resource Manager 101 - Unlocking the Essentials for Seamless Cloud Deployment and Management"
datePublished: Fri Jan 26 2024 06:35:47 GMT+0000 (Coordinated Universal Time)
cuid: clru9rcn2000009l31abugq3l
slug: azure-resource-manager-101-unlocking-the-essentials-for-seamless-cloud-deployment-and-management
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1706234068843/a3c6828c-83c4-47d8-80b0-e8dd1dfc618b.png
tags: cloud, azure, cloud-computing, azure-certified, cloud-architecture

---

Globally, Azure has millions of active customers building complex cloud solutions. As the complexity grows, it is essential to rely on Azure Resource Manager service, which will assist in efficient, consistent, and scalable management of Azure resources, providing a foundation for Infrastructure as Code, streamlined deployment processes, and robust resource governance.

Before diving further into Azure Resource Manager, first, let's understand its building blocks - resources and resource groups.

## Resources

Azure provides more than 200 services. A resource is defined as an object that manages one of these services. The compute, network and storage service type that supplies resources is called a resource provider. This resource provider will be responsible for interpreting and processing requests for the resource type. In other words, when you perform lifecycle operations like create, update and delete for a resource, you are interacting with a resource provider.

### 💡Pro Tip

Do you struggle with naming your objects, functions and files in your code like me? I always find it easy to follow naming conventions as they provide order and consistent awareness of the resource. So, when starting a new project, make it a best practice to define the naming convention standard the team should follow. For convenience, start with a lowercase letter and a number at the end for Azure resources. However, specific naming rules and conventions are applicable for different Azure resources. More details can be found in this [link](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/resource-name-rules).

## Resource Groups

A logical grouping of resources is known as a resource group. Logical grouping can be interpreted differently, so different strategies can be applied to group the resources:

* Group by resource type
    
* Group by service lifecycle
    
* Group by business domain
    
* Group by location
    
* Group by purpose
    
* Group by billing groups
    

No one shoe size fits all similarly, no one grouping strategy suits all businesses. Often, a mix of these grouping strategies is used to create resource groups. Resource groups are defined before the resources because the group must be referenced when creating the resource.

### 💡Pro Tip

A resource group can have multiple resources, whereas a resource can only be associated with one resource. And, unlike Google Cloud, resource groups cannot be nested. So, organising resources or resource groups hierarchically is not doable in Azure.

## Azure Resource Manager

Azure Resource Manager (ARM) is defined as a deployment and management service that assists in creating, updating and deleting resources in your Azure account. Azure Resource Manager uses a unified language (JSON notation). The language is consistent across all the Azure interfaces (Azure Portal, Azure CLI, Cloud Shell, PowerShell). It is also responsible for checking the privileges and whether a resource has the required access and control to execute the relevant operation.

## 🌩Bonus Points

* A resource can be created in a location different to a resource group. You read it correctly! The resource group stores the meta-data about the resource, so for compliance reasons, you may want to have the resource group stored in a region different to the resource is in. In this case, grouping resources by location is the obvious choice.
    
* All resources associated with the group are deleted when a resource group is deleted.
    
* Azure Resource Manager will only support Transport Layer Security 1.2 or later.
    
* By default, you can associate 800 instances of a resource type in a resource group. However, some exceptions can be found in this [link](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/resources-without-resource-group-limit).
    

### 📚Resources

* [https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview)
    
* [https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/resource-name-rules](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/resource-name-rules)
    
* [https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/resources-without-resource-group-limit](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/resources-without-resource-group-limit)
    
* [https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/naming-and-tagging](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/naming-and-tagging)
    

# **Thank you for Reading - Let's Connect!**

Did you enjoy my blog? For more such blog articles - follow, subscribe, and let's connect.