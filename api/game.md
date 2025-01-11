## game

Usage: `game.{interface_or_function}`

This table exposes various internal services and global objects used by Fatality, and also provides a way to retrieve any additional services you need.

## global_vars

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`global_vars_t`](/api/game/global-vars-t "An instance of this type provides a way to read several global variables that are used by the game. Changing any of the values is not and will never be supported.")

This service exposes global variables used by the game, such as frame time or current server time.

## engine

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`cengine_client`](/api/game/cengine-client "An instance of this type provides a way to interface with Source 2's Engine-to-Client service.")

This service exposes the engine client, which includes commonly used engine-related functions.

## input

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`ccsgo_input`](/api/game/ccsgo-input "This type represents the game's command input system.")

This service exposes the command input system.

## input_system

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`cinput_system`](/api/game/cinput-system "This type represents the game's control input system.")

This service exposes the control input system.

## game_ui_funcs

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: [`cgame_ui_funcs`](/api/game/cgame-ui-funcs "This type represents the game's UI functions.")

This service exposes the game's UI functions.