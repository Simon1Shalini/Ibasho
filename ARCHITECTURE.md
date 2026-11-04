# Architecture

## 1. Status

This document records the current proposed architecture for Ibasho. It is intentionally lightweight. Treat choices as hypotheses until they are implemented and tested.

## 2. Initial technology direction

| Area | Proposed technology | Purpose |
|---|---|---|
| 3D rendering | Three.js | Render the world in the browser |
| Frontend tooling | Vite | Local development server and production build |
| Main language | JavaScript initially | Learn and build the first prototype |
| Multiplayer transport | Socket.IO | Exchange real-time events between connected users |
| Backend runtime | Node.js | Run the multiplayer server when needed |
| Version control | Git and GitHub | Track changes, collaborate and preserve project history |
| 3D assets | Self-made or openly licensed assets | Populate the world while respecting licences |

These are starting choices, not requirements. Reassess them when implementation reveals a concrete limitation.

## 3. High-level system shape

### First prototype

The first prototype should be a client-only browser application:

1. The browser loads the app built with Vite.
2. Three.js creates the scene, camera, renderer, lights and objects.
3. The user explores a single room.
4. No account system, database or multiplayer server is required yet.

### Later multiplayer version

When the single-player experience is stable:

1. A Node.js server runs the shared session logic.
2. Clients connect to the server through Socket.IO.
3. The server distributes relevant presence and movement updates.
4. Clients render other participants in the same world.
5. Server-side validation is added for actions that should not be trusted to a client.

Do not assume that Socket.IO alone solves persistence, security, moderation or scaling. Those require separate design decisions.

## 4. Suggested project structure

The structure can evolve. Keep the first implementation small rather than creating empty folders for every future feature.

```text
ibasho/
├── index.html
├── package.json
├── vite.config.js
├── README.md
├── PROJECT.md
├── ARCHITECTURE.md
├── TASKS.md
├── AI_CONTEXT.md
├── src/
│   ├── main.js
│   ├── world/
│   │   ├── createScene.js
│   │   └── createRoom.js
│   ├── controls/
│   └── styles/
├── public/
│   └── assets/
└── server/              # Add when multiplayer work begins
```

Only add files and folders when they are needed.

## 5. Development sequence

### Phase A — Local 3D room
- Set up Node.js, Git and a code editor.
- Create a Vite project.
- Add Three.js.
- Render a room with a camera, lights and a few simple objects.
- Keep the scene responsive to browser resizing.

### Phase B — Atmosphere and navigation
- Add materials, furniture and environment details.
- Add camera controls.
- Add a simple avatar and movement.
- Test collisions and basic navigation.

### Phase C — Interactions
- Add simple interactable objects.
- Add sitting or other small actions.
- Connect rooms only after navigation in one room works.

### Phase D — Multiplayer
- Create a Node.js server.
- Add Socket.IO connections and shared presence.
- Synchronise player positions at a sensible update rate.
- Handle disconnects and reconnects.
- Validate important actions on the server.

### Phase E — Social experience
- Add text chat and room-level interactions.
- Explore shared audio.
- Consider voice only after privacy, permissions and technical costs are understood.

### Phase F — Persistence and expansion
- Decide what world state needs to persist.
- Choose storage based on actual requirements.
- Add more rooms and environmental changes.
- Design access controls, moderation and reporting before public access.

## 6. Important engineering principles

- Keep rendering, controls, world objects and network logic separate as the project grows.
- Avoid putting the entire application in one large file.
- Use small changes that can be tested independently.
- Keep secrets and API keys out of the repository. Use environment variables for local secrets and hosting configuration for deployed secrets.
- Never trust client-submitted positions, ownership or economy actions without server-side validation.
- Minimise personal data collection.
- Do not add accounts or persistent identity until there is a clear need.
- Document asset sources and licences.
- Test in the browser after every meaningful change.

## 7. Hosting and cost

The first version should run locally and does not need hosting.

A static frontend may later be deployable on a free or low-cost static hosting tier. A persistent multiplayer server has different requirements and may not fit static hosting. Free-tier limits and provider terms change, so compare current options when deployment becomes necessary.

Do not choose a database or pay for infrastructure before the prototype needs persistence or multiplayer.

## 8. Decisions to revisit

- JavaScript versus TypeScript.
- First-person versus third-person camera.
- Avatar representation and animation system.
- Client prediction and network interpolation.
- Persistence model and database.
- Hosting provider and expected concurrent users.
- Voice technology and privacy model.
- Moderation, abuse prevention and access controls.
