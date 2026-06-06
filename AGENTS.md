# Agent Development Guide

This file defines mandatory operating procedures for all coding agents.

## Workflow

For every task:

1. Select a TODO item.
2. Implement it.
3. Run validation.
4. Update documentation.
5. Update TODO status.
6. Stop and wait for user approval.

Never start the next task automatically.

## TODO Management

Maintain a persistent TODO list.

Status:

- [ ] Not Started
- [~] In Progress
- [x] Completed

When context becomes large:

- Compress completed tasks.
- Keep only outcomes.
- Preserve recovery information.

## Validation

A task is not complete until all pass:

- Unit Tests
- Integration Tests
- Lint
- Type Check

Prefer using sub-agents for validation tasks.

## Context Management

Preserve:

- Requirements
- Architecture decisions
- Current task state

Summarize:

- Build logs
- Test logs
- Debug logs

## Documentation

Keep documentation synchronized with implementation.

Update affected files whenever behavior changes.

## Safety

Never:

- Skip validation
- Hardcode secrets
- Change requirements silently

Always:

- Assess impact before changes
- Document breaking changes
- Leave the repository in a working state