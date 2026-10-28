# CodeMap

**CodeMap** es una herramienta en desarrollo para explorar la arquitectura de proyectos de software y entender cómo se relacionan sus archivos y módulos.

## Objetivo

Convertir la estructura de un repositorio en una vista comprensible de sus componentes, dependencias y posibles puntos de acoplamiento.

## Funcionalidades previstas

- **Mapa de dependencias:** visualizar las relaciones entre archivos y módulos.
- **Estructura del proyecto:** explorar directorios y componentes desde una vista unificada.
- **Puntos de entrada:** localizar archivos o módulos desde los que comienza la ejecución.
- **Acoplamiento:** señalar módulos con muchas relaciones o dependencias difíciles de mantener.
- **Informe de arquitectura:** generar un resumen de la organización del proyecto y sus relaciones.

Estas funciones son objetivos del proyecto, no capacidades implementadas todavía.

## Tecnología prevista

- **Rust** para el análisis del código y la extracción de relaciones.
- **TypeScript** para la interfaz de visualización.

La arquitectura y las tecnologías pueden cambiar durante el desarrollo.

## Estado

**Fase inicial — planificación.** Este repositorio contiene únicamente documentación y la licencia del proyecto. Todavía no incluye código ejecutable.

## Hoja de ruta inicial

1. Definir los lenguajes y formatos de proyecto que se analizarán primero.
2. Diseñar el modelo de datos para archivos, módulos y dependencias.
3. Implementar un análisis inicial de la estructura del repositorio.
4. Representar las dependencias en una interfaz navegable.
5. Añadir métricas de acoplamiento e informes de arquitectura.

## Licencia y uso

El proyecto está publicado en GitHub para que pueda consultarse públicamente, pero **no es software de código abierto**. Todos los derechos están reservados. La consulta pública del repositorio no concede permiso para copiar, modificar, redistribuir o utilizar el contenido fuera de los límites permitidos por la legislación aplicable. Consulta el archivo [LICENSE](./LICENSE).
