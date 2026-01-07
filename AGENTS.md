# Agent Guide for PyLoxone (Home Assistant Loxone Binding)

This repository contains a Home Assistant integration that binds to the **Loxone Miniserver**. Use this guide when implementing new features, fixing bugs, or extending the binding.

## Documentation
- Loxone Miniserver API reference: https://www.loxone.com/wp-content/uploads/datasheets/CommunicatingWithMiniserver.pdf
- Structure-File (LoxAPP3.json) reference: https://www.loxone.com/wp-content/uploads/datasheets/StructureFile.pdf

## Coding Style
- **Python style**: follow `ruff.toml` for linting/formatting rules.
- **Typing**: prefer explicit type hints for public functions and complex data structures.
- **Async first**: Home Assistant integrations are async; prefer `async def` APIs and `await` IO operations.
- **Naming**: keep entity/platform naming consistent with existing files in `custom_components/loxone`.
- **Logging**: use the module logger via `logging.getLogger(__name__)`; do not use `print`.
- **Config flow**: when adding new configuration options, update config flow and translations together.
- **Home Assistant conventions**: follow patterns in this repo for coordinators, entities, and data updates.

## Contribution Tips
- Keep changes focused to the Loxone binding under `custom_components/loxone` unless the change is repo-wide.
- Update or add tests if the repo has coverage for the area you change.
- If you introduce a new API call or endpoint, document it in code comments and ensure error handling matches existing patterns.
