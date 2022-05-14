# 8 reasons why Model-Driven Development is dangerous

(original article: http://www.theenterprisearchitect.eu/blog/2009/06/25/8-reasons-why-model-driven-development-is-dangerous)

## 1. MDD actually introduces a lot of rigidity 

If you’re used to programming everything by hand, MDD can be quite rigid. The goal of MDD is to ‘program’ on a higher level of abstraction. This means that you have to specify less and generate more. However, this also means that you can’t change every little detail you want. It is, for example, often the case that generated graphical user interface are inflexible and they all look like each other.

## 2. Models are only flexible where flexibility has been designed

The problem with using models to directly drive the engineering of software is that they are far from flexible. First, you are limited by the kind of Model Driven Engineering tool you use. Second, you’re only flexible in the parts of the solution covered by the used Domain-Specific Languages. The higher level the DSL the more commonalities are ‘hard-coded’ in the framework or engine you use. Third, sometimes models are made flexible at predefined points by lower level expressions or languages. That’s nice, but hopefully it is exactly done at the points you’ll need it.

## 3. The roles of project members are quite different

You need to be aware of the fact that the roles in Model-Driven Engineering are different from the roles in traditional development. The real technical or programming part is mostly moved to the ‘meta-team’ building the model-driven software factory. Building the solution is done by so-called business engineers instead of programmers. These people need to understand the business (like e.g. traditional functional designers) but they also need to express the knowledge they gather in a formal model. People able to do both these things are quite rare.

## 4. The modeling environment doesn’t always support version control

If you have experience with building (enterprise) software applications I guess you’re using a version control system. If not you should go and read this nice explanation. Existing version control systems work very well for textual programming languages. However, versioning of graphical models is a far less researched field. Most existing modeling and model-driven tools don’t include a full featured versioning system. That’s a pain when working with large teams.

## 5. The modeling tool/approach is "almost" finished at project start

The famous word "almost" is pitifully used a lot when talking about how far the model-driven software factory is finished at the start of a project. People building a model-driven software factory using DSL tools will have a lot of fun during the process. However, if the factory isn’t finished and tested in practice before you are going to start a big project you will have a huge risk! If you’re not scared by this article to use MDD, at least use a proven tool/approach!

## 6. The requirements team needs to understand what is allowed and what not

In point 1 and 2 I pointed at the rigidity and inflexibility of MDD. This is mostly dangerous from a technical perspective. However, it is even more dangerous when the requirements team, i.e. the people talking with the customer, don’t understand the limitations of the used tool/approach. In the ideal situation, the people talking with the customer directly translate their knowledge in executable models. However, in big projects you often see a separation in two roles. As in traditional development this can lead to a gap. This gap can become a nasty problem if the requirements team doesn’t understand the limitations of the tool/approach. For example, the requirements team reaches a consensus with the customer on a certain part of the graphical user interface (let’s say a form), while it isn’t possible to build that form with the model-driven tool without a lot of custom handiwork.

## 7. MDD is sold to the customer, but the team has no experience

While MDD is becoming more popular, customers start to ask for model-driven solutions. Actually I think MDD will become a hype (again!) very soon, and as with each hype everybody will start sticking the MDD label on their products. Doing a project in a model-driven way with an inexperienced team can lead to at least two problematic situations. First, the solution will not be build on time and it will not fulfill the customers’ expectations due to most of the issues mentioned in the previous points. Second, big chance the end product isn’t as easy to change as you expect from a solution built using a model-driven approach, due to misuse of the tool, not knowing its limitations, or due to using immature tools.

## 8. Innovation distracts

Last but not least, MDD is dangerous because innovation distracts. People tend to focus on the new tool they are using with all its cool features. Even more, people will start bragging about the great advantages they have with the new technology, in the end forgetting the projects objectives. Experiments have been done actually showing this behavior of project teams starting to use new innovative tools. The important lesson: don’t forget your project management, your process, and all other things you need beside the tool or technical approach you use!
