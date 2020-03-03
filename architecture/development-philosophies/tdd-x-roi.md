# TDD × ROI: Is Test-Driven Development worth the money?

(original article: https://medium.com/crowdbotics/tdd-roi-is-test-driven-development-worth-the-money-d535c8d5a5f)

Weighing the cost of production errors versus upfront development overhead.

Test-Driven Development has many advantages, undoubtedly. However, one of the significant problems that are standing in the way of its implementation is the fact that writing unit tests is more time-consuming than the traditional approach to development. It is possible that creating unit tests could take as much as twice of the time it would take to write the code without unit tests. And this is not counting the time needed for the team training and changing the team’s approach.

How often do we hear:

*"test coverage of the code is lower because we wanted to make our software cheaper or faster (or, maybe... both)"*

Or:

*"we do not write unit test - it takes too much time"*

Let’s ask ourselves a question: Is this how we really save the money? Is TDD worth it?

## The cost of the change

In the early 80s, Barry Boehm published statistics proving that the cost of changes and bug-fixing in the applications is rising significantly during the software lifetime. The corporations like Hewlett-Packard, IBM, Hughes Aircraft and TRW did the analysis pointing out that the price of the change in the software is rising with the transition to the next phase of the iterative cascade model (a.k.a. waterfall model):

- business requirements
- analysis and design
- coding
- testing
- production

Cost of the code modification after phase of the analysis, coding, testing and, finally, giving it away to the client could be two hundred times higher (!) than when the change is unearthed during the business requirement definition phase. Of course, the value depends on many factors such as size and complexity of the project. In the worst-case scenario, the cost of the change increases exponentially.

Let’s illustrate the situation with an example: one page of the business requirements could translate into five pages of diagrams, 500 lines of source code, 15 pages of documentation and several dozens of test cases. Not only the phases of the projects are cascaded, but also the code issues. At least in a Waterfall model approach.

How could we reduce the cost of changes in the development project? In 1999 Kent Beck proposed flattening of the above chart with the implementation of his Extreme Programming techniques (XP). The ingredients that affect code flexibility and introduces low cost of change are:

- Code and its design simplicity, including K.I.S.S. (Keep It Simple, Stupid!) and Y.A.G.N.I. (You Ain't Gonna Need It!) principle.
- Automatic tests, thanks to which we could be certain that there are no defects, and we could significantly reduce the time of work done while manually testing the software.
- Experience in the changing environment, especially client’s requirements and changes in code design.

So let’s recap, can back ourselves up with statistics from 80s waterfall and waterfallish model projects, and from the cost reduction by using Extreme Programming paradigms. Nevertheless, this is not enough to clearly confirm (or deny) the TDD profitability hypothesis. Below is the wider perspective.

## Microsoft and IBM

In 2008, the experiment [Nagappan et al.] under the brand of Microsoft Research was conducted. The focus group of the research were IBM and Microsoft teams. Four teams were using TDD, and another four were not. All of the teams were similar to each other in size and velocity. The experiment was conducted on “live” projects that the teams were developing at that moment.

The teams were selected based on their different characteristics to achieve wider picture illustration. The teams:

Were either collocated or working remotely.
Had different development experience level, from low to high.
Had different domain experience level, from low to high.
Used different programming languages and environments: Java, C++, .NET.
Produced various types of applications: software drivers, system software, Internet service, and desktop application.

The findings were indeed interesting:

- TDD teams were creating software with fewer errors.  
> IBM team did 40% fewer defects than non-TDD team,
- Microsoft team: 60–90% (fewer defects than non-TDD fellows).
- TDD teams spent 15–33% more time to write the code.
- The important aspect in improving the quality was the creation of the automated test infrastructure, i .e. unit, integration and functional tests.
- The teams that continued to use TDD after the experiment experienced a lower amount of defects in production.
- The interesting information came from the IBM team: after the experiment, some of the team members stopped running the regression unit tests. The situation resulted in the higher amount of defects in production.

## Small project in pairs

Another experiment [Boby et al.] was conducted among 24 experienced software developers who were challenged to write small Java application. The pairs of developers created the code, where one pair was writing the code using the TDD, and another pair didn’t. Three different companies were involved in conducting the tests. The authors of the experiment prepared 20 black box tests to verify the results.

The findings were:

- The applications written by the TDD developers passed on average 18% more black box test cases than applications written by non-TDD developers.

> After the experiment, 87.5% of the developers acknowledged that TDD helps in understanding the business requirements better. 95% of the developers recognised that TDD facilitated their work by reduction of time and energy for debugging.

## Meta-analysis

The meta-analysis of the TDD-oriented 27 thesis and three other meta-analysis is one of the most interesting elaboration on TDD [Rafique et al.] The theses were divided by the experiments done in the academic environment and the business environment. Out of all commonly available theses, the author filtered out those with the lowest credibility, i.e.:

- lack of enough data.
- lack of control group.
- lack of TDD process compatibility (components testing, testing during code creation but not before, etc.)

The author also did not take into account the group of theses that based their findings on existing elaborations. The result of this analysis was:

- TDD teams obtained higher quality indicators in comparison to non-TDD teams.
- The difference is clearly visible in case of business environment projects, were more lines of codes, more experienced developers and more significant tasks are usually present (in comparison to academic projects).
- Business environment projects consisting of 10’000–100’000 lines of codes scored 35–90% better quality for TDD teams.

## Summary: Is TDD worth it?

Reliable sources confirms that Test-Driven Development connects directly with the higher quality of the code resulting in fewer defects. The cost of the time overhead for writing the unit tests quickly pays because the cost of changes that need to be done later without automated test coverage is much higher, in pessimistic scenarios can ever rise exponentially.

There is nothing against to empirically verify the profitability of additional testing layers. However, it would be useful for every project to prove that the unit testing layer is worth expanding by integration tests, Acceptance Test-Driven Development (ATDD), Behavior-Driven Development (BDD), or, at least, consider such option on its own.

> In object-oriented languages, TDD is well examined, and the Return on Investment (ROI) of the projects is backed up with top quality.

Some theses and use cases are missing for the non-object oriented languages and ecosystems with the additional layers of automated tests, like integration or functional ones. We definitively need more data on such cases. For now, let’s red, green and refactor.
