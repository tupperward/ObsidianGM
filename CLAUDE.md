# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is an Obsidian vault for tabletop RPG game mastering. It contains campaign notes, adventure content, and a bestiary of creatures.

## Vault Structure

- **GameMastering/** - Campaign content and adventure notes (e.g., "Adventures in the Weird West")
- **z_Bestiary/** - Monster/creature entries organized by type (e.g., Artificials)
- **.obsidian/** - Obsidian configuration and plugins

## Installed Plugins

Key plugins that affect content format:
- **obsidian-5e-statblocks** - Renders creature statblocks using `\`\`\`statblock` code blocks
- **obsidian-dice-roller** - Dice notation support (e.g., `d4`, `Cd4`)
- **initiative-tracker** - Combat encounter management
- **rpg-manager** - Campaign organization
- **obsidian-leaflet-plugin** - Interactive maps
- **fantasy-content-generator** - Random content generation
- **obsidian-admonition** - Callout blocks
- **obsidian-excalidraw-plugin** - Drawings and diagrams

## Bestiary Entry Format

Creature entries follow this structure:
```markdown
*Size Type*

**HD**: X (Y HP)
**Speed:** X'
**Zone**: Position
**Morale:** X
**# Appearing:** dice
**Armor**: X [description]
**Immune**: damage types
**Status Immunities**: conditions

***ACTIONS***
---
Attack Name [Type]: modifier (damage)

***ABILITIES***
---
**Ability Name:** Description

\`\`\`statblock
dice: true
layout: Basic Fate Core Layout
name: Creature Name
creature: Creature Name
columns: 2
forceColumns: true
bestiary: true
\`\`\`
```

The statblock code block at the end triggers the 5e-statblocks plugin to render a formatted stat card.
