## cs2_player_pawn

This type represents a `C_CSPlayerPawn` class.

> This type inherits [`base_entity`](/api/entities/base-entity "This type represents a base game entity.") type. All of its base methods and fields are also available in this type.

## should_draw

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the game will draw this player on screen.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if will. |

**Example**

```lua
if player:should_draw() then
    -- ...
end
```

## is_left_handed

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if left-hand mode is enabled.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if left-handed. |

**Example**

```lua
if player:is_left_handed() then
    -- ...
end
```

## get_abs_origin

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the absolute origin (the one that is used for rendering).

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Origin. |

**Example**

```lua
local org = player:get_abs_origin();
```

## get_abs_angles

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the absolute angles (the one that is used for rendering).

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Angles. |

**Example**

```lua
local ang = player:get_abs_angles();
```

## set_abs_origin

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Sets the new absolute origin.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `vec` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | New origin. |

**Returns**

Nothing.

**Example**

```lua
player:set_abs_origin(my_vec);
```

## set_abs_angles

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Sets new absolute angles.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `ang` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | New angles. |

**Returns**

Nothing.

**Example**

```lua
player:set_abs_angles(my_ang);
```

## is_alive

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the player is alive.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if alive. |

**Example**

```lua
if player:is_alive() then
    -- ...
end
```

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

## is_enemy_to

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns whether this player is an enemy to another entity.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `ent` | [`base_entity`](/api/entities/base-entity "This type represents a base game entity.") | Other entity. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if an enemy. |

**Example**

```lua
if player:is_enemy_to(other_player) then
    -- ...
end
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

## get_view_offset

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the player's view offset (eye location relative to the player's origin).

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | View offset. |

**Example**

```lua
local vo = player:get_view_offset();
```

## get_eye_pos

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the player's eye position.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Eye position. |

**Example**

```lua
local eyes = player:get_eye_pos();
```