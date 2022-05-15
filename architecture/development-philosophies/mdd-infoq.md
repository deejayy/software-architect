# Model Driven Development Misperceptions and Challenges

(original article: https://www.infoq.com/articles/mdd-misperceptions-challenges/)

After many years, it still seems that the level of adoption of MDD is not what would be expected. There are a number of inhibiting factors that limit the usage of MDD, such as the lack of awareness of practical MDD success stories, doubts on how it can be used on a daily basis, lack of funding model for up-front investment, or lack of focus for strategic initiatives.

If you have tried to use MDD in the past, you may have encountered challenges and as a result you may not be using MDD today. Or maybe you are trying to adopt MDD, and you are faced with challenges and obstacles. If you find yourself in either of these situations, then this paper is for you. In this paper, we are going to look at challenges and misperceptions related to the adoption of MDD.

Modeling has proven itself to provide value by improving communication, business-alignment, quality, and productivity. Its applicability includes a number of disciplines such as analysis, design, or development.  With this in mind, we’ll take a look at a number of misperceptions and challenges regarding MDD and how they can be addressed with a modern approach and set of associated tools.

## 1 - Challenge: The method was not in place and not consumable

One of the key Model Driven Development (MDD) inhibitors was that the MDD best practices were not readily available to people as they were performing their activities. For example, people had access to process documentation on how to perform a specific task (e.g., design a highly available solution), and that description did not include any MDD content. To access the MDD practices, they had to go find it in articles or books, and then try to apply it to their existing non-MDD documentation. 

Today, more MDD guidance is available to practitioners when they perform their daily duties, and that information is embedded in the tooling they use on a daily basis. We start to see development processes, which include “tool mentor” best practices that leverage MDD principles, and these “tool mentors” are attached to the overall method and process.    

Now, the guidance for specific tasks (e.g., review requirements, design a user interface, or design a highly available solution) includes links to MDD contents. For example, a design pattern is recommended, and guidance is provided on how to apply the pattern to the design, using an implementation of the pattern in the tool at hand. 

Another inhibiting factor was that MDD was too intermingled with specific development methods, and people could not extract the MDD best practices out, and apply them in a different context. A typical example is that a great deal of material existed on Object Oriented Analysis and Design (OOAD), and either you adopted the full OOAD contents, and as part of it you could reap the benefits of MDD, or you didn’t adopt it at all. The MDD best practices were part of an OOAD framework, but people didn’t know how to leverage these best practices outside of the framework. It was not possible to extract out the MDD contents and apply them in a different situation.

These and other factors made it difficult for enterprises to adopt best practices (including MDD best practices) in their environment. Companies had their existing processes and methods in place, and it was difficult to add the MDD aspects to that method.

The industry is now getting better at tailoring a specific development process to adopt it for an organization - and for specific types of projects.  For instance, there are workshops aimed at guiding a team through the development of a customized development process, usually referred to as “method adoption workshops”. The goal of the workshop is to tailor existing method contents for a specific project, and it usually involves the following people: the process engineer (the person who owns the development process for the organization), the lead architect, the lead developer, and the project manager.

Supporting such customization, we saw the advent of method tools such as Rational Method Composer and Eclipse Process Framework Composer, which contain componentized best practice libraries.  The idea with these tools is that the best practices are codified and packaged, and the tool is used to tailor and adopt these best practices for your organization. In the tool, you select the specific method elements that you want to adopt, modify them, codify your own, and organize the contents into processes that you want to follow. Then you make the resulting process available to the organization in a format that is readable (e.g., HTML) by the practitioners as they perform their daily tasks.

Even though there is more guidance available using the tooling and approaches discussed, it still requires the user to find, interpret and follow that guidance.  One step that helps overcome this obstacle is the including of tooling that not only provides guidance but can also automate aspects of the solution.  For instance, when using Eclipse based products you can leverage Cheat Sheets.  A Cheat Sheet provides step-by-step guidance in completing a task and can automate steps within the workflow. 

A discussion on a third mechanism, pattern implementations, will appear in the next section.  Regardless of the method chosen - the key point is that more and more guidance is being captured and put into places and tooling to better guide the user as they look to leverage models in their efforts.  

Just as it is possible to over-engineer a software solution - the same can happen when creating the guidance.  The final piece needed to overcome this challenge is a need to be realistic, pragmatic and proactive.  There is little sense, value - and likely time - to figure out all details around all steps needed to build out a solution.  What are the key steps?  How do they align with the skills of the team?  Where does it make sense to invest time in documenting steps?  How much should be invested in creating static documentation versus automation?           

Processes, and MDD in particular, are not one-size fits all solutions - as discussed in misperception 4. 

## 2 - Challenge: The right infrastructure and tools weren’t in place to reap the benefits of MDD 

In recent years, we have seen modeling tools evolve from merely supporting a given graphical notation such as the Unified Modeling Language (UML), to significantly helping practitioners do their job. Not only do the tools support a graphical modeling notation, but they now have built-in MDD features that benefit as follows: 

- **Business alignment**: Business alignment is a critical aspect of successful approaches like Service Oriented Architecture (SOA). By using the MDD models and automations and their associated “traces”, you keep track of the reasons why you are making decisions, tracing all the way up to your business requirements.  In addition, we can look at leveraging specialized versions of MDD, such as Business-Driven Development (BDD).  As the name implies, with BDD the concern is on modeling the business.  In this case you can model and in some cases simulate the processes that comprise the business.
- **Higher quality**: Because the practice is codified in the tool and automated, there is less or no room for error.
- **Increased consistency and governance**: As the tooling provides support for guidance and automation of best practices it improves the consistency of elements within the solution.  In addition, the tooling can ensure that elements that are built are tied to and stay aligned with both requirements and best practices.
- **Enhanced productivity**: Repetitive, time-consuming tasks are now automated. Practitioners are able to “reuse” and spend time on what matters the most (e.g., business logic).  Depending on the automation built, the level of sophistication of the user base, and the aspects being automated - the ROI for the investment can either be achieved within the current project or may be spread out over multiple projects.
- **Improved communication**: Using the models, tools and automations, practitioners (e.g., architects) can create different perspectives that target different audiences.
- **Impact analysis**: MDD traceability allows you to analyze the impact of a change in the requirements on your solution, and vice versa. 

To illustrate how MDD is brought to life by tools, let us use a design pattern as an example. Think for example of having the design pattern described in a book. We refer to this as the pattern specification. That specification is very useful. It describes drivers for when to use the pattern, the parameters of the pattern, the benefits and implications of using the pattern. The pattern specification helps people understand the pattern and select it if appropriate. The pattern specification, however, doesn’t ensure higher quality of the design or enhanced productivity. To get these benefits, you need the pattern to be “automated”. We refer to this as the pattern implementation, a reusable codification of the pattern specification in the tool. Using the pattern implementation, designers can now very quickly apply the pattern to their design and be certain that it will be applied correctly. 

It is very unlikely that a domain-independent tool will have built-in all the MDD artifacts that you require for your domain. In addition to the MDD artifacts provided out-of-the-box by tools (e.g., a set of design pattern implementations), tools also allow you to “extend” what is provided and build your own. Tools now include “extensibility frameworks” with best practices, templates, and APIs. Tools such as Rational Software Architect allow you to build MDD artifacts (e.g., pattern implementations, rules, constraints, etc.) that are applicable to your domain. 

Now that you are able to build these MDD artifacts, Asset Based Development (ABD) provides the practices and infrastructure that allows you to share these artifacts with others and promote reuse. In other words, the ABD best practices and infrastructure improvements support the adoption of MDD. Reusable asset repositories, such as the Rational Asset Manager, allow you to manage reusable software artifacts and have development communities share and reuse artifacts. Think about a pattern implementation created for your domain - you can now submit it to the asset repository, have it reviewed and approved, and have other practitioners in the community reuse it. As part of this ecosystem you can monitor how and when the asset is reused, gather feedback and ensure that the entire team is using the right version of the right asset.  

Again - we come back to being pragmatic and practical.  An ABD and reuse initiative needs to be adopted as it makes sense to you and your organization.  You need to recognize your level of maturity and adopt the necessary tools and processes that support it.  With forethought and planning, you can grow and roll-out your ABD program as needed and avoid unnecessary overhead and cost.

## 3 - Misperception: MDD == UML?

One misperception is that MDD means that you have to use the Unified Modeling Language (UML) - as-is, in its entirety as it is stated in the UML specification from the Object Management Group (OMG).  There are a number of ways in which we can dispel this misperception. 

A first way in which we can dispel this notion is that to work in an MDD approach only requires that you use models as a key artifact in the work that you perform - and automations that leverage these models.  In this context, a model is a simplification of reality using a language with well defined syntax and semantics.  As such, there are many languages that can be used in MDD - not just UML.   

As with most scenarios, we really need to focus on picking the right tool for the task at hand.  If we need a standardized, well-known and widely supported language for our MDD efforts, then UML is a good choice.  UML is also built to be extensible.  As such, it can be customized via the use of a Profile - offering customized elements, properties and constraints.  This can assist in making UML specific to the work that you are doing and make the language easier to learn and use.  Another option for enhancing the consumability or specificity of the modeling language can be achieved by creating your own Domain Specific Language (DSL). 

The key to keep in mind is that we are deriving the benefits from the language we use and the models that we create.  To guide the investments that we make, we can leverage the following questions:

- Are you able to effectively design and understand the solution space? 
- Can you communicate easily with others? 
- Can you generate other portions of the solution based on what has been modeled?
- Can you effectively leverage the results outside the development lifecycle?
- Can you effectively trace the implementation to the design?  To the requirements?

## 4 - Misperception: MDD is a one size fits all solution.

Following on from the previous misperception, it should be apparent that MDD is not a one size fits all solution, any more than a default manufacturing product-line toolset could be used to build any product.  MDD is all about using models in ways that add value to your specific situation, applicable to your specific domain, and suited towards the type of software that you are developing.  To that end we can look at a number of ways in which we can use MDD and do so as makes sense in our situation. 

One example is the way in which we can use MDD along with traditional Object Oriented Analysis and Design (OOAD) approaches.  Often, when looking at OOAD and MDD, we see the use of a number of models such as Use Case, Analysis, Design and Implementation.  Many examples and much documentation exists that show these models being used together to craft a solution.  However, this is not meant to say that you have to use all of these models.  The key point is that we are effectively leveraging abstraction.  The number of levels of abstraction will depend on your situation, the language in use, associated constraints, rules and assumptions - along with the automations that may be brought to bear.

In addition to being pragmatic about the number of models (and associated levels of abstraction) - we also need to be just as pragmatic when it comes to choosing the diagrams that are used within the model - diagrams are used to communicate perspectives.  For instance, if we are using UML as the language for modeling - we do not have to use each of the diagram types available (class, interaction, …).  There is such a range of diagram choices in the language, as a recognition that it is a general purpose modeling language servicing a wide range of needs.  In your specific situation it makes sense to pick only those diagrams that add value and help you communicate what you are trying to accomplish.  And for completeness, we can take the discussion a step further and point out that even within a diagram you do not need to use all of the available model elements.

## 5 - Misperception: The diagrams are the model

A key thing in MDD is the recognition that we are creating a model - as discussed earlier, a model is a simplification of reality using a language with well defined syntax and semantics.  Within that model we find numerous modeling elements and a set of diagrams.  Each of the diagrams provides a view on top of the model elements.  Each of the model elements can belong to zero or more diagrams.  We need to focus on those model elements - what are they?  What are the relationships?  What are the properties?  We usually use diagrams to help us think through these aspects.  In addition, we will use diagrams as a way to communicate with others.  However, the key information from the model is found in the model elements - as this allows us to generate the views needed, create diagrams as needed, and to support the generation of other elements from the model.  If MDD was just about diagrams, then all we would need for tooling would be a application that allows us to draw pretty pictures.  That’s not to say that the diagrams (and the tooling support for them) are not important.  Tooling for creating the models and diagrams within needs to be tailored to the target audience.

Combined with being selective in the diagrams used - we can also look to leverage viewpoints as a way to make models more consumable and communicative.  A viewpoint is a way of organizing a model so that certain areas of the model provide additional diagrams to make the model targeted to multiple audiences.  Usually a perspective will only contain diagrams and no additional semantic elements.  As such, when you update the semantic elements, the perspectives are automatically kept in synch.  The use of perspectives adds value to your MDD effort by allowing you to effectively support communication with other roles and groups.  Each of the groups will want to understand portions of the solutions - those portions that are relevant to their needs.  Perspectives allow you to support these needs without cluttering the model, building separate models, or wasting time in maintaining multiple versions of the same elements.  Keep in mind that we are not stating that you need to support any and all different groups and create a gigantic set of perspectives.  Again, the key is to be pragmatic and create the diagrams and viewpoints that make sense and add value.

## 6 - Misperception: The code is the model and the model is the code 

One of the early MDD misperceptions was that it can only be applied to code. Basically MDD was limited to a low level of abstraction and therefore could only have a limited impact. A lot of people simply used the MDD tools as a way of “visualizing” their code (think of a reverse transformation that gives you a graphical view of your code). This has benefits; for example, you get a better understanding for large pieces of code and the relationships between your components or classes. Taken in isolation, however, visualizing the code doesn’t allow you to reap the benefits of MDD we discussed earlier (e.g., business alignment, enhanced quality, improved productivity, or impact analysis) - as all it is doing is allowing you to view code graphically. This is a basic, low level approach to using diagrams and as expected provides a low return - on a low investment. 

Getting a little more sophisticated, the next step up is to visualize your code, and then be able to reconcile it with the intended design. For example, imagine that the designer or architect wants to review the code produced by the development team. The graphical view of the code allows them to compare the code to their design because it uses the same visualization (e.g., UML classes). However, although both are represented using the same language, there is still a gap between the two representations as they exist at different levels of abstraction.  MDD tooling - via visualization, traceability, analysis and discovery features, and refactoring support - helps to assist the designer in their efforts.  Once areas of design-code divergence are flagged, manual intervention is usually required for the designer to communicate with the development team. This adds value, but doesn’t allow you to reap the full benefits of MDD.  Time and effort is added to the project to support the analysis and communication - an investment that is needed multiple times per project.

MDD should be applied at any level of abstraction and also helps you traverse the different levels. You should model at high levels of abstraction as well. Think for example of an analysis model (e.g., a system use case model) that is used as input to a transformation into a design model. There are things in the analysis model that can be leveraged in the design. For example, the categorization of information into functional area (packages), or each use case can be used to create a base template for interaction diagrams in the design model where the use case is realized. Using tools and their extensibility features, you can codify this “analysis to design” transformation, and then have people in your organization reap the quality and productivity benefits.

MDD is applied at any level of abstraction, and there is an infinite set of levels of abstraction. Use the levels of abstraction that make sense for your domain and your organization. As an example, with Service Oriented Architecture (SOA), you can consider the following levels of abstraction when you develop your solution: 

- **Business**: This level makes sense to business strategists, business analysts, or product owners. At this level, your model elements are things like business goals, key performance indicators, business policies, functional areas.
- **Analysis**: Analysis and Design are usually looked at together, and the analysis model elements sometimes evolve into design elements. In the context of SOA, we believe it is important to consider the Analysis because it is where the technical model elements originate, to support the business elements.
- **Design**: It is in the design that most of the architecturally significant elements of the SOA solution are modeled. The design documents the key elements of the architecture, and also how they are realized.
- **Implementation**: Implementation is the “code” level of abstraction. This is where using MDD allows you to generate the code stubs based on the design, and then reconcile code and design if needed. 

On the other end of the spectrum, there has been situations where people have been so excited about models and MDD that they simply modeled for the sake of modeling, and forgot to turn their models into something that is actionable or executable.  The architect can communicate with stakeholders, designers and developers - but once again, you guessed it, you do not reap the full benefits of MDD. When you plan your MDD strategy and method, always think about how you will leverage your models.  For example, what is the platform the solution is eventually deployed to? How can you improve the quality of the code and the productivity of developers? Do you have transformations that would take your models and turn them into code stubs? 

And, as the models created contain useful information about the design that goes beyond what is needed for code generation, we can also look at the other ways in which we can leverage the important and valuable information that has been captured.  This can include the generation of documentation, test cases, deployment scripts, etc - significantly boosting the overall productivity of the project.  As we all know, the actual writing of the code is just a portion of the overall effort that goes into a project. 

There is no silver bullet. Not all the code you need is going to be automatically generated (unless your domain is not large at all). At the end, you have to manage models and code, and MDD guides you on making sure your models can be leveraged, and your code is in synch with the models. 

But what about round-trip engineering?  How can we leverage automation to keep models synchronized across levels of abstraction?  This is still a tough problem to solve with a general solution.  For example as we move from a higher level model to a lower level model there is a fan out of elements - where a single element can spawn many elements at the lower level.  Then once created, the user can update, remove and add elements to the lower level model.  How do we map back to that higher level?  What is the translation/mapping of some set of detailed elements to a smaller number of high level elements?  With the challenges involved it makes sense to question if this is an approach that you want to pursue as part of your development approach. 

Because modifications are likely to happen at code level, without an approach to try and “reconcile” the models with the code, models will soon be seen as documentation-only. Recently, tools such as Rational Software Architect have improved a great deal in the area of “reconciliation”, providing capabilities to visualize code, diff, and merge. Please note that the approach used to reconcile these changes is more important than the tooling capabilities, and this is related to governance. For example, when the architect sees discrepancies between the code and the model, what happens? Does the architect discuss with the developer? Does the architect ask the developer to change their code? Does the architect change the models? As you can see, it is probably not going to be a fully automated approach. 

Another approach that has had a great deal of success is to invest in advance in tooling (either purchased or custom to your organization) that narrows the problem space through the use of constraints, rules and assumptions.  The more that you can constrain the problem space, the more likely that you can generate higher percentages of the solution, reduce the levels of abstraction and eliminate the need to round-trip.  In such situations, the focus is on forward only engineering.

## 7 - Challenge: Platform independence is challenging

Not sure when or why it happened, but a great deal of attention has gone into the idea of modeling at a very high level and then be able to generate solutions.  Perhaps it’s from the MDA platform independent model, perhaps from elsewhere.  Regardless of the source, it’s important to recognize that it is very difficult to go from something that is very high-level and use that one representation to target many different types of implementations.  There have been some solutions that have allowed users to leverage models and generate 100% of the resulting code for the solution.  However, in those cases - and as alluded to in the previous section, the tooling was very specific to a domain and leveraged a set of constraints, rules and assumptions to make that transition possible.  The solution space was kept very narrow and as such provides opportunity for high levels of generation.  As we increase the scope of the solution space, generation becomes more difficult.

Even with the migration to DSLs questions come up about how easy it will be to use that same model to serve as the input to generate multiple underlying implementations.  When looking at leveraging the DSL, the key should be on the specifics of the domain and the current project.  As we’ve learned through many of the agile processes (and our own experiences) there is a price to be paid for over engineering and accounting for every possibility.  The same goes for modeling and the languages that we use.  Being specific to a domain is not necessarily a bad thing - and as a matter of fact can be in our best interests.  However, it is unrealistic to expect that we can craft a domain specific solution and then apply it to a wide range of solutions. 

## 8 - Challenge: Keep coders creative

As we move to MDD and look to simplify how we capture our design, improve our communication and generate portions of the solution - we also need to recognize that this can have an impact on the team.  Some members of the team may prefer to work at a lower level of abstraction; they may feel constrained by the modeling environment or prefer more freedom in how they work toward a solution.  Not all of these concerns are valid concerns - but the underlying theme needs recognition.  We need to make sure that we are getting the most from each member of the team. 

Even when working with models we need expertise in the underlying implementations.  What frameworks should be used?  How do the frameworks come together?  Let’s look at the example of patterns. A key input into building pattern implementations is a reference solution, known as an exemplar, which is used for determining what and how the pattern implementation should work.  If we are building our own pattern implementations, who will build the exemplars?  Who will judge if the exemplar is indeed the best way to solve a problem?  When looking at simplifying the modeling experience, who will figure out the rules, assumptions and constraints?  How will they get codified into the tooling that everyone will use?  Hopefully these questions highlight the fact that there are many places where expertise, creativity and problem solving skills are needed.  When planning and starting an MDD effort, it is important to communicate these challenges to the team and ensuring that everyone on the team is able to find ways in which they can constructively and productively contribute to the project.  Reflect on past projects - how much time was spent on truly creative work?  How much time was spent on mechanical, boring and repetitive tasks?

## 9 - Challenge: There was no content to be leveraged 

Like any other relatively new approaches, until the best practices are understood and the infrastructure is in place (the challenges we discussed in previous sections), only very limited content is produced. Now that MDD is getting more mature and getting traction in the software industry, we start to see high quality MDD content and assets being produced. Having this content available to start from is essential for the adoption of MDD. 

Having the tools and infrastructure in place is not enough to deliver the software that addresses the challenging business issues we face. At the end, it is not the tools that solve the problem, but it is the people using the tools. And if we want people to use tools, then it makes a big difference if the tools already have content to start from. Have you ever been in front of a blank white board, piece of paper, or IDE workspace? Wouldn’t it be easier if you had a reference or template to start from, something to guide and structure your approach? 

Here the MDD contents we are talking about are not just design patterns or UML project templates. We are talking about things like a reference architecture for an industry or solution (e.g., call center reference architecture or banking reference architecture), the codification of an industry standard as actionable models (e.g., ACORD for insurance or SID for telecommunications), or comprehensive templates for implementation stubs. A successful example of this kind of asset is the WebSphere Business Services Fabric (WBSF) Industry Content Packs (ICPs). The WBSF frameworks comprise a runtime and the associated tools. The ICPs then complement the framework by providing customizable content for specific industries (domains). This content includes models and templates at different levels of abstraction (e.g., business, design, and implementation) that comply with that industry’s standards, and can be tailored and adopted by your organization. 

The key value proposition of these assets is that they provide higher business value and are closer to the organization’s strategy. In other words, the business can see that they affect the bottom line. If we start to compare the value of a reusable design pattern or an industry framework, then of course the industry framework provides higher value. The applicability of the industry framework however, is more limited. For example, if it is a framework for Insurance, then you can not use it if what you do is Telecommunications. On the contrary, the design pattern is applicable regardless of the industry - but provides limited value and is further from the bottom line. As recognized by the Asset Based Development (ABD) community, having this content customizable (the technical term is “variability points”) helps augment their applicability.

Note that this type of content is not limited to high levels of abstraction (e.g., business models). Operational assets do affect the bottom line because they are actionable and executable. Think for example of assets in the area of security, fine-grained access control policies that you can reuse and adapt. Surely these impact the bottom line and people can make the link from these to the high level business security policies.

## 10 - Misperception: MDD is just for Development

When building a software solution, there has been great value in using models to specify the architecture, the associated services and components and from there other aspects of the solution.  However, that is just a portion of where and how MDD can provide value to an organization.  When looking to leverage and benefit from models - there is no need to limit the scope to such a narrow scope of use. 

Earlier, we discussed Business-Driven Development as a specialized form of MDD.  In that case, the focus is on modeling the business - what are the processes within the business?  How do they work?  How can they be optimized?  If we do not get this part of the effort right, everything else will suffer - garbage in, garbage out.

In addition, we can leverage models to support regulatory compliance efforts.  A model can be used to provide an easily understood representation detailing how the resulting solution supports regulatory requirements.  For example, a model can be used to fulfill a regulatory requirement showing how the organization is consistently applying a rule across customer segments, LOBs or channels.  Just providing code to document compliance is a sub-optimal solution.

What about cases where we are looking to enhance the functionality of an existing solution?  If requirement ‘A’ changes, what impact will that have on the system?  How do you determine which parts of your IT landscape must be verified?  Modified?  Without traceability from requirements through to implementation this becomes a difficult and expensive question to answer. 

Additional examples where MDD can be leveraged in the enterprise include, but are not limited to, the support of Enterprise Architecture and Operational Modeling.  Although the intent and targets are different - we still look to communicate, leverage abstraction, ensure governance, support compliance and improve productivity.  

Summary

MDD is something to consider as it provides many benefits by improving communication, business-alignment, quality, and productivity.  If you’ve looked at it in the past, it may be time to take another look. If you haven’t looked at it before, now is a good time as the tooling support has matured vastly.

MDD is another tool in your toolkit - just as you wouldn’t use just one language or a single library within a language - you need to pick the right approaches and aspects of MDD to succeed.  As you look at leveraging MDD in your projects, some questions to keep in mind as an approach to finding your way include:

- What is your situation?
- What do you need from a modeling tool?
- What do you need from your modeling language?
- What levels of abstraction are needed?
- How can you simplify and automate how the solution gets built?
- What diagrams types are needed?  How many diagrams?
- Who are you trying to communicate with?  What do they need to know?
- How do you make sure that the MDD approach and tooling is consumable by the entire team?
- How do you best leverage the skills of the team and keep everyone involved?
- Is there existing content available for your problem space?
- How can you leverage MDD in supporting the business?  How can you leverage MDD in support of IT?  How can you leverage MDD to provide Business and IT Alignment?
- What content is available?  How can it be customized to your situation?