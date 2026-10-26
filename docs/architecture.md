# Architecture

## Overview

Music Workspace is a full-stack web application built around a REST API architecture.

The project is organized as a monorepo containing the frontend, backend, documentation and specifications.

The architecture prioritizes:

- Simplicity
- Maintainability
- Extensibility
- Strong typing
- Clear separation of responsibilities

The application should evolve incrementally without introducing unnecessary complexity.

---

# Tech Stack

## Frontend

- React
- Vite
- TypeScript
- Tailwind CSS
- React Router

## Backend

- FastAPI
- Python

## Database

- PostgreSQL
- SQLAlchemy
- Alembic

## Development

The project should maintain a modern development workflow.

This includes:

- Git version control
- Pull Requests
- Continuous Integration (CI)
- Automated linting
- Automated formatting
- Automated tests

Deployment strategy may evolve independently from the application architecture.

Docker is used to provide a consistent local development environment.

Running the project should not require manual installation of infrastructure dependencies.

---

# Project Structure

```
music-workspace/

frontend/
backend/

docs/
specs/

README.md
AGENTS.md
```

Each application is responsible only for its own concerns.

The frontend never accesses the database directly.

All communication happens through the backend API.

---

# Frontend

The frontend is responsible for:

- User interface
- Navigation
- State management
- Rendering chord diagrams
- Consuming the backend API

Business rules must be implemented in the backend.

The frontend is responsible only for presentation and user interaction.

---

# Backend

The backend is responsible for:

- Business rules
- Authentication
- Authorization
- Data validation
- Database access
- Public API

The backend should remain stateless whenever possible.

---

# Database

PostgreSQL is the primary database.

Relational data includes, but is not limited to:

- Users
- Songs
- Artists
- Chords
- Playlists
- Notes
- Comments

Database schema should evolve through migrations.

---

# File Storage

Binary files should not be stored inside the database.

Examples:

- Images
- PDFs
- Audio recordings

These should be stored using a dedicated storage solution.

The database stores only metadata and references.

---

# AI

Artificial Intelligence is an auxiliary component.

AI may be used for tasks such as:

- OCR
- Importing chord sheets
- Parsing documents
- Data extraction

AI must never replace business rules or application validation.

Every AI-generated result must be validated before persistence.

---

# Chord Engine

Chord diagrams are provided through an internal abstraction.

The application must not depend directly on a specific external provider.

Possible implementations include:

- Local database
- Open-source libraries
- Third-party APIs

The implementation may change without affecting the rest of the application.

---

# API

The frontend communicates exclusively with the backend through a REST API.

The API is the single source of truth for application data.

Public contracts should remain stable whenever possible.

---

# Authentication

Authentication will use JWT (JSON Web Tokens).

Protected endpoints require a valid access token.

Authentication is only required for features that involve user-specific data, such as:

- Personal workspace
- Playlists
- Notes
- Imported files
- Community features

Public resources, such as browsing the music library, should remain accessible without authentication whenever possible.

---

# General Principles

- Prefer simple solutions.
- Avoid premature optimization.
- Avoid unnecessary abstractions.
- Build only what is currently required.
- Keep documentation and implementation synchronized.
- Every architectural decision should prioritize long-term maintainability.

---

# Guiding Principles

- Open source first
- Offline-friendly whenever possible
- API-first architecture
- Mobile-responsive by default
- Accessibility should be considered during development
- Favor maintainability over clever implementations