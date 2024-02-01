---
layout: "../../layouts/ContentLayout.astro"
title: "Argumento"
description: "Un argumento es el valor que se pasa a una función cuando se invoca."
related: [{ href: "Params", title: "Parámetro" }]
---

Los argumentos son como los datos que le proporcionas a una función para que pueda trabajar y realizar una tarea específica.
Un argumento es el valor que se pasa a una función cuando se invoca.

Las funciones pueden tener cero o más argumentos. Los argumentos se especifican entre paréntesis después del nombre de la función.

```js
function sumar(numero1, numero2) {
  return numero1 + numero2;
}

const resultado = sumar(5, 10); // 15

// En este ejemplo:
// "sumar" es la función
// "numero1" y "numero2" son los parámetros de la función
 5 y 10 son los argumentos que se le pasan a la función
// "resultado" es la variable que almacena el valor devuelto por la función
```
