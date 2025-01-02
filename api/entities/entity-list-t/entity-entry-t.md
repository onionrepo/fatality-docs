## entity_entry_t

Represents an entity entry.

## entity

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `<type>`

Entity instance. Type depends on the list you get it from.

## had_dataupdate

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `bool`

`true` if the client had received any updates to this entity at least once.

## handle

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `chandle<type>`

Entity's handle. You **may** store this elsewhere if you need to have global access to an entity.

## avatar

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `texture`

> This field is only available on entries that use `cs2_player_controller` type.

Player's profile picture. Will be `nil` if was yet to be initialized.