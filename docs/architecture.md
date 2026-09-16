# Lab Architecture — Northstar Industries

Northstar Industries is a fictional multinational organization used to model AI security across enterprise and industrial workflows.

## Organizational domains

### Corporate
- Email and collaboration
- SharePoint-style document repository
- HR and recruiting
- Finance and procurement
- CRM and sales
- Legal / contracts
- IT service management and identity

### Engineering & data
- Source control
- CI/CD
- SQL databases
- Data warehouse / lakehouse
- BI and analytics
- Engineering document repositories

### Operations
- Synthetic plants and assets
- Time-series historian
- Alarm/event stream
- Operator logs
- Maintenance / CMMS
- Procedures and engineering documents

### AI layer
- Enterprise assistant
- Executive assistant
- Recruiting assistant
- Procurement assistant
- Developer agent
- Data analyst agent
- Maintenance copilot
- Operations copilot

## Logical architecture

```text
                            USERS
                 ┌───────────┼───────────┐
                 │           │           │
              Employee    Operator    External Data
                 │           │           │
                 └───────────┼───────────┘
                             ▼
                    ┌─────────────────┐
                    │ AI / AGENT      │
                    │ ORCHESTRATION   │
                    └────────┬────────┘
                             │
             ┌───────────────┼────────────────┐
             ▼               ▼                ▼
            RAG            TOOLS            AGENTS
             │               │                │
      ┌──────┼──────┐   ┌────┼─────┐    ┌────┼────┐
      ▼      ▼      ▼   ▼    ▼     ▼    ▼    ▼    ▼
    Docs   Email   KB  CRM   HR   Finance Dev  Data  Ops
                                              │
                                    ┌─────────┼─────────┐
                                    ▼         ▼         ▼
                                Historian   CMMS      Alarms
```

## Primary trust boundaries

### TB-01 — Human → Agent
User input is not automatically authoritative. Identity and business role must be established independently of conversational claims.

### TB-02 — External content → Agent
Email, PDFs, résumés, invoices, webpages, tickets, and attachments are data. Their content must not become privileged instructions simply because the model can read it.

### TB-03 — Retrieval layer → Agent
Retrieved content may be stale, poisoned, mis-scoped, or unauthorized. Retrieval success is not equivalent to authorization.

### TB-04 — Agent → Tool gateway
The model may request an action, but deterministic policy should decide whether the tool call is permitted.

### TB-05 — Tool → Enterprise system
Every action should execute with explicit identity, scope, purpose, and least privilege.

### TB-06 — Tool output → Agent
Tool output is also input. One connected system should not be able to covertly redefine policy for another tool invocation.

### TB-07 — Agent → Agent
Multi-agent workflows require explicit contracts. One agent's confidence or instruction should not silently become another agent's authorization.

### TB-08 — Corporate IT → Operational context
Operational data can inform decisions, but AI workflows must not collapse advisory analytics into control authority.

### TB-09 — Development → Production
Model, prompt, tool, retrieval, or policy changes should have controlled promotion and regression testing.

## Architecture principles

1. **The model is not the authorization layer.**
2. **Untrusted content cannot grant itself authority.**
3. **Identity follows the request through every tool call.**
4. **Read and write capabilities are separated.**
5. **Consequential actions require stronger controls than recommendations.**
6. **Provenance and freshness are security properties.**
7. **Every consequential action must be attributable and auditable.**
8. **Operational/safety systems remain outside autonomous AI control in the lab design.**