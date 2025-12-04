# Step 1 — Folder Structure

Project folder **task 9-10** ke andar `.claudecode` create karein, phir `skills/` ke andar 3 skill folders:
task 9-10/
└─ .claudecode/
└─ skills/
├─ summary-maker/
│ └─ SKILL.md
├─ translation-helper/
│ └─ SKILL.md
└─ code-linter/
└─ SKILL.md


---

# Step 2 — SKILL.md Content Template

Har skill ke liye ye template use karein:

```md
# Skill Name: <Skill Name>
**Description:** <Short description of the skill>

## Context / Purpose
<Explain why this skill is useful and when to use it>

## Inputs
- <List inputs>

## Outputs
- <List outputs>

## Usage Example
```python
# Example usage code

Notes:
<Any special notes, limitations, or tips>


---

# Step 3 — Example SKILL.md for Each Skill

## 1. summary-maker/SKILL.md

```md
# Skill Name: Summary Maker
**Description:** Generates concise summaries from long text, articles, or chapters.

## Context / Purpose
Useful for book writing or research. Converts long content into easy-to-read summaries.

## Inputs
- text: string — the content to summarize
- length: integer (optional) — desired summary length in sentences

## Outputs
- summary: string — concise summary of the input text

## Usage Example
```python
handle({"text": "Long chapter content here", "length": 5})

Notes:

Works best with coherent paragraphs

Can be reused for multiple chapters or articles

---

## 2. translation-helper/SKILL.md

```md
# Skill Name: Translation Helper
**Description:** Translates text between multiple languages, including Urdu, English, and French.

## Context / Purpose
Useful for multilingual books, localization, and understanding content in different languages.

## Inputs
- text: string — text to translate
- target_language: string — language code to translate into (e.g., 'ur', 'fr')

## Outputs
- translated_text: string — translated content

## Usage Example
```python
handle({"text": "Hello World", "target_language": "ur"})


---

## 3. code-linter/SKILL.md

```md
# Skill Name: Code Linter
**Description:** Analyzes and improves code snippets for syntax, readability, and best practices.

## Context / Purpose
Helps developers ensure clean, readable, and error-free code for book or project scripts.

## Inputs
- code: string — code snippet to analyze
- language: string — programming language (e.g., 'python', 'javascript')

## Outputs
- suggestions: string — improvements and fixes
- issues: list — list of detected problems

## Usage Example
```python
handle({"code": "print('Hello'", "language": "python"})

Notes:

Supports multiple languages

Does not execute code, only analyzes

---

# Step 4 — Create Agents Directory

Project folder → `.claudecode` → new folder:

.claudecode/
agents/


---

# Step 5 — Create 3 Agent Files

.claudecode/
agents/
writing-sub-agent.md
editing-sub-agent.md
orchestrator-agent.md


---

# Step 6 — Agent Descriptions

## 1. writing-sub-agent.md

```md
# Agent Name: Writing Sub-Agent

## Task Description
This agent generates book content including chapters, explanations, dialogues, and examples.  
It expands outlines into full sections and maintains tone, structure, flow, and clarity.  
It ensures creativity, consistency, and adherence to the user’s writing style.

2. editing-sub-agent.md
# Agent Name: Editing Sub-Agent

## Task Description
This agent edits the written content for grammar, clarity, structure, and readability.  
It removes repetition, fixes sentence structure, and polishes the writing to professional standards.

3. orchestrator-agent.md
# Agent Name: Orchestrator Agent

## Task Description
This agent coordinates all sub-agents.  
It receives the main user request, selects the correct sub-agent, sends the task, gathers results, and returns the final output.  
It manages workflow between writing, editing, summarizing, and other skills.

Final Folder Overview
.claudecode/
   skills/
      summary-maker/
      translation-helper/
      code-linter/
   agents/
      writing-sub-agent.md
      editing-sub-agent.md
      orchestrator-agent.md

Reflection Summary

I created a full ClaudeCode skills and agents system.
Three skills (Summary Maker, Translation Helper, Code Linter) and three agents (Writing, Editing, Orchestrator) were added with proper documentation.
This improved understanding of modular AI tools, multi-agent workflows, and reusable skill structures for book automation.

