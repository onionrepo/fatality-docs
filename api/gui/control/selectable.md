## selectable

This type represents a selectable control.

> This type inherits [`control`](/api/gui/control "This type represents an abstract GUI control.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the selectable.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | Control ID. |
| `str` | `string` | Text string. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `selectable` | Selectable object. |

**Example**

```lua
local sel = gui.selectable(id, 'Hello!');
```