## Getting Started

Welcome to the basics of scripting with our API.

Fatality’s API is designed to mirror the software’s internal structure, giving you substantial control over its subsystems. Some features that could cause instability or damage are restricted.

> **Important Note:** Workshop scripts are currently unprotected and can potentially be extracted. Protection measures will be introduced soon.

## Basic Concepts
Our scripting engine uses LuaJIT 2.1 (with minor customizations). It’s fully compatible with Lua 5.1 and includes some Lua 5.2 enhancements.

The standard libraries `baselib`, `bit`, `ffi`, `math`, `string` and `table` are available. Note that the `ffi` library is **only** available if the **Allow insecure** option is enabled. Refer to [the official Lua documentation](https://www.lua.org/manual/5.1/) for more details.

If we ever modify any standard functions, we will document those changes to keep you informed.

## Documentation Overview
Throughout the API reference, you’ll encounter various labels used to describe a certain method or a field.

### Labels

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Function][This is a regular function that must be called using a dot (.).]rw]
[![Method][This field is a method and must be invoked using a colon (:).]rw]
[![Constructor][This is a constructor definition for this type.]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]
[![Insecure Only][This function exists only when "Allow insecure" is enabled.]i]

All the possible labels are listed above.

* **Field**: this label indicates that the item is a standard **field**. It's type will be explained just below the name.

* **Function**: this label indicates that the item is a **function**, which you call using a dot syntax (`obj.fn()`).

* **Method**: this label indicates that the item is a **method**, which is also a function, but it's advised to call it with the colon syntax (`obj:fn()`).

* **Constructor**: this label indicates that the item is a **constructor** definition. You don't have to call any field in particular, but instead you must invoke the **type itself** (example: `vector` has `__call`, meaning you should invoke it like this: `vector()`).

* **Read Only**: this label indicates that the item is **read only**, and it's value cannot be changed. Typically, this restriction does not extend to any child elements.

* **Insecure Only**: this label indicates that the item is **insecure only**, and won't be accessible when 'Allow insecure' is turned off in the Lua settings.

### Argument and return lists
Arguments and return values are listed in the exact order you must supply or capture them. For instance, if a parameter is shown first, it is to be passed as the first argument to the function. The same goes for return values: the first listed value will be placed in the first variable you declare, and so on.

### Types
Some type descriptions have special symbols in place:

* `type?` means that the type might be `nil`.

* `type<other>` means that inner methods or fields will use `other` type.

* `<other>` means that the type will be either `other`, or any of its child types.

## Rules

To keep your scripts safe and easy to use, we have quite a lot of safety measures in place. But, due to how specific stuff works, we are unable to fully make it as safe as possible. Therefore, here are some notes you should know before writing scripts:

### You Control the Lua State
You may replace or override API functions, but you’re responsible for maintaining stable behavior. If you encounter any bugs in the default API (**excluding FFI**), please report them so we can address the issue.

### Prioritize Safety
Using FFI grants you extensive freedom. Keep in mind that scripts which could harm users in any way are disallowed and will be removed. Whenever possible, **rely on the provided API** or request additional functionality if you need something not currently offered. Custom “script loaders” are strictly disallowed.

### Keep the Software Usable
Avoid hiding unrelated UI elements, obstructing user input, or interfering with the overall user experience. Scripts that disrupt functionality or harass users risk removal from the Workshop.