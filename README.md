# OtterLife Translator Skill

This repository contains the `otterlife-translator` skill for Trae, designed to automate the localization of OtterLife app metadata.

## Skill Description

**Name**: `otterlife-translator`

**Function**: Automates translation of "OtterLife" app metadata and release notes with specific formatting rules (no newlines) and supported locales.

**Usage**: Invoke when asked to translate or update OtterLife metadata.

## Installation

1. Clone this repository into your `.trae/skills/` directory (or manually copy the `otterlife-translator` folder).
2. Ensure the directory structure is `.trae/skills/otterlife-translator/SKILL.md`.

## Features

- **Dynamic Locale Support**: Automatically detects supported languages from App Store Connect.
- **Strict Formatting**: Ensures no newlines (`\n`) in output, suitable for App Store "What's New" fields.
- **Variable Protection**: Preserves variables like `{{name}}` during translation.
- **Brand Consistency**: Keeps "OtterLife" brand name consistent across languages.
