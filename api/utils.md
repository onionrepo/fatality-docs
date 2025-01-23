## utils

Usage: `utils.{function}`

This table exposes various utility functions.

## base64_encode

[![Function][This is a regular function that must be called using a dot (.).]rw]

Encode a string to Base64 format.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `str` | `string` | Source string. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Base64-encoded string. |

**Example**

```lua
local enc = utils.base64_encode('Hello!'); -- SGVsbG8h
```

## base64_decode

[![Function][This is a regular function that must be called using a dot (.).]rw]

Decode Base64-encoded string.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `str` | `string` | Base64-encoded string. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Source string. |

**Example**

```lua
local dec = utils.base64_decode('SGVsbG8h'); -- Hello!
```

## get_unix_time

[![Function][This is a regular function that must be called using a dot (.).]rw]

Returns current time as UNIX timestamp.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Timestamp. |

**Example**

```lua
local ts = utils.get_unix_time();
```

## murmur2

[![Function][This is a regular function that must be called using a dot (.).]rw]

Returns MURMUR2-hashed string.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `str` | `string` | Source string. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Hash. |

**Example**

```lua
local hash = utils.murmur2('Hello');
```

## fnv1a

[![Function][This is a regular function that must be called using a dot (.).]rw]

Returns FNV1A-hashed string.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `str` | `string` | Source string. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Hash. |

**Example**

```lua
local hash = utils.fnv1a('Hello');
```

## find_export

[![Function][This is a regular function that must be called using a dot (.).]rw]
[![Insecure Only][This function exists only when 'Allow insecure' is enabled.]i]

Returns an address to an export in an image.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mod` | `string` | Image to look in. |
| `exp` | `string` | Export symbol. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Address, or `0` on failure. |

**Example**

```lua
local message_box = utils.find_export('user32.dll', 'MessageBoxA');
```

## find_pattern

[![Function][This is a regular function that must be called using a dot (.).]rw]
[![Insecure Only][This function exists only when 'Allow insecure' is enabled.]i]

Searches for a code pattern in an image.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `mod` | `string` | Image to search in. |
| `pattern` | `string` | Code pattern. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `int` | Address, or `0` on failure. |

**Example**

```lua
local something = utils.find_pattern('engine2.dll', 'DE AD ? ? ? ? BE EF');
```

## clipboard_get

[![Function][This is a regular function that must be called using a dot (.).]rw]
[![Insecure Only][This function exists only when 'Allow insecure' is enabled.]i]

Returns current clipboard content.

**Arguments**

None.

**Returns**

| Type | Description |
| ---- | ----------- |
| `string` | Clipboard content. |

**Example**

```lua
local clip = utils.clipboard_get();
```

## clipboard_set

[![Function][This is a regular function that must be called using a dot (.).]rw]
[![Insecure Only][This function exists only when 'Allow insecure' is enabled.]i]

Sets new clipboard content.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `str` | `string` | New content. |

**Returns**

Nothing.

**Example**

```lua
utils.clipboard_set('Hello!');
```