# ReDeploy 2018 Conf
## TL;DR
 First edition of a conference I hope will be held regularly on the topic of resilience.

Systems resilience, but mostly human resilience and how to start to approach the field of Human Factors and Ergonomics for the world of Software Cloud engineering.

## The longer  version

While short and small, this first edition of ReDeploy touched a lot of aspects of resilience. From the technical side on how to improve systems throughz experimentation and the introduction of chaos in a system[6][13] . Community, psychology even neurology were topics of discussion trying to paint a picture of how building more resilient systems should take into account.

There were no real answers, there were many unanswered questions, but knowing what to look for is what can allow discovery of solutions. 

### The technical

On the technical side talks from the Netflix folks[][6], Jhon deer[], Stripe, and more showed example architectures and how to leverage systems like the now famed chaos monkey that allow you to build failure as a constant to your system in order to root out potential  surprises if not weeknesses. 

Breaking a system was not meant  as a means to fix, the intent was to know what kind of damages would then be exerted on the said systems and allow the ops and engineering teams to figure out what was considered acceptable or desired. Basically showing us ways to suss out resilience out of a system.

### Communities

While we were presented with a very concrete case of how pivoting can be key to resiliency and how sometimes pausing all work for an extended time may seem catastrophic, doing so may be the only way out. 

The case was also made that strong communities, psychological safe communities augment the resilience of the individuals. Making failures known,  and also making the consequences of failure have no ill effect, on. Careers or otherwise, is an important aspect of fostering psychological safe environments. 


### Psychology & Neurology

Some presenters showed how our biology can work against us blind us even, by overstimulation[] . And how no matter how we wish we operated, psychological biases can hamper our ability to be resilient participants of systems.

[more?]


## Take aways

While I’ve been an adamant herald of documentation, this conference has offered me a different perspective on the topic and may have enlightened me on the perspective that documentation being hard to maintain. One presenter (John Alspaw) posited we should try to view complex systems not  as tools we look at through windows trying to decipher what they do and how they work, but to try to view and build them as a team member offering information to aid human operator make proper decision.

Luckily for us this is an active field of research, not yet fully. Applied to problems in the cloud space but still there are enough material to start the conversation and look for potential avenues of solutions.

For example we tend to monitor platform instrumenting for what we think will go wrong. Rarely do systems tell us exactly was is wrong they usually present us with crumbs of information we need to piece together like a puzzle and more often than not require us to have archeological talents in order to reveal the information from the layers of logs. Deciphering what is important from what is not usually requires experience. Which if we are to build more and more complex systems will not always be possible.

Proper context at the error level will be key to start making better system. Also adding recommendations on what can be done within a given context will also help lessen operator burden when issues arise. An attempt at something in those lines was mentioned: Nagios Herald, which augmented alerts with context allowing the receiver to have enough context to make an actionalbe decision about the alert. 

In short complex systems should not force the humans to adapt to them, they should be designed to adapt to the human as they are tools and the humans are the operators.

### The future, a new hope

The world of software development has examples of software that in the face of error attempt to aid the user, best examples in the realm of compilers are the RUST and Elm. Concerning cloud software like CloudFoundry(CF) or Kubernetes(K8), there may not be one tool that  will present itself as a solution, it may just be that we need a different way of building or instrumenting those systems. Or we may need systems that can prove/verify themselves and annotate their failures with proper context that will make sense to a human. If CF and K8 are cloud level Operating Systems(OS), maybe constructing cloud compilers and valdiators are they way to start getting to a better if not in between ideal.


# Links

[1] In the Center of the Cyclone: Finding Sources of Resilience — [John Allspaw (@allspaw) ](https://re-deploy.io/2018/speakers/#john-allspaw) 

[2] Availability, Latency and Cost: Withstanding Regional Outages - [Aaron Blohowiak (@aaronblohowiak)](https://re-deploy.io/2018/speakers/#aaron-blohowiak) 

[3] Resilient Systems Require Resilient People —  [Hannah Foxwell (@hannahfoxwell)](https://re-deploy.io/2018/speakers/#hannah-foxwell) (From Pivotal)

[4] When Will They Ever Learn? - [David Blank-Edelman (@otterbook)](https://re-deploy.io/2018/speakers/#david-blank-edelman) 

[5] Recognizing Zombies, Black Holes & Tribbles Before You Get Eaten: Techniques to Avoid Cascading Failure —  [Avery Regier (@averyregier)](https://re-deploy.io/2018/speakers/#avery-regier) 
 
[6] Chaos Engineering: A Step Towards Resilience — [Nora Jones (@nora_js)](https://re-deploy.io/2018/speakers/#nora-jones) 
 
[7] The Human Nature of Failure and Resiliency — [VM (Vicky) Brasseur (@vmbrasseur) ](https://re-deploy.io/2018/speakers/#vm-(vicky)-brasseur). [Slides](https://ia601504.us.archive.org/35/items/redeploy2018-failure/03-redeploy2018-failure-with_speaker_notes.pdf)

[8] The Origins of Opera and the Future of Programming - [Jessica Kerr (@jessitron)](https://re-deploy.io/2018/speakers/#jessica-kerr) 

[9] Try Catch Blocks for your Distributed System — [Cecilia Deng (@cicikendiggit)](https://re-deploy.io/2018/speakers/#cecilia-deng) 

[10] Fight, Flight, or Freeze — Releasing Organizational Trauma - [Matty Stratton (@mattstratton)](https://re-deploy.io/2018/speakers/#matty-stratton) 

[11] Mindfulness at Work: A Way to Overcome the Overwhelm — [Lee Kussmann (@leekussmann)](https://re-deploy.io/2018/speakers/#lee-kussmann) 

[12] Out of Maintenance Mode: Refactoring a Community - [Matt Broberg (@mbbroberg)](https://re-deploy.io/2018/speakers/#matt-broberg) 

[13] How our Security Requirements Turned Us into Accidental Chaos Engineers - [Paul Carleton (@paulcarletonjr) ](https://re-deploy.io/2018/speakers/#paul-carleton) 

[14] Operating at the Edge of the Envelope - [Laura MD Maguire (@LauraMDMaguire)](https://re-deploy.io/2018/speakers/#laura-md-maguire) 

# Software

[15] [GitHub - etsy/nagios-herald: Add context to Nagios alerts](https://github.com/etsy/nagios-herald) ]
[Introducing nagios-herald - Code as Craft](https://codeascraft.com/2014/06/06/introducing-nagios-herald/)

# reading list

[16] [Resilience Engineering Resources](https://github.com/adaptivecapacitylabs/Resilience-Engineering-Resources)

[17] [STELLA: Report from the SNAFUcatchers Workshop on Coping With Complexity](https://snafucatchers.github.io)

[18] [Human Factors & Ergonomics in Practice](https://www.amazon.com/Human-Factors-Ergonomics-Practice-Performance/dp/1472439252)

[19] [The Human Nature of Failure and Resiliency - reading list](https://www.zotero.org/groups/287407/failure/items?)

# Videos

[20] [Working at the Center of the Cyclone - Dr. Richard Cook - YouTube](https://www.youtube.com/watch?v=3ZP98stDUf0)

[21]() [Velocity NY 2013: Richard Cook, “Resilience In Complex Adaptive Systems” - YouTube](https://www.youtube.com/watch?v=PGLYEDpNu60)

[22]() [REdeploy 2018 - The Human Nature of Failure and Resiliency : Free Download, Borrow, and Streaming : Internet Archive](https://archive.org/details/redeploy2018-failure)
