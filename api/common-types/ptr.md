## ptr

This type is a literal pointer.

To preserve interoperability with C++, several functions return `void*` as the type, which then get converted to `light_userdata`. Since you can’t directly cast FFI types to `light_userdata`, we’ve introduced a specialized type helping with this conversion.

Before you convert your pointer to one that is supported by the API, you **need** to cast it to `uintptr_t`. This can be done in the following manner:

```lua
local ptr_num = ffi.cast('uintptr_t', ptr_cdata);
```

Then, you can use the cast value in this type's constructor.

## __call
[![Constructor][This is a constructor definition for this type.]rw]

Converts a number to pointer.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `num` | `int` | Pointer, as number. |

**Returns**

| Name | Description |
| ---- | ----------- |
| `ptr` | Pointer, as `light_userdata`. |

**Example**

```lua
-- cast to number first
local ptr_num = ffi.cast('uintptr_t', ptr_cdata);

-- then cast to light_userdata
local ptr_ld = ptr(ptr_num);
```