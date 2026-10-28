# CodeMap

**[English](./README.md) · [Español](./README.es.md)**

CodeMap es un explorador de dependencias para entender cómo se relacionan los archivos de código de un proyecto.

**[Abrir la versión de GitHub Pages](https://ericsnet.github.io/CodeMap/)**

## Qué funciona en la vista previa actual

- Abrir una carpeta de proyecto desde el navegador o cargar el grafo de demostración.
- Detectar imports relativos habituales y llamadas a `require` en JavaScript/TypeScript, además de imports básicos de Python.
- Explorar un grafo de dependencias y una lista de archivos con búsqueda.
- Consultar qué archivos importa un archivo seleccionado y cuáles dependen de él.
- Mostrar un recuento sencillo de archivos aislados y ciclos aproximados.
- Exportar a JSON el grafo y las relaciones detectadas.

La primera versión es una aplicación estática que funciona en el navegador. Lee los archivos que seleccionas y no los sube a un servidor de CodeMap. Todavía no es un analizador completo ni sustituye al análisis sintáctico específico de cada lenguaje.

## GitHub Pages y uso local

### GitHub Pages

Entra en **https://ericsnet.github.io/CodeMap/**. Pages sirve como vista previa rápida, sin instalación. Pulsa **Cargar demo** para probar la interfaz sin seleccionar un proyecto o selecciona una carpeta de tu dispositivo.

Una web alojada en GitHub Pages no puede leer silenciosamente cualquier carpeta de tu ordenador. Tienes que seleccionar explícitamente la carpeta o los archivos mediante el selector del navegador.

### Ejecutarlo en local

1. Descarga o clona este repositorio.
2. Abre `index.html` con un navegador moderno.
3. Pulsa **Cargar demo** o selecciona una carpeta de proyecto.

Esta vista previa no necesita gestor de paquetes, compilación, servidor ni cuenta.

## Limitaciones actuales

- La detección de dependencias se basa en patrones de texto, no en un parser completo del lenguaje.
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
