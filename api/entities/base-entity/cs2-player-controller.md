## cs2_player_controller

This type represents a `CCSPlayerController` class.

> This type inherits [`base_entity`](/api/entities/base-entity "This type represents a base game entity.") type. All of its base methods and fields are also available in this type.

## is_enemy

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if this player is an enemy to the local player.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if an enemy. |

**Example**

```lua
if player:is_enemy() then
    -- ...
end
```

## get_name

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the sanitized player name.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Player's name. |

**Example**

```lua
local name = player:get_name();
```

## get_pawn

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the pawn attached to this controller.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`cs2_player_pawn`](/api/entities/base-entity/cs2-player-pawn "This type represents a C_CSPlayerPawn class.") | Pawn instance. |

**Example**

```lua
local pawn = ctrl:get_pawn();
```

## get_active_weapon

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the active weapon.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`cs2_weapon_base_gun`](/api/entities/base-entity/cs2-weapon-base-gun "This type represents a CCSWeaponBaseGun class.") | Weapon instance. |

**Example**

```lua
local wep = player:get_active_weapon();
```

## get_observer_pawn

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the observer pawn used for this controller.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`base_entity`](/api/entities/base-entity "This type represents a base game entity.") | Entity. |

**Example**

```lua
local obs_pawn = ctrl:get_observer_pawn();
```

## get_observer_target

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the pawn this controller is currently observing.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`base_entity`](/api/entities/base-entity "This type represents a base game entity.") | Entity. |

**Example**

```lua
local obs = ctrl:get_observer_target();
```

## get_observer_mode

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the current observer mode.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`observer_mode_t`](/api/entities/observer-mode-t "This enum represents the observer modes available in the game.") | Observer mode. |

**Example**

```lua
local mode = ctrl:get_observer_mode();
```