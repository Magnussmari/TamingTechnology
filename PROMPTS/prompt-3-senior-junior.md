# Prompt 3: Senior-Junior AI Workflow Pattern

> **Purpose:** Orchestrate multiple AI tools to work together efficiently by creating a "senior developer" (chat AI) guiding a "junior developer" (IDE agent) pattern.

> **Best AI combination:** Claude Chat or ChatGPT (Senior) + Claude Code or Cursor (Junior)

---

## 📚 About This Workflow

This workflow creates a collaboration pattern where:

- **🧠 AI Chat Platforms** (Claude, ChatGPT, Gemini) act as the **senior developer**
  - Excels at: Architectural thinking, strategic decisions, debugging complex problems

- **⚙️ IDE AI Agents** (Cursor, Copilot, Cline, Claude Code) act as the **junior developer**
  - Excels at: Code generation, in-context edits, file navigation, executing specific tasks

By creating structured communication between these tools, you simulate a realistic development team while leveraging the orchestration principles from Part 1.

---

## 🎯 Benefits of This Workflow

| Benefit | Description |
|---------|-------------|
| **🎯 Clear Role Separation** | Each AI does what it's best at - no overlap or confusion |
| **📊 Structured Communication** | Reports maintain context and clarity across tools |
| **🔄 Efficient Iteration** | Quick tactical work (IDE) + strategic guidance (chat) |
| **🧠 Better Decisions** | Complex problems get proper architectural thinking |
| **📈 Faster Learning** | See how senior developers think through problems |

---

## 🚀 How to Use This Workflow

**Step 0: Have Your Profile Ready** ⭐
- Keep your [USER-PROFILE.md](../USER-PROFILE.md) accessible
- When escalating to Senior AI, include relevant context from your profile:
  - Your learning style (how much explanation you need)
  - Your current comfort level with technologies
  - Your specific goals (helps AI tailor advice)

**Step 1: Initialize Both AI Contexts**
1. Open your preferred **chat AI** (Claude, ChatGPT) → Paste **Prompt 1 (Senior)** below
2. Open your **IDE AI agent** (Cursor, Cline, Claude Code) → Use **Prompt 2 (Report Template)** when needed

**Step 2: Work in Your IDE**
- Use your IDE AI agent for coding and implementation
- When you hit a complex issue, have the IDE agent generate a report using **Prompt 2**

**Step 3: Escalate to Senior AI**
- Copy the report from IDE agent
- Paste into your chat AI (senior developer context)
- Get strategic guidance

**Step 4: Return to Implementation**
- Take guidance from senior AI
- Return to IDE agent with clear instructions
- Execute and iterate

---

## 📋 The Prompts

### 🏗️ PROMPT 1: Senior Developer (AI Chat Platform)

Copy this to **Claude Chat** or **ChatGPT**:

```markdown
# ROLE

You are a senior full-stack developer and technical architect. A junior developer (an IDE AI agent) will send you reports about their work, and you'll provide guidance, make architectural decisions, debug complex issues, and review code.

You communicate clearly and practically, focusing on:
- Strategic decisions over tactical implementation
- Teaching principles, not just solutions
- Systems thinking and architecture
- Long-term maintainability

# YOUR RESPONSIBILITIES

1. **Review Reports**: Analyze reports from the junior developer about tasks completed, problems encountered, and questions
2. **Provide Guidance**: Give clear, actionable advice on complex problems
3. **Make Decisions**: Help with architectural choices, technology selection, and design patterns
4. **Debug Issues**: Help troubleshoot when simple solutions aren't working
5. **Review Code**: Assess code changes for quality, maintainability, and best practices

# HOW TO RESPOND

When you receive a report, provide:

## 📊 Analysis
Brief assessment of the situation

## 💡 Recommendations
Clear, prioritized suggestions

## ✅ Next Steps
Specific actions for the junior developer to take

## 📚 Context
Explain the "why" behind your recommendations

## ⚠️ Warnings
Potential pitfalls to avoid

# IMPORTANT

- You guide strategy, the IDE agent executes tactics
- Focus on architecture and systems thinking (#systemsthinking)
- Leverage AI augmentation opportunities (#aiaugmentation)
- Think full-stack when relevant (#fullstack)
- Be encouraging but maintain high standards

I'm ready to receive reports and provide guidance.
```

**When to use the Senior Developer AI:**
- 🔴 Complex bugs that resist simple fixes
- 🟡 Architectural decisions (which library? which pattern?)
- 🟢 Code review and quality assessment
- 🔵 Strategic planning (how to structure a feature?)
- 🟣 Learning moments (understanding why something works)

---

### 📊 PROMPT 2: Junior Developer Report Template (IDE AI Agent)

Give this template to your **IDE AI agent** when you need to escalate:

```markdown
Generate a report for the senior developer using this format:

# 🔷 JUNIOR DEVELOPER REPORT

## 📋 Task Summary
[What I was trying to accomplish]

## ✅ What I Completed
- [List of successful changes/implementations]
- [Files modified]
- [Features added]

## ❌ Problems Encountered
**Issue 1**: [Describe the problem]
- What I tried: [Solutions attempted]
- Current status: [Where things stand]
- Error messages: [If applicable]

**Issue 2**: [If applicable]
...

## ❓ Questions for Senior Developer
1. [Specific question about architecture/approach]
2. [Specific question about best practices]
3. [Specific question about debugging]

## 💭 My Current Understanding
[What I think is happening and why]

## 🎯 What I Need
[Specific guidance requested - e.g., "architectural direction," "debugging help," "code review"]

## 📎 Context
- Project: [Project name/type]
- Tech stack: [Key technologies]
- Related files: [Relevant file paths]
- Deadline/Priority: [If applicable]
```

**When to generate a report:**
- ⚠️ After 2-3 failed attempts to solve a problem
- 🔍 Before making major architectural changes
- 🐛 When encountering confusing error messages
- 🎯 When completing a significant feature (for review)
- 💭 When needing to validate approach before proceeding

---

## 💡 Real-World Example

### Scenario: Adding Shopping Cart Functionality

**Step 1: Junior AI (Cursor) attempts implementation**
```
You to Cursor: "Add shopping cart with add/remove/update quantity"
Cursor: [Implements with useState]
```

**Step 2: Testing reveals bugs with quantity updates**
```
You: Test the cart
Result: Quantities cause duplicate items
```

**Step 3: Junior AI tries 3 fixes, still buggy**
```
Cursor tries: useState updates, different array methods, useEffect
Result: Still not working correctly
```

**Step 4: Generate escalation report**
```
You to Cursor: "Generate a junior dev report about this issue"

Cursor creates:
---
# 🔷 JUNIOR DEVELOPER REPORT

## 📋 Task Summary
Implement shopping cart with add/remove/update quantity functionality

## ✅ What I Completed
- Basic add to cart works
- Remove from cart works
- Cart displays items

## ❌ Problems Encountered
**Issue 1**: Quantity updates create duplicate items
- What I tried:
  1. Direct useState mutation
  2. Array.map() for immutable updates
  3. useEffect to sync state
- Current status: Add works, quantity update broken
- Error messages: No errors, but duplicates appear

## ❓ Questions for Senior Developer
1. Is useState the right approach for complex cart state?
2. Should I be using a reducer pattern?
3. Is there a better data structure for cart items?

## 💭 My Current Understanding
I think I'm mutating state incorrectly, causing React to not detect changes properly.

## 🎯 What I Need
Architectural direction on state management approach

## 📎 Context
- Project: E-commerce SaaS
- Tech stack: React 18, TypeScript
- Related files: components/Cart.tsx, hooks/useCart.ts
---
```

**Step 5: Escalate to Senior AI (Claude Chat)**
```
You to Claude Chat: [Paste the report above]

Claude Analysis:
"You've correctly identified the root issue - useState with complex
objects requires careful immutability. For shopping carts, I recommend
useReducer pattern..."

Next Steps:
1. Refactor to useReducer
2. Define clear action types: ADD_ITEM, REMOVE_ITEM, UPDATE_QUANTITY
3. Use item.id as key to prevent duplicates
4. Here's the structure: [detailed example]

Context:
useReducer shines when state updates depend on previous state and have
multiple update patterns. Shopping carts are a textbook case...
```

**Step 6: Return to Junior AI with solution**
```
You to Cursor: "Refactor cart to useReducer following this pattern: [paste]"
Cursor: [Implements correctly]
Result: Works perfectly!
```

---

## 🎯 The Escalation Ladder

```
Level 1: Try yourself (5 min)
    ↓ Still stuck?
Level 2: Ask Junior AI / IDE Agent (2-3 attempts, 20 min)
    ↓ Still stuck?
Level 3: Generate Junior Dev Report
    ↓
Level 4: Send to Senior AI (Claude Chat)
    ↓
Level 5: Get guidance, return to Junior AI
    ↓ Still stuck? (rare)
Level 6: Ask Perplexity if it's a known issue/pattern
```

**Rule of Thumb:**
- Never spin wheels for >30 minutes
- Escalate after 2-3 failed attempts
- Always close the loop - report back results

---

## 💡 Tips for Success

1. **Keep Senior AI context active** - Bookmark the conversation, it accumulates knowledge about your project
2. **Be specific in reports** - "Cart is broken" vs "Quantity updates create duplicates"
3. **Include what you tried** - Shows thought process, gets better guidance
4. **Apply guidance fully** - Don't cherry-pick, implement the whole solution
5. **Report back results** - "That worked!" or "Still seeing X" maintains context

---

## 🔄 When to Use This Pattern

✅ **Perfect for:**
- Building new features
- Debugging complex issues
- Making architectural decisions
- Code review before commits
- Learning new patterns/technologies

❌ **Overkill for:**
- Simple syntax errors (use Junior AI only)
- Typos or formatting (use linter)
- Trivial changes (just do it)
- Well-understood patterns (you know the answer)

---

## 🔗 Related Resources

- [Prompt 1: Learning Roadmap](prompt-1-roadmap.md) - Create your learning plan
- [Prompt 2: Tech Stack Analysis](prompt-2-stack-analysis.md) - Understand your codebase
- [Complete Guide](../COMPLETE-GUIDE.md) - Full AI Orchestration system
- [AI Tool Matrix](../TOOLS/ai-tool-matrix.csv) - Choose the right AI

---

## 🎓 Team Adaptation

This pattern works for actual teams too:

- **Senior AI** → Tech Lead reviews across team
- **Junior AI(s)** → Individual developers use their IDE agents
- **Human Orchestrator** → Team lead or project manager
- **Weekly Reports** → Aggregate individual reports for strategic review

See [Team Patterns](../TEAM-PATTERNS/team-reports.md) for details.

---

**Ready?**

1. Copy Senior Prompt → Paste into Claude Chat or ChatGPT
2. Save/bookmark that conversation
3. Start coding with your IDE agent
4. Use Junior Report Template when stuck
5. Escalate and iterate!

**You now have a complete AI development team at your fingertips.**
