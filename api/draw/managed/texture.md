## texture

This type represents a texture object.

> This type inherits [`managed`](/api/draw/managed "This type represents a managed object. You cannot create an instance of this type directly.") type. All of its base methods and fields are also available in this type.

> Supported texture formats are:
> * JPEG (.jpg, .jpeg) - 12 bpc/arithmetic are not supported
> * PNG (.png)
> * TGA (.tga) 
> * BMP (.bmp) - 1 bpp and RLE variants are not supported
> * PSD (.psd) - composited view only, no extra channels, 8/16 bpc
> * GIF (.gif) - only first frame, for animated gifs use [`animated_texture`](/api/draw/managed/texture/animated-texture "This type is an animated texture. This texture type only supports GIF types, and does not support APNG.")
> * HDR (.hdr)
> * PIC (.pic)
> * PNM (.pnm, .ppm, .pgm) - PPM and PGM are binary only

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs an instance of this type.

> Passing an invalid pointer, or a memory region that is smaller than the size will result in a **crash**.

**Arguments**

*1. From file:*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `path` | `string` | Path to a valid texture file. |

*2. From memory:*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `data` | [`ptr`](/api/common-types/ptr "This type is a literal pointer.") | Pointer to texture **file** data in memory. |
| `sz` | `int` | Size of the texture **file** data. |

*3. From RGBA data:*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `data` | [`ptr`](/api/common-types/ptr "This type is a literal pointer.") | Pointer to **RGBA** data in memory. |
| `w` | `int` | Width. |
| `h` | `int` | Height (row count). |
| `p` | `int` | Pitch (row width). This is the amount of **bytes** per row. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `texture` | Texture object. |

**Example**

```lua
local tex = draw.texture('funny_meme.png');
```

## is_animated

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

**Type:** `bool`

Set to `true` if this is an instance of [`animated_texture`](/api/draw/managed/texture/animated-texture "This type is an animated texture. This texture type only supports GIF types, and does not support APNG.").

## get_size

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns size of this texture.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Texture dimensions. |

**Example**

```lua
local sz = tex:get_size();
```