# My Simple AI Plugin

An AI Agent & Skill plugin designed for developer workflow orchestration, project management, and full-stack software architecture. It delivers specialized multi-agent collaboration with a focus on modern **React**, **Angular**, and **NestJS** development patterns.

---

## Features

* **Multi-Agent Orchestration:** Specialized roles for planning, architecture design, development, research, and testing.
* **Domain-Driven Architecture Skills:** Pre-configured skills for Angular Screaming Architecture, React Screaming Architecture, and NestJS DDD (Domain-Driven Design).
* **Model Context Protocol (MCP) Support:** Built-in MCP declarations for Angular CLI and full-stack tools.

---

## Structure

```text
mysimpleaiplugin/
├── agents/                     # Specialized agent prompt definitions (.agent.md)
│   ├── angular.agent.md
│   ├── developer.agent.md
│   ├── nestjs.agent.md
│   ├── orchestrator.agent.md
│   ├── planner.agent.md
│   ├── react.agent.md
│   ├── researcher.agent.md
│   └── testing.agent.md
├── skills/                     # Architectural guidelines and best practices
│   ├── angular-screaming-architecture/
│   ├── nestjs-ddd-architecture/
│   └── react-screaming-architecture/
├── mcp.json                    # Model Context Protocol server declarations
└── plugin.json                 # Plugin manifest file

```

---

## Installation

To install this plugin directly from the source in your Agent Customizations panel:

1. Open **Agent Customizations** in your IDE.
2. Navigate to the **Plugins** section.
3. Click **Install Plugin from Source**.
4. Paste the URL of this repository:

```text
https://github.com/luisghtz/mysimpleaiplugin
```

---

### MCP Servers

The plugin registers MCP servers using standard environment resolvers (`npx`). When launched inside an IDE session initialized from your shell, tools like `angular-cli` automatically resolve to your active Node/Bun environment.

---

### Sub-agent Cost Model

Worker agents (`Angular`, `React`, `NestJS`, `Testing`, `Researcher`, `Developer`) pin `model: GPT-6 Luna (copilot)` in their frontmatter, so any agent that delegates to them (including the default agent, VS Code 1.140+) uses the cheaper model. The `Orchestrator` restricts its sub-agents with the `agents` frontmatter and only passes an explicit `model` when you ask for one. To change the worker model, edit the `model` line in each worker's frontmatter.

---

## License

[MIT](https://www.google.com/search?q=LICENSE)
