## accessor

This type represents a safe way to access maps.

> Note that `<type>` indicates the specific type this instance holds. `accessor<texture>` for example means that `get` will return an instance of `texture`, and `set` will only accept the type `texture` as it's `obj` parameter.

## __index

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Returns an object by key.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `key` | `string` | Object key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `<type>` | Object. |

**Example**

```lua
local main_font = draw.fonts['gui_main'];

-- this also works
local main_font_2 = draw.fonts.gui_main;
```

## __newindex

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Sets an object by key.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `key` | `string` | Object key. |
| `obj` | `<type>` | Object. |

**Returns**

Nothing.

**Example**

```lua
draw.fonts['my_font'] = my_font;

-- this also works
draw.fonts.my_font = my_font;
```