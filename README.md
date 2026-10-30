# SpecForge

Agent platform that turns a structured spec (Jira ticket or GitHub issue) into a pull request.

A planner, coder and reviewer agent read the spec through MCP servers. The coding agent runs in an isolated pod using Azure AI Foundry models and opens a PR on GitHub, where CI runs tests and Playwright E2E. A human approves through an MS Teams Adaptive Card, and every tool call is written to an audit log in PostgreSQL.

## Contents

- MCP servers (Java with Spring AI, Python) with strict input validation and audit logging
- Orchestrator (planner, coder, reviewer)

## Related repositories

- [specforge-infra](https://github.com/NestorSegura/specforge-infra): Azure platform in Terraform
- [specforge-gitops](https://github.com/NestorSegura/specforge-gitops): Kubernetes manifests, Argo CD
