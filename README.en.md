# Old-School Programmer

[简体中文](README.md) | [English](README.en.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/aidealee/old-school-programmer/pulls)

[Development principles: AGENTS.md](AGENTS.md) · [Download the raw file](https://raw.githubusercontent.com/aidealee/old-school-programmer/main/AGENTS.md)

**Put the quality of the result first, act on evidence, and deliver the work in full.**

Old-School Programmer is a set of development guidelines for AI coding assistants. It makes correctness, working functionality, algorithm and experiment outcomes, runtime efficiency, and maintainability the goals of the work. It guides assistants toward direct implementations, proportionate verification, and clear delivery.

All principles are contained in [AGENTS.md](AGENTS.md). Place it in a project and have an assistant that supports project instructions read it for everyday development, bug fixes, refactoring, and research engineering.

## Working principles

| Principle | How it applies to development |
|---|---|
| **Put the quality of the result first** | Choose a simple solution that fully resolves the problem. Decide whether to reuse or refactor based on actual outcomes, complexity, and migration costs. |
| **Act on evidence and keep work moving** | Identify causes from relevant implementations and runtime records, reuse valid evidence, and complete the task within the authorized scope. |
| **Keep implementations simple and safeguards proportionate** | Stay faithful to the algorithm and generalize within its intended scope. Base validation, retries, caching, and concurrency mechanisms on actual requirements and supported failure risks. |
| **Stop when verification is sufficient** | Choose the smallest sufficient checks for the risk and deliver once the agreed safety and acceptance requirements are met. |
| **Protect useful data** | Preserve historical facts, useful data, and changes from other tasks. Use existing recovery mechanisms and promptly handle artifacts confirmed to be unnecessary. |
| **Follow progress efficiently and close clearly** | Choose tools, waits, and notifications to suit the task. Report actual results, verification scope, gaps, and how to resume. |

## Use cases

- **Feature development and bug fixes**: identify shared causes around a concrete goal, complete the implementation, and run the necessary checks.
- **Refactoring and performance optimization**: adjust structure based on actual costs, benefits, and migration effort; eliminate repeated reads, writes, computation, requests, and rendering.
- **Algorithm, experiment, and evaluation engineering**: faithfully implement the chosen algorithm and accurately preserve data splits, scoring definitions, learning order, and actual runtime records.
- **Background and concurrent tasks**: report runtime state accurately, manage tasks and resources, and follow progress at intervals suited to the expected duration.

The rules in AGENTS.md are written in Chinese, and delivery summaries default to concise Chinese. The current task and project requirements determine the technology stack, implementation goals, permissions, and acceptance criteria.

## Quick start

### 1. Get the guidelines

```sh
git clone https://github.com/aidealee/old-school-programmer.git
```

You can also open the [raw AGENTS.md file](https://raw.githubusercontent.com/aidealee/old-school-programmer/main/AGENTS.md) and save it as UTF-8 text with the filename `AGENTS.md`.

### 2. Add it to your project

Copy `AGENTS.md` from the cloned repository to the root of your target project. When the project already has a file with that name, merge these guidelines with its existing instructions, preserving project-specific commands, constraints, and acceptance requirements.

```text
your-project/
├── AGENTS.md
└── project files and directories
```

The guidelines apply to the directory where the file is placed and its subdirectories. When copying or distributing it, retain the copyright and permission notice in [LICENSE](LICENSE), either alongside the file or in the project's third-party license notices.

### 3. Load it and start working

**Codex**: start a new session with the target project as the working directory. Ask the assistant to list the loaded instruction files and summarize the development principles, then submit your task. Codex loads project instructions along the directory hierarchy: `AGENTS.override.md` takes precedence over `AGENTS.md` in the same directory, and instructions in deeper directories take precedence over those above them. When combining multiple instruction files, check the `project_doc_max_bytes` loading limit to ensure that the required rules are loaded in full. See the [official Codex documentation](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

**Other assistants**: load the file through the client's project instruction mechanism. When attaching the file or pasting its text, explicitly ask the assistant to read it in full and use it as instructions for the current development task.

Example task:

```text
Fix [specific issue] according to this project's AGENTS.md.
Identify the cause from the relevant implementation and runtime records,
then complete the changes within the authorized scope.
Run sufficient checks for this change and briefly report the results,
the scope of those checks, and any outstanding items.
```

State the goal, scope, and acceptance criteria when submitting a task. Read-only reviews, planning, implementation changes, and ongoing monitoring each follow their own authorized scope.

## Scope and constraints

- **Authorization and permissions**: follow the current user task and applicable project instructions within actual permissions and safety requirements. Continue authorized work; consolidate requests for confirmation when required authorization is missing or the scope or impact changes.
- **Necessary correctness mechanisms**: retain checks and constraints that provide actual guarantees, handle input at real trust boundaries, and add checks for specific consistency gaps.
- **Verification and experiments**: preserve mandatory safety and acceptance requirements. Report local checks according to their actual scope. Explain the concrete gap and necessary cost of extending the agreed verification scope, and let the user decide.
- **Data and recovery**: preserve useful data and historical facts, and adjust research settings according to the user's explicit goals. Follow the specific confirmation requirements for irreversible deletion. When an operation's outcome is unknown and repeating it could cause side effects, verify the original operation first.
- **Background work and delivery**: follow the user's stopping conditions when continuous monitoring is requested. For tasks that can run independently and have a continuation plan, report their state and how to resume. Distinguish changes made, changes deployed, and results verified.

See [AGENTS.md](AGENTS.md) for the complete constraints and exceptions.

## Repository contents

| File | Purpose |
|---|---|
| [AGENTS.md](AGENTS.md) | Complete development principles that can be loaded independently |
| [README.md](README.md) | Project introduction and usage instructions in Chinese |
| [README.en.md](README.en.md) | Project introduction and usage instructions in English |
| [LICENSE](LICENSE) | MIT license and copyright notice |

## Contributing

[Pull requests](https://github.com/aidealee/old-school-programmer/pulls) that improve wording and usage instructions are welcome. Preserve the meaning, scope, and exceptions of the development principles.

## Related project and license

[Old-School Researcher](https://github.com/aidealee/old-school-researcher), from the same series, provides guidelines for writing and revising Chinese and English academic texts. This project focuses on development collaboration and is used through AGENTS.md.

Licensed under the [MIT License](LICENSE). Copyright © 2026 aidealee.
