## math

Usage:
`math.{func}`

This table extends the existing `math` table that is a part of Lua.

## calc_angle

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Calculates angles between 2 vectors.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `src` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Source vector. |
| `dst` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Destination vector. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Angles. |

**Example**

```lua
local ang = math.calc_angle(vec1, vec2);
```

## angle_normalize

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Normalizes an angle.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `angle` | `float` | Input angle. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Normalized angle. |

**Example**

```lua
local norm = math.angle_normalize(560);
```

## approach_angles

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Approaches an angle over time.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `from` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Start angle. |
| `to` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | End angle. |
| `speed` | `float` | Approach speed. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Delta angle. |

**Example**

```lua
local ang = math.approach_angles(from, to, 1.0 / game.global_vars.frametime);
```

## edge_point

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Returns a point on the edge of a box.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mins` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Box mins. |
| `maxs` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Box maxs. |
| `dir` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Point direction (angle). |
| `radius` | `float` | Area radius. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Point. |

**Example**

```lua
local point = math.edge_point(mins, maxs, dir, 5);
```

## lerp

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Linear interpolation.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `t1` | `float` | Start value. |
| `t2` | `float` | End value. |
| `progress` | `float` | Interpolation amount. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Interpolated value. |

**Example**

```lua
local mid = math.lerp(0, 100, 0.5);
```

## vector_angles

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Calculates angles from a vector.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `forward` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Source vector. |
| `up` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Up vector. Defaults to `nil`. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Angles. |

**Example**

```lua
local ang = math.vector_angles(fw);
```

## world_to_screen

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Transforms a point in the game world onto the viewport.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `xyz` | [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).") | Point in the world. |
| `round` | `bool` | Whether should round the output. Defaults to `true`. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Point on the viewport. |

**Example**

```lua
local point = math.world_to_screen(game_point);
```

## clamp

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Clamps a value between min and max.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `n` | `float` | Value. |
| `lower` | `float` | Lowest value. |
| `upper` | `float` | Highest value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Clamped value. |

**Example**

```lua
local x = math.clamp(50, 5, 25); -- 25
```

## remap_val

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Maps the value from one range to another range.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `val` | `float` | Value. |
| `a` | `float` | Lowest source value. |
| `b` | `float` | Highest source value. |
| `c` | `float` | Lowest destination value. |
| `d` | `float` | Highest destination value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Mapped value. |

**Example**

```lua
local mapped = math.remap_val(0.5, 0, 1, 0, 100); -- 50
```

## remap_val_clamped

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Maps the value from one range to another range. Additionally, clamps the value based on the source range.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `val` | `float` | Value. |
| `a` | `float` | Lowest source value. |
| `b` | `float` | Highest source value. |
| `c` | `float` | Lowest destination value. |
| `d` | `float` | Highest destination value. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Mapped value. |

**Example**

```lua
local mapped = math.remap_val_clamped(5, 0, 1, 0, 100); -- 100
```

## vec2

[![Function][This field is a function and must be invoked using a dot (.)]rw]

An alias to [`draw.vec2()`](/api/draw/common-types/vec2#call "This type is a 2D vector used within the rendering system.").

**Example**

```lua
local vec = math.vec2(5, 5);
```

## vec3

[![Function][This field is a function and must be invoked using a dot (.)]rw]

An alias to [`vector()`](/api/common-types/vector#call "Constructs a vector.").

**Example**

```lua
local vec = math.vec3(5, 12, 5);
```