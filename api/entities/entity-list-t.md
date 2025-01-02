## entity_list_t

This type represents an entity list.

> Never save any entities you get from this list if you don't know what you are doing! You may be left with dangling pointers, which will inevitably lead to a crash.

## for_each

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Loops the entities.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `fn` | `function(entity_entry_t)` | Function callback. |

Nothing

**Example**

```lua
entities.players:for_each(function (entry)
    -- ...
end);
```

## for_each_z

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Loops the entities in the reverse order.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `fn` | `function(entity_entry_t)` | Function callback. |

Nothing

**Example**

```lua
entities.players:for_each_z(function (entry)
    -- ...
end);
```