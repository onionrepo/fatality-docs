## context_input

This type represents the GUI input context.

> You can use `cursor`, `is_mouse_up`, `is_mouse_down`, `is_key_up` and `is_key_down` methods outside [`input`](/api/events?id=input "Invoked every time the GUI processes input.") context. Using other methods will not make any sense, as the information will be outdated.

## cursor

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns current cursor position.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Cursor position. |

**Example**

```lua
local cur = gui.input:cursor();
```
## cursor_prev

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns previous cursor position.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Previous cursor position. |

**Example**

```lua
local prev = gui.input:cursor_prev();
```

## cursor_delta

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Delta value between previous and current cursor positions.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "This type is a 2D vector used within the rendering system.") | Cursor delta. |

**Example**

```lua
local delta = gui.input:cursor_delta();
```

## did_cursor_move

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the cursor did move since the last input.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if moved. |

**Example**

```lua
if gui.input:did_cursor_move() then
    -- ...
end
```

## did_wheel_move

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if mouse scroll wheel did move since the last input.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if moved. |

**Example**

```lua
if gui.input:did_wheel_move() then
    -- ...
end
```

## did_process_mouse

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if any mouse key's state had changed.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if processed. |

**Example**

```lua
if gui.input:did_process_mouse() then
    -- ...
end
```

## button_released

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if any key was released since the last input.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if released. |

**Example**

```lua
if gui.input:button_released() then
    -- ...
end
```

## wheel_delta

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the amount of rows scrolled this input.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Rows scrolled. |

**Example**

```lua
local scroll = gui.input:wheel_delta();
```

## is_mouse_up

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the mouse key is up (depressed).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mb` | [`mouse_button`](/api/gui/context-input/mouse-button "This enum represents mouse buttons.") | Mouse button. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if depressed. |

**Example**

```lua
if gui.input:is_mouse_up(gui.mouse_button.left) then
    -- ...
end
```

## is_mouse_down

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the mouse key is down (pressed).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mb` | [`mouse_button`](/api/gui/context-input/mouse-button "This enum represents mouse buttons.") | Mouse button. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if depressed. |

**Example**

```lua
if gui.input:is_mouse_down(gui.mouse_button.left) then
    -- ...
end
```

## is_mouse_clicked

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the mouse key is clicked (switched from depressed to pressed state).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mb` | [`mouse_button`](/api/gui/context-input/mouse-button "This enum represents mouse buttons.") | Mouse button. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if clicked. |

**Example**

```lua
if gui.input:is_mouse_clicked(gui.mouse_button.left) then
    -- ...
end
```

## is_mouse_released

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if the mouse key is released (switched from pressed to depressed state).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mb` | [`mouse_button`](/api/gui/context-input/mouse-button "This enum represents mouse buttons.") | Mouse button. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if released. |

**Example**

```lua
if gui.input:is_mouse_clicked(gui.mouse_button.left) then
    -- ...
end
```

## did_process_key

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if any key's state had changed.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if state changed. |

**Example**

```lua
if gui.input:did_process_key() then
    -- ...
end
```

## is_key_up

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if a key is up (depressed).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `k` | `int` | Virtual key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if depressed. |

**Example**

```lua
if gui.input:is_key_up(0x41) then -- 0x41 = "A"
    -- ...
end
```

## is_key_down

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if a key is down (pressed).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `k` | `int` | Virtual key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if pressed. |

**Example**

```lua
if gui.input:is_key_down(0x41) then -- 0x41 = "A"
    -- ...
end
```

## is_key_clicked

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if a key is clicked (switched from depressed to pressed state).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `k` | `int` | Virtual key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if clicked. |

**Example**

```lua
if gui.input:is_key_clicked(0x41) then -- 0x41 = "A"
    -- ...
end
```

## is_key_released

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns `true` if a key is released (switched from pressed to depressed state).

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `k` | `int` | Virtual key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if released. |

**Example**

```lua
if gui.input:is_key_released(0x41) then -- 0x41 = "A"
    -- ...
end
```