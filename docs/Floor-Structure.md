# Floor Structure

Every floor presents a problem, opportunity, or decision.

## Encounter Types

| Type | Purpose |
| --- | --- |
| Combat | Standard fight and reward |
| Elite | Harder fight with stronger rewards |
| Treasure | Valuable loot with low combat pressure |
| Shop | Spend resources on useful options |
| Event | A choice with an uncertain outcome |
| Challenge | A special ruleset or objective |
| Rest | Recover and prepare for the next section |
| Mystery | An unusual or hidden interaction |
| Boss | Major progression milestone |

## Physical Route Selection

Ascend's first playable map uses physical exploration instead of requiring a separate node-map UI.

Each floor is assembled from handmade modular rooms. Players walk through the environment and choose which visible route to take.

Example:

```text
          START
            |
         Clearing
        /        \
    Combat      Event
       |           |
   Treasure      Elite
        \        /
          EXIT
```

The world itself communicates possible destinations through visual cues such as:

- Overgrown paths
- Glowing doorways
- Merchants under trees
- Strange locked doors
- Visible treasure areas
- Distinctive room entrances

The underlying run system can still use a graph to determine which rooms connect.

## Room Library

The first Garden vertical slice uses a small set of reusable handmade rooms.

```text
GardenRooms/
├── Entrance_01
├── Combat_01
├── Combat_02
├── Combat_03
├── Elite_01
├── Treasure_01
├── Event_01
├── Event_02
├── Shop_01
├── Rest_01
├── Secret_01
├── Exit_01
└── GardenerArena
```

Rooms should have a consistent gameplay contract while remaining visually distinct.

```text
Room
├── Entrance
├── Exit(s)
├── SpawnPoints
├── PlayerSpawn
├── Encounter
├── Reward
└── Environment
```

## The Garden

The first map is a 10-floor Garden.

### Floor 1 — The Clearing

Introductory combat and basic exploration.

### Floor 2 — The Fork

A meaningful physical route choice between different encounter types.

### Floor 3 — Overgrowth

Combat begins interacting more heavily with the Garden's environment.

### Floor 4 — Garden Shrine

An event-focused floor with unusual choices and discoveries.

### Floor 5 — Bloomkeeper

The first major elite encounter.

### Floor 6 — The Merchant

A controlled opportunity to spend resources and adjust the build.

### Floor 7 — The Forgotten Path

Stranger combat and older Garden elements.

### Floor 8 — Unknown

A secret or unusual event that depends on the run.

### Floor 9 — Heart of the Garden

A pre-boss floor where the state of the Garden can affect what happens next.

### Floor 10 — The Gardener

The Garden's first map boss.

## Garden Growth

The Garden can change as the player climbs.

The intended progression is:

```text
normal
  ↓
overgrown
  ↓
ancient
  ↓
living
  ↓
impossible
```

Individual rooms can change state based on player actions and the run's Growth level.

This lets a relatively small room library create different experiences without requiring hundreds of unique rooms.

## Pacing

Floors should alternate pressure and relief. The climb should have moments of danger, discovery, preparation, and payoff rather than being one continuous fight.
