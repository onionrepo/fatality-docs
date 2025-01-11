## slider

This type represents a slider control.

> This type inherits [`control`](/api/gui/control "This type represents an abstract GUI control.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the slider.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | Control ID. |
| `low` | `float` | Minimum value. |
| `high` | `float` | Maximum value. |
| `fmt` | `table[...]` | Format. Defaults to `{'%.0f'}`. |
| `step` | `float` | Step value. Defaults to `1.0`. |

**Format Table**

> Format table can either be a single string with the desired format, or multiple elements with different minimum actuators. You **have** to pass multiple values in the descendant order, starting from the highest value to the lowest value. `min` and `add` values are both optional, but it makes no sense to leave either of them out.

> Formatting uses standard `printf` syntax. [Documentation](https://cplusplus.com/reference/cstdio/printf/)

> Passing invalid format will lead to an undefined behavior.

*1. Single Formatting.*

| Type | Description |
| ---- | ----------- |
| `string` | Format string. |

*2. Multi Formatting.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `min` | `float?` | Minimal value. |
| `add` | `float?` | Add step. |
| `fmt` | `string` | Format string. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Slider object. |

**Example**

```lua
local slider = gui.slider(id, 0, 100, {'%.0f%%'});
```

## get_value

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns slider' value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`value_param<float>`](/api/gui/control/value-param "This type represents a value data used by some control types.") | Value data. |

**Example**

```lua
local val = slider:get_value():get();
```