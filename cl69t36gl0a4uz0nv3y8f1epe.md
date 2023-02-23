# Integration Architecture Patterns

In today's world, it's common knowledge that most of the systems/ solutions built are complex. The nature of the complexity lies in sharing information between multiple systems that requires communication interwoven across like a spider web. I guess it will be easy to question the idiocy of the designer who designed the solution in the first place. But the reality, the shift from a monolithic architecture to microservices has also paved the way in giving independence in choosing what serves the purpose best irrespective of its dependence on the other applications or systems. This necessitates the requirement to build a process that aids in communicating the data between disparate applications, systems and/or environments.

# What is Integration Architecture?

Integration is one of the core architectures and by its name intends to connect systems, organisations and people. The systems involved can be heterogeneous in nature. This means that not all systems process information in the same format. There is a need for transforming the messages to the relevant format for the receiving systems to process them accordingly. And as we do that, there is a need to establish guardrails to enforce the right data policies, and guidelines for systems, organisations and teams to follow.

The guardrails are implemented through four main patterns:

# Integration Patterns

## File Transfer

A file is used as the media to transfer data between applications. When designing solutions for this particular integration, the key points of interest should be file name, file location, size, format, frequency of updates and read-write access to define the delete privilege - Job Scheduler, WORM (Write once and Read Many).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677123360737/d6ae4f16-4cce-4c53-974d-bb0351feb13a.png align="center")

When migrating servers from data centres to the cloud, this will be a common pattern to implement to transfer files from on-premises legacy applications to cloud storage like Amazon EFS or Amazon S3.

## Shared Database

The database is the media in which integration happens. Multiple applications share a common database where the shared data is stored. Applications in this instance share a common data schema and avoid data duplication and data transfer between the systems.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677123132397/6ea2b10f-3ca5-4dfb-985e-3b38b2537c2a.png align="center")

## Remote Procedure Invocation

A standard functionality or service is built to be exposed by one of the applications. This will be later accessed or invoked as a remote procedure by other applications—For example REST API.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677123539316/756d470c-5734-407d-a2ec-0d871188d350.png align="center")

## Messaging

The applications integrate by sharing messages between them. Similar to file transfer, this pattern integrates the applications by sharing messages. In some cases, this is achieved by an application publishing the information of interest to a messaging channel from which the consumer applications access/ subscribe. This leads to the definition of different message types:

* Request - response
    
* Fire and Forget
    
* Pub-Sub
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677123884892/64fa7394-ed37-43d1-a4db-fba233f2d5c6.png align="center")

When designing a messaging integration pattern, it is important to agree on the message translation format, schema structure and the composition of data attributes, types, lengths and business rules to validate the transfer.

# Resources:

https://www.enterpriseintegrationpatterns.com/

# Thank you for Reading - Let's Connect!

Enjoy my blog? For more such awesome blog articles - follow, subscribe and let's connect.