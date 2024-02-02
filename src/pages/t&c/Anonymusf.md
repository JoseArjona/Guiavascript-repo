---
layout: "../../layouts/ContentLayout.astro"
title: "Funciones Anónimas"
description: "Las funciones anónimas son funciones que no tienen nombre y se definen en el momento."
related: [{ href: "Hoisting", title: "Hoisting" }]
---

Las funciones anónimas son funciones que no tienen un nombre y se utilizan para realizar tareas específicas dentro de otra función o bloque de código.

En JavaScript, una función anónima es una función que se define sin usar la palabra clave `function` y un nombre. Se define usando una expresión de función.

```js
const sumar = function (numero1, numero2) {
  return numero1 + numero2;
};

const resultado = sumar(5, 10); // 15

// En este ejemplo:
// "sumar" es una variable que almacena una función anónima
// La función anónima recibe dos parámetros: "numero1" y "numero2"
// La función anónima devuelve la suma de "numero1" y "numero2"
// Se utiliza la función anónima para calcular la suma de 5 y 10
```

```js
// Version Arrow Function
const sumar = (numero1, numero2) => {
  return numero1 + numero2;
};

const resultado = sumar(5, 10); // 15
```

#### Puntos importantes:

- Las arrow functions son funciones anónimas
- Las funciones anónimas no sufren de Hoisting
- Pueden evitar errores y el código es más legibles y limpio.
