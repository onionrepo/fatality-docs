## cengine_client

Usage: `game.engine.{method}`

An instance of this type provides a way to interface with Source 2's Engine-to-Client service.

## get_last_timestamp

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns last timestamp, in seconds.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `float` | Timestamp, in seconds. |

**Example**

```lua
local last_time = game.engine:get_last_timestamp();
```

## get_last_server_tick

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns last server tick number.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Server tick number. |

**Example**

```lua
local server_tick = game.engine:get_last_server_tick();
```

## in_game

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns whether the client is currently in game.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | In-game status. |

**Example**

```lua
if game.engine:in_game() then
    print("I'm in game!");
end
```

## is_connected

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns whether the client is currently connected to a game server.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | `true` if connected. |

**Example**

```lua
if game.engine:is_connected() then
    print("I'm connected!");
end
```

## get_netchan

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns the Network Channel used for network communication.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| [`cnet_chan`](https://lua.fatality.win/cnet-chan.html "Provides a way to interface with a Network Channel's class") | Network channel, or `nil` if does not exist. |

**Example**

```lua
local chan = game.engine:get_netchan();
```

## client_cmd

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Executes a client-sided console command.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `cmd` | `string` | Command to execute. |
| `bool` | `unrestricted` | Whether should the execution preserve any restrictions. Defaults to `false`. |

**Returns**

Nothing.

**Example**

```lua
game.engine:client_cmd('say Hello!');
```

## get_screen_size

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns client window screen size.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Width. |
| `int` | Height. |

**Example**

```lua
local w, h = game.engine:get_screen_size();
```