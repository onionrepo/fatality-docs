## font_gdi

This type represents a font object. Internally, this type uses **GDI** library to rasterize font glyphs.

> This type inherits [`font_base`](/api/draw/managed/font-base "This type represents the base class for font types. You cannot create an instance of this type. Instead, use the children types.") type. All of its base methods and fields are also available in this type.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs a font object.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `name` | `string` | System font name (example: 'Arial'). |
| `size` | `float` | Font height, in pixels. |
| `fl` | [`font_flags`](/api/draw/managed/font-base/font-flags "This enum determines which flags a font object should possess. Setting those flags is only possible during type construction.") | Font flags. Use `bit` library to construct them. Defaults to `0`. |
| `mi` | `int` | Starting codepoint. Defaults to `0`. |
| `ma` | `int` | Ending codepoint. Defaults to `255` (entire ASCII code page). |
| `weight` | `int` | Font weight. Defaults to `400` (regular). |

**Returns**

| Type | Description |
| ---- | ----------- |
| `font_gdi` | Font object. |

**Example**

```lua
local sys_font = draw.font_gdi('Calibri', 14);
```