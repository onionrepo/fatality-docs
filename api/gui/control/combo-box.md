## combo_box

This type represents a combo box control.

> This type inherits [`control_container`](/api/gui/container/control-container "This type represents an abstract control with a container.") type. All of its base methods and fields are also available in this type.

> `add` method expects an instance of [`selectable`](/api/gui/control/selectable "This type represents a selectable control."). Passing other control types will not add them to the list.

> Value bits are toggled in order of selectables. That means if the first element is toggled, so will be the first bit, etc.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the combo box.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | ID. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `combo_box` | Combo box instance. |

**Example**

```lua
local cb = gui.combo_box(gui.control_id('my_id'));
```

## allow_multiple

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `bool`

If set to `true`, the checkbox will be able to toggle multiple selectables.

## get_value

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns combo box' value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`value_param<bits>`](/api/gui/control/value-param "This type represents a value data used by some control types.") | Value data. |

**Example**

```lua
local val = cb:get_value():get();
```