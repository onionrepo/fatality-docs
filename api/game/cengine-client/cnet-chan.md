## cnet_chan

Provides a way to interface with a Network Channel's class.

## get_address

[![Method][This field is a method and must be invoked using a colon (:).]rw]

> If the current channel is `null`, this function will return `nil` instead.

Returns address string of the remote machine.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `string?` | IP-address or Steam Server Address. |

**Example**

```lua
local chan = game.engine:get_netchan();
if chan and not chan:is_null() then
    print(chan:get_address());
end
```

## is_loopback

[![Method][This field is a method and must be invoked using a colon (:).]rw]

> If the current channel is `null`, this function will return `nil` instead.

Returns whether the current channel is connected to the local machine (loopback address).

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool?` | `true` if connected to the local machine. |

**Example**

```lua
local chan = game.engine:get_netchan();
if chan and not chan:is_null() and chan:is_loopback() then
    print('Connected to localhost!');
end
```

## is_null

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Returns whether the channel is stubbed.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `bool` | true if current channel is a dummy channel. |

**Example**

```lua
local chan = game.engine:get_netchan();
if not chan or chan:is_null() then
    print('Not connected!');
end
```

## get_latency

[![Method][This field is a method and must be invoked using a colon (:).]rw]

> If the current channel is `null`, this function will return `nil` instead.

Returns current latency to the remote server (in seconds).

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `float?` | Latency (in seconds). |

**Example**

```lua
local chan = game.engine:get_netchan();
if chan and not chan:is_null() then
    print('Current latency: ' .. tostring(math.round(chan:get_latency() * 1000.0)) .. 'ms');
end
```