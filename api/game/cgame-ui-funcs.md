## cgame_ui_funcs

Usage: `game.game_ui_funcs:{method}`

This type represents the game's UI functions.

## get_binding_for_button_code

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the binding name for a button code.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `code` | `int` | Button code. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Binding. |

**Example**

```lua
local bind = game.game_ui_funcs:get_binding_for_button_code(code);
```