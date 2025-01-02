## events_t

Usage: `mods.events.{method}`

This module lets you manage custom in-game event listener.

> Please note that the game server **knows** which events you are listening to. Internally, we only listen to events that will get sent to the client anyway in one way or another. If you decide to listen to something the server generally does not expect, it **may** cause issues on official servers.

## add_listener

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a game event to the listener.

> Internally we listen to the following events:
> * `player_hurt`
> * `item_purchase`
> * `bullet_impact`
> * `weapon_fire`
> * `bomb_beginplant`
> * `bomb_abortplant`
> * `bomb_planted`
> * `bomb_defused`
> * `bomb_exploded`
> * `round_start`
> * `game_newmap`
> * `map_shutdown`
>
> Adding those events to the listener is not needed.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `name` | `string` | Event name. |

**Returns**

Nothing.

**Example**

```lua
mods.events:add_listener('round_end');
```