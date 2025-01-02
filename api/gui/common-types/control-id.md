## control_id

This type represents a control ID.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the ID structure.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | `string` | ID. |

**Returns**

| Name | Description |
| ---- | ----------- |
| `control_id` | ID structure. |

**Example**

```lua
local id = gui.control_id('my_id');
```

## id

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

Hashed representation of the ID.

## id_string

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `string`

Normal representation of the ID.