# ReDeploy 2018 Conf
## TL;DR
 First edition of a conference I hope will be held regularly on the topic of resilience.

Systems resilience, but mostly human resilience and how to start to approach the field of Human Factors and Ergonomics for the world of Software Cloud engineering.

## The longer  version
While short and small, this first edition of ReDeploy touched a lot of aspects of resilience. From the technical side on how to improve systems through more experimentation and the introduction of chaos in a system[ link to. Chaos monkey] . Community, psychology even neurology were topics of discussion trying to paint a picture of how building more resilient systems should take into account.

There were no real answers, there were many unanswered questions, but knowing what to look for is what can allow discovery of solutions. 

### The technical

On the technical side talks from  the Netflix folks, Jhon deer, etc  showed examples of architecture and processes and systems like the now famed chaos monkey that allow you to build failure as a constant to your system in order to root out potential  surprises if not weeknesses. 

Breaking a system was not meant  as a means to fix, the intent was to know what kind of damages would then be exerted on the said systems and allow the ops and engineering teams to figure out what was considered acceptable or desired. 

While the tools and processes  

### Communities

While we were presented with a very concrete case of how pivoting can be key to resiliency and how sometimes pausing all work for an extended time may seem catastrophic, doing so may be the way out. 

The case was also made that strong communities, psychological safe communities augment the resilience of the individuals. Making failures known,  and also making the consequences of failure have no ill effect, on. Careers or otherwise, is an important aspect of fostering psychological safe environments. 

### Psychology & Neurology

Some presenters showed how our biology can work against us. Blind us even by overstimulation  [ talk more about the thrashing signals PTSD] . And how no matter how we wish we operated psychological biases can hamper our ability to be resilient participants of systems.

### Coping with failure

Coping with failure … ?

### What does it mean for Pivotal?

We had a pivot presenting, which leads me to believe that the conversation has or is already started internally 

We do share information, but we have a hard time making it dicoverable, we pretty much are in the experience business but have a hard time offering other means of teaching.

While I’ve been an adamant herald of documentation, this conference has offered me a different perspective on the topic and may have enlightened me on the adage concerning documentation being hard to maintain. John alspaw posited we should try to view complex systems not  as tools we look at through windows trying to decipher what they do and how they work, but to try to view and build them as a team member  offering information to aid human operator make proper decision.

Luckily for us this is an active field of research, not yet fully. Applied to problems in the cloud space but still there are enough material to start the conversation and look for potential avenues of solutions.

For example we tend to monitor platform instrumenting for what we think will go. Wrong, rarely do systems tell us exactly was is wrong they usually present us with crumbs of information we need to piece together like a puzzle and more often than not require us to have archeological talents in order to reveal the layers of logs important to the problem at hand and most often they require interpretation to be valuable. An attempt at something different was mentioned Nagios Herald, which augmented alerts with context allowing the receiver to have quality context to make a decision about the alert. 

### The future, a new hope

I hope to build systems that allow operators to be given more context when they break down.  The world of software development has examples of software that  in the face of error attempt to aid the user, best examples in the realm of compilers are the RUST compiler and ELM compiler.  NAgios herald is another attempt. 

The complexity of systems will only increase, there may not be one tool that  will present itself as a fix, they may just be that we need a different way of building systems, systems that can prove/verify themselves and annotate their failures with proper context that will make sense to a human


Mention nagios herald[ [GitHub - etsy/nagios-herald: Add context to Nagios alerts](https://github.com/etsy/nagios-herald) ]
[Introducing nagios-herald - Code as Craft](https://codeascraft.com/2014/06/06/introducing-nagios-herald/)

## Key take aways

Coping with failure (vmbrasseur)

Your task is uncertain because you can't know everything.

Because we think we know more than we really do, we have a tendency not to look around for potential (and potentially obvious) problems.
These are the "Unknown unknowns." It's not just a funny thing a politician said once: It's a legit psychological concept known as Latent Errors
These are the overlooked near misses
Look a lot like successes, simply because they haven't failed...yet

And that's because those latent errors have yet to meet their enabling condition
This is the trigger that turns a latent error to the dark side
Deepwater Horizon example: Oil rig tragedy in the Gulf of Mexico in 2010/
* Incorrectly followed cementing procedure -> (ergo) Escaping gas. Normally not a problem & the way it was usually done, anyway.
* Welding nearby, normally not a problem. Happens all the time on an oil rig
* Windless day <-- enabling condition
* Killed 11, injured 16 more, led to one of largest environmental disasters our countryʼs ever seen


We kinda suck at post mortems
Research shows we do a bad job at these. We prefer symptoms to causes.
We have a preference for blame, so we want a root cause (that almost never exists)
We suffer from selection bias: look at those things we prefer to rather than the hard stuff
Therefore we have a tendency to postmortem non-representative data sets
Part of that non-representative data set problem is we typically only post-mortem the things that went "wrong". This is called "negative outcome bias"
Only doing post-mortems on the "failures" means you never review those near misses. The things that went right, pretty much just by chance.
Which is to say, we ignore latent errors, and
We ignore complex process that led to a successful outcome
How can we minimize the impact of these tendencies?
✦ Pre-mortems
✦ Seek out latent errors
✦ Include different perspectives
Perform a pre-mortem, and specifically look for latent errors (among other things)
When you do the pre-mortem, get a skeptic or an "outsider" in the room & on your team
These people will ask questions that the team doesn't think to ask.

Research doesn't have very nice things to say about assumptions
Nearly every piece of research points to assumptions as a frequent contributor to failure
Why is that?
For starters, assumptions are usually based on incorrect or invalid information, including those aforementioned mental snapshots of the world
We then use these assumptions as a basis for a set of heuristics that we apply to the real world
For example: they're used to create estimates, which are rarely correct (for a variety of reasons, assumptions among them)
Research shows that we prefer to jump to the solution phase rather than take time in the problem definition phase.
Which means often we make assumptions about a problem that is itself an assumption
As you can imagine, assumptions based on an assumption are far from reliable, but we use them anyway.
We in technology like to say "fail fast," but that's impossible if you don't define the problem.
Without that, you don't know what success looks like, which means you also can't identify failure.
This leads to more failures and, even worse, zombies that failed long ago but never die.
So define the problem, list its requirements, do all those things you know you should do but don't.
As you consider the problem, treat each "requirement" as an assumption -> something to be questioned and confirmed
Now, it's important to question all assumptions, because (read slide)
Example: "We assume this will take 2 weeks but we need to confirm"
Research shows: No one hears anything after the "2 weeks", so we need to build cultures where verifying assumptions is the rule, not the exception
People claim they don't have the time to verify assumptions, but they do seem to have the time to work on the wrong thing for the wrong end users, then scrap it and start over later.
How can we minimize the impact of these assumptive tendencies?
✦ Take the time to define the problem
✦ Perform pre-mortems to list and verify all
assumptions
✦ Document everything
✦ Revisit assumptions throughout the process

Explicitly list all assumptions, challenge them
Gather risks & what-ifs
Document!
Build in checkpoints: Environment changed, assumption still valid?
Still need to assume? Or assumption converted to knowledge?

Now on to the final item on our list of factors contributing to failure: Humans
Research shows that humans are the leading cause of failure.
We can't exactly take humans out of the picture, but we can do something about their organisation and culture, each of which play a large role in contributing to failure.

Research shows, we're kinda arrogant, as species go.
We have a tendency to over-estimate the impact our actions can have.
We overestimate the things we can control or even the things we can simply influence.
This is called Illusion of Control.
While Illusion of Control has been around for as long as there've been humans
It was Ellen Langer, a psychologist at Harvard, who first named and published about it
Talked about these a bit earlier: Deepwater Horizon example
We think we can control everything, so we let down our guard and overlook latent errors
The thing is, if we look for & find them, we DO actually have the power to control latent errors. (Deepwater Horizon)
However, have almost no chance to control enabling conditions. They're out of our hands entirely. (we can't stop the wind from blowing)
We therefore cannot truly control the outcome of most situations, at best we can only influence them.
Another contributor to ignoring latent errors is a lack of psychological safety
Psychological safety is a complex matter, but one of its many benefits is that people feel safe pointing out oversights like latent errors.
If people fear retribution or punishment, they're unlikely to call attention to things like latent errors, which may make more senior or powerful people feel foolish.

One of the many contributors to psychological safety is the structure or organisation of your team or group.
It can affect the communication routes and the reaction or resistance to change required to prevent or iterate after a failure.

Is it organised into silos?
"These people design, those people develop, those other people test, that group deploys, those ones over there support"
But what if a process is contributing to failures?
When an org mirrors processes, then when a process needs to change the org may need to as well
Increases difficulty in changing the problematic process, so it may never change.

Experience comes for free. Learning does not.
Unshared failures are just experience of an individual, not shared learning, and therefore are of low value.
That's because experience comes for free. It just happens to us. Learning, however, does not.
We must share information about failures if we're to learn from it.


 If you have no reports about failures or problems, that's a warning sign.
It doesn't mean they're not happening. It just means they're being hidden, which is much worse.
People become afraid to try new things: innovation stifled
Another problem with punishment is that it prevents people from trying new things. Innovation slows down or even stops.
Not just the big Silicon Valley INNOVATION. The important everyday innovation also
Removing unneeded processes, streamlining others, trying out new ideas large and small
They all stop because people are afraid of what will happen if they fail.
This is a sign of a lack of psychological safety

Not sharing failures or pointing out latent errors can lead to them being seen as "normal" -> normalised deviance
Identified/labeled by Diane Vaughn: American sociologist; studied the Space Shuttle Challenger explosion
An example of latent errors, hiding right out in the open and intentionally ignored
Example: log files
Just one race condition away from catastrophe.
We're probably all familiar with another way that culture contributes to failure.
We humans have an unfortunate tendency, to push ourselves too hard. To try doing too much in too little time. To put in long hours, often unnecessarily.
This leads to a lot of problems. Attention slips. More reliance on untested assumptions.
Some of the best research in this area has occurred in hospitals. Lives have been saved by allowing people to work fewer hours.

Inability/reluctance to pull the plug (Sunk Cost Fallacy)
✦ Can't tell what 'done' looks like
✦ Project champions (reality distortion field) ✦ Lack of communication skills
✦ No exit plan

Studies show that humans have a hard time NOT seeing things through to the "end." This is related to the earlier finding that our brains prefer to work in serial rather than parallel.
Leads to zombie projects, shambling along consuming the brains of the team
Hard to tell whether your on the right path if you haven't set a destination
Group think, Deeply held belief that it will succeed: BLIND FAITH
* Lead us to continue to believe things even when facts show they're just not true
Not trained to deliver that sort of news properly.
Don't create a plan for what happens should a project fail. No safety net for the people. Particularly bad when there's no psychological safety.

Experience is automatic. Learning is not.
Through word & deed, encourage people to share their mistakes & failures
Learning develops intuition & skill
Example: Very senior technical staff aren't very senior because of their age. It's because "they've seen some shit, man."
They've experienced failure and have learned from it, developed intuition & skill.
Teaches you what doesn't work so you can avoid future failure.

Suggestion: Include truth-seeking people
Those who question "we've always done it this way" and other assumptions.

Designated "project skeptic"
"Outsiders" in post- and pre-mortems: from other teams and departments
Bring on truth-seeking people
TRANSITION!! Now, let's talk about how to make failure work in your favour...

And that's because of evolution
In life forms as in all things: No change is possible without some failures
Evolution is a constant series of "works for now" solutions
Experimentation should similarly be continuous if you'd like your business/ project to evolve

Nature of successful experiments
✦ Small & survivable
✦ Explicit success and failure criteria ✦ Have an exit strategy

Research shows that the best way to minimise, avoid, and learn from failure is to start talking openly about it and inspecting your failure environment
What sort of questions should you be asking of your project/team/ organisation?

Questions to ask
✦ What problem are we trying to solve?
✦ What problem is our end user trying to solve? ✦ What are our assumptions?
✦ Have we checked in on our assumptions?
✦ What are the possible latent errors?
Questions to ask (continued)
✦ What does "failure" look like?
✦ What is our exit strategy?
✦ What is our postmortem process?
✦ How does our organisation view & treat failure?
✦ Do we have a culture that provides psychological safety?



### Day 1
      
| sdfs | sfsd |
| - | - |
| sdfds | dfsdsds |

In the Center of the Cyclone: Finding Sources of Resilience — [John Allspaw (@allspaw) ](https://re-deploy.io/2018/speakers/#john-allspaw) 

Availability, Latency and Cost: Withstanding Regional Outages - [Aaron Blohowiak (@aaronblohowiak)](https://re-deploy.io/2018/speakers/#aaron-blohowiak) 

Resilient Systems Require Resilient People —  [Hannah Foxwell (@hannahfoxwell)](https://re-deploy.io/2018/speakers/#hannah-foxwell)

  

When Will They Ever Learn? - [David Blank-Edelman (@otterbook)](https://re-deploy.io/2018/speakers/#david-blank-edelman) 

Recognizing Zombies, Black Holes & Tribbles Before You Get Eaten: Techniques to Avoid Cascading Failure —  [Avery Regier (@averyregier)](https://re-deploy.io/2018/speakers/#avery-regier) 
 

Chaos Engineering: A Step Towards Resilience — [Nora Jones (@nora_js)](https://re-deploy.io/2018/speakers/#nora-jones) 
 

The Human Nature of Failure and Resiliency — [VM (Vicky) Brasseur (@vmbrasseur) ]( https://re-deploy.io/2018/speakers/#vm-(vicky)-brasseur)
    [Slides](https://ia601504.us.archive.org/35/items/redeploy2018-failure/03-redeploy2018-failure-with_speaker_notes.pdf)
Experience comes for free, learning does not.

## Day 2
## Friday, August 17th

The Origins of Opera and the Future of Programming - [Jessica Kerr (@jessitron)](https://re-deploy.io/2018/speakers/#jessica-kerr) 

Try Catch Blocks for your Distributed System — [Cecilia Deng (@cicikendiggit)](https://re-deploy.io/2018/speakers/#cecilia-deng) 

Fight, Flight, or Freeze — Releasing Organizational Trauma - [Matty Stratton (@mattstratton)](https://re-deploy.io/2018/speakers/#matty-stratton) 

Mindfulness at Work: A Way to Overcome the Overwhelm — [Lee Kussmann (@leekussmann)](https://re-deploy.io/2018/speakers/#lee-kussmann) 

Out of Maintenance Mode: Refactoring a Community - [Matt Broberg (@mbbroberg)](https://re-deploy.io/2018/speakers/#matt-broberg) 


How our Security Requirements Turned Us into Accidental Chaos Engineers - [Paul Carleton (@paulcarletonjr) ](https://re-deploy.io/2018/speakers/#paul-carleton) 

Operating at the Edge of the Envelope - [Laura MD Maguire (@LauraMDMaguire)](https://re-deploy.io/2018/speakers/#laura-md-maguire) 


# reading list
Chapter 29: SRE Cognitive Work  SRE Handbook 

[Resilience Engineering Resources](https://github.com/adaptivecapacitylabs/Resilience-Engineering-Resources)

[STELLA: Report from the SNAFUcatchers Workshop on Coping With Complexity](https://snafucatchers.github.io)

Human Factors & Ergonomics in Practice

[The Human Nature of Failure and Resiliency - reading list](https://www.zotero.org/groups/287407/failure/items?)

# Videos

[Working at the Center of the Cyclone - Dr. Richard Cook - YouTube](https://www.youtube.com/watch?v=3ZP98stDUf0)

[Velocity NY 2013:   Richard Cook, “Resilience In Complex Adaptive Systems” - YouTube](https://www.youtube.com/watch?v=PGLYEDpNu60)

([REdeploy 2018 - The Human Nature of Failure and Resiliency : Free Download, Borrow, and Streaming : Internet Archive](https://archive.org/details/redeploy2018-failure)