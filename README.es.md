# CodeMap

**[English](./README.md) · [Español](./README.es.md)**

CodeMap es un explorador de dependencias para entender cómo se relacionan los archivos de código de un proyecto.

**[Abrir la versión de GitHub Pages](https://ericsnet.github.io/CodeMap/)**

## Qué funciona en la vista previa actual

- Abrir una carpeta de proyecto desde el navegador, analizar un repositorio público de GitHub mediante su URL o cargar el grafo de demostración.
- Detectar relaciones de código habituales en JavaScript/TypeScript, Python, HTML, CSS y preprocesadores, Rust, C/C++, C#, Java, Kotlin, Go, PHP, Ruby, Swift, Dart, Vue/Svelte y algunos archivos de proyecto/configuración.
- Explorar un grafo de dependencias y una lista de archivos con búsqueda.
- Consultar qué archivos importa un archivo seleccionado y cuáles dependen de él.
- Mostrar un recuento sencillo de archivos aislados y ciclos aproximados.
- Exportar a JSON el grafo y las relaciones detectadas.

La vista previa es una aplicación estática que funciona en el navegador. Lee los archivos que seleccionas y no los sube a un servidor de CodeMap. La detección multilenguaje usa patrones de texto y heurísticas de rutas: no es un parser completo ni sustituye al análisis específico de cada lenguaje.

## GitHub Pages y uso local

### GitHub Pages

Entra en **https://ericsnet.github.io/CodeMap/**. Pages sirve como vista previa rápida, sin instalación. Puedes pulsar **Cargar demo**, seleccionar una carpeta o pegar una URL de un repositorio público (por ejemplo, `https://github.com/owner/repo`) en el campo de GitHub y pulsar **Analizar GitHub**. También puedes indicar una rama con una URL como `https://github.com/owner/repo/tree/nombre-rama`.

Una web alojada en GitHub Pages no puede leer silenciosamente cualquier carpeta de tu ordenador. Tienes que seleccionar explícitamente la carpeta o los archivos mediante el selector del navegador.

### Ejecutarlo en local

1. Descarga o clona este repositorio.
2. Abre `index.html` con un navegador moderno.
3. Pulsa **Cargar demo** o selecciona una carpeta de proyecto.

Esta vista previa no necesita gestor de paquetes, compilación, servidor ni cuenta. La función de GitHub consulta los metadatos mediante la API de GitHub y descarga los archivos desde `raw.githubusercontent.com`; no necesita un token de acceso.

## Limitaciones actuales

- El análisis de GitHub solo admite repositorios públicos. Los privados requieren autenticación y no son compatibles con esta vista previa.
- Los límites de la API de GitHub, restricciones de red o políticas CORS del navegador/red pueden impedir las descargas. Si ocurre, descarga o clona el repositorio y usa el selector de carpetas local.
- Se omiten directorios comunes de dependencias y archivos generados, archivos de más de 500 KB, y el análisis está limitado a 400 archivos candidatos y unos 8 MB por ejecución.
- La compatibilidad depende del estilo de dependencias: se intentan detectar enlaces locales en HTML, `@import`/`url()` en CSS, `mod` en Rust, includes entre comillas en C/C++ y patrones habituales de importación en otros lenguajes. La resolución de namespaces, macros, reglas del sistema de compilación, alias, código generado y dependencias dinámicas puede fallar.
- Se admiten rutas relativas y extensiones habituales; puede que no se resuelvan alias, paquetes, imports dinámicos, código generado ni muchas estructuras de paquetes Python.
- La detección de ciclos es aproximada: debe considerarse una pista, no una auditoría formal de arquitectura.
- El grafo muestra como máximo 100 archivos a la vez para mantener la legibilidad; la lista y la exportación JSON incluyen todos los archivos detectados.
- El motor de análisis en Rust y una interfaz TypeScript dedicada siguen siendo objetivos de desarrollo futuro; todavía no están integrados en esta vista previa.

## Hoja de ruta

1. Mejorar la resolución de imports y añadir pruebas automatizadas.
2. Crear un núcleo de análisis en Rust con un formato estable para grafos e informes.
3. Desarrollar una interfaz TypeScript más completa para repositorios grandes.
4. Añadir detección de puntos de entrada, métricas de acoplamiento e informes de arquitectura.
5. Ampliar los lenguajes compatibles y validar la detección de ciclos.

## Licencia

CodeMap puede consultarse públicamente en GitHub, pero **no es software de código abierto**. Todos los derechos están reservados. El acceso público no concede permiso para copiar, modificar, redistribuir ni utilizar de otro modo el contenido del proyecto, salvo en los casos permitidos por la legislación aplicable o con autorización previa por escrito. Consulta [LICENSE](./LICENSE).
