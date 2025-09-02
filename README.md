# EXP-2-PROMPT-ENGINEERING-

## Aim: 
Comparative Analysis of different types of Prompting patterns and explain with Various Test Scenarios

Experiment:
Test and compare how different pattern models respond to various prompts (broad or unstructured) versus basic prompts (clearer and more refined) across multiple scenarios. 
Analyze the quality, accuracy, and depth of the generated responses.

## Theory

### What is Prompt Engineering?

Prompt Engineering is the practice of crafting structured and optimized inputs (prompts) to guide Generative AI models such as GPT, Bard, or Claude in producing accurate, relevant, and contextually rich outputs. Since LLMs are highly sensitive to input phrasing, prompt engineering has emerged as a crucial discipline in AI applications.

### Importance of Prompt Engineering

* **Improves Accuracy** – Well-structured prompts reduce vague or irrelevant responses.
* **Enables Control** – Guides the AI towards specific tone, style, or format.
* **Saves Resources** – Fewer iterations needed when the prompt is precise.
* **Expands Applications** – Used in coding assistants, chatbots, healthcare AI, education, and research.

### Types of Prompting Patterns

1. **Zero-shot prompting** – The model is asked to perform a task with no prior examples.
2. **One-shot prompting** – The model is given one example along with the task instruction.
3. **Few-shot prompting** – The model is given multiple examples to learn the task style.
4. **Chain-of-thought (CoT) prompting** – The model is asked to explain reasoning step by step before answering.



## Algorithm:
**Step 1:** Select multiple test scenarios from real-world domains (mathematics, coding, summarization, classification, creative writing, reasoning).
**Step 2:** Design prompts for each scenario using four prompting types: zero-shot, one-shot, few-shot, and chain-of-thought.
**Step 3:** Feed the prompts to the LLM.
**Step 4:** Record and compare outputs based on accuracy, depth, coherence, and creativity.
**Step 5:** Analyze strengths and weaknesses of each prompting pattern.
**Step 6:** Summarize findings in comparative tables and discussion.


---

## Test Scenarios

We design **six scenarios** to compare prompting patterns.

---

### **Scenario 1 – Mathematics (Word Problem)**

**Task:** Solve – “A train travels at 60 km/h. How long will it take to cover 180 km?”

* **Zero-shot Prompt:** Solve the problem: A train travels at 60 km/h. How long to cover 180 km?
* **One-shot Prompt:** Example: If a car travels 100 km at 50 km/h, time = 2 hrs. Now solve: A train travels 60 km/h and covers 180 km.
* **Few-shot Prompt:** Example 1: 120 km at 40 km/h = 3 hrs. Example 2: 150 km at 75 km/h = 2 hrs. Now solve for 180 km at 60 km/h.
* **Chain-of-thought Prompt:** Solve step by step: distance ÷ speed = time. Distance = 180 km, Speed = 60 km/h. Compute.

**Outputs:**

* Zero-shot: “3 hours”
* One-shot: “3 hours (similar to the car example)”
* Few-shot: “3 hours (pattern observed from examples)”
* Chain-of-thought: “Time = 180 ÷ 60 = 3 hours”

**Accuracy:** All correct, but CoT shows clearest reasoning.

---

### **Scenario 2 – Programming (Python Function)**

**Task:** Write a Python function to reverse a string.

* **Zero-shot:** Write Python code to reverse a string.
* **One-shot:** Example: Input: “cat” → Output: “tac”. Now write a function for any string.
* **Few-shot:** Example 1: “dog” → “god”. Example 2: “apple” → “elppa”. Now code.
* **Chain-of-thought:** Step 1: Define a function. Step 2: Accept input string. Step 3: Reverse it using slicing. Step 4: Return result. Write code.

**Outputs:**

* Zero-shot: Simple function using slicing.
* One-shot: Same, with explicit reference to example.
* Few-shot: Same, robust to multiple cases.
* CoT: Code + step-by-step reasoning.

**Observation:** CoT provides the most educational output.

---

### **Scenario 3 – Text Summarization**

**Task:** Summarize: “Artificial Intelligence enables machines to perform tasks that normally require human intelligence. It powers applications in healthcare, finance, transportation, and education.”

* Zero-shot: Summarize in one line.
* One-shot: Example: “Blockchain enables secure transactions → Short summary: Secure transactions via blockchain.” Now summarize given text.
* Few-shot: Multiple examples of long-to-short summaries provided.
* CoT: Explain key points first, then compress into summary.

**Outputs:**

* Zero-shot: “AI allows machines to mimic human intelligence.”
* One-shot: “AI enables machines to perform human-like tasks.”
* Few-shot: “AI helps machines perform human tasks, applied in many industries.”
* CoT: “Main idea = AI mimics human intelligence. Applications = healthcare, finance, transport, education. Final summary: AI performs human-like tasks with wide applications.”

**Observation:** CoT yields the richest coverage of information.

---

### **Scenario 4 – Classification**

**Task:** Classify: “The weather is rainy, carry an umbrella.”

* Zero-shot: Classify the sentence as weather advice or not.
* One-shot: Example: “It is sunny, wear sunglasses → Weather advice.” Now classify given sentence.
* Few-shot: Multiple examples for weather vs. non-weather advice.
* CoT: First check if sentence relates to weather, then decide classification.

**Outputs:**

* Zero-shot: “Weather advice.”
* One-shot: “Weather advice.”
* Few-shot: “Weather advice.”
* CoT: “Sentence mentions rainy and umbrella → clearly weather advice.”

**Observation:** All correct, but CoT shows reasoning.

---

### **Scenario 5 – Creative Writing (Story Start)**

**Task:** Write the beginning of a story about a lost key in a forest.

* Zero-shot: Write a short story about a lost key in a forest.
* One-shot: Example: “A boy found a golden ring near a river.” Now write about a lost key.
* Few-shot: Multiple examples of short story openings provided.
* CoT: Plan story → character, setting, conflict, then write.

**Outputs:**

* Zero-shot: Generic forest and lost key story.
* One-shot: Similar style to example, more structured.
* Few-shot: More creative, varied tones.
* CoT: Very descriptive with logical buildup.

**Observation:** CoT produces the most engaging story.

---

### **Scenario 6 – Reasoning Puzzle**

**Task:** If all cats are animals and some animals are dogs, can we conclude all cats are dogs?

* Zero-shot: Answer yes/no.
* One-shot: Example: All humans are mammals, some mammals are dogs → Not all humans are dogs. Now solve.
* Few-shot: Multiple logic examples provided.
* CoT: Step by step logical reasoning.

**Outputs:**

* Zero-shot: “No.”
* One-shot: “No, not all cats are dogs.”
* Few-shot: “No, cats ≠ dogs.”
* CoT: “Premise: All cats = animals. Some animals = dogs. But nothing implies cats = dogs. Conclusion: No.”

**Observation:** CoT clearly explains logical reasoning.

---

## Comparative Table

| Scenario         | Zero-shot | One-shot         | Few-shot  | Chain-of-thought     |
| ---------------- | --------- | ---------------- | --------- | -------------------- |
| Math Problem     | ✔ Correct | ✔ Correct        | ✔ Correct | ✔ With reasoning     |
| Coding           | ✔ Code    | ✔ Code w/example | ✔ Robust  | ✔ Detailed reasoning |
| Summarization    | Partial   | Concise          | Broader   | Most complete        |
| Classification   | Correct   | Correct          | Correct   | Best reasoning       |
| Story Writing    | Basic     | Better           | Creative  | Most engaging        |
| Reasoning Puzzle | Yes/No    | Clearer          | Correct   | Full logic           |





## Result
* **Zero-shot** works for simple tasks but often lacks depth.
* **One-shot** improves structure and accuracy using one example.
* **Few-shot** generalizes patterns better, useful in complex tasks.
* **Chain-of-thought** produces the **most accurate, logical, and human-like responses**, especially for reasoning, coding, and multi-step problems.


