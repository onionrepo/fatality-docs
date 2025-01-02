## cs2_weapon_base_gun

This type represents a `CCSWeaponBaseGun` class.

> This type inherits [`base_entity`](https://lua.fatality.win/base-entity.html "This type represents a base game entity.") type. All of its base methods and fields are also available in this type.

## get_abs_origin

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the absolute origin (the one that is used for rendering).

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](https://lua.fatality.win/vector.html "This type is a common 3D vector (x, y, z).") | Origin. |

**Example**

```lua
local org = wep:get_abs_origin();
```

## get_max_speed

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the maximal player speed when holding this weapon.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Max speed, in UPS. |

**Example**

```lua
local spd = wep:get_max_speed();
```

## get_inaccuracy

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the current inaccuracy value.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mode` | [`csweapon_mode`](https://lua.fatality.win/csweapon-mode.html "This enum represents the firing mode for a weapon.") | Weapon mode. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Inaccuracy value. |

**Example**

```lua
local inacc = wep:get_inaccuracy(csweapon_mode.primary_mode);
```

## get_spread

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the current spread value.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mode` | [`csweapon_mode`](https://lua.fatality.win/csweapon-mode.html "This enum represents the firing mode for a weapon.") | Weapon mode. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Inaccuracy value. |

**Example**

```lua
local spread = wep:get_spread(csweapon_mode.primary_mode);
```

## get_id

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the weapon ID.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`weapon_id`](https://lua.fatality.win/weapon-id.html "This enum represents the unique identifier for various weapons in the game.") | Weapon ID. |

**Example**

```lua
local wep_id = wep:get_id();
```

## get_type

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the weapon type.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`csweapon_type`](https://lua.fatality.win/csweapon-type.html "This enum represents the weapon type in the game.") | Weapon type. |

**Example**

```lua
local type = wep:get_type();
```

## get_data

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the weapon static data.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`ccsweapon_base_vdata`](https://lua.fatality.win/ccsweapon-base-vdata.html "This type represents a weapon's static data.") | Weapon data. |

**Example**

```lua
local data = wep:get_data();
```

## is_gun

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if this weapon is a **firearm**.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if a firearm. |

**Example**

```lua
if wep:is_gun() then
    -- ...
end
```

## is_attackable

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if you can attack with this weapon.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if can attack. |

**Example**

```lua
if wep:is_attackable() then
    -- ...
end
```

## has_secondary_attack

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if this weapon has a secondary attack mode.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if has the secondary attack mode. |

**Example**

```lua
if wep:has_secondary_attack() then
    -- ...
end
```

## has_spread

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns true if this weapon has spread (e.g. knives do not have any spread).

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if has spread. |

**Example**

```lua
if wep:has_spread() then
    -- ...
end
```