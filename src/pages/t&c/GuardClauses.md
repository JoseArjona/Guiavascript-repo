---
layout: "../../layouts/ContentLayout.astro"
title: "Guard Clauses"
description: "Las Guard Clauses son una técnica de refactorización que se utiliza para mejorar la legibilidad y la mantenibilidad del código."
---

Las Guard Clauses son una técnica de refactorización que se utiliza para
mejorar la legibilidad y la mantenibilidad del código.

Las Guard Clauses son como filtros que se usan al inicio de una función para evitar que se ejecute el código si no se cumplen ciertas condiciones.

Las Guard Clauses son una forma de evitar ejecutar código innecesario en una función. Permiten verificar si se cumplen ciertas condiciones antes de ejecutar el resto del código.

Sin Guard Clauses

```js
function userIsAdmin(user) {
  if (user.role == "admin") {
    if (user.manager == true) {
      return true;
    } else {
      return false;
    }
  } else {
    return false;
  }
}
```

Con Guard Clauses

```js
function userIsAdmin(user) {
  if (!user.role == "admin" || !user.manager) {
    return false;
  }
  return true;
}
```

#### Puntos importantes:

- Las Guard Clauses se usan para verificar condiciones al inicio de una función.
- Si la condición no se cumple, la función se detiene y no se ejecuta el resto del código.
- Las Guard Clauses ayudan a mejorar la legibilidad del código y a evitar errores.
