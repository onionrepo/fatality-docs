## bits

This type represents a bitset value.

> Maximal bit number for this type is **63**. Setting or getting any bits outside of that range will cause a **crash**.

## reset

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Resets the value.

**Arguments**

None.

**Returns**

Nothing.

**Example**

```lua
bits:reset();
```

## get_raw

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the raw value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Raw value. |

**Example**

```lua
local raw = bits:get_raw();
```

## set_raw

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Sets the raw value.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `val` | `int` | Raw value. |

**Returns**

Nothing.

**Example**

```lua
bits:set_raw(long_long_value);
```

## none

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns true if no bits are set.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if no bits are set. |

**Example**

```lua
if bits:none() then
    -- ...
end
```

## set

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Enables a bit.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `bit` | `int` | Bit number. |

**Returns**

Nothing.

**Example**

```lua
bits:set(5); -- set bit #5 (same as bit.bor(val, bit.lshift(1, 5)))
```

## unset

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Disables a bit.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `bit` | `int` | Bit number. |

**Returns**

Nothing.

**Example**

```lua
bits:unset(5);
```

## get

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns bit state.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `bit` | `int` | Bit number. |

**Returns**

| Name | Description |
| ---- | ----------- |
| `bool` | Bit status. |

**Example**

```lua
if bits:get(5) then
    -- ...
end
```

## toggle

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Toggles bit state.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `bit` | `int` | Bit number. |

**Returns**

Nothing.

**Example**

```lua
bits:toggle(5);
```