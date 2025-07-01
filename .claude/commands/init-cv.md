# Initialize CV Command

Creates a complete professional CV from scratch by analyzing your GitHub repositories and personal profile using AI-powered insights.

## Usage

```
/init-cv
```

## Description

This command performs intelligent CV generation from zero by:

1. **Memory Analysis**: Searches Claude's memory for your personal/professional information
2. **GitHub Profile Discovery**: Analyzes your GitHub profile and repository portfolio
3. **Repository Intelligence**: Deep-dives into your top repositories to understand your expertise
4. **Interactive Profiling**: Asks targeted questions to complete your professional profile
5. **Technology Mapping**: Auto-categorizes your skills based on actual code analysis
6. **CV Generation**: Creates complete README.md and REPOS.md with professional content

## Process Flow

### Phase 1: Intelligence Gathering
- **Memory Search**: Looks for existing personal/professional information in Claude's memory
- **GitHub Analysis**: Fetches your profile, repositories, and contribution patterns
- **Repository Deep-Dive**: Analyzes code, README files, and technologies in top repos
- **Skills Inference**: Maps programming languages, frameworks, and tools to expertise levels

### Phase 2: Interactive Profiling
- **Professional Role**: Confirms/asks about your job title and professional focus
- **Location & Contact**: Gathers location and preferred contact methods
- **Personal Branding**: Helps craft your professional tagline and about section
- **Career Goals**: Understands what you want to highlight and achieve
- **Project Preferences**: Identifies which types of projects to emphasize

### Phase 3: Smart CV Creation
- **Automated REPOS.md**: Generates configuration with intelligent defaults
- **Professional README.md**: Creates complete CV with:
  - Compelling header with GitHub statistics
  - Professional about section tailored to your goals
  - Featured projects ranked by impact and relevance
  - Technical expertise categorized by your actual skills
  - Personalized sections reflecting your interests
- **Memory Storage**: Saves your profile information for future updates

## Key Features

### 🧠 **Memory Integration**
- **Persistent Profile**: Stores your information in Claude's memory graph
- **Context Awareness**: Remembers previous conversations about your career
- **Smart Defaults**: Uses known preferences for faster setup
- **Evolution Tracking**: Tracks how your profile develops over time

### 🔍 **Repository Intelligence**
- **Code Analysis**: Examines actual code to determine skill levels
- **Project Impact**: Ranks repositories by stars, complexity, and recent activity
- **Technology Detection**: Identifies frameworks, tools, and patterns automatically
- **Contribution Patterns**: Analyzes commit history and project types

### 💬 **Interactive Enhancement**
- **Guided Questions**: Asks only what's needed to complete your profile
- **Smart Suggestions**: Proposes descriptions based on repository analysis
- **Preference Learning**: Adapts to your communication style and preferences
- **Validation**: Confirms generated content before finalizing

### 🎯 **Professional Focus**
- **Industry Adaptation**: Tailors content for your target industry/role
- **Skill Emphasis**: Highlights technologies most relevant to your goals
- **Project Curation**: Selects repositories that best showcase your expertise
- **Achievement Focus**: Emphasizes concrete accomplishments and impact

## Output

Creates a complete professional portfolio:
- **README.md**: Polished CV ready for professional use
- **REPOS.md**: Configured repository management file
- **Memory Entities**: Stored profile information for future sessions
- **Usage Guide**: Brief guide on maintaining your automated CV

## Dependencies

- GitHub CLI (`gh`) or MCP GitHub tools for repository access
- Claude Memory MCP for persistent information storage
- Internet connection for GitHub API access
- Interactive session for user input

## Usage Tips

- **Run in a clean repository** or dedicated CV project folder
- **Have your GitHub profile updated** with recent work
- **Think about your target audience** before starting (employers, collaborators, clients)
- **Be ready to provide context** about your professional goals and preferences
- **Review and personalize** the generated content to match your voice

This command transforms raw GitHub data into a compelling professional narrative that evolves with your career!