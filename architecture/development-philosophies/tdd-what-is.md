# Test Driven Development: what it is, and what it is not.

(original article: https://www.freecodecamp.org/news/test-driven-development-what-it-is-and-what-it-is-not-41fa6bca02a2/)

Test driven development has become popular over the last few years. Many programmers have tried this technique, failed, and concluded that TDD is not worth the effort it requires.

Some programmers think that, in theory, it is a good practice, but that there is never enough time to really use TDD. And others think that it is basically a waste of time.

If you feel this way, I think you might not understand what TDD really is. (OK, the previous sentence was to catch your attention). There is a very good book on TDD, Test Driven Development: By Example, by Kent Beck, if you want to check it out and learn more.

In this article I will go through the fundamentals of Test Driven Development, addressing common misconceptions about the TDD technique. This article is also the first of a number of articles I’m going to publish, all about Test Driven Development.

## Why use TDD?

There are studies, papers, and discussions about how effective TDD is. Even though it is definitely useful to have some numbers, I don’t think they answer the question of why we should use TDD in the first place.

Say that you are a web developer. You have just finished a small feature. Do you consider it enough to test this feature just by interacting manually with the browser? I don’t think it’s enough to rely just on tests done by developers manually. Unfortunately this means that part of the code is not good enough.

But the consideration above is about testing, not TDD itself. So why TDD? The short answer is “because it is the simplest way to achieve both good quality code and good test coverage”.

The longer answer comes from what TDD really is… Let’s start with the rules.

## Rules of the game


Uncle Bob describes TDD with three rules:

- You are not allowed to write any production code unless it is to make a failing unit test pass.
- You are not allowed to write any more of a unit test than is sufficient to fail; and compilation failures are failures.
- You are not allowed to write any more production code than is sufficient to pass the one failing unit test.

I also like a shorter version, which I found here:

- Write only enough of a unit test to fail.
- Write only enough production code to make the failing unit test pass.

These rules are simple, but people approaching TDD often violate one or more of them. I challenge you: can you write a small project following strictly these rules? By small project I mean something real, not just an example that requires like 50 lines of code.

Those rules define the mechanics of TDD, but they are definitely not everything you need to know. In fact, the process of using TDD is often described as a Red/Green/Refactor cycle. Let’s see what it is about.

## Red, Green, Refactor cycle

### Red phase

In the red phase, you have to write a test on a behavior that you are about to implement. Yes, I wrote behavior. The word “test” in Test Driven Development is misleading. We should have called it “Behavioral Driven Development“ in the first place. Yes, I know, some people argue that BDD is different from TDD, but I don’t know if I agree. So in my simplified definition, BDD = TDD.

Here comes one common misconception: “First I write a class and a method (but no implementation), then I write a test to test that class method”. It actually doesn’t work this way.

Let’s take a step back. Why does the first rule of TDD require that you write a test before you write any piece of production code? Are we TDD people maniacs?

Each phase of the R.G.R. cycle represents a phase in the code’s lifecycle and how you might relate to it.

In the red phase, you act like you’re a demanding user who wants to use the code that’s about to be written in the simplest possible way. You have to write a test that uses a piece of code as if it were already implemented. Forget about the implementation! If, in this phase, you are thinking about how you are going to write the production code, you are doing it wrong!

It is in this phase where you concentrate on writing a clean interface for future users. This is the phase where you design how your code will be used by clients.

This first rule is the most important one and it is the rule that makes TDD different from regular testing. You write a test so that you can then write production code. You don’t write a test to test your code.

Let’s look at an example.

```js
// LeapYear.spec.js
describe('Leap year calculator', () => {
  it('should consider 1996 as leap', () => {
    expect(LeapYear.isLeap(1996)).toBe(true);
  });
});
```

The code above is an example of how a test might look in JavaScript, using the Jasmine testing framework. You don’t need to know Jasmine - it is enough to understand that ```it(...)``` is a test and ```expect(...).toBe(...)``` is a way to make Jasmine check if something is as expected.

In the test above, I’ve checked that the function ```LeapYear.isLeap(...)``` returns ```true``` for the year 1996. You may think that 1996 is a magic number and is thus a bad practice. It is not. In test code, magic numbers are good, whereas in production code they should be avoided.

That test actually has some implications:

- The name of the leap year calculator is ```LeapYear```
- ```isLeap(...)``` is a static method of ```LeapYear```
- ```isLeap(...)``` takes a number (and not an array, for example) as an argument and returns ```true``` or ```false``` .

It’s one test, but it actually has many implications! Do we need a method to tell if a year is a leap year, or do we need a method that returns a list of leap years between a start and end date? Are the name of the elements meaningful? These are the kinds of questions you have to keep in mind while writing tests in the Red phase.

In this phase, you have to make decisions about how the code will be used. You base this on what you really need at the moment and not on what you think may be needed.

Here comes another mistake: do not write a bunch of functions/classes that you think you may need. Concentrate on the feature you are implementing and on what is really needed. Writing something the feature doesn’t require is over-engineering.

What about abstraction? Will see that later, in the refactor phase.

### Green phase

This is usually the easiest phase, because in this phase you write (production) code. If you are a programmer, you do that all the time.

Here comes another big mistake: instead of writing enough code to pass the red test, you write all the algorithms. While doing this, you are probably thinking about what is the most performing implementation. No way!

In this phase, you need to act like a programmer who has one simple task: write a straightforward solution that makes the test pass (and makes the alarming red on the test report becomes a friendly green). In this phase, you are allowed to violate best practices and even duplicate code. Code duplication will be removed in the refactor phase.

But why do we have this rule? Why can’t I write all the code that is already in my mind? For two reasons:

- A simple task is less prone to errors, and you want to minimize bugs.
- You definitely don’t want to mix up code which is under testing with code that is not. You can write code that is not under testing (aka legacy), but the worst thing you can do is mixing up tested and untested code.

What about clean code? What about performance? What if writing code makes me discover a problem? What about doubts?

Performance is a long story, and is out of the scope of this article. Let’s just say that performance tuning in this phase is, most of the time, premature optimization.

The test driven development technique provides two others things: a to-do list and the refactor phase.

The refactor phase is used to clean up the code. The to-do list is used to write down the steps required to complete the feature you are implementing. It also contains doubts or problems you discover during the process. A possible to-do list for the leap year calculator could be:

```
Feature: Every year that is exactly divisible by four is a leap year, except for years that are exactly divisible by 100, but these centurial years are leap years if they are exactly divisible by 400.

- divisible by 4
- but not by 100
- years divisible by 400 are leap anyway

What about leap years in Julian calendar? And years before Julian calendar?
```

The to-do list is live: it changes while you are coding and, ideally, at the end of the feature implementation it will be blank.

### Refactor phase

In the refactor phase, you are allowed to change the code, while keeping all tests green, so that it becomes better. What “better” means is up to you. But there is something mandatory: you have to remove code duplication. Kent Becks suggests in his book that removing code duplication is all you need to do.

In this phase you play the part of a picky programmer who wants to fix/refactor the code to bring it to a professional level. In the red phase, you’re showing off your skills to your users. But in the refactor phase, you’re showing off your skills to the programmers who will read your implementation.

Removing code duplication often results in abstraction. A typical example is when you move two pieces of similar code into a helper class that works for both the functions/classes where the code has been removed.

For example the following code:

```js
class Hello {
  greet() {
    return new Promise((resolve) => {
      setTimeout(()=>resolve('Hello'), 100);
    });
  }
}

class Random {
  toss() {
    return new Promise((resolve) => {
      setTimeout(()=>resolve(Math.random()), 200);
    });
  }
}

new Hello().greet().then(result => console.log(result));
new Random().toss().then(result => console.log(result));
```

could be refactored into:

```js
class Hello {
  greet() {
    return PromiseHelper.timeout(100).then(() => 'hello');
  }
}

class Random {
  toss() {
    return PromiseHelper.timeout(200).then(() => Math.random());
  }
}

class PromiseHelper {
  static timeout(delay) {
    return new Promise(resolve => setTimeout(resolve, delay));
  }
}

const logResult = result => console.log(result);
new Hello().greet().then(logResult);
new Random().toss().then(logResult);
```

As you can see, in order to remove the ```new Promise``` and ```setTimeout``` code duplication, I created a ```PromiseHelper.timeout(delay)``` method, which serves both ```Hello``` and ```Random``` classes.

Just keep in mind that you cannot move to another test unless you’ve removed all the code duplication.

## Final considerations

In this section I will try to answer to some common questions and misconceptions about Test Drive Development.

### T.D.D. requires much more time than “normal” programming!

What actually requires a lot of time is learning/mastering TDD as well as understanding how to set up and use a testing environment. When you are familiar with the testing tools and the TDD technique, it actually doesn’t require more time. On the contrary, it helps keep a project as simple as possible and thus saves time.

### How many test do I have to write?

The minimum amount that lets you write all the production code. The minimum amount, because every test slows down refactoring (when you change production code, you have to fix all the failing tests). On the other hand, refactoring is much simpler and safer on code under tests.

### With Test Driven Development I don’t need to spend time on analysis and on designing the architecture.

This cannot be more false. If what you are going to implement is not well-designed, at a certain point you will think “Ouch! I didn’t consider…”. And this means that you will have to delete production and test code. It is true that TDD helps with the “Just enough, just in time” recommendation of agile techniques, but it is definitely not a substitution for the analysis/design phase.

### Should test coverage be 100%?

No. As I said earlier, don’t mix up tested and untested code. But you can avoid using TDD on some parts of a project. For example I don’t test views (although a lot of frameworks make UI testing easy) because they are likely to change often. I also ensure that there is very a little logic inside views.

### I am able to write code with very a few bugs, I don’t need testing.

You may able to to that, but is the same consideration valid for all your team members? They will eventually modify your code and break it. It would be nice if you wrote tests so that a bug can be spotted immediately and not in production.

### TDD works well on examples, but in a real application a lot of the code is not testable.

I wrote a whole Tetris (as well as progressive web apps at work) using TDD. If you test first, code is clearly testable. It is more a matter of understanding how to mock dependencies and how to write simple but effective tests.

### Tests should not be written by the developers who write the code, they should be written by others, possibly QA people.

If you are speaking about testing your application, yes it is a good idea to ask other people to test what your team did. If you are speaking about writing production code, then that’s the wrong approach.
