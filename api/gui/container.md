## container

This type represents an abstract container.

## add

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a control to the container.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `ctrl` | [`control`](/api/gui/control "This type represents an abstract GUI control.") | Control to add. |

**Returns**

Nothing.

**Example**

```lua
container:add(my_control);
```

## remove

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Removes a control from the container.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `ctrl` | [`control`](/api/gui/control "This type represents an abstract GUI control.") | Control to remove. |

**Returns**

Nothing.

**Example**

```lua
container:remove(my_control);
```

## find

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Finds a control by ID.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | `string` | Control ID. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `<control>?` | Casted control. Returns `nil` if the control was not found, or casting failed. |

**Example**

```lua
local some_cb = container:find('some_cb');
```