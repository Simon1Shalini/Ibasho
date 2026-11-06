# AI Collaboration Context — Ibasho

This file is the shared briefing for any AI assistant helping with Ibasho. Read it before proposing changes.

## Project in one paragraph

Ibasho is a browser-based virtual social world inspired by the Japanese word 居場所 (ibasho), meaning a place where someone feels they belong. It begins as one welcoming palace or villa with rooms for reading, music, creativity and gathering. People may later enter as avatars, explore together, talk, listen to music and host gatherings. The longer-term idea is a community-created village or society with homes, gardens, farming, exchange and shared spaces.

## The creator's goals

- Build a real product from the ground up while learning how the technology works.
- Use AI as a tutor, coding partner and independent reviewer.
- Keep the initial prototype free or close to zero-cost.
- Retain ownership of product decisions, source code and project direction.
- Move in small, understandable steps rather than accepting large unexplained code drops.
- Document the making process and potentially share progress publicly later.

## Current technical direction

- Three.js for browser 3D.
- Vite for frontend tooling.
- JavaScript initially.
- Node.js and Socket.IO later for multiplayer.
- GitHub for the shared source of truth.
- Prefer free/openly licensed assets and verify their licences.

These choices are provisional. Do not change the stack casually; explain the reason and trade-offs before recommending a change.

## Product priorities

Build in this order:

1. One small room that loads in a browser.
2. Atmosphere: lighting, materials and a fireplace-like focal point.
3. Avatar and movement.
4. Small object interactions.
5. Multiplayer presence and movement.
6. Chat and shared experiences.
7. Environmental changes and additional rooms.
8. Persistence, community systems and any economy.

Do not start with a large map, virtual currency, marketplace or complex society simulation.

## How to work with the creator

- Explain unfamiliar terms in plain language.
- Give a short sequence of steps, ideally one manageable step at a time.
- Explain what a command or code change does before asking the creator to run it.
- When providing code, state the file path and whether it is new or replacing existing content.
- Prefer small changes that can be run and tested immediately.
- Do not assume a command succeeded. Ask for or inspect the actual output.
- When debugging, identify the likely cause and explain how to verify it.
- Distinguish facts, assumptions, recommendations and open questions.
- Be constructive and candid. Do not agree merely to be encouraging.
- Do not introduce paid services or APIs without explaining why they are needed and offering a free or lower-cost alternative where practical.
- Never ask the creator to paste passwords, personal access tokens or API secrets into chat.

## Claude's addition — who does what

- **ChatGPT** builds: it writes and explains code.
- **Claude** reviews and advises; it does not build unless asked.
- Text added by Claude sits under a heading beginning "Claude's addition", and by ChatGPT under "ChatGPT's addition". Commit messages start with [Claude] or [ChatGPT]. The creator decides what stays.

## Collaboration between AI assistants

- GitHub is the source of truth; chat history is not the only record.
- One assistant may propose or implement a change while another independently reviews it.
- Do not have two assistants modify the same files simultaneously.
- Before editing, inspect the current files and preserve existing work.
- Summarise changed files, important decisions, commands run and tests performed.
- Never claim code was tested unless it was actually run.
- Use separate branches or pull requests for substantial competing implementations.
- The creator makes final product and architecture decisions.

## Repository conventions

- Keep documentation current when decisions change.
- Record significant trade-offs in DECISIONS.md if/when that file is added.
- Keep tasks in TASKS.md small and verifiable.
- Keep secrets out of version control.
- Cite asset sources and licences in the project when assets are added.
- Avoid unnecessary dependencies.

## Open product questions

- Visual style: realistic, stylised, whimsical or hybrid?
- Camera: third-person, first-person or switchable?
- What should the first room feel like?
- What is the smallest useful social interaction?
- How should invite-only and public spaces differ?
- What safety and moderation controls are needed before inviting others?
