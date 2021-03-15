## Week 2 Goals

Steps to learning
Concrete
Concept
^^These are things that you come across everyday as a developer - google, stackoverflow, blogs, videos etc

Skills - feedback, coaching, code reviews
Behaviour

Continue reflection on learning goals and use this to model what I work on each day.

By the end of the week all developers can:

**Use all of week 1's skills (don't underestimate the importance of this)** - Used Encapsulation, TDD and pair pgrogramming

- This week is a continuation of week 1 topics

List of week 1 skills to review and further learn if needed
- TDD coding - ensure all code is test driven
- Encapsulation
- SRP

Make sure these are reviewed an I can evidence them by:
- Putting them into practice
- Explaining the concepts

**Break one class into two classes that work together, while maintaining test coverage** - Extracting class using domain models.

- Think more about how several classes interact with one another.
- What does it mean if 2 classes are working together
- What method should be in what class?
- RSpec writing tests - process workshops

- Look at Rspec practicals
- Do further research
- Udemy rspec??

**Unit test classes in isolation using mocking** - Lots done over the weekend

- Do Mocking and mocking with RSpec workshops

**Explain some basic OO principles and tie them to high level concerns (e.g. ease of change)** - Can explain polymorphism and encapsulation

- Going further into object oriented design
- how classes can interact together
- Testing relationships
- Polymorphism
- Ease of change

**Review another person's code and give them meaningful feedback** - done on Monday

- Read more into rubric
- Understand how to give feedback or help my pair partner
- Read process workshop info

**Get a review this week**

- Reach out to a coach this week

## Evidence

Oyster Card -- challenge 15 and out
End of unit challenge - completed

### Daily Plans

**Monday 8th March**

GOAL: Seek to understand where I struggled with Airport challenge & understand feedback
PLAN: Break down and understand what is actually happening in the code/test
EVIDENCE: Can logically understand and code the rest of the challenge
Learnings: Had code review and started pair programming task. There are times when i really understand the attributes and time when i don't. This will come with experience.

**Tuesday 9th March**

GOAL: Attend EQ workshop, Learning by building RSpec
PLAN: Work through practical
EVIDENCE: Can finish 2 challenges

**Wednesday 10th March**

GOAL: Attend Domain Models Workshop. Self-led --> look at OO relationships practical x 2
PLAN: Finish BOTH practicals and determine further reading/learning
EVIDENCE: Can finish BOTH challenges
LEARNING: Finished one challenge, the pair programming has reached the point of polymorphism so looking into it more on Thursday

**Thursday 11th March**


GOAL: Mocking and double workshop. Continue looking into polymorphism/challenge 14
PLAN: Research polymorphism, speak to Sean
EVIDENCE: Can complete challenge 14 with understanding, can write short blog post on subject
LEARNING: Went through the practical and speaking to Sean, it's important to map out user stories and plan properly before committing to changes/starting a project.

Determined what should move to journey class and re-wrote the methods from scratch. Moved the journey hash to intialized and initialised a new journey instance when oystercard instance is created.

Set the entry and exit station arguements as the value for the methods within journey that define the values for start and finish of journey.

Changed in_journey to be dependent on an entry_station value within journey.

Made conditional in touch_in and touch out based on in_journey being true or false to determine if penalty charge is applied. So if touch_in is called whilst in_journey is true then that would mean the user hasn't touched out.

In this case decut is called with a value of 6 and the incomplete journey is pushed into journey history

Refactored into private methods - using encapsulation and SRP.
User story used polymorphism and forwarding.
Need to look more at OO principles and mocking.

**Friday 12th March**


GOAL: Focus on working through Polymorphism and OO principles work
PLAN: Finish OO Relationships (Forwarding, Polymorphism) practical, and Polymorphism workshop. If time work through Dependency injection and OOP3 delegate.
EVIDENCE: Can write blog post on polymorphism. Can complete challenges
LEARNING: Worked through challenges on Polymorphism and made good progress. Started Dependency injection workshop. Made slow progress in pairing. Lots of debugging.

**Weekend**

Takeway Challenge - Enure proper planning with domain modelling and README
Workshops and practicals on mocking and refactoring
If time start Udemy RSpec course.
Write blog post on polymorphism
