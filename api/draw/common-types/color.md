## color

This type is a color used within the rendering system.

> Do not mistake this type with [`color`](https://lua.fatality.win/color.html "This type is a color used within the game.") that is used in game! While these types are interchangeable internally, they are **NOT** in the API.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Creates a new color instance.

**Arguments**

*1. Default color (translucent black).*

None.

*2. Integer colors.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | `int` | Red color (`0` to `255`). |
| `g` | `int` | Green color (`0` to `255`). |
| `b` | `int` | Blue color (`0` to `255`). |
| `a` | `int` | Opacity (`0` to `255`). Defaults to `255`. |

*3. Hex string.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `hex` | `string` | Hex string. Formats are: `#rrggbbaa`, `#rrggbb`, `#rgba` and `#rgb`. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Color object. |

**Example**

```lua
local white = draw.color(255, 255, 255);
```

## white

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Returns a white, opaque color.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Color object. |

**Example**

```lua
local white = draw.color.white();
```

## white_transparent

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Returns a white, transparent color.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Color object. |

**Example**

```lua
local white_t = draw.color.white_transparent();
```

## black

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Returns a black, opaque color.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Color object. |

**Example**

```lua
local black = draw.color.black();
```

## black_transparent

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Returns a black, transparent color.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Color object. |

**Example**

```lua
local black_t = draw.color.black_transparent();
```

## percent

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Returns a red-to-green color, depending on the provided percent.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `p` | `float` | Percentile (`0` to `1`). |
| `a` | `float` | Opacity. Defaults to `1`. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Color object. |

**Example**

```lua
local yellow = draw.color.percent(0.5);
```

## gray

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Returns a black-to-white color, depending on the provided percent.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `p` | `float` | Percentile (`0` to `1`). |
| `a` | `float` | Opacity. Defaults to `1`. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Color object. |

**Example**

```lua
local gray = draw.color.gray(0.5);
```

## interpolate

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Interpolates two colors.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `a` | `color` | Starting color. |
| `b` | `color` | Ending color. |
| `t` | `float` | Interpolation percentile. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Color object. |

**Example**

```lua
local a = draw.color.white();
local b = draw.color.black();
local i = draw.color.interpolate(a, b, 0.5); -- gray
```

## rgba

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns integer representation of this color (RGBA format)

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | RGBA color. |

**Example**

```lua
local num = col:rgba();
```

## argb

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns integer representation of this color (ARGB format)

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | ARGB color. |

**Example**

```lua
local num = col:argb();
```

## bgra

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns integer representation of this color (BGRA format)

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | BGRA color. |

**Example**

```lua
local num = col:bgra();
```

## abgr

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns integer representation of this color (ABGR format)

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | ABGR color. |

**Example**

```lua
local num = col:abgr();
```

## darken

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns darker variant of this color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Modulation amount (`0` to `1`). |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Darker color. |

**Example**

```lua
local darker = col:darken(0.5);
```

## mod_a

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Modulate opacity of the color. This will take existing opacity, and multiply it by whatever value you provide. It is useful if you want to modulate same color in steps, instead of setting the accurate opacity number.

**Arguments**

*1. Float variant.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Opacity modulation (0 to 1). |

*2. Integer variant.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `int` | Opacity modulation (0 to 255). |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | Modulated color. |

**Example**

```lua
local half_opacity = col:mod_a(0.5);
```

## r

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Override red and return new color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | New value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | New color. |

**Example**

```lua
local full_red = col:r(1);
```

## g

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Override green and return new color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | New value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | New color. |

**Example**

```lua
local full_green = col:g(1);
```

## b

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Override blue and return new color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | New value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | New color. |

**Example**

```lua
local full_blue = col:b(1);
```

## a

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Override opacity and return new color.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | New value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | New color. |

**Example**

```lua
local full_opacity = col:a(1);
```

## get_r

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns red color value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Color value. |

**Example**

```lua
local r = col:get_r();
```

## get_g

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns green color value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Color value. |

**Example**

```lua
local g = col:get_g();
```

## get_b

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns blue color value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Color value. |

**Example**

```lua
local b = col:get_b();
```

## get_a

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns opacity color value.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Color value. |

**Example**

```lua
local a = col:get_a();
```

## h

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Return hue value of the color.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Hue (`0` to `359`). |

**Example**

```lua
local hue = col:h();
```

## s

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns saturation value of the color.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Saturation (`0` to `1`). |

**Example**

```lua
local saturation = col:s();
```

## v

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns brightness value of the color.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Brightness (`0` to `1`). |

**Example**

```lua
local brightness = col:v();
```

## hsv

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Construct new color from provided HSB values.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `hue` | `int` | Hue (`0` to `359`). |
| `saturation` | `float` | Saturation (`0` to `1`). |
| `brightness` | `float` | Brightness (`0` to `1`). |
| `alpha` | `float` | Override opacity of the source color. **Must** be either left out, or provided `0` to `1` value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `color` | New color. |

**Example**

```lua
local new_col = col:hsv(250, 0.5, 0.1);
```