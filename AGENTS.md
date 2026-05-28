# AI Development Rules

## Project Context

- This is a single-file HTML project.
- The main application lives in `index.html`.
- Gesture Drive v1.1 is the current stable version.
- Gesture Drive v1.2 should focus only on UI and experience upgrades.

## Editing Rules

- Do not split the project into multiple files by default.
- Before modifying the project, preserve the current runnable version first.
- Before the next round of UI work, preserve the current stable version first.
- Do not casually change the core gesture recognition logic.
- Do not touch the gesture core logic when doing UI-only iterations unless explicitly requested.
- Do not change existing DOM `id` values unless explicitly requested.
- Do not modify stable v1.1 behavior when preparing v1.2 UI or experience updates.
- Store background assets under `assets/backgrounds/`.
- Store future model assets under `assets/models/`.
- Store future texture assets under `assets/textures/`.

## Required Workflow

- Before changing code, read `README.md`, `CHANGELOG.md`, and `index.html`.
- After changing code, explain what changed.
- After changing code, explain how the change was tested or verified.
