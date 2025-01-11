## spacer

This type represents a spacer control.

> This type inherits [`control`](/api/gui/control "This type represents an abstract GUI control.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the spacer.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | ID. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `spacer` | Spacer instance. |

**Example**

```lua
local sp = gui.spacer(gui.control_id('my_id'));
```