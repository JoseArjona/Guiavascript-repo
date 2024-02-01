---
layout: "../../layouts/ContentLayout.astro"
title: "Scope/Alcance"
description: "El alcance es el área de un programa en el que una variable o función es visible/usable."
related: [{ href: "Hoisting", title: "Hoisting" }]
---

<p>
        El alcance es el área de un programa en el que una variable o función es visible/usable. <br>
        Cada función tiene su propio Scope, y las variables declaradas dentro de una función no son accesibles fuera de ella. <br>
        El Scope se determina por la ubicación de la declaración de la variable o función.
</p>

```js
function miFuncion() {
  var miVariable = "Hola mundo!";
  console.log(miVariable); // "Hola mundo!"
}

console.log(miVariable); // Error: miVariable no está definida

// En este ejemplo:
// "miVariable" se declara dentro de la función "miFuncion"
// "miVariable" solo es accesible dentro de la función "miFuncion"
// Se produce un error al intentar acceder a "miVariable" fuera de la función
```

#### Puntos importantes:

- Se puede usar las palabras clave <span class="txt-blue">let y const</span> para crear un Scope de bloque.
- Las variables declaradas dentro de una función no son accesibles fuera de ella.
- El Scope se determina por la ubicación de la declaración.
