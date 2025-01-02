## notification_system

This type represents a notification system.

## add

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a notification to the list.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `notif` | [`notification`](https://lua.fatality.win/notification.html "This type represents a notification item.") | Notification object. |

**Returns**

Nothing.

**Example**

```lua
notif:add(my_notification);
```