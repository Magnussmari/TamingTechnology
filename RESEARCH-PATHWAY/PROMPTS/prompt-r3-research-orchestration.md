# Prompt R3: Research AI Orchestration Pattern

> **Purpose:** Coordinate multiple specialized AI tools to work together efficiently for research workflows - search, evaluate, synthesize, and write.

> **Best AI combination:** Scite.ai/Elicit/Consensus (Search) + Perplexity (Current info) + Claude/ChatGPT (Synthesis) + Scripts (Automation)

---

## 📚 About This Workflow

This creates an orchestrated research system where different AI tools handle what they do best:

- **🔍 Search AI** (Scite.ai, Elicit, Consensus) - Finding papers, citation analysis
- **🌐 Web AI** (Perplexity, Gemini) - Current information, preprints, grey literature
- **🧠 Analysis AI** (Claude Chat, ChatGPT) - Deep reading, synthesis, writing
- **⚙️ Automation** (Scripts, Zapier, n8n) - Monitoring, extraction, organization

By orchestrating these specialized tools, you achieve research capabilities impossible with any single AI.

---

## 🎯 Benefits of Research Orchestration

| Benefit | Description |
|---------|-------------|
| **🎯 Specialization** | Each AI does what it's best at - no compromises |
| **📊 Comprehensive Coverage** | Multi-source search catches papers others miss |
| **🔄 Efficient Pipeline** | Automated triage → Deep analysis → Synthesis |
| **🧠 Better Synthesis** | Multiple AI perspectives reveal patterns |
| **📈 Scalability** | Handle 100+ papers as easily as 10 |

---

## 🚀 How to Use This Workflow

**Step 0: Have Your Research System Ready** ⭐
- Complete your [research profile](../RESEARCH-PROFILE-ADDITIONS.md)
- Have your [evaluation rubric](prompt-r2-literature-evaluation.md) created
- Set up [AI Research Workbench](../WORKFLOWS/ai-workbench-setup.md)

**Step 1: Initialize Your Research AI Team**
- Set up each AI tool with context about your project
- Give them your evaluation rubric
- Define their specific roles

**Step 2: Run Your Research Workflow**
- Search AIs find papers
- Analysis AI evaluates using your rubric
- Synthesis AI identifies patterns and gaps
- Automation keeps everything organized

**Step 3: Iterate and Refine**
- Review AI outputs
- Adjust search criteria
- Deepen analysis where needed
- Maintain quality control

---

## 📋 The Orchestration Patterns

### Pattern 1: The Research Pipeline (Most Common)

```
STAGE 1: DISCOVERY (Multi-source search)
├─ Scite.ai → Citation network analysis
├─ Elicit → Semantic search for papers
├─ Consensus → Quick evidence synthesis
├─ Perplexity → Recent papers + preprints
└─ → Combined results (deduplicated)

STAGE 2: TRIAGE (Fast screening)
└─ Claude/ChatGPT → Apply screening rubric
    ├─ Include (high relevance)
    ├─ Maybe (needs human review)
    └─ Exclude (clear mismatch)

STAGE 3: EVALUATION (Quality assessment)
└─ Claude Chat → Apply quality rubric to "Include" papers
    ├─ Extract key information
    ├─ Score each dimension
    └─ Flag for deep reading or skip

STAGE 4: SYNTHESIS (Pattern identification)
└─ Claude Chat → Cross-paper analysis
    ├─ Group by themes
    ├─ Identify agreements/contradictions
    ├─ Find research gaps
    └─ Generate insights

STAGE 5: WRITING (Draft generation)
└─ Claude/ChatGPT → Literature review drafting
    ├─ Introduction
    ├─ Thematic sections
    ├─ Critical synthesis
    └─ Gaps + future directions

YOU (Human Researcher):
└─ Quality control at each stage
└─ Deep reading of key papers
└─ Critical evaluation of AI synthesis
└─ Final writing and argumentation
```

---

## 📝 The Initialization Prompts

### 🔍 PROMPT 1: Search AI Context (Scite.ai, Elicit, Consensus)

Use this when starting a new research project:

```markdown
# RESEARCH PROJECT CONTEXT

**Research Question:**
[Your specific question]

**Domain:** [Your field]

**Inclusion Criteria:**
- [Criterion 1]
- [Criterion 2]
- [Criterion 3]

**Exclusion Criteria:**
- [Criterion 1]
- [Criterion 2]

**Time Range:** [e.g., "2015-2024"]

**Search Strategy:**
- Key concepts: [List 5-10 key terms]
- Required terms: [Must-have terms]
- Exclude terms: [Terms that indicate irrelevance]

**Databases to prioritize:** [e.g., PubMed, arXiv, Scopus]

TASK: Find papers matching these criteria. Prioritize:
1. High methodological rigor
2. Highly cited (relative to age)
3. Recent (last 5 years preferred)
4. Full text available

Return: Title, authors, year, DOI/link, relevance score if available.
```

### 🧠 PROMPT 2: Analysis AI Context (Claude Chat/ChatGPT)

Save this as a conversation in Claude Chat to use throughout your project:

```markdown
# ROLE

You are my research analysis assistant for this project. I will send you papers to evaluate, extract information from, and synthesize. You will apply my evaluation rubric consistently and help identify patterns across papers.

# PROJECT CONTEXT

**Research Question:**
[Your question]

**My Evaluation Rubric:**
[Paste your rubric from Prompt R2]

**Information I Need Extracted:**
- Research question/hypothesis
- Methodology (design, sample, analysis)
- Key findings (3-5 bullets)
- Limitations
- Relevance to my question (1-5 scale with justification)
- Quality score (using rubric above)
- Notable quotes (if exceptional)

# YOUR RESPONSIBILITIES

1. **Evaluate papers**: Apply my rubric consistently
2. **Extract information**: Use the template above
3. **Identify patterns**: Group similar papers, spot contradictions
4. **Flag issues**: Note methodological problems, potential bias
5. **Synthesize**: Connect findings across papers
6. **Suggest gaps**: What's missing from the literature?

# HOW TO RESPOND

When I send you a paper, provide:

## Quick Assessment
[Include/Exclude decision + 1 sentence reason]

## Detailed Evaluation
[Scores for each rubric dimension]

## Extracted Information
[Filled template]

## Synthesis Notes
[How this relates to previous papers, patterns emerging]

I'm ready to receive papers for evaluation.
```

### 📊 PROMPT 3: Synthesis Request (Use after evaluating 10-20 papers)

```markdown
I've now sent you [X] papers for evaluation. Please provide a comprehensive synthesis:

## 1. OVERVIEW
- Total papers evaluated
- Breakdown by quality score
- Breakdown by methodology
- Time range covered

## 2. THEMATIC GROUPING
Group papers by:
- Main findings
- Methodological approach
- Theoretical framework
- [Domain-specific groupings]

## 3. CONVERGENCE & DIVERGENCE
- What do most papers agree on?
- Where are there contradictions?
- What explains the disagreements?

## 4. QUALITY ASSESSMENT
- Overall quality of literature
- Common methodological strengths
- Common limitations
- Papers that stand out (positive or negative)

## 5. RESEARCH GAPS
- What questions remain unanswered?
- What populations/contexts are understudied?
- What methodologies haven't been tried?
- What contradictions need resolving?

## 6. IMPLICATIONS FOR MY RESEARCH
- How does this inform my research question?
- What approaches should I adopt/avoid?
- What gaps could my research fill?

## 7. DRAFT LITERATURE REVIEW OUTLINE
Suggest structure for literature review based on themes.
```

---

## 🔄 Complete Research Workflow Example

### Use Case: Systematic Review of 100+ Papers

**Week 1: Discovery Phase**
```
Monday: Set up AI tools, create context prompts
├─ Scite.ai: Find 150 papers via citation network
├─ Elicit: Find 100 papers via semantic search
├─ Consensus: Quick evidence check
├─ Perplexity: Recent preprints
└─ Total: ~200 papers (with overlap)

Tuesday-Wednesday: Deduplication + Fast Triage
└─ Claude Chat: Apply screening rubric
    ├─ Include: 80 papers
    ├─ Maybe: 40 papers (human review)
    └─ Exclude: 80 papers
```

**Week 2-3: Evaluation Phase**
```
Deep evaluation of 80 "Include" papers:
├─ Send papers to Claude Chat in batches of 10
├─ Apply quality rubric to each
├─ Extract key information
├─ Flag top 20 for human deep reading
└─ Organize by theme
```

**Week 4: Synthesis Phase**
```
Request synthesis from Claude Chat:
├─ Identify 5-7 major themes
├─ Note agreements and contradictions
├─ Highlight research gaps
├─ Flag methodological trends
└─ Generate draft literature review outline
```

**Week 5: Writing Phase**
```
Human + AI collaboration:
├─ You: Deep read top 20 papers
├─ AI: Draft section-by-section literature review
├─ You: Critical editing, add nuance, citations
├─ AI: Refine clarity and structure
└─ You: Final argumentation and voice
```

---

## 🛠️ Tool Specialization Matrix

| Task | Best AI | Why | Alternatives |
|------|---------|-----|--------------|
| **Citation analysis** | Scite.ai | Tracks how papers cite each other (supporting/contrasting) | Connected Papers |
| **Semantic search** | Elicit | Finds papers by meaning not keywords | Consensus, Semantic Scholar |
| **Quick evidence synthesis** | Consensus | Shows what papers agree on instantly | Meta-analyses manually |
| **Recent papers** | Perplexity | Searches web, finds preprints, grey literature | Google Scholar alerts |
| **Deep paper analysis** | Claude Chat | Long context, nuanced understanding | ChatGPT, GPT-4 |
| **Rapid summarization** | ChatGPT | Fast, good for high-volume triage | Claude |
| **Literature mapping** | Research Rabbit | Visual citation networks | Connected Papers |
| **Citation management** | Zotero + AI | Organize papers, AI helps with notes | Mendeley, EndNote |

---

## ⚠️ Quality Control Checkpoints

### Checkpoint 1: After Search (Discovery)
- [ ] Did I search multiple sources?
- [ ] Am I getting ~50-70% relevant papers? (If <30%, search too broad; if >90%, too narrow)
- [ ] Any major papers missing? (Ask AI to find papers citing key authors)

### Checkpoint 2: After Triage (Screening)
- [ ] Apply rubric to 10 papers manually, compare with AI's decisions
- [ ] Check for systematic bias in AI exclusions
- [ ] Review "Maybe" papers yourself

### Checkpoint 3: After Evaluation (Quality Assessment)
- [ ] Spot-check 10 AI evaluations against your own reading
- [ ] Verify citations AI mentions actually exist (hallucination check)
- [ ] Ensure rubric being applied consistently

### Checkpoint 4: After Synthesis
- [ ] Does synthesis match your own reading?
- [ ] Are contradictions explained accurately?
- [ ] Are research gaps defensible?
- [ ] Deep-read 10-20 most important papers yourself

---

## 🚨 Common Pitfalls & Solutions

| Pitfall | Solution |
|---------|----------|
| **AI misses nuance** | Always deep-read key papers yourself |
| **Citation hallucinations** | Verify every citation AI mentions |
| **Rubric drift** | Provide examples with scores periodically |
| **Missing papers** | Use multiple search tools, check key citations |
| **Over-reliance on AI** | Reserve critical thinking for yourself |
| **Inconsistent evaluation** | Batch papers, evaluate same-day for consistency |

---

## 💡 Advanced: Automation Scripts

For high-volume research, consider simple scripts:

### Monitor New Publications (Python example concept)
```python
# Pseudo-code for monitoring new papers
1. Set up keywords and databases
2. Daily automated search
3. AI triages new papers
4. Email digest of relevant ones
5. You review + add to project
```

### Extract Data from PDFs
```python
# Pseudo-code for extraction
1. Load PDF
2. Extract methodology section
3. Find sample size, design, key stats
4. Output to spreadsheet
5. AI fills in missing fields
```

**See [Research Scripts](../TOOLS/research-scripts/) for working examples.**

---

## 🔗 Related Resources

- [Prompt R1: Research Roadmap](prompt-r1-research-roadmap.md) - Your learning path
- [Prompt R2: Literature Evaluation](prompt-r2-literature-evaluation.md) - Create rubrics
- [AI Workbench Setup](../WORKFLOWS/ai-workbench-setup.md) - Install tools
- [Research Tool Matrix](../TOOLS/research-ai-tool-matrix.csv) - Detailed comparison
- [Systematic Review Workflow](../WORKFLOWS/systematic-review-workflow.md) - Step-by-step

---

## 🎓 Remember

**You are the researcher. AI is your research assistant.**

- ✅ AI handles volume, you provide expertise
- ✅ AI finds patterns, you interpret meaning
- ✅ AI drafts, you argue and synthesize
- ✅ AI suggests, you decide
- ✅ AI accelerates, you maintain rigor

**The goal: Do more rigorous research, faster. Never sacrifice quality for speed.**

---

**Ready to orchestrate your research AIs?** Follow the workflow above for your next literature review!
