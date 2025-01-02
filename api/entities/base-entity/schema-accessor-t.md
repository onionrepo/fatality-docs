## schema_accessor_t

This type represents a special structure that references a certain field in the entity object.

> You can check the returned type by using `type()` function.

> Do not **ever** store an instance of this type anywhere but in a scope of an event because entity might be removed.

## get

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `<type>` | Value. |

**Example**

```lua
local health = player.m_iHealth:get();
```

## set

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Sets the value.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `<type>` | Value. |

**Returns**

Nothing.

**Example**

```lua
player.m_iHealth:set(50); -- won't really do anything with the health
```