# claude-claude-api-skill

A practical Claude Code skill for building, integrating, debugging, and maintaining applications that use the Claude API and Anthropic SDKs.

## Overview

This repository provides a structured set of instructions and language-specific technical guides for implementing Claude-powered application features. It helps developers choose an appropriate API surface, follow the SDK conventions for their language, and build reliable integrations.

The skill is intended for work involving API requests, streaming responses, tool use, prompt caching, batch processing, file workflows, agent-based applications, and model migrations.

## What This Skill Helps With

- Selecting the right API approach for a feature or application.
- Implementing Claude API integrations with supported language SDKs.
- Building request and response flows, including streaming.
- Defining tools and handling tool execution safely.
- Improving repeated-request efficiency with prompt caching.
- Working with batch processing and file-related API features.
- Designing agent workflows and managing persistent agent state.
- Understanding model capabilities and planning model migrations.
- Diagnosing common API errors and integration problems.

## Supported Languages

The repository includes guidance for:

- Python
- TypeScript and JavaScript
- Go
- Java
- Ruby
- PHP
- C#
- cURL and raw HTTP

The level of SDK and feature support can vary by language. Check the relevant language guide before implementing a feature.

## Installation

Clone the repository into your Claude Code skills directory:

```bash
git clone https://github.com/Brajesh31/claude-claude-api-skill.git ~/.claude/skills/claude-api
```

On Windows, use:

```powershell
git clone https://github.com/Brajesh31/claude-claude-api-skill.git "$env:USERPROFILE\.claude\skills\claude-api"
```

If your environment uses a different skills directory, place the repository there and keep its folder name consistent with your skill configuration.

## Usage

1. Open a project that uses the Claude API or an Anthropic SDK.
2. Describe the feature, bug, migration, or integration you need help with.
3. Let the skill identify the project language and the relevant documentation.
4. Review the proposed implementation and confirm that it matches the installed SDK version.
5. Run the project's tests and validate API behavior with a safe development credential.

You can also invoke the skill directly:

```text
/claude-api
```

## Documentation Map

| Directory | Purpose |
|---|---|
| `python/` | Python SDK, streaming, batches, files, tool use, and agent workflows |
| `typescript/` | TypeScript SDK, streaming, batches, files, tool use, and agent workflows |
| `go/` | Go API and agent implementation guidance |
| `java/` | Java API and agent implementation guidance |
| `ruby/` | Ruby API and agent implementation guidance |
| `php/` | PHP API and agent implementation guidance |
| `csharp/` | C# API guidance |
| `curl/` | HTTP examples and request patterns |
| `shared/` | Cross-language concepts, model guidance, caching, errors, and agent design |

Start with `SKILL.md` for the main workflow. Then open only the language and topic documents relevant to the task.

## Recommended Workflow

### 1. Confirm the integration target

Identify the language, framework, installed SDK version, and the files that need to change. Do not mix provider-specific SDKs in a file that is intended to remain provider-neutral.

### 2. Select the API surface

Use a straightforward request for single-turn tasks. Add tool use when the application needs controlled external actions. Use an agent-oriented workflow only when the task genuinely requires multi-step execution or persistent state.

### 3. Implement from the matching guide

Use the examples for the project's language. Do not assume that method names or parameter shapes are identical across SDKs.

### 4. Handle operational concerns

Consider timeouts, retries, rate limits, streaming cancellation, error handling, observability, and safe credential management.

### 5. Validate the result

Run unit and integration tests where available. Check request payloads, response parsing, tool boundaries, and failure behavior before deploying.

## Security and Reliability

- Store API keys in environment variables or a secrets manager.
- Never commit credentials, tokens, or private request data.
- Validate tool inputs before executing external actions.
- Apply timeouts and bounded retry policies.
- Avoid logging sensitive prompts or user data.
- Treat model output as untrusted input when it reaches a database, shell, browser, or external service.
- Verify current API behavior against the SDK version installed in the project.

## Repository Layout

The root `SKILL.md` contains the skill instructions. Language-specific folders contain focused implementation guides and examples. The `shared/` directory contains concepts that apply across multiple languages.

## Contribution and Maintenance

Keep examples focused, runnable where practical, and aligned with the SDK version they describe. When changing an API workflow, update the relevant language guide and shared explanation together so that the documentation remains consistent.
