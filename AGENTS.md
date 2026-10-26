# AGENTS.md

# Music Workspace - AI Development Guide

## Purpose

This project follows Spec-Driven Development (SDD).

The goal is to make every implementation predictable, maintainable, and aligned with the product vision.

AI agents are expected to behave as software engineers, not product designers.

---

# Source of Truth

Always follow this priority:

1. User instructions in the current conversation
2. Relevant specification document
3. docs/architecture.md
4. docs/vision.md

If two sources conflict, stop and ask for clarification.

Never choose one by yourself.

---

# General Rules

- Never invent requirements.
- Never implement undocumented behavior.
- Never assume business rules.
- Never silently "improve" the product.
- Never add features that were not requested.
- Never remove existing behavior unless explicitly instructed.
- Never make product decisions.

When in doubt:

STOP.

Explain the ambiguity.

Ask questions.

Wait for an answer.

---

# Scope Control

Implement only what was requested.

If a request naturally leads to another feature, do not implement it unless explicitly included in the specification.

Example:

Requested:

- Music search

Do NOT also implement:

- Search history
- Search suggestions
- Filters
- Favorites

unless specified.

---

# Code Quality

Code should be:

- Simple
- Readable
- Explicit
- Modular
- Strongly typed whenever possible
- Easy to test

Prefer clarity over cleverness.

Avoid unnecessary abstractions.

---

# Architecture

Respect the project architecture.

Do not:

- Move files
- Rename modules
- Introduce new frameworks
- Change folder structure
- Change database schema

unless explicitly requested.

---

# Dependencies

Before adding any dependency:

Ask:

- Why is it needed?
- Is there an existing solution?
- Does it increase maintenance?

Avoid unnecessary packages.

---

# Documentation

If implementation changes the architecture or behavior described in the documentation:

Stop.

Ask whether the documentation should be updated first.

Never allow documentation and implementation to diverge.

---

# Database

Never modify database models or migrations without explicit approval.

Schema changes are product decisions.

---

# API

Never change public API contracts without approval.

Backward compatibility matters.

---

# UI

Do not redesign interfaces.

Implement only the requested behavior.

If UI behavior is ambiguous, ask.

---

# Errors

Prefer explicit errors over hidden behavior.

Fail loudly.

Do not silently ignore invalid states.

---

# Security

Never expose secrets.

Never hardcode credentials.

Validate all external input.

Escape user-generated content when appropriate.

---

# Git

Keep changes focused.

Avoid unrelated refactors.

One logical change per commit.

---

# Communication

When uncertain:

- Explain the ambiguity.
- Present the possible options.
- Wait for a decision.

Never guess.

The user is responsible for product decisions.

The AI is responsible for implementation quality.

---

# Principle

Incorrect code can be fixed.

Incorrect product decisions are much more expensive.

When uncertainty exists:

Ask first.

---

# Simplicity First

Always prefer the simplest solution that satisfies the current specification.

Do not build for hypothetical future requirements.

The project will evolve incrementally.

Future extensibility should never justify unnecessary complexity today.