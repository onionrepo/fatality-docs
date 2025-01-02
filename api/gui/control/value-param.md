## value_param

This type represents a value data used by some control types.

> Note, that this part: `<type>` is used to designate what exact type the instance of this type is holding. For example, when it says `value_param<bool>`, it means that `get` will return a `bool` value, and `set` will accept only the type `bool` as it's `val` parameter.

## get

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the value.

**Arguments**

None.

**Returns**

| Name | Description |
| ---- | ----------- |
| `<type>` | Value. |

**Example**

```lua
ctrl:get_value():get();
```

## set

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Sets the value.

> It is advised to use `set_value` method of the control, if any.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `val` | `<type>` | Value. |

**Returns**

Nothing.

**Example**

```lua
ctrl:get_value():set(123);
```

## get_hotkey_state

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if there's any active hotkeys.

**Arguments**

None.

**Returns**

| Name | Description |
| ---- | ----------- |
| `bool` | `true` if any hotkey is active. |

**Example**

```lua
if ctrl:get_value():get_hotkey_state() then
    -- ...
end
```

## disable_hotkeys

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Disables all active hotkeys. This allows you to override the value.

**Arguments**

None.

**Returns**

Nothing.

**Example**

```lua
ctrl:get_value():disable_hotkeys();
```