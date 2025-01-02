## control

This type represents an abstract GUI control.

## id

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

Control ID.

## id_string

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `string`

String representation of control's ID. This may be empty for some controls.

## is_visible

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Control's visibility state.

## parent

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `control?`

Parent control. Might be `nil` on some controls.

## type

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`control_type`](https://lua.fatality.win/control-type.html "This enum determines the current control's type.")

Control's type.

## inactive

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `bool`

If set to `true`, will mark this control to the inactive state.

## inactive_text

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `string`

Tooltip replacement to show when control is inactive.

## inactive_color

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.")

Label color override for inactive controls.

## tooltip

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `string`

Tooltip text.

## aliases

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `table[string]`

Alias list for this control. Used in search box to support different naming (e.g. if a user searches for "Double tap", will find "Rapid fire" instead).

## get_hotkey_state

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns true if any of the control's hotkeys are active.

**Arguments**

None.

**Returns**

| Name | Description |
| ---- | ----------- |
| `bool` | `true` if any hotkey is active. |

**Example**

```lua
if ctrl:get_hotkey_state() then
    -- ...
end
```

## set_visible

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Changes visibility state for this control.

> Calling this method on controls that are located in layouts with large amount of other controls will inevitably cause performance issues due to auto-stacking.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `val` | `bool` | Visibility state. |

**Returns**

Nothing.

**Example**

```lua
ctrl:set_visible(false);
```

## add_callback

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a callback to this control.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `cbk` | `function` | Callback. |

**Returns**

Nothing.

**Example**

```lua
ctrl:add_callback(function ()
    print('Callback invoked!');
end);
```

## cast

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Attempts to downcast the control to the correct type.

> Due to Lua engine's limitations, it is impossible to automatically downcast variables. Usually there is no need to call this method, unless you found some control that wasn't somehow already cast to the desired type. `find()` methods automatically perform the cast to the correct type.

**Arguments**

None.

**Returns**

| Name | Description |
| ---- | ----------- |
| `<control>` | New type, if any. |

**Example**

```lua
local checkbox = maybe_checkbox:cast();
```

## reset

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Resets control's state. This action is usually required if you change control's value directly by interacting with [`value_param`](https://lua.fatality.win/value-param.html "This type represents a value data used by some control types.").

**Arguments**

None.

**Returns**

Nothing.

**Example**

```lua
ctrl:reset();
```