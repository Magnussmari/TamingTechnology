# Week 1 Launch Plan: Your AI Orchestration Journey Starts Here

**Time Investment:** 10-15 hours total
**Goal:** Complete setup and create your personalized learning roadmap

---

## Day 1: Foundation Setup (2.5 hours)

### ⭐ FIRST THING: Create Your Profile (30 min)
**DO THIS BEFORE ANYTHING ELSE - It's your foundation!**

- [ ] Open [USER-PROFILE.md](../USER-PROFILE.md)
- [ ] Review the [example profile](../USER-PROFILE-EXAMPLE.md) to see what a completed one looks like
- [ ] Fill out YOUR profile completely and honestly:
  - Current experience level
  - Goals & outcomes
  - Tech stack preferences
  - Time availability
  - Learning style
  - Known blockers
- [ ] Save as: `MY-PROFILE.md` in your `AI_Learning_Journey/` folder
- [ ] **This is your source of truth** - all prompts will reference this!

### Morning: Read & Understand (1 hour)
- [ ] Read [AI Orchestration Philosophy](../COMPLETE-GUIDE.md#-part-1-ai-orchestration-philosophy)
- [ ] Study the [AI Tool Matrix](../TOOLS/ai-tool-matrix.csv)
- [ ] Understand the [Three Laws of AI Orchestration](../COMPLETE-GUIDE.md#the-three-laws-of-ai-orchestration)

### Afternoon: Choose Your Tools (1 hour)
- [ ] **Research AI:** Sign up for [Perplexity](https://perplexity.ai) (free tier)
- [ ] **Strategy AI:** Choose [Claude Chat](https://claude.ai) or [ChatGPT](https://chat.openai.com)
- [ ] **Implementation AI:** Download [Cursor](https://cursor.sh) (recommended) or set up Claude Code
- [ ] Test each tool with a simple question

### Evening: Organize Your Workspace (30 min)
- [ ] Create folder: `AI_Learning_Journey/`
- [ ] Subfolders: `Roadmaps/`, `Context_Docs/`, `Learning_Log/`
- [ ] Decide on conversation naming convention
  - Example: `"[YourName] - [Purpose] - [AI Type]"`
  - `"Sam - Learning Roadmap - Perplexity"`
  - `"Sam - Senior Dev Mentor - Claude Chat"`

---

## Day 2: Create Your Roadmap (1-2 hours)

### Task: Use Prompt 1 (WITH Your Profile!)

- [ ] **Open YOUR profile** (`MY-PROFILE.md`) - you'll reference it!
- [ ] Open [Prompt 1: Learning Roadmap Generator](../PROMPTS/prompt-1-roadmap.md)
- [ ] **Use your profile to fill in** all `[INSERT: ...]` sections:
  - Copy from "Current Experience Level" section
  - Copy from "Goals & Outcomes" section
  - Copy from "Tech Stack Preferences" section
  - Copy from "Time Availability" section
  - Your specific goals (2-3)
- [ ] Copy the completed prompt
- [ ] Paste into **Perplexity** or **Claude Chat**
- [ ] Review the generated roadmap
- [ ] Save as: `Roadmaps/[YourName]_Learning_Roadmap_[Date].md`

### Validate Your Roadmap (optional but recommended)
- [ ] If you used Perplexity, paste the roadmap into Claude Chat
- [ ] Ask: "Does this roadmap make sense given my background? Any adjustments?"
- [ ] Update based on feedback

---

## Day 3: Understand Your Stack (1-2 hours)

### If You Have an Existing Project:

- [ ] Open [Prompt 2: Tech Stack Analysis](../PROMPTS/prompt-2-stack-analysis.md)
- [ ] Fill in project details
- [ ] Use **Claude Code** or **Claude Chat** to analyze
- [ ] Save output as: `Context_Docs/Tech_Stack_Analysis_[ProjectName].md`
- [ ] Identify top 3 technologies to focus on first

### If Starting Fresh:

- [ ] Use Perplexity to research: "Best tech stack for [your goal] in 2025"
- [ ] Ask Claude Chat: "Which stack should I learn for [your goal]? Consider: ease of learning, AI tool support, job market"
- [ ] Document decision in `Context_Docs/Tech_Stack_Decision.md`

---

## Day 4: Set Up Senior AI Context (30 minutes)

### Initialize Your "Senior Developer"

- [ ] Open **Claude Chat** or **ChatGPT**
- [ ] Copy [Prompt 3: Senior Developer](../PROMPTS/prompt-3-senior-junior.md#-prompt-1-senior-developer-ai-chat-platform)
- [ ] Paste to initialize the AI
- [ ] Name conversation: `"[YourName] - Senior Dev Mentor"`
- [ ] Bookmark/save this conversation link
- [ ] Test with simple question: "I'm learning [tech]. What should I focus on first?"

### Create Reference Doc

- [ ] Create `Context_Docs/Senior_AI_Context.md`:
```markdown
# My Senior AI Context

**AI Used:** Claude Chat / ChatGPT
**Conversation Link:** [paste link]
**Initialized:** [date]

## Project Context
- Learning: [technologies]
- Goals: [your goals]
- Timeline: [your timeline]

## When to Escalate
- Complex bugs (>30 min stuck)
- Architectural decisions
- Code review before commits
- Strategic planning
```

---

## Day 5-7: Start Building (2-4 hours per day)

### Follow Your Roadmap

- [ ] Open your roadmap from Day 2
- [ ] Start Week 1 tasks from the roadmap
- [ ] Use **Cursor** or **Claude Code** for implementation

### Practice Orchestration

**For simple tasks:**
- [ ] Use Cursor/Claude Code directly
- [ ] Complete at least 3 small tasks

**When you get stuck:**
- [ ] Try solving yourself (5 min)
- [ ] Ask your IDE AI for help (2-3 attempts)
- [ ] If still stuck after 30 min:
  - [ ] Generate Junior Dev Report (use template from [Prompt 3](../PROMPTS/prompt-3-senior-junior.md#-prompt-2-junior-developer-report-template-ide-ai-agent))
  - [ ] Send to Senior AI
  - [ ] Apply guidance
  - [ ] Report back results

### Keep a Learning Log

Create `Learning_Log/Week1.md`:
```markdown
# Week 1 Learning Log

## Day 5
**What I built:** [task]
**AI tools used:** [which AIs]
**What worked:** [successes]
**What I learned:** [insights]
**Stuck on:** [blockers]

## Day 6
...

## Day 7
...

## Week 1 Reflections
**Wins:**
**Challenges:**
**Next week focus:**
```

---

## Week 1 Success Criteria

By the end of Week 1, you should have:

### ✅ Setup Complete
- [ ] Have 3 AI tools set up and tested
- [ ] Organized workspace folder structure
- [ ] Senior AI context initialized

### ✅ Roadmap Created
- [ ] Personalized 8-week learning roadmap
- [ ] Understand your tech stack (or chosen stack)
- [ ] Top 3 learning priorities identified

### ✅ First Projects Started
- [ ] Completed at least 3 small tasks using AI
- [ ] Used at least 3 different AIs appropriately
- [ ] Generated at least 1 Junior Dev Report

### ✅ Orchestration Basics
- [ ] Successfully transferred context between AIs
- [ ] Escalated when stuck (didn't spin wheels >30 min)
- [ ] Kept learning log up to date

### ✅ Confidence Building
- [ ] Feel less overwhelmed by AI tool choices
- [ ] Have clear next steps for Week 2
- [ ] Starting to see how orchestration saves time

---

## 🚨 Troubleshooting

### "I'm overwhelmed by all the AIs"
→ Start with just 2: Claude Chat + Cursor. Add others as needed.

### "My roadmap feels too ambitious"
→ Re-run Prompt 1 with more realistic time constraints or narrower goals.

### "I don't have a project to analyze"
→ Clone a simple open-source project in your target tech and analyze that.

### "I'm stuck but don't know what to ask"
→ Use the Junior Dev Report template - it structures your thoughts.

### "I'm not making progress"
→ Check: Are you following your roadmap sequentially? Are you escalating when stuck?

---

## 📊 Week 1 Self-Assessment

Rate yourself 1-5 (1=struggling, 5=confident):

| Area | Rating | Notes |
|------|--------|-------|
| Tool selection | /5 | Do I know which AI for what? |
| Context transfer | /5 | Can I hand off between AIs? |
| Escalation timing | /5 | Do I escalate at the right time? |
| Learning progress | /5 | Am I building skills? |
| Confidence | /5 | Do I feel capable? |

**If any rating < 3:** Review that section in the [Complete Guide](../COMPLETE-GUIDE.md)

---

## 🎯 Prepare for Week 2

Before starting Week 2:
- [ ] Review your learning log
- [ ] Adjust Week 2 roadmap goals if needed
- [ ] Set up any new tools you'll need
- [ ] Schedule your learning time
- [ ] Celebrate what you built! 🎉

---

## 💡 Pro Tips

1. **Timebox tasks** - Use 25-min Pomodoros to avoid rabbit holes
2. **Save everything** - Context is gold when you return tomorrow
3. **Name conversations clearly** - "New chat" becomes "WTF is this?" in 2 days
4. **Report back to AIs** - "That worked!" or "Still broken" maintains context
5. **Don't aim for perfect** - "Good enough to learn" beats "stuck seeking perfection"

---

## 🔗 Quick Links

- [Complete Guide](../COMPLETE-GUIDE.md)
- [Prompt 1: Learning Roadmap](../PROMPTS/prompt-1-roadmap.md)
- [Prompt 2: Tech Stack Analysis](../PROMPTS/prompt-2-stack-analysis.md)
- [Prompt 3: Senior-Junior Pattern](../PROMPTS/prompt-3-senior-junior.md)
- [AI Tool Matrix](../TOOLS/ai-tool-matrix.csv)

---

**Ready? Let's go! You've got this! 🚀**

Start with Day 1 and work through systematically. The orchestration skills you build this week will compound every week after.

**See you at Week 2!**
