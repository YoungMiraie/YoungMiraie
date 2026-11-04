# LVX Central — local operations and engineering

[Back to profile](../README.md)

LVX Central started from a practical problem in my own work: keeping daily operations, project context, engineering tasks and agent workflows connected. It is a local Windows application built around that need.

**Stage: implemented locally; connections and real operational workflows are still being validated.**

## My work

I am developing a local workspace for the technology operation: connecting the operational knowledge base to engineering work, keeping plans and review visible, and making it easier to understand the state of each project.

## Engineering focus

- Electron and React interface with TypeScript.
- Local SQLite persistence and a Markdown knowledge base.
- Agent workflows with a plan, bounded scope, verification and review.
- Codex App Server and Claude Agent SDK adapters.
- Read integrations for engineering and system health.
- Clear handling of missing or stale monitoring data.

## Technical foundation

Electron, React, TypeScript, SQLite, Node.js, Codex App Server and Claude Agent SDK.

## Project context

Internal application for local Windows use. It has no public demo or hosted service. Implemented adapters do not establish that every provider is connected: Claude authentication, private metrics and the first real engineering workflow still need validation. Local implementation and local tests are distinct from operational acceptance.
