## text_input

This type represents a text input control.

> This type inherits [`control`](/api/gui/control "This type represents an abstract GUI control.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs the text input.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | [`control_id`](/api/gui/common-types/control-id "This type represents a control ID.") | ID. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `text_input` | Text input instance. |

**Example**

```lua
local sp = gui.text_input(gui.control_id('my_id'));
```

## placeholder

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `string`

Placeholder text.

## value

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `string`

Value.

## set_value

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Sets the new text.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `str` | `string` | New value. |

**Returns**

Nothing

**Example**

```lua
input:set_value('Hello!');
```