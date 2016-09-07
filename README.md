# leccion20-ej2
Lección 20 / Ejercicio 2

Closures / Hoisting

El código muestra el mensaje JS coders love its callbacks, mientras que el resultado debería ser JS developers love its closures.

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
La palabra reservada var de la variable local feature ='callbacks' es eliminada, lo cual la convierte en una
variable global.

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
