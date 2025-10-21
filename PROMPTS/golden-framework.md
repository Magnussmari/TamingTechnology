# The GOLDEN Framework: Evidence-Based Prompt Engineering

**Status:** Industry Standard (2025)
**Source:** Consolidated from Anthropic, OpenAI, and academic prompt engineering research

## What Is GOLDEN?

The GOLDEN framework is the consensus approach for comprehensive AI prompts. It addresses the most common prompt failures while remaining flexible for diverse applications.

**GOLDEN = Goal + Output + Limits + Data + Evaluation + Next**

This framework evolved from research showing that structured prompts significantly outperform vague requests across all major AI models.

---

## The Six Components

### 🎯 G - Goal

**Define the objective and success criteria clearly.**

**Include:**
- What you want to accomplish
- Why you're doing this (context)
- What success looks like
- Who the output is for

**Example - Vague:**
```
Write about AI
```

**Example - GOLDEN:**
```
GOAL: Create an educational blog post explaining AI orchestration to
software developers who are familiar with single-AI tools (like ChatGPT)
but haven't explored multi-tool workflows. Success means readers understand
when to use which AI and can implement one orchestration pattern immediately.
```

### 📝 O - Output

**Specify format, length, tone, and structure.**

**Include:**
- Format (essay, code, list, table, JSON, etc.)
- Length (word count, number of examples)
- Tone (professional, casual, technical, beginner-friendly)
- Structure (sections, headers, specific elements)

**Example - Vague:**
```
Make it professional
```

**Example - GOLDEN:**
```
OUTPUT:
- Format: Blog post with markdown formatting
- Length: 800-1000 words
- Tone: Professional but accessible, avoid jargon where possible
- Structure:
  1. Problem statement (current pain points)
  2. Solution overview (orchestration concept)
  3. Practical example (Draft + Refinement pattern)
  4. Call to action (try one pattern this week)
- Include 1-2 code examples or workflow diagrams
```

### 🚧 L - Limits

**Define scope, constraints, rules, and boundaries.**

**Include:**
- What to avoid
- Scope boundaries (what's in/out)
- Constraints (time, resources, complexity)
- Rules and requirements

**Example - Vague:**
```
Don't make it too complicated
```

**Example - GOLDEN:**
```
LIMITS:
- Scope: Focus ONLY on Development Pathway (exclude Research tools)
- Avoid: Academic jargon, theoretical frameworks, tools not available in 2025
- Constraints: Readers have max 15 minutes to understand and try
- Rules:
  * Use only free-tier or commonly available tools
  * All examples must be actionable (not hypothetical)
  * No promotional content for specific companies
  * Maintain security awareness (mention validation needs)
```

### 📊 D - Data

**Provide context, examples, sources, and background.**

**Include:**
- Relevant background information
- Examples of good outputs (few-shot learning)
- Source materials or references
- User profile or audience details

**Example - Vague:**
```
Here's some info...
```

**Example - GOLDEN:**
```
DATA:
Context: This is for TamingTechnology repository (v2.1), targeting
developers transitioning from single-AI to orchestrated workflows.

Target audience profile:
- Experience: 2-5 years coding
- Current AI usage: Primarily ChatGPT for everything
- Pain point: Inconsistent results, not sure which AI for what
- Time available: 10-20 hours/week for learning

Example of good output style (from existing docs):
"Stop using one AI for everything. Learn to orchestrate specialized AI
tools like a conductor leading an orchestra—each instrument playing its
perfect part."

Key tools to reference:
- Claude (coding, 72.7% SWE-bench)
- ChatGPT (learning, memory)
- Cursor (IDE integration)

Research findings to incorporate:
- 45% of AI code has vulnerabilities (mention security)
- Anti-dependency strategies prevent skill decay
```

### ✅ E - Evaluation

**Specify how to judge quality (rubric or acceptance criteria).**

**Include:**
- Quality criteria
- Must-have elements
- Success metrics
- Review checklist

**Example - Vague:**
```
Make it good
```

**Example - GOLDEN:**
```
EVALUATION:
The output will be considered successful if it:

✅ Clarity: A developer unfamiliar with orchestration can understand
   the core concept in under 3 minutes

✅ Actionability: Contains at least one specific pattern they can
   implement today with step-by-step instructions

✅ Evidence-based: References real benchmarks (Claude's SWE-bench score,
   productivity studies) not marketing claims

✅ Balanced: Acknowledges limitations and risks (security, dependency)
   not just benefits

✅ Practical: All examples use tools with free tiers or common availability

❌ Fails if: Contains jargon without explanation, promotes specific vendors,
   lacks concrete next steps, or exceeds 1200 words
```

### ➡️ N - Next

**Define follow-up actions or next steps.**

**Include:**
- What happens after this output
- Follow-up questions or refinements
- Next steps in the workflow
- Iteration expectations

**Example - Vague:**
```
We'll iterate
```

**Example - GOLDEN:**
```
NEXT:
1. After you generate the blog post, I'll review it against the
   evaluation criteria

2. If it meets criteria, you'll create:
   - A companion "Quick Start" checklist (1 page)
   - 3 tweet-sized summaries for social sharing

3. If it needs refinement, I'll provide specific feedback on which
   evaluation criteria weren't met

4. Final version will be added to TamingTechnology/WORKFLOWS/

5. Expected iterations: 1-2 rounds maximum
```

---

## Complete GOLDEN Example

### Bad Prompt (Before):
```
Write a tutorial about using AI for coding
```

### GOLDEN Prompt (After):
```
GOAL:
Create a tutorial teaching software developers how to use AI coding
assistants effectively while maintaining their own skills. Target audience:
developers with 1-3 years experience who are curious about AI but worried
about becoming dependent. Success = readers can start using AI productively
TODAY without compromising skill development.

OUTPUT:
- Format: Step-by-step tutorial with markdown formatting
- Length: 1,200-1,500 words
- Tone: Encouraging but realistic, mentor-like
- Structure:
  1. Hook: Common fears about AI dependency (200 words)
  2. Anti-Dependency Strategies (400 words)
  3. Your First Week with AI (500 words)
  4. Assessment Checklist (200 words)
- Include practical code examples (Python or JavaScript)
- Add "Try This Today" sections after each main point

LIMITS:
- Scope: Focus on first month of AI usage only
- Avoid: Advanced orchestration, multiple tools (keep it simple)
- Constraints: Readers should complete tutorial in 30 minutes
- Rules:
  * Every strategy must be evidence-based (cite research)
  * All tools mentioned must have free tiers
  * No vendor promotion
  * Include security warnings for code validation

DATA:
Context: Part of TamingTechnology's Anti-Dependency module

Target reader profile:
- 1-3 years coding experience
- Never used AI coding assistants OR tried briefly and stopped
- Fears: Skill atrophy, becoming "dependent," producing bad code
- Motivation: Productivity, learning faster, staying competitive

Research to incorporate:
- Microsoft/CMU 2025 study: AI reliance → reduced critical thinking
- Attempt-first protocol: 15-30 min before consulting AI
- Phase-gated progression: Minimal AI months 1-3
- 45% of AI code has security vulnerabilities

Example of tone we want (from existing docs):
"This is not a shortcut. This is a method for sustainable, effective
work with AI tools while maintaining and building your own skills."

EVALUATION:
Output succeeds if:

✅ Addresses fear directly: Acknowledges dependency concerns upfront
✅ Evidence-based: Cites at least 2 research studies
✅ Immediately actionable: Contains Week 1 day-by-day plan
✅ Balanced: Equal coverage of benefits AND risks
✅ Security-aware: Mentions code validation requirements
✅ Assessment: Includes self-check to detect dependency
✅ Practical: All strategies testable within first month

Fails if:
❌ Dismisses dependency concerns as unfounded
❌ Lacks specific daily actions
❌ Promotes AI without acknowledging risks
❌ Exceeds 1,700 words
❌ Requires paid tools

NEXT:
1. Generate tutorial following this framework
2. I'll review against evaluation criteria
3. If approved, create companion materials:
   - Week 1 Daily Checklist (PDF-ready)
   - Self-Assessment Quiz (10 questions)
   - Quick Reference Card (1 page)
4. Integrate into ANTI-DEPENDENCY/ directory
5. Cross-link from main README
```

---

## Educational-Specific Patterns

When using GOLDEN for learning and teaching:

### Pattern: Socratic Questioning

**Instead of asking AI to solve directly:**
```
GOAL: Help me understand recursion by guiding me to discover the
concept myself through questions

OUTPUT: Series of 5-7 leading questions that build understanding

LIMITS: Don't give me the answer. Ask questions that make ME think.

DATA: I understand loops and functions. I'm working in Python.

EVALUATION: Success if I can explain recursion in my own words after
your questions

NEXT: After I answer your questions, verify my understanding and fill
any gaps
```

### Pattern: Formative Assessment

**Check understanding before continuing:**
```
GOAL: Verify I understand AI orchestration before moving to advanced
patterns

OUTPUT: 3 scenario-based questions that test understanding

LIMITS: No yes/no questions. Require explaining reasoning.

DATA: I've read the basic orchestration patterns (Draft+Refinement,
Volume+Depth)

EVALUATION: If I get 2/3 correct with good reasoning, I'm ready to
proceed

NEXT: Based on my answers, either continue to advanced patterns or
review fundamentals
```

### Pattern: Adaptive Feedback

**Get feedback calibrated to skill level:**
```
GOAL: Get feedback on my code that matches my skill level

OUTPUT: Code review in three sections:
1. Critical issues (must fix)
2. Learning opportunities (should understand)
3. Advanced optimizations (nice to have)

LIMITS: Don't just tell me what to fix. Explain WHY and HOW to think
about it.

DATA: I'm 3 months into learning JavaScript. Here's my code: [code]

EVALUATION: Success if I understand the reasoning behind each suggestion

NEXT: I'll fix critical issues myself before asking for solution
```

---

## Common Prompt Anti-Patterns (Avoid These!)

### ❌ Anti-Pattern 1: Vague Goals
```
"Help me with my code"
"Write something about AI"
"Make this better"
```

**Fix:** Specify exact objective, success criteria, who it's for

### ❌ Anti-Pattern 2: Missing Constraints
```
"Write a comprehensive guide to Python"
```

**Fix:** Define scope, length, depth, audience level

### ❌ Anti-Pattern 3: No Context
```
"Debug this function: [code]"
```

**Fix:** Provide background, what you've tried, expected vs actual behavior

### ❌ Anti-Pattern 4: Overloading
```
"Write code AND debug AND explain AND create tests AND document"
```

**Fix:** Break into sequential prompts. Chain outputs.

### ❌ Anti-Pattern 5: Assuming Knowledge
```
"Fix the bug" (AI doesn't know what you consider a bug)
"Make it professional" (AI doesn't know your standards)
```

**Fix:** Be explicit about expectations and evaluation criteria

---

## Research-Backed Techniques

### Chain-of-Thought Prompting
**Research:** Wei et al. 2022 - significant improvements on reasoning tasks

**Implementation:**
```
Before providing your answer, think step-by-step in <thinking> tags.
Show your reasoning process.
```

### Few-Shot Learning
**Research:** 2-5 examples show major gains, plateau after 5

**Implementation:**
```
DATA: Here are 3 examples of good outputs:

Example 1: [...]
Example 2: [...]
Example 3: [...]

Now create output following this pattern for: [your task]
```

**Note:** Example ordering matters! Place best examples last.

### Structured Outputs
**Research:** Claude trained with XML, GPT-4o achieves 100% JSON schema compliance

**Implementation:**
```
OUTPUT: Respond using this XML structure:

<response>
  <summary>Brief overview</summary>
  <details>
    <point>First point</point>
    <point>Second point</point>
  </details>
  <next_steps>
    <step>Action 1</step>
    <step>Action 2</step>
  </next_steps>
</response>
```

---

## GOLDEN Framework Template

Copy and customize this template:

```
GOAL:
[What you want to accomplish]
[Why you're doing this]
[What success looks like]
[Who this is for]

OUTPUT:
- Format: [essay/code/list/table/etc.]
- Length: [word count/number of items]
- Tone: [professional/casual/technical/etc.]
- Structure: [sections, specific elements]

LIMITS:
- Scope: [what's included/excluded]
- Avoid: [things to stay away from]
- Constraints: [time/resource limits]
- Rules: [specific requirements]

DATA:
[Background context]
[Target audience details]
[Examples of good outputs]
[Source materials]
[Relevant information]

EVALUATION:
Output succeeds if:
✅ [Criterion 1]
✅ [Criterion 2]
✅ [Criterion 3]

Fails if:
❌ [Failure condition 1]
❌ [Failure condition 2]

NEXT:
1. [What happens after output]
2. [Follow-up actions]
3. [Iteration expectations]
```

---

## When to Use GOLDEN

**Use GOLDEN for:**
- Complex tasks requiring high quality
- Educational content where understanding matters
- Production code or important documents
- When you've had poor results from simple prompts
- Team workflows requiring consistency

**Skip GOLDEN for:**
- Quick questions or simple requests
- Exploratory brainstorming
- When speed matters more than precision
- Simple code completions in IDE

**Rule of thumb:** If the output matters and you'll iterate, use GOLDEN. If you just need a quick answer, keep it simple.

---

## Practice Exercise

**Transform this vague prompt using GOLDEN:**

```
Make a function that processes user data
```

**Your GOLDEN version should include:**
1. What kind of processing? For what purpose?
2. What format should the function return?
3. What constraints (performance, security)?
4. What's the context (language, framework, use case)?
5. How will you evaluate if it's correct?
6. What testing or next steps?

---

## Additional Resources

- See [prompt-1-roadmap.md](prompt-1-roadmap.md) for GOLDEN in practice
- See [prompt-3-senior-junior.md](prompt-3-senior-junior.md) for orchestration prompts
- See [ANTI-DEPENDENCY/complete-guide.md](../ANTI-DEPENDENCY/complete-guide.md) for learning-focused prompting

---

**Remember:** The GOLDEN framework is a tool, not a rule. Use it when precision matters, adapt it to your needs, and skip it when simplicity suffices. The goal is better outputs, not longer prompts for their own sake.
