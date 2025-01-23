## Entity System

### Accessing Schemas
We grab your local pawn, then return health through the m_iHealth schema. a complete schema dump can be found in Quick Links. The local pawn will be a `C_CSPlayerPawn` class, it inherits all schemas from this class and any subsequent parents (ex: `C_CSPlayerPawnBase`).

```lua
local local_pawn = entities.get_local_pawn() -- cs2_player_pawn

local health_field = local_pawn.m_iHealth:get()
local health_index = local_pawn['m_iHealth']:get()

print(health_field, ", ", health_index) -- [lua] 100, 100
```

### Looping the Entity List

We loop through the provided entity table, these can be found in the entities tab (Examples are: `players`, `controllers`, ...). The returned function arg is an `entity_entry_t`, we can access the actual entity through it's entity field.

```lua
entities.players:for_each(function(entry)
    local player = entry.entity
    local is_alive = player:is_alive()

    print(is_alive) -- [lua] true
end)
```

### Casting an Entity Pointer

[![Insecure Only][This function exists only when 'Allow insecure' is enabled.]i]

If you need a direct entity pointer for whatever reason, the API supports directly casting them.

```lua
local local_controller = entities.get_local_controller()

local local_pointer = ffi.cast("uintptr_t*", local_controller)[0]
if (local_pointer == 0) then
    return
end

local CCSPlayerController = {
    m_iPing = 0x740, -- offset to use for example, could be out dated
}

local local_ping = ffi.cast("int*", local_pointer + CCSPlayerController.m_iPing)[0]
print(local_ping) -- [lua] 43
```

## Rendering System

### Rendering a Rectangle

We grab the rendering layer `draw.surface`, then call a layer method `add_rect_filled` on it to render.

```lua
local layer = draw.surface

events.present_queue:add(function()
    layer:add_rect_filled(
        draw.rect(50, 50, 200, 200),
        draw.color(255, 255, 255, 255)
    )
end)
```

### Creating a Font

We create the font through `draw.font`, with two required arguments being the **font path** (defaulting to the Fatality folder), and the other being the **font size**. We additionally add the `outline` and `anti_alias` font flags through the bor bitwise operation. After that we ensure the `font_base` managed object is created, then set the layer font and render text.

```lua
local layer = draw.surface

local verdana = draw.font("C:\\Windows\\Fonts\\Verdana.ttf", 16, bit.bor(draw.font_flags.outline, draw.font_flags.anti_alias))
verdana:create()

events.present_queue:add(function()
    layer.font = verdana -- Remember to use this field on your layer object

    layer:add_text(draw.vec2(50, 50), "Hello World!", draw.color(255, 255, 255, 255))

    layer.font = nil
end)
```