# Context Engineering

## Overview
Fine-tune how agents assemble their prompts using **policies**.

## Policy Editor
- **Slots** — Logical sections of context (e.g., system, history, documents).
- **Weights** — Relative importance of each slot.
- **Gates** — Rules for including/excluding a slot.
- **Budgets** — Character/token limits per slot.

## Assembly Preview
Enter a query to see the assembled prompt and per-slot statistics.

## Saving Policies
Changes are saved to `/api/policy/{policy_id}` and used in production runs.
