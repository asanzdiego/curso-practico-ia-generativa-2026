% De un PDF a la web de notas de corte de las universidades de Madrid con ayuda de IA

# Introducción

Hay proyectos pequeños que explican muy bien qué significa usar inteligencia artificial de forma realista en desarrollo de software. La web [Notas de corte de las universidades de Madrid curso 2025-2026](https://asanzdiego.github.io/notas-de-corte-universidades-madrid-25-26/) es uno de ellos. No por su complejidad técnica, sino porque muestra cómo la IA puede actuar como copiloto para convertir una fuente difícil de explotar en una aplicación web clara, útil y publicada en abierto.

Lo más interesante no es solo la interfaz final, sino la forma de trabajar. El proyecto se organizó en **tres fases**:

1. extraer datos desde un **PDF a CSV**,
2. transformar ese **CSV a JSON** y
3. construir la **interfaz web**.

Esa separación ayudó mucho a colaborar con la IA, revisar resultados intermedios y reducir fricción técnica.

# Contexto del proyecto

El [repositorio del proyecto](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26) reúne tanto la preparación de datos como la parte front-end. En la carpeta [data](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/tree/main/data) aparecen el [PDF de origen](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/notas-de-corte-universidades-madrid-25-26.pdf), el [CSV resultante](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/notas-de-corte-universidades-madrid-25-26.csv), el [JSON consumido por la aplicación](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/notas-de-corte-universidades-madrid-25-26.json) y dos cuadernos de Jupyter: uno para la [extracción de PDF a CSV](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/extraccion-notas-de-corte-de-pdf-a-csv.ipynb) y otro para la [transformación de CSV a JSON](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/extraccion-notas-de-corte-de-pdf-a-csv.ipynb)

La [aplicación publicada]((https://asanzdiego.github.io/notas-de-corte-universidades-madrid-25-26/)) permite consultar las notas de corte mediante **filtros por universidad, rama de estudios, titulación y nota**, además de ordenar los resultados. La interfaz responde a esa necesidad con filtros en la parte superior y una tabla de resultados abajo, pensada para consultar la información de forma cómoda.

# Fase 1: del PDF al CSV

La primera fase fue una de las más importantes del proyecto. El punto de partida era un [PDF con la información de las notas de corte](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/notas-de-corte-universidades-madrid-25-26.pdf). A partir de ahí, con ayuda de IA, se diseñó y refinó un [cuaderno de Jupyter para extraer los datos relevantes y volcarlos en un fichero CSV estructurado](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/extraccion-notas-de-corte-de-pdf-a-csv.ipynb).

Aquí hay una idea clave: **pasar de PDF a CSV ya aporta mucho valor**. Un PDF puede ser cómodo para leer, pero no para reutilizar. En cambio, un CSV permite revisar, filtrar, corregir, analizar y reutilizar los datos con mucha más facilidad. Incluso sin llegar a construir la web, esta conversión inicial ya habría sido útil por sí misma.

Además, esta fase muestra bien el papel real de la IA. Puede ayudar a plantear la extracción y proponer una primera solución, pero después hace falta revisar si los campos se han interpretado bien y si la estructura resultante es correcta. La IA acelera, pero no sustituye el criterio humano.

# Fase 2: del CSV al JSON

Una vez [obtenido el CSV](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/notas-de-corte-universidades-madrid-25-26.csv), el siguiente paso fue transformarlo en un [JSON listo para ser consumido por la web](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/notas-de-corte-universidades-madrid-25-26.json). En el proyecto esto se resolvió con un segundo [cuaderno de Jupyter para transformar el CSV a JSON](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/data/extraccion-notas-de-corte-de-pdf-a-csv.ipynb)-

Este paso fue muy acertado desde el punto de vista de la mantenibilidad. El CSV funciona bien como formato intermedio de trabajo y revisión, mientras que el JSON encaja mejor con una aplicación web en cliente. Separar ambos formatos hace que el proyecto sea más claro, reutilizable y fácil de evolucionar.

También refuerza una idea importante: el reto no estaba solo en la interfaz. **Preparar bien los datos** era una parte esencial del proyecto, y ese trabajo previo condicionaba el buen funcionamiento de la web.

# Fase 3: del JSON a una web responsive

Con los datos ya preparados, la última fase consistió en generar la parte front-end usando exclusivamente 3 fihceros:

1. un [index.html](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/index.html),
2. un [script.js](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/script.js) y
3. un [styles.css](https://github.com/asanzdiego/notas-de-corte-universidades-madrid-25-26/blob/main/styles.css).

Esa decisión ayudó a mantener la aplicación sencilla, portable y fácil de entender.

La interfaz no se limita a mostrar una tabla. Incluye filtros por universidad y rama, búsqueda por titulación, control del rango de nota y ordenación de resultados. Todo ello permite consultar la información de manera práctica y clara. Además, la web se planteó como una **interfaz responsive**, pensada para adaptarse correctamente a distintos tamaños de pantalla.

Esta fase deja otra lección útil: la parte visual era importante, pero no era el único desafío. La calidad de la experiencia final dependía también de haber construido antes una base de datos limpia y bien estructurada.

# Publicación de la web con GitHub Pages

El proyecto se cerró con la publicación de la aplicación mediante [GitHub Pages](https://docs.github.com/es/pages). Esto permitió utilizar el propio repositorio no solo como fuente del código, sino también como canal de despliegue.

Tiene bastante valor práctico y didáctico. El repositorio reúne los datos, los cuadernos de transformación, los archivos del front-end y la web ya publicada. Gracias a [GitHub Pages](https://docs.github.com/es/pages), el proyecto completa todo el ciclo: preparación de datos, interfaz y puesta en producción en un formato accesible desde navegador.

# Qué aportó la IA en cada fase

La IA aportó valor de forma distinta en cada etapa. En la extracción ayudó a estructurar el cuaderno para convertir el PDF en un formato utilizable. En la transformación facilitó la limpieza y normalización necesarias para generar un JSON coherente. Y en la fase final aceleró la creación de una interfaz funcional, responsive y fácil de usar.

Pero quizá su mayor aportación fue ayudar a **ordenar el trabajo**. Dividir el proyecto en fases permitió plantear mejor las peticiones, validar cada resultado intermedio y construir la solución con más control. Pedir primero los cuadernos de transformación y después la interfaz fue una estrategia especialmente acertada.

# Retos, correcciones y validación humana

Conviene insistir en que aquí no hubo magia, sino iteración. En un flujo de este tipo siempre hay que comprobar si el PDF se ha interpretado bien, si el CSV quedó correctamente estructurado, si el JSON conserva los campos necesarios y si los filtros y la ordenación funcionan como se espera.

Eso resume bien el papel real de la IA en este proyecto: **aceleró el desarrollo, redujo fricción y propuso soluciones útiles**, pero **fue necesaria una supervisión humana** constante para revisar, corregir, probar y ajustar. La IA actuó como copiloto técnico, no como sustituto del trabajo humano.

# Conclusión

La web de notas de corte de las universidades de Madrid 2025-2026 es un buen ejemplo de uso práctico de IA aplicada al desarrollo de software. No por su tamaño, sino porque muestra que, con una estrategia clara por fases, la IA puede ayudar de verdad en proyectos sencillos y útiles.

También deja una enseñanza importante: el valor del proyecto **empieza antes de la web**. Empieza cuando una información encerrada en un PDF se convierte en un CSV reutilizable, continúa con su transformación a JSON y culmina con una interfaz accesible publicada con GitHub Pages.

A veces se habla de IA aplicada al desarrollo como si solo tuviera sentido en proyectos grandes. Este caso demuestra lo contrario. Un proyecto pequeño y bien acotado puede ser un excelente ejemplo de uso realista y productivo de IA: **no para sustituir el trabajo técnico, sino para hacerlo más fluido, ordenado y eficiente**.




