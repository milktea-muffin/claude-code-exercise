# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build & Run Commands

- **Run the app:** `uv run python main.py`
- **Sync dependencies:** `uv sync` (or `make sync`)
- **Add a dependency:** `uv add <package>`
- **Add a dev dependency:** `uv add --dev <package>`
- **Lint:** `make lint` (runs `ruff check .`)
- **Format:** `make format` (runs `ruff format .`)
- **Type check:** `make type-check` (runs `mypy .`)
- **Install dev tools (ruff, mypy):** `make dev-tools`

## Project Overview

Fresh Python 3.13 project using **uv** for package/environment management. Entry point is `main.py`. Dependencies are defined in `pyproject.toml` and locked in `uv.lock`.
