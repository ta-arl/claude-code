# Migration Guide for Pending Features

This document outlines the changes introduced by open pull requests that are pending merge. Review this guide to understand upcoming features and any necessary migration steps.

## PR #53: 【Feat】Automate Docker Image Builds with GitHub Actions

### Summary of Changes
This PR introduces a new GitHub Actions workflow to automate Docker image builds. The workflow triggers automatically on branch updates, ensuring the Docker image stays synchronized with the latest code.

### Key Features
- **New Workflow File**: Adds a `.github/workflows/docker-build.yml` (or similar) GitHub Actions workflow.
- **Automated Triggers**: Runs on `push` events to the branch, providing continuous integration for Docker image creation.
- **Based on Templates**: Leverages existing GitHub Action templates for Docker builds, following best practices.

### Configuration / Environment Variables
No new environment variables are mentioned. The workflow uses standard GitHub Actions environment and secrets (e.g., `DOCKER_REGISTRY`, `DOCKER_USERNAME`, `DOCKER_PASSWORD`) if configured.

### Installation / Usage Instructions
1. Merge the PR.
2. Ensure Docker configuration (Dockerfile) exists in the repository.
3. The workflow will automatically run on subsequent pushes to the branch.
4. Monitor the GitHub Actions tab for build status.

### Notes
- This workflow improves reliability by catching build issues early.
- Reduces manual effort for Docker image builds.
- Provides faster feedback on Docker build status.

---

## PR #52: feat: add shell completions (bash, zsh, fish)

### Summary of Changes
Adds static shell completion scripts for Bash, Zsh, and Fish shells, enabling tab autocompletion for the Claude Code CLI.

### Key Features
- **Completion Scripts**: Adds three files under `shell-completions/`:
  - `claude-completions.bash`
  - `claude-completions.zsh`
  - `claude-completions.fish`
- **Manual Sourcing**: Users must manually source the appropriate script since upstream integration is not possible (the client is not open source).

### Configuration / Environment Variables
None required.

### Installation / Usage Instructions
1. Merge the PR.
2. For Bash users: `source shell-completions/claude-completions.bash`
3. For Zsh users: `source shell-completions/claude-completions.zsh`
4. For Fish users: `source shell-completions/claude-completions.fish`
5. To make persistent, add the sourcing command to your shell's profile file (`.bashrc`, `.zshrc`, `config.fish`).

### Notes
- Ideal solution would be integrated completions via `claude completion $SHELL`, but not possible due to closed-source client.
- These static scripts provide a workaround for better user experience.

---

## PR #51: Enhance Statsig event logging in GitHub workflows

### Summary of Changes
Enhances Statsig event logging in GitHub workflows by adding events for issue management, specifically when issues are closed as duplicates and when duplicate comments are added.

### Key Features
- **Additional Events**: Logs extra events for duplicate issue closure and duplicate comment addition.
- **Consistency**: Ensures logging patterns align with existing workflows.

### Configuration / Environment Variables
No new environment variables mentioned. Assumes Statsig integration is already configured.

### Installation / Usage Instructions
1. Merge the PR.
2. Existing GitHub workflows will automatically log the additional events.
3. No user action required.

### Notes
- Generated with Claude Code.
- Maintains consistency with existing logging patterns.
- Helps improve analytics around issue management.

---

## General Migration Notes
- These PRs are independent and can be merged in any order.
- No breaking changes are introduced.
- All PRs are from forks and have been automatically mirrored.
- Review each PR's diff for specific file changes.