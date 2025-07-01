# Refresh Repositories Command

Updates the REPOS.md file with the latest repository information from GitHub while preserving manual configurations.

## Usage

```
/refresh-repos
```

## Description

This command:
1. Fetches all public repositories from GitHub using the GitHub CLI or MCP
2. Retrieves repository metadata (stars, languages, descriptions, dates)
3. Reads existing REPOS.md configuration
4. Merges new repository data with existing manual configurations
5. Preserves user customizations (include_in_cv, priority, custom_description, etc.)
6. Adds new repositories with default settings
7. Updates the REPOS.md file

## Dependencies

- GitHub CLI (`gh`) or MCP GitHub tools
- Internet connection for GitHub API access

## Behavior

- **New repositories**: Added with `include_in_cv: false` by default
- **Existing repositories**: Manual settings preserved, only metadata updated
- **Deleted repositories**: Removed from the list
- **Repository metadata**: Stars, descriptions, languages automatically updated

## Output

Updates REPOS.md with:
- Latest repository information
- Preserved manual configurations
- New repositories ready for configuration
- Updated metadata for existing repositories

After running this command, review REPOS.md to configure new repositories before running `/update-cv`.