## vector

This type is a common 3D vector (x, y, z).

> This type supports operations, such as `+`, `-`, `/`, `*` and `==`.

## x

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

X coordinate.

## y

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Y coordinate.

## z

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Z coordinate.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs a vector.

**Arguments**

*1. Default vector (0, 0, 0).*

None.

*2. Single value.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `value` | `float` | X and Y coordinates. |

*3. XYZ values.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `x` | `float` | X coordinate. |
| `y` | `float` | Y coordinate. |
| `z` | `float` | Z coordinate. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `vector` | Vector. |

**Example**

```lua
local vec = vector(5, 25, 12);
```

## is_zero

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if this vector is within tolerance range.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `tolerance` | `float` | Max allowed tolerance. Defaults to `0.01`. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if ranges between `-tolerance` and `tolerance`. |

**Example**

```lua
local vec = vector(0, 0.1, 0.5);
print(tostring(vec:is_zero(1))); -- will print 'true', because every value fits in the range of -1 and 1
```

## dist

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns distance to another vector.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `vector` | Vector to calculate distance against. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Distance to other vector. |

**Example**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist(vec2)));
```

## dist_sqr

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns squared distance to another vector.

> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `vector` | Vector to calculate distance against. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Squared distance to other vector. |

**Example**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_sqr(vec2)));
```

## dist_2d

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns 2D (only `x` and `y` values) distance to another vector.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `vector` | Vector to calculate distance against. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Distance to other vector. |

**Example**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_2d(vec2)));
```

## dist_2d_sqr

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns squared 2D (only `x` and `y` values) distance to another vector.

> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `vector` | Vector to calculate distance against. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Squared distance to other vector. |

**Example**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_2d_sqr(vec2)));
```

## cross

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns a cross product to another vector.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `vector` | Vector to calculate cross product against. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `vector` | Cross product. |

**Example**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
local cross = vec1:cross(vec2);
```

## is_valid

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if all values in this vector are finite.

**Arguments**

None

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if values are finite. |

**Example**

```lua
local vec = vector(5, 1, 6);
if vec:is_valid() then
    -- ...
end
```

## length

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns length of this vector.

**Arguments**

None

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Length of this vector. |

**Example**

```lua
local vec = vector(5, 1, 6);
local length = vec:length();
```

## length_sqr

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns squared length of this vector.

> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

**Arguments**

None

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Length of this vector. |

**Example**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_sqr();
```

## length_2d

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns 2D length of this vector.

**Arguments**

None

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Length of this vector. |

**Example**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_2d();
```

## length_2d_sqr

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns squared 2D length of this vector.

> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

**Arguments**

None

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Length of this vector. |

**Example**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_2d_sqr();
```

## dot

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns dot product of 2 vectors.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `other` | `vector` | Vector to calculate dot product against. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Dot product. |

**Example**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
local dot = vec1:dot(vec2);
```