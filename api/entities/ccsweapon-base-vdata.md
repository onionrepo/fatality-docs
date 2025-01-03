## ccsweapon_base_vdata

This type represents a weapon's static data.

## built_right_handed

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon is designed for right-handed use.

## allow_flipping

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon can be flipped for left-handed use.

## linked_cooldowns

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon's cooldowns are linked with other weapons.

## flags

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

Represents various flags associated with the weapon.

## primary_ammo_type

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The type of ammo used in the primary clip.

## secondary_ammo_type

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The type of ammo used in the secondary clip.

## max_clip1

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The maximum number of rounds the primary clip can hold.

## max_clip2

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The maximum number of rounds the secondary clip can hold.

## default_clip1

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The default number of rounds in the primary clip.

## default_clip2

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The default number of rounds in the secondary clip.

## reserve_ammo_as_clips

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether reserve ammo is stored as additional clips.

## weight

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

Represents the weight of the weapon.

## auto_switch_to

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the game will automatically switch to this weapon when picked up.

## auto_switch_from

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the game will automatically switch away from this weapon.

## rumble_effect

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

Represents the rumble effect associated with this weapon.

## slot

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The inventory slot this weapon occupies.

## position

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The position of the weapon in the inventory slot.

## weapon_type

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`csweapon_type`](/api/entities/csweapon-type "This enum represents the weapon type in the game.")

The type of the weapon.

## weapon_category

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`csweapon_category`](/api/entities/csweapon-category "This enum represents the category classification for weapons in the game.")

The category of the weapon.

## gear_slot

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

Represents the gear slot associated with the weapon.

## gear_slot_position

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The position of the weapon in the gear slot.

## default_loadout_slot

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The default loadout slot for the weapon.

## s_wrong_team_msg

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `string`

The message displayed when the weapon is used by the wrong team.

## price

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The purchase price of the weapon.

## kill_award

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The cash reward given to the player for a kill with this weapon.

## primary_reserve_ammo_max

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The maximum amount of reserve ammo for the primary clip.

## secondary_reserve_ammo_max

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The maximum amount of reserve ammo for the secondary clip.

## melee_weapon

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon is classified as a melee weapon.

## has_burst_mode

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon has a burst fire mode.

## is_revolver

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon is classified as a revolver.

## cannot_shoot_underwater

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon cannot be fired underwater.

## name

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `string`

The internal name of the weapon.

## anim_extension

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `string`

The animation extension used by the weapon.

## e_silencer_type

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

Represents the type of silencer compatible with the weapon.

## crosshair_min_distance

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The minimum crosshair spread distance for this weapon.

## crosshair_delta_distance

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The change in crosshair spread distance when firing.

## is_full_auto

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon is fully automatic.

## num_bullets

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The number of bullets fired per shot.

## cycle_time

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The time between successive shots.

## max_speed

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The maximum movement speed of the player while holding this weapon.

## spread

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The base spread of the weapon when fired.

## inaccuracy_crouch

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The inaccuracy of the weapon while crouching.

## inaccuracy_stand

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The inaccuracy of the weapon while standing.

## inaccuracy_jump

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The inaccuracy of the weapon while jumping.

## inaccuracy_land

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The inaccuracy of the weapon upon landing from a jump.

## inaccuracy_ladder

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The inaccuracy of the weapon while climbing a ladder.

## inaccuracy_fire

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The inaccuracy of the weapon while firing.

## inaccuracy_move

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The inaccuracy of the weapon while moving.

## recoil_angle

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The angle of recoil for the weapon when fired.

## recoil_angle_variance

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The variance in the angle of recoil.

## recoil_magnitude

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The magnitude of recoil for the weapon.

## recoil_magnitude_variance

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<float>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The variance in the magnitude of recoil.

## tracer_frequency

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`cfiring_mode<int>`](/api/entities/ccsweapon-base-vdata/cfiring-mode "Firing mode information.")

The frequency of tracers visible when firing the weapon.

## inaccuracy_jump_initial

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The initial inaccuracy of the weapon upon jumping.

## inaccuracy_jump_apex

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The inaccuracy of the weapon at the apex of a jump.

## inaccuracy_reload

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The inaccuracy of the weapon after reloading.

## recoil_seed

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The seed value used for determining recoil patterns.

## spread_seed

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The seed value used for determining weapon spread.

## time_to_idle_after_fire

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The time it takes for the weapon to transition to idle after firing.

## idle_interval

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The time interval between idle animations for the weapon.

## attack_movespeed_factor

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The factor by which the player's movement speed is reduced while attacking with this weapon.

## heat_per_shot

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The heat generated by the weapon per shot.

## inaccuracy_pitch_shift

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The pitch shift caused by inaccuracy when firing.

## inaccuracy_alt_sound_threshold

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The threshold for inaccuracy at which an alternative sound is played.

## bot_audible_range

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The range at which bots can hear this weapon being fired.

## use_radio_subtitle

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `string`

Indicates whether this weapon uses radio subtitles for its actions.

## unzooms_after_shot

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the weapon unzooms automatically after firing.

## hide_view_model_when_zoomed

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `bool`

Indicates whether the view model is hidden when the weapon is zoomed in.

## zoom_levels

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The number of zoom levels available for this weapon.

## zoom_fov1

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The field of view (FOV) for the first zoom level.

## zoom_fov2

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The field of view (FOV) for the second zoom level.

## zoom_time0

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The time it takes to transition to the initial zoom state.

## zoom_time1

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The time it takes to transition to the first zoom level.

## zoom_time2

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The time it takes to transition to the second zoom level.

## iron_sight_pull_up_speed

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The speed at which the weapon's iron sights are pulled up.

## iron_sight_put_down_speed

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The speed at which the weapon's iron sights are put down.

## iron_sight_fov

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The field of view (FOV) when aiming down the weapon's iron sights.

## iron_sight_pivot_forward

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The forward pivot point for the weapon's iron sights.

## iron_sight_looseness

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The looseness of the weapon's iron sights when aiming.

## ang_pivot_angle

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).")

The pivot angle for the weapon's iron sights.

## vec_iron_sight_eye_pos

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).")

The eye position when aiming down the weapon's iron sights.

## damage

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The base damage dealt by the weapon.

## headshot_multiplier

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The multiplier applied to damage for headshots.

## armor_ratio

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The ratio determining how much damage penetrates armor.

## penetration

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The penetration power of the weapon for materials.

## range

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The effective range of the weapon.

## range_modifier

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The modifier applied to damage based on range.

## flinch_velocity_modifier_large

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The velocity modifier for large flinch effects.

## flinch_velocity_modifier_small

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The velocity modifier for small flinch effects.

## recovery_time_crouch

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The recovery time for accuracy when crouching.

## recovery_time_stand

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The recovery time for accuracy when standing.

## recovery_time_crouch_final

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The final recovery time for accuracy when crouching.

## recovery_time_stand_final

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The final recovery time for accuracy when standing.

## recovery_transition_start_bullet

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The starting bullet count for recovery transition.

## recovery_transition_end_bullet

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `int`

The ending bullet count for recovery transition.

## throw_velocity

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `float`

The velocity of thrown items (e.g., grenades).

## v_smoke_color

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`vector`](/api/common-types/vector "This type is a common 3D vector (x, y, z).")

The color of smoke effects for this weapon.

## anim_class

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: `string`

The animation class associated with this weapon.