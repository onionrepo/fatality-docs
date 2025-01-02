## vec2

This type is a 2D vector used within the rendering system.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Creates a new 2D vector instance.

**Arguments**

*1. Default vector (0, 0).*

None.

*2. Single value.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | X and Y coordinates. |

*3. XY values.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `x` | `float` | X coordinate. |
| `y` | `float` | Y coordinate. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `vec2` | New vector. |

**Example**

```lua
local vec = draw.vec2(5, 10);
```

## x

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

X coordinate.

## y

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Y coordinate.

## floor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns floored variant of this vector.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `vec2` | Floored variant. |

**Example**

```lua
local fl = vec:floor();
```

## ceil

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns ceiled variant of this vector.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `vec2` | Ceiled variant. |

**Example**

```lua
local ceiled = vec:ceil();
```

## round

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns rounded variant of this vector.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `vec2` | Rounded variant. |

**Example**

```lua
local rounded = vec:round();
```

## len

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns length of this vector.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Length. |

**Example**

```lua
local len = vec:len();
```

## len_sqr

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns squared length of this vector.

> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Length. |

**Example**

```lua
local len = vec:len_sqr();
```

## dist

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns distance to another vector.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `vec2` | Other vector. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Distance. |

**Example**

```lua
local dist = vec1:dist(vec2);
```

## dist_sqr

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns squared distance to another vector.

> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `vec2` | Other vector. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Distance. |

**Example**

```lua
local dist = vec1:dist_sqr(vec2);
```