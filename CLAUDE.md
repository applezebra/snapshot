# SnapSpot Project Playbook

## Project Overview
SnapSpot is a gamified social mobile web app connecting travelers who need photos with nearby photographers. Built with React, TypeScript, and Vite, photographers are rewarded with social currency (Instagram mentions, in-app levels, portfolio building) instead of money.

---

## Core Development Principles

### 1. Tiny Steps Approach
**MANDATORY: All code changes must follow these constraints:**
- **Maximum Lines**: 300 lines of code per step
- **Maximum Files**: 3 files modified per step
- **Test-Runner Trigger**: MUST run when 600 LOC accumulated
- **Autonomous Execution**: Agents execute within constraints automatically
- **Quality Gates**: test-runner and code-reviewer validate all changes
- **Documentation Exemption**: LOC limits do NOT apply to .md/.txt files in /docs/

### 2. Agent Role Separation
Each agent maintains strict boundaries:
- **codebase-explainer**: Analysis and understanding only
- **spec-analyzer**: Requirements gathering and clarification
- **spec-writer**: Product specifications (WHAT to build) → `/docs/spec/`
- **impact-analyzer**: Analyze specs, create parallel delivery lanes
- **plan-writer**: Implementation plans (HOW to build) → `/docs/impl/`
- **feature-scaffolder**: Create initial file structure and boilerplate
- **code-implementer**: Code changes within size constraints
- **debug-triage**: Bug investigation without code changes
- **bug-fixer**: Apply minimal fixes to failing tests
- **test-runner**: Test execution and reporting
- **code-reviewer**: Code quality review (pre-test and post-test)
- **security-auditor**: Security review (read-only)
- **git-strategist**: Git workflow strategy (branching, merge planning)
- **git-steward**: Git execution only (stage, commit, push)
- **pr-butler**: Create pull requests with automated metadata
- **ui-advisor**: UI/UX guidance for component design
- **ux-advisor**: User experience design and flow optimization

Agents MUST NOT overlap responsibilities.

---

## Development Workflows

### Software Development Life Cycle (SDLC)

#### Phase 1: Requirements & Analysis
1. Use **spec-analyzer** to interview and clarify requirements
2. Use **spec-writer** to document product specification → `/docs/spec/`
3. Define WHAT to build: user needs, acceptance criteria, success metrics
4. Focus on product thinking, NOT technical implementation

#### Phase 2: Design & Planning
1. Use **impact-analyzer** to analyze specs and create parallel delivery plans
2. Use **plan-writer** to document implementation plan → `/docs/impl/`
3. Include WHAT/WHY/HOW context for each step

#### Phase 3: Implementation
1. Use **git-strategist** to plan feature branch strategy
2. Use **git-steward** to execute the strategy:
   - Create feature branch from `main` (or `dev` if exists)
   - Create worktree from feature branch
3. **Development Iteration** (repeat as needed):
   - Use **code-implementer** for changes in worktree (Tiny Steps: 300 lines max)
   - **test-runner MUST run when 600 LOC accumulated**
   - Use **git-steward** to commit and push changes
   - Iterate until feature complete
4. After implementation complete:
   - Merge worktree → feature branch (via **git-steward**)
   - Proceed to Phase 4 for final testing

#### Phase 4: Testing & Validation
1. **code-reviewer** performs quick sanity check (Pre-Test Review)
2. Run tests with **test-runner** after code review passes
3. **MANDATORY: If tests fail** → Use **debug-triage** to analyze root cause BEFORE fixing
4. After triage → Use **bug-fixer** to apply minimal fix
5. Re-run **test-runner** to verify fix
6. **code-reviewer** performs final quality review after all tests pass (Post-Test Review)
7. Security review with **security-auditor** for sensitive code

#### Phase 5: Deployment
1. Use **pr-butler** to create pull request
2. Merge to main branch
3. Deploy to hosting platform (Railway/Vercel/Netlify)
4. Verify deployment in production

---

## Critical Rules

### Code Change Rules

#### Size Constraints (STRICT)
```
Per Step Limits:
├── Lines of Code: 300 maximum per step
├── Files Modified: 3 maximum
├── Test Trigger: 600 LOC accumulated → MUST run test-runner
├── Documentation: LOC limits exempt for /docs/**/*.{md,txt}
├── Execution: Autonomous within constraints
└── Validation: test-runner + code-reviewer
```

#### Autonomous Execution Protocol
1. Agents execute changes within size constraints
2. code-implementer tracks cumulative LOC across steps
3. test-runner MUST run when 600 LOC threshold reached
4. Agents report summary of changes made
5. code-reviewer ensures quality and scope adherence
6. Documentation changes exempt from LOC tracking

---

## Git Workflow Strategy

### Branch Strategy
- **main** - Production-ready code
- **Feature branches** - Development work (`feat/*`, `fix/*`)
- Naming: `feat/real-time-matching`, `fix/location-bug`

### Worktree-First Development
1. Phase 3 Start: **git-strategist** recommends feature branch strategy
2. **git-steward**: Create feature branch from `main` + create worktree
3. **code-implementer**: Implement changes step by step in worktree
4. **test-runner** + **code-reviewer**: Validate in worktree
5. **git-steward**: Merge worktree → feature branch, push to remote
6. **pr-butler**: Create PR from feature branch → `main`
7. Merge to `main` → deploy to production

---

## Project-Specific Guidelines

### Technology Stack
- **Frontend**: React with TypeScript
- **Build**: Vite
- **Mobile**: Mobile-responsive web app (not native)
- **State**: TBD (Zustand or Context API)
- **Styling**: TailwindCSS
- **Backend**: TBD (Firebase/Supabase or custom Node.js)
- **Deployment**: Railway + GitHub integration

### Key Features to Implement
1. **Real-time photographer matching** (like Uber for photos)
2. **Gamification system** (levels, points, leaderboards)
3. **Instagram integration** (mentions, sharing)
4. **Location services** (see nearby photographers)
5. **Session management** (request photo, accept, complete)
6. **Portfolio display** (photographer photos with Instagram likes)
7. **Review system** (ratings, feedback)

### Testing Requirements
- Use Vitest for all tests
- Test after each implementation step
- Minimum coverage for new features: 70%
- Integration tests for matching logic
- Mobile responsiveness tests

---

## Available Agents (from Nexusdesk)

### Planning & Analysis
- **spec-analyzer**: Requirements gathering through interviews
- **spec-writer**: Product specification documentation
- **impact-analyzer**: Create parallel delivery lanes
- **plan-writer**: Implementation plan documentation

### Implementation
- **feature-scaffolder**: Initial boilerplate creation
- **code-implementer**: Code changes within constraints
- **ui-advisor**: UI/UX component guidance
- **ux-advisor**: User experience flow design

### Quality & Testing
- **debug-triage**: Bug investigation
- **bug-fixer**: Minimal bug fixes
- **test-runner**: Test execution
- **code-reviewer**: Code quality review
- **security-auditor**: Security review

### Git & Deployment
- **git-strategist**: Git workflow strategy
- **git-steward**: Git execution
- **pr-butler**: Pull request creation

### Business & Strategy
- **chief-strategy-officer**: Strategic guidance
- **compliance-trust-architect**: Compliance guidance
- **nexvoice-brand-architect**: Brand voice guidance
- **orbit-growth-analyst**: Growth metrics analysis

---

## Documentation Structure

- `/docs/spec/` - Product specifications (WHAT to build)
- `/docs/impl/` - Implementation plans (HOW to build)
- `/docs/impl/completed/` - Archive of successfully deployed features
- `/docs/references/` - Technical reference docs
- `/docs/validation/` - Phase 1 validation results

---

## Quick Start

### For New Features
1. Run **spec-analyzer** to clarify requirements
2. Use **spec-writer** to document the spec
3. Use **impact-analyzer** to create delivery plan
4. Use **plan-writer** to document implementation
5. Use **git-strategist** + **git-steward** to set up branch/worktree
6. Use **code-implementer** to build (300 LOC max per step)
7. Run **test-runner** every 600 LOC
8. Use **code-reviewer** before and after tests
9. Use **pr-butler** to create PR
10. Merge and deploy

---

## Phase 1 Validation Results

Before building the full app, we validated:
- ✅ Tourist demand (landing page signups, surveys)
- ✅ Photographer willingness to work for social currency
- ✅ Instagram mention value
- ✅ Premium feature interest (revenue model)

Results stored in: `/docs/validation/phase1-results.md`

---

## Revision History
- v1.0.0 (2025-11-23) - Initial SnapSpot playbook creation
- Adapted from NexusDesk SDLC protocols
- Last Updated: 2025-11-23

---

**This playbook is the authoritative guide for all development work on SnapSpot. All agents and developers must follow these workflows and rules.**
