### 4. Agent2Agent Protocol (A2A)

The A2A protocol is an open standard for agent communication originally launched by Google and now managed by the Linux Foundation.

It uses a client-server architecture.

The workflow includes three stages:

1. Discovery

A user or agent sends a request to a client agent.  
The client agent identifies remote agents capable of completing the task.

2. Authentication

The selected remote agent verifies authorization and grants permissions.

3. Communication

The client agent sends the task request and the remote agent processes it.

Communication occurs over HTTPS with JSON-RPC 2.0 for structured data exchange.

---

### 5. Model Context Protocol (MCP)

The Model Context Protocol, introduced by Anthropic, provides a standardized way for AI models to access external context.

MCP enables agents to connect with:

- APIs
- databases
- files
- search tools
- external services

The MCP architecture includes three components.

MCP Host  
Contains orchestration logic and connects clients to servers.

MCP Client  
Converts user requests into structured protocol messages and manages sessions.

MCP Server  
Provides tools and services such as APIs or databases.

Communication between clients and servers occurs through JSON-RPC using either:

- standard input/output (stdio)
- HTTP transport

---

### 6. Agent Payments Protocol (AP2)

The Agent Payments Protocol enables AI agents to perform secure financial transactions on behalf of users.

Introduced by Google in 2025, AP2 enables cross-platform agent-driven payments.

Instead of users manually clicking purchase buttons, agents can execute transactions automatically.

AP2 uses digitally signed instructions called **mandates**.

Two types of mandates exist.

Intent Mandate  
Captures the user's request and intent.

Cart Mandate  
Finalizes the transaction with a secure record of items, price, and terms.

This ensures transparency and security during agent-driven purchases.

---

## Example Workflow Using A2A, MCP, and AP2

Consider the request:

"Order noise-cancelling wireless headphones under $250."

Step 1 — A2A communication  
The shopping agent communicates with retailer and payment agents.

Step 2 — MCP context retrieval  
The agent gathers product data, user preferences, and past purchase history.

Step 3 — AP2 payment execution  
The agent generates a Cart Mandate and completes the transaction securely.

---

## Criteria for Choosing an Agent Protocol

Organizations evaluating agent protocols typically consider:

Efficiency  
Protocols should minimize latency and enable fast responses.

Reliability  
Protocols must handle network disruptions and support long-running tasks.

Scalability  
Protocols should support large ecosystems with many agents and services.

Security  
Strong authentication, encryption, and access control are essential.
