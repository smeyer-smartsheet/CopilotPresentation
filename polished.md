---
marp: true
theme: default
class: lead
style: |
  section {
    font-size: 24px;
    background-color: #f0f0f0;
    color: #333;
  }
  h1 {
    color: #007acc;
  }
  h2 {
    color: #005f99;
  }
  ul {
    font-size: 20px;
  }
  .important {
    color: red;
    font-weight: bold;
  }
---

# Deep Dive in GitHub Copilot — Becoming a power user! 🚀

- **Presenters:**
    - Shuky Meyer — Principal Software Engineer
    - Divya Moorjany — Principal Machine Learning Engineer
- **Goal:**
    - Maximize efficiency and skills using GitHub Copilot through a deep dive into prompt engineering and advanced techniques. This demo will showcase how to leverage Copilot for more sophisticated and effective coding assistance.
- **Resources:**
    - [Slack](#askus-copilot) - Ask us anything!
    - [Internal Wiki](https://smar-wiki.atlassian.net/wiki/spaces/DEV/pages/71190085833/Copilot+Github+GenAI+Code+Companion) - Internal resources and tips.
    - [GitHub Copilot Docs](https://docs.github.com/en/copilot/using-github-copilot/best-practices-for-using-github-copilot) - Copilot Best practices (github.com).
---

# Agenda

1. **Introduction** – Getting started, GitHub Copilot basics
 - `/help`, `@workspace`, `/explain`, `@github`, etc..
2. **Prompt Engineering Basics** (Divya)
    – Building strong prompts for coding assistance.
3. **Advanced Copilot Hacks** (Shuky)
    – Unlocking advanced techniques and hidden features.
4. **Understanding LLMs** – (Shuky)
    - How a better understanding of context helps.
5. **Q&A & Live Problem-Solving** – (both)
    - Real-time examples and answers.

---

# Introduction 🌟

- **Presenters:**
  - Shuky – Principal Software Engineer with a lengthy background in HCI / Big Data.
  - Divya – Principal Machine Learning Engineer, <span class="important">bio?</span>
- **Overview:** Deep dive and become a power user with GitHub Copilot.

---

# Prompt Engineering Basics (Divya) 🤖
- **Prompt Structure:** Crafting effective prompts for targeted code assistance.
    - normal prompt: `Write a function that processes data`
    - improved prompt: `Write a Python function that takes a list of numbers and returns the sum of the even numbers.`
    - why: The 'improved prompt' is better because it provides specific details about the function's input and expected output, guiding Copilot to generate more accurate code.
- **Iteration & Refinement:** How to improve and refine prompts iteratively.
    - normal prompt: `Create a web server that handles requests`
    - improved prompt: `Create a simple Flask web server in Python that responds with "Hello, World!" when accessed at the root URL.`
    - why: The 'improved prompt' is better because it specifies the framework (Flask) and the exact behavior of the web server, making the task clear and focused.
---
# Prompt Engineering Basics (Continued...)
- **Few-Shot Prompting:** Provide examples to guide Copilot's output.
    - normal prompt: `Generate a SQL query to retrieve user data`
    - improved prompt: `Generate a SQL query to select all columns from the "users" table where the "age" is greater than 30.`
    - why: The 'improved prompt' is better because it includes an example of the desired SQL query, helping Copilot understand the specific requirements and generate accurate code.

- **Chain of Thought Prompting:** Get step-by-step logical code suggestions.
    - normal prompt: `Sort a list of numbers`
    - improved prompt: `Write a Python function that sorts a list of integers in ascending order. First, implement a function to find the smallest element, then use it to sort the list.`
    - why: The 'improved prompt' is better because it breaks down the task into smaller steps, guiding Copilot through the logical process needed to achieve the final result.

---
# Prompt Engineering Basics (Continued...)

- **Negative Examples:** Demonstrating how to guide Copilot by showing what not to do, helping it avoid common pitfalls and errors.
    - normal prompt: `Write a function to calculate the area of a circle using a fixed value for pi`
    - improved prompt: `Write a function to calculate the area of a circle. Do not use the value of pi as 3.14; instead, use the math library's pi constant.`
    - why: The 'improved prompt' is better because it explicitly instructs Copilot to avoid a common mistake and use a more accurate value for pi, leading to more precise code.

- **Prompt Chaining:** Linking prompts to build on previous context and generate more complex code.
    - normal prompt: `Create a login form for a website`
    - improved prompt: `Create an HTML login form with fields for username and password. Then, write a JavaScript function to validate the input and display an error message if the fields are empty.`
    - why: The 'improved prompt' is better because it builds on the initial task by adding a follow-up step, guiding Copilot to generate more comprehensive and functional code.

---

# Advanced Copilot Hacks (Shuky) 🛠️

1. **Marp for Documentation & Slides**
   - Use Copilot to auto-generate markdown slides (like this one!) with formatting.
   - Demo time! Generate slides, documentation, and more with Copilot.

2. **Unstructured Data to Structured Info**
   - Convert logs, JSON, or errors into readable, structured data.
   - Simplify parsing of HAR files using `jq` and Copilot.
   - Image -> Unstructured Text -> Copilot -> Structured Data

3. **Dynamic Prompting in Copilot Chat:**
   - Use Copilot in chat to generate code snippets, explanations, and more.

---

# Advanced Copilot Hacks Continued...(Shuky) 🛠️

4. **Bug-Fix Generation & Debugging**
   - Collect context like bug reports, error messages, and workspace data (#file, @workspace) to start debugging faster.
   - Explain This! (terminal) – Use Copilot to explain code snippets and debug complex issues.

5. **Glue Techniques for Automation & APIs**
   - Use Copilot to integrate systems and automate workflows by generating code across different systems.
   - Use output from one prompt to focus another.
   - Use #file, new editors, focused learning to improve prompting techniques.

---

# RECAP: Advanced Prompt Engineering & Copilot Hacks

- **Chain of Thought Prompting**: Break down complex tasks into smaller steps.
- **Role-based Prompting**: Assume a role to guide the model's responses.
- **Disambiguation Prompts**: Clarify ambiguous questions for more precise answers.

---

# RECAP: Real-World Applications

- **Code Generation**: Automate repetitive coding tasks.
- **Debugging Assistance**: Identify and fix bugs faster.
- **Documentation**: Generate comments and documentation for code.

---

# Best Practices

- **Iterate and Refine**: Continuously improve your prompts.
- **Provide Context**: Give the model enough information to generate accurate responses.
- **Use Examples**: Guide the model with few-shot examples.

---

# Common Pitfalls

- **Overly Broad Prompts**: Avoid vague questions.
    - *Example*: "Write some code."
    - *Why it's a pitfall*: The prompt is too general, leading to unpredictable and often irrelevant results.
    - *How to avoid*: Be specific about what you need. For example, "Write a Python function that calculates the factorial of a number."

- **Lack of Context**: Ensure the model has all necessary information.
    - *Example*: "Generate a function to process data."
    - *Why it's a pitfall*: Without context, Copilot may not understand what kind of data or processing is required.
    - *How to avoid*: Provide detailed context. For example, "Generate a Python function that takes a list of integers and returns a list of their squares."

- **Ignoring Iteration**: Refine prompts based on the model's output.
    - *Example*: Accepting the first suggestion without review.
    - *Why it's a pitfall*: The initial output may not be perfect or fully aligned with your needs.
    - *How to avoid*: Review and refine the prompts iteratively. For example, if the first output is not accurate, tweak the prompt to be more precise and try again.

---
# Common Pitfalls (Continued...)

- **Overlooking Edge Cases**: Not considering all possible scenarios.
    - *Example*: "Write a function to divide two numbers."
    - *Why it's a pitfall*: The function might not handle division by zero or non-numeric inputs.
    - *How to avoid*: Specify edge cases in the prompt. For example, "Write a Python function to divide two numbers, ensuring it handles division by zero by returning 'undefined'."

- **Misunderstanding Model Limitations**: Expecting Copilot to understand highly specialized or proprietary code.
    - *Example*: "Optimize this proprietary algorithm."
    - *Why it's a pitfall*: Copilot may not have the necessary context or knowledge about proprietary algorithms.
    - *How to avoid*: Provide as much context as possible and be prepared to manually refine the output. For example, "Optimize this sorting algorithm used in our proprietary system, which sorts large datasets efficiently."

---


# Future Trends

- **Enhanced Collaboration**: AI tools working seamlessly with human developers.
- **Increased Accessibility**: Making advanced AI tools available to non-experts.
- **Continuous Learning**: AI models that grow smarter and more efficient with each interaction.
- **Ethical AI**: Developing and deploying AI responsibly, ensuring fairness and transparency.
- **Scalability**: Creating AI systems that effortlessly handle increasing amounts of data and users.
- **Interoperability**: Making sure AI tools seamlessly integrate across various platforms and systems.
- **User-Centric Design**: Crafting AI tools that prioritize user experience and ease of use.
- **Security and Privacy**: Safeguarding user data and maintaining secure AI operations.

---

# Partnering AI Models with Copilot 🧠

- **Understanding Which Tool To Use:**
    - When to use Copilot, when to use other AI models, and how to combine them effectively.
    - Odd ways to use Copilot: generating poetry, recipes, etc.
    - Generating project plans
    - Generating UML
    - etc.

- **Contextualizing Outputs:**
   - Generate outputs with citations, summaries, and links to relevant sources.
   - Copilot can link to documentation, Stack Overflow, and other resources to provide context.
   - Copilot can link to source code in the workspace or on GitHub.
   - Copilot can generate comments and explanations.
   - Demystify complex branching logic and nested loops. (regex, uml, etc.)

---

# Resources

- [Vaswani et al., 2017, "Attention is All You Need"](https://arxiv.org/abs/1706.03762)
- [Brown et al., 2020, "Language Models are Few-Shot Learners"](https://arxiv.org/abs/2005.14165)
- [Chowdhery et al., 2022, "PaLM: Scaling Language Models with Pathways"](https://arxiv.org/abs/2204.02311)
- [Ouyang et al., 2022, "InstructGPT"](https://arxiv.org/abs/2203.02155)

---

# Q&A & Live Problem-Solving 🎤

- **Bring your questions!**
   Shuky & Divya will answer specific Copilot use cases, troubleshooting tips, and hacks.
- **Live Debugging:**
   We'll solve real issues in real-time using prompt techniques and Copilot’s advanced features.

---

# Thank You! 🙌

- **Questions? Reach out to us anytime!**
- Stay tuned for more advanced AI-powered development tips!
