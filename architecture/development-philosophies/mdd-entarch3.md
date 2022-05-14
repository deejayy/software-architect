# 10 Misperceptions and challenges of Model Driven Development

(original article: http://www.theenterprisearchitect.eu/blog/2009/01/21/10-misperceptions-and-challenges-of-model-driven-development)

## 1 - Challenge: The method was not in place and not consumable

Due to the lack of best practices and MDD methodologies in the early days, it was difficult for enterprises to adopt MDD as addition to their existing processes and methods.

> *What we need is tooling which not only provides guidance (which still requires the user to find, interpret and follow that guidance) but can also automate aspects of the solution. For instance, when using Eclipse based products you can leverage Cheat Sheets. A Cheat Sheet provides step-by-step guidance in completing a task and can automate steps within the workflow.*

I totally agree. One of the most important aspects of tooling supporting a model driven approach is the incorporation of a methodology. By methodology I mean: what models have to be created, in what order, and how are they related? Tooling can automate parts of this process by wizard like structures and the automatic creation and checking of references among models.

## 2 - Challenge: The right infrastructure and tools weren’t in place to reap the benefits of MDD

In principle this is a detailed explanation of the outcome of the previous challenge, i.e. how tools can support MDD. Portier and Ackerman state the following tool features (a bit summarized):

- **Business alignment**: by using the MDD models and automations and their associated "traces", you keep track of the reasons why you are making decisions, tracing all the way up to your business requirements.
- **Higher quality**: because the practice is codified in the tool and automated, there is less or no room for error.
- **Increased consistency and governance**: as the tooling provides support for guidance and automation of best practices it improves the consistency of elements within the solution. In addition, the tooling can ensure that elements that are built are tied to and stay aligned with both requirements and best practices.
- **Enhanced productivity**: repetitive, time-consuming tasks are now automated. Practitioners are able to "reuse" and spend time on what matters the most (e.g., business logic).
- **Improved communication**: using the models, tools and automations, practitioners (e.g., architects) can create different perspectives that target different audiences.
- **Impact analysis**: MDD traceability allows you to analyze the impact of a change in the requirements on your solution, and vice versa.

I think business alignment, improved communication, and impact analysis are the most important aspects of good tooling.

I don’t agree with the higher quality. First, codifying the practice without room for error means also that you have to work precisely as the tool prescribes. That sounds a bit like a one-size fits all solution. I think it is important to give users the freedom to follow their own process and iterations. The tooling should ensure quality by change propagation, consistency checking, and testing facilities.

## 3 - Misperception: MDD == UML?

> *One misperception is that MDD means that you have to use the Unified Modeling Language (UML) – as-is, in its entirety as it is stated in the UML specification from the Object Management Group (OMG).*

I think it is no surprise that I agree that MDD or MDE doesn’t need UML. See DSL in the context of UML and GPL for a full discussion on using UML or DSLs for Model Driven Engineering.

## 4 - Misperception: MDD is a one size fits all solution

> *Following on from the previous misperception, it should be apparent that MDD is not a one size fits all solution, any more than a default manufacturing product-line toolset could be used to build any product. MDD is all about using models in ways that add value to your specific situation, applicable to your specific domain, and suited towards the type of software that you are developing.*

I think we can distinguish two types of approaches having different applicability levels:

- An MDD factory focused at the problem domain. Models in this approach directly model the problem space. An example can be an MDD approach for insurance products.
- An MDD factory focused at the solution domain. Models in this approach model the different system aspects with use of different DSLs. For example models for data, presentation (GUI), security, business rules, workflows, etc. These models have a much higher level of abstraction than GPLs like Java or C#, but are still applicable to more than one problem domain.

What approach best fits your situation depends on the effort you want to spend on building a specific factory and the benefits it brings you in terms of domain specificity.

## 5 - Misperception: The diagrams are the model

Portier and Ackerman make a distinction between the model and views on that model with diagrams. I agree with them that for communication purposes the construction of different views on the same model is very helpful. However, I think we have to go a step further. We need to split the model of a system in multiple small models. This gives the following advantages:

- Each model can be specified in its own DSL thereby enabling the use of very specific, small languages.
- Small models are easier to manage (both for users as for the tooling).
- It is easier to enable versioning and team development.

## 6 - Misperception: The code is the model and the model is the code

Portier and Ackerman state that MDD is not just about code visualization and generation. You need more and higher levels of abstraction enabling analysis, traceability, refactoring, etc. The also state:

> *On the other end of the spectrum, there has been situations where people have been so excited about models and MDD that they simply modeled for the sake of modeling, and forgot to turn their models into something that is actionable or executable. The architect can communicate with stakeholders, designers and developers – but once again, you guessed it, you do not reap the full benefits of MDD.*

I agree with both views. First MDD is not just modeling at a very low level enabling code generation and visualization. On the other hand MDD is also not only documentation with use of models. What you need is a full end-to-end methodology describing how to model your business process and how to transform that model into an executable artifact with use of both manual and automatic transformations.

I want to add one view: I think the model can be the code. Not by using low level models, but by using execution engines for high(er) level models. In other words: using model interpretation instead of code generation. Examples of such engines are business rules engines and BPEL engines. We at Mendix also use this approach to make our lowest level (but still high opposed to source code!) models executable.

## 7 - Challenge: Platform independence is challenging

> *Not sure when or why it happened, but a great deal of attention has gone into the idea of modeling at a very high level and then be able to generate solutions. Perhaps it’s from the MDA platform independent model, perhaps from elsewhere. Regardless of the source, it’s important to recognize that it is very difficult to go from something that is very high-level and use that one representation to target many different types of implementations.*

Indeed very challenging! The question is: do we need it? What kind of different platforms do you want to target? Isn’t it enough that you can execute the generated code or the model interpreter on different application servers, which on their turn run on all different kinds of operation systems and hardware?

## 8 - Challenge: Keep coders creative

In principle this challenge is about the changing roles in software engineering. Instead of programming a solution we need to program the software factory. I’m currently working on a detailed article on this subject, i.e. roles and workbenches in MDE.

## 9 - Challenge: There was no content to be leveraged

> *Having the tools and infrastructure in place is not enough to deliver the software that addresses the challenging business issues we face. At the end, it is not the tools that solve the problem, but it is the people using the tools. And if we want people to use tools, then it makes a big difference if the tools already have content to start from. Have you ever been in front of a blank white board, piece of paper, or IDE workspace? Wouldn’t it be easier if you had a reference or template to start from, something to guide and structure your approach?*

Portier and Ackerman do not only point at patterns and templates, but also reference architectures and industry standards. I totally agree with them on this point. For traditional software engineering an enormous amount of patterns, examples, reference implementations, templates, etc. are available to start with. For MDD we need the same.

## 10 - Misperception: MDD is just for Development

In short this point states: don’t use MDD just for development. Extend the scope to modeling business problems, enterprise architecture, etc.

I think for effectively using MDD and raising the productivity of the MDD approach in comparison with traditional software development it’s not just a matter of extension, you WILL NEED to do this! The advantages of MDE / MDD are about the higher level of specification (if possible in business terms) and the tracing of implementation with requirements and even business strategy.
