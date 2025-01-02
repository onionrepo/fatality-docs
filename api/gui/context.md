## context

This type represents the GUI context.

## find

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Finds a control by ID.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `id` | `string` | Control ID. |

**Returns**

| Name | Description |
| ---- | ----------- |
| `<control>?` | Casted control. Returns `nil` if the control was not found, or casting failed. |

**Example**

```lua
local some_cb = ctx:find('some_cb');
```

## user

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`user_t`](https://lua.fatality.win/user-t.html "This type represents basic user information.")

User's basic information.