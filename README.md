# OtterLife Translator Skill

This repository contains the `otterlife-translator` skill for Trae, designed to automate the localization of OtterLife app metadata.

## Skill Description

**Name**: `otterlife-translator`

**Function**: Automates translation of "OtterLife" app metadata and release notes with specific formatting rules (no newlines) and supported locales.

**Usage**: Invoke when asked to translate or update OtterLife metadata.

## Installation

### For Trae (Recommended)

1. Clone this repository into your `.trae/skills/` directory:
   ```bash
   mkdir -p .trae/skills/otterlife-translator
   git clone https://github.com/ryohgicc/otterlife-translator-skill.git .trae/skills/otterlife-translator
   ```
2. The skill will be automatically recognized. You can invoke it by saying:
   > "Translate this release note using otterlife-translator..."

### For Claude Code (Anthropic CLI)

Claude Code can read and follow the instructions in `SKILL.md` as context.

1. Clone or copy the `SKILL.md` file into your project (e.g., in `docs/skills/`).
2. When asking Claude to translate, explicitly reference the file:
   > "Please translate this text following the rules in `docs/skills/otterlife-translator/SKILL.md`..."

### For Cursor

1. Add the content of `SKILL.md` (or a reference to it) to your `.cursorrules` file.
2. Example rule:
   > "When asked to translate OtterLife metadata, always follow the guidelines in `.trae/skills/otterlife-translator/SKILL.md`."

## Features

- **Dynamic Locale Support**: Automatically detects supported languages from App Store Connect.
- **Formatted Release Notes**: Supports bullet points and newlines (using ANSI-C quoting `$'...'`) for clean, list-style display in App Store.
- **Variable Protection**: Preserves variables like `{{name}}` during translation.
- **Brand Consistency**: Keeps "OtterLife" brand name consistent across languages.
