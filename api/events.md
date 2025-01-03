## events

Usage: `events.{event_name}`

There are a number of events that Fatality provides to use in the API - from various hooks, to in-game events. Each event entry is an object of [`event_t`](/api/events/event-t "Event usertype. An instance of this type can be found in events."). This table documents events to be used by your scripts.

> You are not required to remove events when your script unloads. It is done automatically by the API engine.

## present_queue

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked each time the game queues a frame for rendering. This is the only permitted location for drawing on screen.

**Arguments**

None.

## frame_stage_notify

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked every time the game progresses onto another frame stage. This event is called before the game handles a new frame stage.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `stage` | [`client_frame_stage`](/api/common-enums/client-frame-stage "Contains keys for various frame rendering stages.") | Current frame stage. |

## render_start_pre

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked every time game starts the scene rendering process. This event is called before the game's function runs.

**Arguments**

None.

## render_start_post

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked every time game starts scene rendering process. This event is called after the game's function runs.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `setup` | [`cview_setup`](/api/common-types/cview-setup "Describes view setup parameters.") | View setup information. |

## setup_view_pre

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked every time the game sets up the view. This event is called **before** the game's function runs.

**Arguments**

None.

## setup_view_post

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked every time the game sets up the view information. This event is called **after** the game's function runs.

> You can retrieve the view information from `game.view_render` service.

**Arguments**

None.

## override_view

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked every time the game internally overrides view information. You are free to change whatever you like in the provided view setup.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `setup` | [`cview_setup`](/api/common-types/cview-setup "Describes view setup parameters.") | View setup information. |

## event

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked every time a game event fires.

> We do not listen to every single event that exists in the game. If you need something that we don't listen to, please use [`mods.events`](/api/events/event-t "This module lets you manage custom in-game event listener.")

| Name | Type | Description |
| ---- | ---- | ----------- |
| `event` | [`game_event_t`](/api/common-types/game-event-t "Describes a game event.") | Game event. |

## handle_input

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Invoked every time the game processes mouse/controller input. This is a good place to alter mouse movement, if needed.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `type` | [`input_type_t`](/api/common-enums/input-type-t "Contains keys for value input options.") | Type of the input. |
| `value` | [`ref_holder_t<float>`](/api/common-types/ref-holder-t "This type acts as a proxy for reference variables that are used internally. Since Lua is a value-only language, it does not support references. Instead, an instance of this type is used to preserve interoperability with C++.") | Input value. |