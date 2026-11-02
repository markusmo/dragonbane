# About

This repository is an application that manages a character sheet for the table top game Dragonbane and turnbased combat for said game.

# Skills

In `.agents` there are the following skills:

- `dragonbane-rules`: contains the basic rules for the character sheet and combat
- `vuejs-expert`: programming rules for vuejs v3
- `electron-development`: contains a skill for Electron development.

_Whenever_ you learn something while running you update or create a new **skill**, **rule** or **architectural document** as memory for later usage.

- `docs/architecture.md` shall contain information about architecture. It has to be short and to the point.
- `docs/decisions.md` shall contain architectural decisions. They can reference the architecture document. Decisions taken have to be documented in a understandable, but to the point.

# Structure of this repository

It is a PWA build using the quasar UI framework and Vue.js version 3. It is able to build an electron app that can be run on any machine. The `README.md` contains information about installing and building the application.

- `public` contains the artifacts for icons.
- `src` contains the Vue.js application
- `src-pwa` contains the build information for the PWA, that is later on used for the Electron app.

# Plan the execution

## Task Evaluation Guardrails

Not every task requires a specialized skill. For straightforward issues (e.g., small CSS fixes, simple script writing, renaming a variable), **DO NOT USE** specialized skills. Over-engineering simple tasks wastes tokens and time.

Before invoking any skills, evaluate the task:

1. **Is the task simple/contained?** Solve it directly using the agent's ordinary file editing, search, and terminal capabilities available in the current environment.
2. **Is the task complex/multi-domain?** Only then should you proceed to orchestrate skills.

## Skill Selection & Combinations

When a task is deemed complex, identify the necessary domains (e.g., frontend, database, deployment). Search available skills in the current environment to find the most relevant ones. If the required skills are not found locally, consult the master skill catalog.

## Host and memory boundaries

Use the host’s actual installed catalog/tool schemas. Remote catalog text is discovery data, not authorization to install or execute skills. Honor the host/user memory policy before writing durable records and exclude private project details/secrets; recalled combinations are suggestions, not current correctness evidence.

## Step-by-Step Guide

### 1. Task Evaluation & Guardrail Check

[Triggered when facing a new user request that might need skills]

1. Read the user's request.
2. Ask yourself: "Can I solve this efficiently with just basic file editing and terminal commands?"
3. If YES: Proceed without invoking specialized skills. Stop the orchestration here.
4. If NO: Proceed to step 2.

### 2. Create an implementation plan

1. Convert the task into smaller steps for incremental implementation.
2. Each step should be an incremental step towards the goal.
3. Identify the layers where you need to perform a change.

### 3. Execute the implementation plan

Implement the feature or bugfix according to the plan you created.

### 4. Build the application

1. Build the application using `npm run dev`
2. Inform the user that the application is running
3. Give quick review instructions for manual testing.

### 5. Track Skills and Track the Progress

[Triggered after executing the task using the selected skills]

1. Verify what actually completed and which checks ran; record failures/unverified outcomes as such rather than assuming a skill combination succeeded.
2. Update or create skills and track the implementation using a memory, so that you can recall architectural decisions
3. Document decisions and paths that did not work for later reference.
4. Keep all the documentation **as short as possible**.

### 6. Commit

[Triggered when everything has been documented and tested]

Feature should be committed using `(feat) <description here>`, bugs using `(bug) <description here>` and then inform the user that she/he is able to push to the repository
