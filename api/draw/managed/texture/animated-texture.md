## animated_texture

This type is an animated texture. This texture type only supports **animated GIF** types, and does not support **APNG**.

> This type inherits [`texture`](https://lua.fatality.win/texture.html "This type represents a texture object.") type. All of its base methods and fields are also available in this type.

> If you pass an unsupported type, it will instead work **exactly** like [`texture`](https://lua.fatality.win/texture.html "This type represents a texture object.") type, meaning controlling frames and looping will be meaningless.

> Using this type for texture atlases is possible, although highly unrecommended. It will produce extra texture objects in memory, and overall will be much slower. Instead, it is advised to construct an actual texture atlas, use [`texture`](https://lua.fatality.win/texture.html "This type represents a texture object.") type, and use texture mapping.

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs animated texture.

> Passing an invalid pointer, a or memory region that is smaller than the size will result in a **crash**.

**Arguments**

*1. From file.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `path` | `string` | Path to the texture file. |

*2. From memory.*

| Name | Type | Description |
| ---- | ---- | ----------- |
| `data` | [`ptr`](https://lua.fatality.win/ptr.html "This type is a literal pointer.") | Pointer to texture **file** data in memory. |
| `sz` | `int` | Size of the texture **file** data. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `animated_texture` | Animated texture instance. |

**Example**

```lua
local gif = draw.animated_texture('funny_gif.gif');
```

## should_loop

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `bool`

If set to `false`, will not loop the animation automatically. Defaults to `true`.

## reset_loop

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Reset loop to run from the first frame.

**Arguments**

None.

**Returns**

Nothing.

**Example**

```lua
gif:reset_loop();
```

## set_frame

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Set a specific frame on the animation. If looping is enabled, will continue the cycle from the passed frame. Otherwise, will display a specific frame of the animation.

> Frame count starts from `0`.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `frame` | `int` | Frame number. Invalid frame numbers will be clamped. |

**Returns**

Nothing.

**Example**

```lua
gif:set_frame(5);
```

## get_frame_count

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns amount of frames in the animation.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Frame count. |

**Example**

```lua
local frames = gif:get_frame_count();
gif:set_frame(frames - 2); -- set to the last frame
```