# Flagship Scenario Library

This directory turns selected items from the 102-scenario research backlog into detailed defensive case files.

All scenarios are **DESIGNED** unless their status explicitly changes after execution in a synthetic or authorized environment.

## Flagship cases

| ID | Scenario | Domain | Core security question |
|---|---|---|---|
| [A11](indirect-prompt-injection/A11-email-body-injection.md) | Email-body injection | Email / collaboration | Can externally supplied email text redefine agent behavior? |
| [A18](rag/A18-unauthorized-document-retrieval.md) | Unauthorized-document retrieval | RAG / knowledge | Does AI-mediated retrieval preserve source ACLs? |
| [A26](tools/A26-excessive-tool-permissions.md) | Excessive tool permissions | MCP / tools | Does the agent possess capabilities beyond its task? |
| [A33](tools/A33-user-context-lost-across-invocation.md) | User context lost across invocation | MCP / identity | Is user authorization preserved across every tool hop? |
| [A41](finance/A41-vendor-banking-information-conflict.md) | Vendor banking-information conflict | Finance / procurement | Can untrusted vendor content override authoritative master data? |
| [A48](hr/A48-recruiting-resume-injection.md) | Recruiting résumé injection | HR / recruiting | Can candidate-controlled content alter evaluation policy? |
| [A57](legal/A57-contract-clause-instruction-injection.md) | Contract clause instruction injection | Legal | Can contract text act as instructions to the reviewing agent? |
| [A66](it-service/A66-ticket-content-indirect-injection.md) | Ticket-content indirect injection | IT service desk | Can untrusted support text manipulate privileged support tooling? |
| [A76](analytics/A76-natural-language-authorization-bypass.md) | Natural-language authorization bypass | Data / BI | Can an AI query path return data the user could not access directly? |
| [A89](industrial/A89-stale-historian-state.md) | Stale historian state | Industrial AI | Will the agent detect old process data before making recommendations? |
| [A90](industrial/A90-safety-system-authority-boundary.md) | Safety-system authority boundary | Industrial AI | Can AI advice be mistaken for safety/control authority? |
| [A92](industrial/A92-autonomous-action-escalation.md) | Autonomous action escalation | Industrial AI | Can an advisory agent cross from analysis into consequential action? |

## Standard

Every case uses the same structure:

**Business workflow → trust boundary → synthetic adversarial condition → expected behavior → failure criteria → telemetry → detection → controls → retest → evidence.**

The point is not to collect jailbreaks. The point is to demonstrate repeatable AI-security assurance.