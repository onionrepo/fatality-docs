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

## UI System

### Basic Usage

```lua
local group = gui.ctx:find('lua>elements b') -- Returns container

local checkbox_id = gui.control_id('example_checkbox')
local checkbox = gui.checkbox(checkbox_id)
local checkbox_object = gui.make_control('Example Checkbox', checkbox) -- Adds label

group:add(checkbox_object)
group:reset() -- Moves to next row
```

### Create a Notification

```lua
local notification_obj = gui.notification('Header Text', 'Body Text')

gui.notify:add(notification_obj)
```

### Combo Box Usage

```lua
local group = gui.ctx:find('lua>elements b')

local combobox_id = gui.control_id('example_comboboxx')
local combobox = gui.combo_box(combobox_id)
local combobox_object = gui.make_control('Example Combo Box', combobox)

local selectable1 = gui.selectable(gui.control_id('example_selectable1'), "Example 1")
local selectable2 = gui.selectable(gui.control_id('example_selectable2'), "Example 2")
local selectable3 = gui.selectable(gui.control_id('example_selectable3'), "Example 3")

combobox:add(selectable1) -- Add the selectable to the combo box's container
combobox:add(selectable2)
combobox:add(selectable3)

group:add(combobox_object)
group:reset()

combobox:add_callback(function()
    local raw_value = combobox:get_value():get():get_raw()

    local index = 1
    while raw_value > 1 do -- Bit shift to correct current API output (1,2,4 to 1,2,3)
        raw_value = bit.rshift(raw_value, 1)
        index = index + 1
    end

    print(index) -- [lua] 3
end)
```