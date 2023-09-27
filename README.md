# PRIMERA PRÁCTICA DE PRUEBA DE DWEC
## ENUNCIADO DE LA PRÁCTICA

1. Ventajas de incorporar el script desde un fichero externo frente a hacerlo en línea (código javascript directamente en el fichero HTML)
(Respuesta a la pregunta)

```js
document.addEventListener("DOMContentLoaded", function() {
    // this function runs when the DOM is ready, i.e. when the document has been parsed
    document.getElementById("user-greeting").textContent = "Welcome back, Bart";
});
```