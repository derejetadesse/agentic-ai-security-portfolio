# Agentic AI Security | Learning & Hands-On Portfolio

**Author:** Dereje Deressa  
**Focus:** Agentic AI Security, OWASP, Threat Modeling, SOC Operations, and Defensive Security Engineering  
**Learning Platform:** TryHackMe

## About This Project

This repository documents my ongoing journey studying Agentic AI Security through TryHackMe's Agentic AI Security Path. It includes my study notes, security concepts, threat analysis, and practical exercises as I complete them.

My objective is to understand how autonomous AI agents operate, identify security risks, and develop practical defensive techniques to secure agentic applications.

## Lesson 01: Introduction to Agentic AI Security

### What Is Agentic AI?

Agentic AI refers to AI systems capable of planning tasks, making decisions, interacting with tools and APIs, and executing actions toward a defined goal.

### Why Does Agentic AI Need Dedicated Security?

Traditional LLM applications primarily generate responses. Agentic systems may also interact with files, databases, APIs, and other services. A successful attack can therefore influence actions, not just generated text.

The OWASP Top 10 for Agentic Applications addresses security concerns arising from agent autonomy, tool access, delegated authority, and multi-step workflows.

### Key Security Risks

- Prompt injection through untrusted content
- Excessive agent permissions
- Unauthorized tool execution
- Sensitive information disclosure
- Manipulation of agent workflows
- Insufficient monitoring and audit logging

### Defensive Security Principles

- Enforce least-privilege permissions
- Validate and authorize tool calls outside the AI model
- Require human approval for sensitive operations
- Separate trusted instructions from untrusted content
- Monitor and log agent actions
- Restrict access to sensitive data and external services

## Learning Progress

| Task | Topic | Documentation | Status |
|---|---|---|---|
| 01 | Introduction to Agentic AI Security | README introduction | Study notes prepared |
| 02 | Putting the Agency in Agentic | [Task 2 Notes](notes/02-putting-the-agency-in-agentic.md) | Study notes prepared |
| 03 | ReAct and Agent Tools | [Task 3 Notes](notes/03-react-and-agent-tools.md) | Study notes prepared |
| 04 | Multi-Agent Systems | [Task 4 Notes](notes/04-multi-agent-systems.md) | Study notes prepared |
| 05 | Agent Communication: MCP and A2A | [Task 5 Notes](notes/05-agent-communication-mcp-a2a.md) | Study notes prepared |
| 06 | Least Agency | [Task 6 Notes](notes/06-least-agency.md) | Study notes prepared |
| Practical Labs | Hands-on security exercises | To be documented | Planned |

## Planned Portfolio Deliverables

- Structured study notes and diagrams
- Threat models and security risk assessments
- Hands-on lab documentation
- Python-based defensive security demonstrations
- Security findings and remediation recommendations

## References

- [TryHackMe Agentic AI Security Path](https://tryhackme.com/path/outline/agentic-ai-security)
- [OWASP GenAI Security Project](https://genai.owasp.org/)

---

*This is an independent educational portfolio based on my ongoing studies. Practical exercises and completed labs will be documented as they are performed.*
