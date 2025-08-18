---
title: "Fifty Quick Ideas To Improve Your Tests"
date: 2025-08-18T23:51:04.269+02:00
category: books
tags: []
excerpt: My highlights
---

## Page 283

> Just because something is difficult to test, we shouldn’t give up on capturing or expressing expectations. If an aspect of a system is difficult to test, this should not prevent people from discussing how well the system needs to perform before development starts. Even if you’re not going to actively measure an important aspect of quality, try to quantify it.


----
## Page 293

> If the target improvement is quantified, product managers can decide easily if it has been delivered, or if they need to prioritise more performance improvement work.


----
## Page 759

> An even worse problem is that specifying acceptance criteria like this pretty much defeats the point of user stories – to have a useful conversation. This level of detail is too low to keep people interested in discussing the underlying assumptions.


----
## Page 761

> Don’t describe how you will be testing something, keep the discussion focused on what you want to test instead.


----
## Page 772

> Such discussions are impossible to have when the difficult decisions are hidden behind clicks and page loads.


----
## Page 773

> It’s much faster to discuss what needs to be done instead of how it will be tested in detail, so keeping the discussion on a higher level allows the team to go through more stories faster, or in more depth.


----
## Page 780

> Decoupling how something will be tested from what is being tested significantly reduces future test maintenance costs. 2


----
## Page 817

> Avoid specifying input equivalence classes using intervals or formulas. Insist on concrete examples around the relevant boundaries instead.


----
## Page 885

> Acceptance criteria for stories are pretty useless if people can’t quickly understand their purpose.


----
## Page 897

> One of the best ways of untangling messy scenarios is to separate inputs and outputs.


----
## Page 904

> For information captured in tables, it’s good to pull inputs to the left and keep outputs on the right.


----
## Page 906

> For information captured in sentences or bullet points, put inputs at the top and outputs at the bottom.


----
## Page 908

> Ideally, have only one ‘when’ statement – that’s the action under test.


----
## Page 924

> A good solution for such situations is to ask ‘what happens instead?’ and validate the resulting condition. For example, instead of checking that a transaction does not exist after a period of time, check that a failed transaction was logged in an audit trail.


----
## Page 929

> Describing an alternative event instead of the absence of an event makes a test more reliable, because we can wait until an event happens instead of just waiting for a period of time.


----
## Page 988

> A good trick that prevents most accidental misuses of Given-When-Then is to use past tense for ‘Given’ clauses, present tense for ‘When’ and future tense for ‘Then’.


----
## Page 1007

> Each test should ideally be focused on one topic.


----
## Page 1008

> Watch out for multiple ‘When’ clauses, actions with conjunctions and scenario names that suggest a lack of focus. Break them down into several independent tests, and you will get a lot more value out of them. 3


----
## Page 1026

> If the individual steps do not show important variations, but are executed in sequence just because of the technical flow of implementation, then the entire block can be replaced


----
## Page 1043

> Tests with too many edge cases are difficult to understand and difficult to update. They are often also very brittle, so they will be costly to maintain.


----
## Page 1046

> Difficult testing is a symptom, not a problem.


----
## Page 1141

> Conciseness (of specification) Completeness (of test coverage) Coherence (of documentation)


----
## Page 1149

> A specification is optimal when it is as concise as possible.


----
## Page 1152

> A suite of acceptance tests needs to be complete in terms of its coverage of the target feature and of other features with which it is integrated.


----
## Page 1153

> Good acceptance tests ensure that not just the ‘happy path’ is checked, but all alternative paths and dead ends too.


----
## Page 1158

> Documentation needs to be coherent, meaning that each artifact is logical and understandable on its own, as well as consistent with others in its style and terminology.


----
## Page 1196

> Starting from the outputs makes it highly unlikely that a test will try to check many different things at once, as those different aspects will naturally be split into different outputs.


----
## Page 1198

> Writing outputs first helps to enforce many other aspects of good test design, such as focusing on a single action in a test and balancing clarity and completeness.


----
## Page 1220

> Mixing technical and business aspects in a single test gives teams the worst of both worlds. 4


----
## Page 1229

> Both the technical and the business aspects are important, and they both need to be tested, but teams will often get a lot more value out of two separate sets of tests rather than one mixed-role test.


----
## Page 1232

> keep tests for aspects that require business domain feedback in a human readable form, so domain experts can provide good feedback.


----
## Page 1238

> By splitting business and technical checks, teams get the opportunity to consolidate automation code.


----
## Page 1319

> Most database systems automatically isolate individual transactions, so tests running in different transactions are fully isolated.


----
## Page 1321

> Rolling back transactions after each


----
## Page 1395

> A pretty good solution for time-based constraints is to design the system to use a concept of business time instead of relying on the operating system clock.


----
## Page 1408

> A typical way of implementing business time is to separate out an application clock component, and make all other components use it instead of the operating system clock.


----
## Page 1424

> Their test execution system would run all the tests five times and mark the tests that passed at least once as OK. This is a very problematic strategy.


----
## Page 1444

> If possible, design the system so that it creates a file of this type under a temporary name, and when it completes and closes the file, renames it in accordance with the final expected output.


----
## Page 1459

> Wait for events, not time 5


----
## Page 1473

> Even if adding a few seconds to a single test doesn’t create a problem, this practice just does not scale. With a few hundred tests, the additional feedback delay can easily extend to hours.


----
## Page 1478

> Whenever possible, avoid waiting for a period of time, but instead wait for an event to happen.


----
## Page 1481

> Any arbitrary time limit will be either too short or too long, and cause tests to flicker or delay feedback unnecessarily.


----
## Page 1493

> If the remote process is not under your control, check if it generates any log files or additional outputs.


----
## Page 1497

> check if the page contains a particular title or element every 100 milliseconds.


----
## Page 1540

> Minimise UI interactions


----
## Page 1544

> UI interactions in tests often describe how something can be tested, not the actual purpose of the test


----
## Page 1557

> Keep UI actions only in tests that deal with UI-specific risks.


----
## Page 1575

> instead of launching a browser and waiting for asynchronous javascript events, simulate HTTP calls that the application would make to the back end.


----
## Page 1600

> One of the most important ideas is to apply a three-layer approach to automation: divide business- oriented decisions, workflows and technical interactions into separate layers.


----
## Page 1613

> Applications with a lot of messy user interface logic often need a good set of integration tests as well as business checks. 6


----
## Page 1620

> using Concordion, the top-level (human readable specification) can be reserved for the business- decision layer,


----
## Page 1675

> In addition, when specialists are hired to automate tests, they are often overwhelmed by work. Ten developers can produce a lot more code than a single person can test, so specialist automation often introduces a bottleneck.


----
## Page 1677

> The second scenario is horrible because developers stop caring about testing, and automated tests then just come to seem like a waste of time and money.


----
## Page 1680

> Separate automation specialists rarely have the insight into system internals, so the only option for them is to automate tests end-to-end. Such tests will be unnecessarily slow and brittle, and take a lot of time to maintain.


----
## Page 1685

> The only economically sustainable way of writing and automating hundreds of tests is to make developers responsible for doing it. Avoid using specialist groups and test automation experts.


----
## Page 1688

> When the same people are responsible for implementing and changing code and automating the related tests, tests are generally automated a lot more reliably and execute much faster.


----
## Page 1692

> In addition, when developers are responsible for automation, they will design the system to make it easy to control and observe functionality in the first place.


----
## Page 1702

> the entire team (including business stakeholders and testers) should be involved in deciding what needs to be tested.


----
## Page 1703

> External experts should only be hired to teach developers how to use a particular tool for automation, and provide advice on how best to design tests. 7


----
## Page 1710

> If the work of one team depends on the work of another, the first team’s work can get blocked in delivery, waiting for information or for an updated version of a component.


----
## Page 1770

> When the tests are organised according to business activities, not software work items, small business changes introduce small organisational changes for tests.


----
## Page 1863

> The gallery of examples served both as documentation to help new team members understand how to write good checks, but also as a database that anyone could quickly search to see if a feature was already supported or not.


----
## Page 1877

> There are always specific scenarios that might be better served by a different approach, because it might significantly improve readability or isolation.


----
## Page 1905

> For example, you can have business-oriented unit tests, or technical end-to-end checks.


----
## Page 1919

> Likewise, it’s perfectly fine to use tools commonly known as unit testing frameworks for more than just unit tests,


----
## Page 1932

> a very low test coverage figure is a useful piece of information, because it tells us that testing was not performed on part of the product.


----
## Page 1932

> A very high test coverage figure isn’t a particularly useful piece of information, because it doesn’t say anything about the type of testing that was performed,


----
## Page 1958

> Try to avoid publishing coverage metrics outside the team, as they are likely to be misused for setting targets or cross-team comparisons that don’t make any sense.


----
## Page 1974

> Start measuring the half-life of your tests, that is, their stability. Practically this means measuring the amount of change within your tests and their associated underlying features. 8


----
## Page 1986

> Tests that need to be frequently updated because they intermittently fail point to a potential problem with test design, or maybe even fragility in the underlying system.


----
## Page 1991

> create a heat map showing the amount of change in tests and/or failing tests grouped by business feature.


----
## Page 2005

> Instead of quarantining flickering tests, performing this analysis may point to a pattern of weakness or failure across tests that can be resolved by a change in the common automation code they share.


----
## Page 2034

> Similarly, if a test is difficult to understand, and doesn’t clearly communicate its purpose, pinpointing problems is very difficult when it fails.


----
## Page 2036

> Avoid using tools that allow people to knock up dozens of tests quickly, because such tests won’t be easy to maintain or understand.


----
## Page 2037

> Tests that are easy to understand will be easier to update and maintain.


----
## Page 2039

> However, improved readability of tests brings benefits far beyond just catching problems.


----
## Page 2050

> Name tests for search engine optimisation


----
## Page 2059

> Adding new tests for every change is a vicious circle, because it becomes even more difficult to understand what existing tests cover, so the problem just gets bigger over time.


----
## Page 2081

> A good heuristic for naming tests is to imagine a hierarchical navigation through the test suite, then collect all the names of the modules that would lead to a particular test. Add to that name whatever makes a particular test specific or different from the other tests in the same group. 9


----
## Page 2083

> tests describing net salary calculations in payroll could be named ‘Payroll – calculations – net salary – full-time employees’ and ‘Payroll – calculations – net salary – part-time employees’.


----
## Page 2086

> Conjunctions are a sign the test is trying to do too much, or lacks focus.


----
## Page 2089

> If people changed the test to make it pass, it was marked as bad.


----
## Page 2098

> Because contextual information is not really needed at the time when a test is written, tests rarely have any good introductory information.


----
## Page 2106

> Another common misuse of context in tests is to explain the mechanics of test execution.


----
## Page 2111

> Answer the question ‘why?’ in the context, and let the rest of the test deal with ‘what’ and ‘how’.


----
## Page 2116

> Unless all your colleagues have perfect memory, all this information is helpful even to the person who wrote a particular test.


----
## Page 2117

> Contextual information explaining the purpose of a test and why certain examples were chosen enables teams to discuss the tests more effectively with external stakeholders.


----
## Page 2128

> Avoid repeating the data or the information already provided by the body of the test. Instead, explain why you’ve chosen those particular examples, or that particular way of specifying the test.


----
## Page 2130

> avoid trying to force descriptions into the format of a user story. This almost never works well, because tests shouldn’t really be structured around work task hierarchies 10


----
## Page 2157

> A common set-up is to execute only the key examples using a primary continuous build job, and then run the secondary examples only if the primary job succeeds. With more complex models, the additional examples can also be split into several different build jobs to optimise feedback.


----
## Page 2167

> We tend to keep both groups of examples in the same file, but the key examples are on the top, and there is a clear separation between them and the additional scenarios.


----
## Page 2169

> It’s also useful to use tags to mark additional scenarios and examples. People can quickly execute only the scenarios without the tag for quick feedback, and continuous build tools can execute additional scenarios as secondary jobs.


----
## Page 2190

> Letting the chaos monkey out periodically allows teams to cause artificial crises in a safe environment, so they can improve their processes without having to put out fires at the same time.


----
## Page 2202

> For the best results, schedule such sessions periodically, time-box them and agree on a list of key risks to explore.

