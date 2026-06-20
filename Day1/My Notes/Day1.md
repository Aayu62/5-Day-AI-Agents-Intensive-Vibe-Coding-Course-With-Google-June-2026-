# Day 1 Technical Notes: The New SDLC with Vibe Coding

---

## 1. Traditional SDLC vs. AI-Driven SDLC Changes (Page 20)

* 
**Traditional Model:** A slow, manual step-by-step process where humans write code line-by-line, leading to longer release cadences.


* 
**AI-Driven Shift:** Uneven compression of the software cycle. Coding tasks that typically took weeks are completed by autonomous AI loops in minutes.


* 
**The Human Role:** Humans shift away from typing boilerplate code to focusing heavily on high-level tasks like setting requirements, designing architecture, and final verification.



---

## 2. Vibe Coding, Structured AI-Assisted, & Agentic Engineering (Page 4)

The core difference across this spectrum is how strictly the generated code is checked and verified.

* 
**Vibe Coding:** * Uses casual, conversational prompts.


* Verified simply by clicking around to see if it "seems to work".


* Errors are handled by blindly copy-pasting terminal bugs back into the AI.


* Best for throwaway scripts and quick prototypes.




* 
**Structured AI-Assisted Coding:** * Uses detailed prompts filled with target constraints and specific code examples.


* Verified through manual testing alongside pre-written test suites.


* Humans actively find the root cause of errors, and the AI implements the directed fix.


* Best for isolated feature updates inside mature codebases.




* 
**Agentic Engineering:** * Uses formal system specifications, architectural blueprints, and strict rule configurations like `AGENTS.md`.


* Verified through fully automated validation pipelines and language-model judges.


* AI agents autonomously diagnose and repair their own errors within defined boundaries.


* Best for mission-critical production platforms and complex enterprise setups.





---

## 3. The Factory Model (Page 24)

* 
**The Shift:** The developer transitions from a manual builder to a system orchestrator. You are no longer building the product directly; you are building the assembly line system that constructs it.


* 
**The Metaphor:** Like a factory manager, you do not assemble components by hand. Instead, you design the assembly line layout, add safety sensors, and build verification checkpoints.


* 
**Execution:** Success relies on providing autonomous agents with clear success criteria rather than micro-managed step-by-step instructions, letting them iterate independently.



---

## 4. Harness Engineering (Page 26)

* **The Core Equation:** 
$$\text{Agent} = \text{Model} + \text{Harness}$$


* 
**The Blueprint:** The AI model is just a non-deterministic reasoning engine. The **Harness** is the surrounding software scaffolding, middleware, and operational constraints that make it run reliably.


* **Harness Infrastructure:**
* 
**Rule Files (`AGENTS.md`):** Defines the agent's absolute operational boundaries and style guidelines.


* 
**Isolated Sandboxes:** Secure command lines and file systems where agents safely execute code without threatening production setups.


* 
**Deterministic Hooks:** Guardrails that block bad behavior automatically (e.g., stopping a commit if the agent generates cleartext passwords).


* 
**Observability Telemetry:** Tracking logs that record the exact trajectory and reasoning path the agent took to reach an output.




* **The Proof:** Building a better harness drastically improves performance. On *Terminal Bench 2.0*, modifying only the harness middleware boosted an agent from outside the Top 30 straight into the Top 5—with zero changes to the underlying model.



---

## 5. The Economics of AI Development (Page 39)

* 
**Vibe Coding (Low CapEx, High OpEx):** Costs almost nothing upfront (Low Capital Expenditure) , but creates a compounding operational cost (High Operational Expenditure). Dumping messy code into prompts wastes expensive API tokens through repetitive trial-and-error loops , while producing unstructured "spaghetti" code that requires manual human cleanup later.


* 
**Agentic Engineering (High CapEx, Low OpEx):** Requires significant upfront time to engineer rule structures and validation tools (High Capital Expenditure). However, it keeps ongoing runtime costs low because structured constraints maximize first-pass success and eliminate wasteful token burn.


* 
**Intelligent Model Routing:** Maximizes token efficiency by using heavy, premium frontier models for high-level architecture planning while automatically offloading simple tasks (like writing unit tests or linting code) to faster, cheaper small models.