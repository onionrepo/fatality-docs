## rect

This type is a rectangle used within rendering system.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Creates a new rectangle.

**Arguments**

*1. Default rectangle (0, 0 position; 0, 0 size).*

None.

*2. Single value.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Mins XY, maxs XY value. |

*3. Single vector.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Mins vector, maxs vector. |

*4. Double value.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `x` | `float` | Mins/maxs X coordinate. |
| `y` | `float` | Mins/maxs Y coordinate. |

*5. Double vector.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mins` | [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Mins vector. |
| `maxs` | [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Maxs vector. |

*6. Four values.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `x0` | `float` | Mins X coordinate. |
| `y0` | `float` | Mins Y coordinate. |
| `x1` | `float` | Maxs X coordinate. |
| `y1` | `float` | Maxs Y coordinate. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | New rectangle. |

**Example**

```lua
local my_rect = draw.rect(50, 50, 150, 150);
```

## mins

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.")

Mins (top-left) vector.

## maxs

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.")

Maxs (bottom-right) vector.

## width

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Either returns rectangle's width, or sets a new width.

**Arguments**

*1. Get width.*

None.

*2. Set width.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | New width. |

**Returns**

*1. Get width.*

| Type | Description |
| ---- | ----------- |
| `float` | Width. |

*2. Set width.*

| Type | Description |
| ---- | ----------- |
| `rect` | New rectangle with changed width. |

**Example**

```lua
local half_width = rect:width(rect:width() * 0.5);
```

## height

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Either returns rectangle's height, or sets a new height.

**Arguments**

*1. Get height.*

None.

*2. Set height.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | New height. |

**Returns**

*1. Get height.*

| Type | Description |
| ---- | ----------- |
| `float` | Height. |

*2. Set height.*

| Type | Description |
| ---- | ----------- |
| `rect` | New rectangle with changed height. |

**Example**

```lua
local half_height = rect:height(rect:height() * 0.5);
```

## size

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Either returns rectangle's size, or sets a new size.

**Arguments**

*1. Get size.*

None.

*2. Set size.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | New size. |

**Returns**

*1. Get size.*

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Size. |

*2. Set size.*

| Type | Description |
| ---- | ----------- |
| `rect` | New rectangle with changed size. |

**Example**

```lua
local half_size = rect:size(rect:size() * draw.vec2(0.5, 0.5));
```

## explode

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Explodes the rectangle by given vector (increase size from center into all directions by coordinates in the vector).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Explode size. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Exploded rectangle. |

**Example**

```lua
local exp = rect:explode(draw.vec2(6, 6)); -- will subtract -3,-3 from mins and add 3,3 to maxs
```

## half_width

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns a rectangle with half of the width of this rectangle.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Rectangle with halved width. |

**Example**

```lua
local half = rect:half_width();
```

## translate

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Translates (moves) this rectangle by vector coordinates.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Translation amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Translated rectangle. |

**Example**

```lua
local rect = draw.rect(50, 50, 150, 150);
local translated = rect:translate(draw.vec2(5, 5)); -- mins/maxs will be 55,55 and 155,155
```

## margin_left

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Move rectangle from the left by given amount.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Margin amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Moved rectangle. |

**Example**

```lua
local new = rect:margin_left(5); -- moves to the right by 5px
```

## margin_right

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Move rectangle from the right by given amount.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Margin amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Moved rectangle. |

**Example**

```lua
local new = rect:margin_right(5); -- moves to the left by 5px
```

## margin_top

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Move rectangle from the top by given amount.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Margin amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Moved rectangle. |

**Example**

```lua
local new = rect:margin_top(5); -- moves to the bottom by 5px
```

## margin_bottom

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Move rectangle from the bottom by given amount.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Margin amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Moved rectangle. |

**Example**

```lua
local new = rect:margin_bottom(5); -- moves to the top by 5px
```

## padding_left

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds the value to the left side of the rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Padding amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Resized rectangle. |

**Example**

```lua
local new = rect:padding_left(5); -- adds 5 to mins x
```

## padding_right

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds the value to the right side of the rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Padding amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Resized rectangle. |

**Example**

```lua
local new = rect:padding_right(5); -- adds 5 to maxs x
```

## padding_top

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds the value to the top side of the rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Padding amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Resized rectangle. |

**Example**

```lua
local new = rect:padding_top(5); -- adds 5 to mins y
```

## padding_bottom

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds the value to the bottom side of the rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Padding amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Resized rectangle. |

**Example**

```lua
local new = rect:padding_bottom(5); -- adds 5 to maxs y
```

## shrink

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Shrinks (implodes) the rectangle by given amount.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Shrink value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Resized rectangle. |

**Example**

```lua
local shrinked = rect:shrink(5); -- adds 5,5 to mins and subtracts 5,5 from maxs
```

## expand

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Expands (explodes) the rectangle by given amount.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | Expand value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Resized rectangle. |

**Example**

```lua
local expanded = rect:expand(5); -- subtracts 5,5 from mins and adds 5,5 to maxs
```

## contains

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if this rectangle contains either vector or another rectangle.

> Rectangle overload will return `true` **ONLY** if entire other rectangle is within the bounds of this one.

**Arguments**

*1. Vector variant.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Vector to check against. |

*2. Rectangle variant.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `rect` | Rectangle to check against. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if other object is in bounds of this rectangle. |

**Example**

```lua
if rect:contains(cursor_pos) then
    -- ...
end
```

## overlaps

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the other rectangle overlaps with this rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `rect` | Rectangle to check against. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if other rectangle overlaps with this rectangle. |

**Example**

```lua
if rect:overlaps(another_rect) then
    -- ...
end
```

## intersect

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Intersects this rectangle with another rectangle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `rect` | Rectangle to intersect with. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Intersected rectangle. |

**Example**

```lua
local intersected = rect:intersect(another_rect);
```

## tl

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns top-left vector.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Top-left vector. |

**Example**

```lua
local tl = rect:tl();
```

## tr

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns top-right vector.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Top-right vector. |

**Example**

```lua
local tr = rect:tr();
```

## br

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns bottom-right vector.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Bottom-right vector. |

**Example**

```lua
local br = rect:br();
```

## bl

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns bottom-left vector.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Bottom-left vector. |

**Example**

```lua
local bl = rect:bl();
```

## center

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns center point of this rectangle.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Center point. |

**Example**

```lua
local center = rect:center();
```

## circle

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Treats this rectangle as an ellipsis and returns point on it. Note, that this "ellipsis" will be perfect with no modified curvature (basically if this rectangle is a box - you will get a point on a perfect circle).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `r` | `float` | Radians value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Point on the ellipsis. |

**Example**

```lua
local point = rect:circle(rad(250)); -- returns point on the 250th degree
```

## floor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns floored rectangle.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Floored rectangle. |

**Example**

```lua
local floored = rect:floor();
```

## ceil

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns ceiled rectangle.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Ceiled rectangle. |

**Example**

```lua
local ceiled = rect:ceil();
```

## round

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns rounded rectangle.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `rect` | Rounded rectangle. |

**Example**

```lua
local rounded = rect:round();
```

## is_zero

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if both mins and maxs are equal to 0.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if this is a zero rectangle. |

**Example**

```lua
if rect:is_zero() then
    -- ...
end
```