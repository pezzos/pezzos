# Backlog de sujets (Notion Database)

This database tracks blog ideas that have been explored with ChatGPT. Use the Notion MCP tools to read, list, and maintain its entries.

## Identifiers
- **Database title:** `Backlog de sujets`
- **Database URL:** `https://www.notion.so/2a12c6b40808805fb9f8c7729299afb8`
- **Primary data source ID:** `collection://2a12c6b4-0808-8022-9b1d-000b3c2cfbfb`
- **Default view:** `view://2a12c6b4-0808-80e7-a431-000c58b22e5a`

## Schema
| Property              | Type         | Notes                                                                 |
| --------------------- | ------------ | --------------------------------------------------------------------- |
| `Titre provisoire`    | Title        | Required title of the subject.                                        |
| `Description / Angle` | Text         | Short description or framing.                                         |
| `Brouillon`           | Text         | Long-form draft text that feeds future articles or vidéos.             |
| `Priorité`            | Select       | One of `High`, `Medium`, `Low`.                                       |
| `Type`                | Multi-select | Any of `Série`, `Short`, `Article`, `Vidéo`.                          |
| `Destinations`        | Multi-select | Any of `Blog`, `YouTube`, `HackerNews`, `Reddit`, `Instagram`, `LinkedIn`. |
| `Tags`                | Multi-select | Any of `#intro`, `#parcours`, `#relation`, `#ia`, `#émotion`, `#productivité`, `#routine`, `#habitudes`, `#workflow`, `#devops`, `#éthique`, `#dev`, `#tdah`, `#apprentissage`, `#infrastructure`, `#automation`, `#astuces`, `#minimalisme`, `#santé`, `#expérience`, `#projets`, `#humour`, `#pause`, `#réalité`, `#métaphore`, `#mental`, `#philosophie`, `#analyse`, `#digitaldetox`, `#écriture`, `#authenticité`, `#création`, `#n8n`, `#aiagents`, `#mindset`, `#organisation`, `#entrepreneuriat`, `#developerbranding`, `#mcp`, `#promptengineering`, `#brainstorming`, `#voix`, `#codex`, `#notion`, `#chatgpt`, `#github`, `#créativité`, `#hack`. |

## Common Operations

### Fetch metadata
```bash
/notionMCP/fetch {"id":"https://www.notion.so/2a12c6b40808805fb9f8c7729299afb8"}
```
Returns the schema, data sources, and available views.

### List current entries
Use a single-space query to return all rows.
```bash
/notionMCP/search {"query":" ","data_source_url":"collection://2a12c6b4-0808-8022-9b1d-000b3c2cfbfb"}
```

### Create a new row
When setting multi-select values (`Type`, `Tags`), pass them as JSON strings.
```bash
/notionMCP/create-pages {
  "parent": {"data_source_id":"2a12c6b4-0808-8022-9b1d-000b3c2cfbfb"},
  "pages": [{
    "properties": {
      "Titre provisoire": "Example subject",
      "Description / Angle": "What we will cover",
      "Priority": "Medium",
      "Type": "[\"Short\"]",
      "Tags": "[\"Activation\"]"
    },
    "content": "## Summary\nTwo lines that capture the idea.\n\n## Notes\n- Key takeaway.\n- Links or reminders."
  }]
}
```

### Update draft content
Use `notion-update-page` to edit the `Brouillon` field on an existing row.
```bash
/notionMCP/update-page {
  "page_id": "<page-id>",
  "command": "update_properties",
  "properties": {
    "Brouillon": "Paragraphs of draft text go here."
  }
}
```

### Remove entries from the database
There is no direct delete command. Move the page out of the data source instead:
```bash
/notionMCP/move-pages {
  "page_or_database_ids": ["<page-id-to-remove>"],
  "new_parent": {"type":"workspace"}
}
```
This archives the row from the database while keeping the page accessible in the workspace trash.

## Tips
- Run `notion-search` with a more specific `query` string to find individual subjects quickly.
- Capture page IDs from search results (they follow the `2a12...` pattern) for updates or moves.
- Keep the database empty between sessions unless a subject is actively being tracked, to avoid mixing work-in-progress ideas.
