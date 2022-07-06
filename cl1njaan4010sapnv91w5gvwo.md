## How to choose your AWS Region?

The recent pandemic has brought a surge in digital transformations with a growing demand to migrate the applications and/or services to the cloud to cut down on costs. According to [ISG Provider Lens Report](https://www.tcs.com/content/dam/tcs/pdf/discover-tcs/about-us/analystreport/tcs-recognised-leader-aws-services-australia.pdf), there has been a demand from firms in seeking out AWS provider partners. Now, if you have been part of this transformation, one of the most commonly asked questions is about the selection of the AWS region. 

# What is a Region?

A region is a self-contained geographic location positioned within a single country boundary and hence bounded by a single set of laws. 

![A view of the data centres.](https://cdn.hashnode.com/res/hashnode/image/upload/v1649159659287/Jglf8A8mo.jpg)

To put this into context, imagine you have a group of logical data centres within a single geographic location (let's say, Sydney West). This is called an availability zone (AZ). Now group a cluster of these AZs which are connected by a proprietary high-speed fibre network (100GbE fibre network backbone) with multiple lines between every AZ so the cluster of data centres can be treated as a single area. This area will end up being your region. 

# Why does it matter?

AWS resources are hosted across multiple locations. These locations are categorized into regions, availability zones, and local zones. The full list of regions and the global AWS infrastructure available from each region can be found [here](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/?p=ugi&l=na).

Largely, AWS services are region scoped. Let's say you have your service available in the Asia Pacific (Sydney) region. When you choose Asia Pacific (Singapore), it is expected that the data related to the service available in Sydney is no longer accessible unless it is specifically replicated. Data is not synced between regions without the explicit configuration. 

On the other hand, some of the AWS services are global and hence do not require a region selection. These services operate at a global level and are accessible from all regions. Example: IAM. 

# Which region to choose?

As mentioned above, the majority of the AWS services are region-based. Let's say you have made the call to move your existing enterprise application to AWS. Before the application is deployed to an EC2 instance, your first step will be the region selection. This can be determined by answering the following questions: 

- Are the services required to deploy your enterprise application available in a region?
- Where are your end-users located?
- Are there any additional costs involved in your selected region?
- Are there any compliance requirements stated by the law in the location the region is in?

## Service Availability

![Service is available in a particular AWS region.](https://cdn.hashnode.com/res/hashnode/image/upload/v1649161610072/bGAMAfwFl.png)

Not all AWS services are available in all regions. Most importantly, AWS tends to release its services incrementally across its regions and the first region that they release is to US East (N. Virginia). To check whether a service is available in a particular region, click this [link](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/?p=ugi&l=na). This site is updated daily by AWS and will have the latest information. 

## Latency

![Light speed in sharing data.](https://cdn.hashnode.com/res/hashnode/image/upload/v1649162246212/SCC0sHOxh.png)

Research where your user volume is located. Let's say all your users are from Australia then it is wise to choose the Sydney region. This will ensure that there is minimal latency in responding to your user requests. Although choosing a Singapore region, in this case, may incur a fraction of a milliseconds delay in comparison to the Sydney region. 

## Cost

![money tree](https://cdn.hashnode.com/res/hashnode/image/upload/v1649223118678/2ao_7F3c_.png)

As regions are geographic locations within a single country, these regions are bound to the laws governed by the location. This in turn will have a variance in taxes and the costs involved in hosting the resources within the AWS infrastructure. 

Depending on your costs, you can choose by selecting a region that will work within your budget. 

## Compliance

![compliance requirements](https://cdn.hashnode.com/res/hashnode/image/upload/v1649245921615/jEHEbYdpZ.png)

Depending on the region you choose, the data managed within your application must abide by the compliance requirements from that location. 

- what are the different types of user data you are allowed to store?
- how long can you store the data?
- what are the different encryption policies applied to the data?

For example, if your data source location mandates that the user data should be stored within the country. This will limit your choice of region to the regions within that country. 

Considering the responses to the above 4 factors, you should be able to easily conclude the selection of your AWS region. However, if your application is being deployed to multi-regions, the compliance requirements should be considered on how the data is replicated across different regions.

# Thank you for Reading - Let's Connect!
Enjoy my blog? For more such awesome blog articles - follow, subscribe and let's connect.





