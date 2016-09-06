# leccion20-ej2
var feature = 'closures'; 
(function () {     
	if ( typeof feature === 'undefined' ){         
		var feature = 'callbacks';         
		console.log('JS coders love its ' + feature );     
	} else {         
		console.log('JS developers love its ' + feature );     
	} 
})();

### Solución:
Eliminar la palabra reservada "var" de ( var feature === 'callbacks') para que esta deje de ser local y se convierta 
en global.
