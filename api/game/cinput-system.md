## cinput_system

Usage: `game.input_system:{method}`

This type represents the game's control input system.

## vk_to_button_code

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Converts a virtual key to button code.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `vk` | `int` | Virtual key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Button code. |

**Example**

```lua
local button = game.input_system:vk_to_button_code(0x41); -- 'A'
```