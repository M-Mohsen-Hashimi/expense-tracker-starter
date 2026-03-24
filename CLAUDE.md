# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev       # Start development server (Vite)
npm run build     # Build for production
npm run lint      # Run ESLint
npm run preview   # Preview production build
```

No test framework is configured.

## Architecture

This is a React 19 + Vite single-page application. The entire app lives in `src/App.jsx` — there is no component decomposition. All state (transactions list, form inputs, active filters) is managed in a single component with `useState`.

**App.jsx responsibilities:**
- Hardcoded sample transaction data (initial state)
- Summary calculations (total income, total expenses, balance)
- Add-transaction form with fields: description, amount, type (income/expense), category
- Transactions table with filter controls (by type and category)

**Categories:** food, housing, utilities, transport, entertainment, salary, other

This project is a deliberately unstructured starter meant to be refactored — expect a large monolithic component rather than a well-organized component hierarchy.
