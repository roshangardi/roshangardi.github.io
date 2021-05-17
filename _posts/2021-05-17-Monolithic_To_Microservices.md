---
layout: post
author: roshangardi
title: Monolithic To Microservices
date: 2021-05-17T07:35:20.613+00:00
thumbnail: "/assets/img/posts/monovsmicro.PNG"
category: cloud
summary: Transition from monolithic to microsrevices
keywords: monolithic, microservices
permalink: "/blog/using-netlify-cms/"

---
***

Developers often decide whether to build monolithic or microservices architectures based on personal preference. This article tells you how to design the best platform for your client by considering both methods.

Monolithic all-connected platforms might serve a startup’s needs, but they often have problems with scaling to support growth. Architectures built with modular microservices work well for bigger enterprises, but they might be over-engineered to require more resources than a startup can spare. This article explains how to incorporate both these build approaches to design a functional strategy from the start that evolves to fit each point in a project’s life cycle.

This topic fosters all kinds of discussions. For some reason, both the microservice and the monolithic approaches generate fanatical devotees. Meaningless discussions without solid arguments often happen when designers have strong feelings about the architecture method they prefer.

### 

**Problems that kill business**

To be clear, monolithic architectures are great. And so are microservices. But each approach serves a specific purpose at a specific point in the timeline of a project. Problems arise when you commit one of these two biggest business killers:

* **Over-engineering**. If you over-engineer a platform with more components than it needs at each stage of development, you create a flawed, unwieldy structure. Over-engineering can cause serious technical debt later when your product crashes and must be repaired or completely redone.
* **Lack of planning**. If you charge forward and start coding without a plan, you skip an important and critical design step. Don’t assume that your favorite build type will fit all your clients’ needs at any point in their growth cycle.

All projects are unique, and all business goals are different. We need to plan the best approach right from the start in collaboration with our client as a partner. Then we need to adjust our approach as the project unfolds. We need to work agile. This article lays out foundational knowledge about monoliths and microservices, goes over each approach and describes a hybrid approach. It ends with recommendations that address some common problems you might face.

### **The Monolith approach**

Picture this structure as a single black box that has some inputs and some outputs. The code might be exceptionally well organized. But overall, it’s still just one big black box. In other words, the inner workings of a monolith are opaque, or hard to see, instead of transparent. So if you’re not very familiar with a platform, it might take time and effort to find a code that needs to be adjusted. And it’s all connected in one piece, so anything that goes wrong in one place usually affects the entire structure, which means even more digging.

![](/uploads/themonolith.png)
The code inside the monolith can follow software architecture and code organization patterns like model-view controller (MVC) or model view view model (MVVM). These types of apps are mostly used to create Minimum Viable Products (MVPs) or proof of concepts. But after these applications start to grow, they usually become more sophisticated. A more modular approach is required for these platforms to be sustainable.

### **The microservices approach**

There are many definitions of what microservices architecture means. The one I like best is

> “A particular way of designing software applications as suites of independently deployable services”
> — Martin Fowler (2014)

**_Independently_** is the keyword. Microservices without independent modules are just chaos. If we don’t design independent components, we only create a highly coupled, low-cohesion Frankenstein that requires a lot of work to deliver, run, and maintain. By definition, a microservices architecture has more weak links and more entropy than a monolith. So it needs more documentation and a highly skilled team.

#### Modularity

A big benefit of decomposing an application into independent smaller microservices is improved modularity. Microservice apps are easier to understand, develop, and test than monoliths. And they’re more resilient to architecture erosion.

#### Cost-effective and scalable

It’s more cost-effective to scale microservice platforms because you only need to scale individual components. You don’t have to make global changes to an entire connected structure. And it’s much easier to identify bottlenecks when you can monitor each component individually.

#### Faster

Microservice development is also faster than monolithic because specialized teams can work at the same time on independent parts of the project. By parallelizing development, small autonomous teams can develop, deliver, run, and scale their respective services independently.

![](/uploads/microservicearch.png)
The most important thing about this diagram is to consider each “service” as a separate entity.

Your main design goal is for each service to solve each business goal in the most optimal way. So each individual service might need a NoSQL database, Redis cache, or different programming language than the others. And the architecture and deployment services must support all the different design decisions. Ideally, the separate subsystems don’t speak to each other, but they’re loosely coupled

> The golden rule: can you make a change to a service and deploy it by itself without changing anything else?
> ― Sam Newman, Building Microservices

### The perils of over-engineering

There’s one more important thing to note. If your team can’t build a monolith properly, they definitely can’t build microservices architecture. One of the worst things inexperienced teams often do is over-designing a project at the beginning. That newbie mistake can kill a business because most startup companies don’t have money to burn. They don’t have the resources to maintain excess components when they’re not needed or to pay for major platform overhauls to have harm-causing parts adjusted or removed. Over-engineering is dangerous. It can bleed out a company’s budget until there’s nothing left to operate on. I’ve seen many more companies fail due to Over-engineering than from lack of good architecture.

> Make solid design decisions
>
> Poorly designed big architecture sometimes means no design.

Over-engineering is a sign that a design team doesn’t know how to build a platform that fits the needs of their client. Sometimes the client’s team doesn’t clearly understand or agree on their own needs. They might make unrealistic assumptions about their businesses’ true potential. Alluring fantasies about overnight success can cause a disconnect from reality. When a dev team and its client are overly confident or biased, they’re likely to make faulty decisions based on gut feelings instead of accurate data. A high-functioning agile design team will point their clients in the right direction and work with them to build the best platform to take them there.

Over-engineering usually means too many assumptions, lack of connection to reality, too much self-confidence, and bias to take gut feeling-based decisions (instead of much more accurate data-driven ones).

### Hybrid approaches

We often take hybrid approaches in real-life situations. A simple example is wearing a hooded jacket to work. With this jacket’s various options for wearing or not wearing, you’re prepared for variable temperatures and rain or dry weather. Now consider all the variables involved in software architecture: time restrictions, team, budget, scalability, maturity of the company, and desired business outcomes. A hybrid approach is a flexible solution that covers the possible needs of all these elements.

#### Plan your platform

Long-term planning gives us enough information to decide whether to implement a monolith or go for a more microservice-oriented architecture. Usually, it’s not hard to estimate scalability needs. For a project to grow and succeed, it must be built on a high-quality platform that’s designed to easily identify bottlenecks and scale up one step at a time.

#### The modular monolith

What I call a modular monolith is a hybrid architecture where the platform isn’t made up of multiple independent services. But code is organized so that semantic concepts are clear. With this design type, you first identify distinct but separate high-level ideals or groups of functionalities. Then you partition your code architecture to reflect this natural separation. An MVC architecture is an example. You can view this platform as a collection of MVCs subsystems, and you can segregate the code of each subsystem. Changing your monolith architecture to a modular monolith makes it easier for the platform to evolve. And it removes the barriers to converting the platform toward microservices if they’re needed in the future.

#### The life cycle of a successful product

Let’s say that your company goes from a napkin idea to a multimillion-dollar business that went public and that it all started with an MVP. You probably started with a well-designed monolith. Your company tried to identify product-market fit and made many data-driven decisions. As your business started to gain traction, some bottlenecks were identified, either reactively or by using load test simulations. These pain points required architecture changes that made the system become increasingly more modular. After more changes, some modules became near-independent systems. Teams could work on each module individually. At the same time, DevOps and deployment management became more sophisticated, and the level of automation increased every day. Now your product looks like a microservices approach, but it evolved to that state naturally.

### How most companies succeed

* Design an architecture that supports desired business outcomes.
* Make data-driven decisions.
* Do not over-engineer.
* Anticipate scalability challenges and plan for them. Be pragmatic.
* Avoid ego-driven decisions, and stay agile.

To build a profitable platform, you have to solve design problems in the most effective and efficient way. You can’t waste resources with overcomplicated solutions and unnecessary over-engineering. And you must follow robust architecture guidelines and standards, so the platform can scale.

## There is no “versus”

Monoliths are great for some problems, microservices are great for others. Know how and when to adapt the best solution or combination of solutions to fit the evolving needs of your project. Your true value as a developer is how well you create the best solutions for specific problems.

Data knowledge, experience, intuition, skills, and pragmatism separate the bad engineers from the good and the best ones — those who make a real difference to their client’s long-term success.

### References

Conway, M.E. (1968, April). “How do committees invent?” Retrieved from \[link\] (http://www.melconway.com/Home/Committees_Paper.html)

Fowler, M. (2014, March 25). “Microservices: a definition of this new architectural term.”

Fowler, M., and Webber, J. (2008, June 6). “Does my bus look big in this?”

Richardson, C. (2019). “What are microservices?

***