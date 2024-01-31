---
layout: "../../layouts/ContentLayout.astro"
title: "Guard Clauses"
description: "Las Guard Clauses son una técnica de refactorización que se utiliza para mejorar la legibilidad y la mantenibilidad del código."
---

Las Guard Clauses son una técnica de refactorización que se utiliza para
mejorar la legibilidad y la mantenibilidad del código. Consisten en
reemplazar una serie de condiciones anidadas por una única condición que
evalúa si la variable en cuestión tiene un valor válido. Ejemplo:

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
