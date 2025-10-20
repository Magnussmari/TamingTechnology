# AI Research Workbench Setup

**Time:** 2-3 hours
**Goal:** Set up a complete AI-augmented research system from scratch

---

## 🎯 What You're Building

Your **AI Research Workbench** includes:
- 🔍 Multiple search & discovery tools
- 🧠 Analysis & synthesis AI
- 📚 Citation & reference management
- 📝 Note-taking & knowledge management
- ⚙️ (Optional) Automation scripts

---

## 📋 Prerequisites

- [ ] Completed [research profile](../RESEARCH-PROFILE-ADDITIONS.md)
- [ ] Have a research question or project in mind
- [ ] Email account (for tool signups)
- [ ] Budget decided: Free-only or willing to pay for premium tiers

---

## 🛠️ Setup Sequence

### Phase 1: Search & Discovery Tools (30 min)

#### Essential (Pick at least 2):

**1. Scite.ai**
```
What: Citation context analysis
Why: See how papers cite each other (supporting vs. contrasting)
Cost: Free limited, $20/month Pro
Setup:
1. Visit scite.ai
2. Sign up with email
3. Try search: [your research topic]
4. Bookmark key papers
```

**2. Elicit**
```
What: Semantic search + paper summaries
Why: Find papers by concept, get quick summaries
Cost: Free tier (generous), $10/month Plus
Setup:
1. Visit elicit.org
2. Sign up with email
3. Try search: "What is the effect of [your topic]?"
4. Review paper summaries
```

**3. Consensus**
```
What: Quick evidence synthesis
Why: See what papers agree on instantly
Cost: Free + Paid tiers
Setup:
1. Visit consensus.app
2. Ask yes/no question about your topic
3. Review aggregated evidence
```

**4. Google Scholar + Alerts**
```
What: Comprehensive academic search
Why: Free, covers everything, alerts for new papers
Cost: Free
Setup:
1. Visit scholar.google.com
2. Search your topic
3. Click "Create alert" to monitor new papers
4. Configure weekly digest email
```

#### Optional Power Tools:

**Research Rabbit** (Visual citation mapping)
- Visit researchrabbit.ai
- Upload seed papers
- Explore citation network visually

**Semantic Scholar** (Free academic search)
- Visit semanticscholar.org
- Create account
- Set up paper alerts

---

### Phase 2: Analysis & Synthesis AI (20 min)

**1. Claude Chat** (Recommended for research)
```
Setup:
1. Visit claude.ai
2. Sign up (free tier available)
3. Consider Pro ($20/month) for longer papers
4. Create conversation: "[Your Name] - Research Analysis"
5. Initialize with Prompt R3 context (Analysis AI section)
6. Bookmark this conversation - you'll use it throughout project
```

**2. ChatGPT** (Alternative/Supplement)
```
Setup:
1. Visit chat.openai.com
2. Sign up (free tier available)
3. Consider Plus ($20/month) for GPT-4
4. Use for rapid triage and brainstorming
```

**3. Perplexity** (Current information)
```
Setup:
1. Visit perplexity.ai
2. Sign up (free tier excellent)
3. Use for: Recent papers, preprints, news
4. Consider Pro ($20/month) for unlimited searches
```

---

### Phase 3: Citation & Reference Management (30 min)

**Zotero** (Recommended - Free & Open Source)
```
Setup:
1. Visit zotero.org
2. Download desktop app (Windows/Mac/Linux)
3. Install browser connector (Chrome/Firefox/Safari)
4. Create account (for syncing)
5. Create collection: [Your Project Name]
6. Configure settings:
   - File storage: Local or cloud
   - Citation style: [Your field's standard]
   - PDF handling: Rename files automatically
7. Test: Save a paper from Google Scholar
```

**Alternative: Mendeley**
```
Setup:
1. Visit mendeley.com
2. Create account
3. Download desktop app
4. Install web importer
5. Create folder for project
```

**Zotero + AI Integration**
```
Advanced (optional):
- Install Zotero plugins:
  - Better BibTeX (for citation keys)
  - Zotfile (for PDF management)
  - Zotero OCR (for scanned papers)
- Connect to Notion/Obsidian for notes
```

---

### Phase 4: Note-Taking & Knowledge Management (30 min)

**Choose ONE primary system:**

#### Option A: Notion (Recommended for beginners)
```
Setup:
1. Visit notion.so
2. Create account (free personal tier)
3. Create workspace: "Research Projects"
4. Create databases:
   - Papers (linked to Zotero)
   - Notes & Insights
   - To-Read Queue
   - Synthesis & Themes
5. Use templates from community (search "research")
```

#### Option B: Obsidian (For linked thinking)
```
Setup:
1. Visit obsidian.md
2. Download app (free)
3. Create vault: [Your Project Name]
4. Install plugins:
   - Zotero Integration
   - Dataview (for queries)
   - Graph View
5. Use Zettelkasten method:
   - Atomic notes (one idea per note)
   - Link related concepts
   - Build knowledge graph
```

#### Option C: Simple Spreadsheet (Minimalist)
```
Setup:
1. Create Google Sheet or Excel file
2. Columns:
   - Title
   - Authors
   - Year
   - DOI/Link
   - Relevance (1-5)
   - Quality (1-5)
   - Key Findings
   - Notes
3. Use filters and conditional formatting
```

---

### Phase 5: Organization & Workflow (20 min)

**Create Research Folder Structure**
```
Your_Research_Project/
├── Papers/
│   ├── To_Read/
│   ├── Reading/
│   ├── Completed/
│   └── Rejected/
├── Notes/
│   ├── Paper_Summaries/
│   ├── Synthesis_Notes/
│   └── Research_Ideas/
├── Writing/
│   ├── Drafts/
│   └── Final/
├── Data/
│   ├── Extracted_Data/
│   └── Analysis/
└── AI_Outputs/
    ├── Search_Results/
    ├── Evaluations/
    └── Syntheses/
```

**Naming Conventions**
```
Papers: "Author_Year_ShortTitle.pdf"
Notes: "YYYYMMDD_Topic_Notes.md"
Synthesis: "YYYYMMDD_Synthesis_[Theme].md"
```

---

### Phase 6: Workflow Integration (30 min)

**Connect Everything Together**

**1. Paper Discovery → Storage Flow**
```
Scite.ai/Elicit search → Find paper →
Browser extension (Zotero) → Save to collection →
Auto-download PDF → File to "To_Read" folder
```

**2. Paper Evaluation Flow**
```
Open paper →
Skim with evaluation rubric →
Pass to Claude Chat for detailed analysis →
Save AI evaluation to Notion/Obsidian →
Tag paper with quality score →
Move to appropriate folder
```

**3. Synthesis Flow**
```
Batch of 10-20 papers evaluated →
Request synthesis from Claude Chat →
Copy synthesis to Notion/Obsidian →
Link related notes →
Update themes and patterns →
Identify next search queries
```

**4. Writing Flow**
```
Review synthesis notes →
Create outline →
AI drafts section (Claude) →
Human edits for nuance →
Verify citations (Zotero) →
Polish and finalize
```

---

## ⚙️ Optional: Automation Setup (Advanced)

**For tech-comfortable researchers handling high volume (100+ papers)**

### Simple Automation (No coding):

**1. Zapier/n8n Workflows**
```
Trigger: New paper in Google Scholar alert
Action 1: Send to Scite.ai for citation analysis
Action 2: Save to Zotero
Action 3: Create Notion entry
Action 4: Email digest weekly
```

**2. IFTTT Rules**
```
If: New paper matches criteria
Then: Add to reading list + notify
```

### Script-Based Automation (Python):

**See [research-scripts/](../TOOLS/research-scripts/) for examples:**
- Paper monitoring scripts
- PDF text extraction
- Citation network analysis
- Automated literature reviews

---

## ✅ Workbench Checklist

### Core Setup (Everyone needs)
- [ ] At least 2 search tools (Scite, Elicit, Scholar)
- [ ] Claude Chat OR ChatGPT for analysis
- [ ] Perplexity for current information
- [ ] Zotero OR Mendeley for citations
- [ ] Notion OR Obsidian OR Spreadsheet for notes
- [ ] Organized folder structure created

### Integration Setup
- [ ] Browser extension installed (Zotero connector)
- [ ] Citation style configured
- [ ] Paper discovery → storage flow tested
- [ ] AI analysis → notes flow tested
- [ ] Test workflow with 3-5 papers

### Customization
- [ ] Created project-specific collections/folders
- [ ] Set up paper alerts for your topics
- [ ] Initialized Claude Chat with research context
- [ ] Created evaluation rubric (Prompt R2)
- [ ] Saved workflow templates

---

## 🎯 Test Your Workbench

**Complete this 30-minute test:**

1. **Search**: Find 5 papers on your topic using 2 different tools
2. **Save**: Add all 5 to Zotero with proper metadata
3. **Evaluate**: Send 1 paper to Claude Chat for evaluation
4. **Note**: Save AI's evaluation to your notes system
5. **Cite**: Generate a bibliography from Zotero

**If all 5 steps work smoothly → Workbench ready! ✅**

---

## 🚨 Common Setup Issues

| Problem | Solution |
|---------|----------|
| **Browser extension not working** | Check permissions, try different browser |
| **Zotero won't save PDFs** | Check storage settings, verify file permissions |
| **Claude Chat doesn't remember context** | Save as named conversation, bookmark URL |
| **Too many tools overwhelming** | Start with 2-3, add more as needed |
| **Citations not formatting correctly** | Install correct citation style, update Zotero |

---

## 📊 Budget Planning

### Free Tier (Totally Possible)
- Elicit: Free tier (limited searches)
- Consensus: Free tier
- Google Scholar: Free
- Claude Chat: Free tier
- Perplexity: Free tier
- Zotero: Free (open source)
- Obsidian: Free
- **Total: $0/month**

### Recommended Paid Tier
- Scite.ai Pro: $20/month
- Claude Chat Pro: $20/month
- Perplexity Pro: $20/month
- Notion: Free (personal use)
- Zotero: Free
- **Total: $60/month**
- **ROI**: Save 10+ hours/week = $60 for 40+ hours saved

### Power User Tier
- All above: $60/month
- ChatGPT Plus: $20/month
- Elicit Plus: $10/month
- Research Rabbit: Free
- **Total: $90/month**

---

## 🔄 Maintenance

**Weekly:**
- [ ] Check paper alerts (15 min)
- [ ] Process "To Read" queue (1-2 hours)
- [ ] Update synthesis notes (30 min)

**Monthly:**
- [ ] Review and organize Zotero library
- [ ] Backup notes and data
- [ ] Assess workflow efficiency
- [ ] Adjust search alerts if needed

---

## 🔗 Next Steps

1. ✅ Complete workbench setup
2. 📝 Create your [evaluation rubric](../PROMPTS/prompt-r2-literature-evaluation.md)
3. 🔄 Run your first [research workflow](systematic-review-workflow.md)
4. 🎓 Follow your [research roadmap](../PROMPTS/prompt-r1-research-roadmap.md)

---

**Your AI Research Workbench is now ready!** 🚀🔬📚

Start with a small project (10-20 papers) to test the workflow, then scale to larger reviews.
