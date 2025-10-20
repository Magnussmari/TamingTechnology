# Prompt R1: Research Roadmap Generator

> **Purpose:** Create a personalized learning path for researchers transitioning from manual research workflows to AI-augmented research systems.

> **Best AI for this:** Perplexity (for current research tools) or Claude Chat (for strategic planning)

---

## 📚 About This Prompt

This prompt creates a **custom learning roadmap** for academic researchers who want to:
- Automate literature reviews
- Use AI for paper evaluation and synthesis
- Build research scripts and workflows
- Set up an AI Research Workbench
- Progress from zero AI knowledge to advanced research automation

**What this prompt does:**

✅ Assesses your current research workflow and pain points
✅ Identifies which AI tools best fit your research needs
✅ Creates a step-by-step path from manual → AI-augmented research
✅ Provides domain-specific tool recommendations
✅ Includes milestone projects to validate learning

**Who is this for?**

Researchers ready to:
- 🔬 Automate repetitive research tasks
- 📚 Handle larger paper volumes efficiently
- 🎯 Improve literature review quality and speed
- 🤖 Learn research-specific AI tools (Scite.ai, Elicit, etc.)
- 📊 Build simple scripts for research automation

---

## 🚀 How to Use This Prompt

**Step 0: Have Your Research Profile Ready** ⭐
- Complete [USER-PROFILE.md](../../USER-PROFILE.md) first
- Then complete [RESEARCH-PROFILE-ADDITIONS.md](../RESEARCH-PROFILE-ADDITIONS.md)
- Combine into `MY-RESEARCH-PROFILE.md`

**Step 1: Fill in Your Information**
- Reference your research profile sections
- Replace all `[INSERT: ...]` placeholders below
- Be specific about your research domain and goals

**Step 2: Copy the Entire Prompt**
- Select everything from "# ROLE" to "# OUTPUT REQUIREMENTS"
- Copy to clipboard

**Step 3: Send to AI**
- Paste into **Perplexity** or **Claude Chat**
- Review the generated research learning roadmap

**Step 4: Follow Your Roadmap**
- Work through milestones sequentially
- Practice with real research tasks
- Build your AI Research Workbench

---

## 📋 The Prompt

Copy everything below and customize the `[INSERT: ...]` sections:

```markdown
# ROLE

You are an expert research methodologist and AI tools specialist. You help academic researchers transition from manual, time-intensive research workflows to efficient AI-augmented research systems. You understand the unique needs of researchers across domains and can recommend appropriate AI tools and workflows.

# CONTEXT

**My Research Background:**
- **Field**: [INSERT: e.g., "Neuroscience," "Economics," "Medieval History"]
- **Sub-field**: [INSERT: specific area]
- **Research stage**: [INSERT: e.g., "PhD student (dissertation)," "Postdoc," "Assistant Professor"]
- **Current project**: [INSERT: what you're researching]

**Current Research Workflow (What's Broken):**
```
[INSERT: Describe your current process and pain points, e.g.,
"I search Google Scholar, download 100+ PDFs, read abstracts manually,
take notes in Word, spend 10+ hours/week just finding papers.
I'm overwhelmed by volume and miss important papers. Citation management
is chaos. Can't keep up with new publications."]
```

**Paper Volume I Handle:**
- [INSERT: "10-20 papers/project" or "100+ for systematic review" or "Monitor 50+ new papers/month"]

**Tools I Currently Use:**
- Search: [INSERT: e.g., "Google Scholar, PubMed"]
- Citations: [INSERT: e.g., "Zotero," "EndNote," "chaos"]
- Notes: [INSERT: e.g., "Notion," "Word docs," "paper notebooks"]
- AI tried: [INSERT: e.g., "ChatGPT for summaries sometimes," "None yet"]

**Technical Comfort Level:**
- Programming: [INSERT: "Never coded" or "Can copy scripts" or "Comfortable with Python"]
- Willing to learn scripting: [INSERT: YES/NO - "If yes, for what tasks?"]

**What I Want AI to Help With:** [Check your top 3-5]
- [ ] Literature search and discovery
- [ ] Paper evaluation (quality, relevance)
- [ ] Summarization and key findings extraction
- [ ] Synthesis across multiple papers
- [ ] Gap identification
- [ ] Hypothesis generation
- [ ] Writing (papers, grants, reviews)
- [ ] Data analysis
- [ ] Citation management
- [ ] Staying current with new publications
- [ ] Other: [Specify]

**My Research Goals (Next 3-6 Months):**

1. [INSERT: e.g., "Complete comprehensive literature review for dissertation (100+ papers)"]
2. [INSERT: e.g., "Submit 1-2 papers for publication"]
3. [INSERT: e.g., "Write grant proposal with strong lit review"]

**Time Availability:**
- Hours per week for learning AI tools: [INSERT: e.g., "5 hours," "10 hours"]
- Urgency: [INSERT: e.g., "Dissertation deadline in 6 months," "Steady progress fine"]

# TASK

Based on my research profile and needs above, create a personalized AI-augmented research learning roadmap that:

1. **Assesses My Starting Point**: Acknowledge my current workflow and validate the transition I'm making from manual to AI-augmented research. Identify my biggest pain points that AI can address immediately.

2. **Recommends Research-Specific AI Tools**: Based on my domain, paper volume, and technical comfort, suggest:
   - **Search & Discovery**: Which AI tools for finding papers (Perplexity, Elicit, Consensus, Scite.ai, etc.)
   - **Evaluation & Synthesis**: Which tools for analyzing papers (Claude, ChatGPT, specialized research AI)
   - **Organization**: Citation management integration, note-taking systems
   - **Automation**: Whether scripting makes sense for my needs (and if so, what language/tools)

3. **Builds a Progressive Learning Path**: Structure the roadmap in phases:

   **Phase 1: Foundation (Week 1-2)**
   - Set up AI Research Workbench (essential tools)
   - Learn basic AI prompting for research
   - Practice on 5-10 papers in my field

   **Phase 2: Core Skills (Week 3-4)**
   - Master literature search with AI
   - Systematic paper evaluation
   - Build evaluation rubrics for my domain
   - Organize findings effectively

   **Phase 3: Advanced Integration (Week 5-6)**
   - Multi-tool orchestration workflows
   - Synthesis and gap identification
   - Writing assistance (if requested)
   - Basic scripting (if applicable)

   **Phase 4: Automation & Mastery (Week 7-8)**
   - Automated monitoring of new publications
   - Custom research workflows
   - Integration with existing tools (Zotero, Notion, etc.)
   - Full research project using AI system

4. **Provides Domain-Specific Guidance**: Tailor recommendations to my field:
   - Which databases/sources to prioritize
   - Domain-specific evaluation criteria
   - Typical research workflows in my area
   - Common pitfalls in my field that AI can help avoid

5. **Includes Milestone Projects**: Define 3-5 specific research tasks to validate progress:
   - Week 2: Process 10 papers on [my topic] using AI, create summary table
   - Week 4: Build paper evaluation rubric for my domain, apply to 20 papers
   - Week 6: Complete mini-literature review (30-50 papers) using full AI workflow
   - Week 8: Set up automated monitoring + synthesis system for my field

6. **Addresses Research Ethics & Quality**: Include guidance on:
   - Verifying AI-generated summaries
   - Avoiding hallucinations in citations
   - Maintaining research rigor
   - When to use AI vs. deep reading
   - Transparency in AI-assisted research

# OUTPUT REQUIREMENTS

**Format**: A personalized research learning roadmap structured as a markdown document with:
- Clear weekly phases
- Specific tool recommendations with rationale
- Step-by-step instructions for each phase
- Milestone validation projects
- Time estimates for each activity

**Tone**: Academic but practical. Respect my research expertise while introducing AI tools. Use field-appropriate language. No condescension.

**Constraints**:
- Focus on tools I actually have access to or can access
- Match recommendations to my technical comfort level
- Don't recommend complex scripting if I said "NO" to programming
- Prioritize tools that integrate with my existing workflow
- Address my specific pain points identified above
- Suggest realistic timeline based on my time availability
- Include both free and paid tool options where relevant
- Length: 800-1200 words depending on complexity of needs

**Special Considerations**:
- If I handle high paper volume (100+), emphasize automation
- If I'm non-technical, focus on no-code AI solutions
- If I'm technical, include scripting opportunities
- Tailor to my domain's norms (citations styles, databases, etc.)
- Account for my deadline pressure (or lack thereof)
```

---

## 💡 Tips for Best Results

1. **Be specific about your field** - "Machine learning in NLP" beats "Computer science"
2. **Honest about technical skills** - Accurate assessment = better tool recommendations
3. **Describe current pain** - Detail what's broken in your workflow
4. **Set clear goals** - Specific outputs ("submit 2 papers") beat vague ("get better")
5. **Note your paper volume** - Drives automation recommendations
6. **Save your output** - Name it `[YourName]_Research_Roadmap_[Date].md`

---

## 🔄 When to Re-run This Prompt

- Starting a new research project with different scope
- Moving to a new research domain
- Technical skills level up (now ready for scripting)
- Current roadmap complete, want next level
- Research goals significantly change

---

## 🔗 Related Resources

- [Prompt R2: Literature Evaluation Framework](prompt-r2-literature-evaluation.md) - Create paper rubrics
- [Prompt R3: Research AI Orchestration](prompt-r3-research-orchestration.md) - Multi-tool workflows
- [AI Research Workbench Setup](../WORKFLOWS/ai-workbench-setup.md) - Tool installation guide
- [Research Tool Matrix](../TOOLS/research-ai-tool-matrix.csv) - Which AI for what research task

---

**Ready?** Copy the prompt above, customize with your research profile, and send to Perplexity or Claude Chat!
