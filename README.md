# 2º DAW | Desarrollo web en entorno cliente
###### José Luis Tejero Bermudo
## UD. 1 TAREA 2 

##### 1. Ventajas de incorporar el script desde un fichero externo frente a hacerlo en línea (código javascript directamente en el fichero HTML)
La principal ventaja es que el código será más limpio y legible. HTML y JavaScript son muy distintos entre sí por lo que es conveniente mantenerlos en archivos separados. Otra ventaja es que el navegador guarda en caché los archivos .js externos, por lo tanto se reduce el tiempo de carga de la página web.

##### 2. Atributos aplicables a la etiqueta script
- async: Especifica que el script se descargue mientras se analiza el HTML y hace que el análisis se pare para ejecutarlo cuando haya terminado de descargarse.
- defer: Especifica que el script se descargue mientras se analiza el HTML y, a diferencia del atributo *async*, el script se ejecutará cuando la página haya acabado el análisis.
- crossorigin: Controla si se mostrará información de errores cuando el script se obtiene de otros orígenes.
- integrity: Permite al navegador comprobar el script para asegurar que el código no se cargue si la fuente ha sido manipulada. 
- nomodule: Evita que un script se ejecute en navegadores que soportan scripts de módulo.
- referrerpolicy: Especifica qué información de referencia enviar cuando se recupera un script.
- fetchpriority: Su propósito es establecer la prioridad utilizada al recuperar el script.
- src: Especifica la URL de un script externo.
- type: Permite personalizar el tipo del script.

##### 3. Atributos por defecto

##### 4. Atributos booleanos. Qué implican.
En HTML algunos atributos son booleanos, lo cual implica que pueden ser *true* o *false*. La presencia de un atributo en un elemento representa el valor *true*, mientras que la ausencia del atributo representa el valor *false*.

Podríamos tomar como ejemplo lo siguiente, donde se usan los atributos booleanos *checked* y *disabled* de un label tipo checkbox:
```html
<label><input type="checkbox" checked name="ejemplo" disabled>Ejemplo</label>
```
Sería lo equivalente a hacer:
```html
<label><input type="checkbox" checked="checked" name="ejemplo" disabled="disabled">Ejemplo</label>
```

##### 5. Sitio recomendado para colocar la etiqueta script.
La forma moderna de hacerlo es colocar la etiqueta script dentro de la etiqueta \<head> y usar los atributos *async* o *defer* (dependiendo de si queremos que el script se ejecute mientras se analiza el HTML o cuando finalice el análisis), de forma que los scripts se descarguen lo antes posible sin bloquear el navegador.

Aquí se puede ver un ejemplo de la colocación y uso apropiado de la etiqueta:
```html
<!DOCTYPE html>
<html lang="es">
    <head>
        <title>Mi Página</title>
        <script src="script.js" type="text/javascript" defer></script>
    </head>
    <body>
    </body>
</html>
```

##### 6. Etiqueta noscript: utilidad, atributos y dónde colocar
La etiqueta \<noscript> se utiliza para definir un contenido alternativo que queramos que aparezca cuando el navegador o bien no soporta la ejecución de scripts, o están deshabilitados.

La etiqueta soporta los atributos globales en HTML tales como *id*, *class*, *spellcheck* o *accesskey* entre otros.

La etiqueta se puede utilizar dentro de la etiqueta \<head> o dentro de la etiqueta \<body>. Si se utiliza dentro de la etiqueta \<head>, suele afectar a etiquetas como \<link>, \<style> y \<meta>, de forma que permite realizar la carga alternativa de estos elementos en caso de que el navegador no permite la ejecución de scripts.

Un ejemplo del uso y colocación de la etiqueta \<noscript> puede ser el siguiente:
```html
<!DOCTYPE html>
<html lang="es">
    <head>
        <title>Mi Página</title>
        <script src="script.js" type="text/javascript"></script>
        <noscript>El navegador no soporta JavaScript.</noscript>
    </head>
    <body>
    </body>
</html>
```