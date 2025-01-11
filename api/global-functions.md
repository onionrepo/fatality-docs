## Global Functions

Below is a list of all global functions. By “global”, we mean these functions do not require a preceding namespace - so you can call them directly, unlike other functions.

## print
[![Function][This field is a function and must be invoked using a dot (.)]rw]

Prints text to game's console.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `...` | ... | Values to print in the console. |

**Returns**

Nothing.

**Example**

```lua
print('Hello world!', 123); -- prints out "Hello world! 123" to the console
```

## error
[![Function][This field is a function and must be invoked using a dot (.)]rw]

Prints an error text to game's console, and shuts down the script. Try to avoid using this function - use it only if an error happens which you can't recover from.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `text` | string | Read [`print`](api/global-functions?id=print "Prints text to game's console.") for documentation. |

**Returns**

Nothing.

**Example**

```lua
error('Can\'t recover from this one! Error: ' .. tostring(123));
```