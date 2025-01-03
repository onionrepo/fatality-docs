## cs2_grenade_projectile

This type represents a grenade projectile.

> This type inherits [`base_entity`](/api/entities/base-entity "This type represents a base game entity.") type. All of its base methods and fields are also available in this type.

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
local org = wep:get_abs_origin();
```

## get_grenade_type

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the grenade type.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Grenade type. |

**Example**

```lua
local type = gren:get_grenade_type();
```