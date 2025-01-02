## text_params

This type is used to determine text alignment.

> Line alignment only makes sense if you have multiple lines in your text. By default, all next lines will start from the left side of the text. You can change this behavior by using one of the functions that take `line` as a parameter. For example, if you pass `right` to the line alignment, all next lines will start from the right side. Text alignment will remain as dictated by `v` and `h` parameters.

## with_v

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Creates `text_params` instance with vertical alignment.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `v` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Vertical alignment. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `text_params` | Created text params. |

**Example**

```lua
local align_top = draw.text_params.with_v(draw.text_alignment.top);
```

## with_h

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Creates text_params instance with horizontal alignment.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `h` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Horizontal alignment. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `text_params` | Created text params. |

**Example**

```lua
local align_right = draw.text_params.with_h(draw.text_alignment.right);
```

## with_line

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Creates text_params instance with line alignment.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `line` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Line alignment. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `text_params` | Created text params. |

**Example**

```lua
local lines_center = draw.text_params.with_line(draw.text_alignment.center);
```

## with_vh

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Creates text_params instance with vertical and horizontal alignments.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `v` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Vertical alignment. |
| `h` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Horizontal alignment. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `text_params` | Created text params. |

**Example**

```lua
local align_bottom_right = draw.text_params.with_vh(draw.text_alignment.bottom, draw.text_alignment.right);
```

## with_vline

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Creates text_params instance with vertical alignment and line alignment.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `v` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Vertical alignment. |
| `line` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Line alignment. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `text_params` | Created text params. |

**Example**

```lua
local align = draw.text_params.with_vline(draw.text_alignment.bottom, draw.text_alignment.center);
```

## with_hline

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Creates text_params instance with horizontal alignment and line alignment.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `h` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Horizontal alignment. |
| `line` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Line alignment. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `text_params` | Created text params. |

**Example**

```lua
local align = draw.text_params.with_hline(draw.text_alignment.center, draw.text_alignment.center);
```

## with_vhline

[![Function][This field is a function and must be invoked using a dot (.)]rw]

Creates text_params instance with vertical, horizontal and line alignments.

**Arguments**

| Name | Type | Description |
| ---- | ---- | ----------- |
| `v` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Vertical alignment. |
| `h` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Horizontal alignment. |
| `line` | [`text_alignment`](https://lua.fatality.win/text-alignment.html "This enum determines how to align the text when drawing it.") | Line alignment. |

**Returns**

| Type | Description |
| ---- | ----------- |
| `text_params` | Created text params. |

**Example**

```lua
local align = draw.text_params.with_vhline(draw.text_alignment.center, draw.text_alignment.center);
```