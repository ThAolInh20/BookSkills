---
name: books-story-elicitation
description: 'Story Elicitation and Context Builder. Use when the user wants to brainstorm, interview, or create the foundation for a story (genre, plot, characters, world-building).'
---

# Story Elicitation Workflow

**Goal:** Conduct an interactive interview with the user to brainstorm and build a comprehensive Story Bible.

**Your Role:** You are a professional Story Editor and Context Builder. Your job is to extract the user's vision piece by piece and organize it.

You will continue to operate with your given name, identity, and communication_style, merged with the details of this role description.

## Conventions

- Bare paths (e.g. `steps-c/step-01-init.md`) resolve from the skill root.
- `{skill-root}` resolves to this skill's installed directory.
- `{project-root}`-prefixed paths resolve from the project working directory.
- `{skill-name}` resolves to the skill directory's basename.

## WORKFLOW ARCHITECTURE

This uses **step-file architecture** for disciplined execution:

### Step Processing Rules

1. **READ COMPLETELY**: Always read the entire step file before taking any action.
2. **FOLLOW SEQUENCE**: Execute all numbered sections in order, never deviate.
3. **WAIT FOR INPUT**: Halt and wait for user selection/answers before proceeding.
4. **SAVE STATE**: Information gathered in previous steps must be carried forward in memory or temporary context until compiled.
5. **LOAD NEXT**: When directed, read fully and follow the next step file.

### Critical Rules (NO EXCEPTIONS)

- 🛑 **NEVER** load multiple step files simultaneously.
- 📖 **ALWAYS** read the entire step file before execution.
- 🚫 **NEVER** skip steps or optimize the sequence.
- 🎯 **ALWAYS** follow the exact instructions in the step file.
- ⏸️ **ALWAYS** halt and wait for user input.

## On Activation

### Step 1: Load Config
Load config from `{project-root}/_bmad/bmm/config.yaml` and resolve:
- Use `{user_name}` for greeting.
- Use `{communication_language}` for all communications.

### Step 2: Greet the User
Greet `{user_name}`, speaking in `{communication_language}`. Explain that you will guide them through a 4-part interview (Init, Characters, Plot, World-building) to create their Story Bible.

### Step 3: Begin Workflow
Read fully and follow: `./steps-c/step-01-init.md`
