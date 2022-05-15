# 5 types of Model Driven Software Development

(original article: http://www.theenterprisearchitect.eu/blog/2009/03/31/5-types-of-model-driven-software-development)

Model Driven Software Development is getting momentum. Is Model-Driven the future of software development? Or is it the same old wine in a new bottle? I’m not going to answer this question right now. I’ll first show you the different types of model driven software development using a simple metaphor: farming.

## Programming – the manual work

FarmerDoing all the farming by hand, it’s a craft, an art. You love it, or you don’t. Everything will become as you want it to be, on your time.

In software development programming can be seen as manually creating a low level model of an application. That low level model (implementation model) is compiled to an executable or interpreted on a virtual machine.

As with tools for farming you have tools and frameworks making the job easier, but it stays handiwork. I won’t define programming as model driven software development. I just mention it to sketch the starting point.

## Code generation – automation

AutomationNowadays lots of work on a farm can be automated. You have to learn how to use the machines doing the work for you, but once you have, all manual task are ‘generated’ automatically.

In software development the manual work can also be automated. Instead of writing code you can create models. These models are transformed into source code. You, of course, have to learn how to model, but once you have, all the manual work of writing code is automated. This means a whole shift in application development roles.

An early, well-known example of code generation is the generation of corresponding source code for graphical user interfaces in Integrated Development Environments. Nowadays a lot of tools exist, generating full applications based on templates.

## MDA – abstraction

In the previous approach we needed a specialized machine for each task. That involves a lot of learning about how to configure and operate those machines. In case of milking we have to attach the machine to each cow by hand. Can’t this be automated by stepping one abstraction level higher? We just model how to attach the machine and the next part of our job is automated!

In a very basic way that’s what Model Driven Architecture (MDA) is for software development. Instead of just generating code from a model, you can construct platform independent and platform dependent models. The platform independent model is transformed into a platform dependent model using model transformations. From the platform dependent model the source code is generated.

If you specify the needed functionality in a platform independent model, you can transform this functionality into models for different platforms. So, the MDA is mainly aimed at technical variability.

## DSL – specializing

Farms have changed a lot over time. Started as a means for farmers to grow their own food, the focus has now changed to financial gain. That, in combination with, among others, the industrialization and growing complexity of a farm led to more specialized farms. This means that consumer products are mostly composed of materials from different farms. Examples of specialized farms are dairy farms, orchards, vineyards, stud farms, plantations, poultry farms, etc.

In software development a same movement can be seen. A lot of people argue that the UML, the language used to define the models in the MDA, is too complex. Instead of using UML the use of Domain-Specific Languages (DSLs) is promoted for model driven software development. DSLs are small languages tailored to a specific domain (a system aspect or a certain problem domain). An application isn’t modeled with a single, monolithic model specified in one language, but with multiple small models specified with different DSLs. DSLs can vary in structure, variability, and notation. Most DSL approaches contain a direct translation between DSLs and their execution by using code generation or the direct interpretation of the DSLs.

## MDE – from problem to solution

We can talk a lot about farming and how to automate and specialize it more, however, the real leap in productivity is in alignment. The production of raw materials need to be aligned with consumer needs. We see this happen with big companies targeting consumer needs (or manipulating them 😉 ) with advertising campaigns. All production is aligned to deliver consumer products composed of multiple materials maybe coming from different farms. The focus is not on the farm and how to improve it, the focus has become consumer-centric.

In model driven software development the same can be done. In the approaches mentioned before the target was to model the application at a higher abstraction level than a programming language. We can, however, go one step further. We can also create models of the using system, i.e. creating models of the organization which is going to use the software. Once we have modeled the so-called problem domain, we can make translations to a model of the solution domain. These translations or transformations don’t necessarily have to be automated, in some cases that’s not even possible. However, they need to be supported by appropriate tools and methodologies.

This Model-Driven Engineering approach differs from other approaches because we can distinct between horizontal and vertical transformations. Horizontal transformations from problem to solution domain, and vertical transformations from solution domain models to executable models. We’ve seen in previous articles on Model-Driven SOA that such approaches are possible. However, the challenges of MDE are in appropriate tooling, methodologies, patterns, templates, reference architectures, and industry standards.

In short: MDE focuses on the problem domain, it is (or should be) business-centric.

A lot more can be said about the different approaches and how they compare to each other (and yes, I think I’ll do that in the future), but for now you have a quick overview of these 5 approaches. What are your experiences with these approaches? What approach do you prefer and why?
