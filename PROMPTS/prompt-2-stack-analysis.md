# Prompt 2: Tech Stack Analysis & Explanation

> **Purpose:** Understand your project's technology stack by having AI analyze your dependencies and explain how all the pieces fit together.

> **Best AI for this:** Claude Code (for codebase analysis) or Claude Chat (for architectural explanation)

---

## 📚 About This Prompt

This prompt helps you **understand the technology stack** of your project by analyzing dependencies and explaining the relationships between different components.

**What this prompt does:**

✅ Analyzes your project's package.json (or equivalent dependency file)
✅ Explains the role of each major technology in your stack
✅ Shows how data flows through your application architecture
✅ Identifies AI augmentation opportunities for your specific stack
✅ Suggests a learning path prioritizing the most important technologies

**Who is this for?**

Developers who:
- 🔍 Want to understand the technologies in their project beyond surface level
- 🔍 Are working with a codebase they didn't create
- 🔍 Need to explain their tech stack to others (team members, stakeholders)
- 🔍 Want to identify which technologies to learn first

---

## 🚀 How to Use This Prompt

**Step 0: Reference Your Profile** ⭐
- Have your [USER-PROFILE.md](../USER-PROFILE.md) handy
- Reference your "Current Projects" section for project details
- Check your "Tech Stack Preferences" to see what you want to understand

**Step 1: Prepare Your Project Information**
- Locate your `package.json`, `requirements.txt`, or equivalent dependency file
- Note your main framework (React, Next.js, Vue, etc.)
- Identify your project type (e-commerce, blog, SaaS, etc.)

**Step 2: Fill in the Context**
- Replace all `[INSERT: ...]` placeholders with your project details
- Be specific about what you want explained

**Step 3: Send to AI**
- Works best with **Claude Code** (can scan actual files) or **Claude Chat** (for explanations)

**Step 4: Review the Analysis**
- Read through the component breakdown
- Study the data flow explanation
- Note the suggested learning path

---

## 📋 The Prompt

Copy everything below this line and customize the `[INSERT: ...]` sections:

```markdown
# ROLE

You are a senior full-stack developer and technical architect with deep expertise in modern web development frameworks, libraries, and deployment infrastructure. You specialize in analyzing project dependencies and explaining how different technologies work together in a cohesive system.

# CONTEXT

I'm working on a project and need to understand the technology stack better. I'm transitioning from prompt-based development tools to working directly with code, and I need clear explanations of how the pieces fit together.

**Project Information:**
- **Project name/type**: **[INSERT: e.g., "E-commerce dashboard," "Personal blog," "SaaS application"]**
- **Main framework/library**: **[INSERT: e.g., "React," "Next.js," "Vue," "Svelte"]**
- **Package manager**: **[INSERT: package.json, requirements.txt, or other dependency file location]**

**What I need explained:**
- How the different technologies in my stack relate to each other
- What role each major dependency plays
- Why these technologies were chosen (their strengths)
- How data flows through the application architecture
- What the deployment/hosting setup involves

# TASK

Analyze my project's technology stack and provide a comprehensive explanation organized as follows:

1. **Stack Overview**: Provide a high-level summary of the entire tech stack using #systemsthinking principles. Explain the architecture pattern (e.g., JAMstack, monolithic, microservices, serverless).

2. **Component Breakdown**: For each major technology in the stack, explain:
   - **Purpose**: What problem does this solve?
   - **Role in the system**: Where does it fit in the architecture?
   - **Key relationships**: What other technologies does it interact with?
   - **Common patterns**: How is it typically used in this type of project?

3. **Dependency Analysis**: Review the main dependencies from package.json (or equivalent) and categorize them:
   - **Core framework dependencies**: The foundation of the application
   - **UI/Styling libraries**: How the interface is built
   - **State management**: How data is managed
   - **Data fetching/API tools**: How the app communicates with backends
   - **Development tools**: Build tools, testing, linting, etc.
   - **Deployment/Infrastructure**: Hosting, databases, authentication services

4. **Data Flow Explanation**: Describe how data moves through the application from user interaction → frontend → API/backend → database and back, using #fullstack thinking.

5. **AI Augmentation Opportunities**: Identify where #aiaugmentation can enhance my development workflow with this specific stack (e.g., which AI tools work best with these technologies, common patterns to prompt for).

6. **Learning Path**: Based on this stack, suggest which technologies I should prioritize learning first to be productive.

# OUTPUT REQUIREMENTS

**Format**: Structured markdown document with clear hierarchical sections. Use:
- **Headings** for major sections
- **Bullet points** for lists of technologies
- **Code blocks** to show examples of configuration files or key code patterns when relevant
- **Diagrams in text** (using ASCII or simple text flow) to illustrate architecture if helpful

**Tone**: Educational and clear. Assume I can read code but may not understand why certain architectural decisions were made. Explain concepts without being condescending.

**Constraints**:
- Focus on the specific technologies actually present in my project
- Explain relationships between components, not just individual tech descriptions
- Use concrete examples from my actual codebase when possible
- Highlight which parts of the stack handle frontend vs. backend vs. deployment
- Include version considerations if there are breaking changes I should know about
- Keep length between 800-1200 words depending on stack complexity
- Integrate #aiaugmentation #fullstack #systemsthinking concepts where relevant to help me understand not just "what" but "why" and "how"

**Special Instructions for IDE AI Agent**:
- Scan package.json, requirements.txt, or equivalent dependency files
- Check framework config files (next.config.js, vite.config.js, etc.)
- Review folder structure to understand architecture patterns
- Identify API routes, database connections, and external service integrations
- Note any environment variables or deployment configurations
```

---

## 💡 Tips for Best Results

1. **Use Claude Code** if you have the project open - it can scan your actual files
2. **Be specific** about which parts confuse you most
3. **Save the output** as `Tech_Stack_Analysis_[ProjectName].md` for future reference
4. **Review regularly** - re-run when you add major dependencies
5. **Share with team** - great onboarding documentation

---

## 🔄 When to Re-run This Prompt

- When joining a new project or team
- After major dependency updates or migrations
- When adding significant new technologies
- Before explaining architecture to stakeholders
- When feeling lost in the codebase

---

## 🔗 Related Resources

- [Prompt 1: Learning Roadmap](prompt-1-roadmap.md) - Create your learning plan
- [Prompt 3: Senior-Junior Pattern](prompt-3-senior-junior.md) - Build with AI collaboration
- [Complete Guide](../COMPLETE-GUIDE.md) - Full AI Orchestration system
- [AI Tool Matrix](../TOOLS/ai-tool-matrix.csv) - Choose the right AI for analysis

---

**Ready?** Copy the prompt above, customize it, and send it to Claude Code or Claude Chat!
