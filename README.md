# mtoolbox

A single-file Bash CLI for managing and updating milvasic tools, plus a static discovery page hosted on GitHub Pages.

**Live:** https://milvasic.github.io/mtoolbox/

## Install

```sh
bash -c "$(curl -fsSL https://raw.githubusercontent.com/milvasic/mtoolbox/refs/heads/main/install.sh)"
```

## Usage

```
mtoolbox <command> [tools...] [--yes] [--refresh]

Commands:
  list                 List all catalog tools with installed/version status
  install <tools..>    Install one or more tools from the catalog
  update               Check installed tools for available upgrades (read-only)
  upgrade [tools..]    Apply upgrades (all outdated, or named subset)
  refresh              Force-refresh manifest cache
  version, --version   Print mtoolbox version
  help, --help         Show help

Options:
  --yes, -y            CI-friendly, skip prompts
  --refresh            Bypass cache for this invocation
```

### Examples

```sh
# See which tools are installed and their versions
mtoolbox list

# Install tools from the catalog
mtoolbox install mcli motd

# Check for available updates (read-only)
mtoolbox update

# Upgrade all outdated tools
mtoolbox upgrade

# Upgrade a specific tool
mtoolbox upgrade mcli

# Self-upgrade mtoolbox
mtoolbox upgrade mtoolbox

# Force-refresh the manifest cache
mtoolbox refresh
```

## Tools

| Tool | Description |
|------|-------------|
| [diffcheck](https://github.com/milvasic/diffcheck) | A .NET 10 tool for comparing CSV and XLSX files with color-coded HTML diff reports. |
| [motd](https://github.com/milvasic/motd) | A single-file Bash script that displays a system information dashboard at login. |
| [mcli](https://github.com/milvasic/mcli) | A single-file Bash CLI for managing Docker Compose services. |
| [tinit](https://github.com/milvasic/tinit) | A single-file Bash CLI that sets up a Debian/Ubuntu terminal environment from scratch. |
| [distill](https://github.com/milvasic/distill) | A single-file Bash CLI that generates a self-contained install.sh for any CLI tool. |
| [syskeeper](https://github.com/milvasic/syskeeper) | Coming soon. |

## How to add a new tool

1. **Add an entry to `index.html`** — copy an existing `<li class="tool-card">` block and update the tool name, description, and GitHub repo URL.
2. **Add a row to the table in this README** — follow the existing format.
3. Commit, push, and open a PR. GitHub Pages redeploys automatically on merge to `main`.

Keep descriptions to a single sentence derived from the tool's own README.
