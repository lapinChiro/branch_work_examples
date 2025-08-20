# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a documentation project for creating branch workflow diagrams using Mermaid format in Markdown. The main goal is to document different Git branching strategies (GitFlow, GitHubFlow, GitLabFlow) using Mermaid diagrams.

## Repository Structure

- `diagram.md` - Main file containing the branch workflow diagrams in Mermaid format
- `mermaid-docs/` - Reference documentation for Mermaid syntax and features
  - `syntax/` - Detailed documentation for each diagram type
  - `config/` - Configuration and setup documentation
  - `community/` - Community contribution guidelines

## Primary Task

Complete the `diagram.md` file with comprehensive branch workflow examples for:
1. GitFlow
2. GitHubFlow
3. GitLabFlow

## Working with Mermaid Diagrams

When editing Mermaid diagrams in `diagram.md`:
- Use the `gitGraph` diagram type for visualizing Git branching workflows
- Refer to `mermaid-docs/syntax/gitgraph.md` for detailed gitGraph syntax
- Common gitGraph commands:
  - `commit id: "message"` - Create a commit
  - `branch branch-name` - Create a new branch
  - `checkout branch-name` - Switch to a branch
  - `merge branch-name` - Merge a branch

## Language

The project documentation is primarily in Japanese. Maintain consistency by using Japanese for:
- Section headers in `diagram.md`
- Commit messages in the diagrams
- Documentation comments