# Timely Optimizer: Teacher Breaks

This repository contains a product take-home exploring how Timely could help school schedulers catch and address teacher-break problems across the schedule-building process.

## The exercise

The prompt focuses on two patterns: **uneven breaks**, where teachers have long runs of consecutive classes, and **clustered breaks**, where free periods fall on one rotation day but not another. The work covers discovery questions and expected insights, solution options and trade-offs, user stories, an implementation sequence, and a clickable concept.

## Proposed solution

- **Pre-run check:** Before a full build, check the school's own break rules against the current setup and assignments. Surface issues while they are still easier to address.
- **Schedule health flags:** After the build, show break outcomes with an explanation and a next step for each error or warning. Use Info for context the scheduler cannot resolve in the schedule, such as a staffing limit.
- **Keep the Optimizer in control of the math:** The Optimizer remains deterministic and is the source of truth. Suggested changes are checked by the Optimizer. An LLM may explain a multi-factor outcome using build data, but it does not choose fixes or change the schedule.

The proposed measures include the share of teachers meeting their school's break rules and the share of error and warning flags resolved before publishing, alongside student scheduling and core-request outcomes. Run time and AI accuracy are guardrails.

## Prototype

[Open the interactive concept](https://melanieps1.github.io/timely-optimizer-concept/).

The prototype is a concept with sample data. It is not Timely's real interface or production data.
