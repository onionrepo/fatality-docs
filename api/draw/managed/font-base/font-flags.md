## font_flags

This enum determines which flags a font object should possess. Setting those flags is only possible during type construction.

## shadow

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Adds a 1px shadow to font glyphs.

## outline

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Adds a 1px outline to font glyphs.

## anti_alias

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Enable antialiasing on font glyphs. This flag only works on GDI fonts.

## no_dpi

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Disable DPI scaling on this font. By default, font glyphs will be scaled in accordance to the global DPI scale.

## no_kern

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Disable glyph kerning on this font.

## mono

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Enables a strong hinting algorithm for rasterization. Only works on FreeType fonts.

## light

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Enables a light hinting algorithm for rasterization. Only works on FreeType fonts.