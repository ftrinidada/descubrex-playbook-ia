# Introducción a IA, modelos, chat y agentes

Este capítulo da un vocabulario común antes de usar IA para un sitio web, una app, un juego, una automatización o cualquier otro proyecto. El objetivo no es memorizar nombres de productos, sino saber qué pedir, qué validar y cuándo conservar el control humano.

## 1. El mapa mental básico

**Inteligencia artificial (IA)** es un término amplio para sistemas que realizan tareas que normalmente asociamos con razonamiento, percepción, predicción o generación. La **IA generativa** crea contenido nuevo: texto, código, imágenes, audio o una combinación de ellos.

Un **modelo** es el sistema entrenado que recibe una entrada y genera una salida. Un modelo de lenguaje grande (LLM) trabaja con lenguaje y código; no es una base de datos perfecta ni una fuente automática de verdad. Su respuesta puede ser útil, pero puede equivocarse, inventar un detalle o entender mal una instrucción incompleta.

Piensa en la IA como un colaborador muy rápido que necesita buen contexto, una tarea concreta y revisión. No como una autoridad final.

## 2. Modelos, tokens y contexto

Un modelo recibe una instrucción, el texto o archivos disponibles y, cuando tiene herramientas autorizadas, resultados de esas herramientas. Después genera una respuesta. El resultado depende de cuatro cosas principales:

- La capacidad del modelo: calidad de razonamiento, programación, análisis visual o uso de herramientas.
- El contexto disponible: instrucciones, conversación, archivos y datos relevantes.
- La tarea: claridad, dificultad y criterios de éxito.
- Los límites configurados: tiempo, costo, longitud de respuesta, permisos y herramientas.

Los modelos procesan **tokens**, unidades pequeñas de texto. Existe una ventana de contexto limitada: en una conversación muy larga, no conviene asumir que todos los detalles antiguos siguen presentes o son igual de importantes. Repite el objetivo, los requisitos y las decisiones críticas cuando retomes una tarea extensa.

Al elegir modelo no busques solamente “el más potente”. Equilibra calidad, rapidez, costo, tamaño de contexto, modalidad (texto, imagen o audio) y acceso a herramientas. Una corrección pequeña puede requerir un modelo rápido; investigar un problema complejo o revisar una arquitectura puede justificar uno con más capacidad.

## 3. Chat, proyectos y contexto persistente

Un **chat** es una conversación: sirve para preguntas, ideas, explicaciones, borradores y tareas pequeñas. El contexto de un chat incluye lo que escribes, los archivos adjuntos y las instrucciones que la plataforma conserve para esa conversación.

Un **proyecto** o espacio de trabajo agrupa conversaciones, archivos e instrucciones sobre un tema. Ayuda a mantener orden, pero no sustituye una especificación. Mantén en un archivo corto las decisiones que no pueden cambiar: objetivo, usuarios, tecnología, restricciones, fuentes de verdad y cómo probar el resultado.

El contexto no es lo mismo que memoria infalible. Una IA no debe adivinar requisitos, acceder por sí sola a sistemas privados ni conocer cambios recientes si no tiene una fuente actual autorizada. Para asuntos actuales, sensibles o importantes, aporta la fuente y pide que la cite o la revise.

## 4. Prompts que dan resultados revisables

Un **prompt** es la instrucción que das a la IA. Un prompt útil no tiene que ser largo; tiene que eliminar ambigüedades relevantes. Esta estructura funciona para casi cualquier tarea:

1. **Objetivo:** qué resultado quieres y para quién.
2. **Contexto:** información, archivos, restricciones y fuentes disponibles.
3. **Alcance:** qué debe incluir y qué queda fuera.
4. **Formato:** código, tabla, plan, texto, lista de archivos o pasos concretos.
5. **Validación:** cómo comprobar que el resultado está bien y qué debe preguntar antes de actuar.

Ejemplo para un sitio web:

```text
Quiero una página de inicio para una cafetería local. Usa HTML, CSS y JavaScript sin dependencias.
El público son visitantes que buscan horario, ubicación y menú. Incluye versión móvil y accesibilidad básica.
No inventes precios ni testimonios. Entrega los archivos completos y una lista de pruebas manuales.
Antes de agregar servicios externos o publicar algo, explícame qué acceso se requiere y espera mi aprobación.
```

Después de la primera respuesta, mejora de forma iterativa: señala el problema observado, aporta el archivo o dato correcto, fija una decisión y pide una verificación. Pedir “hazlo mejor” ayuda menos que “el formulario no muestra errores; añade mensajes accesibles y prueba los tres estados”.

## 5. Límites que hay que entender

- **Errores y alucinaciones:** la IA puede dar una respuesta convincente y equivocada. Verifica datos, enlaces, cálculos, código y afirmaciones importantes.
- **Información incompleta:** si faltan requisitos, la IA puede asumir. Pídele que enumere supuestos o que haga una pregunta antes de decidir.
- **Actualidad:** sin una fuente reciente, no asumas precios, reglas, APIs, horarios o noticias actualizados.
- **Privacidad:** no pegues contraseñas, tokens, llaves API, certificados ni datos personales innecesarios. Usa variables de ejemplo como `API_KEY` en la documentación.
- **Permisos:** que una IA pueda proponer un comando, enviar un mensaje o modificar un archivo no significa que deba hacerlo. Define quién aprueba acciones externas.
- **Responsabilidad:** revisa antes de desplegar, cobrar, publicar, borrar, enviar a clientes o tomar una decisión de impacto legal, médico, financiero o de seguridad.

## 6. Chat, Work y Codex: cuál usar

Las funciones disponibles pueden cambiar según el plan y la plataforma, pero esta distinción es una buena regla práctica:

| Opción | Úsala para | Aporta | Revisión humana necesaria |
| --- | --- | --- | --- |
| **Chat** | Preguntas, ideas, aprendizaje y borradores | Conversación rápida y explicación | Comprobar datos y aplicar el resultado |
| **Work** | Investigar, analizar fuentes, preparar entregables o dar seguimiento a trabajo estructurado | Tarea enfocada con fuentes y, cuando se configura, conexiones o seguimiento | Definir alcance y aprobar acciones externas |
| **Codex** | Construir o cambiar software en un repositorio | Contexto de código, edición, pruebas y herramientas de desarrollo | Revisar cambios, pruebas, secretos y publicación |

No es obligatorio escoger una sola opción. Por ejemplo, puedes usar Chat para convertir una idea en requisitos, Work para investigar alternativas y Codex para implementar y probar el proyecto.

## 7. Qué es un agente

Un **agente** combina un objetivo, contexto, reglas y herramientas para avanzar por varios pasos. No tiene que ser un modelo distinto y no es autónomo por definición. La diferencia importante es que puede planear, consultar información, editar archivos o ejecutar herramientas dentro de los permisos que tenga.

Trátalo como a un colaborador con acceso limitado. Antes de usarlo, define este contrato mínimo:

- Resultado esperado y forma de medirlo.
- Alcance y elementos explícitamente fuera de alcance.
- Fuentes permitidas y qué información es privada.
- Acciones autorizadas: solo lectura, editar archivos, crear una rama, enviar un borrador, publicar, etc.
- Punto de alto: cuándo debe pedir aprobación.
- Evidencia de cierre: pruebas, enlaces, lista de archivos o reporte de cambios.

Ejemplo de instrucción segura para un agente:

```text
Revisa este repositorio para detectar llaves expuestas y configuraciones inseguras.
Trabaja solo en modo lectura. No modifiques archivos, no subas resultados y no muestres valores secretos completos.
Entrega hallazgos con archivo, línea, impacto y una recomendación. Si necesitas usar una fuente externa, indícalo antes.
```

En Work, una tarea enfocada puede revisar fuentes conectadas, preparar un entregable o monitorear cambios; debe tener condiciones claras y esperar aprobación antes de acciones externas. En Codex, un agente puede trabajar sobre un repositorio, pero publicar, desplegar o alterar datos sigue requiriendo el permiso que tú definas.

## 8. Ejercicio: llevar una idea a una tarea controlada

Elige un proyecto sencillo: una página para un negocio, un minijuego o una automatización de reportes.

1. Escribe en cinco líneas el objetivo, usuarios, tecnología, límites y cómo sabrás que funciona.
2. Pide en Chat una propuesta de alcance y una lista de preguntas abiertas.
3. Convierte las respuestas en una especificación corta y guárdala en el repositorio.
4. Pide a Codex una primera implementación o un plan de cambios, indicando los archivos permitidos y las pruebas esperadas.
5. Revisa el resultado, prueba el proyecto y documenta qué corrigió la IA y qué decisión tomaste tú.

El hábito clave es conservar las decisiones y la evidencia. Así, la IA acelera el trabajo sin volverlo opaco.

## Fuentes para seguir aprendiendo

- [Inicio rápido de ChatGPT](https://learn.chatgpt.com/docs/quickstart?translationFallback=es-419)
- [Configura un compañero de equipo para el proyecto en ChatGPT Work](https://learn.chatgpt.com/es-419/use-cases/project-teammate)
- [Habilidades y complementos de ChatGPT](https://learn.chatgpt.com/es-419/docs/skills-and-plugins)
- [Generative AI for Beginners, en español](https://github.com/microsoft/generative-ai-for-beginners/blob/main/translations/es/README.md)
