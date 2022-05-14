# 15 reasons why you should start using Model Driven Development

(original article: http://www.theenterprisearchitect.eu/blog/2009/11/25/15-reasons-why-you-should-start-using-model-driven-development/)

## 1. MDD is faster

In Model-Driven Development the model of a software application is specified on a higher abstraction level than traditional programming languages. This model is automatically transformed into a working software application by generating code or interpreting / executing the model. While the used model is on a higher abstraction level it is much smaller compared to the same model expressed in code. In other words: each element in the model represents multiple lines of code. Hence, you can build more functionality in the same time. See for example this comparison between Mendix and Java development. MetaEdit+, another MDD tool is told to be five times faster than traditional programming.

## 2. MDD is more cost-effective

MDD can be more cost effective. The first reason is that you have a shorter time-to-market because MDD is faster (see point 1). The second reason is that it is possible to do it at lower cost (i.e. with less people, non-specialists, increased quality, etc. – see the points that follow). This of course depends on the costs of learning the MDD approach and the costs to develop or buy the tool. It also depends on your business model. If you are used to selling programming hours your business will be affected by using MDD.

Changing and maintaining applications build using an MDD approach is also more cost-effective. It is easier to understand the behavior of an application by reading high-level models (see also point 6). Additionally it is faster to add functionality or change existing functionality using a high-level language.

## 3. MDD leads to increased quality

Because a software application is specified in a high-level model which is executed by an engine or transformed into code; the (technical) quality of the application depends on the generator or engine. Hence, the quality can increase a lot because we can let our best people work on the generator. Furthermore, all best practices we learn in projects can be included in the generator and will automatically be applied to projects build using the MDD tool. In case of buying an MDD tool the tool can contain even more best practices because it builds on the knowledge of all projects build by the MDD tool in the past.

## 4. MDD is less error-prone

Everyone having experience with delivering a new software application knows that testing costs a lot of time and expertise. MDD ensures that you can focus on testing the functionality of the application, i.e. acceptance testing. Technical problems are covered by testing the MDD tool. Think for example about infrastructure related problems or security leaks in the technology.

## 5. MDD leads to meaningful validation

Even the functionality itself is less-error prone when using an MDD approach, because meaningful validations can be executed on the high-level models. When using traditional programming languages you will have some syntax checking in your IDE and maybe even some static code analyzers. However, due to the generality of the programming language this does not really help you to avoid functional errors.

When using an MDD approach domain-specific validations can be executed at design-time. The resulting error message can be domain-specific too. See for example this article on the static verification of a textual DSL. In the Mendix modeling environment we use real-time consistency checking to ensure that the model is consistent and can be executed by the runtime environment.

## 6. MDD results in software being less sensitive to changes in personnel

When using an MDD approach the resulting software will be less sensitive for changes in personnel. As you do not need a technical specialist anymore to build software you can draw from a larger pool of people. Furthermore, if someone joins a project it is far easier to understand the high-level model of the software application compared to trying to understand the behavior of the application by reading source code.

## 7. MDD empowers domain experts

MDD enforces a separation of concerns and skills. Domain experts can focus on modeling the domain, while technical specialist focus on building the tools needed for MDD (see also point 8). Building complex applications is not only for ‘elite’ programmers anymore. MDD can introduce suitable notations (e.g. textual, graphical, tabular) to empower domain experts. They can model a software solution by translating their knowledge of the domain into a high-level model.

## 8. MDD lets advanced programmers focus on the hard stuff

In MDD, advanced developers do far less repetitive work. They can focus on the creative aspects of their work. They can focus, for example, on building the MDD tools. They can also mentor junior developers or domain experts, or they can pick up the hard parts of application building. A domain expert can for example model the graphical user interface, processes and business rules. The integration parts of the application (using webservices, API calls, database integration, etc.) can be too difficult or technical for domain experts. Programmers can focus on this kind of tasks as part of the project team.

## 9. MDD bridges the gap between business and IT

Business-IT alignment is a returning item when talking about building software. MDD can bring business and IT closer together in the following ways:

- Domain experts (or business analysts) are directly involved in the development process (see also point 7).
- IT (a software application) is defined on a much higher-level. The models are as much as possible declarative and defined in domain concepts.
- As MDD is faster (see point 1) software can be build in shorter iterations and therefore have a better fit-for-purpose (due to fast feedback of the business / end-users).
- By defining explicit transformations between a model of an organization and a model of an IT system. For example by using a framework for model-driven SOA.

## 10. MDD results in software being less sensitive to changes in business requirements

One of the problems of software development is that business requirements often change faster than the supporting software systems. In a previous article I stated: it is questionable whether enterprises can actually maintain a focused strategy long enough to align their core business processes with IT. The current dynamic business environments do not give enterprises that time.

However, MDD can provide a solution because it makes software development faster (see point 1), it also leads to easier to change applications (due to point 2 and 6). If there is an explicit link between business requirements and the model of the software application it is even possible to propagate part of the changes automatically (see also point 9).

## 11. MDD results in software being less sensitive to changes in technology

Technology changes follow each other faster and faster. Think about things like Java EE, SOA / SOBA, webservices, REST, SCA, OSGi, and more recently restrictions in technology when moving applications to the cloud (e.g. other database structures). MDD makes sure you do not have to change your application model when you want to migrate your application to other technologies. The only thing which needs to change is the code generator (or interpreter). After changing the code generator (or adding additional code generating options) all application models can directly be transformed into code for the new technology.

## 12. MDD really enforces architecture

Companies often define architecture principles. Software applications have to comply with these principles, but how to check or enforce compliance when all code is created by hand? When using MDD software applications are guaranteed to comply with the chosen architecture. You can really standardize your IT landscape because architecture principles are enforced in the MDD tools. See also this article about the relation of Model Driven Engineering and architecture.

In general, functional architecture principles guide function design. These principles are reflected in the domain specific languages used in your MDD approach. They also condition the model validations (see also point 5). Constructional architecture principles guide construction design and are reflected in the code generator or interpreter.

## 13. MDD captures domain knowledge

The nice thing about MDD is that you are not only creating software, but you are also capturing domain knowledge in formal, high-level models. In most cases this knowledge is not explicit and you need to talk with people in the domain or let different people in the domain work together on describing their knowledge with formal models. In this context there is a strong relation between MDD and Domain Driven Design (DDD).

## 14. MDD provides up-to-date documentation

When using MDD you will not suffer from incomplete or outdated documentation, because the model is the documentation. When using the right abstractions, the models are readable for domain experts and business owners. This point is of course related to point 13.

## 15. MDD enables to focus on business problems instead of technology

Building on the previous fourteen points we can state that MDD allows you to focus on business problems and how to solve these problems using IT, instead of focusing on technology. So, stop discussing whether you should use WS-* or REST (or any other technology discussion) and start using MDD to deliver business value fast.
