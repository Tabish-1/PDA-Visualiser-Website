# PDA Visualiser

An interactive web application for visualizing and simulating Pushdown Automata (PDAs). Built with Next.js and TypeScript.

## Features

- Canvas-based state diagram with animated transitions
- Real-time stack visualization showing push and pop operations
- Input tape display with read head tracking
- Step-through simulation with a detailed log of each transition
- Pre-loaded examples for common PDA languages
- Auto-generate a PDA from a natural language description
- Fully manual configuration for states, alphabets, and transitions
- Dark and light theme toggle
- Keyboard shortcuts for simulation controls

## Tech Stack

- Next.js 16 (App Router)
- TypeScript
- Tailwind CSS
- HTML5 Canvas API

## Getting Started

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## How to Use

**Using the pre-loaded examples (quickest)**

Click any example card in the left sidebar — Balanced Parentheses, aⁿbⁿ, or wcwᴿ Palindrome. Enter a test string and click Play.

**Auto-generate from a description**

Type a description into the Quick Builder (e.g. "balanced parentheses") and click Auto-Generate. The PDA is configured automatically.

**Manual configuration**

1. Define states in the Configuration panel — use `*` to mark accept states (e.g. `q0, q1, q2*`)
2. Set the input and stack alphabets
3. Add transitions using the transition form
4. Enter a test string and click Play

## Transitions

Each transition follows the form:

```
δ(from_state, read_symbol, pop_symbol) → (to_state, push_symbols)
```

Use `ε` for epsilon — to take a transition without consuming input, without popping from the stack, or without pushing to the stack.

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| Space | Step forward |
| P | Play / Pause |
| R | Reset |

## Project Structure

```
pda-main/
├── app/            # Next.js app router pages and layout
├── components/     # UI components
├── engine/         # PDA simulation logic
├── types/          # TypeScript type definitions
└── utils/          # Helper functions
```
