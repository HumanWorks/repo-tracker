# Git Repos Collection

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## About This Project

This is an intelligent repository tracking system that helps you monitor and organize any Git repositories you find interesting. 

### What it does

This project serves as a personal collection and monitoring system for Git repositories. It automatically:

- **Tracks and organizes** any repositories you want to follow
- **Monitors changes** across all tracked repositories with a single command
- **Maintains descriptions** of each repository's purpose and capabilities
- **Prevents duplicates** by checking URLs before adding new repos
- **Provides easy management** through natural language commands

### Why it's useful

With thousands of open source projects evolving daily on GitHub, it's challenging to keep track of the ones that matter to you. This tracker helps you:

- Build a curated collection of repositories you find interesting
- Stay informed about updates and new features across multiple projects
- Maintain a personal library of tools, libraries, and resources
- Quickly understand what each repository does without visiting each one individually
- Check for updates across all your tracked repos with a simple "hi"

### Perfect for

- Developers who want to track their favorite open source projects
- Teams monitoring dependencies and tools they use
- Anyone collecting interesting repositories for future reference
- Researchers following developments across multiple projects

## Prerequisites

- [Claude Code](https://claude.ai/code) - This tool is designed to work with Claude Code's AI assistant
- Git installed on your system
- A GitHub account (for cloning repositories)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/git-repos-collection.git
   cd git-repos-collection
   ```

2. Open the project in Claude Code
   ```bash
   claude
   ```

3. Start using natural language commands to manage your repository collection!

## Quick Start

1. **Add your first repository:**
   ```
   "Add https://github.com/facebook/react"
   ```

2. **Check for updates:**
   ```
   "Hi" or "Check for updates"
   ```

3. **View your collection:**
   ```
   "Which repos do you track?"
   ```

## How to use

### Commands

- **Add a repository**: Simply provide a GitHub URL like `https://github.com/username/repo`
  - The tool will clone the repo, analyze it, and add it to the collection
  - Duplicate repos are automatically detected and prevented

- **Check for updates**: Just say "hi" or ask to check for updates
  - All tracked repositories will be pulled for latest changes
  - You'll get a summary of what changed in each repo

- **Delete a repository**: Ask to delete a repo by name or URL
  - The tool will confirm which repo you mean
  - Removes both the local clone and the tracking entry

- **List repositories**: Ask "which repos do you track?"
  - Shows all currently tracked repositories with their descriptions

### Automatic behavior

When you greet the tool (say "hi"), it automatically checks all repositories for updates and reports any changes.

## How it Works

### Storage Structure

The system maintains two separate files:

- **README.md** (this file) - Contains the documentation and instructions for using the system
- **REPOS.md** (git-ignored) - Contains your personal collection of tracked repositories

The repository list is kept in REPOS.md which is not tracked by git, meaning:
- Your personal repository collection stays local to your machine
- You can share the tracking system without sharing your specific tracked repos
- Each user maintains their own unique collection

### Local Repository Management

When you add a repository:
1. The system clones it into a local directory (e.g., `react/`)
2. It reads the repository's README to understand its purpose
3. It adds an entry to REPOS.md with the repository details
4. These cloned directories are also git-ignored to keep your workspace clean

This design keeps the tracking system itself separate from the repositories being tracked, making it easy to maintain and share the tool while keeping your collection private.

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details on how to get started.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a list of changes and version history.

## Support

If you encounter any issues or have questions, please [open an issue](https://github.com/yourusername/git-repos-collection/issues) on GitHub.
