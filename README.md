<img src="assets/banner.svg" alt="Diogo Stein. I build LLM agents for business software." width="100%">

<p align="center">
  <a href="https://www.linkedin.com/in/diogo-stein-ab83b122b/"><b>LinkedIn</b></a>
  &nbsp;·&nbsp;
  <a href="#how-i-put-an-llm-inside-a-product"><b>How I build</b></a>
  &nbsp;·&nbsp;
  <a href="#selected-work"><b>Selected work</b></a>
</p>

Hey, I'm Diogo, Head of Tech at **LVX Digital** in Brazil. I design business software and decide where a language model actually helps. The model reads the conversation and proposes; the software checks the rules and decides; a person steps in when it matters.

- 🛠️ Building **Kontar**, a CRM with AI agents that act through scoped tools
- 🧪 Writing a lesson on testing agent tools: rules in tests, model choices in evals
- 🤖 Shipping code with coding agents, one ticket per branch, reviewed before merge

## Selected work

<a href="./work/kontar.md"><img src="assets/card-kontar.svg" alt="Kontar: a commercial CRM where the model proposes changes and the backend decides what is allowed." width="100%"></a>

<a href="./work/polaris.md"><img src="assets/card-polaris.svg" alt="Polaris: internal platform for client operations, projects, communication and finance." width="49%"></a>&nbsp;<a href="./work/lvx-central.md"><img src="assets/card-lvx-central.svg" alt="LVX Central: archived local desktop app for daily operations and coding agent workflows." width="49%"></a>

> 🔒 These are private systems. The overviews explain the engineering decisions; source code and client data stay private.

## How I put an LLM inside a product

```mermaid
flowchart LR
    U(["Customer message"]) --> M["Model reads the conversation"]
    M -->|"proposes a tool call"| B{"Backend checks record,<br/>organization and allowed values"}
    B -->|"valid"| W["Write + audit log"]
    B -->|"out of scope"| R["Refuse"]
    M -->|"asks for a human"| H["Pause the AI,<br/>route to the team"]
```

1. **Scope the action.** The model gets a small set of named tools, never the database.
2. **Validate in the backend.** Every proposal is checked against the record, the organization and the allowed values before anything is written. Repeated calls don't repeat the effect.
3. **Hand off to a person.** A separate path pauses the AI and gives the conversation to the team.
4. **Verify the behavior.** Tests prove the rules. Evals measure the model's choices. I keep the two apart.

## Toolbox

**AI** &nbsp;`OpenAI API` `tool calling` `agents` `evals` `Claude Code` `Codex`<br>
**Backend** &nbsp;`TypeScript` `Node.js` `NestJS` `PostgreSQL` `Prisma` `Redis` `BullMQ`<br>
**Frontend** &nbsp;`React` `Next.js` `Vite` `Tailwind CSS`<br>
**Delivery** &nbsp;`Docker` `Linux` `GitHub` `Vercel` `Firebase`

<sub>Before tech, I worked in marketing and operations. That's why I start with the process and the people, and only then decide what to build.</sub>
