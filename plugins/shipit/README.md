# shipit

Quick commit and push for Claude Code - analyze changes, generate commit message, commit, and push in one command.

## Prerequisites

Before installing, ensure you have:

- **Claude Code** installed and working ([installation guide](https://docs.anthropic.com/en/docs/claude-code))
- **Git** configured with your identity:
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  ```
- A **git repository** with a remote configured (e.g., GitHub, GitLab)

## Installation

### Option 1: Via Claude Code (Recommended)

Run this command in Claude Code:

```
/plugin install github:1-Martian-Way/shipit
```

### Option 2: Manual Installation

Clone directly to your Claude Code plugins directory:

```bash
git clone https://github.com/1-Martian-Way/shipit.git ~/.claude/plugins/shipit
```

### Verify Installation

After installing, run in Claude Code:

```
/shipit
```

If installed correctly, Claude will analyze your changes (or tell you there's nothing to commit).

## Usage

```
/shipit
```

That's it! Claude will:
1. Check for changes
2. Analyze the diff
3. Generate a commit message (conventional commits format)
4. Stage, commit with co-author attribution, and push

## Example Output

```
Committed and pushed to main:

  refactor: simplify PM2 restart by delegating to pm2.sh

  - Changed build-prod.sh to call ./pm2.sh instead of inline restart
```

## Why shipit?

- **One command** - No more `git add`, `git commit -m "..."`, `git push`
- **Smart messages** - AI-generated commit messages following conventional commits
- **Attribution** - Automatic co-author credit for Claude

## Compatibility

- Works with any git repository (GitHub, GitLab, Bitbucket, etc.)
- Supported platforms: macOS, Linux, Windows (anywhere Claude Code runs)

## Uninstall

Remove the plugin by deleting its directory:

```bash
rm -rf ~/.claude/plugins/shipit
```

## Contributing

Found a bug or have a suggestion? [Open an issue](https://github.com/1-Martian-Way/shipit/issues) on GitHub.

## License

MIT
