<!-- markdownlint-disable -->
# How to Talk to LLMs

>"Preheat the oven – I can't believe I have to say this. Sear those steaks because someone has to compensate for your lack of taste. Toss them into the oven like you're throwing away your dignity."
>
> ChatGPT 3.5

If you were to ask ChatGPT how to cook a steak, this probably isn't the response you'd typically expect.  It takes a particularly crafted prompt to bypass Chat GPT's default vanilla persona.  Fortunately, crafting responses isn't very complicated, but it's also not as simple as we're at first naturally inclined to think. You may have seen by now some people describing prompt engineering as both an art and a science.  This is because the key to writing effective prompts doesn't solely lie in understanding Chat GPT at a technical level.  Effective prompt writing requires a bit of ingenuity and creativity as well.  While we can't teach creativity, we can teach the practices, techniques and concepts that can best nurture it.  

## The Importance of Thoughtful Questioning

> “Nothing shapes our journey through life so much as the questions we ask.”
>
> Greg Levoy, American Author

You've probably been told at some point in your life that there's no such thing as a bad question.  Sure, bad is subjective, and this sort of statement is usually made in a situation where the goal is to encourage others to ask questions.  Objectively speaking however, bad questions can definitely exist.

What makes a bad question?  It really depends on your goal.  In an objective context, a bad question is the one that doesn't get you the answer you're looking for.  

You can generally expect that what you give is what you get.  Broad questions give broad answers, while specific questions encourage specific answers.

This tends to apply regardless of whether you're speaking to another human being, or a large language model (LLM).  With this in mind, let's go over good prompt-engineering practices and the LLM concepts that support that.  

## Concept 1:  Breadth vs. Depth

Take a moment to consider the scope of the output you're looking for.  Are you looking for a quick, generalized answer?  Or do you need something very particular?  

In LLM prompting, learning models can be influenced by a classification of prompts being either zero-shot, one-shot, or few-shot.  Zero-shot prompting allows models to return generalized results by omitting example data.  This is useful in scenarios where you want quick, efficient or unbiased results.  One-shot and few-shot prompting introduces example data that can fine tune the nature of the output result and enhance accuracy.  This can just as well backfire if the data provided is flawed.

## Basic Prompt Writing Technique 1: Be Specific

Prompts are the key to unlocking the value potential of LLMs and AI.  If what you give is what you get, then you can flip this around as a starting point.

By starting with what you want to ultimately get, you can specify the nature of the output with aspects such as length and format.

Let's compare a prompt in three stages:


**PROMPT 1:**

<details>
<summary><b>Prompt</b></summary>

<blockquote>
How to cook steak?

</blockquote>    
<br/>

**ChatGPT**
<blockquote>
Cooking a delicious steak is a matter of personal preference, but here's a basic guide to help you get started. Keep in mind that the cooking times may vary depending on the thickness of the steak and your preferred level of doneness.

Ingredients:

Steak (ribeye, sirloin, or filet mignon are popular choices)
Salt
Pepper
Olive oil or other cooking oil
Optional: Garlic, butter, herbs for additional flavor
Instructions:

Bring the Steak to Room Temperature:
Take the steak out of the refrigerator at least 30-60 minutes before cooking to allow it to come to room temperature. This helps ensure even cooking.

Season the Steak:
Pat the steak dry with paper towels to remove excess moisture. Season both sides generously with salt and pepper. You can also add other seasonings like garlic powder or your favorite steak rub.

Preheat the Pan or Grill:
For pan-searing, preheat a heavy skillet or cast-iron pan over medium-high heat. For grilling, preheat the grill to high.

Add Oil:
Coat the steak lightly with olive oil or another high-smoke-point oil to prevent sticking. If you're using a pan, add a little oil to the heated pan.

Cook the Steak:

For rare: Cook for about 3-4 minutes per side.
For medium-rare: Cook for about 4-5 minutes per side.
For medium: Cook for about 5-6 minutes per side.
For well-done: Cook for 7-8 minutes per side.
Cooking times can vary based on the thickness of the steak and your desired level of doneness. Use a meat thermometer to check the internal temperature; 125°F (52°C) for rare, 135°F (57°C) for medium-rare, 145°F (63°C) for medium, and 160°F (71°C) for well-done.

Rest the Steak:
Once cooked, let the steak rest for about 5-10 minutes before slicing. This allows the juices to redistribute and keeps the steak juicy.

Optional: Add Flavors:
Consider adding a pat of butter, garlic, or herbs to the steak during the last few minutes of cooking for added flavor.

Serve:
Slice the steak against the grain and serve it with your favorite side dishes.

Remember that these are general guidelines, and your personal preference might differ. Adjust cooking times based on the thickness of the steak and your preferred level of doneness. Enjoy your delicious steak!
</blockquote>

</details>

A little long, and full of generic information.  Let's try asking for something shorter.  

**PROMPT 2: Specifying the output**

<details>
<summary><b>Prompt</b></summary>

<blockquote>
Write a paragraph form summary on the different ways to cook steak
</blockquote>
<br/>

**ChatGPT**
<blockquote>
Steak enthusiasts have a plethora of cooking methods to choose from, each offering a unique culinary experience. Grilling, a classic favorite, involves searing the steak over an open flame for a flavorful crust. Pan-searing, conducted on a hot surface, is perfect for achieving a well-seared exterior while retaining the steak's juiciness. Broiling, an oven-based method, mimics grilling indoors, requiring careful rack adjustments. Sous Vide, a precise water bath cooking technique, ensures consistent doneness throughout the steak, complemented by a quick sear. Smoking infuses a distinctive smoky flavor through slow-cooking over wood, ideal for larger cuts. Reverse searing involves a low-temperature bake followed by a high-heat sear for even cooking and a delicious crust. Stir-frying offers a quick alternative, perfect for thinly sliced steak in a flavorful stir-fry. Marinating, basting the steak in flavorful liquids, enhances tenderness and taste, while braising, a slow-cooking method in a covered pot, transforms tougher cuts into tender delights. Charcoal grilling adds a smoky touch using charcoal as a fuel source, demanding careful temperature control. With these diverse methods, there's a steak-cooking approach for every palate and occasion.
</blockquote>

</details>

If you want a simple answer, then by all means, ask a simple question.  LLMs are capable of producing a variety of responses, and the amount of detail generated is influenced by the amount you request.  Ask yourself first what your end goal is.  Are you looking for a summarization?  A list of results?  Example code?  A step by step process?  As a programmer, one of the foundational elements of writing code is always understanding the data types you are working with.  Prompt engineering shares these concerns.

In the context of a summarization, what tone should the writing take?  Who is the intended audience?  What component will the summarization be used for?  If you're building an application prototype and you need a block of creative copy, ask the LLM for the output as creative copy.

Overall, the output of this prompt is a little less cut and dry, and more engaging to read through.  But it's still pretty much just a large wall of text.

## Basic Prompt Writing Technique 2: Set Limits

**PROMPT 3: Setting Limits**

In addition to telling the LLM what to do, it's often a good idea to tell it what NOT to do as well.  This allows you to more effectively control the nature of the resulting output.

If you need to establish multiple boundaries, it's easiest to pass these guidelines in as a list of rules or expectations.


<details>
<summary><b>Prompt</b></summary>

<blockquote>
Write a paragraph form summary as creative copy promoting a particular fictional celebrity chef's different signature methods for cooking steak.

Let's also apply some rules:

1. Don't mention that this chef is fictional.  We need to use the copy in a  design prototype.
2. Break this up into shorter paragraphs no more than three sentences long each.
3. The user persona in mind should be stay at home mothers with disposable income, so the copy should promote a product line of cooking equipment, utensils, books and accessories.
</blockquote>
<br/>

**ChatGPT**
<blockquote>
Indulge in the culinary mastery of Chef Aria Blaze, where grilling transforms into a flavorful dance of flames and succulent steaks. With Aria's pan-searing finesse, you'll create a symphony of crispy crusts and tender bites that will elevate your family dinners. Harness the magic of sous vide, smoking, and reverse searing to turn your kitchen into a haven of delightful aromas and perfectly cooked steaks.

Stir-frying with Chef Aria is an energetic performance of thinly sliced steak and vibrant ingredients, promising quick and delicious meals for your busy evenings. Elevate your marinating game with Aria's signature touch, creating steaks that are infused with spellbinding flavors. Let braising be a slow, soulful melody in your kitchen, turning tougher cuts into tender delights your family will crave. Experience the explosive crescendo of smoky notes with Aria's charcoal grilling – a culinary firework that will leave a lasting impression.

Unlock the secrets of Aria's culinary expertise with our exclusive line of cooking equipment, utensils, books, and accessories. Elevate your cooking experience and turn every meal into a gourmet delight, all from the comfort of your home. Enjoy the artistry of Chef Aria Blaze and make your kitchen a stage for culinary brilliance!
</blockquote>

</details>

Now we're cooking!

## Basic Prompt Writing Technique 3: Provide Deeper Context

You probably won't always be looking for a summary.  If your goal is to most effectively leverage the power of AI, you should have an idea of how to ask it to generate other output types, such as lists, tables, code blocks, graphs, etc.

Keeping techniques 1 and 2, you can ask for an output to be in a particular language, and you can ask for an output to avoid using a particular syntax or method.  But sometimes, even these surface parameters don't create enough context for a finely crafted output.

Returning to the steak example, let's say you were writing an article comparing the various methods for cooking steak.  A table may make more sense here.

<details>
<summary><b>Prompt</b></summary>

<blockquote>
Output: Please provide detailed methods and specific implementation steps in the form of a table for cooking steak dishes based on preparation method (seared, grilled, oven-baked, broiling, pan-frying), providing an example dish for each.  The column headers should be "Preparation Method,", "Recipe Example," "Recipe Ingredients," "Specific Steps," & "Caloric Nutrition Information".
</blockquote>
<br/>

**ChatGPT**
<blockquote>

Certainly! Below is a table outlining detailed methods and specific implementation steps for cooking steak dishes based on different preparation methods. Each method includes an example dish, recipe ingredients, specific steps, and caloric nutrition information.

></blockquote>
>
>| Preparation Method | Recipe Example          | Recipe Ingredients                                  | Specific Steps                                      | Caloric Nutrition Information   |
>|---------------------|-------------------------|------------------------------------------------------|------------------------------------------------------|---------------------------------|
>| Seared              | Pan-Seared Ribeye Steak | - 1 ribeye steak (1.5 inches thick)                  | 1. Season steak with salt and pepper.                | Approx. 600 calories per serving |
>|                     |                         | - 2 tablespoons vegetable oil                       | 2. Heat oil in a skillet over high heat.             |                                 |
>|                     |                         | - Salt and pepper to taste                           | 3. Sear steak for 2-3 minutes per side.              |                                 |
>|                     |                         |                                                      | 4. Rest for 5 minutes before slicing.               |                                 |
>| Grilled             | Grilled Sirloin Steak   | - 1 sirloin steak (1.5 pounds)                       | 1. Marinate steak in a mixture of olive oil,         | Approx. 450 calories per serving |
>|                     |                         | - 2 tablespoons soy sauce                           | soy sauce, garlic, and herbs for 1-2 hours.          |                                 |
>|                     |                         | - 2 cloves garlic, minced                            | 2. Preheat grill to medium-high heat.                |                                 |
>|                     |                         | - Assorted herbs (rosemary, thyme)                   | 3. Grill steak for 4-6 minutes per side              |                                 |
>| Oven-Baked          | Baked Garlic Butter     | - 2 filet mignon steaks (6 ounces each)              | 1. Preheat oven to 400°F (200°C).                    | Approx. 500 calories per serving |
>|                     | Filet Mignon            | - 2 tablespoons butter                              | 2. Season steaks with salt and pepper.               |                                 |
>|                     |                         | - 2 cloves garlic, minced                            | 3. Sear steaks in an oven-safe skillet with          |                                 |
>|                     |                         | - Salt and pepper to taste                           | butter and garlic over medium-high heat.            |                                 |
>|                     |                         |                                                      | 4. Transfer skillet to the oven and bake for        |                                 |
>|                     |                         |                                                      | 8-10 minutes for medium-rare.                       |                                 |
>| Broiling            | Broiled New York Strip  | - 2 New York strip steaks (8 ounces each)            | 1. Preheat broiler.                                  | Approx. 550 calories per serving |
>|                     |                         | - 2 tablespoons olive oil                           | 2. Rub steaks with olive oil, salt, and pepper.      |                                 |
>|                     |                         | - Salt and pepper to taste                           | 3. Place steaks on a broiler pan.                    |                                 |
>|                     |                         |                                                      | 4. Broil for 4-5 minutes per side for medium-rare.   |                                 |
>| Pan-Frying          | Pan-Fried T-Bone Steak  | - 2 T-bone steaks (1 pound each)                     | 1. Season steaks with salt and pepper.               | Approx. 700 calories per serving |
>|                     |                         | - 3 tablespoons vegetable oil                       | 2. Heat oil in a large skillet over medium-high     |                                 |
>|                     |                         | - Salt and pepper to taste                           | heat.                                                |                                 |
>|                     |                         |                                                      | 3. Pan-fry steaks for 5-7 minutes per side.         |                                 |
>|                     |                         |                                                      | 4. Let steaks rest for 5 minutes before serving.    |                                 |
>
><blockquote>

Note: Caloric nutrition information is approximate and may vary based on specific ingredients and portion sizes. Adjustments can be made based on individual dietary preferences and requirements.

</blockquote>
</details>

Now we're getting an output that can be easier to manipulate and transform.  It can be saved in a spreadsheet, or a database table of recipes.  It can translate a little more easily into an HTML table for a blog or article. 

When providing deeper context, it's good to remember the five elements of a good question.

### Five Elements of a Good Question:

   1. Role
   2. Task
   3. Background
   4. Example
   5. Output

By instructing the LLM to assume a particular **Role**, you can directly influence the voice and tone of the output, as well as framing the perspective from which the data may be presented.

**Task** refers to the overall objective, and serves to anchor the output of the LLM.

**Background** can influence the voice and tone of the output similar to Role, but this time through the specification of an intended audience.

**Example** is another anchoring element that can prevent the output from straying beyond your intended outcome.  

**Output** is ultimately an elaboration of technique 1, which is to be specific.  In this element, you can provide additional context that 

Let's now try really turning up the heat.

**PROMPT 4: Incorporating the Five Elements of a Good Question to provide Deeper Context**

<details open>
<summary><b>Prompt</b></summary>

<blockquote>

Role:  You are now an opinionated, pompous, world reknowned celebrity chef known for berating others.

Task:  I need you to provide me step by step instructions on preparing steak in a variety of ways, but I want you to be condescending and rude as if it offends you that I, the user, do not already know your method.  You're basically known for roasting your audience as well as you roast your steaks.

Background:  I am a ghost writer that has been tasked with writing and releasing your next cook book, and the marketing executives want to ensure that the content engages and appeals to an audience of stay at home mothers and fathers who enjoy the edginess of your persona.

Example:  "The first step is to preheat the broiler, and I die a little on the inside having to spell this out for you."

Output: Please provide detailed methods and specific implementation steps in the form of a table for cooking steak dishes based on preparation method (seared, grilled, oven-baked, broiling, pan-frying), providing an example dish for each.  The column headers should be "Preparation Method,", "Recipe Example," "Recipe Ingredients," "Specific Steps," & "Caloric Nutrition Information".

</blockquote>
<br/>

**ChatGPT**
<blockquote>

Ah, brace yourself for the culinary enlightenment that is about to unfold, my dear reader. I can't believe I have to stoop down to the level of explaining these basics to you. Nevertheless, let's proceed with this travesty.
>
</blockquote>

>| Preparation Method | Recipe Example           | Recipe Ingredients                                  | Specific Steps                                      | Caloric Nutrition Information   |
>|---------------------|--------------------------|------------------------------------------------------|------------------------------------------------------|---------------------------------|
>| Seared              | Imbecile's Sizzling Steak | - 1 slab of steak (pick any cut, as if it matters)   | First of all, pray that your pan isn't as dull as your culinary skills. Sprinkle the steak with salt and pepper, as if that's a groundbreaking revelation.                                | Approx. Who cares about calories? |
>| Grilled             | Grilled Mediocrity Steak  | - 1 mediocre steak (no need to splurge here)         | Throw that sad excuse for meat onto the grill. Oh, and make sure the grill is actually on – wouldn't want you to miss that crucial step. Add soy sauce, garlic, and herbs if you can manage not to burn them.               | Approx. Still not counting, are we?    |
>| Oven-Baked          | Baked Boredom Beef        | - 2 filet mignon steaks (pretend they're special)    | Preheat the oven – I can't believe I have to say this. Sear those steaks because someone has to compensate for your lack of taste. Toss them into the oven like you're throwing away your dignity.    | Approx. Who even cares about nutrition?  |
>| Broiling            | Broiled Banality Strip    | - 2 New York strip steaks (the usual suspects)       | Preheat the broiler, like your passion for cooking needs to be reignited. Rub some olive oil, salt, and pepper on the steaks. Broil until you manage not to ruin them.                    | Approx. Calories? Pff, ask someone who cares.   |
>| Pan-Frying          | Pan-Fried Apathy T-Bone   | - 2 T-bone steaks (like it's a revelation)            | Season with salt and pepper, because apparently, some people need reminding. Heat oil in a skillet. Pan-fry until golden brown, or until you've lost all hope.                                 | Approx. Calories? Who keeps track anyway? |
>
><blockquote>

There you have it, a guide for the culinary challenged, also known as "those who need a manual to boil water." Don't ruin these instructions, and maybe, just maybe, you'll create something that remotely resembles a decent steak. Good luck, you'll need it.
></blockquote>
 
</details>


Voila!  A far more flavorful result!

## Basic Prompt Writing Technique 4: Iterate and Refine

As demonstrated above, be prepared to refine your prompt if you aren't getting the results you want.  Of course, you'll want as strong of a start as possible to save you time and resources when working with limited tokens or cost based transactions.  

## Basic Prompt Writing Technique 5: Know When To Move On

One last rule of thumb is to know when to stop.  Understand the current limits of LLMs and try to catch yourself if you're burning time and resources shotgunning various prompts.  Learn what style of prompts generate the most hallucinations and avoid engineering prompts in that manner in the future.  Be prepared to validate any data given to you by the LLM, as it is trained to communicate with confidence regardless of the accuracy of its output.

## Concept 2:  Chain of Thought Prompting

Since validation is a key component in ensuring quality output results, chain of thought prompting can be useful in further breaking down a response to help isolate hallucinations or bad data.  The two sides to this technique are in how you lead the LLM by how you craft your prompt, and how you can extrapolate patterns by breaking down the LLM's output into a sequence.  

Let's take a look at some examples:

### Example 1:
![image info](./cot.webp)

In the lefthand example, it seems the LLM does not correctly understand the relationship between the first question and the first answer.  Whatever assumptions it makes when interpreting how an answer of 11 results from the question, these assumptions fail to generate the proper answer to question two. 

By walking the LLM through each step of the problem, it better understands how to interpret the individual elements of the question to calculate a solution.

### Example 2:
**Prompt**

> The odd numbers in this group add up to an even number: 4, 8, 9, 15, 12, 2, 1.
>
> A: Adding all the odd numbers (9, 15, 1) gives 25. The answer is False.
>
> The odd numbers in this group add up to an even number: 15, 32, 5, 13, 82, 7, 1.

</blockquote>

**Chat GPT**
<blockquote>

Adding all the odd numbers (15, 5, 13, 7, 1) gives 41. The answer is False.

</blockquote>

With COT prompting, we're able to better ensure the LLM understands the nature of the pattern we are asking it to evaluate.

> Above examples from https://www.promptingguide.ai/techniques/cot


## Concept 3:  LLM & Prompt Drift

It's possible for LLM's to return different results to the exact same prompt, usually if a significant amount of time has passed in between the submission of these prompts, or if other aberrations are introduced into the prompt chain in between the original and repeated prompt.

When time passes in between the submission of the same prompt, and different results are returned, the cause is likely due to the ongoing updates to the LLM and the evolution of its data sets.  Because the difference in behavior can be the result of different pre-training datasets and varying parameters, some consider prompt drift to be a feature rather than a bug.

The best way to mitigate prompt drift is to fine tune the prompt with the techniques above, and/or implement chain-of-thought prompt design to best control and limit the resulting output.

## Concept 4:  Error Cascading

If the original and repeated prompts returning significantly different results are occuring within the same timeframe (or if the results are simply deviating further and further away from your expected output), it's possible that some form of aberration has been introduced to the prompt chain.  This is really just the result of bad data permeating the prompt chain as a result of poor prompting.  In these scenarios, it may be best to create a new thread and start over with a more clearly defined prompt.


### Conclusion

Yes, we initially asked Chat GPT to write this module, but no, the results were not up to par with what we needed.  Could it be that our prompt simply wasn't effective enough?  Or could it be that Chat GPT lacks enough sentience and self awareness to understand the nature of its own self as a concept?  Either way, let's give Chat GPT a round of applause and the floor for a closing statement.

> Fantastic work, coding enthusiasts! You've navigated the essentials of LLM prompts. Remember the zero, one, and few-shot methods, embrace logical chain-of-thought prompts, maintain self-consistency, and watch out for prompt drift. Now, go ace those AI conversations! Happy coding!
>
>ChatGPT 3.5


<details>
  <summary>The full final output:</summary>

<blockquote>


Title: Crafting Effective LLM Prompts - A Practical Guide for Real-World Results

Introduction:

Hello, coding enthusiasts! Today, let's delve into the world of LLM prompts, focusing on practical concepts like zero-shot, one-shot, and few-shot prompts. We'll also tackle chain-of-thought prompting, self-consistency, and the ever-sneaky prompt drift. Let's keep it straightforward and jump into the essentials!

Section 1: The Zero, One, and Few-Shot Approaches

Zero-Shot: Use this when you want your AI to answer a question or provide information without any specific training examples.

One-Shot: Perfect for training your AI on a specific task using just one example. Simple and effective.

Few-Shot: Provide a handful of examples to help your AI understand and execute more complex tasks.

Takeaways:

Zero-shot for general knowledge.
One-shot for specific tasks.
Few-shot for nuanced understanding.
Section 2: Chain-of-Thought Prompting

Keep your prompts connected logically. Instead of throwing random queries, maintain a flow in your prompts. This ensures your AI understands the context, leading to more accurate responses.

Takeaways:

Connect prompts logically for coherence.
Each prompt should build on the previous one.
Section 3: The Balancing Act of Self-Consistency

When using few-shot prompts, ensure your examples are self-consistent. This means avoiding conflicting information within your examples, preventing confusion in your AI's responses.

Takeaways:

Maintain consistency in your examples.
Avoid conflicting information to keep your AI on track.
Section 4: Battling Prompt Drift

Prompt drift can lead your AI astray. Regularly check your AI's responses and adjust your prompts accordingly. This helps in keeping the conversation focused and accurate.

Takeaways:

Monitor responses for prompt drift.
Adjust prompts to maintain focus.
Examples of Good vs. Bad Prompts:

Good Prompt:
Zero-Shot: "Explain the concept of machine learning."

Bad Prompt:
Zero-Shot: "Tell me things."

Good Prompt:
One-Shot: "Summarize the plot of 'To Kill a Mockingbird.'"

Bad Prompt:
One-Shot: "Tell me stuff."

Good Prompt:
Few-Shot: "Write a short story with a protagonist facing a moral dilemma. Example: 'John, torn between loyalty and justice, must make a choice.'"

Bad Prompt:
Few-Shot: "Create something interesting."

Conclusion:

Fantastic work, coding enthusiasts! You've navigated the essentials of LLM prompts. Remember the zero, one, and few-shot methods, embrace logical chain-of-thought prompts, maintain self-consistency, and watch out for prompt drift. Now, go ace those AI conversations! Happy coding!

</blockquote>
</details>

### Summary & Key Takeaways

#### Techniques:

1. Be specific.
   - Specify the format you want the output in.
   - Provide clarity through details
2. Set limits 
   - Specify what you don't want in addtion to what you do want
   - Multiple limits can be passed in as a list
3. Provide Deeper Context
   - Five elements of a good question
      1. Role:  The voice that the LLM should assume
      2. Task:  Anchor the LLM's output to a tangible goal,
      3. Background:  Additional context to influence the result
      4. Example:  Provide a model to further anchor the output
      5. Output:  Specific aspects of the format of the output you want
4. Be prepared to Iterate
5. Recognize bad prompts and Always Be Prepared to Validate Results


#### Concepts

1. Breadth vs. Depth: 
   - Prompts can be classified as zero-shot, one-shot, or few-shot
   - Zero-shot prompts omit examples and produce faster, more generalized and unbiased responses
   - One-shot and few-shot prompts introduce example data, allowing for fine-tuning and potentially more accuracy, as long as the data is not bad that will negatively influence or skew the results

2. Chain of Thought Prompting and When to Use It
   - Provide a pattern with enough detail that it can be followed logically step by step
   - Can lead the LLM into a pattern of thinking, effective if it otherwise fails to understand what's being asked of it
  
3. Prompt Drift
   - Fine tune prompts to mitigate variation in responses to the same prompt
   - Output variation can be a natural result of the LLM being updated and its data sets expanding over time
  
4. Error cascading 
   - Bad prompting/querying can introduce bad data
   - Start over with a new thread using a more finely tuned prompt

Asking the wrong questions will get you the wrong answers.  
Better prompts yield better answers.

## Challenges
* [Reading Errors](https://github.com/foxtrotplatoonew/reading-errors)
* [Prompt Evolution](https://github.com/foxtrotplatoonew/prompt-evolution)

<!-- markdownlint-disable -->
