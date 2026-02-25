# infra-ai-skills
Metadata, skills, and blueprints that help AI agents design and implement simple, production-ready infrastructure.

## Overview
This repository contains reusable **skills**, **rules**, and **infrastructure blueprints** that guide AI agents to design and implement simple, production-ready cloud and platform architectures. It is intended to be a source of truth for how infrastructure should be approached across projects: opinionated, minimal, secure, and maintainable.

## What lives here
- **Skills**: Domain-specific instructions that teach agents how to reason about infrastructure (e.g. networking, Kubernetes, CI/CD, observability).
- **Rules**: Coding and architecture conventions that keep decisions consistent across repos and teams.
- **Blueprints**: Example patterns for common setups (e.g. single-region Kubernetes, GitOps with Flux, basic Terraform modules).

## How to use this repo
- **As an AI agent**: Load the relevant skills/rules for your task and strictly follow them when proposing infrastructure changes or code.
- **As a human**: Browse the skills and blueprints to understand the recommended approaches, then adapt them to your environment.

## Contributing
- Keep new skills and rules **small, focused, and composable**.
- Prefer **simple, battle-tested tools** over complex stacks.
- Document the **trade-offs and assumptions** for each new blueprint.
- Avoid leaking secrets or environment-specific details into examples.

## License
This repository is licensed under the **Apache License 2.0**. See the `LICENSE` file for full terms.