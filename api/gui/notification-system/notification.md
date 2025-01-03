## notification

This type represents a notification item.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the notification.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `hdr` | `string` | Header (title). |
| `txt` | `string` | Text (body). |
| `ico` | [`texture?`](/api/draw/managed/texture "This type represents a texture object.") | Icon. Defaults to `nil`. |

**Returns**

| Name | Description |
| ---- | ----------- |
| `notification` | Notification object. |

**Example**

```lua
local notif = gui.notification('Hello', 'Lua works!');
```