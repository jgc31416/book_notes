
Definition of SW Eng:  the application of an **empirical, scientific approach** to finding **efficient**, **economic** solutions to practical problems in software.

I guess the empirical/scientific approach is characteristic from this definition, it serves to distill the "engineering" knowledge body.

Looks like the central problem in SW is complexity. 

Interesting mention to SW productivity from '68, there is no technology or management strategy that can double productivity every 10 years, still remains true.

Eng. practices should be measured by the question: applying this would allow me to make better software faster? 

The fail safe behavior from Apollo:
"The assumption was not that you could plan and get it right first time, rather that you treated all ideas, solutions, and designs with skepticism until you ran out of ideas about how things could go wrong. Occasionally, reality is still going to surprise you, but this is engineering empiricism at work."

The engineering-focused team will use accurate measurement, rather than waiting for something bad to happen. They will measure the performance of their software to detect leaks before they become a problem!

Engineering Vs Craftmanship: craft is not enough for SW, it gives interesting values to the field like skill, creativity and innovation, but it misses things like scaling and improvement beyond human skills.

Tools matter only to the degree to which they “move the dial” on some more fundamental things.


The measures are stability and throughput. Teams with high stability and high throughput are classified as “high performers,” while teams with low scores against these measures are “low performers.”


Stability is tracked by the following:
• Change Failure Rate: The rate at which a change introduces a defect at a particular point in the process
• Recovery Failure Time: How long to recover from a failure at a particular point in the process


Throughput is tracked by the following:
• Lead Time: A measure of the efficiency of the development process. How long for a single-line change to go from “idea” to “working software”?
• Frequency: A measure of speed. How often are changes deployed into production?

Counterintuitive: Approval board, they slow things up.


## Modularity ##

When interfasing with 3rd party systems there needs to be a connection layer that separates the inner working of the system with the 3rd party system.

There should be just only one deployment pipeline for a given module, if the code is monorepo a fast enought pipeline should be in place, if multirepo then we need to ensure stability of a distributed system. **There is no middle ground**

At small scale, dependency injection helps with modularity and testability. 

In large systems modularity means we can develop in parallel safely, this leads to a microservices architecture. This architecture must be matched by the organization, otherwise it does not work.



## Cohesion ##

*Pull the things that are related together, put the things that are unrelated further apart*

Modules internally need cohesion, each part of the code needs to be focused in one specific task.

Domain Driven Design might be helpful when trying to find the balance between cohesion and modularity:
- Ubiquitous language: shared language between code and the business problem domain.
- Bounded contexts: order in an order management system is different than in an invoicing system. 
- If the SW design mimics the structure of the business problem, a small change in the business process will lead to a small change in the code.

Cohesion implies some degree of coupling, but it is not the same, A and B are coupled if a change in A forces a change in B, they are coherent if a change in A adds value to B.

A key measure for cohesion is the cost of making a change in the system, if you have to change things in a lot of places then you have poor cohesion.


## Separations of concerns ##

Keep the focus small.
Dependency injection helps acting as a demacration between concerns.

Essential complexity: complexity that comes directly from the problem to solve, in contrast wito accidental complexity, what we need to do in computing systems to solve the problem. 

Separating essential from accidental complexity helps untangling the system.

DDD can help also with separations of concerns, it can give us the initial modules to be refined later.

As soon as we describe a module with a sentence like this: This module deals with A and B, it can be a signal that we should decompose it further. 


## Coupling ##

Coupling is needed for communication, managing it is central for SW scalability and managing complexity.
It is the main reason why you can't speed up a project just by throwing more people at it. 

Microservices architecture helps figthing coupling, the key there is to be able to deploy it independently and a solution when you need to scale up development in the organization.
The cost comes in the design and the complexity of the isolated system.
Good practice in microservices will push communications between services to be async. 
Organizations that go into microservices do loose control as there is little need for coordination.

Decoupling usually means more code and taking it to the extreme can affect even performance. 

Michel Nygard coupling model:
- Operational: one system needs another to operate.
- Developmental: two systems need to be deployed at the same time or in sync.
- Semantic: they need to change together because shared concept, usually a concept will be a collection of facets, if that collection changes then both systems have to be changed. It is better to allow the systems to deal with the needed facets.
- Functional: i.e. systems share similar message technology
- Incidental: no good reason.

Coupling usually makes the whole chain of components to behave as bad as its weakest component (throughput, availability, latency and so on).

There is no middle way between a monolith and a microservice approach in terms of system testing/deploy you need to test the whole thing ( if monolith, invest on the test system to be fast enough so coupling doesn't bring down the speed of development)



