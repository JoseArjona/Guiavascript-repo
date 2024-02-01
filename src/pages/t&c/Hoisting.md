---
layout: "../../layouts/ContentLayout.astro"
title: "Hoisting"
description: "El Hoisting es un comportamiento del motor de JavaScript que eleva las declaraciones de variables y funciones."
related: [{ href: "Scope", title: "Alcance" }]
---

El Hoisting es un comportamiento del motor de JavaScript que eleva las declaraciones de variables y funciones al principio del ámbito en el que se encuentran, antes de que se ejecuten otras líneas de código en el mismo ámbito.

Esto significa que las variables y funciones pueden ser utilizadas antes de ser declaradas.

```js
console.log(miVariable);

var miVariable = "Hola mundo!";

// En este ejemplo:
// "miVariable" se usa antes de ser declarada
// El motor de JavaScript eleva la declaración de "miVariable" al principio del ámbito
```

#### Puntos importantes:

- El Hoisting permite usar variables y funciones antes de declararlas.
- Las variables y funciones se elevan al principio del ámbito en el que se encuentran.
- Es importante tener cuidado al usar el Hoisting, ya que puede generar errores si no se utiliza correctamente.
- Se puede usar las palabras clave <span class="txt-blue">const y let</span> para evitar el Hoisting de variables.
