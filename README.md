# Curso práctico de IA generativa 2026

Materiales del curso **"Curso práctico de Inteligencia Artificial Generativa"**, con contenidos preparados para docencia, reutilización y exportación en distintos formatos.

El repositorio reúne principalmente:

- Presentaciones en Markdown.
- Exportaciones HTML y PDF de las diapositivas.
- Versiones PowerPoint de varias sesiones.
- Imágenes, logos y recursos visuales de apoyo.
- Kahoots en formato `.gift`.
- Notas de feedback y planificación de futuras ediciones.

## Contenido del curso

Los temas principales del curso incluyen:

- Introducción a la inteligencia artificial generativa.
- Introducción a los LLM.
- Introducción a ChatGPT.
- Prompt engineering.
- Comparativa de modelos LLM.
- Herramientas de IA gratuitas o freemium.

Además, el repositorio incorpora materiales complementarios para dinámicas de clase, revisión del curso y preparación de nuevas ediciones.

## Estructura del repositorio

```text
.
├── FEEDBACK.md                  # Notas de mejora y propuesta de agenda
├── kahoots/                     # Cuestionarios en formato GIFT
├── slides/
│   ├── md/                      # Fuente principal de las presentaciones
│   ├── export/                  # Exportaciones HTML tipo "book"
│   ├── ppt/                     # Exportaciones PDF y PPTX
│   ├── img/                     # Imágenes usadas en las sesiones
│   ├── logos/                   # Logos e iconografía
│   ├── templates/               # Plantillas de presentación/exportación
│   ├── lib/                     # Dependencias locales para reveal.js y otros recursos
│   └── build.properties         # Configuración de generación/exportación
└── curso-practico-ia-generativa-2026-v1.odt
```

## Punto de entrada recomendado

Si quieres revisar o editar el contenido del curso, empieza por los ficheros de [`slides/md/`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/slides/md), ya que ahí está el material fuente de las sesiones.

Archivos especialmente relevantes:

- [`slides/md/010-introduccion-IA-generativa.md`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/slides/md/010-introduccion-IA-generativa.md)
- [`slides/md/020-introduccion-LLMs.md`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/slides/md/020-introduccion-LLMs.md)
- [`slides/md/030-introduccion-ChatGPT.md`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/slides/md/030-introduccion-ChatGPT.md)
- [`slides/md/040-prompt-engineering.md`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/slides/md/040-prompt-engineering.md)
- [`slides/md/050-comparativa-modelos-LLM.md`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/slides/md/050-comparativa-modelos-LLM.md)
- [`slides/md/060-herramientas-IA-gratuitas.md`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/slides/md/060-herramientas-IA-gratuitas.md)

## Formato y generación de materiales

Por la estructura del proyecto y la configuración de [`slides/build.properties`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/slides/build.properties), las presentaciones están preparadas para trabajar con una cadena de generación basada en:

- [MarkdownSlides](https://github.com/asanzdiego/markdownslides)
- exportaciones a HTML, PDF y PowerPoint

En este repositorio ya se incluyen múltiples materiales generados, por lo que puede usarse directamente como repositorio de contenidos sin necesidad de reconstruirlo desde cero.

## Uso habitual

Algunas formas prácticas de aprovechar este repositorio:

- Consultar y actualizar los contenidos docentes en Markdown.
- Reutilizar las exportaciones ya generadas para impartir clase.
- Adaptar imágenes, ejemplos y comparativas para nuevas ediciones.
- Importar los ficheros de `kahoots/` en plataformas compatibles con formato GIFT.
- Revisar [`FEEDBACK.md`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/FEEDBACK.md) para iterar sobre el diseño del curso.

## Estado del repositorio

Este repositorio funciona como **base de materiales docentes** más que como aplicación software tradicional. Por eso:

- No hay un flujo de instalación documentado dentro del propio repositorio.
- Sí existen recursos fuente y exportados listos para edición y reutilización.
- Parte del contenido está actualizado específicamente para **marzo de 2026**.

## Licencia

Consulta el fichero [`LICENSE`](/home/adolfo/Cursos/2026/curso-practico-ia-generativa-2026/LICENSE).
