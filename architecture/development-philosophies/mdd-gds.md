# Model-Driven-Development (part 1) — RAD, BPMS and Low-Code Development Platforms

(original article: https://blog.gds-gov.tech/model-driven-development-part-1-rad-bpms-low-code-development-platform-etc-287060722058)

TL;DR — Ten years ago, model-driven-development (MDD) was a ‘thing’. Then came MDD products like RAD (Rapid Application Development) platform and BPMS (Business Process Management Software).

Today, low-code development platform is the new old buzzword. Here are some thoughts on what’s different as well as, the good, the bad and the ugly.

First, the definition...

> Forrester Research defines low-code development platforms as “platforms that enable rapid application delivery with a minimum of hand-coding, and quick setup and deployment, for systems of engagement.”

## #SameSameButDifferent

Like MDD, low-code development platforms allow developers to express their solutions with visual models and minimum hand-coding. The solution is graphically developed in IDE, using ERD (Entity Relationship Diagram), form widgets and/or BPMN (Business Process Model and Notation), made possible by WYSIWYG and drag-and-drop techniques.

### Open vs. closed platform for pre-built components

Components in the visual model are reusable in both traditional MDD and low-code development platforms. The difference is in the creation and distribution of reusable components. Traditional MDD platforms are closed. Pre-built components are solely created and distributed by ISVs.

In contrast, low-code development platforms are open platform and have a public marketplace. Pre-built components can be developed by any developer and made available at the marketplace for other developers to review, download and install — highly affordable.

### Time and effort to set up and deploy code

Another important difference is the time and effort to set up and deploy code. Unlike traditional MDD that uses thick-client IDE and charges by the number of named/concurrent developers in the enterprise, low-code development platforms usually use browser-based IDE and charge by named/concurrent runtime users.

Like many respectable modern IDEs, low-code development platforms are cloud-friendly. Hence, developers can push code to cloud from their IDE, easily and frequently.

### And lastly, low-code development platforms are for systems of engagement

Accordingly to Geoffrey Moore, systems of engagement are social platforms that are highly collaborative, highly interactive, mobile 1st and user-experience-centric. Here’s an explanatory video on systems of engagement.

## The Good

The value proposition of a low-code development platform is to accelerate application delivery and improve business agility by:

- Encapsulating and abstracting out code with visual modelling. E.g. Form designer, BPMN, workflow runtime versioning and entity relationship diagram.
- Reusable components from the app marketplace, e.g. audit trail logging, form controls, dashboard widgets, data connectors
- Easy to start small and deploy frequently to the cloud, which is essential for rapid prototyping.

## The Bad

### Open standard vs. open platform vs. open source software (OSS)

Myth: Open standard means no effort is needed to port the application from one platform to another.

Fact: BPMN is an open standard so there’s no vendor lock-in for BPMS that supports BPMN. Given two development platforms that support BPMN v2.0, business process definition meta-model (BPDM) can be migrated between them. Unfortunately, BPDM does not include UI, form controls, and data validation logic. So some work is still needed to port the UI to another platform.

Myth: Open platform means no vendor lock-in.

Fact: Open platform creates a marketplace for pre-built components to be purchased and shared. An open platform does not mean open-source pre-built components. Neither is it an open-source development platform. It also doesn’t prevent vendor lock-in. Open platform merely means you have more pre-built components to choose from in the marketplace.

Myth: Open source programming language means open source software (OSS).

Fact: Another common misconception is about the development platform programming language. Just because the platform uses an open source programming language — such as Java — it does not mean that platform is OSS. It merely means the application runtime is not locked in to vendor. You will still need the development platform to view or modify the visual model because generated source code is not the most beautiful thing to read.

### Deployment is easy. Data patching is hard.

Developers on low-code development platforms can easily push code to cloud from their IDE. However, that’s not the real challenge to solve because code is stateless and data is stateful.

The real challenge about pushing changes to production frequently is to ensure backward compatibility with existing processes. For example, in a HR leave system, there are 3 leave applications running workflow version 1 and you are going to deploy workflow version 2 for new leave applications. However, version 2 is not backward compatible with version 1 processes. These processes are often long-running, as new leave applications are received every second.

In this situation, how frequent can you deploy to production? Especially for applications with high volume transactions, bulk of the deployment effort is spent on data patching, not code deployment.

> If you don’t know what problems you are solving for, any snake oil will suffice.
