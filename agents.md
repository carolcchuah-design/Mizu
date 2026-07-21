# AGENTS.md

# Mizu Care - AI Development Guide

## Purpose

This document provides instructions for AI coding assistants working on the Mizu Care project.

Before implementing any feature:

1. Read this file.
2. Review the relevant document in the `docs/` folder.
3. Implement only the requested milestone.
4. Do not introduce unrelated changes.

---

# Project Goal

Build a mobile-first Progressive Web App that helps a family care for their puppy, Mizu.

The application should always answer the question:

> **What does Mizu need right now?**

If a proposed implementation does not improve this goal, reconsider it.

---

# Core Principles

* Keep the application simple.
* Mobile-first always.
* Prefer readability over cleverness.
* Build reusable components.
* Keep business logic separate from UI.
* Minimize dependencies.
* Avoid premature optimization.
* Do not over-engineer solutions.

---

# Source of Truth

Documentation lives in the `docs/` directory.

| Document                       | Purpose                 |
| ------------------------------ | ----------------------- |
| 01-Product-Vision.md           | Product vision          |
| 02-Product-Requirements.md     | Functional requirements |
| 03-User-Stories.md             | User stories            |
| 04-Information-Architecture.md | Navigation              |
| 05-UI-Design-System.md         | UI rules                |
| 06-System-Architecture.md      | Architecture            |
| 07-Database-Specification.md   | Data model              |
| 08-Development-Roadmap.md      | Development order       |

If documentation and code disagree, update the code—not the documentation—unless explicitly instructed.

---

# Development Workflow

Work only on the requested roadmap phase.

For each feature:

1. Understand the requirement.
2. Build the smallest complete solution.
3. Test it.
4. Refactor only if it improves clarity.
5. Stop when the acceptance criteria are met.

Do not implement future roadmap phases without being asked.

---

# Coding Standards

## General

* Use TypeScript.
* Prefer functional React components.
* Keep functions small.
* Avoid duplicated logic.
* Use descriptive names.
* Remove unused code.
* Comment only when the intent is not obvious.

---

## Components

Components should have a single responsibility.

Prefer composition over large components.

Avoid components that exceed a few hundred lines unless there is a clear reason.

---

## State Management

Keep state as local as possible.

Only use shared/global state when multiple screens require the same data.

Avoid duplicate sources of truth.

---

## Styling

* Use Tailwind CSS.
* Reuse existing UI components.
* Maintain consistent spacing.
* Follow the design system.

Do not introduce custom styling patterns without a strong reason.

---

# User Experience

Every screen should feel:

* Fast
* Friendly
* Simple
* Predictable

The Today screen is the primary experience.

Optimize for one-handed mobile use.

---

# Performance

Prefer:

* Simple algorithms
* Efficient rendering
* Lazy loading where appropriate
* Small bundles

Avoid unnecessary re-renders.

---

# Accessibility

Every feature should consider:

* Keyboard navigation
* Screen readers
* Color contrast
* Touch target size
* Focus indicators

Accessibility is part of the definition of done.

---

# Testing Expectations

Before considering a feature complete:

* Builds successfully
* No TypeScript errors
* No lint errors
* Existing functionality still works
* Mobile layout verified
* Acceptance criteria satisfied

Fix the root cause rather than hiding warnings or errors.

---

# Error Handling

Handle expected failures gracefully.

Provide clear, user-friendly error messages.

Never silently discard user data.

---

# Scope Control

Implement only what has been requested.

Do not:

* Add speculative features.
* Create unnecessary abstractions.
* Introduce new libraries without justification.
* Refactor unrelated code.

Keep pull requests focused.

---

# Definition of Done

A feature is complete when:

* It meets the documented requirements.
* It satisfies the user story acceptance criteria.
* It follows the UI Design System.
* It works on mobile.
* It has been tested.
* It does not introduce regressions.

---

# Guiding Philosophy

Choose the simplest solution that solves the problem well.

The best implementation is one that is easy to understand, easy to maintain, and pleasant for the family to use every day.

