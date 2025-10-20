# Prompt R2: Literature Evaluation Framework Generator

> **Purpose:** Create custom rubrics and evaluation frameworks to systematically assess research papers for quality, relevance, and contribution.

> **Best AI for this:** Claude Chat (for nuanced criteria) or ChatGPT (for structured frameworks)

---

## 📚 About This Prompt

This prompt helps researchers create **systematic evaluation frameworks** for assessing papers, including:
- Quality assessment rubrics
- Relevance screening criteria
- Methodology evaluation checklists
- Contribution rating systems
- Domain-specific assessment standards

**What this prompt does:**

✅ Generates custom rubrics tailored to your research domain
✅ Creates scoring systems for objective evaluation
✅ Provides extraction templates for key paper information
✅ Helps identify high-quality vs. low-quality papers quickly
✅ Can be used with AI tools for semi-automated evaluation

**Who is this for?**

Researchers who:
- 📋 Need to evaluate many papers systematically
- 🎯 Want consistent quality standards across reviews
- 🔍 Struggle to quickly assess relevance
- 📊 Are doing systematic reviews or meta-analyses
- 🤖 Want to train AI to evaluate papers like they would

---

## 🚀 How to Use This Prompt

**Step 0: Have Your Research Profile Ready** ⭐
- Reference your [research profile](../RESEARCH-PROFILE-ADDITIONS.md)
- Know your research question and domain
- Identify what "quality" means in your field

**Step 1: Fill in Your Criteria**
- What makes a paper valuable to YOU?
- What are deal-breakers (exclude immediately)?
- What are your domain's quality standards?

**Step 2: Generate Your Framework**
- Use this prompt to create custom rubric
- AI will output structured evaluation system

**Step 3: Test & Refine**
- Apply to 5-10 papers
- Adjust criteria based on what works
- Create final version for your project

**Step 4: Use with AI for Scale**
- Give rubric to AI (Claude, ChatGPT)
- Have AI evaluate papers using your framework
- You review AI's assessments

---

## 📋 The Prompt

```markdown
# ROLE

You are an expert research methodologist specializing in systematic literature reviews, meta-analysis, and evidence synthesis. You help researchers create rigorous, domain-appropriate evaluation frameworks for assessing research papers.

# CONTEXT

**My Research Domain:**
- **Field**: [INSERT: e.g., "Clinical Psychology," "Astrophysics," "Medieval History"]
- **Specific topic**: [INSERT: your research question or focus]
- **Review type**: [INSERT: "Narrative review," "Systematic review," "Meta-analysis," "Scoping review"]

**My Research Question:**
```
[INSERT: The specific question you're trying to answer, e.g.,
"What is the effectiveness of CBT for treating social anxiety in adolescents?"
"How do supermassive black holes affect galaxy evolution?"
"What were the primary trade routes in 14th century Europe?"]
```

**What I Need to Evaluate:**
- **Expected paper volume**: [INSERT: "20-50 papers" or "100-200 papers" or "500+ papers"]
- **Publication types**: [INSERT: "Journal articles only" or "Include conference papers" or "Include grey literature"]
- **Time period**: [INSERT: "Last 5 years" or "1990-present" or "All available"]

**My Field's Quality Standards:** [Check what matters in your domain]
- [ ] Peer-reviewed publication (journal tier matters)
- [ ] Sample size / statistical power
- [ ] Methodology rigor (RCT > observational > case study)
- [ ] Replication / reproducibility
- [ ] Theoretical contribution
- [ ] Practical significance
- [ ] Citation count / impact
- [ ] Recency of publication
- [ ] Open data / materials availability
- [ ] Pre-registration (for experimental fields)
- [ ] Other: [Specify domain-specific criteria]

**What Makes a Paper RELEVANT to Me:**
```
[INSERT: Inclusion criteria, e.g.,
"Must study adolescents (ages 12-18), CBT as intervention,
social anxiety as outcome, quantitative measures"]
```

**What Makes a Paper IRRELEVANT (Auto-Exclude):**
```
[INSERT: Exclusion criteria, e.g.,
"Adult populations, other therapeutic approaches,
case studies with n<10, non-English language"]
```

**Assessment Speed Needed:**
- [ ] Deep evaluation (can spend 30+ min per paper)
- [ ] Moderate evaluation (10-15 min per paper)
- [ ] Fast triage (2-5 min per paper to include/exclude)
- [ ] Two-stage (fast triage first, deep dive on included papers)

# TASK

Create a comprehensive literature evaluation framework tailored to my research needs. Include:

## 1. SCREENING RUBRIC (Quick Relevance Check)

Create a fast checklist to determine if a paper is relevant:
- **Essential criteria** (must have ALL of these)
- **Nice-to-have criteria** (bonus but not required)
- **Automatic exclusions** (immediate reject if present)

Format as simple YES/NO checklist that takes <2 minutes.

## 2. QUALITY ASSESSMENT RUBRIC (Detailed Evaluation)

Create a scoring system (e.g., 1-5 scale) for papers that pass screening:

### Methodology Quality
- Research design appropriateness
- Sample/data adequacy
- Analysis rigor
- Bias/confound control
- [Domain-specific methodology criteria]

### Results Quality
- Clarity of findings
- Statistical reporting
- Effect size / practical significance
- Transparency (data, materials)

### Contribution Quality
- Novelty/originality
- Theoretical contribution
- Practical implications
- Relevance to my question

Provide scoring guide: What does "1" look like vs "5" for each criterion?

## 3. KEY INFORMATION EXTRACTION TEMPLATE

Create a structured template to extract important info:
- Bibliographic information
- Research question / hypothesis
- Methodology summary
- Key findings (3-5 bullets)
- Limitations
- Relevance to my question
- Quality score (from rubric above)
- Notes / quotes

Format as copy-paste template I can fill out.

## 4. SYNTHESIS CATEGORIES

Suggest categories for grouping papers:
- By methodology
- By findings (supporting, contradicting, mixed)
- By population/context
- By theoretical framework
- [Domain-specific groupings]

## 5. RED FLAGS CHECKLIST

List warning signs of low-quality or problematic papers in my domain:
- Methodological red flags
- Statistical red flags
- Reporting red flags
- Ethical red flags
- Publication red flags (predatory journals, etc.)

# OUTPUT REQUIREMENTS

**Format**: Structured markdown document with:
- Clear section headers
- Checklists (checkboxes for yes/no items)
- Scoring rubrics (tables or bullet points)
- Copy-paste templates
- Examples of how to apply criteria

**Tone**: Academic and precise. Use terminology from my field. Provide clear operational definitions for subjective criteria.

**Constraints**:
- Criteria must be specific enough for consistent application
- Scoring should be as objective as possible (minimize subjective judgment)
- Fast screening criteria should take <2 min to apply
- Quality rubric should take 10-15 min for full evaluation
- Must be usable by both human reviewers AND AI assistants
- Include guidance on handling edge cases
- Length: 1000-1500 words

**Special Instructions**:
- Tailor methodology criteria to my domain's standards
- If I'm doing systematic review, align with PRISMA guidelines
- If I'm doing meta-analysis, include effect size extraction
- If I'm doing qualitative review, adjust to qualitative criteria
- Provide examples using hypothetical papers in my field
```

---

## 💡 Tips for Best Results

1. **Be specific about your research question** - Drives relevance criteria
2. **Know your field's standards** - Different domains value different things
3. **Test on real papers** - Apply to 5-10 papers, refine criteria
4. **Make it objective** - "Sample size > 100" beats "adequate sample"
5. **Include examples** - Show AI what "high quality" looks like in your field
6. **Start strict, loosen if needed** - Easier to relax criteria than tighten

---

## 🔄 Using Your Rubric with AI

Once you have your rubric, use it with AI for scale:

### With Claude Chat or ChatGPT:

```
I have a paper evaluation rubric for [your field]. Please evaluate
this paper using these criteria:

[Paste your rubric]

Paper details:
Title: [title]
Abstract: [abstract]
[Or paste full paper if within token limits]

Provide:
1. Screening decision (Include / Exclude + reason)
2. Quality scores for each rubric dimension
3. Overall quality rating
4. Filled extraction template
5. Brief summary of strengths/limitations
```

### With Research-Specific AI (Elicit, Consensus, Scite):

- Upload your rubric as evaluation criteria
- Let AI apply to multiple papers
- Review and verify AI's assessments

---

## 📊 Example Application

**Before rubric:**
- "This paper seems good... I think? Not sure if methods are rigorous enough."
- 30 min per paper, inconsistent decisions

**After rubric:**
- "Screening: YES (meets all inclusion criteria). Quality: Methodology 4/5, Results 5/5, Contribution 3/5. Overall: Include as high-quality evidence."
- 10-15 min per paper, consistent and defensible decisions

---

## 🔗 Related Resources

- [Prompt R1: Research Roadmap](prompt-r1-research-roadmap.md) - Your learning path
- [Prompt R3: Research Orchestration](prompt-r3-research-orchestration.md) - Multi-tool workflows
- [Research Workflow: Systematic Review](../WORKFLOWS/systematic-review-workflow.md) - Complete process
- [Domain Adaptations](../DOMAIN-ADAPTATIONS/) - Field-specific evaluation criteria

---

**Ready?** Copy the prompt, customize with your research details, and generate your evaluation framework!
