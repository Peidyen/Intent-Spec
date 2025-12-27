# Intent-First AI Specification Template

This repository provides a lightweight, AI-native standard for defining systems using intent and meaning before implementation.

It introduces two complementary files:

INTENT.md — defines what a system means

RAG.md — defines what an AI should know while reasoning about it

Together, these files allow humans and AI agents to reason, build, and iterate on systems without collapsing intent into code.

Why This Exists

Modern AI tools are excellent at writing code, but fragile at preserving meaning over time.

This template exists to solve that problem by:

Separating intent from implementation

Making invariants explicit

Reducing hallucination and over-engineering

Enabling rapid, disposable execution (PoCs) without losing semantic clarity

Execution is cheap.
Intent is not.

Core Concepts
INTENT.md — Semantic Contract

INTENT.md defines:

Purpose

Core semantics

Invariants and laws

Constraints and non-goals

Exit criteria

It answers the question:

What must be true for this system to be correct?

If code and INTENT.md disagree, INTENT.md wins.

RAG.md — Context and Knowledge

RAG.md defines:

Domain background

Canonical definitions

Reference models

Examples and scenarios

Known approximations and failure modes

It answers the question:

What should an AI know while reasoning about this system?

RAG.md informs reasoning. It does not enforce behavior.

How This Is Used

This template is designed to work naturally with modern AI tooling.

ChatGPT

ChatGPT uses:

INTENT.md as the semantic contract

RAG.md as grounding and contextual knowledge

It is used for reasoning, explanation, validation, and iteration, while respecting explicit invariants and avoiding hallucination.

Replit

Replit uses:

INTENT.md as authoritative intent

RAG.md as supporting domain knowledge

Replit instantiates runnable proofs of concept quickly and surfaces emergent behavior through execution.

Execution is disposable. Insight is not.

Cursor and GitHub

Cursor and GitHub are used once a concept is validated and needs to live longer.

Implementations are hardened, but INTENT.md continues to govern correctness and meaning.

Repository Structure

This repository contains:

Root-level INTENT.md and RAG.md as canonical templates

A workflow directory explaining how AI tools consume these files

An examples directory containing complete, real-world examples

Canonical Example: Planetary Orbit Simulator

The planetary orbit simulator example demonstrates:

Momentum conservation

Barycenter motion

Emergent system drift

Absence of a privileged reference frame

The example intentionally produces a non-intuitive but correct outcome: after an inelastic collision, the entire system moves.

This behavior emerges naturally when intent and invariants are respected.

When to Use This Template

Use this template when:

Exploring a concept, model, or system

Building AI-assisted proofs of concept

You care about invariants and semantics

You want fast execution without losing meaning

Do not use this template when:

You already have a stable production system

You require strict formal verification

You are writing low-level infrastructure code

Philosophy

Intent before code

Meaning before implementation

Declarative over procedural

Execution is disposable

Specifications are now for machines as well as humans

License

MIT (or your preferred license)