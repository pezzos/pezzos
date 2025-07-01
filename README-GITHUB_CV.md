# 🤖 GitHub CV Generator with Claude AI

Transform your GitHub repositories into a professional, automatically-updated CV using Claude AI commands.

## 🎯 What This Is

This project demonstrates how to create an **automated CV generation system** that:
- ✅ Pulls all your public GitHub repositories automatically
- ✅ Generates professional project descriptions 
- ✅ Creates technical expertise sections from your actual code
- ✅ Updates statistics (repos, stars, followers) in real-time
- ✅ Preserves your personal content while automating the technical showcase
- ✅ Uses simple configuration files to control what appears

## 🚀 How It Works

### Core Components

1. **REPOS.md** - Configuration file that controls:
   - Which repositories appear in your CV
   - Priority ordering (1-10 scale)
   - Custom descriptions and highlights
   - Technology tags for categorization

2. **Claude Commands** - Automation tools:
   - `/init-cv` - 🆕 Intelligently generates complete CV from scratch
   - `/refresh-repos` - Syncs latest GitHub data
   - `/update-cv` - Regenerates CV sections from configuration

3. **Live Integration** - Real-time data:
   - GitHub API for repository information
   - MCP (Model Context Protocol) tools for seamless automation
   - Intelligent parsing of README files and code

### The Magic ✨

#### 🚀 **Smart Initialization with `/init-cv`**

For first-time users, the AI does the heavy lifting:
1. **Analyzes your GitHub profile** - repositories, languages, contribution patterns
2. **Searches Claude's memory** - for any previous information about you
3. **Asks intelligent questions** - only what's needed to complete your profile
4. **Auto-generates everything** - professional README.md and configured REPOS.md
5. **Stores your profile** - in Claude's memory for future sessions

#### 🔄 **Effortless Maintenance**

Once set up, you simply:
1. **Configure once** in REPOS.md which projects to showcase
2. **Run `/update-cv`** whenever you want to refresh your CV
3. **Your CV stays current** with live GitHub statistics and project updates

## 🛠️ How to Build Your Own

### Prerequisites

- [Claude Code](https://claude.ai/code) (Claude's official CLI)
- GitHub account with public repositories
- Basic familiarity with markdown files

### Prerequisites

1. **Clone or fork this repository** as a template
2. **Install Claude Code** and ensure GitHub CLI (`gh`) is configured

### Step 1: Install
**Copy the automation files** (optional, use only if you already have a GitHub presentation page)
   - `.claude/commands/init-cv.md` 
   - `.claude/commands/update-cv.md`
   - `.claude/commands/refresh-repos.md`
   - `CLAUDE.md` (project-specific Claude instructions)

### Step 2: First-Time CV Generation
**Run Claude Code** in your directory

**🆕 To create the first presentation** - Use the intelligent CV generator:

1. **Run `/init-cv`** in your project directory
2. **Answer interactive questions** about your professional profile:
   - Current role and career focus
   - Location and contact preferences  
   - Professional goals and target audience
   - Technology preferences and expertise areas
3. **Review the generated CV** - Claude analyzes your repos and creates:
   - Complete professional README.md
   - Configured REPOS.md with intelligent defaults
   - Your profile stored in Claude's memory for future updates

### Step 3: Update info from your other repos (only if you didn't use /init-cv)
1. **Run `/refresh-repos`** to generate your initial REPOS.md or update it
2. **Edit REPOS.md** to configure:
   ```markdown
   - **include_in_cv**: true/false
   - **priority**: 1-10 (1 = highest)
   - **custom_description**: Your professional description
   - **highlights**: Key achievements to showcase
   - **tags**: Technologies for auto-categorization
   ```

### Step 4: Finalize Your CV

**If you used `/init-cv`**:
1. **Review the generated content** - everything is already created!
2. **Fine-tune personal sections** if desired (interests, philosophy, etc.)
3. **Test `/update-cv`** to see how future updates work
4. **Commit your changes** and push to GitHub

**Else**:
1. **Run `/update-cv`** to generate your professional README.md
2. **Review and adjust** personal sections as needed
3. **Commit your changes** and push to GitHub

### Step 5: Maintenance

- **Add new projects**: Run `/refresh-repos` then configure new entries in REPOS.md
- **Update descriptions**: Edit REPOS.md and run `/update-cv`
- **Refresh stats**: `/update-cv` automatically pulls latest GitHub statistics

## 🧠 Enhanced with Claude Memory

For even better results, connect Claude Code with Claude Desktop and enable memory:

- **Context Persistence**: Your preferences and project history carry between sessions
- **Smart Descriptions**: Claude learns your writing style and technical preferences  
- **Better Categorization**: Improved understanding of your technology stack
- **Project Evolution**: Tracks how your projects develop over time

## 🎨 Customization Ideas

- **Industry Focus**: Adapt technology categories for your field
- **Project Types**: Configure different highlight templates
- **Branding**: Customize the personal sections and contact information
- **Metrics**: Add custom statistics or achievement tracking
- **Multi-language**: Generate CVs in different languages
- **Theme Variations**: Create different CV styles for different audiences

## 🤝 Contributing

This project demonstrates the power of AI-assisted automation for developers. If you:

- **Build improvements** to the system
- **Create new CV templates** or automation commands  
- **Add features** like multi-language support or new integrations
- **Fix bugs** or enhance the documentation

Please consider contributing back! Open issues, submit PRs, or share your innovations.

### 💡 Attribution

If this system helps you land a great opportunity or impresses potential collaborators, a mention would be awesome:

> *"CV automation system inspired by [Alexandre Pezzotta's GitHub CV Generator](https://github.com/pezzos/pezzos)"*

## 📄 License

This project is released under the **MIT License** - feel free to use, modify, and distribute!

```
MIT License - Use freely, modify as needed, share with attribution
```

## 🔗 Learn More

- **Claude AI**: [claude.ai](https://claude.ai)
- **Claude Code**: [Claude Code Documentation](https://docs.anthropic.com/claude-code)
- **MCP (Model Context Protocol)**: [MCP Docs](https://docs.anthropic.com/claude-code/mcp)
- **Original Creator**: [Alexandre "Pezzos" Pezzotta](https://github.com/pezzos)

---

**Ready to automate your professional presence?** Star this repo and start building your own AI-powered CV! 🌟