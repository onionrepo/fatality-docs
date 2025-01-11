## color_picker

This type represents a color picker control.

> This type inherits [`control`](/api/gui/control "This type represents an abstract GUI control.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the color picker.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | Control ID. |
| `allow_alpha` | `bool` | Whether to enable alpha channel. Defaults to `true`. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color_picker` | Color picker object. |

**Example**

```lua
local picker = gui.color_picker(id);
```

## get_value

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns color picker' value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`value_param<color>`](/api/gui/control/value-param "This type represents a value data used by some control types.") | Value data. |

**Example**

```lua
local val = picker:get_value():get();
```