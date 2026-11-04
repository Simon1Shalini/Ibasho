# Ibasho — Build Tasks

A living checklist. Keep the next step small and update this file when something is completed or a decision changes.

## Current milestone: first browser-based room

### 0. Project setup
- [ ] Confirm the repository is cloned locally.
- [ ] Install and verify Node.js LTS.
- [ ] Install and verify Git.
- [ ] Open the project folder in VS Code.
- [ ] Create the initial Vite application.
- [ ] Add Three.js.
- [ ] Run the app locally and confirm it opens in a browser.

### 1. First 3D room
- [ ] Create a Three.js scene.
- [ ] Add a camera and renderer.
- [ ] Add basic lighting.
- [ ] Create floor, walls and ceiling.
- [ ] Add a simple fireplace-like focal point.
- [ ] Make the canvas resize correctly.
- [ ] Confirm the room works on the target desktop browser.

### 2. Make the room feel like a place
- [ ] Choose an initial visual direction.
- [ ] Add a small set of furniture and props.
- [ ] Improve materials, lighting and shadows.
- [ ] Add a few environmental details.
- [ ] Check asset licences and record asset sources.

### 3. Navigation and avatar
- [ ] Choose first-person, third-person or switchable camera.
- [ ] Add basic movement controls.
- [ ] Add a simple avatar representation.
- [ ] Add collision or movement boundaries.
- [ ] Test navigation and adjust speed and camera feel.

### 4. Simple interactions
- [ ] Define an interaction pattern.
- [ ] Add one interactable object.
- [ ] Add a sitting or resting interaction.
- [ ] Test interaction feedback and controls.

### 5. Multiplayer foundation
- [ ] Create a separate Node.js server.
- [ ] Add Socket.IO.
- [ ] Connect one browser client to the server.
- [ ] Show another connected participant.
- [ ] Synchronise movement.
- [ ] Handle disconnects and reconnects.
- [ ] Test with multiple browser windows.

### 6. Shared social experiences
- [ ] Add basic text chat.
- [ ] Decide how rooms or gatherings work.
- [ ] Prototype shared music or ambient audio.
- [ ] Define privacy and access expectations.
- [ ] Identify moderation needs before inviting external users.

### 7. Atmosphere and expansion
- [ ] Prototype a day/night cycle.
- [ ] Explore weather and ambient sound.
- [ ] Add a second room.
- [ ] Connect rooms through navigation.
- [ ] Explore voice commands for a small set of actions.

### 8. Deployment and reliability
- [ ] Deploy a basic static prototype.
- [ ] Choose a hosting option for the multiplayer server when needed.
- [ ] Document environment variables without committing secrets.
- [ ] Test reconnects and failure states.
- [ ] Review privacy, security and moderation before a wider release.

## Working rule

Work on one small task at a time. A task is complete only when it has been run and tested—not merely when code has been generated.
