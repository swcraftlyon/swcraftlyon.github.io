---
title: "Open forum avec DDD Iran"
date: 2021-03-11T18:30:00+02:00
tags: ["ddd", "unconf"]
---


- Subject : Open-forum DDD with DDD Iran community
- Meetup : https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/276378533/
- Attendees : ~25

# Session 1 (35 minutes) 19h - 19h35

## Room 1:

* [Colin] WTF is DDD?
* [milad] Introduction to DDD, related tools/frameworks/libraries w/e that exists for it
* [milad] Where should business constraints be checked in DDD? (on dtos? domai entities? persistence entities?)
* [milad] What is a Domain Event? Does it have anything to do with transactions?
* [milad] What libraries and frameworks are available in Java ecosystem to implement the DDD approach?
* [milad] In Clean Architecture, it suggests that domain shouldn't be dependent on DB. So can a domain utilizes the Repository interface on its implementation? Or getting data (and using repository interface) should occur in use cases?
* [milad] Can you suggest any real world code samples (repositories) in github or so, which adhering to the best practices in DDD?

### Session

We talked about tactical and strategic patterns, toolbox and the likes :D

**Resources**

* https://www.infoq.com/minibooks/domain-driven-design-quickly/
* https://www.amazon.fr/Domain-Driven-Design-Distilled-Vaughn-Vernon/dp/0134434420
* https://gitlab.com/cdamon/padbowl
* https://gitlab.ippon.fr/twitch/live-coding-fr/-/tree/master/borestop
* https://blog.ippon.fr/2021/02/17/spring-boot-hexagone/
* https://blog.ippon.fr/2021/02/22/publier-des-domain-events-depuis-un-hexagone/
* https://blog.ippon.fr/2020/04/01/des-objets-pas-des-data-classes/

## Room 2:

[Anthony] Are DDD principles relevant in Front-End applications?

### Session    

Back-End is not the only brick that have business operation.
It's totally possible to represent things using DDD concepts (Aggregates, Value Objects, Entities, Repositories, Builders …)
Hexagonal archicture helps a lot to not be dependent on the infrastructure and having a better domain model
    
Conclusion: There is not a lot of differences between Back-End and Frond-End applications, so it's actually possible and relevant to use DDD concepts in the two worlds.
    
## Room 3:

[Elahe] Where DDD can go wrong in a project?

### Session

Share experiences :

* A series of DDD Project without advertising 
* Change many files to modify  Data
* Used Hexagonal Architecture to separate concerns (UI, Domain, DB)
* If CRUD, you don't need DDD and many layers
* Work with developers that don't have the same mindset -> Failed to board other developers
* Focus on technologies and DDD is not about Technologies
* DDD needs learning -> give time to people to take time -> Zahra suggest Clean Architecture of Uncle Bob
* Mix of DDD with traditional concepts
* Absence of a coach
* Don't focus on names but concepts. That's not because we tell you, you are working on a DDD project that you are doing DDD -> important is concepts
* A big focus on tactical design more than Strategic Design and Collaborative Modeling
* Don't use the same model in Front and Back -> separation of concerns
* Data structure should not impact our Domain modeling
* Team Topologies can create some problems
* Frameworks can impact our Domain. We should get rid of them in Domain layer
* Domain should change when business rules changes, not when the technologies changes
* DDD language : for example Entity. People could think about en Entity in DB side (ORM)
* Explain concepts except using keywords

## Room 4:

* [moreka] functional programming, scala; use cases and the future of it
* [Masoud] Adhering to domain purity, trade offs, pitfalls and solutions (case study: separating domain model form persistence model)

### Session

FP: pure computations without side effects: 

* Pure: a function with the same inputs will always return the same output
* No side effect: no operations like I/O that you can't see as you are calling the function
    
**Resources**

* https://pragprog.com/titles/swdddf/domain-modeling-made-functional/ by https://twitter.com/ScottWlaschin
* https://fsharpforfunandprofit.com/books/
* https://github.com/HackYourJob/introFSharp-TypeDD-Fable/blob/master/fsharp/Game.fsx
* https://enterprisecraftsmanship.com/posts/having-the-domain-model-separate-from-the-persistence-model/

# Session 2 (35 minutes) 19h40 - 20h15

## Room 1:

[Nolwenn] How to share knowledge or coding skills between team members ?

### Session

* Pair or mob programing to share business knowledge but how to sell it to our manager
* Living documentation https://www.youtube.com/watch?v=LG4SADs2nf8 (in french)
* https://www.youtube.com/watch?v=D_vmf2ktUt4 (in french)
* About mob programming in a startup https://www.youtube.com/watch?v=yhBne591Zbk (in french)
* https://woodyzuill.com/
* Eventstorming or event modeling to share knowlegde between dev and business people
* https://www.eventstorming.com/ by https://twitter.com/ziobrando
* https://eventmodeling.org/ by https://twitter.com/adymitruk
    
Tools for online workshop sessions :

* https://miro.com/
* https://metroretro.io/ (for retrospectives)
    
## Room 2:

[Elahe] How our communities work :). let's share ideas

### Session

* http://www.lyontechhub.org/#!/
* https://www.youtube.com/watch?v=-PX0BV9hGZY   Tail Call Optimization
    
## Room 3:

[Elahe] primitive obsession and Value objects can be a good topic too :)

### Session

* Value objects are more precise to express domain and can manage business operations.
* https://refactoring.guru/smells/primitive-obsession
* https://martinfowler.com/articles/replaceThrowWithNotification.html
* Memento pattern: a technique to store and restore state of an aggregate root 

## Room 4:

[Matt] Has anyone used DDD outside of software engineering to approach non-technical concepts?

### Session

* Try to use storytelling
* Example : Mariage : I want Flowers; a big Hall and Music is not important. This story can help us to create Bounded Contextes and give some priority too them
* It's hard for other people can not think like software developers
* Break down a problem to smallest parts
* Problem space -> solution space : example : it's too dark, so turn on the light -> Again it's hard for other people to understand software engineers
* Software engineers try always to find a solution for a problem. Other people can accept a problem without a solution and not try to find a solution and live with the problem.
* Bounded contexts in our mind : Emtional part and logical part
* A way to prioritize
* People can interact with each other in primary/secondary
* Event storming to understand the stories/use cases of a particular event which can be interpreted as bounded contexts with subsystems
* Let someone tell their story and that will be the ubiquitous language
* People from the outside don’t understand why we do what we do
* We’re always looking for solutions whereas others are willing to put up with their problems
* Perhaps writing out a decision or emotionally difficult situation in code would help us move through with the ideas

# ROTI

* 5 -> 13
* 4 -> 5
