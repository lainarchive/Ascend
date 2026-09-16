# Technical Architecture

Ascend should stay modular from the beginning.

## Principles

- Server-authoritative gameplay
- Clear client/server separation
- Modular systems instead of giant scripts
- Validated RemoteEvents and RemoteFunctions
- Isolated persistence / DataStore code
- Reusable content definitions
- Clear ownership of game state

## Core Systems

Likely system boundaries include:

- Run management
- Floor generation
- Combat
- Enemies
- Abilities
- Items / rewards
- Build management
- Player progression
- Co-op / party state
- UI communication
- Persistence

Exact implementation is intentionally open until the prototype proves what the game actually needs.
