# Editor3s CSS Interactivos

Este proyecto está compuesto por dos versiones de un editor interactivo de CSS embebido en HTML. Está orientado a usuarios que quieran experimentar con estilos CSS directamente en el navegador y ver los resultados en tiempo real.

## Archivos del proyecto

### lanzador.html

![lanzador](https://github.com/user-attachments/assets/80d20b6f-05d6-4ce2-ad43-7d80a013c820)

Archivo de inicio del proyecto. Solo presenta botones para acceder a cualquiera de las dos versiones anteriores de forma rápida.

### index.html

![editor-css](https://github.com/user-attachments/assets/90ae63ec-ae1a-4566-80cb-4017a20fbe54)

Una versión básica del editor que permite modificar el contenido CSS directamente dentro de una etiqueta <style> con contenteditable="true". Las modificaciones se aplican inmediatamente sobre los elementos de la página sin necesidad de recargar.

✅ Edición rápida e inmediata

❌ Sin resaltado de sintaxis

❌ Sin validación ni autocompletado

### indexValidacion.html

![editor-css-avanzado](https://github.com/user-attachments/assets/ed53a1ff-9cb4-4100-9c81-5cd9f605b431)

Una versión un poco más avanzada que utiliza CodeMirror para proporcionar:

✅ Resaltado de sintaxis CSS

✅ Autocompletado con Ctrl + Espacio

✅ Validación de errores de sintaxis con CSSLint

✅ Aplicación inmediata de estilos conforme se escribe

✅ Ejemplos incluidos (imagen y tabla para estilizar)

Esta versión es un poco mas chanchi para usuarios que desean una experiencia "similarmente más parecida" a un editor profesional.

## Instrucciones

Abre lanzador.html en tu navegador.

Elige una de las versiones disponibles del editor:

Editor CSS Básico (index.html)

Editor CSS Avanzado (indexValidacion.html)

Comienza a escribir o modificar el código CSS y observa los cambios en tiempo real.

## ⚠️ Limitaciones y Consideraciones

- **Compatibilidad de CSSLint**: La validación de CSS funciona correctamente solo si `CSSLint` está disponible globalmente. Se recomienda usar la versión `1.0.5`, cargada antes de `css-lint.min.js`.
  
- **Orden de carga de scripts**: Asegúrate de que los scripts se cargan en el siguiente orden:
  1. `csslint.min.js`
  2. `lint.min.js`
  3. `css-lint.min.js`

- **Integración con CodeMirror**: Esta integración depende de versiones específicas de `CodeMirror` (probado con `5.65.16`).

- **Validación en tiempo real**: La validación se activa cuando el contenido del editor cambia. Si ves que no se muestran errores, revisa la consola del navegador por posibles conflictos de versiones o errores de carga.

