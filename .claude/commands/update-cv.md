# Update CV Command

Updates specific sections of the README.md based on the REPOS.md configuration file while preserving personal content.

## Usage

```
/update-cv
```

## Description

This command performs targeted updates to README.md:
1. **Updates statistics line**: Repository count, stars, followers from GitHub
2. **Regenerates "🏆 Featured Projects" section**: Based on `include_in_cv: true` repos, sorted by priority and stars
3. **Updates "💻 Technical Expertise" section**: Extracted from repository tags and technologies
4. **Preserves all other content**: About me, philosophy, personal interests, contact info remain unchanged

## Targeted Sections Updated

- **Statistics**: `📍 Lyon, France | 🚀 X Public Repositories | ⭐ X GitHub Stars | 👥 X Followers`
- **Featured Projects**: Complete regeneration based on REPOS.md configuration
- **Technical Expertise**: Languages, specializations, tools derived from project tags

## Preserved Sections

- Personal introduction and about me
- Philosophy & approach
- Fun facts & personal interests
- Contact information
- Future projects (manually maintained)

## Dependencies

- GitHub CLI (`gh`) for live statistics
- REPOS.md configuration file with proper formatting
- Existing README.md structure

## Behavior

- **Non-destructive**: Only updates specified sections
- **Configuration-driven**: Uses REPOS.md priorities and settings
- **Live data**: Fetches current GitHub statistics
- **Smart sorting**: Projects sorted by priority (1-10) then by star count

This approach allows you to maintain personal content while automatically updating the technical portfolio sections.