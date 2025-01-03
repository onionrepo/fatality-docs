## adapter

This type represents a rendering adapter used within the rendering system.

## get_back_buffer

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns a back buffer texture. May return a blank or outdated texture, if the back buffer texture was not updated.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`ptr`](/api/common-types/ptr "This type is a literal pointer.") | Back buffer texture pointer. |

**Example**

```lua
local bb = adapter:get_back_buffer();
```

## get_back_buffer_downsampled

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns a 4x down sampled version of the back buffer texture.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`ptr`](/api/common-types/ptr "This type is a literal pointer.") | Downsampled back buffer texture pointer. |

**Example**

```lua
local ds = adapter:get_back_buffer_downsampled();
```

## get_shared_texture

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns a shared texture. This texture usually replicates the down sampled back buffer texture, although it is updated automatically ONCE before the rendering on the layer starts.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`ptr`](/api/common-types/ptr "This type is a literal pointer.") | Shared texture pointer. |

**Example**

```lua
local shared = adapter:get_shared_texture();
```