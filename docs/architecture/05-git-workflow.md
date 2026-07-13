# Gardenia Git Workflow

## Purpose

This document defines the Git workflow used during the development of Gardenia.

The objective is to keep the repository clean, understandable, and easy to maintain.

---

# Branch Strategy

The project follows a simplified Git workflow.

Main branches:

- main

Feature branches:

- feature/*

Examples:

feature/product-catalog

feature/create-product

feature/user-authentication

feature/shopping-cart

---

# Main Branch

The main branch always contains stable code.

Every completed feature is merged into main after being reviewed.

---

# Feature Branches

Every new feature should be developed in its own branch.

Example:

feature/product-images

feature/product-search

feature/order-management

Once completed, the branch is merged into main.

---

# Commit Convention

Gardenia follows Conventional Commits.

Examples:

feat: add product entity

feat: implement create product use case

fix: correct stock validation

refactor: simplify product mapping

docs: update domain model

test: add product use case tests

chore: configure dependency injection

---

# Commit Guidelines

A commit should represent one logical change.

Avoid commits like:

update

changes

fix

final version

Instead, describe what was actually modified.

---

# Pull Requests

Although Gardenia is currently developed by a single developer, every feature should be treated as if it were submitted through a Pull Request.

Before merging, verify:

- Code compiles.
- No unnecessary code remains.
- Naming follows project conventions.
- Business rules are respected.
- Documentation is updated if necessary.

---

# Naming Conventions

Projects

Gardenia.Api

Gardenia.Application

Gardenia.Domain

Gardenia.Infrastructure

Classes

PascalCase

Methods

PascalCase

Private fields

_prefix

Interfaces

Prefix with I

Example:

IProductRepository

Namespaces

Gardenia.Domain.Entities

Gardenia.Application.UseCases.Products

Gardenia.Infrastructure.Persistence

---

# Repository Philosophy

Gardenia is intended to simulate a professional software project.

For this reason:

- Every feature starts with analysis.
- Architecture decisions are documented.
- Business rules are identified before implementation.
- Code quality is prioritized over speed.

---

# Future Improvements

Future versions of the workflow may include:

- GitHub Flow
- Protected branches
- Pull Request templates
- GitHub Actions
- CI/CD pipelines