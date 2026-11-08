# Claude API

"Build, debug, and optimize Claude API / Anthropic SDK apps. Apps built with this skill should include prompt caching. Also handles migrating existing Claude API code between Claude model versions (4.5 → 4.6, 4.6 → 4.7, retired-model replacements). TRIGGER when: code imports `anthropic`/`@anthropic-ai/sdk`; user asks for the Claude API, Anthropic SDK, or Managed Agents; user adds/modifies/tunes a Claude feature (caching, thinking, compaction, tool use, batch, files, citations, memory) or model (Opus/Sonnet/Haiku) in a file; questions about prompt caching / cache hit rate in an Anthropic SDK project. SKIP: file imports `openai`/other-provider SDK, filename like `*-openai.py`/`*-generic.py`, provider-neutral code, general programming/ML."

## Overview

This repository preserves the complete AITMPL Claude API skill and its published language-specific examples, SDK guidance, streaming, tool-use, batch, file API, managed-agent, migration, caching, and shared reference documentation.

## Installation

Clone into the Claude Code personal skills directory:

```bash
git clone https://github.com/Brajesh31/claude-claude-api-skill.git ~/.claude/skills/claude-api
```

On Windows, use `%USERPROFILE%\.claude\skills\claude-api` as the destination.

## Usage

Claude Code can load the skill when a request concerns Anthropic's Claude API or related SDK workflows. Invoke it directly with `/claude-api`.

## Repository structure

```text
claude-api/
├── SKILL.md
├── LICENSE.txt
├── csharp/claude-api.md
├── curl/examples.md
├── curl/managed-agents.md
├── go/claude-api.md
├── go/managed-agents/README.md
├── java/claude-api.md
├── java/managed-agents/README.md
├── php/claude-api.md
├── php/managed-agents/README.md
├── python/agent-sdk/README.md
├── python/agent-sdk/patterns.md
├── python/claude-api/README.md
├── python/claude-api/batches.md
├── python/claude-api/files-api.md
├── python/claude-api/streaming.md
├── python/claude-api/tool-use.md
├── python/managed-agents/README.md
├── ruby/claude-api.md
├── ruby/managed-agents/README.md
├── shared/agent-design.md
├── shared/error-codes.md
├── shared/live-sources.md
├── shared/managed-agents-api-reference.md
├── shared/managed-agents-client-patterns.md
├── shared/managed-agents-core.md
├── shared/managed-agents-environments.md
├── shared/managed-agents-events.md
├── shared/managed-agents-memory.md
├── shared/managed-agents-multiagent.md
├── shared/managed-agents-onboarding.md
├── shared/managed-agents-outcomes.md
├── shared/managed-agents-overview.md
├── shared/managed-agents-tools.md
├── shared/managed-agents-webhooks.md
├── shared/model-migration.md
├── shared/models.md
├── shared/prompt-caching.md
├── shared/tool-use-concepts.md
├── typescript/agent-sdk/README.md
├── typescript/agent-sdk/patterns.md
├── typescript/claude-api/README.md
├── typescript/claude-api/batches.md
├── typescript/claude-api/files-api.md
├── typescript/claude-api/streaming.md
├── typescript/claude-api/tool-use.md
├── typescript/managed-agents/README.md
├── README.md
└── LICENSE
```

## Languages and topics

- Python and TypeScript SDK guides, streaming, tool use, batches, files, and Agent SDK patterns.
- Go, Java, Ruby, PHP, C#, and cURL API examples.
- Shared references for model migration, prompt caching, tool use, agent design, errors, and Managed Agents.

## Dependencies

No package installation is required to load the skill. Install the official Anthropic SDK for the language you use, following the corresponding language guide. API access requires an Anthropic API key and appropriate account access. Keep credentials outside source control.

## Validation

The repository import preserves source documentation and examples. Code samples have not been executed or tested as part of this import.
