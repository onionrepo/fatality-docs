## event_t

Event usertype. An instance of this type can be found in [`events`](https://lua.fatality.win/events.html "There are a number of events that Fatality provides to use in the API - from various hooks, to in-game events. Each event entry is an object of event_t. This table documents events to be used by your scripts.").

## add

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Adds a callback to the event.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `fn` | `function` | Callback function. Arguments that are accepted by the function are dictated by the event instance. |

**Returns**

Nothing.

**Example**

```lua
events.present_queue:add(function ()
    -- will be called every time game queues a frame for rendering
end);
```

## remove

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Removes a callback from the event.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `fn` | `function` | Callback function, that was earlier passed to the `add()` function. |

**Returns**

Nothing.

**Example**

```lua
local function on_present()
    if some_condition then
        events.present_queue:remove(on_present)
    end
end

events.present_queue:add(on_present)
```