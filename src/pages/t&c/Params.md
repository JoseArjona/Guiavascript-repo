---
layout: "../../layouts/ContentLayout.astro"
title: "Parámetro"
description: "Los parámetros son las variables que se definen dentro de una función."
related: [{ href: "Arguments", title: "Argumento" }]
---

Los parámetros son las variables que se definen dentro de una función para recibir los datos que necesita para realizar su tarea.

Las funciones pueden tener cero o más parámetros. Los parámetros se definen entre paréntesis después del nombre de la función.

```js
function sumar(numero1, numero2) {
  return numero1 + numero2;
}

const resultado = sumar(5, 10); // 15

// En este ejemplo:
// "sumar" es la función
 "numero1" y "numero2" son los parámetros de la función
// 5 y 10 son los argumentos que se le pasan a la función
// "resultado" es la variable que almacena el valor devuelto por la función
```
