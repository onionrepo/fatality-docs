## cs2_weapon_base

This type represents a `CCSWeaponBase` entity.

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