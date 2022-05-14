# An Introduction to Feature-Driven Development

(original article: https://dzone.com/articles/introduction-feature-driven)

Feature-Driven Development (FDD) is one of the agile processes not talked or written about very much. Often mentioned in passing in agile software development books and forums, few actually know much about it. However, if you need to apply agile to larger projects and teams, it is worthwhile taking the time to understand FDD a little more

The natural habitat of Scrum and XP-inspired approaches is a small team of skilled and disciplined developers. It remains a significant challenge to scale these approaches to larger projects and larger teams. Some have been successful but many have struggled.

Feature-Driven Development (FDD) invented by Jeff De Luca is different. While just as applicable for small teams, Jeff designed FDD from the ground up to work for a larger team. Larger teams present different challenges. For example, a small team of disciplined and highly skilled developers by definition is likely to succeed regardless of which agile method they use. In contrast, it is unrealistic to expect that everyone in a larger team is equally skilled and disciplined. For this and other reasons, FDD makes different choices to Scrum and XP in a number of areas.

In the first part of this two-part article, we briefly introduce the ‘just enough’ upfront activities that FDD uses to support the additional communication that inevitably is needed in a larger project/team. In the second part of the article, we cover how the highly iterative delivery part of FDD differs from Scrum and XP-inspired approaches.

## Iteration Zero:Getting Set to Deliver

Most experienced agile teams are familiar with the concept of an iteration zero, a relatively short period for a team to put in place what they need to start delivering client-valued functionality in subsequent iterations. Despite general acceptance within the agile community that some form of iteration zero is a pragmatic necessity on most projects, neither Scrum nor eXtreme Programming formally have much to say about it.

In contrast, an FDD project is organized around five 'processes', of which the first three can be considered roughly the equivalent of iteration zero activities. FDD does not use the term, iteration zero. It calls these three ‘processes’ initial project-wide activities.

Each of the FDD processes is described so that it can be printed, in a typical-sized font, on no more than two sides of letter-sized paper. The most recent versions of the FDD processes are available from the FDD section of the Nebulon website, but very briefly an FDD project:

> … starts with the creation of a domain object model in collaboration with Domain Experts. Usinginformation from the modeling activity, and from any other requirements activities that have taken place, the developers go onto create a features list. Then a rough plan is drawn up and responsibilities assigned. Now we are ready to repeatedly take small groups of features through a design and build iteration that lasts no longer than two weeks and is often much shorter, sometimes only a matter of hours.

## FDD Process #1: Develop an Overall Model

For many who have escaped from the perils of large, upfront analysis and design phases to the freedom and discipline of Scrum and eXtreme Programming-inspired approaches, the idea of developing a domain object model at the start of a project is controversial. In FDD, however, the building of an object model is not a long, drawn-out, activity performed by an elite few using expensive CASE tools. The modelers do not format the resulting model into a large document and throw it over the wall for developers to implement.

Instead, building an initial object model in FDD is an intense, highly iterative, collaborative and generally enjoyable activity involving ‘domain and development members under the guidance of an experienced object modeler in the role of Chief Architect'. FDD Process #1 describes the tasks and quality checks for executing this work, and while not mandatory, the object model is typically built using Peter Coad's modeling in color technique (modeling in color needs an introductory article all of its own).

The idea is for both domain and development members of the team to gain a good, shared understanding of the problem domain. It is important that everyone understands the key problem domain concepts, relationships, and interactions. In doing so, the team as a whole learn to communicate with each other and start to establish a shared vocabulary, what Eric Evans calls a Ubiquitous Language [Evans]. The object model developed at this point concentrates on breadth rather than depth; depth is added iteratively through the lifetime of the project. The model is, therefore, a living artifact. Throughout the project, the model becomes the primary vehicle around which the team discusses, challenges, and clarifies requirements.

## FDD Process #2: Build a Features List

With the first activity being to build an object model, some may conclude FDD is a model-driven process. It is not. While the model is central to the process, an FDD project is like a Scrum or eXtreme Programming project in being requirement-driven. Small, client-valued requirements referred to as features drive the project; the model merely helps guide. Formally, FDD defines a feature as a small, client-valued function expressed in the form: `<action> <result> <object>` (e.g., 'calculate the total of a sale'). By small, we mean a feature typically takes 1-3 days to implement, occasionally 5 days but never 10 or more days to implement.

Unlike Scrum and eXtreme Programming that use a flat list of backlog items or user stories, FDD organizes its features into a three level hierarchy that it unimaginatively calls the feature list. Larger projects/teams need this extra organization. It helps them manage the larger numbers of items that are typically found on an FDD features list than on a Scrum-style backlog.

To define the upper levels in the feature list hierarchy, the team derives a set of domain subject areas from the high-level breakdown of the problem domain that the domain experts naturally used during the object modeling sessions. Then within these areas, the team identifies the business activities of that area and places individual features within one of those activities. Therefore, in the features list we have areas containing activities that in turn contain features.

In practice, building the features list is a formalization of the features already discussed during the development of the object model. For this reason, lead developers or Chief Programmers can perform this task using the knowledge they gained during the modeling (FDD refers to lead developers as Chief Programmers in honor of Mills/Brooks idea of 'surgical teams'). Other members of the modeling team including the domain experts provide input to, and verification of the list as necessary.

Not only does this avoid the problems often encountered when customers/domain experts that are unused to doing this sort of formal decomposition try to do it, it provides another level of assurance that the Chief Programmers do understand what is required.

In addition, the ubiquitous language the model provides helps phrase features consistently. This helps reduce frustration in larger teams caused by different domain experts using different terms for the same thing or using the same terms differently.

## FDD Process #3: Plan by Feature

The third and last of the iteration-zero-style FDD processes involves constructing an initial schedule and assigning initial responsibilities. The planning team initially sequence the feature sets representing activities by relative business value. Feature sets are also assigned to a Chief Programmer who will be responsible for their development. At the end of this process, each Chief Programmer effectively has a subset of the features list assigned to them. For a Chief Programmer this is their backlog or ‘virtual inbox’ of features to implement.

The planning team may adjust the overall sequence of feature sets to take into account technical risk and dependencies where appropriate. In larger development efforts, the dependencies that have an impact on the sequence may be purely technical in nature but are just as likely to revolve around which feature sets are assigned to which Chief Programmers, and as we shall see, which classes are owned by which developers.

FDD also departs from traditional agile thinking, in that it chooses not to adopt collective ownership of source code. Instead, it assigns individual developers to be responsible for particular classes. The initial assignment of developers to classes takes place during this planning process.

The advantages of individual class ownership are many but include the following:

- There is someone responsible for the conceptual integrity of that class. As enhancements are made, the class owner ensures that the purpose and design of the class is not compromised.
- There is an expert available to explain how a specific class works. This is especially important for complex or business-critical classes.
- The class owner typically implements a required change faster than another developer that is not as familiar with the class.
- The class ownerhas something of his or her own that he or she can take personal pride in.

In addition, it can become tricky to maintain true collective ownership of code as team sizes increase. In my experience, over time, the same developers naturally gravitate to working with the same parts of the code again and again and effectively take ownership of them.

Of course, there are issues with code ownership. eXtreme programming chose collective ownership to solve real problems. We do not want delivery of features held up because one developer is waiting a long time for other developers to make changes. However, instead of allowing any pair of developers to edit any source code files whenever they think they need to, FDD address the problem differently.

Firstly, in FDD, class ownership implies responsibility not exclusivity. A class owner may allow another developer to make a change to a class they own. The big difference is that the class owner is aware of, and approves of, the change and is responsible for checking that the change is made correctly.

The other strategy that FDD uses to enable effective feature-by-feature development with individual class ownership is the idea of dynamically formed feature teams but that is a topic best postponed to the next part of this article.

As with other agile approaches, planning in FDD is not a ‘chisel in stone’ activity. Indeed, the planning team reviews and modifies the assignment of feature sets to Chief Programmers and classes to developers as often as necessary throughout the project. In addition, the planning team does not always assign owners to all the domain classes at this time and more classes inevitably emerge as the project progresses. These will get owners later. Again it is a ‘just enough’ activity.

## Conclusion

One of the biggest challenges in any iteration-zero-style or upfront activity is knowing when to stop. It is not about big design upfront (BDUF). It is about doing Just Enough Design Initially (JEDI). We are not looking for a model and set of requirements that have every t crossed and i dotted. We are looking for initial, broad understanding, enough of a foundation to build on, recognizing that the model, features list and plan are living artifacts not formal documents set in concrete.

While there are rules of thumb and general guidelines, recognizing and stopping at ‘just enough’ is not easy and requires both discipline and experience. It is for this reason, that an experienced object modeler in the role of Chief Architect guides the modeling team, and an experienced Development Manager and Project Manager guides the planning team. After all, with no apologizes for the awful Star Wars pun, one cannot become a JEDI master overnight!

These three processes are not all the activities that may take place in iteration zero. Some projects may also need to evaluate, select, install and configure tools, set up development, testing and integration environments, decide on infrastructure components, etc, etc. Given the almost infinite variation here, the five FDD processes do not attempt to specify anything for these tasks. Instead, FDD assumes that ‘just enough’ is done here to enable the team to start delivering frequent, tangible, working results as it executes processes #4 and #5 for each feature. This is what we will cover in the second part of this article.

