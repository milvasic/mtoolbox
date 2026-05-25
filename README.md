# mtoolbox

A static discovery page for all [milvasic](https://github.com/milvasic) CLI tools, hosted on GitHub Pages.

**Live:** https://milvasic.github.io/mtoolbox/

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
