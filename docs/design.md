# Dungeon Crawler — Design Doc

## One-line pitch
A player explores a small dungeon, fights enemies in real-time combat,
finds a key, and unlocks the exit door to win.

## Locked scope (MVP)

### Player
- Top-down view
- Moves with WASD or arrow keys
- Has HP
- One attack: melee swing (spacebar or left-click), hits enemies in front

### World
- Three rooms connected by doorways
- Hand-designed, not procedurally generated
- Walls block movement

### Enemies
- One enemy type
- Walks toward player, deals contact damage
- Three of them total across the dungeon

### Progression
- One key item, picked up by walking over it
- One locked door, opens when player has the key
- Walking through unlocked door triggers win screen

### Screens
- Title screen: game name + Start button
- Win screen: "You escaped" + Restart button
- Lose screen: "You died" + Restart button

### Audio
- One attack sound
- One hit sound
- One pickup sound
- One background music loop

## Out of scope (do not add)
- Inventory
- Multiple weapons
- Leveling up
- Save system
- Multiple floors
- Story / NPCs / shops
- Options menu beyond start/restart
- Original art (use Kenney.nl assets)

## Team
- Tanmoy (gameplay programmer): player, enemy AI, combat, win/lose, repo, builds
- Raad (world & systems): rooms/tilemap, door/key logic, UI, sound, asset sourcing

## Milestones
- Week 1: Project setup, player moves on screen
- Week 2: Player attack, enemy walks toward player, damage works
- Week 3: One full room with collision-blocking walls (tilemap)
- Week 4: Three connected rooms, key pickup, locked door opens
- Week 5: Title/win/lose screens, HP bar, sound effects
- Week 6: Bug fixing, music, export to HTML5, upload to itch.io

## Engine
Godot 4.6.2, Compatibility renderer (for clean HTML5 export)
