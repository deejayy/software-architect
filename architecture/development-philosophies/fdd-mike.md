# A Practical example of Feature Driven Development

(original article: http://www.mike-dixon.com/2012/01/24/a-practical-example-of-feature-driven-development/)

Feature Driven Development (FDD) is often theorised about on many web sites with blog posts, articles and essays being published on a regular basis and this blog post will give you a much needed practical example of it in use.

One article that is worth pointing out is DZone’s Introduction to Feature Driven Development. This is part one of a two part article describing a theoretical project and a theoretical team and the first three of five steps to achieving Feature Driven Development. It is extremely well written and gives you some really good insight into what is needed.

In my experience, I find that when you take these theories and methodologies and apply them to real life situations and projects, that they need adapting and shaping to fit with what you are trying to deliver.

An example of this is when I was leading the Product Development across five different web sites and one development team. The way in which I had implemented the Kanban methodology was different for each site due to different stakeholders and different commercial strategies needing to be delivered.

Anyway, back to a practical example of Feature Driven Development.

The example that I am using is the build of Mousebreaker, a casual gaming site that utilised a mixture of Kanban and Feature Driven Development to quickly and effectively deliver a new web site with a new code base in 28 days.

Traditionally, my approach had always been to gather all requirements, build the infrastructure, then the code, and finally the front end for a web site.  This information gathering and the writing of functional and technical specs can take a long time to complete. Then, when the development begins, the whole spec needed to be delivered before the site could launch. By which time 6 months has passed and requirements may well have changed and what is delivered is not necessarily what the business or the market needs.

Feature Driven Development tries to get around this by defining the requirements as features, then the business owners and development teams prioritise these features into a backlog of work and then the developers deliver these features in the order that offers the most business value.

One thing to note is that there is some pre-work that needs to happen before development can start. The general technical approach needs to be agreed; technologies need to be discussed, terminology needs to be agreed and basic development, testing and live environments need to be created.

In addition, certain standards would have been discussed such as coding, SEO and accessibility standards and any automated testing. In addition, any front/back end frame works that will be used as well should also be discussed.

If you look at the Mousebreaker site, you will see that the primary user function is for the user to play flash games. So the first feature that was worked on was that the user needs to be able to play a game on a web page.

At first, the developers approach was to start building a database infrastructure that could be used for the whole site. They were also wanting designs for pages etc. You need to be careful here as that is not what was required by the feature. All the feature required was for the user to be able to play a game. Nothing else.

So to deliver this feature, all that was required was a static html page with some embed code that would allow a user to play a game. The game needed to be in a web facing folder.

Once complete and tested, the feature can then be released.

The next story was that a user needs to be able to play all games on a web page.

This is where the database gets created and the initial html page is turned into a template. Again, the developers only needed to create a database that delivers the feature’s requirement.

In the meantime, while the initial features were being delivered, the designers were working with the development and business teams to deliver the designs for the site. There was a further feature for the site to have a premium look and feel that eventually would need to be delivered which could be applied to the site around the templates that were being delivered.

This felt a little back to front, but you need to remember that we were delivering features in the order of business priority.

As the features kept being delivered, the site quickly started to take shape. Throughout the development, the business representatives were always attending the stand ups and were constantly making decisions on scope of work and what would be required for launch.

We found that the close collaboration between the business and the development team was the most effective way of managing scope and ensuring that what the dev team delivered is what was expected.

I have applied this form of Feature Driven Development many times and I find that it really works. You do need buy in and effort from the business owners, and you do need to make sure that the developers do only focus on what is required to deliver the features rather than architecting a full solution before understanding all the requirements.

This allows more of a front to back development process. Where the features take priority over the implementation. One thing that I would like to point out is that there would be occasions where future considerations are sometimes ignored or put to one side to get functionality out and that this may result in refactoring work further down the line.

The thing to remember is that you will have already delivered the highest business value functionality required at that point and that the business will understand that any refactoring work should also have a value and then a discussion can be had about options and whether this work needs to be done or not. If it does and it takes a longer period of time, then allowances should be made for this.

