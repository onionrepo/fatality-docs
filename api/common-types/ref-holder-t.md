## ref_holder_t

This type acts as a proxy for reference variables that are used internally. Since Lua is a **value-only** language, it does not support references. Instead, an instance of this type is used to preserve interoperability with C++.

> Note that `<type>` indicates the specific type this instance holds. For example, if you see `ref_holder_t<float>`, it means the `val` field holds a float value and will **only** accept float values when it’s updated.

## val

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Type: `<type>`

Value holder. Use as the source value, or override it to change internally.