# Repository Management for CV Generation

This file documents all your public repositories with metadata to control what appears in your CV/README.md.
`README.md` should only surface factual, evidence-based claims and explicit limits.

## Configuration

For each repository, you can configure:
- `include_in_cv`: Whether to include this repo in the CV (true/false)
- `priority`: Display priority (1=highest, 10=lowest)
- `custom_description`: Override the default description
- `highlights`: Key achievements/features to highlight
- `tags`: Technology tags for categorization

Selection rule used by `README.md`:
- Include repos where `include_in_cv: true`
- Order by `priority` ascending for featured projects
- Keep summaries grounded in implementation evidence from each repository

## Repositories (sorted by stars, then by interest)

### ⭐ cursor-openrouter-proxy (7 stars)
- **Repository**: https://github.com/pezzos/cursor-openrouter-proxy
- **Language**: Go
- **Description**: This project sets up a Docker Compose configuration for the Cursor Deepseek API Proxy
- **Created**: 2025-01-27
- **Last Updated**: 2025-06-16
- **include_in_cv**: true
- **priority**: 1
- **custom_description**: OpenAI-compatible proxy that lets Cursor use OpenRouter models with runtime switching.
- **highlights**:
  - Problem solved: Cursor expects OpenAI-style APIs, which blocks direct use of many OpenRouter models.
  - Implementation proof: `proxy.go` implements `/v1/chat/completions`, `/v1/models`, and model switch endpoints (`/v1/config`, `/switch-model`) with Docker and Traefik deployment files.
  - Limitation/risk: Requires Cursor Pro plus an OpenRouter API key, and is dependent on upstream provider availability and pricing.
- **tags**: Go, Docker, AI, Proxy, HTTP/2, LLM, DevTools

### ⭐ Whisper-to-Notion (2 stars)
- **Repository**: https://github.com/pezzos/Whisper-to-Notion
- **Language**: Python
- **Description**: Use quick ways to add your ideas on-the-go to Notion leveraging the power of Whisper, GPT and Siri/Shortcuts
- **Created**: 2024-01-03
- **Last Updated**: 2025-02-07
- **include_in_cv**: true
- **priority**: 3
- **custom_description**: Voice-capture workflow that turns spoken ideas into structured Notion entries with Whisper, GPT, and Siri Shortcuts.
- **highlights**:
  - Problem solved: Capturing ideas on mobile and manually rewriting them into Notion creates friction.
  - Implementation proof: proof pending / non verifie localement (implementation references not verified in this inventory pass).
  - Limitation/risk: Depends on iOS Shortcuts and external AI/API services; transcription quality depends on audio quality and prompts.
- **tags**: Python, AI, Whisper, GPT, Notion, iOS, Automation

### ⭐ jsonl_dataset_generator (1 star)
- **Repository**: https://github.com/pezzos/jsonl_dataset_generator
- **Language**: JavaScript
- **Description**: Generate rich JSONL datasets from topics to fine-tune Large Language Models. This tool transforms topics into diverse Q&A pairs by leveraging multiple AI providers to ensure variety and quality in training data.
- **Created**: 2025-02-08
- **Last Updated**: 2025-06-06
- **include_in_cv**: true
- **priority**: 4
- **custom_description**: Multi-provider JSONL dataset generator for LLM fine-tuning workflows.
- **highlights**:
  - Problem solved: Manual dataset authoring for fine-tuning is slow and hard to scale consistently.
  - Implementation proof: proof pending / non verifie localement (implementation references not verified in this inventory pass).
  - Limitation/risk: Generated samples still need human review for quality, factuality, and licensing before model training.
- **tags**: JavaScript, AI, Machine Learning, Dataset, LLM, Fine-tuning

### PezzosCode
- **Repository**: https://github.com/pezzos/PezzosCode
- **Language**: Mixed (Markdown + Python)
- **Description**: Docs-first bootstrap kit for AI-assisted software delivery.
- **Created**: 2026-01-19
- **Last Updated**: 2026-03-02
- **include_in_cv**: true
- **priority**: 5
- **custom_description**: Docs-first bootstrap toolkit that standardizes AI-assisted repo delivery with deterministic scripts and process contracts.
- **highlights**:
  - Problem solved: AI-assisted solo projects drift when context, process, and execution tooling are not standardized.
  - Implementation proof: Includes `tools/bootstrap-into`, `make prepare-features`, `make review-features`, and explicit workflow docs under `docs/04-process/`.
  - Limitation/risk: Process rigor adds setup overhead and can be heavy for very small throwaway projects.
- **tags**: Python, Markdown, Developer Tooling, Documentation, AI Workflow

### ⭐ plex-pi (1 star)
- **Repository**: https://github.com/pezzos/plex-pi
- **Language**: Groovy
- **Description**: The full setup of Plex Media Server on a Raspberry Pi with scripts like S3 backup
- **Created**: 2021-11-02
- **Last Updated**: 2025-03-12
- **include_in_cv**: false
- **priority**: 4
- **custom_description**: Complete Raspberry Pi Plex Media Server setup with automated backups and system optimization
- **highlights**:
  - Automated installation scripts
  - S3 backup integration
  - Hardware optimization (SSD boot, fan control)
  - System maintenance automation
- **tags**: Raspberry Pi, Plex, DevOps, Automation, Docker, Media Server

### remote-mcp-proxy (0 stars)
- **Repository**: https://github.com/pezzos/remote-mcp-proxy
- **Language**: Go
- **Description**:
- **Created**: 2025-06-20
- **Last Updated**: 2025-06-30
- **include_in_cv**: true
- **priority**: 2
- **custom_description**: Dockerized Go proxy that exposes local MCP servers as Remote MCP endpoints for MCP-compatible clients.
- **highlights**:
  - Problem solved: MCP servers that only run locally are not reachable by remote MCP clients without a bridge.
  - Implementation proof: `main.go` and `proxy/server.go` expose `/sse`, `/sessions/{sessionId}`, `/health`, and `/listmcp`; `config.example.json` documents proxy/server mappings for client setup.
  - Limitation/risk: Production setup needs wildcard DNS/TLS (Traefik path), and proxy-managed MCP processes increase operational/security surface.
- **tags**: Go, Proxy, MCP

### claude-task-master (0 stars)
- **Repository**: https://github.com/pezzos/claude-task-master
- **Language**: JavaScript
- **Description**: It's a fork of an AI-powered task-management system you can drop into Cursor, Lovable, Windsurf, Roo, and others.
- **Created**: 2025-06-06
- **Last Updated**: 2025-06-10
- **include_in_cv**: false
- **priority**: 5
- **custom_description**: AI-powered task management system for modern development environments
- **highlights**:
  - Multi-IDE compatibility
  - AI-driven task optimization
  - Drop-in integration
- **tags**: JavaScript, AI, Task Management, IDE, Productivity

### ruby (0 stars)
- **Repository**: https://github.com/pezzos/ruby
- **Language**: Shell
- **Description**: This project provides a containerized Ruby development environment that seamlessly integrates with your local machine while maintaining isolation and consistency.
- **Created**: 2025-01-17
- **Last Updated**: 2025-06-11
- **include_in_cv**: false
- **priority**: 9
- **custom_description**: Containerized Ruby development environment
- **highlights**: []
- **tags**: Ruby, Docker, Development Environment

### cursor-proxy (0 stars)
- **Repository**: https://github.com/pezzos/cursor-proxy
- **Language**: Go
- **Description**: A high-performance HTTP/2-enabled proxy server designed specifically to enable Cursor IDE's Composer to use DeepSeek's and OpenRouter's language models. This proxy translates OpenAI-compatible API requests to DeepSeek/OpenRouter API format, allowing Cursor's Composer and other OpenAI API-compatible tools to seamlessly work with these models.
- **Created**: 2025-01-28
- **Last Updated**: 2025-02-17
- **include_in_cv**: false
- **priority**: 7
- **custom_description**: HTTP/2 proxy for Cursor IDE to use DeepSeek/OpenRouter models (superseded by cursor-openrouter-proxy)
- **highlights**: []
- **tags**: Go, Proxy, AI, HTTP/2

### raycast-script-commands (0 stars)
- **Repository**: https://github.com/pezzos/raycast-script-commands
- **Language**: Shell
- **Description**: Script Commands let you tailor Raycast to your needs. Think of them as little productivity boosts throughout your day.
- **Created**: 2025-01-28
- **Last Updated**: 2025-03-12
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Custom Raycast script commands for productivity
- **highlights**: []
- **tags**: Shell, Raycast, Productivity, macOS

### raycast-ai-assistant (0 stars)
- **Repository**: https://github.com/pezzos/raycast-ai-assistant
- **Language**: TypeScript
- **Description**: A collection of AI-powered tools to enhance your productivity.
- **Created**: 2025-01-31
- **Last Updated**: 2025-02-14
- **include_in_cv**: true
- **priority**: 6
- **custom_description**: Raycast extension suite for dictation, AI prompting, and local/online speech workflows.
- **highlights**:
  - Problem solved: Writing, rewriting, and dictating text across apps causes repetitive context switching.
  - Implementation proof: `extensions/ai-assistant` ships commands for Dictate Text, Dictate AI Prompt, settings, dictionary/history, and local model management (Whisper/Parakeet).
  - Limitation/risk: macOS + Raycast dependency, microphone permissions, and optional OpenAI key requirements for cloud modes.
- **tags**: TypeScript, AI, Raycast, Productivity, macOS

### wpzo-hosting (0 stars)
- **Repository**: https://github.com/pezzos/wpzo-hosting
- **Language**: Shell
- **Description**:
- **Created**: 2021-08-16
- **Last Updated**: 2025-07-01
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Hosting automation scripts
- **highlights**: []
- **tags**: Shell, Hosting, Automation

### Claude-code-pwa (0 stars)
- **Repository**: https://github.com/pezzos/Claude-code-pwa
- **Language**: null
- **Description**:
- **Created**: 2025-06-24
- **Last Updated**: 2025-06-24
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: PWA experiment for AI coding workflows
- **highlights**: []
- **tags**: PWA, AI

### cursor-llm-switch (0 stars)
- **Repository**: https://github.com/pezzos/cursor-llm-switch
- **Language**: TypeScript
- **Description**:
- **Created**: 2025-02-04
- **Last Updated**: 2025-03-12
- **include_in_cv**: false
- **priority**: 9
- **custom_description**: LLM switching utility for Cursor
- **highlights**: []
- **tags**: TypeScript, Cursor, LLM

### raycast-extensions (0 stars)
- **Repository**: https://github.com/pezzos/raycast-extensions
- **Language**: TypeScript
- **Description**: Everything you need to extend Raycast.
- **Created**: 2025-02-01
- **Last Updated**: 2025-02-14
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Raycast extensions development
- **highlights**: []
- **tags**: TypeScript, Raycast, Extensions

### cursor-auto-rules-agile-workflow (0 stars)
- **Repository**: https://github.com/pezzos/cursor-auto-rules-agile-workflow
- **Language**: Shell
- **Description**:
- **Created**: 2025-02-21
- **Last Updated**: 2025-02-21
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Cursor auto-rules for agile workflow
- **highlights**: []
- **tags**: Shell, Cursor, Agile

### awesome-cursor-rules-mdc (0 stars)
- **Repository**: https://github.com/pezzos/awesome-cursor-rules-mdc
- **Language**: Python
- **Description**: Curated list of awesome Cursor Rules .mdc files
- **Created**: 2025-02-18
- **Last Updated**: 2025-02-18
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Curated Cursor Rules collection
- **highlights**: []
- **tags**: Python, Cursor, Documentation

### cursor-xml-rules-trial (0 stars)
- **Repository**: https://github.com/pezzos/cursor-xml-rules-trial
- **Language**: null
- **Description**:
- **Created**: 2025-02-21
- **Last Updated**: 2025-02-21
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Cursor XML rules trial
- **highlights**: []
- **tags**: XML, Cursor

### raycast-ai-assistant-service (0 stars)
- **Repository**: https://github.com/pezzos/raycast-ai-assistant-service
- **Language**: Python
- **Description**:
- **Created**: 2025-02-13
- **Last Updated**: 2025-02-14
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Backend service for Raycast AI assistant
- **highlights**: []
- **tags**: Python, Raycast, AI, Backend

### config-icon_converter (0 stars)
- **Repository**: https://github.com/pezzos/config-icon_converter
- **Language**: HTML
- **Description**:
- **Created**: 2025-02-08
- **Last Updated**: 2025-02-08
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Icon converter configuration tool
- **highlights**: []
- **tags**: HTML, Icons, Converter

### pezzos (0 stars)
- **Repository**: https://github.com/pezzos/pezzos
- **Language**: null
- **Description**: Some info about me 🤓
- **Created**: 2025-01-28
- **Last Updated**: 2025-01-28
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Personal profile repository
- **highlights**: []
- **tags**: Profile, About

### reenchanted (0 stars)
- **Repository**: https://github.com/pezzos/reenchanted
- **Language**: Swift
- **Description**: Enchanted is iOS and macOS app for chatting with private self hosted language models or publicly available ones.
- **Created**: 2025-01-28
- **Last Updated**: 2025-01-28
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: iOS/macOS app for self-hosted LLM chat
- **highlights**: []
- **tags**: Swift, iOS, macOS, LLM

### ollama-docker-traefik (0 stars)
- **Repository**: https://github.com/pezzos/ollama-docker-traefik
- **Language**: null
- **Description**: Access your Ollama everywhere from a simple Docker setup with Traefik
- **Created**: 2025-01-24
- **Last Updated**: 2025-03-16
- **include_in_cv**: false
- **priority**: 9
- **custom_description**: Ollama deployment with Docker and Traefik
- **highlights**: []
- **tags**: Docker, Traefik, Ollama, AI

### terraform-azure-metsys-demo1 (0 stars)
- **Repository**: https://github.com/pezzos/terraform-azure-metsys-demo1
- **Language**: HCL
- **Description**:
- **Created**: 2020-08-26
- **Last Updated**: 2020-08-27
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: Terraform Azure demo project
- **highlights**: []
- **tags**: Terraform, Azure, Infrastructure

### scripts (0 stars)
- **Repository**: https://github.com/pezzos/scripts
- **Language**: null
- **Description**:
- **Created**: 2020-05-24
- **Last Updated**: 2020-05-24
- **include_in_cv**: false
- **priority**: 10
- **custom_description**: General utility scripts
- **highlights**: []
- **tags**: Scripts, Utilities

---

## Instructions for Customization

1. **Review each repository** and update the configuration:
   - Set `include_in_cv: true` for repos you want in your CV
   - Adjust `priority` (1-10, 1 being highest priority)
   - Update `custom_description` to better reflect the project's value
   - Add relevant `highlights` to showcase key achievements
   - Verify and update `tags` for proper categorization

2. **After customization**, the workflow should:
   - Regenerate `README.md` from the curated metadata
   - Keep featured projects ordered by configured priority
   - Preserve bilingual clarity (`FR/EN`) and explicit credibility limits
   - Avoid fabricated statistics or absolute outcome guarantees

3. **Commit the changes** when you're satisfied with the configuration.
