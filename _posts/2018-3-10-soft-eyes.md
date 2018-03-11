---
layout: post
---

_"If you got soft eyes, you can see the whole thing. If you got hard eyes — you staring at the same tree missing the forest"_ -Detective Bunk, The Wire S-4, EP-2

### My First Post as an Automation Engineer
As a QA/SDET I have a hybrid role. For the SDET part we essentially write internal software for our team using the Ruby programming language and various web-driver libraries.

This software automatically runs a suite of test scenarios that we created to mimic a user interacting with our apps page, or our back end API where applicable.

Whenever our developers check in code to our dev environment (its first stop on its way to production) the suite runs against everything with their new code included.

The dev environment can be named anything, often it's something like _dev_, _qa1_, _integrationOne_, or **_Silo\_1_**.

### QA
This post is about the QA part of my job, and how I first approach new features that are given to me to test. This part of my job I would argue is much more complicated than the automation part.

For starters the execution is far more abstract, while the consequences of "bad" QA is most certainly NOT abstract.

Imagine data being blown away never to be recovered, or a single customer receiving hundreds of thousands of emails for things they did not purchase.

We could go deeper and talk about how the QA process informs what will be done at the automation step of my job (SDET), but that seems like a future topic.

### Object Names are for Humans
I love to write code, particularly code that tries to bring order to chaos, or my real favorite....code that tries to solve a problem that really does not have a clear _right_ answer. Which is why the process I'm going describe is important to me.

When I'm writing programs in Ruby, I think of it as defining objects and then defining the behavior of those objects. I like to think that the object name is for _humans_ while the behavior defined is for the _machine_.

In keeping with the theme of the quote at the top, we will define some objects as trees. All together those trees make a patch of forest someone ordered, which makes the forest the feature.

### The Trees in the Forest
As an engineer what really interests me are the elements that make up the forest and the things that affect them individually.

Things like- leaves (light and moister absorption rate), the type and quality of the soil (nutrient and sediment makeup), level of light pollution, prevailing winds and erosion....you can see the pattern. Changing any one of those things will have an impact, could be small, could be big.

Maybe changing the type of soil causes the tress to fair better in the summer but is worse for the grass, and maybe all the flowers die off and never come back (which _no-one_ saw coming!)

I am not a biologist but before I decide those things are not important I will need to observe them _not being_ important, and that observation would be useless if done exclusively up close..in the "weeds" as the coder in me would.

### Know something has been added. Assume nothing has changed.
My goal would be to interact with the environment knowing something has been _added_, but assuming nothing has _changed_.

If you read that and think that's a pretty naive way for quality assurance to go about observing something, you are right, we are approaching the addition of this feature with "Soft" eyes.

In approaching the forest assuming that nothing has changed allows us to have a clean slate...which is good because the list of observed changes will grow fast!

### Down from the clouds
I believe its good to start from a simple place, as it helps me to ask the questions that matter.

However it has been well documented that no plan survives the first few minutes of battle. In future posts we will see how that can play out in real life.

Names and details will be changed to protect the innocent :)
