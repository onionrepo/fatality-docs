## button

This type represents a button control.

> This type inherits [`control`](/api/gui/control "This type represents an abstract GUI control.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the button.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | Control ID. |
| `str` | `string` | Text string. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `button` | Button object. |

**Example**

```lua
local btn = gui.button(id, 'Hello!');
```