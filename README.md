# EXP-2-PROMPT-ENGINEERING-

## Aim: 
Comparative Analysis of different types of Prompting patterns and explain with Various Test Scenarios

Experiment:
Test and compare how different pattern models respond to various prompts (broad or unstructured) versus basic prompts (clearer and more refined) across multiple scenarios. 
Analyze the quality, accuracy, and depth of the generated responses.


## Algorithm:
1. **Select Prompting Patterns to Compare**

   * Zero-shot prompting (no examples, direct instruction).
   * Few-shot prompting (include examples before the query).
   * Chain-of-thought prompting (ask the model to “think step by step”).
   * Role-based prompting (assign roles, e.g., “You are a teacher…”).
   * Refined/basic prompting (clearer instructions vs vague).

2. **Choose Test Scenarios**

   * Scenario A: Factual Q\&A (e.g., “Explain Newton’s 3 laws”).
   * Scenario B: Creative writing (e.g., “Write a poem about the ocean”).
   * Scenario C: Problem-solving (e.g., “Solve 12 + 18 / 3”).
   * Scenario D: Summarization (e.g., “Summarize a paragraph in one line”).

3. **Run Experiment**

   * Input same scenario with different prompting styles.
   * Collect generated responses.

4. **Evaluate Responses**

   * **Quality**: fluency, clarity.
   * **Accuracy**: correctness of information.
   * **Depth**: level of reasoning or creativity.

5. **Compare**

   * Highlight differences in response quality across prompting styles.



## Output
### **Scenario A – Factual Q\&A: Newton’s Laws**

* **Zero-shot Prompt:** *“Explain Newton’s laws.”*
  → “Newton’s laws are three rules about motion and force.” (Vague)

* **Few-shot Prompt:**
  *“Example: Law 1 – An object stays at rest unless acted on by a force.
  Now explain all Newton’s laws.”*
  → Gives clear explanation of all 3 laws with examples.

* **Chain-of-thought Prompt:** *“Explain Newton’s laws step by step.”*
  → Provides detailed reasoning and separate stepwise breakdown.

* **Role-based Prompt:** *“You are a physics teacher. Explain Newton’s 3 laws with real-world examples.”*
  → Response includes classroom-like examples (car braking, football kick).

---

### **Scenario B – Creative Writing: Poem about the Ocean**

* **Zero-shot:** Short, generic 2-line poem.
* **Few-shot:** Mimics given poetic style, richer language.
* **Chain-of-thought:** Builds imagery step by step, more coherent theme.
* **Role-based:** Writes poem as if from the perspective of a sailor.

---

### **Scenario C – Math Problem (12 + 18 / 3)**

* **Zero-shot:** Might output only final answer, sometimes wrong if careless.
* **Chain-of-thought:** Writes calculation: “18 / 3 = 6, then 12 + 6 = 18.” (Correct).

---

### **Scenario D – Summarization**

* **Zero-shot:** Generic one-liner, sometimes misses nuance.
* **Few-shot:** Matches structure of given example summary, more precise.
* **Role-based:** Summarizes in style requested (e.g., “as a news reporter”).



## Result
1. **Zero-shot prompting**: Fast but often vague or surface-level. Works well for simple queries, weak for complex reasoning.
2. **Few-shot prompting**: Improves accuracy and style consistency by showing examples.
3. **Chain-of-thought prompting**: Best for reasoning, math, or step-by-step explanations. Improves correctness.
4. **Role-based prompting**: Best for context-specific or creative tasks (teaching, storytelling, summarization in a style).
5. **Refined/clearer prompts always outperform broad or unstructured prompts.**

