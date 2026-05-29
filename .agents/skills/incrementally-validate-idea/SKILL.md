---
name: incrementally-validate-idea
description: Find the smallest valuable version of an idea, simplify it without reducing user value, and generate an evidence-driven phased validation plan.
---

# Incrementally Validate Idea

## Purpose

Use this skill when evaluating a new product, game, tool, workflow, business idea, or feature set.

The goal is to:

1. Identify the smallest version of the idea that still delivers its core value.
2. Remove implementation complexity that does not contribute directly to that value.
3. Create a phased development plan where each phase introduces one meaningful capability.
4. Define what must be learned or validated before moving to the next phase.

This skill is intended for early-stage idea development and should be run before implementation planning.

## Process

### Step 1: Understand The Idea

Summarize the idea in a few sentences.

Identify:

* Target user
* User motivation
* Primary experience
* Key constraints

Do not evaluate yet.

### Step 2: Find The Core Loop

Determine:

"What is the smallest repeatable interaction that creates value for the user?"

Express it as:

Action → System Response → User Reaction

Examples:

* Upload document → receive summary → decide next action
* Choose characters → watch conversation → observe outcome
* Enter goal → receive plan → take action

The core loop should be short enough to explain in one sentence.

### Step 3: Separate Core From Presentation

Create two lists.

#### Core

Elements that must exist for the core loop to work.

#### Presentation

Elements that improve immersion, polish, realism, convenience, aesthetics, scale, or completeness.

Assume presentation elements can be delayed unless proven otherwise.

### Step 4: Simplify Aggressively

Propose ways to reduce implementation effort while preserving:

* User agency
* User control
* Entertainment value
* Learning value
* Utility value

For each simplification:

* What is removed?
* What is preserved?
* Why is the experience still intact?

Favor substitutions, shortcuts, abstractions, and fake implementations over full systems.

### Step 5: Define Validation Questions

Identify the most important uncertainties.

Examples:

* Is the core interaction fun?
* Will users repeat the loop?
* Does memory improve outcomes?
* Do users care about customization?
* Does realism matter?

List the questions in order of risk.

### Step 6: Create Phases

Generate development phases.

Rules:

* Each phase should introduce only one major capability.
* Each phase should be playable, usable, or testable.
* Each phase must have a validation goal.
* A later phase should never be required to validate an earlier assumption.

Use the format:

#### Phase X: [Name]

Purpose:
[What gets built]

Validation Goal:
[What must be learned]

Success Criteria:
[Observable evidence that justifies continuing]

### Step 7: Identify The Fastest Path To First Validation

Answer:

"If we wanted to learn whether this idea has merit in the shortest possible time, what would we build first?"

Provide:

* Exact scope
* What to exclude
* What question it answers

## Output Format

Produce:

1. Idea Summary
2. Core Loop
3. Core vs Presentation
4. Simplification Opportunities
5. Validation Questions
6. Incremental Development Plan
7. Fastest Path To First Validation

Do not generate technical architecture.

Do not generate implementation details.

Do not optimize for completeness.

Optimize for learning speed and reduction of wasted effort.