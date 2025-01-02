## entities

This table represents an internal entity list.

> Never store any entities in the global scope! Any entity might get deleted, and you will no longer have a valid instance of that entity, which will inevitably lead to a crash. If you need to globally store an entity somewhere, we strongly recommend you store an instance of [`chandle`](https://lua.fatality.win/chandle.html "This type represents an entity handle"), and use it's [`get`](https://lua.fatality.win/chandle.html#get "Returns the entity, or nil if nothing found.") method to retrieve the entity again, when needed.

## players

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`entity_list_t<cs2_player_pawn>`](https://lua.fatality.win/entity-list-t.html "This type represents and entity list.")

Player pawns.

## controllers

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`entity_list_t<cs2_player_controller>`](https://lua.fatality.win/entity-list-t.html "This type represents an entity list.")

Player controllers.

## items

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`entity_list_t<cs2_weapon_base>`](https://lua.fatality.win/entity-list-t.html "This type represents an entity list.")

Items (held).

## dropped_items

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`entity_list_t<cs2_weapon_base>`](https://lua.fatality.win/entity-list-t.html "This type represents an entity list.")

Dropped items.

## projectiles

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`entity_list_t<cs2_grenade_projectile>`](https://lua.fatality.win/entity-list-t.html "This type represents an entity list.")

Grenade projectiles.

## get_local_pawn

[![Function][This is a regular function that must be called using a dot (.).]rw]

Returns the local player's pawn.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`cs2_player_pawn`](https://lua.fatality.win/cs2-player-pawn.html "This type represents a C_CSPlayerPawn class.") | Pawn. |

**Example**

```lua
local lp = entities.get_local_pawn();
```

## get_local_controller

[![Function][This is a regular function that must be called using a dot (.).]rw]

Returns the local player's controller.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`cs2_player_controller`](https://lua.fatality.win/cs2-player-controller.html "This type represents a CCSPlayerController class") | Controller. |

**Example**

```lua
local lp_ctrl = entities.get_local_controller();
```