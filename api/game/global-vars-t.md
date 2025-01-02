## global_vars_t

Usage: `game.global_vars.{field}`

An instance of this type provides a way to read several global variables that are used by the game. Changing any of the values is not and will never be supported.

## real_time

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Time passed since the game start, in seconds.

## frame_count

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `int`

Amount of frames rendered since the game start.

## abs_frame_time

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Absolute (averaged) frame time. It is calculated over a set of previous frame times, and should not be used for anything that requires accurate frame time like animation.

## max_clients

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `int`

Maximum amount of clients on the current server.

## ticks_this_frame

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `int`

Amount of ticks passed during the currently rendered frame. Any value above 1 might indicate a stall during rendering.

## frame_time

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Time, in which a previous frame was rendered. May be used for animation or by any other means that require accurate frame time.

## cur_time

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Time passed since the **server**'s game start. This does not indicate the accurate time on the server, although in several events it might be synced by the software.

## tick_fraction

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `float`

Current tick's fractional value.

## tick_count

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `int`

Ticks passed since the **server**'s game start.

## map_path

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `string`

Relative path to current loaded map's file.

## map_name

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `string`

Name of the currently loaded map.