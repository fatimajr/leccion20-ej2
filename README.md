# leccion20-ej2
Lección 20 / Ejercicio 2

Closures / Hoisting

El código muestra el mensaje JS coders love its callbacks, mientras que el resultado debería ser JS developers love its closures.
Esto es debido al fenónemo hoisting eleva la variable var feature = 'callbacks';  y le da el valor de undefined, lo que cumple
con la condición de la estructura if y muestra el mensaje " JS coders love its callbacks".

```javascript
var feature = 'closures'; 
(function () {     
    if ( typeof feature === 'undefined' ){         
        var feature = 'callbacks';         
        console.log('JS coders love its ' + feature );     
    } else {         
        console.log('JS developers love its ' + feature );     
    } 
})();
"JS coders love its callbacks"
```
#Solución:
La palabra reservada var de la variable local feature ='callbacks' es eliminada, lo cual la convierte en una variable global.
El hoisting prioriza las variables locales y al no encontrar ninguna, entonces toma el valor del la primera variable
global: var feature = 'closures';  y ejecuta el else, mostrando finalmente el mensaje: "JS developers love its closures".

```javascript
var feature = 'closures'; 
(function () {     
    if ( typeof feature === 'undefined' ){
    	feature = 'callbacks'
        console.log('JS coders love its ' + feature );     
    } else {         
        console.log('JS developers love its ' + feature );     
    } 
})();
"JS developers love its closures"
```
