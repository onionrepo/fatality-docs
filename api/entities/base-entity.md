## base_entity

This type represents a base game entity.

> This type may be returned for any other abstract entity class, but internally will point to the correct type.

## __index

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Attemps to search for a field in this class.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `name` | `string` | Field name. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`schema_accessor_t`](/api/entities/base-entity/schema-accessor-t "This type represents a special structure that references a certain field in the entity object.") | Accessor instance. |

**Example**

```lua
local health = player.m_iHealth;
local health = player['m_iHealth']; -- this also works
```