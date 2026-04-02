% Prompt Engineering
% Adolfo Sanz De Diego
% Marzo 2026



# Introducción



## ¿Qué es Prompt Engineering?

- **Definición**:
    - Disciplina orientada a **diseñar, estructurar y optimizar instrucciones** para modelos de IA generativa con el fin de obtener respuestas **más útiles, precisas, consistentes y adaptadas al contexto**.
- **Qué incluye realmente**:
    - No consiste solo en “hacer una buena pregunta”. Implica también decidir, entre otras, **qué contexto aportar**, **qué rol asignar**, **que público objetivo**, **qué restricciones fijar**, **qué formato exigir**, **qué ejemplos mostrar**, **que acciones realizar**, etc.
- **Ámbito actual**:
    - Hoy un prompt puede incluir no solo **texto**, sino también **imágenes, audio, vídeo, tablas, documentos, código** u otros materiales, según el sistema utilizado.
- **Objetivo principal**:
    - Reducir ambigüedad, orientar mejor el comportamiento del modelo y conseguir salidas **más fiables y aprovechables**.
- **Ejemplo básico**:
    - Comparar: **“Resume el texto”** frente a **“Resume este artículo en 3 ideas clave, en formato Markdown, para un público técnico, para publicarlo en LinkedIn”**.
- **Idea clave**:
    - Un prompt no es solo una orden: es una **especificación de tarea**.

## Importancia de los prompts

- **Impacto directo en los resultados**:
    - La forma en que se formula la petición influye de manera decisiva en la **calidad, profundidad, estructura y utilidad** de la respuesta.
- **Mayor precisión**:
    - Un buen prompt ayuda al modelo a entender, entre otras, **qué se quiere**, **para quién**, **con qué nivel**, **en qué formato**, **con qué límites**, etc.
- **Eficiencia**:
    - Prompts bien diseñados reducen iteraciones innecesarias y ahorran **tiempo, coste y esfuerzo**.
- **Consistencia**:
    - Cuando se usan plantillas o instrucciones estables, resulta más fácil obtener respuestas **repetibles** y comparables.
- **Flexibilidad**:
    - Permiten adaptar la salida a tareas muy distintas: **redacción**, **resumen**, **clasificación**, **extracción**, **traducción**, **programación**, **análisis documental**, **generación de ideas** o **creación multimodal**.
- **Fiabilidad operativa**:
    - En contextos profesionales, un buen prompting mejora la **robustez del flujo de trabajo**, sobre todo cuando las respuestas se reutilizan en procesos, informes, formularios, aplicaciones o automatizaciones.
- **Importancia creciente**:
    - Aunque los modelos actuales suelen seguir instrucciones cada vez mejor, el **prompt engineering sigue siendo clave** en tareas complejas, especializadas, largas o con requisitos estrictos.



# Partes más importantes



## Contexto

- Añade **el contexto relevante** para que el modelo entienda mejor la tarea:
    - Objetivo.
    - Tema o dominio.
    - Información previa.
    - Restricciones del entorno.
    - Materiales de referencia.
- Puedes aportar:
    - **Texto**.
    - **Documentos**.
    - **Tablas**.
    - **Imágenes**.
    - **Código**.
    - **Enlaces**.
    - **Datos estructurados**.
- No se trata de añadir “todo” sin criterio, sino de aportar **todo lo necesario y útil**.
- Cuanto más ambiguo sea el problema, más importante suele ser el contexto.
- Es recomendable separar con claridad:
    - **Instrucciones**.
    - **Contexto**.
    - **Datos de entrada**.
    - **Ejemplos**.
- La cortesía no es lo más importante; lo esencial es la **claridad**, la **precisión** y la **ausencia de ambigüedad**.

## Actor y público

- Indica **qué papel o perspectiva** debe adoptar el modelo:
    - Profesor.
    - Analista.
    - Programador.
    - Traductor.
    - Revisor.
    - Experto jurídico.
    - Divulgador.
- Definir el actor ayuda a ajustar:
    - El nivel técnico.
    - El vocabulario.
    - La profundidad.
    - El enfoque.
    - El tipo de explicación.
- También conviene indicar **a quién va dirigida la respuesta**:
    - Un alumno de primaria.
    - Un estudiante de secundaria.
    - Un público universitario.
    - Un equipo técnico.
    - Un directivo.
    - Un usuario sin conocimientos previos.
- Cuanto mejor se defina el público, más fácil será obtener una respuesta adecuada en:
    - **registro**,
    - **complejidad**,
    - **densidad conceptual**,
    - **ejemplificación**.
- Ejemplo:
    - **“Actúa como profesor de secundaria y explica este concepto para alumnado de 4.º de ESO con ejemplos sencillos y lenguaje claro.”**

## Acción

- Indica claramente **la acción que quieres que realice** el modelo:
    - Escribe.
    - Genera.
    - Crea.
    - Resume.
    - Expande.
    - Corrige.
    - Reescribe.
    - Traduce.
    - Convierte.
    - Clasifica.
    - Identifica.
    - Compara.
    - Evalúa.
    - Extrae.
    - Ordena.
- La acción debe ser **específica y observable**.
- Es mejor pedir:
    - **“Clasifica estas incidencias en 4 categorías y justifica cada clasificación en una frase”**
    - que pedir solo:
    - **“Analiza estas incidencias”**.
- Si la tarea es compleja, conviene descomponerla en pasos o subacciones.

## Restricciones

- Indica lo que **debe** y lo que **no debe** hacer el modelo.
- Algunas restricciones útiles son:
    - Idioma de salida.
    - Extensión máxima o mínima.
    - Temas que debe evitar.
    - Nivel técnico permitido.
    - Estructura obligatoria.
    - Prohibición de inventar datos.
    - Necesidad de reconocer incertidumbre.
- Ejemplos:
    - **“Responde en español de España.”**
    - **“No inventes referencias bibliográficas.”**
    - **“Si falta información, indícalo explícitamente.”**
    - **“No uses tablas.”**
    - **“No superes las 200 palabras.”**
- Las restricciones son especialmente importantes cuando el resultado:
    - se publicará,
    - se evaluará,
    - se integrará en un sistema,
    - o se reutilizará automáticamente.

## Ejemplos

- Indica **uno o varios ejemplos** de cómo quieres la respuesta.
- Los ejemplos ayudan a mostrar:
    - el formato esperado,
    - el nivel de detalle,
    - el tono,
    - el criterio de clasificación,
    - el tipo de transformación deseada.
- Suelen ser muy útiles cuando quieres:
    - respuestas homogéneas,
    - salidas estructuradas,
    - clasificación consistente,
    - o adaptación a un estilo concreto.
- Conviene que los ejemplos sean:
    - **claros**,
    - **correctos**,
    - **representativos**,
    - **diversos**.
- Un mal ejemplo puede empeorar el resultado, porque el modelo tenderá a imitarlo.

## Formato de salida

- Indica el **formato exacto** en que quieres la respuesta:
    - Lista.
    - Tabla.
    - Esquema.
    - Mapa mental.
    - Párrafos.
    - Markdown.
    - HTML.
    - JSON.
    - CSV.
    - XML.
    - Código.
- Cuanto más explícito sea el formato, más fácil será:
    - leer la respuesta,
    - reutilizarla,
    - validarla,
    - procesarla automáticamente.
- En tareas técnicas o integradas en aplicaciones, puede ser preferible pedir una **estructura rígida**.
- Ejemplo:
    - **“Devuelve la respuesta en JSON con los campos `titulo`, `resumen`, `riesgos` y `recomendaciones`.”**
- Cuando el resultado deba ser consumido por software, conviene definir:
    - campos obligatorios,
    - valores permitidos,
    - y tratamiento de datos ausentes.

## Tono

- Indica el **tono** deseado:
    - Formal.
    - Informal.
    - Profesional.
    - Cercano.
    - Persuasivo.
    - Expositivo.
    - Crítico.
    - Motivador.
    - Neutral.
- El tono influye en la percepción del mensaje, aunque no cambie el contenido esencial.
- Puede adaptarse al contexto:
    - educativo,
    - institucional,
    - comercial,
    - divulgativo,
    - técnico.
- Ejemplo:
    - **“Explica el tema con tono didáctico, claro y profesional, sin sonar demasiado académico.”**

## Estilo

- Indica el **estilo de redacción**:
    - Científico.
    - Técnico.
    - Argumentativo.
    - Periodístico.
    - Académico.
    - Divulgativo.
    - Literario.
    - Publicitario.
- El estilo afecta a:
    - la organización del discurso,
    - la selección léxica,
    - la densidad conceptual,
    - el tipo de ejemplos,
    - la forma de enlazar ideas.
- También puede ser útil pedir características concretas del estilo:
    - frases cortas,
    - lenguaje sencillo,
    - estructura muy visual,
    - uso moderado de tecnicismos,
    - presencia o ausencia de metáforas.

## Longitud de la respuesta

- Indica el **número aproximado** de:
    - palabras,
    - caracteres,
    - frases,
    - párrafos,
    - apartados,
    - viñetas.
- También puedes pedir el grado de desarrollo:
    - **breve**,
    - **conciso**,
    - **ampliado**,
    - **detallado**,
    - **profundo**.
- Es mejor concretar:
    - **“En 5 viñetas”**,
    - **“En un máximo de 150 palabras”**,
    - **“En 3 apartados y una conclusión”**,
    - que limitarse a decir:
    - **“Hazlo corto”**.
- En tareas complejas, la longitud debe alinearse con el objetivo real: una respuesta demasiado corta puede ser incompleta y una demasiado larga puede dificultar su uso.

## Criterios de calidad y verificación

- Además de pedir una tarea, conviene indicar **cómo debe considerarse correcta** la respuesta.
- Puedes fijar criterios como:
    - exactitud factual,
    - claridad,
    - completitud,
    - coherencia,
    - ausencia de repeticiones,
    - neutralidad,
    - trazabilidad,
    - uso de fuentes.
- Ejemplos:
    - **“Separa hechos, inferencias y opiniones.”**
    - **“Indica dudas o lagunas de información.”**
    - **“Comprueba al final si has cumplido todos los requisitos.”**
    - **“No cites normas o artículos que no estés seguro de poder identificar correctamente.”**
- Esto resulta especialmente útil en tareas de:
    - análisis,
    - revisión,
    - clasificación,
    - extracción,
    - asesoramiento,
    - documentación.

## Delimitadores y estructura

- En prompts largos o complejos, conviene separar bien cada bloque mediante:
    - títulos,
    - listas,
    - comillas triples,
    - etiquetas,
    - bloques XML,
    - secciones numeradas.
- Esta separación ayuda a distinguir:
    - las instrucciones,
    - los documentos de referencia,
    - los ejemplos,
    - y la entrada variable.
- Ejemplo de estructura útil:


```text
[INSTRUCCIONES]
...

[CONTEXTO]
...

[DATOS DE ENTRADA]
...

[FORMATO DE SALIDA]
...
```

- Una buena estructura mejora la interpretación y reduce errores de lectura del prompt.

## Fuentes, documentos y materiales de apoyo

- Cuando la tarea depende de información concreta, es recomendable aportar:
    - documentos,
    - normativa,
    - artículos,
    - datos,
    - tablas,
    - ejemplos reales.
- Si el modelo debe basarse solo en cierto material, conviene decirlo expresamente.
- Ejemplos:
    - **“Responde únicamente con base en el documento adjunto.”**
    - **“Si el dato no aparece en las fuentes aportadas, indícalo.”**
    - **“Prioriza la normativa más reciente.”**
- En tareas con documentación extensa, también ayuda indicar:
    - qué partes son prioritarias,
    - qué documentos son más fiables,
    - y qué información debe ignorarse.



# Técnicas avanzadas



## Zero-shot

- Consiste en pedir una tarea **sin aportar ejemplos previos**.
- En muchos casos funciona bien, sobre todo con tareas sencillas o muy conocidas.
- Es una buena forma de empezar cuando quieres comprobar si el modelo ya entiende la instrucción con claridad.
- Suele ser suficiente para:
    - resúmenes simples,
    - reformulaciones,
    - traducciones,
    - lluvia de ideas,
    - explicaciones generales.
- Aun así, incluso en zero-shot conviene especificar:
    - objetivo,
    - público,
    - formato,
    - restricciones.

## Few-shot

- Consiste en añadir **uno o varios ejemplos** de entrada y salida.
- Es especialmente útil cuando quieres enseñar al modelo:
    - un patrón,
    - un formato,
    - un criterio de clasificación,
    - un estilo,
    - o una convención propia.
- Suele mejorar la consistencia en tareas como:
    - etiquetado,
    - extracción,
    - normalización,
    - corrección,
    - generación con formato fijo.
- Los ejemplos deben parecerse al tipo de casos reales que esperas procesar.
- No conviene abusar de ejemplos repetitivos o poco representativos.

## Cadena de pensamiento (CoT)

- Tradicionalmente, la **cadena de pensamiento** se ha usado para pedir al modelo que razone paso a paso.
- Esta técnica puede ayudar en algunos contextos, sobre todo cuando la tarea requiere:
    - descomposición lógica,
    - cálculos,
    - planificación,
    - comparación entre alternativas.
- Sin embargo, conviene actualizar esta idea:
    - en algunos **modelos de razonamiento actuales**, pedir explícitamente **“piensa paso a paso”** no siempre mejora el resultado y puede ser innecesario.
- En muchos casos es preferible pedir:
    - **una respuesta final clara**,
    - **una comprobación breve**,
    - o **una justificación resumida**,
    - en lugar de solicitar un razonamiento extenso en todos los casos.
- Una alternativa más útil puede ser:
    - **“Resuelve el problema y verifica al final si cumples todas las restricciones.”**

## Cadena de prompting

- Consiste en **dividir una tarea compleja en tareas más pequeñas** y resolverlas una a una.
- Puede hacerse de dos formas:
    - diseñando varios prompts sucesivos,
    - o pidiendo al propio modelo que organice el trabajo por fases.
- Resulta útil cuando una tarea mezcla varios objetivos, por ejemplo:
    - leer,
    - analizar,
    - clasificar,
    - sintetizar,
    - redactar.
- Ejemplo de cadena:
    1. Extraer ideas principales.
    2. Agruparlas por temas.
    3. Detectar repeticiones.
    4. Redactar una versión final.
- Esta estrategia suele mejorar la calidad en tareas complejas y reduce la confusión.

## Verificación y revisión

- Una técnica muy útil es pedir una **segunda fase de comprobación**.
- Por ejemplo, después de generar una respuesta, se puede pedir que revise:
    - si ha cumplido el formato,
    - si faltan datos,
    - si hay contradicciones,
    - si existen repeticiones,
    - si se han respetado las restricciones.
- Esto no garantiza exactitud absoluta, pero sí puede mejorar la **coherencia** y el **cumplimiento de requisitos**.
- Ejemplo:
    - **“Tras redactar la respuesta, revisa si has cumplido los 6 criterios indicados y corrige lo que no se ajuste.”**

## Prompting multimodal

- En muchos sistemas actuales, los prompts pueden combinar **texto con imágenes, documentos, audio o vídeo**.
- Esto amplía mucho las posibilidades del prompt engineering.
- Algunos usos habituales son:
    - analizar una imagen,
    - resumir un PDF,
    - describir una gráfica,
    - comparar capturas de pantalla,
    - extraer información de formularios,
    - comentar una tabla o documento.
- En prompting multimodal conviene indicar con claridad:
    - qué elemento debe analizarse,
    - qué relación hay entre los materiales,
    - y qué tipo de salida se espera.
- Ejemplo:
    - **“Analiza la imagen adjunta y extrae únicamente los elementos visibles del diagrama, sin inferir información no representada.”**

## Prompts reutilizables y plantillas

- Cuando una tarea se repite con frecuencia, conviene convertir el prompt en una **plantilla**.
- Una plantilla permite mantener fijos:
    - el objetivo,
    - el formato,
    - los criterios,
    - el tono,
    - las restricciones,
    - y dejar variables solo los datos de entrada.
- Ejemplo sencillo:

```text
Actúa como [ROL].

Objetivo:
[OBJETIVO]

Contexto:
[CONTEXTO]

Entrada:
[ENTRADA]

Formato de salida:
[FORMATO]

Restricciones:
[RESTRICCIONES]
```

- Esto favorece respuestas más consistentes y facilita la mejora incremental.

## Evaluación e iteración

- El prompting rara vez se resuelve a la primera en tareas complejas.
- Lo normal es trabajar de forma iterativa:
    1. Se redacta un prompt inicial.
    2. Se observa la salida.
    3. Se detectan fallos.
    4. Se ajusta el prompt.
    5. Se vuelve a probar.
- En entornos profesionales, conviene evaluar los prompts con ejemplos de prueba y criterios definidos.
- Esta práctica ayuda a mantener la calidad cuando:
    - cambia el modelo,
    - cambia el contexto,
    - o cambia el tipo de entrada.
- Un prompt bueno no solo “suena bien”: **funciona bien de forma repetida**.

## Prompting para herramientas y agentes

- En sistemas que usan herramientas externas, funciones o agentes, el prompt también debe dejar claro:
    - cuándo usar una herramienta,
    - para qué,
    - con qué límites,
    - y cómo presentar el resultado.
- En estos casos importa mucho especificar:
    - el objetivo operativo,
    - el criterio de éxito,
    - la necesidad de verificar resultados,
    - y la persistencia de restricciones importantes.
- Este tipo de prompting suele ser más cercano a la **orquestación de tareas** que a una simple pregunta.


# Otras consideraciones


## Errores frecuentes

- Pedir algo demasiado genérico.
- No indicar el público destinatario.
- Mezclar varias tareas distintas en una sola instrucción desordenada.
- Dar contexto irrelevante y ocultar la información importante.
- No definir el formato de salida.
- No imponer restricciones cuando el resultado debe cumplir requisitos estrictos.
- Aportar ejemplos confusos o incorrectos.
- No revisar la salida antes de reutilizarla.
- Tratar el primer resultado como definitivo sin iterar.
- Pedir exactitud factual sin aportar fuentes ni mecanismos de verificación.

## Plantilla base de prompt

```text
Actúa como [ROL].

Tu objetivo es [TAREA ESPECÍFICA].

El público destinatario es [PÚBLICO].

Contexto relevante:
[CONTEXTO]

Material de entrada:
[ENTRADA]

Instrucciones específicas:
- [INSTRUCCIÓN 1]
- [INSTRUCCIÓN 2]
- [INSTRUCCIÓN 3]

Restricciones:
- [RESTRICCIÓN 1]
- [RESTRICCIÓN 2]
- [RESTRICCIÓN 3]

Formato de salida:
[FORMATO]

Criterios de calidad:
- [CRITERIO 1]
- [CRITERIO 2]

Si falta información suficiente, indícalo de forma explícita.
```


# Ejemplos prácticos



## Ejemplo 1: resumen ajustado a un público

```text
Actúa como docente universitario.

Resume el siguiente texto en 5 viñetas para alumnado de primer curso.
Usa lenguaje claro, mantén los conceptos clave y añade una breve conclusión final.
No superes las 180 palabras.

Texto:
[PEGAR TEXTO]
```

## Ejemplo 2: revisión de un documento

```text
Actúa como revisor editorial.

Analiza el documento adjunto y detecta:
1. errores de claridad,
2. repeticiones,
3. cambios bruscos de tema,
4. apartados mal titulados.

Devuelve la respuesta en Markdown con los apartados:
- Problemas detectados
- Propuestas de mejora
- Versión reescrita del fragmento más problemático
```

## Ejemplo 3: extracción estructurada

```text
Extrae la información del texto y devuélvela en JSON con esta estructura:
{
  "tema": "",
  "ideas_clave": [],
  "riesgos": [],
  "acciones_recomendadas": []
}

Si algún campo no puede completarse con seguridad, déjalo vacío.

Texto:
[PEGAR TEXTO]
```

## Ejemplo 4: trabajo multimodal

```text
Analiza la imagen y el documento adjuntos.

Objetivo:
- identificar coincidencias entre ambos,
- detectar contradicciones,
- resumir la información común.

Formato de salida:
1. Coincidencias
2. Contradicciones
3. Resumen final

No deduzcas datos que no estén respaldados por los materiales aportados.
```

# Conclusión

- El **prompt engineering** no consiste en memorizar fórmulas mágicas, sino en **aprender a dar instrucciones mejores**.
- Cuanto más clara esté la tarea, mejor definido el contexto y más explícito sea el resultado esperado, más probable será obtener una salida útil.
- En la práctica, un buen prompt combina:
    - **claridad**,
    - **contexto**,
    - **estructura**,
    - **criterios**,
    - **verificación**,
    - **iteración**.
- Por eso, más que preguntar “¿cuál es el prompt perfecto?”, suele ser mejor preguntarse:
    - **“¿qué necesita exactamente el modelo para resolver bien esta tarea?”**

# Referencias y recursos recomendados

- [OpenAI - Prompt engineering](https://developers.openai.com/api/docs/guides/prompt-engineering/)
- [OpenAI - Reasoning best practices](https://developers.openai.com/api/docs/guides/reasoning-best-practices/)
- [OpenAI - Structured outputs](https://developers.openai.com/api/docs/guides/structured-outputs/)
- [OpenAI - Prompt engineering best practices for ChatGPT](https://help.openai.com/en/articles/10032626-prompt-engineering-best-practices-for-chatgpt)
- [Google Cloud - Introduction to prompting](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/introduction-prompt-design)
- [Google Cloud - Design multimodal prompts](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/multimodal/design-multimodal-prompts)
- [Anthropic - Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)
