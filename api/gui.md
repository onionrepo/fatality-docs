## gui

Usage: `gui.{func_or_field}`

This table exposes the GUI system of the software.

> All types and enums described in the child sections must be prefixed with `gui.`.

## ctx

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`context`](/api/gui/context "This type represents the GUI context.")

GUI context.

## notify

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`notification_system`](/api/gui/notification-system "This type represents a notification system.")

Notification system.

## input

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`context_input`](/api/gui/context-input "This type represents the GUI input context.")

Input context.

## make_control

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Wraps a control into a layout consisting of a label and that specific control. You should add **this** new control to groupboxes if you want your control to be displayed nicely. Additionally, you can add any extra controls to the returned one - those will get stacked to the left side of your initial control.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `text` | `string` | Label value. |
| `c` | [`control`](/api/gui/control "This type represents an abstract GUI control.") | Control object. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`layout`](/api/gui/container/control-container/layout "This type represents a layout control.") | Layout object. |

**Example**

```lua
local row = gui.make_control('Hello checkbox!', my_cb);
```