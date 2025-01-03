## checkbox

This type represents a checkbox control.

> This type inherits [`control`](/api/gui/control "This type represents an abstract GUI control.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the checkbox.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | ID. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `checkbox` | Checkbox instance. |

**Example**

```lua
local cb = gui.checkbox(gui.control_id('my_id'));
```

## get_value

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns checkbox' value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`value_param<bool>`](/api/gui/control/value-param "This type represents a value data used by some control types.") | Value data. |

**Example**

```lua
local val = cb:get_value():get();
```

## set_value

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Sets checkbox' value.

> It is advised to use this method instead of [`value_param`](/api/gui/control/value-param "This type represents a value data used by some control types.")'s [`set`](/api/gui/control/value-param?id=set "Sets the value.") method.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `val` | `bool` | New value. |

**Returns**

Nothing.

**Example**

```lua
cb:set_value(true);
```