## Understanding Design Concerns in Systems Architecture


For the past 8 years, apart from leading projects delivery, I have been heavily involved in designing solutions and had my fair share of documenting solutions blueprints. Before you build any system - looking at it from different perspectives, working the optimal solution out of multiple alternatives, selecting infrastructure, and estimating - is always a unique and challenging problem-solving exercise. It is an art, one you need to be passionate about and have the instinct to make the risky decisions that balance out with the right outcomes. 

This blog focuses on understanding the design concerns which drive some of the key decisions in systems architecture. These design concerns are the thumb rules that guide in making the right choices throughout the project life cycle. 

## What is Systems Architecture?

According to [SEBOK WIKI](https://www.sebokwiki.org/wiki/System_Architecture): 

> Systems Architecture is abstract, conceptualization-oriented, global, and focused to achieve the mission and life cycle concepts of the system. It also focuses on high-level structure in systems and system elements.

Now that sounds very complex. In simple terms, systems architecture is the fundamental and unifying system structure defined in terms of system elements, interfaces, processes, constraints, and behaviors.

## Is it Just Software or Hardware?

This is one of the common questions that is posed by most beginners. When we say system elements, interfaces, and processes. It deludes that maybe a systems architecture should just cover the software side of the system and has nothing to do with the hardware layer. Well, that is not correct. 

It includes elements of both software and hardware and is used to enable the design of such a composite system. For example, let's say you are building the systems architecture for an online booking system. A very high-level view would entail a web front-end, business service layer, and the web backend (database). 

![scott-graham-5fNmWej4tAA-unsplash.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1648787943656/8jvRb0V9d.jpg)

## Why is it important? 

Now you know what is systems architecture but why do you need it? Can't I simply build the system without the trouble to brainstorm the different components, capabilities, and functions that make up the system's architecture? 

Understand that systems architecture is a powerful tool and a common language that enables collaboration between all your diverse teams working to build a single system. This common language aids in being understood and represents the multiple views of all the teams. 

Let's look into the last example of the online booking system - let's say there is a business requirement that states the system must handle 1M transactions per second. Now, designing and implementing this requirement will involve the cohesive effort of the infrastructure team, and the back-end team. Both teams should converge on an agreed approach to handle the requirement. Often it is misunderstood that solutions architecture is a single person's job but in reality, it involves input from a group of SMEs who are experts in their areas. 

## Planning

When you look at SDLC, the first phase of any project irrespective of the project methodology or framework you are following, you will start with planning. 

The first step before we start working on the systems architecture draft is analyzing the as-is architecture. Yes, you heard me right before you start diving into various solutions for the problem statement. Understand the client's existing architecture - identify their pain points and the stakeholder concerns. Sometimes these are not obvious and require multiple workshops to unearth the ongoing issues faced by the end-users. This analysis will help categorize the list of requirements (aiming to address the problem statement) into functional requirements and technical requirements. 

> What? Why? How?

![ana-municio-PbzntH58GLQ-unsplash.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1648792036151/iaVj4BO3l.jpg)

Trust me, it's way easier to find a rock with a question mark symbol when compared to identifying some of the unknown assumptions made on the requirements. An in-depth analysis should be performed on what a particular requirement is going to achieve, why is it needed in the first place, and how to implement it will lay the foundations for the design. 

## Design Concerns

Even when there are no explicit requirements stated by the client, there will still be expectations, stated or not. The architect should understand what is requested, what is needed, and what is possible for each of the design concerns. 

- Scalability - how many users or transactions can it process concurrently?
- Performance - how fast does it respond? what is the max throughput?
- Recoverability - how does the application recover from a fault?
- Security - can it sustain attacks? is data protected? 
- Maintainability - how easy is it to maintain? 
- Operability - how easy is it to use and manage? how is it operated? 
- Availability - is it available 24x7 and is it 99.9% or 99.99%?

These concerns should always be in the back of your mind to rule out all known and unknown assumptions. 

## Two Additional Concerns

- Affordability
- Sustainability

In this year's Accenture's Fjord Trends 2022, there is one trend that can be adapted to the design thinking process. The pandemic has brought some unforeseen challenges to the supply chain. If there is something it taught us is to end the abundance thinking approach. 

Yes, the cloud and some of the latest technologies can provide infinite and bottomless computing power but every responsible business understands that they have to play a part in tackling climate change and how they can help achieve the net-zero carbon emission targets. Similarly, working towards affordability will help the clients to keep the costs low and bring in additional value. 

One thing to keep in mind is that when designing for the balance between affordability and sustainability, it is important to decouple innovation from the notion of new. 

## Use Case

To learn how to apply the above-mentioned design concerns to a use case on deploying a highly available and scalable WordPress site on AWS - check this [youtube video](https://www.youtube.com/watch?v=rOSpqA3UmwA&t=53s). 

# Thank you for Reading - Let's Connect!
Enjoy my blog? For more such awesome blog articles - follow, subscribe, and let's connect.

 








