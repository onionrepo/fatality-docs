## layer

A layer is a type that is used to store render commands, as well as vertex and index data. This is the only way to push shapes and control rendering state.

## g

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`command`](https://lua.fatality.win/command.html "This type is used to change render command parameters.")

The next render command to be pushed to the queue. This is the object you want to change to, for example, set a texture, or change rendering modes.

## font

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`font_base`](https://lua.fatality.win/font-base.html "This type represents the base class for font types. You cannot create an instance of this type. Instead, use the children types.")

Font to use with `add_text`. If nothing has been set, no text will get rendered.

## tex_sz

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`vec2?`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.")

Texture dimensions. This value is only required if you are trying to render rounded shapes with a texture, so the rendering system will correctly map your UV coordinates to whatever shape you are rendering.

## skip_dpi

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `bool`

If set to `true`, will skip global DPI scale. Defaults to `true`.

## add_triangle_filled

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled triangle with a single color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `a` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | A point. |
| `b` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | B point. |
| `c` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | C point. |
| `col` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Shape color. |

**Returns**

Nothing.

**Example**

```lua
layer:add_triangle_filled(
    draw.vec2(50, 50), draw.vec2(25, 75),
    draw.vec2(75, 75), draw.color(255, 255, 255));
```

## add_quad_filled

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled quad with a single color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `tl` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Top left point. |
| `tr` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Top right point. |
| `br` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Bottom right point. |
| `bl` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Bottom left point. |
| `col` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Shape color. |

**Returns**

Nothing.

**Example**

```lua
layer:add_quad_filled(
    draw.vec2(50, 50), draw.vec2(100, 60),
    draw.vec2(100, 100), draw.vec2(30, 70),
    draw.color(255, 255, 255));
```

## add_rect_filled

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled rectangle with a single color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Rectangle. |
| `col` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Shape color. |

**Returns**

Nothing.

**Example**

```lua
layer:add_rect_filled(draw.rect(50, 50, 150, 150), draw.color(255, 255, 255));
```

## add_circle_filled

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled circle with a single color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `center` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Center point. |
| `radius` | `float` | Circle radius. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Shape color. |
| `segments` | `int` | Circle segments. If set to `0`, will attempt automatic segment deduction. Defaults to `0`. |
| `fill` | `float` | Fill amount (clockwise, `0` to `1`). Defaults to `1`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_circle_filled(draw.vec2(50, 50), 10, draw.color(255, 255, 255));
```

## add_triangle_filled_multicolor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled, multicolor triangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `a` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | A point. |
| `b` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | B point. |
| `c` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | C point. |
| `cols` | `table[color, color, color]` | Colors for each point. Colors go in the very same order as the parameter list. |

**Returns**

Nothing.

**Example**

```lua
layer:add_triangle_filled_multicolor(
     draw.vec2(50, 50), draw.vec2(25, 75),
     draw.vec2(75, 75), {
        draw.color(255, 0, 0),
        draw.color(0, 255, 0),
        draw.color(0, 0, 255)
     });
```

## add_rect_filled_multicolor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled, multicolor rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Rectangle. |
| `cols` | `table[color, color, color, color]` | Colors for each corner of the rectangle, in clockwise order starting from top-left. |

**Returns**

Nothing.

**Example**

```lua
layer:add_rect_filled_multicolor(
    draw.rect(50, 50, 150, 150), {
        draw.color(255, 0, 0),
        draw.color(0, 255, 0),
        draw.color(0, 0, 255),
        draw.color(255, 255, 0)
    });
```

## add_circle_filled_multicolor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled, multicolor circle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `center` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Center point. |
| `radius` | `float` | Circle radius. |
| `cols` | `table[color, color]` | Colors for the gradient, starting with the inner and ending with the outer color. |
| `segments` | `int` | The number of segments to approximate the circle. Defaults to `36`. |
| `fill` | `float` | The portion of the circle to fill, where 1.0 is a full circle. Defaults to `1.0`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_circle_filled_multicolor(
    draw.vec2(100, 100), 50, {
        draw.color(255, 0, 0),
        draw.color(0, 0, 255)
    }, 36, 1.0);
```

## add_quad_filled_multicolor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled, multicolor quad.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `tl` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Top left point. |
| `tr` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Top right point. |
| `br` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Bottom right point. |
| `bl` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Bottom left point. |
| `cols` | `table[color, color]` | Colors for the gradient, applied from bottom to top. |

**Returns**

Nothing.

**Example**

```lua
layer:add_quad_filled_multicolor(
    draw.vec2(50, 50), draw.vec2(150, 50),
    draw.vec2(150, 150), draw.vec2(50, 150), {
        draw.color(255, 0, 0),
        draw.color(0, 0, 255)
    });
```

## add_pill_multicolor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a multicolor pill shape.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mins` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Top left point of the pill. |
| `maxs` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Bottom right point of the pill. |
| `radius_min` | `float` | The minimum radius of the pill's rounded edges. |
| `radius_max` | `float` | The maximum radius of the pill's rounded edges. |
| `cols` | `table[color, color]` | Colors for the gradient, applied from bottom to top. |
| `segments` | `int` | The number of segments for approximating rounded edges. Defaults to `16`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_pill_multicolor(
    draw.vec2(50, 50), draw.vec2(150, 100),
    10, 20, {
        draw.color(255, 0, 0),
        draw.color(0, 0, 255)
    }, 16);
```

## add_shadow_line

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a shadow line.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Bounding box for the shadow line. |
| `dir` | [`shadow_dir`](https://lua.fatality.win/shadow-dir.html "This enum is used to determine shadow direction for add_shadow_line method.") | Shadow direction. |
| `a` | `float` | Max opacity. Defaults to `0.25`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_shadow_line(
    draw.rect(50, 50, 150, 150), draw.shadow_dir.down, 0.25);
```

## add_shadow_rect

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a shadowed rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Rectangle. |
| `radius` | `float` | Shadow distance, in pixels, outwards. |
| `bg` | `bool` | Whether to draw a background for the rectangle. Defaults to `true`. |
| `a` | `float` | Max opacity of the shadow. Defaults to `0.25`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_shadow_rect(
    draw.rect(50, 50, 150, 150), 15, true, 0.25);
```

## add_glow

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a glow box.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Box rectangle. |
| `radius` | `float` | Glow distance, in pixels, outwards. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Glow color. |
| `parts` | [`glow_parts`](https://lua.fatality.win/glow-parts.html "This enum is used to determine which parts of the glow around the shape should get rendered.") | Parts of the glow to enable. Defaults to `all`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_glow(draw.rect(50, 50, 150, 150), 15, draw.color(255, 0, 0));
```

## add_rect_filled_rounded

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled, rounded rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Rectangle. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Fill color. |
| `amount` | `float` | Rounding amount. |
| `rnd` | [`rounding`](https://lua.fatality.win/rounding.html "This enum is used to determine the rounding for rounded shapes.") | Rounding mode. Defaults to `all`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_rect_filled_rounded(
    draw.rect(50, 50, 150, 150),
    draw.color(255, 0, 0),
    10,
    draw.rounding.all
);
```

## add_rect_filled_rounded_multicolor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a filled, multicolor rounded rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Rectangle. |
| `c` | `table[color, color, color, color]` | Fill colors. Used clockwise, starting from top left. |
| `amount` | `float` | Rounding amount. |
| `rnd` | [`rounding`](https://lua.fatality.win/rounding.html "This enum is used to determine the rounding for rounded shapes.") | Rounding mode. Defaults to `all`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_rect_filled_rounded_multicolor(
    draw.rect(50, 50, 150, 150), {
        draw.color(255, 0, 0),
        draw.color(0, 255, 0),
        draw.color(0, 0, 255),
        draw.color(255, 255, 0)
    },
    10,
    draw.rounding.all
);
```

## add_triangle

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a stroked triangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `a` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Point A. |
| `b` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Point B. |
| `c` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Point C. |
| `col` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Line color. |
| `thickness` | `float` | Line thickness. Defaults to `1.0`. |
| `mode` | [`outline_mode`](https://lua.fatality.win/outline-mode.html "This enum is used to determine the outline mode for outlined shapes.") | Outline mode. Defaults to `inset`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_triangle(
    draw.vec2(50, 50),
    draw.vec2(25, 75),
    draw.vec2(75, 75),
    draw.color(255, 0, 0),
    1.0,
    draw.outline_mode.inset
);
```

## add_quad

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a stroked quad.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `tl` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Top-left point. |
| `tr` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Top-right point. |
| `br` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Bottom-right point. |
| `bl` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Bottom-left point. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Line color. |
| `thickness` | `float` | Line thickness. Defaults to `1.0`. |
| `mode` | [`outline_mode`](https://lua.fatality.win/outline-mode.html "This enum is used to determine the outline mode for outlined shapes.") | Outline mode. Defaults to `inset`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_quad(
    draw.vec2(50, 50),
    draw.vec2(150, 50),
    draw.vec2(150, 150),
    draw.vec2(50, 150),
    draw.color(255, 0, 0),
    1.0,
    draw.outline_mode.inset
);
```

## add_rect

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a stroked rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Rectangle. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Line color. |
| `thickness` | `float` | Line thickness. Defaults to `1.0`. |
| `mode` | [`outline_mode`](https://lua.fatality.win/outline-mode.html "This enum is used to determine the outline mode for outlined shapes.") | Outline mode. Defaults to `inset`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_rect(
    draw.rect(50, 50, 150, 150),
    draw.color(255, 0, 0),
    1.0,
    draw.outline_mode.inset
);
```

## add_circle

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a stroked circle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `center` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Center point. |
| `radius` | `float` | Circle radius. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Line color. |
| `segments` | `int` | Circle segments. Defaults to `36`. |
| `fill` | `float` | Fill amount. Defaults to `1.0`. |
| `thickness` | `float` | Line thickness. Defaults to `1.0`. |
| `mode` | [`outline_mode`](https://lua.fatality.win/outline-mode.html "This enum is used to determine the outline mode for outlined shapes.") | Outline mode. Defaults to `inset`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_circle(
    draw.vec2(100, 100),
    50,
    draw.color(255, 0, 0),
    36,
    1.0,
    1.0,
    draw.outline_mode.inset
);
```

## add_line

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a line.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `a` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Start point. |
| `b` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | End point. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Line color. |
| `thickness` | `float` | Line thickness. Defaults to `1.0` |

**Returns**

Nothing.

**Example**

```lua
layer:add_line(
    draw.vec2(50, 50),
    draw.vec2(150, 150),
    draw.color(255, 0, 0)
);
```

## add_line_multicolor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a multicolor line.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `a` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Start point. |
| `b` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | End point. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Start color. |
| `c2` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | End color. |
| `thickness` | `float` | Line thickness. Defaults to `1.0`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_line_multicolor(
    draw.vec2(50, 50),
    draw.vec2(150, 150),
    draw.color(255, 0, 0),
    draw.color(0, 0, 255),
    2.0
);
```

## add_rect_rounded

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a rounded, filled rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | Rectangle. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Line color. |
| `amount` | `float` | Rounding amount. |
| `rnd` | [`rounding`](https://lua.fatality.win/rounding.html "This enum is used to determine the rounding for rounded shapes.") | Rounding mode. Defaults to `all`. |
| `thickness` | `float` | Line thickness. Defaults to `1.0`. |
| `mode` | [`outline_mode`](https://lua.fatality.win/outline-mode.html "This enum is used to determine the outline mode for outlined shapes.") | Outline mode. Defaults to `inset`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_rect_rounded(draw.rect(50, 50, 150, 150),
    draw.color(255, 255, 255), 14);
```

## add_text

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds text.

> If font wasn't set, this function will do nothing.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `p` | [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.") | Text origin point. |
| `text` | `string` | Text. |
| `c` | [`color`](https://lua.fatality.win/rcolor.html "This type is a color used within the rendering system.") | Text color. |
| `params` | [`text_params?`](https://lua.fatality.win/text-params.html "This type is used to determine text alignment.") | Text aligning parameters. Defaults to `nil`. |

**Returns**

Nothing.

**Example**

```lua
layer:add_text(draw.vec2(50, 50), 'Hello world!', draw.color(255, 255, 255));
```

## override_clip_rect

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Overrides clip rectangle with support of intersection.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | [`rect?`](https://lua.fatality.win/rect.html "This type is a rectangle used within rendering system.") | New clip rect. |
| `intersect` | `bool` | Whether this function should intersect previous rect with the new one. Defaults to `true`. |

**Returns**

Nothing.

**Example**

```lua
layer:override_clip_rect(draw.rect(50, 50, 150, 150));
```