## draw

Usage: `draw.{func_or_field}`

This table describes the rendering system of the software.

> All types and enums described in the child sections **must** be prefixed with `draw.`. This is done so specific types are not confused with others, such as the separate `color` types present in rendering and the game.

## adapter

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `adapter`

Rendering adapter.

## frame_time

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

Rendering frame time. An alias to [`global_vars_t.frame_time`](https://lua.fatality.win/global-vars-t.html#frame-time "Type: float").

## time

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

Time, in seconds. An alias to [`global_vars_t.real_time`](https://lua.fatality.win/global-vars-t.html#real-time "Type: float").

## scale

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

Global DPI scale.

## display

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`vec2`](https://lua.fatality.win/vec2.html "This type is a 2D vector used within the rendering system.")

Display area size (viewport dimensions). [`cengine_client:get_screen_size`](https://lua.fatality.win/cengine-client.html#get-screen-size "Returns client window screen size.") will return exactly the same values. Overriding any of this vector's values will lead to an undefined behavior.

## textures

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`accessor<texture>`](https://lua.fatality.win/accessor.html "This type represents a safe way to access maps.")

A string to [`texture`](https://lua.fatality.win/texture.html "This type represents a texture object.") map of all managed textures. You can query and push textures with custom IDs. When you add a texture to this map, it will be automatically destroyed and recreated when required (such as when DX11 device gets lost).

> Built-in textures:
> * `gui_loading`: loading spinner
> * `gui_user_avatar`: current user's profile picture. May be nil if you don't have any avatar set
> * `gui_icon_up`: up chevron
> * `gui_icon_down`: down chevron
> * `gui_icon_copy`: copy icon
> * `gui_icon_paste`: paste icon
> * `gui_icon_add`: add icon
> * `gui_icon_search`: search icon
> * `gui_icon_settings`: settings icon (a cogwheel)
> * `gui_icon_bug`: bug icon
> * `gui_icon_key`.N: keyboard/mouse key icons. Replace N with the char code of a required button
> * `icon_rage`: RAGE tab icon
> * `icon_legit`: LEGIT tab icon
> * `icon_visuals`: VISUALS tab icon
> * `icon_misc`: MISC tab icon
> * `icon_scripts`: LUA tab icon
> * `icon_skins`: SKINS tab icon
> * `icon_cloud`: cloud icon
> * `icon_file`: file icon
> * `icon_refresh`: refresh icon
> * `icon_save`: save icon
> * `icon_configs`: "Configs" popup icon
> * `icon_keys`: keyboard icon
> * `icon_info`: "About" popup icon
> * `icon_close`: close icon (cross)
> * `icon_load`: load icon
> * `icon_import`: import icon
> * `icon_export`: export icon
> * `icon_delete`: delete icon
> * `icon_autoload`: "Autoload" icon
> * `icon_allow_insecure`: "Allow insecure" icon
> * `icon_cloud_upd`: cloud update icon
> * `player_texture`: player preview texture

## fonts

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`accessor<font_base>`](https://lua.fatality.win/accessor.html "This type represents a safe way to access maps.")

A string to [`font_base`](https://lua.fatality.win/font-base.html "This type represents the base class for font types. You cannot create an instance of this type. Instead, use the children types.") map of all managed fonts. You can query and push fonts with custom IDs. When you add a font to this map, it will be automatically destroyed and recreated when required (such as when DX11 device gets lost).

> Built-in fonts:
> * `gui_debug`: Verdana, 13px
> * `gui_title`: Figtree ExtraBold, 23px
> * `gui_main`: Figtree Medium, 14px
> * `gui_main_shadow`: Figree Medium, 14px, with shadow
> * `gui_main_fb`: Segoe UI Semibold, 14px
> * `gui_bold`: Figtree ExtraBold, 14px
> * `gui_bold_fb`: Segoe UI Black, 14px
> * `gui_semi_bold`: Figtree SemiBold, 14px
> * `gui_semi_bold_fb`: Segoe UI Bold, 14px

## shaders

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`accessor<shader>`](https://lua.fatality.win/accessor.html "This type represents a safe way to access maps.")

A string to [`shader`](https://lua.fatality.win/shader.html "This type represents a shader. HLSL documentation") map of all managed shader. You can query and push shader with custom IDs. When you add a shader to this map, it will be automatically destroyed and recreated when required (such as when DX11 device gets lost).

> Built-in shaders:
> * `blur_f`: gaussian blur shader

## surface

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`layer`](https://lua.fatality.win/layer.html "A layer is a type that is used to store render commands, as well as vertex and index data. This is the only way to push shapes and control rendering state.")

The layer you can render on.