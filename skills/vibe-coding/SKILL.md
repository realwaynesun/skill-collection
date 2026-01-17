---
name: vibe-coding-workflow
description: A structured vibe coding workflow for building products from scratch using Claude Code. Use when starting new projects, planning MVPs, managing iterations, or deploying applications. Covers the full lifecycle from initial planning through deployment.
author: waynesun
inspired_by: "@turingou (https://x.com/turingou/status/2009985547130015793)"
---

# Vibe Coding Workflow

A consistent methodology for building products with Claude Code, optimized for maintaining coherence across multiple parallel projects.

## Phase 1: Initial Planning (`/plan` mode)

Start every project by entering `/plan` mode to establish shared context:

1. **Product Background** - Explain why you're building this product
2. **Target Users** - Define who will use it
3. **Core User Stories** - Describe the main user journeys

It's normal to start with only a vague idea. The first planning session creates rough consensus. Claude will ask clarifying questions to enrich your concept, then propose an MVP approach.

## Phase 2: MVP Execution

After plan approval:
1. Set appropriate permissions (auto-accept, etc.)
2. Let Claude execute the MVP in one go
3. Claude will break it into 1-7 phases and auto-execute all

## Phase 3: MVP Validation

**Focus on validating the main user stories first.** Ignore minor bugs during this phase.

Once core functionality is verified:
- Collect all bugfixes and non-critical items
- Move them to a new iteration (use a TODO file or similar)
- The specific iteration format is flexible—don't obsess over consistency

**Pro tip**: Set up a hook to auto-commit whenever the TODO file is modified. This enables easy rollbacks:

```bash
# Example hook concept: auto-commit on TODO changes
```

## Phase 4: UI/UX Polish

Save brand and UI work for last—it's a near-fully-automated task.

**Workflow**:
1. Use Gemini (or similar) to generate reference logo and design style images
2. Find a single-page design reference or use existing design prompts
3. Download the reference HTML locally
4. Let Claude reference it for the full UI overhaul

This phase requires minimal human intervention. Claude can handle it end-to-end.

## Phase 5: Deployment

For **Vercel + Next.js**: Fully automated, no manual steps needed.

**Pre-launch checklist** (use `/plan` mode):
- Generate legal documents (Privacy Policy, Terms of Service, etc.)
- Optional: Use Codex or another reviewer to check for security risks

## Quick Reference

| Phase | Key Action | Human Involvement |
|-------|-----------|-------------------|
| 1. Plan | `/plan` mode, establish context | High |
| 2. MVP | Auto-execute 1-7 stages | Low |
| 3. Validate | Test core user stories | Medium |
| 4. UI/UX | Reference-based redesign | Minimal |
| 5. Deploy | Vercel auto-deploy + legal docs | Low |
