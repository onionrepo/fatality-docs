## shader

This type represents a shader. [`HLSL documentation`](https://learn.microsoft.com/en-us/windows/win32/direct3dhlsl/dx-graphics-hlsl-reference)

> This type inherits [`managed`](/api/draw/managed "This type represents a managed object. You cannot create an instance of this type directly.") type. All of its base methods and fields are also available in this type.

> Only fragment shaders (aka Pixel Shaders) are supported.

> Rendering system uses Shader Version 4 (ps_4_0).

## HLSL structures
The constant buffer fields are the following:

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mvp` | `float4x4` | Projection matrix. |
| `tex` | `float2` | Texture dimensions. |
| `time` | `float` | Render time (**NOT** the frame time). |
| `alpha` | `float` | Global opacity override. |

The input fields are the following:

| Name | Type | Description |
| ---- | ---- | ----------- |
| `pos` | `float4` | Vertex position on screen (x,y,z over w). Register: `SV_POSITION`. |
| `col` | `float4` | Vertex color tint (r, g, b, a). Register: `COLOR0`. |
| `uv` | `float2` | UV coordinates (u, v). Register: `TEXCOORD0`. |

The bound objects are the following:

| Name | Type | Description |
| ---- | ---- | ----------- |
| `sampler0` | `sampler` | Texture sampler. |
| `texture0` | `Texture2D` | Texture object. |

Template:

```shader
cbuffer cb : register(b0) {
    float4x4 mvp;
    float2 tex;
    float time;
    float alpha;
};

struct PS_INPUT {
    float4 pos : SV_POSITION;
    float4 col : COLOR0;
    float2 uv : TEXCOORD0;
};

sampler sampler0;
Texture2D texture0;
```

## __call

[![Constructor][This is a constructor definition for this type.]rw]

Constructs a shader.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `src` | `string` | Shader source code. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `shader` | Shader object. |

**Example**

```lua
local blur = draw.shader([[

// define constant buffer.
cbuffer cb : register(b0) {
    float4x4 mvp;
    float2 tex;
    float time;
    float alpha;
};

// define input.
struct PS_INPUT {
    float4 pos : SV_POSITION;
    float4 col : COLOR0;
    float2 uv : TEXCOORD0;
};

// use texture sampler and texture.
sampler sampler0;
Texture2D texture0;

float4 main(PS_INPUT inp) : SV_Target {
    float radius = 2.0; // blur radius
    float2 inv_size = 1.0 / tex.xy; // inversed size of the texture
    float weight = 0.0; // total weight
    float4 color = 0.0; // total color

    // perform a gaussian blur
    for (float x = -radius; x <= radius; x += 1.0)
    {
        for (float y = -radius; y <= radius; y += 1.0)
        {
            float2 coord = inp.uv + float2(x, y) * inv_size;
            color += texture0.Sample(sampler0, coord) * exp(-((x * x + y * y) / (2.0 * radius * radius)));
            weight += exp(-((x * x + y * y) / (2.0 * radius * radius)));
        }
    }

    // average the color
    color /= weight;
    color.a *= inp.col.a; // apply alpha modulation
    return color;
}
]]);
```