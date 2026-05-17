# VS Code Settings for Debian Linux

![Status](https://img.shields.io/badge/Status-Configured-success)
![Platform](https://img.shields.io/badge/Platform-VS%20Code-blue)
![Focus](https://img.shields.io/badge/Focus-Editor%20Customization%20%7C%20Productivity%20%7C%20Docs-orange)
![Profile](https://img.shields.io/badge/Profile-Linux%20%7C%20zsh%20%7C%20Dark%20Workflow-lightgrey)

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Configuration Overview](#configuration-overview)
4. [System-Specific Values](#system-specific-values)
5. [Required Tools and Extensions](#required-tools-and-extensions)
6. [Markdown Linting](#markdown-linting)
7. [Setup Guide](#setup-guide)
8. [Testing](#testing)
9. [Customization Notes](#customization-notes)
10. [Author](#author)

---

## Project Overview

This repository packages an opinionated VS Code configuration for a Debian-based Linux workflow. The setup is tuned for predictable editing, quiet visuals, and a terminal-first routine while staying easy to review, fork, and adapt.

## Objectives

- Keep the editor focused on readable, low-noise work.
- Make terminal behavior consistent across sessions.
- Preserve a clean dark interface with targeted visual adjustments.
- Reduce watcher, search, and recommendation noise.
- Keep language-specific formatting rules explicit and maintainable.

## Configuration Overview

### Search and files

Reduces noise from generated folders and keeps the workspace tree focused.

### Editor

Sets typography, cursor behavior, suggestions, wrapping, scroll feel, bracket guides, sticky scroll, minimap, and line highlighting.

### Terminal

Makes the integrated shell predictable with zsh, custom fonts, cursor settings, scrollback, and paste behavior.

### Workbench

Controls theme, icons, tree spacing, startup view, header actions, and secondary side bar visibility.

### Window

Keeps the chrome compact and centered on the active project.

### Explorer

Makes delete, drag-and-drop, and decoration behavior explicit.

### Diff editor

Keeps comparisons readable and stable across large changes.

### Git

Tunes smart commit, autofetch, sync prompts, and decorations.

### Extensions

Disables automatic update churn and recommendation noise.

### Telemetry

Keeps usage reporting off.

### Python

Auto-activates the current environment in the terminal.

### Colorize

Highlights known color-like values inline while editing.

### Markdown linting

Uses a relaxed technical-doc profile for long-form Markdown.

### Language overrides

Applies language-specific formatter and wrapping behavior for Markdown, JSON, and JSONC.

### Color customizations

Applies the dark palette and UI accents that define the visual style.

## System-Specific Values

These settings depend on the local machine and should be reviewed before reuse.

### Fonts

```json
"editor.fontFamily": "FiraCode Nerd Font"
"terminal.integrated.fontFamily": "FiraMono Nerd Font Mono"
```

### Shell path

```json
"terminal.integrated.profiles.linux": {
  "zsh": {
    "path": "/usr/bin/zsh",
    "args": ["-l"]
  }
}
```

### External terminal

```json
"terminal.external.linuxExec": "xfce4-terminal"
```

## Required Tools and Extensions

This configuration assumes the following tools and extensions are available:

- GitHub Dark Default theme
- material-icon-theme
- Prettier
- Markdownlint
- zsh
- Nerd Fonts

## Markdown Linting

The Markdown profile is intentionally relaxed for technical documentation. It keeps structure checks useful while avoiding rules that tend to fight README files, prompts, and engineering notes.

## Setup Guide

Copy the JSON content into `~/.config/Code/User/settings.json` and reload VS Code.

## Testing

- Open VS Code and confirm the editor theme, font, and cursor behavior match the intended setup.
- Verify the integrated terminal uses the expected shell and font.
- Check that Markdown files use the relaxed language override.
- Confirm the diff editor and minimap settings behave as expected on a real workspace.

## Customization Notes

Review fonts, shell paths, and desktop-specific values before adapting this configuration to another environment. If you do not use the same Linux desktop or terminal, update the machine-specific values first.

## Author

**Developed by [@dev-mikel](https://github.com/dev-mikel)**
**License**  MIT
