# EXP-2-PROMPT-ENGINEERING-

## Aim: 
Comparative Analysis of different types of Prompting patterns and explain with Various Test Scenarios

Experiment:
Test and compare how different pattern models respond to various prompts (broad or unstructured) versus basic prompts (clearer and more refined) across multiple scenarios. 
Analyze the quality, accuracy, and depth of the generated responses.


## Algorithm:
1. **Select Prompting Patterns**

   * Zero-shot prompting
   * Few-shot prompting
   * Chain-of-thought prompting
   * Role-based prompting
   * Refined/basic prompting

2. **Choose Specific Test Scenarios**

   * **Scenario A (Factual Q\&A):** *“Explain how Newton’s 2nd law of motion applies when pushing a shopping cart with different weights.”*
   * **Scenario B (Creative Writing):** *“Write a 4-line poem about a stormy night at sea.”*
   * **Scenario C (Problem Solving):** *“A worker completes a job in 12 days, another in 18 days. How many days if both work together?”*
   * **Scenario D (Summarization):** *“Summarize this paragraph in 1 line: ‘The rise of electric vehicles is transforming the automobile industry by reducing carbon emissions, lowering fuel dependency, and encouraging governments to invest in green infrastructure.’”*

3. **Run Experiment**

   * Give same scenario prompt using each prompting style.
   * Collect responses.

4. **Evaluate Responses**

   * **Quality** (clarity, fluency)
   * **Accuracy** (correctness, relevance)
   * **Depth** (reasoning, creativity, contextual detail)

5. **Compare**

   * Identify which prompting style gives the best performance per scenario.



## Output
### **Scenario A – Factual Q\&A**

Prompt: *“Explain how Newton’s 2nd law of motion applies when pushing a shopping cart with different weights.”*

* **Zero-shot:** “Newton’s 2nd law says force = mass × acceleration. More weight means harder to push.” (Very short, lacks detail).
* **Few-shot:** With example → explains how a 10 kg vs 30 kg cart requires more force for same acceleration.
* **Chain-of-thought:** “Newton’s 2nd law: F = m × a. If the cart is 10 kg and you want 2 m/s², F = 20 N. If 30 kg, F = 60 N. So more weight = more force.” (Stepwise, clear).
* **Role-based (Teacher):** “Imagine pushing an empty cart at the supermarket (easy). Now imagine it full of groceries (harder). That’s Newton’s 2nd law in action.”

---

### **Scenario B – Creative Writing**

Prompt: *“Write a 4-line poem about a stormy night at sea.”*

* **Zero-shot:** Simple 2 lines, “The sea is rough, the sky is dark.”
* **Few-shot:** Matches poetic rhythm, imagery: thunder, lightning, restless waves.
* **Chain-of-thought:** Builds mood step by step → imagery of storm, waves, sailor’s fear.
* **Role-based (Sailor’s POV):** Writes poem from perspective of sailor battling the storm.

---

### **Scenario C – Problem Solving**

Prompt: *“A worker completes a job in 12 days, another in 18 days. How many days if both work together?”*

* **Zero-shot:** “They take 7 days.” (May or may not explain).
* **Few-shot:** Shows example of combined work → correct answer: 7.2 days.
* **Chain-of-thought:** “Work rate = 1/12 + 1/18 = 5/36 job/day. So time = 36/5 = 7.2 days.” (Accurate).
* **Role-based (Math tutor):** Explains step by step with analogy (painting a wall together).

---

### **Scenario D – Summarization**

Prompt: *“Summarize this in 1 line: EVs reduce emissions, lower fuel use, push governments to fund green infrastructure.”*

* **Zero-shot:** “EVs are good for the environment.” (Too vague).
* **Few-shot:** “EVs cut emissions, reduce fuel reliance, and drive government investment in green energy.” (Precise).
* **Chain-of-thought:** Reads sentence, extracts 3 ideas, combines into concise 1-liner.
* **Role-based (News reporter):** “Governments are investing in green infrastructure as EVs reshape the auto industry.”




## Result
1. **Zero-shot prompting**: Quick but oversimplified, misses depth in factual and summarization tasks.
2. **Few-shot prompting**: Produces structured, style-consistent responses, especially useful in creative writing and summaries.
3. **Chain-of-thought prompting**: Best for **problem-solving and reasoning** tasks; ensures stepwise correctness.
4. **Role-based prompting**: Best for **engagement and contextual clarity** (teaching, storytelling, style-driven summaries).
5. **Conclusion**: Refined and specific prompts yield significantly better responses than vague/general ones.

