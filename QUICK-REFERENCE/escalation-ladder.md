# The Escalation Ladder: When You're Stuck

**Print this out. Keep it visible. Follow it religiously.**

---

## 🎯 The Golden Rule

**Never spin your wheels for more than 30 minutes on a single problem.**

If you're stuck, you're not "bothering" the AI—you're **using it correctly**. Escalate!

---

## 🪜 The 6-Level Escalation System

```
┌─────────────────────────────────────────────────────────┐
│ Level 1: Try Yourself                                   │
│ Time: 5 minutes                                          │
│ Tools: Your brain, Google, docs                          │
│                                                           │
│ ✅ Fixed? → Move on!                                     │
│ ❌ Still stuck? → Level 2                                │
└─────────────────────────────────────────────────────────┘
         ↓
┌─────────────────────────────────────────────────────────┐
│ Level 2: IDE AI (Cursor/Copilot)                        │
│ Time: 20 minutes (2-3 attempts)                          │
│ Tools: Cursor, GitHub Copilot                            │
│                                                           │
│ Try:                                                      │
│ - "Fix this error: [paste]"                              │
│ - "Why isn't this working: [code]"                       │
│ - "Refactor this: [code]"                                │
│                                                           │
│ ✅ Fixed? → Move on!                                     │
│ ❌ Still stuck after 3 tries? → Level 3                  │
└─────────────────────────────────────────────────────────┘
         ↓
┌─────────────────────────────────────────────────────────┐
│ Level 3: Generate Junior Dev Report                     │
│ Time: 5 minutes                                          │
│ Tools: Report template from Prompt 3                     │
│                                                           │
│ Ask your IDE AI:                                         │
│ "Generate a junior developer report about this issue"    │
│                                                           │
│ Or use the template manually:                            │
│ - Task: [what you tried]                                 │
│ - Completed: [what worked]                               │
│ - Problems: [specific blockers]                          │
│ - Tried: [3 solutions attempted]                         │
│ - Questions: [specific asks]                             │
│ - Need: [type of help]                                   │
│                                                           │
│ → Level 4                                                │
└─────────────────────────────────────────────────────────┘
         ↓
┌─────────────────────────────────────────────────────────┐
│ Level 4: Senior AI (Claude Chat/ChatGPT)                │
│ Time: 10-15 minutes                                      │
│ Tools: Claude Chat, ChatGPT                              │
│                                                           │
│ Actions:                                                 │
│ 1. Copy the Junior Dev Report from Level 3               │
│ 2. Paste into your Senior AI conversation                │
│ 3. Wait for strategic guidance                           │
│ 4. Read and understand the recommendations               │
│                                                           │
│ ✅ Got guidance? → Level 5                               │
│ ❌ Guidance unclear? → Ask follow-up questions           │
└─────────────────────────────────────────────────────────┘
         ↓
┌─────────────────────────────────────────────────────────┐
│ Level 5: Implement Solution                             │
│ Time: 20-30 minutes                                      │
│ Tools: Return to Cursor/Claude Code                      │
│                                                           │
│ Actions:                                                 │
│ 1. Return to your IDE AI                                 │
│ 2. Provide clear instructions from Senior AI             │
│    "Implement this solution: [paste guidance]"           │
│ 3. Execute the changes                                   │
│ 4. Test thoroughly                                       │
│                                                           │
│ ✅ Fixed? → Report back to Senior AI ("That worked!")   │
│ ❌ New issues? → Generate new report, back to Level 4    │
│ ❌ Same issue? → Level 6                                 │
└─────────────────────────────────────────────────────────┘
         ↓
┌─────────────────────────────────────────────────────────┐
│ Level 6: Research Known Issues                          │
│ Time: 10 minutes                                         │
│ Tools: Perplexity, Gemini                                │
│                                                           │
│ Ask:                                                     │
│ - "Is [error message] a known issue in [technology]?"   │
│ - "[Technology] [version] breaking changes"             │
│ - "Common problems with [specific pattern/library]"     │
│                                                           │
│ ✅ Found solution? → Back to Level 5 with new info      │
│ ❌ Nothing found? → Back to Level 4 with new context    │
└─────────────────────────────────────────────────────────┘
```

---

## 🎯 When to Skip Levels

### Skip to Level 3 (Senior AI) if:
- ❌ Error is conceptual (not just syntax)
- ❌ You need architectural guidance
- ❌ Multiple approaches possible, need decision
- ❌ Security or performance concern

### Skip to Level 4 (Research) if:
- ❌ Error mentions specific version/library
- ❌ Seems like a framework bug
- ❌ Recent update broke something
- ❌ Error message is cryptic/framework-specific

### Skip Level 1 if:
- ❌ Working on architecture (start at Level 3 or 4)
- ❌ Completely new problem domain
- ❌ Already spent >30 min on similar issue today

---

## 📊 Example Escalation

### Scenario: "useState updates creating duplicate items in cart"

**Level 1: Try Yourself (5 min)**
```
Me: *Reads code, checks for typos*
Result: No obvious errors found
→ Level 2
```

**Level 2: Ask Cursor (20 min)**
```
Try 1: "Fix this cart bug: [paste code]"
Result: Suggests useState mutation fix
→ Doesn't work

Try 2: "Why are duplicates appearing?"
Result: Suggests Array.map() for immutable update
→ Still broken

Try 3: "Refactor cart state management"
Result: Adds useEffect
→ Still broken after 3 tries
→ Level 3
```

**Level 3: Generate Report**
```
Me to Cursor: "Generate junior dev report about this cart issue"

Report created:
---
Task: Shopping cart with update quantity
Completed: Add/remove works
Problem: Quantity update creates duplicates
Tried:
1. Direct mutation fix
2. Immutable Array.map()
3. useEffect sync
Questions: Is useState right for this? Should I use reducer?
Need: Architectural guidance
---
→ Level 4
```

**Level 4: Senior AI**
```
Me to Claude Chat: [Paste report]

Claude response:
"You've correctly identified the issue. For complex state like
shopping carts with multiple update patterns, useReducer is better.
Here's why... [explanation]

Next steps:
1. Refactor to useReducer
2. Define actions: ADD_ITEM, UPDATE_QUANTITY, REMOVE_ITEM
3. Use item.id as key
Here's the structure: [code example]"
→ Level 5
```

**Level 5: Implement**
```
Me to Cursor: "Refactor cart to useReducer with this pattern: [paste]"
Cursor: [Implements]
Me: *Tests*
Result: ✅ WORKS!

Me to Claude Chat: "That worked perfectly! Cart now handles all
updates without duplicates. Thanks!"
→ Done!
```

**Total time:** ~60 min vs. 3+ hours of wandering

---

## 🚨 Red Flags: You're Escalating Wrong

### 🔴 Escalating TOO EARLY
**Symptoms:**
- Asking Senior AI for simple syntax errors
- Using Level 4 for every tiny question
- Not trying anything yourself first

**Fix:** Force yourself through Levels 1-2 first. Build problem-solving muscles.

### 🔴 Escalating TOO LATE
**Symptoms:**
- Stuck >1 hour on same problem
- Tried 10+ "solutions" randomly
- Feeling frustrated/defeated
- Just kept asking same AI repeatedly

**Fix:** Set 30-min timer. When it goes off, ESCALATE.

### 🔴 Not Closing the Loop
**Symptoms:**
- Get solution, never report back
- Jump to new problem immediately
- AIs lose context over time

**Fix:** Always report results: "That worked!" or "Still seeing X"

---

## 💡 Pro Tips

### 1. The 2-3 Rule
Try 2-3 different approaches at each level before escalating. Not 1, not 10.

### 2. The 30-Minute Rule
If you've spent 30 minutes at ANY level without progress, escalate immediately.

### 3. The Documentation Rule
Keep brief notes at each level:
```
Problem: Cart duplicates
Level 1: ❌ (5 min)
Level 2: ❌ (20 min) - tried mutations, maps, effects
Level 3: ✅ Report generated
Level 4: ✅ Got useReducer guidance
Level 5: ✅ Fixed!
Learning: Complex state → useReducer, not useState
```

### 4. The Pattern Recognition Rule
If you escalate 3+ times for same TYPE of problem, that's a knowledge gap.
→ Add to your learning roadmap.

### 5. The Celebration Rule
When you fix something, CELEBRATE! Track your wins.

---

## 📈 Escalation Metrics

Track for one week to build awareness:

| Day | Problems | L1 Success | L2 Success | L3-4 Used | L5 Success |
|-----|----------|------------|------------|-----------|------------|
| Mon | 3 | 1 | 1 | 1 | 1 |
| Tue | 2 | 0 | 1 | 1 | 1 |
| Wed | 4 | 2 | 1 | 1 | 1 |
| ... | | | | | |

**Good patterns:**
- L1 Success increasing (you're learning!)
- L3-4 used when actually stuck (not avoiding)
- L5 Success = 100% (guidance works)

**Bad patterns:**
- Never using L3-4 (too proud, will burn out)
- Always starting at L4 (not building skills)
- L5 Success <80% (not implementing correctly)

---

## 🎯 Your Escalation Commitment

**I commit to:**
- ✅ Following the ladder systematically
- ✅ Never spending >30 min stuck without escalating
- ✅ Generating proper Junior Dev Reports at Level 3
- ✅ Reporting back results to Senior AI
- ✅ Tracking patterns to improve over time

**I will NOT:**
- ❌ Skip levels randomly
- ❌ Escalate too early (rob myself of learning)
- ❌ Escalate too late (waste time stuck)
- ❌ Jump between AIs chaotically

---

## 🔗 Related Resources

- [Prompt 3: Senior-Junior Pattern](../PROMPTS/prompt-3-senior-junior.md) - Full workflow
- [AI Selector](ai-selector.md) - Which AI for what
- [Week 1 Launch Plan](../WORKFLOWS/week-1-launch-plan.md) - Practice orchestration
- [Complete Guide](../COMPLETE-GUIDE.md) - Deep dive

---

**Print this. Follow this. Trust the system.**

**The escalation ladder is your safety net. Use it.** 🪜
