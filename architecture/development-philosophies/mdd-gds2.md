# Model-Driven-Development (part 2) — Pitfalls and Recommendations

(original article: https://blog.gds-gov.tech/model-driven-development-part-2-pitfalls-and-recommendations-%E3%83%84-baf4c9ea0ec8)

Low-code development platforms, BPMS, RAD and other forms of MDD allow developers to express their solution at a higher abstraction level, instead of hand-coding.

## Hand-coding — feature or liability?

In MDD, hand-coding for widget placement, microinteractions, programmatic control flow, exception handling, etc is traded-off for improved productivity.

> If hand-coding is bad, why do all MDD tools allow it?

Although all MDD development platforms allow you to code alongside graphical models, too much hand-coding nullifies the purported productivity gained at best, and very often impedes delivery.

This is because no representation of visual model or code is absolutely bidirectional. Most development platforms are unidirectional — from model to code — while some development platforms are bidirectional for certain models.

> All non-trivial abstractions, to some degree, are leaky — Joel Spolsky

In the last three years, I have learnt of four failed projects. All use MDD.

## Poor testability

Another challenge of using MDD is poor testability. Since we develop visual models in MDD instead of writing lines of code, regression tests are mostly functional UI tests instead of unit tests.

Unfortunately, functional UI test against WYSIWYG form and click-and-drag widgets is a quality engineer’s worst nightmare.

To accelerate development, UI control identifiers are often machine generated and changed when the model is saved. The lack of direct control over UI control identifiers destabilises functional UI tests and creates false alarms. As a result, regression tests become too expensive to maintain.

Without a robust test suite, this approach does not scale for large complex application development.

## Platform becomes a white elephant

The development platform and IDE can be easy to install and setup. But without skilled developers, the development platform will become a white elephant.

Will you be able to find and hire skilled developers for that development platform? Are training courses for that development platform easily available?

## Bespoke or MDD?

For small projects, it is probably easier to develop a bespoke software solution than to use a development platform. For that small amount of development effort, the productivity gain from using a development platform is marginal at best. With bespoke software, you have better technical control over implementation and can deliver superior user experience.

For large complex systems development, I would divide the system into two smaller applications — internet-facing application and intranet-facing application. The internet-facing application will be kept small and developed as bespoke software, while the intranet-facing application will use a low-code development platform or a BPMS. These two applications will then communicate via REST API. This recommendation is based on the following assumptions:

- The productivity gain from using an MDD tool will exceedingly compensate the so-so user-experience of intranet-facing application.
- The MDD tool comes with a functional test tool that can adapt to machine-generated UI control identifiers.
