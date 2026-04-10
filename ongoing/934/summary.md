---
title: "Judge the Judge: Building LLM Evaluators That Actually Work with GEPA — Mahmoud Mabrouk, Agenta AI (en)"
date: 2026-04-10T14:29:48.621+02:00
category: videos
tags: [LLM, AI evaluation, prompt optimization, GAPA, Agenta, customer support AI, policy compliance, machine learning, AI observability, AI calibration]
excerpt: "A detailed exploration of building calibrated LLM judges for AI reliability evaluation using prompt optimization and the GAPA algorithm, demonstrated on a customer support airline agent use case."
---

![thumbnail](https://i.ytimg.com/vi_webp/X4dEHRzBLmc/maxresdefault.webp?v=69d7b1e2)
[https://youtu.be/X4dEHRzBLmc?si=6qS3c90q9XAMnJhg](https://youtu.be/X4dEHRzBLmc?si=6qS3c90q9XAMnJhg)

<!--- My thoughts -->

## Content

### Introduction to LLM as Judges
Large Language Models (LLMs) can be used to monitor the reliability of AI agents in production by acting as judges determining whether outputs are hallucinated or compliant. However, naive usage often fails because an agent inherently cannot self-assess hallucinations without prior calibration. Therefore, building calibrated LLM judges calibrated against human annotations is crucial for both offline evaluation and online monitoring.

Mahmud, co-founder and CEO of Agenta, introduces an approach leveraging prompt optimization via the GAPA algorithm, aiming to develop reliable LLM judges that correlate well with human expert annotations. This improves development speed by automating and accelerating evaluation loops, ultimately enabling rapid detection of behavioral regression or improvement in AI systems.

### Use Case and Dataset
The practical example centers on a customer support airline agent benchmarked with the Towbench dataset—a complex real-world scenario involving 599 annotated conversation traces. The agent must adhere to strict airline policies managing reservations and customer interactions. Annotations indicate compliance or non-compliance with detailed reasoning, crucial for teaching the LLM to understand policy nuances.

### Defining Metrics and Annotation Workflow
Instead of broad metrics like hallucination rates, Mahmud highlights the importance of use-case-specific metrics designed by subject matter experts. For the airline agent, four error clusters are identified:
- Policy adherence issues
- Response style problems
- Information delivery failures
- Tool invocation errors

Each error type leads to a dedicated binary judgment (compliant/non-compliant) supported by annotation reasoning. This reduces complexity and improves the ability to train separate LLM judges effectively for each axis.

### The GAPA Optimization Algorithm
GAPA is inspired by genetic algorithms and operates via iterations of prompt mutation and merging:
1. Start with a seed prompt (e.g., one that assumes compliance by default).
2. Generate new candidate prompts through reflection—where the LLM analyzes failure cases and proposes improvements.
3. Evaluate candidates against batches of data and filter using a Pareto frontier approach that selects diverse candidates excelling on different tasks.
4. Merge prompts to combine strengths.

This process repeats until computational budget is exhausted, gradually enhancing the LLM judge's calibration and accuracy.

### Importance of Seed Prompt and Reflection Template
Mahmud found the initial seed prompt critically affects learning success. Starting with a prompt that assumes compliance unless proven otherwise avoids bias pitfalls. Also, custom reflection templates guiding the LLM refiner to understand specific policies and incorporate feedback from ground-truth annotations significantly improved optimization outcomes compared to default templates.

### Experimental Results
Starting from a naive judge with around 61% accuracy (biased toward compliance), optimization with GAPA improved accuracy to 74% and reduced bias by increasing non-compliance recall and precision. The Pareto frontier algorithm achieved 100% coverage on training tasks, although merging candidates into a single comprehensive prompt remains challenging.

### Challenges and Lessons Learned
- Data quality: Towbench data had noise, redundancies, and AI-generated annotations that complicated learning.
- Model size: Smaller or older models (e.g., GPT-3.5, deepseek) failed to adequately serve as judges or refiners.
- Cost: Running experiments with LLMs is expensive ($200-$300 for a single optimization run).
- Iterative debugging and parameter tuning are essential. Mahmud recommends visualizing intermediate candidate prompts and reasoning to guide improvements.
- Surprisingly, having explicit access to the agent's policy in the prompt sometimes reduced optimization effectiveness, possibly due to local minima entrapment.

### Final Recommendations
- Use larger models for refining prompts and smaller models for scoring to balance effectiveness and cost.
- Start optimization with a strong seed prompt embodying domain knowledge.
- Prioritize detailed human annotations including reasoning to enable the judge LLM to learn policy compliance effectively.
- Consider binary classification metrics over continuous scoring to simplify learning.
- Overfit initially on training data and focus on analyzing failures before scaling.

### Closing
Mahmud encourages readers to explore the Agenta open-source platform for managing prompt engineering, evaluation, and observability of LLM-driven agents. Optimizing LLM judges via algorithms like GAPA enables building more reliable AI systems that continuously improve through automated feedback loops. For those working on autooptimization or prompt improvements, Mahmud invites further discussion and experimentation.

