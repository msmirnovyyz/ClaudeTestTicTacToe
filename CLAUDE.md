# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Single-file browser Tic Tac Toe game. No build tools, no dependencies, no package manager.

## Running

Open `index.html` directly in a browser:
```
start chrome c:\VSCode\ClaudeTestTicTacToe\index.html
```

## GitHub

- Repo: https://github.com/msmirnovyyz/ClaudeTestTicTacToe
- Push via git with token embedded in remote URL (no gh CLI)
- Branch: `main`
- After every change: commit and push to GitHub

## Architecture

Everything lives in `index.html` as a single file with inline `<style>` and `<script>` blocks:

- **Board state**: flat 9-element array (`board[]`), indexed 0–8 left-to-right, top-to-bottom
- **Win detection**: checks 8 hardcoded winning combos (`WINS`) against the board array
- **Score tracking**: in-memory `scores` object `{ X, O, Draw }`, resets on page reload
- **No frameworks**: plain DOM manipulation, `querySelectorAll`, `addEventListener`
