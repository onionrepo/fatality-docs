## font_base

This type represents the base class for font types. You cannot create an instance of this type. Instead, use the children types.

> This type inherits [`managed`](/api/draw/managed "This type represents a managed object. You cannot create an instance of this type directly.") type. All of its base methods and fields are also available in this type.

> Definitions:
> * **codepoint**: Unicode representation of the character.
> * **kerning**: a distance between two characters.
> * **glyph**: visual representation of a character.

## height

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

Font height, in pixels.

## ascent

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Font ascent value, in pixels.

## descent

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Font descent value, in pixels.

## line_gap

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Font line gap, in pixels.

## kerning_gap

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Font kerning gap, in pixels.

## outline_alpha

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Font outline opacity (`0` to `1`). Defaults to `0.45`.

## flags

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`font_flags`](/api/draw/managed/font-base/font-flags "This enum determines which flags a font object should possess. Setting those flags is only possible during type construction.")

Font flags. Use `bit` library to read flags.

## y_offset

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `int`

Glyph Y offset, in pixels. Will alter the location of a glyph in the atlas. Changing this value after the font was created is meaningless.

## x_offset

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `int`

Glyph X offset, in pixels. Will alter the location of a glyph in the atlas. Changing this value after the font was created is meaningless.

## fallback_font

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `font_base`

Fallback font to use, in case a glyph is not found in this font. Is it useful when one font does not have codepoints for specific symbols, that are present in another font, but you still want to prefer this font's glyphs over other font.

## dropshadow_color

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`color`](/api/draw/common-types/color "This type is a color used within the rendering system.")

Shadow color. Only R, G, B values are used.

## get_kerned_char_width

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns character width, included with kerning.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `left` | `int` | Previous character codepoint. |
| `right` | `int` | Current character codepoint. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Distance, in pixels. |

**Example**

```lua
local w = font:get_kerned_char_width(prev_cp, cp);
```

## get_kerning

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns kerning value for a single character. If kerning is disabled, will instead return kerning gap.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `cp` | `int` | Codepoint. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Kerning value, in pixels. |

**Example**

```lua
local k = font:get_kerning(cp);
```

## get_text_size

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns text area size.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `text` | `string` | Text. |
| `skip_scaling` | `bool` | If set to `true`, will skip global DPI scaling. Defaults to `false`. |
| `til_newline` | `bool` | Calculate size only until a line break is met. Defaults to `false`. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Text area size. |

**Example**

```lua
local sz = font:get_text_size('Hello!');
```

## wrap_text

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Wraps text to meet the desired width. Wrapping is done by breaking text by words and inserting line breaks in between. If one of the words is longer than the target width, will instead use that word's width.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `text` | `string` | Text to wrap. |
| `width` | `float` | Target width. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Wrapped text. |

**Example**

```lua
local shorter = font:wrap_text('This is some very long text!', 50);
```

## get_glyph

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns glyph information for a character.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `codepoint` | `int` | Codepoint. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`glyph_t`](/api/draw/managed/font-base/glyph-t "This type represents a glyph object.") | Glyph information. |

**Example**

```lua
local glyph = font:get_glyph(cp);
```

## get_texture

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns a texture atlas that contains the provided glyph.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `gl` | [`glyph_t`](/api/draw/managed/font-base/glyph-t "This type represents a glyph object.") | Character glyph. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Texture pointer, or `nil` if not found. |

**Example**

```lua
local atlas = font:get_texture(glyph);
```