# Task 2: Putting the Agency in "Agentic"

**Learning Path:** TryHackMe Agentic AI Security  
**Topic:** Agentic AI Architecture and Core Capabilities  
**Type:** Technical Study Notes and Security Analysis  
**Status:** Study Notes Prepared

## 1. Learning Objectives

- Explain what makes an AI system agentic.
- Differentiate a traditional LLM, a predefined workflow, and an autonomous agent.
- Identify the three core agentic capabilities.
- Analyze security risks associated with autonomous decisions and tool execution.
- Apply these concepts to a security operations scenario.

## 2. What Makes AI Agentic?

An agentic AI system can perceive information, reason about goals, decide what to do, and take actions with a degree of autonomy.

The core loop is:

**PERCEIVE → REASON → DECIDE → ACT → REPEAT**

An agent can use the results of an action to inform its next decision.

## 3. Traditional LLM vs Workflow vs Agent

| Feature | Traditional LLM | Predefined Workflow | Agentic AI |
|---|---|---|---|
| Generates text | Yes | Yes | Yes |
| Uses external tools | Not necessarily | May | May |
| Selects next action autonomously | Limited | Usually predetermined | Yes |
| Executes multi-step tasks | Limited | According to predefined routes | Can plan and adapt |
| Security concern | Unsafe output | Workflow and integration weaknesses | Autonomous actions and delegated authority |

The key difference is not necessarily the underlying model. It is the architecture and the authority delegated to the system.

## 4. Three Core Agentic Capabilities

### A. Planning & Reasoning

Planning and reasoning determine what needs to happen and in which order to accomplish a goal.

**Example:** A security agent decides to investigate an unusual login by examining authentication logs, checking IP reputation, and correlating related alerts.

**Security risks:**
- Manipulated goals or plans
- Untrusted instructions influencing decisions
- Unsafe action sequences

**Defenses:**
- Enforce task boundaries
- Validate tool permissions independently
- Require approval for sensitive actions

### B. Memory & Statefulness

Memory and statefulness allow an agent to retain relevant context from earlier steps or interactions.

Memory may include conversation history, intermediate findings, and persistent external storage.

**Example:** A SOC assistant remembers the suspicious IP address, affected account, and earlier investigation results.

**Security risks:**
- Memory poisoning
- Retention of sensitive information
- Untrusted stored content influencing future actions

**Defenses:**
- Restrict memory access
- Validate retrieved information
- Apply retention and data protection policies

### C. Action & Tool Use

Action and tool use allow an agent to interact with external systems rather than only generate text.

Examples include calling APIs, querying databases, creating tickets, and using security tools.

**Example:** A SOC agent queries a SIEM and creates an incident ticket.

**Security risks:**
- Unauthorized tool execution
- Excessive permissions
- Data exfiltration
- Unapproved changes to production systems

**Defenses:**
- Apply least privilege
- Use tool allowlists
- Enforce authorization outside the model
- Log tool calls and results
- Require human approval for high-impact actions

## 5. Security Operations Use Case

**Scenario:** An AI security assistant investigates suspicious account activity.

1. **Perceive:** Receive an authentication alert.
2. **Reason:** Evaluate the event and identify missing evidence.
3. **Decide:** Select appropriate investigation steps.
4. **Act:** Query authorized security tools.
5. **Remember:** Retain investigation context.
6. **Repeat:** Reassess findings and determine the next authorized step.

**Security recommendation:** Investigation tools should operate with read-only permissions by default. Account disabling, blocking, or other disruptive actions should require appropriate authorization.

## 6. TryHackMe Knowledge Check

**Q1: Which capability retains context from previous interactions?**  
Answer: Memory & Statefulness

**Q2: Which capability determines the order of required steps?**  
Answer: Planning & Reasoning

**Q3: Which capability performs actions in the real world?**  
Answer: Action & Tool Use

## 7. Key Takeaways

- Autonomy is a defining characteristic of agentic AI.
- Agentic systems can dynamically select tools and actions.
- Memory helps preserve context across steps.
- Planning determines the sequence of actions.
- Tool use connects model decisions to external systems.
- Security controls must enforce boundaries independently of the model.

## 8. Portfolio Reflection

This lesson strengthened my understanding of how AI agents differ from traditional language models and predefined workflows. From a cybersecurity perspective, the most important distinction is the ability to turn model decisions into actions affecting external systems.

I identified least privilege, tool authorization, memory protection, and human approval as important controls for reducing agentic AI risks.

## References

- [TryHackMe Agentic AI Security Path](https://tryhackme.com/path/outline/agentic-ai-security)
- [OWASP GenAI Security Project](https://genai.owasp.org/)

---

*Independent study notes and security analysis based on TryHackMe learning material. No practical lab completion is claimed in this document.*
