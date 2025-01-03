## managed

This type represents a managed object. You cannot create an instance of this type directly.

Every object, that inherits from this type, **must** be `create`d before use. The rendering system will only create them automatically, if you happen to lose a device object (e.g. minimize the game window, and then restore it) and **only** if you add your objects to manage table in [`draw`](/api/draw "This table describes the rendering system of the software.").

## obj

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]
[![Read Only][This field is a read only field, and you cannot change its value. This does not apply to child fields, if any.]r]

Type: [`ptr`](/api/common-types/ptr "This type is a literal pointer.")

Pointer to a GPU object. If this object is not created, this field will be `nil`. You can use the value of this field to pass it to [`command`](/api/draw/layer/command "This type is used to change render command parameters.") directly for example, or if you (for whatever reason we don't recommend you doing) want to have a direct control over the pointer - cast it to FFI's `cdata`.

## create

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Creates a managed object in GPU memory.

> You should `create()` an object only once. Invoking this method after the object was created will be meaningless.

**Arguments**

None.

**Returns**

Nothing.

**Example**

```lua
tex:create();
```

## destroy

[![Method][This field is a method and must be invoked using a colon (:).]rw]

Destroys a managed object in GPU memory.

> **Never** destroy a GPU object if it is being used in rendering (for example, when you have pushed some shape that uses a texture, and then destroyed that texture). This will lead to undefined behavior, and most likely, **crash the game**.

**Arguments**

None.

**Returns**

Nothing.

**Example**

```lua
font:destroy();
```