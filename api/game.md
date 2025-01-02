## game

Usage: `game.{interface_or_function}`

This table exposes various internal services and global objects used by Fatality, and also provides a way to retrieve any additional services you need.

## global_vars

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`global_vars_t`](https://lua.fatality.win/global-vars-t.html "An instance of this type provides a way to read several global variables that are used by the game. Changing any of the values is not and will never be supported.")

This service exposes global variables used by the game, such as frame time or current server time.

## engine

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`cengine_client`](https://lua.fatality.win/cengine-client.html "An instance of this type provides a way to interface with Source 2's Engine-to-Client service.")

This service exposes the engine client, which includes commonly used engine-related functions.