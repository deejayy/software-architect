# Feature-Driven Development: An Agile Alternative to Extreme Programming

(original article: https://www.cmcrossroads.com/article/feature-driven-development-agile-alternative-extreme-programming)

Summary:Feature-driven development (FDD) has the more traditional progression of a systems-engineering life cycle mode as compared to agile methods. It uses distinct phases in its iterations while still being highly iterative and collaborative. FDD does conduct up-front planning, design and documentation and relies very heavily upon domain modeling.

Many judge all of agile development based on what they know about extreme programming. Quite possibly this happens because that is all or most of what they've heard about agile development. I wish all of those folks, especially agile skeptics, would take a close look at feature-driven development (FDD), if for no other reason than it is an example of an agile method that is very different from XP. FDD is quite agile while still employing many of the traditional practices that agile skeptics are probably more accustomed to seeing.

For example, FDD has the more traditional progression of a systems-engineering lifecycle model and uses distinct phases in its iterations, while still being highly iterative and collaborative. It conducts up-front planning, design and documentation and relies very heavily upon domain modeling (including "color modeling" with UML). FDD also uses feature teams with chief architects/ programmers and traditional code-ownership and code-review, as opposed to pair-programming and refactoring.

## A Whirlwind Tour of FDD

FDD grew out of the method initially described by Peter Coad and Jeff DeLuca in chapter six of the book Java Modeling in Color with UML. It is a highly iterative and collaborative agile development method that focuses on:

- Delivering frequent, tangible, working results (about every 2 weeks)
- Domain-driven modeling and design
- Building quality in at each step
- Producing accurate and meaningful progress/status with minimal overhead and disruption for developers

As FDD is useful and desirable to managers, clients, and developers, DeLuca and Coad first employed it with great success on a large (1M+ lines of code) Java project for an international bank in Singapore. Since then, it has been increasingly used in other parts of globe with growing success, including parts of large companies like Sprint and Motorola. It is described more in-depth recently in books such as A Practical Guide to Feature-Driven Development and parts of Agile Management for Software Engineering. The five processes of FDD are:

- Develop an overall model
- Build a features list
- Plan by feature
- Design by feature
- Build by feature

These processes are described using traditional entry task verify exit-based process descriptions. FDD can be done by itself for substantial projects with modest-sized teams. For much larger projects and many teams, the overall FDD method fits quite nicely inside larger systems development models where market-level and system-level technical requirements have already been produced, and where some kind of independent V&V/QA activity takes place after development releases a production-candidate version of the software.

FDD can begin with high-level system requirements in place or with the domain modeling to build the initial shared understanding of what the overall system is and must accomplish. In either event, FDD has other roles that are more formally defined than many of the other agile methods, employing a chief architect, chief programmers, project managers (along with domain experts, developers (who serve as class-owners). It also has several other supporting roles such as build and release managers, to create an overall domain model, partition the system up into features, feature-teams and objects, and also develop, build and deliver the results in an incremental and iterative manner.

## Develop an Overall Model

To develop the overall domain model, the chief architect collaborates with the domain experts and developers to create an overall object-model using color modeling techniques and patterns. This is produced after a number of high-level walkthroughs of the scope and context of the system for each area of the problem domain.

After a walkthrough, they split into small groups of 3 to 4 people to produce object models for their respective portions of the domain,. They then return and review, then compare each other’s models for consistency, correctness, completeness and clarity. Eventually they arrive at a domain object model that captures and conveys the key abstractions and relationships of the system.

## Build a List of Features

With the initial domain model in place, the team then produces a list of features, where a feature is defined as a small, deliverable client-valued piece of functionality that is succinctly expressed using the format: action result object [parameters].

Or, more precisely, with the following grammatical structure: action {a|the} result {of|to|from|for|...} object [{with|for|of|...} parameters].

These are captured in traditional requirements documents, such as use cases or formal specifications, and referenced in the corresponding use cases and designs. Features are then grouped into subject areas, or subject domains, containing one or more feature sets of several individual features. Each subject area tends to take on the name of a core capability, such as subject-name management.

Feature sets within a subject area can be integration tested together and each feature within a feature set maps to a method in the domain model. In business systems, a subject area often maps to a business function or business domain, a feature set to a particular business process within that domain, and a feature to a particular business activity or business transaction within the overall business process/workflow.

Once an initial feature list has been compiled and collated into feature sets and subject areas, a system review is conducted with domain experts/analysts and other stakeholders to evaluate the list for correctness, completeness, and consistency.

## Plan by Feature

With a features list in place, the feature sets and features are analyzed and estimated, and the feature sets (or major feature sets, depending on the size of the system) are sorted into a sequence of time boxes for releases, major milestones (e.g., at least quarterly) and iterations that run at least monthly, but preferably every 2 to 4 weeks. The sequencing is based on customer assigned priorities, estimates, and technical dependencies among the feature sets. Feature sets are assigned to individual feature-teams, each led by a chief programmer. Classes from the domain model are then assigned to individual developers, who are responsible for the creation and maintenance of the class.

## Design by Feature and Build by Feature

Note that, thus far, the FDD process has been very different from other agile methods in that it does a substantial amount of up-front requirements, analysis, modeling, and planning for the entire system. FDD still tries to limit this to the minimally sufficient set of artifacts and keep them as streamlined as is convenient, but nonetheless performs this amount of up-front activity for requirements, modeling, and planning.

Once development is ready to start, the FDD feature-production machine kicks into high gear. Iterations of the sequence design by feature and build by feature begin churning out tangible working results at a frequent and steady pace of about every two weeks, or less.

- Chief programmers select small groups of features to form chief-programmer work packages (CPWPs), which are the basic units of integration with the other feature-sets and feature-teams.
- CPWPs are planned at regular intervals (no less than bi-weekly) and the classes involved are identified and the class-owners are assigned the corresponding development tasks.
- The feature team then collaborates to devise very detailed sequence diagrams and develops the interfaces and declarations for the corresponding classes and methods.
- A design inspection is held, and once successfully passed, the class-owners develop the code and unit-tests for their classes, then integrate their created/updated classes and conduct code inspections.
- When all updates are inspected and the chief programmer is satisfied with the results, the completed work-package and its features are promoted to the main build and the development and build processes are repeated for the next batch of features that make-up the next CPWP.

Notice that not all of the design is up front before implementation begins. The domain modeling work performed at the beginning fleshes out the overall shape of the problem domain and design model, but detailed design and dynamic interactions are done during the design by feature phase.

## FDD Best Practices

That is the essence of the FDD process. It has the ability to fit securely in-between a set of front-end system engineering process of creating initial high level requirements, back-end process of system build/package, and independent system-level testing. It also resembles more traditional plan-based development in its approach to requirements, design and planning. Throughout the FDD process, the set of key or best practices that form the gears of the FDD machine are:

- Domain object modeling (typically using color modeling, though not always explicitly stated) done highly collaboratively with a chief architect and domain experts
- Iterative/incremental development driven by feature-sets and features as the units of integration, build, and promotion
- Feature teams, led by chief programmers
- Individual code ownership, on a per-class basis
- Inspections and reviews for models/designs, feature-lists, and code
- Regular builds
- Configuration management
- Visible and meaningful reporting of status/results

The first five practices above are evident from the description of the five processes of FDD. The later three practices are a bit less apparent and all strongly relate to CM, so let's discuss the CM aspects of FDD in a bit more detail in the next section.

## FDD and SCM

Juha Kolska's 2003 report on Software Configuration Management in Agile Methods describes FDD as one of the few agile methods that explicitly mentions software CM (not just version control) and specific software CM practices as a key element. FDD contains the following practices that relate to configuration planning, identification and baselining, control, status accounting, and auditing and reviews:

- Requirements are explicitly captured and traceability is explicitly maintained from requirements to features, to model-elements, to source-code classes and tests
- Features are tracked by feature, with six milestones per feature: domain walkthrough, design, design inspection, code, code inspection, and promote-to-build (planned and actual dates are tracked)
- Features and feature-sets have status and progress visibly reported to the development team, to project/program leads, and to stakeholders and upper management. FDD defines the content and format for each of these different types of status-accounting reports
- New requirements and features are subject to explicit change-control once development plans are made and development begins
- Change authorization happens by allocating feature sets to feature teams, assigning features (and CPWPs) to chief programmers, and assigning individual owners to control all source-code changes to individual classes/modules.
- Regular build and integration plans are made and monitored using CPWPs that are then promoted to the main build.
- CPWPs are more than just a build or a branch/label. They contain all the information necessary to perform CM audits on the promoted build, such as unique identification of each work-package; completed line-items for the status of each delivered feature; outputs from the tasks defined in the task-descriptions of the feature-development plan; lists of all the deliverables in each work-package.

It should be noted that FDD does not specify the precise content of CPWPs.

- Each feature team uses a feature team integration area (an integration workspace and/or a feature-team integration branch) to base their current in progress work of the appropriate main build version, and to develop, test, and promote changes and work packages from the feature team area to the main build.
- Formal design reviews/walkthroughs and code-inspections are required and tracked before the design/code is promoted to the next level of development readiness.
- The use of both change tracking and version control tools is mandated for carrying out the CM-related activities of FDD.

Notice how FDD embraces, rather than eschews, documentation and traceability while still taking great strides to keep it as light and simple as possible. The feature-lists and detailed domain model are the enabling mechanisms for traceability and status reporting. They also make substantial use of tools and technologies to automatically track and report status/progress of features.

In some ways, FDD attempts to use feature sets and features as configuration items not merely for the functional requirements baselined, but for the development and product baselines and configurations. Organizing and aligning the work and work-packages along feature-boundaries vastly simplifies and facilitates traceability and status accounting/reporting.

## FDD and Color Modeling: The Four Color Archetypes and Their Grammar

Coad's Color Modeling method describes four basic archetypes for the kinds of objects that participate in an object-oriented domain model:

- The moment interval archetype: These are events (an important moment in time) and transactions (an important interval in time) that are the context or backdrop for important system operations and user-interactions. Examples might be a sale, a purchase order, opening/closing an account or withdrawing/depositing to or from an account. They are similar to the states, transitions, and activities in a traditional state-model diagram. Moment interval classes and objects are depicted in UML color modeling diagrams using the color pink.
- The role archetype: A role is a particular way that an actor or an agent (a party, place or thing) participates in an interaction with the system. Role objects are depicted in UML color models with the color yellow.
- The catalog entry description archetype: A description is quite simply a catalog-like entry that classifies or labels an object. Such objects typically represent some abstract collection of values that catalog or classify all objects of their type. Descriptions provide behavior to access information about their characteristics, but they do not, by themselves, change the way the system behaves. They provide structured information but no real overall functionality to the system. They don't do much of anything, they just exist and have attributes and characteristics that need to be used by the system. Description objects are blue in a UML color model.
- The party, place or thing archetype: These are objects that are uniquely identifiable entities that may play different roles in initiating, influencing, or realizing the results of system behavior/functionality. These are made green in UML color models.

These different archetypes from the basic grammatical elements of a sentence that describe a feature or requirement of the system: a subject comprised of a noun (or pronoun) and any descriptive adjectives; and a predicate that consist of a verb (action), an object (or complement) that receives the action of the sentence, along with any descriptive modifiers or qualifiers.There are some other basic color modeling rules that are pretty much the visual equivalent of grammatical rules for the valid and invalid ways of connecting these archetypes together in a domain model. The colors used in the model help make it very easy to see when correct grammatical structure and semantics are and are not present in each part of the model.

## The Domain-Neutral Component (DNC) Pattern

When the different archetypes are put together according to these basic grammatical rules, a resulting structure is a domain neutral component. The domain-neutral component is a particular structural pattern of interactions between archetypes in a sentence that recur over and over again throughout all systems. It has a mostly symmetrical shape, and occurs at all levels of scale within a system (fractal-like in nature).

These domain-neutral components are the higher-level building blocks (components) of the system: they represent business flows and plug in to each other in predictable ways. They also embody a traceable and transparent mapping between features, designs, and code in an FDD project. When a particular instance of a domain-neutral component is created for a particular part of the system, it is sometimes called a domain specific component. Numerous kinds of domain specific components recur throughout many different products and programs within the same domain, and their essential essence may be catalogued and reused as a domain specific component patterns.Domain specific components can themselves be connected to other such components in commonly recurring ways, and the result can be called a compound component. Each component takes on a characteristic shape and the commonly recurring object types and extension points.

The Java Modeling in Color with UML book defines 60+ enterprise component models and 10+ compound components representing patterns that can be used, extended, tailored, and applied to a variety of systems and domains. It should be noted that Color Modeling is not explicitly required in order to do FDD. There are, however, those who feel it is an implicit part of FDD as originally put forth by DeLuca Coad. They would liken doing FDD without consistently applying color modeling, to doing XP without consistently applying refactoring. The color modeling patterns impose a structure and semantics on the model that encapsulate and separate concerns, and isolate and insulate features for parallel work and integration. The resulting code often needs little or no significant refactoring (restructuring). See the following sources for more resources on color modeling:

- Wikipedia page on UML Colors
- Arguments about Color, by Daniel J. Vacanti
- UML Color Modeling with Archetypes

## FDD is Football-Driven Development (and XP is Rugby)

When I first heard about FDD and saw an overview presentation, my initial reaction was that it didn't look very agile to me. Other than the fact that it used iterative development, everything else about it resembled more traditional plan-driven approaches with Waterfall/V-model phases, apparent elements of CMM, and formal ETVX-based process descriptions. I asked if others had the same impression. Several did, but Jim Highsmith chimed in saying he has seen it live and in person, and that it is, indeed, agile. He said that what makes it agile for him, besides the iterations, is the intense focus on collaboration when he has seen FDD practiced.

Bill Wake has a nice review of Nonaka and Takeuchi's book The Knowledge Creating Company. He describes how the book compares a relay race with what we call waterfall and how something else they describe (that is very scrum-like) is more like rugby. This is the book that inspired the scrum method after all! The book also goes on to explain how the authors feel it is possible to combine the best of both, and liken the result to American football.

From this perspective, FDD is an agile method that is more like American football than like rugby. This explains why many proponents of other agile methods perceive FDD as very waterfall-like, document-heavy, and command and control as opposed to barely sufficient, self-organizing, and emergent.

XP, Scrum, Crystal, Agile modeling and most other agile methods (except possibly DSDM) are more like rugby. They are also predominantly code-centric rather than model-centric in that they regard the source-code as the primary artifact for disseminating system knowledge. In FDD, the domain model is the primary artifact for disseminating knowledge of the system. From an XP-based perspective, this is an alien concept and would suggest that XP practices might translate to model-centric practices as follows:

- Test first coding would be test-first modeling: Some of the basic FDD domain/color modeling grammar rules serve this purpose.
- Pair programming would be pair modeling: FDD actually does domain modeling as a collaborative team wide activity led by the chief programmer/architect.
- Refactoring would be behavior preserving transformations of a model's structure rather than of the code: Many of the color modeling patterns do just that.

Those parts of FDD are actually highly iterative and collaborative and, indeed, quite agile. The seemingly less-agile aspects of FDD comes into play when the model is translated into code using formal inspections and reviews, strict code ownership, very little refactoring, and significant documentation for feature requirements and design. Some might argue that FDD also lacks test-driven development, even though FDD places a string emphasis on testing and unit-tests.

These are the tradeoffs that FDD makes in the particular way it chooses to be more like American football rather than rugby, when it makes the choice to treat the domain model as the primary knowledge artifact rather than the source code. It's a different way of getting there, and it is very agile in the way it develops the model, but looks very plan-based in the way it transforms domain models into source code. The first step an XP-er or Scrumm-er needs to take in order to understand it is to temporarily suspend their belief that the code is king and imagine it might be possible if the domain model were king instead.

FDD is an agile method that treats the model as if it was the source code for nearly all but the implementation details of individual classes. In FDD, the domain model is valued over documentation, and it is also valued over the source code (which must be written under closer control/supervision than with XP/scrum). The source code is still valued, but the model is valued more, and it is a much more visual way of communicating system information to more than just programmers.

For some interesting and profoundly insightful and practical extensions of FDD that tie it together with other process improvement methods like Lean, the Theory of Constraints, and Six Sigma, I strongly recommend taking a close look at the work of David Anderson, author of Agile Management for Software Engineering. In particular, his paper and presentation on Feature-Driven Development: Toward a TOC, Lean and Six Sigma Solution for Software Engineering.
