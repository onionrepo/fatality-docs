## game_event_t

Describes a game event.

## get_name

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the event name.

**Arguments**

None

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Event name. |

**Example**

```lua
if event:get_name() == 'player_hurt' then
    -- ...
end
```

## get_bool

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the boolean value by key.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `key` | `string` | Entry key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | Entry value. Returns `false` if such key was not found. |

**Example**

```lua
event:get_bool('some_key');
```

## get_int

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the integer value by key.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `key` | `string` | Entry key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Entry value. Returns `0` if such key was not found. |

**Example**

```lua
event:get_int('some_key');
```

## get_float

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the float value by key.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `key` | `string` | Entry key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Entry value. Returns `0.0` if such key was not found. |

**Example**

```lua
event:get_float('some_key');
```

## get_string

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the string value by key.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `key` | `string` | Entry key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Entry value. Returns `''` if such key was not found. |

**Example**

```lua
event:get_string('some_key');
```

## get_controller

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the controller by key.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `key` | `string` | Entry key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`cs2_player_controller`](https://lua.fatality.win/cs2-player-controller.html "This type represents a CCSPlayerController class.") | Controller. |

**Example**

```lua
event:get_controller('userid');
```

## get_pawn_from_id

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the pawn by key.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `key` | `string` | Entry key. |

**Returns**

| Type | Description |
| ---- | ----------- |
| [`cs2_player_pawn`](https://lua.fatality.win/cs2-player-pawn.html "This type represents a C_CSPlayerPawn class.") | Pawn. |

**Example**

```lua
event:get_pawn_from_id('userid');
```