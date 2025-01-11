## image

This type represents an image control.

> This type inherits [`control`](/api/gui/control "This type represents an abstract GUI control.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the image.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | ID. |
| `tex` | [`texture`](/api/draw/managed/texture "This type represents a texture object.") | Texture. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `image` | Image instance. |

**Example**

```lua
local img = gui.image(gui.control_id('my_id'));
```