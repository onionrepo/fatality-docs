## chandle

This type represents an entity handle.

> You can also compare this type using a `==` operator.

## get

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the entity, or nil if nothing found.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `<type>` | Entity instance. |

**Example**

```lua
local ent = handle:get();
```

## valid

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the handle is valid.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if valid. |

**Example**

```lua
if handle:valid() then
    -- ...
end
```

## is_clientside

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the handle links to a client-side entity.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if client-sided. |

**Example**

```lua
if handle:is_clientside() then
    -- ...
end
```