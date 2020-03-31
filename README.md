# The EverestEngineering Manifesto

We want our company, [EverestEngineering](https://everest.engineering), to be a high performance team. Part of this is focusing on each other and our clients with an explicit goal of creating a human centric environment in which we are connected and supported. The other part is focusing on performance, doing the job and doing it well. The following principles and practices help us act together; read them and work on mastering them. 

This is our manifesto.

---


# Our culture

## Principles

### Empathy for others makes everything better

We need to understand each other and our customers to do our best work.

### Purpose and impact are why we come together

If we don’t know how we’re making a difference then we need to stop and ask why.

### Experimenting and exploring are the DNA of product development

Exploration and learning are inherent to our work. We can’t always know the right path or the outcomes of the work we do. We embrace learning as a pathway to certainty.

### Community is a platform for performance

We are all in this together and we perform best when we know we have the support of other people. Leadership is everyone’s job so we always take the time to make sure others are supported and connected.

### Everything is fractal

Details matter and so does the big picture. We need to zoom in and out to make the right moves. Coherence and alignment mean the principles by which we work apply to strategy, daily choices and the way we interact with each other and our clients.

### There is no one best way

Make mindful decisions in everything. Even this set of principles and practices are subject to challenge. Do the right thing. Or, when it’s a choice between hard decisions do the better thing above all else.

---

## Practices

### Make others successful

We believe that supporting others to be successful is the fastest way to high performing teams.

### Deliver accountability, receive autonomy

By being accountable, we are able to take on more autonomy and make more ambitious contributions.

### Transparency

We are radically transparent with each other and our customers. We build trust by giving full insight into our work and our way of working.

### Seek “better” in all things

We believe that continuous improvement in all things is a critical part of business in the modern age.

### Question everything but maintain a bias for action

Always know why you are doing things but don’t get stuck analysing and questioning. Keep moving forward.

### Find the nexus of science, art and craft

Different problems require different approaches. We seek the right balance across these disciplines based on the situation we are in.

### Bring joy to work

Joy brings energy and helps us work more effectively together.

### Work directly with clients

All team members have direct communication with our customers and end users. This is vital to gain a deep understanding of the domain and stakeholder needs.

### Tackle assumptions and ambiguity

Address assumptions and ambiguity early to reduce risk & improve efficiency. We challenge and ask questions to improve clarity and to set expectations.

### Ship frequently

Enable rapid feedback cycles by delivering often. Frequent shipping is, in turn, enabled by our engineering principles.

### Say no when you cannot commit

Saying yes is making a commitment to deliver. You damage your and our reputation if that commitment cannot be delivered.

### Speak up when something smells

Challenge when something doesn’t make sense or isn’t working. Accepting problems as the status quo contributes to the issue.

---

# Engineering Principles and Practices

## Principles

Our engineering principles are intended to provide guidance. Our aim is to apply these principles as default in the absence of a good rationale not to.

*Context is key in all matters*.

For instance, don’t attempt to deliver a fully industrialised system with AI and Slack integration when the goal is to deliver a tool for internal use that can be delivered by an off-the-shelf system. Doing so would consume the customer’s entire budget before any value can be delivered.

### Tackle complex design

“I have made this longer than usual because I have not had time to make it shorter.” — Blaise Pascal, translated from French.

Software becomes more complicated as an outcome of a system gaining functionality. Complexity, in contrast, is a result of poor design increases coupling, impedes understanding, increases risk and ultimately leads to failure.

### Favor simplicity

Simpler *techniques* are easier to learn, more flexible, and often more extensible than more complicated approaches. All things being equal, try simpler approaches first.

This holds especially true when working on fragile code bases. We must understand the subsystem well enough to figure out how to apply surgical precision to do less work and to limit risk. Strive to limit the blast radius of your changes.

### Stand on the shoulders of giants

We use well supported and battle tested open source libraries rather than implementing our own solutions. This avoids wasted effort due to duplication and allows teams to focus on their prime purpose.

We contribute back to open source projects when opportunities arise so as to build self worth, promote community and enhance our reputation.

### Reflect and improve

We seek to continuously improve ourselves and our clients by looking for opportunities to remove friction and address deficiencies in processes and tooling.

Change is difficult for both individuals and organisations; it takes effort to change deeply entrenched habits. Forcing change on ourselves and our customers risks creating resistance and resentment if people are not open to it. It must be approached gently and with empathy.

Accept that change may not be possible.

### Autonomous teams

Our teams are driven by purpose with a responsibility to deliver value to customers. We believe that this requires them to be in control of their own destiny with full ownership of their deliverables and methods of operation.

Teams are free to pick tooling and processes appropriate to the context of the customer and the work. New ideas are evaluated with curiosity yet tempered with caution.

Ownership extends beyond just building software and includes deploying and operating it in production. Teams therefore have both the license and the accountability to work at a level of quality that gives end users (and themselves) great outcomes.

### Cultivate a beginner’s mind

Regularly [empty your cup](https://wiki.c2.com/?EmptyYourCup) so that there’s room to learn new approaches. Be conscious that the patterns and solutions that you reflexively gravitate towards may not be suitable. Go slow to avoid rushing into wrong decisions. Avoid prejudgement and preconceptions.

Learn a wide range of techniques and practices to expand our individual and collective toolkits. Learn which contexts are the sweet spots for these techniques and practices.

### Automation

We automate whenever we find ourselves repeating tedious work. This includes provisioning of infrastructure and its monitoring, and the deployment of our software.

---

## Practices

Enablers of our engineering principles.

### Tackle complexity & develop deep understanding

We follow the principles of domain driven design (DDD). We share a ubiquitous language, an enabler of clarity in communication and understanding.

We aim for subtle designs around bounded contexts. Our code should be understandable by any person in a customer’s business and captures the knowledge of its people. Bounded contexts are a natural means by which we decompose large problems into smaller, more easily tackled ones that can potentially be assigned to multiple teams.

DDD requires every member of a software team to have a reasonable understanding of the domain. This is not accidental, it is an important factor in providing focus, clarity and a shared understanding that keeps teams aligned.

### Event sourced architecture

We prefer to use event sourcing whenever important business information must be captured.

This safeguards our customers and ourselves against errors and establishes a path for domain refactoring and introducing new features without loss of information.

### Decompose wisely

Microservices introduce complexity that may not be justifiable given the aims and the needs of our customers. We therefore aim to start new projects using monolithic approaches until a need for microservice extraction arises naturally. These monoliths must be modularised to avoid tight coupling in order to permit decomposition into microservices once the need arises.

Bounded contexts provide a natural boundary for microservice extraction.

Microservices should meet the following criteria for goodness:

- they are modeled around a business domain, i.e., a bounded context;
- their infrastructure, testing, monitoring, deployment and scaling is heavily automated;
- their implementation details are hidden by not exposing or allowing database level integration and by not sharing entities across domain boundaries;
- they are independently deployable, decoupled from each other and fault tolerant;
- they are highly observable and monitorable through log aggregation and correlation IDs;
- they are isolated from failures using circuit breakers, timeouts, and bulkheads;
- they are consumer oriented with documented APIs and contract tested.

### Clean code

We follow the notion that code should be self documenting through meaningful naming where classes *and* methods have single responsibilities. Classes are testable *and* tested at an appropriate level. We remove dead code. We prefer composition over inheritance. We know our craft.

### Clean campsites

We look for opportunities to clean up that which came before. We refactor when changes create tension in the code.

We validate that our features add value to users and reduce complexity by discarding those that don’t.

### Refactor safely

Refactoring to make software more testable, maintainable and ultimately extensible should be done with a safety mindset.

This requires analysis to understand the potential impact of changes and for the refactor to be broken down into atomic steps (commit points) so that risks are minimised.

If tests for the affected functionality are missing then these should be written first. If this is not possible given the state of a codebase then a detailed test plan should be created instead to ensure that manual testing can be applied rigorously in a repeatable fashion.

Verify that no regressions have been introduced at every step of the refactor by executing tests and updating tests as you progress. Further exploratory testing may be needed depending on the scale and risk of the refactor.

### Automated Testing

We design our *software systems* to be testable and we automate the testing of our work at the unit level, at integration points, its functionality and the infrastructure it runs on.

Automated tests are vital for any healthy software project. They reduce the likelihood of defects, assert that assumptions made by developers are not broken and that contracts are not violated when interfaces changes are made.

Automated testing accelerates development by giving developers confidence that their changes have no unexpected side effects. They are a form of executable documentation that describe the software’s expected behavior at different granularities. Adopting a testing mindset forces us to consider our implementation through different lenses and from different perspectives.

### Pattern language

We understand software design patterns to the point where it becomes natural to use them as a shared language. The use of design patterns should be tempered by need and the availability of language idioms to avoid the introduction of complexity.

### Continuous integration & deployments

We integrate continuously, creating rapid feedback cycles that give us confidence in our changes. We aim to be continuously deployable.

### Inclusiveness through accessibility

15% of the global population is affected by a disability. We seek to make our software more accessible to these 1 billion people by considering their needs in our UX designs and our technology choices.
