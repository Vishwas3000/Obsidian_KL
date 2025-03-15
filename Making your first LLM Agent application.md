[[LLM Creation]]
#CreateLLMAgent #OpenScource 
 When building a LLM agent application, there are four key components you need: 
- an agent core
- a memory module
- agent tools
- planning module.

### **What is LLM compiler-style approach fused planning and core**

 It is like a compiler, where tasks are broken down and optimised before execution
1. **Parsing & Analysis**: The LLM parses user input like a compiler parses code, extracting intent and structure.
2. **Task Optimization**: Similar to compiler optimizations (e.g., constant folding), redundant or inefficient steps are eliminated.
3.  **Intermediate Representation (IR)**: The query is transformed into structured plans (like AST or bytecode in compilers).
4. **Execution Planning**: The agent decides the best order and tools for execution, optimizing for latency and accuracy.
5. **Execution & Feedback**: The agent runs tasks efficiently, monitoring performance like a runtime optimizer.
### **Analogy: Why This Approach Works Well**

Think of this as **writing a script vs. running commands interactively**:

- **Compiler-style (Plan-Then-Execute)** → The LLM writes a structured script, and a different system runs it.
- **Fused approach (Plan-and-Execute Together)** → The LLM executes commands immediately, which can fail unpredictably.

This structured planning method makes it easier to debug, retry failed steps, and maintain flexibility in execution.


## Lang Flow
This is an opensource framework use to make a basic POC for making agents and llm based applications. This is a node based system for quick drag and drop.
