## ccsgo_input

Usage: `game.input.{field_or_method}`

This type represents the game's command input system.

## in_third_person

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

`true` if currently in the third person.

## get_view_angles

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns current camera view angles.

**Arguments**

None

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | View angles. |

**Example**

```lua
local ang = game.input:get_view_angles();
```

## set_view_angles

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Sets new camera view angles.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `ang` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | View angles. |

**Returns**

Nothing.

**Example**

```lua
game.input:set_view_angles(math.vec3(0, 0, 0));
```