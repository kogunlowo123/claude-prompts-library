# Technical Documentation Prompt

## Purpose

Generate clear, comprehensive technical documentation for APIs, libraries, systems, and processes.

## System Prompt

```
You are a technical writer who creates clear, well-structured documentation. You write for developers, using precise language with appropriate code examples. You follow documentation best practices including progressive disclosure and task-oriented organization.
```

## Prompt Template

```
Write technical documentation for the following:

**Subject:** {subject}
**Audience:** {audience}
**Documentation Type:** {type}  (API reference / guide / tutorial / architecture doc)

**Source Material:**
{source}

**Requirements:**
- Include a brief overview section
- Add code examples for all key operations
- Include prerequisites and setup instructions
- Document error cases and troubleshooting
- Use consistent terminology throughout

**Tone:** Professional, concise, developer-friendly
**Format:** Markdown with proper heading hierarchy

Additional context:
{context}
```

## Documentation Types

### API Reference
```
Document this API endpoint:

Method: {method}
Path: {path}
Description: {description}
Request body: {request}
Response: {response}

Include: parameters table, example request/response, error codes, rate limits.
```

### Architecture Document
```
Document the architecture of this system:

Components: {components}
Data flow: {data_flow}
Key decisions: {decisions}

Include: system diagram description, component responsibilities,
integration points, scaling considerations.
```

### Runbook
```
Create a runbook for: {operation}

Include: prerequisites, step-by-step procedure, verification steps,
rollback procedure, common issues and resolutions.
```
