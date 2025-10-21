# Multi-AI Orchestration Patterns

**Status:** Validated workflows from 2025 research and practitioner reports
**Last Updated:** January 2025

These patterns represent proven workflows for orchestrating multiple AI tools effectively. Each pattern includes real examples, decision criteria, and common pitfalls.

---

## Table of Contents

1. [Pattern 1: Draft + Refinement](#pattern-1-draft--refinement)
2. [Pattern 2: Volume + Depth](#pattern-2-volume--depth)
3. [Pattern 3: Research + Implementation](#pattern-3-research--implementation)
4. [Pattern 4: Multimodal + Text](#pattern-4-multimodal--text)
5. [Pattern 5: Chained Requests](#pattern-5-chained-requests-multi-stage-processing)
6. [Pattern 6: Multi-Agent with Gatekeeper](#pattern-6-multi-agent-with-gatekeeper)
7. [Pattern 7: Parallel Processing](#pattern-7-parallel-processing)
8. [Choosing the Right Pattern](#choosing-the-right-pattern)
9. [Anti-Patterns to Avoid](#anti-patterns-to-avoid)

---

## Pattern 1: Draft + Refinement

**Use Case:** Content creation, documentation, blog posts, explanations

**Core Principle:** Use speed to draft, use quality to refine

### Workflow

```
Step 1: ChatGPT → Rapid initial draft (30-60 seconds)
Step 2: Claude → Quality refinement (1-2 minutes)
Total: 2-3 minutes vs 10 minutes single-tool
```

### Why This Works

- **ChatGPT strengths:** Fast generation, broad knowledge, good structure
- **Claude strengths:** Superior prose, deeper reasoning, better clarity
- **Synergy:** Combined speed + quality beats either alone

### Real Example: Technical Documentation

**Step 1 - ChatGPT:**
```
Prompt: "Write a README for a Python authentication library that uses
JWT tokens. Include installation, quickstart, and basic usage. 300-400 words."

Output: Receives basic structure, installation steps, code examples in 30 seconds
```

**Step 2 - Claude:**
```
Prompt: "Refine this README for clarity, professionalism, and completeness.
Improve code examples, add security notes, make it production-ready.

[Paste ChatGPT output]"

Output: Polished README with better explanations, security warnings, edge cases
```

### Decision Criteria

**Use this pattern when:**
- ✅ You need content quickly but quality matters
- ✅ You're writing documentation, guides, explanations
- ✅ Structure is straightforward but prose needs refinement
- ✅ You want to iterate fast

**Skip this pattern when:**
- ❌ You need deep reasoning from the start (use Claude directly)
- ❌ Content is sensitive/confidential (minimize tool switching)
- ❌ Time is no constraint and you want best first draft

### Common Pitfalls

- ❌ **Over-editing in Step 2:** Claude sometimes over-complicates. Be specific about what to preserve.
- ❌ **Losing voice:** ChatGPT and Claude have different writing styles. Specify tone in both prompts.
- ❌ **Context loss:** If ChatGPT output is long, Claude may miss nuances. Highlight key points.

### Variations

**Variation A: Triple Refinement**
```
ChatGPT (draft) → Claude (refine) → ChatGPT (simplify if Claude over-complicated)
```

**Variation B: Specialized Refinement**
```
ChatGPT (draft) → Claude (technical accuracy) → ChatGPT + DALL-E (add visuals)
```

---

## Pattern 2: Volume + Depth

**Use Case:** Learning new topics, exploring options, research before decisions

**Core Principle:** Broad exploration first, then deep dive on best option

### Workflow

```
Step 1: ChatGPT → Generate multiple options/approaches (2 minutes)
Step 2: You → Select best option based on criteria (1 minute)
Step 3: Claude → Deep analysis of chosen option (3 minutes)
Total: 6 minutes vs 15 minutes exploring sequentially
```

### Why This Works

- **ChatGPT strengths:** Versatility, broad coverage, quick comparisons
- **Claude strengths:** Deep reasoning, nuanced analysis, complex explanations
- **Synergy:** Efficient breadth-first then depth-first search

### Real Example: Choosing State Management

**Step 1 - ChatGPT:**
```
Prompt: "Compare 5 approaches to state management in React applications.
For each, provide: use case, complexity, learning curve, performance,
ecosystem. Format as table."

Output: Comparison of Redux, Zustand, Jotai, Recoil, Context API
```

**Step 2 - You:**
```
Decision: Select Zustand (simple, performance, small team)
```

**Step 3 - Claude:**
```
Prompt: "Explain Zustand state management in depth. Cover:
- Core architecture and philosophy
- Best practices for React applications
- Common patterns and anti-patterns
- Integration with TypeScript
- When to use vs alternatives
- Security considerations

My context: React app with authentication, real-time features, 3-developer team"

Output: Comprehensive guide tailored to your needs
```

### Decision Criteria

**Use this pattern when:**
- ✅ You're exploring unfamiliar territory
- ✅ Multiple valid approaches exist
- ✅ You need to make informed decisions
- ✅ You want to avoid analysis paralysis

**Skip this pattern when:**
- ❌ You already know what you need (go direct to implementation)
- ❌ Only one viable option exists
- ❌ Exploration itself is the goal (no need for depth phase)

### Common Pitfalls

- ❌ **Analysis paralysis:** ChatGPT might present too many options. Limit to 3-5.
- ❌ **Premature selection:** Don't skip your evaluation. AI can't know your specific constraints.
- ❌ **Ignoring context:** Give Claude your selection reasoning in Step 3 for better advice.

### Variations

**Variation A: Iterative Narrowing**
```
ChatGPT (10 options) → You (narrow to 3) → ChatGPT (compare 3) →
You (select 1) → Claude (deep dive)
```

**Variation B: Parallel Depth**
```
ChatGPT (5 options) → You (select top 2) → Claude (deep dive on both) →
You (final selection)
```

---

## Pattern 3: Research + Implementation

**Use Case:** Building features with current best practices, staying up-to-date

**Core Principle:** Research latest → Design architecture → Implement code

### Workflow

```
Step 1: Gemini/Perplexity → Current information, latest practices (3 min)
Step 2: Claude → Architecture and strategy (5 min)
Step 3: Cursor → Implementation in IDE (15-60 min)
Total: Ensures current, well-designed, implemented solution
```

### Why This Works

- **Gemini/Perplexity strengths:** Web access, current information, finding latest docs
- **Claude strengths:** Reasoning, architecture, security considerations
- **Cursor strengths:** IDE integration, contextual code generation, refactoring
- **Synergy:** Up-to-date research → solid design → efficient implementation

### Real Example: Implementing Authentication

**Step 1 - Gemini:**
```
Prompt: "What are 2025 best practices for Next.js 14 authentication?
Include:
- Recommended libraries/approaches
- Security considerations
- Session management options
- Edge runtime compatibility
- Recent changes from 2024"

Output: NextAuth v5 (Auth.js), Clerk, Supabase Auth, better-auth overview
with 2025 updates
```

**Step 2 - Claude:**
```
Prompt: "Design authentication system using NextAuth v5 for Next.js 14 app:

Requirements:
- Email/password + Google OAuth
- Edge runtime compatible
- Role-based access control (user, admin)
- Session management with JWT
- Secure password storage

Provide:
1. Architecture diagram (text description)
2. File structure
3. Security considerations
4. Environment variables needed
5. Database schema for users
6. Edge cases to handle

My stack: Next.js 14 App Router, PostgreSQL, Vercel Edge"

Output: Complete architecture with security best practices
```

**Step 3 - Cursor (in IDE):**
```
Implement based on Claude's architecture:
- Set up NextAuth config
- Create authentication API routes
- Build login/signup components
- Implement middleware for protected routes
- Add role-based access checks

Cursor assists with boilerplate, syntax, integration
```

### Decision Criteria

**Use this pattern when:**
- ✅ Technology/practices change frequently
- ✅ Security or correctness is critical
- ✅ You need current information + solid design
- ✅ Building production features

**Skip this pattern when:**
- ❌ Building internal tools with no external dependencies
- ❌ Using well-understood, stable technologies
- ❌ Time pressure requires moving fast (but accept technical debt)

### Common Pitfalls

- ❌ **Skipping research:** Jumping to Claude without Gemini risks outdated practices
- ❌ **Implementation drift:** Cursor may suggest patterns that differ from Claude's design. Stay aligned.
- ❌ **Security assumptions:** Always validate security claims from research phase

### Variations

**Variation A: Continuous Research**
```
Gemini (initial research) → Claude (design) → Cursor (implement) →
Gemini (research issue encountered) → Claude (adjust design) → Cursor (fix)
```

**Variation B: Documentation Integration**
```
Gemini (find official docs) → You (read key sections) → Claude (design based on docs) →
Cursor (implement) → ChatGPT (generate usage docs)
```

---

## Pattern 4: Multimodal + Text

**Use Case:** Projects needing images, diagrams, UI mockups + written content

**Core Principle:** Use multimodal AI for visuals, specialized AI for text

### Workflow

```
Step 1: ChatGPT + DALL-E → Generate images, mockups, diagrams
Step 2: Claude → Text content, code, technical writing
Step 3: Integration → Combine visual + text components
```

### Why This Works

- **ChatGPT + DALL-E strengths:** Image generation, visual concepts, UI mockups
- **Claude strengths:** Superior prose, code quality, technical depth
- **Synergy:** Best-in-class for each modality

### Real Example: Landing Page

**Step 1 - ChatGPT + DALL-E:**
```
Prompt: "Create hero section image for SaaS productivity app.
Theme: Modern, professional, AI-powered workflow. Color scheme: Blue and white.
Style: Flat design, minimalist"

Output: Hero image
```

```
Prompt: "Create 3 feature icons:
1. AI automation (robot symbol)
2. Team collaboration (people connecting)
3. Analytics dashboard (charts)
Style: Line art, consistent stroke width, professional"

Output: Icon set
```

**Step 2 - Claude:**
```
Prompt: "Write landing page copy for AI productivity SaaS:

Sections needed:
1. Hero headline + subhead (emphasize time saved, AI-powered)
2. Three feature descriptions (match these icons: automation, collaboration, analytics)
3. Social proof section (template for testimonials)
4. CTA (free trial focus)

Tone: Professional, benefit-focused, not hype
Target: Small business owners, 10-50 employees
Value prop: Save 10 hours/week on repetitive tasks

Output: Website copy with clear section breaks
```

**Step 3 - Integration:**
Combine ChatGPT images with Claude copy in your website builder/code

### Decision Criteria

**Use this pattern when:**
- ✅ Project requires both visual and written content
- ✅ You need cohesive branding across modalities
- ✅ Visual quality matters (not just placeholders)
- ✅ Creating marketing materials, presentations, documentation

**Skip this pattern when:**
- ❌ Text-only project (use Claude directly)
- ❌ You have professional designers (they're better than DALL-E)
- ❌ Visuals are incidental/placeholder quality

### Common Pitfalls

- ❌ **Inconsistent style:** DALL-E can produce varied styles. Be specific about consistency.
- ❌ **Text in images:** DALL-E struggles with text. Generate text separately with Claude.
- ❌ **Over-reliance on AI visuals:** For production, human designers often better

### Variations

**Variation A: Diagram Generation**
```
Claude (create Mermaid diagram code) → Render diagram →
Claude (write explanation matching diagram)
```

**Variation B: Presentation Creation**
```
Claude (outline + key points) → ChatGPT + DALL-E (slide visuals) →
Claude (speaker notes)
```

---

## Pattern 5: Chained Requests (Multi-Stage Processing)

**Use Case:** Complex workflows with distinct, sequential stages

**Core Principle:** Process through specialized stages, each AI handling what it does best

### Workflow

```
Tool A: Extract → Tool B: Transform → Tool C: Summarize → Tool D: Format
```

Sequential processing where each stage adds value

### Why This Works

- Each AI optimized for its stage
- Clear hand-offs prevent errors
- Easier to debug than single complex prompt
- Can swap tools per stage as needed

### Real Example: Research Paper Processing

**Stage 1 - Gemini (Extract):**
```
Upload 50-page PDF research paper

Prompt: "Extract from this paper:
1. Research question
2. Methodology
3. Key findings (bullet points)
4. Limitations
5. Future research suggestions
6. All cited statistics/numbers"

Output: Structured extraction
```

**Stage 2 - Claude (Synthesize):**
```
Prompt: "From these extracted findings, create:
1. Executive summary (200 words)
2. Methodology assessment (is it rigorous?)
3. How findings relate to [my research topic]
4. Gaps this paper doesn't address
5. Citations I should follow up on

[Paste Gemini output]"

Output: Synthesized analysis
```

**Stage 3 - ChatGPT (Format):**
```
Prompt: "Convert this analysis into presentation slides outline:
- 1 slide per section
- Bullet points (max 5 per slide)
- Speaker notes under each
- Visual suggestions (charts, diagrams, images)

[Paste Claude output]"

Output: Presentation-ready format
```

### Decision Criteria

**Use this pattern when:**
- ✅ Workflow has clear sequential stages
- ✅ Different AIs excel at different stages
- ✅ You need traceability (can review each stage)
- ✅ Processing large documents or complex data

**Skip this pattern when:**
- ❌ Single AI can handle entire workflow well
- ❌ Stages aren't truly sequential (consider parallel instead)
- ❌ Hand-off friction exceeds benefits

### Common Pitfalls

- ❌ **Information loss:** Each hand-off risks losing context. Include key info in each prompt.
- ❌ **Over-chaining:** Too many stages = complexity. Aim for 2-4 stages maximum.
- ❌ **Wrong tool for stage:** Match AI strengths to stage requirements

### Variations

**Variation A: Code Processing**
```
Claude (design) → Cursor (implement) → Claude (review) →
Cursor (refactor) → You (final validation)
```

**Variation B: Content Pipeline**
```
Gemini (research) → ChatGPT (initial draft) → Claude (refine) →
Grammarly (polish) → You (publish)
```

---

## Pattern 6: Multi-Agent with Gatekeeper

**Use Case:** Complex domains requiring coordination of multiple specializations

**Core Principle:** You route tasks to specialist AIs, integrate results

### Workflow

```
You (Gatekeeper/Orchestrator)
  ├→ Claude (Backend architecture, complex algorithms)
  ├→ Cursor (Frontend implementation)
  ├→ ChatGPT (Documentation, user guides)
  ├→ Consensus/Scite (Research validation)
  └→ You (Integration and quality control)
```

### Why This Works

- **Specialization:** Each AI handles what it does best
- **Parallel work:** Multiple tasks simultaneously
- **Context control:** You maintain overall vision
- **Quality:** Best tool for each subdomain

### Real Example: Full-Stack Feature Development

**Project:** Add payment processing to SaaS app

**Your role (Gatekeeper):** Coordinate all specialists

**Agent 1 - Claude (Backend Design):**
```
Prompt: "Design payment processing backend for SaaS:
- Stripe integration
- Subscription management (3 tiers)
- Webhook handling
- Database schema for subscriptions, payments, invoices
- Security considerations (PCI compliance)
- Error handling and retry logic

Stack: Node.js, PostgreSQL, Express"

Output: Complete backend architecture
```

**Agent 2 - Cursor (Frontend Implementation):**
```
In IDE, implement based on designs:
- Payment form component (React)
- Subscription selection UI
- Payment history table
- Success/failure states

Using Claude's API contracts from Agent 1
```

**Agent 3 - ChatGPT (Documentation):**
```
Prompt: "Create user guide for payment features:
1. How to upgrade subscription
2. How to update payment method
3. How to view payment history
4. FAQ for common issues
5. What happens if payment fails

Tone: Friendly, reassuring, non-technical
Audience: Small business owners"

Output: User-facing documentation
```

**Agent 4 - Consensus (Validation):**
```
Prompt: "What are current PCI compliance requirements for handling
payment data? Latest 2025 standards."

Output: Compliance verification
```

**You (Integration):**
- Ensure Claude's backend contracts match Cursor's frontend
- Verify documentation matches actual feature behavior
- Validate security against Consensus findings
- Test end-to-end flow
- Deploy integrated system

### Decision Criteria

**Use this pattern when:**
- ✅ Project has distinct subdomains (frontend, backend, docs, etc.)
- ✅ Each subdomain benefits from specialized AI
- ✅ You can manage coordination overhead
- ✅ Quality matters more than speed

**Skip this pattern when:**
- ❌ Simple projects (over-engineering)
- ❌ You can't maintain context across agents
- ❌ Time pressure requires simpler workflows

### Common Pitfalls

- ❌ **Lost coherence:** Agents working independently can drift. Define contracts/interfaces upfront.
- ❌ **Coordination overhead:** Too many agents = too much management. Limit to 3-5.
- ❌ **Inconsistent standards:** Each AI has different code style. Establish standards early.

### Variations

**Variation A: Sequential Gatekeeper**
```
You → Agent 1 (design) → You (review) → Agent 2 (implement) →
You (review) → Agent 3 (test) → You (deploy)
```

**Variation B: Hierarchical Agents**
```
You (Project Manager)
  ├→ Claude (Tech Lead) coordinates:
  │    ├→ Cursor (Frontend Dev)
  │    └→ Cursor (Backend Dev)
  └→ ChatGPT (Documentation Lead)
```

---

## Pattern 7: Parallel Processing

**Use Case:** Independent tasks that can run simultaneously

**Core Principle:** Multiple AIs on separate tasks at same time

### Workflow

```
Simultaneously:
Task A → AI 1
Task B → AI 2
Task C → AI 3

Then: Integrate results
```

### Why This Works

- **Time savings:** Parallel vs sequential processing
- **Independence:** No dependencies between tasks
- **Efficiency:** Maximize throughput

### Real Example: New Feature Launch

**Simultaneous tasks:**

**Task A - Claude (Database Schema):**
```
Prompt: "Design PostgreSQL schema for blog feature:
- Posts (title, content, author, tags, status)
- Comments (nested, moderation)
- Tags (many-to-many with posts)
- Media attachments
Include indexes, constraints, migrations"
```

**Task B - ChatGPT (User Documentation):**
```
Prompt: "Write user guide for new blog feature:
- How to create a post
- How to add tags
- How to moderate comments
- How to embed media
Format: Step-by-step with screenshots placeholders"
```

**Task C - Cursor (Project Boilerplate):**
```
In IDE, set up:
- API route files (/api/posts, /api/comments)
- React component structure
- TypeScript interfaces
- Test file templates
```

**Integration:**
- Merge Claude's schema into migration files
- Build API routes using schema
- Implement components in Cursor's structure
- Add ChatGPT's docs to help section

### Decision Criteria

**Use this pattern when:**
- ✅ Tasks are truly independent
- ✅ You can manage multiple conversations
- ✅ Time savings justify coordination
- ✅ No task depends on another's output

**Skip this pattern when:**
- ❌ Tasks have dependencies (use sequential or chained)
- ❌ You'll get confused managing multiple threads
- ❌ Integration complexity exceeds time saved

### Common Pitfalls

- ❌ **Hidden dependencies:** Tasks you thought were independent aren't. Causes rework.
- ❌ **Inconsistent assumptions:** AIs may make different choices. Align constraints upfront.
- ❌ **Context switching cost:** Managing 4+ parallel tasks can slow you down mentally

### Variations

**Variation A: Parallel with Sync Points**
```
Parallel: Tasks A, B, C
→ Sync point: Review all outputs
→ Parallel: Tasks D, E, F (based on A, B, C)
→ Final integration
```

**Variation B: Parallel Exploration**
```
Test 3 different approaches simultaneously:
- Claude: Approach A
- ChatGPT: Approach B
- Cursor: Approach C
→ Compare results, choose best
```

---

## Choosing the Right Pattern

### Decision Matrix

| Pattern | Best For | Time Savings | Complexity | Quality Gain |
|---------|----------|--------------|------------|--------------|
| Draft + Refinement | Content creation | High | Low | Medium |
| Volume + Depth | Exploration, learning | Medium | Low | High |
| Research + Implementation | Current tech, production code | Medium | Medium | High |
| Multimodal + Text | Visual + written projects | Medium | Medium | Medium |
| Chained Requests | Document processing | High | Medium | Medium |
| Multi-Agent Gatekeeper | Complex projects | Low | High | Very High |
| Parallel Processing | Independent tasks | Very High | Medium | Medium |

### By Project Phase

**Planning/Design:**
- Volume + Depth (exploring options)
- Research + Implementation (finding best practices)

**Implementation:**
- Multi-Agent Gatekeeper (complex projects)
- Parallel Processing (independent features)

**Documentation:**
- Draft + Refinement (speed + quality)
- Multimodal + Text (if visuals needed)

**Maintenance:**
- Research + Implementation (staying current)
- Chained Requests (processing updates)

### By Experience Level

**Beginners (Months 1-3):**
- Start with: Draft + Refinement, Volume + Depth
- Avoid: Multi-Agent Gatekeeper (too complex)

**Intermediate (Months 4-6):**
- Add: Research + Implementation, Chained Requests
- Try: Parallel Processing with 2-3 tasks

**Advanced (Month 7+):**
- All patterns
- Custom combinations
- Your own pattern variations

---

## Anti-Patterns to Avoid

### ❌ Anti-Pattern 1: Over-Orchestration

**Problem:** Using 5 AIs for a task one AI handles well

**Example:**
```
ChatGPT (brainstorm) → Claude (refine) → ChatGPT (simplify) →
Gemini (validate) → Claude (final polish)
```

For writing a simple function.

**Fix:** Match complexity to task. Simple tasks → simple workflows.

### ❌ Anti-Pattern 2: Context Loss

**Problem:** Critical information lost in hand-offs between AIs

**Example:**
```
Step 1: Detailed requirements to Claude
Step 2: "Implement this" to Cursor (without requirements)
Result: Implementation missing key constraints
```

**Fix:** Include essential context in every prompt.

### ❌ Anti-Pattern 3: Inconsistent Standards

**Problem:** Each AI using different conventions, styles, approaches

**Example:**
```
Claude: Uses TypeScript strict mode, functional patterns
Cursor: Generates JavaScript, object-oriented patterns
Result: Incompatible code
```

**Fix:** Define standards upfront, include in all prompts.

### ❌ Anti-Pattern 4: Tool Worship

**Problem:** Forcing orchestration because "you should use multiple AIs"

**Example:**
Using Draft + Refinement when Claude alone would be better

**Fix:** Use orchestration when it adds value, not for its own sake.

### ❌ Anti-Pattern 5: No Validation

**Problem:** Trusting each AI output without verification between stages

**Example:**
```
Gemini (research) → Claude (implement based on research)
Without validating Gemini's research was accurate
Result: Implementing based on hallucinated information
```

**Fix:** Validate critical outputs, especially research and data extraction.

---

## Advanced Techniques

### Technique 1: Adaptive Orchestration

Change patterns based on results:

```
Start: Draft + Refinement
If quality insufficient: Switch to Claude-only (no draft phase)
If speed critical: Switch to ChatGPT-only (no refinement)
```

### Technique 2: Nested Patterns

Patterns within patterns:

```
Main: Multi-Agent Gatekeeper
  Agent 1: Uses Draft + Refinement internally
  Agent 2: Uses Research + Implementation internally
  Agent 3: Uses Parallel Processing internally
```

### Technique 3: Feedback Loops

Iterative refinement:

```
Draft + Refinement → Evaluate → If insufficient →
Volume + Depth (explore why) → Redesign → Draft + Refinement again
```

### Technique 4: Pattern Chains

Sequential pattern application:

```
Research + Implementation → Multi-Agent Gatekeeper → Parallel Processing
(Research best approach → Design with specialists → Implement features in parallel)
```

---

## Measuring Effectiveness

### Track These Metrics

**Time Savings:**
- Time with orchestration vs single AI
- Include orchestration overhead
- Aim for >30% savings to justify complexity

**Quality Improvement:**
- Bugs found in code review
- Revisions needed
- User feedback/satisfaction

**Learning:**
- Understanding gained from process
- Patterns discovered
- Skills developed

### When to Adjust

**Increase orchestration if:**
- Quality consistently insufficient
- You're hitting AI limitations
- Projects growing more complex

**Decrease orchestration if:**
- Time overhead exceeds savings
- Results aren't better than single AI
- Losing coherence in outputs

---

## Next Steps

1. **Start simple:** Try Draft + Refinement or Volume + Depth this week
2. **Document what works:** Note which patterns suit which tasks
3. **Gradually add complexity:** Add one new pattern per month
4. **Customize:** Adapt these patterns to your specific needs
5. **Share learnings:** Contribute your patterns to the community

**Remember:** These patterns are tools, not rules. Use what works, skip what doesn't, and create your own variations.

---

## Additional Resources

- [PROMPTS/golden-framework.md](../PROMPTS/golden-framework.md) - Structure individual prompts better
- [ANTI-DEPENDENCY/complete-guide.md](../ANTI-DEPENDENCY/complete-guide.md) - Maintain skills while orchestrating
- [SECURITY/complete-guide.md](../SECURITY/complete-guide.md) - Security validation in workflows
- [WORKFLOWS/case-studies.md](case-studies.md) - Real implementations of these patterns
