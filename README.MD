### Binding to inputs

- `x-model` is used to "bind" the value of an _input element_ with a **data property**

  This means that anytime the value of the input changes, the value of "search" will change to reflect that

### Computed properties using getters

- `filteredItems` is a "getter" property in this object

- Because we are working directly inside the `x-data` object,
  we must reference any properties using `this.[property]` instead of simply `[property]`.

- Any time the value of `this.search` changes, parts of the `<template></template>` that use `filteredItems` will _automatically be updated_

### Looping elements

- `x-for` expressions take the following form: `[item] in [items]` where `[items]` is any **array of data**, and `[item]` is the **name of the variable** that will be assigned to an iteration inside the loop

- `x-for` is declared on a `<template>` element and not directly on the `<li>`. This is a requirement of using `x-for`. It allows Alpine to leverage the existing behavior of `<template></template>` tags in the browser to its advantage
