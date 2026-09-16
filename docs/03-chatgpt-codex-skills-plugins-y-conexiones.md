# ChatGPT, Codex, skills, plugins y conexiones

ChatGPT y Codex pueden colaborar en el mismo proyecto, pero no hacen exactamente el mismo trabajo. Elegir bien la superficie y limitar sus herramientas reduce errores, repeticiones y exposición de información. Las funciones disponibles dependen de la cuenta, el dispositivo y la configuración del espacio de trabajo; confirma siempre qué acceso aparece activo antes de iniciar una tarea.

## 1. Elegir el punto de partida

| Si necesitas… | Empieza con… | Entregable esperado |
| --- | --- | --- |
| Aprender un concepto, generar ideas o convertir una necesidad en requisitos | **ChatGPT** | Explicación, preguntas abiertas, borrador o especificación |
| Investigar fuentes, preparar un entregable o coordinar trabajo estructurado | **Work** | Investigación trazable, plan o borrador para revisar |
| Leer, modificar y probar código en un repositorio | **Codex** | Cambio acotado, pruebas y resumen de archivos modificados |
| Repetir siempre el mismo proceso | Una **skill** | Flujo reutilizable con entradas y salida definidas |
| Instalar o compartir un conjunto de skills y herramientas | Un **plugin** | Paquete instalable y documentación de permisos |
| Consultar o actuar en otro servicio | Una **conexión** o herramienta autorizada | Resultado verificable, con el mínimo acceso necesario |

Una misma iniciativa puede recorrer varias superficies. Por ejemplo: ChatGPT ayuda a definir las historias de usuario; Work reúne fuentes para una comparación; Codex implementa el cambio en el repositorio. No copies sin revisar una respuesta de una superficie a otra: lleva el objetivo, las decisiones confirmadas y las fuentes relevantes.

## 2. ChatGPT y Work: pensar antes de actuar

Usa ChatGPT para tareas conversacionales y de exploración: explicar una tecnología, cuestionar supuestos, proponer una estructura de documentación o convertir notas en una especificación. Una buena petición dice qué resultado esperas, qué información es confiable y qué debe quedar pendiente.

Work resulta útil cuando el trabajo requiere varios pasos, archivos, fuentes o un seguimiento más estructurado. Define desde el inicio:

- El resultado: por ejemplo, «comparación de tres opciones con fuentes, costo aproximado y recomendación condicionada».
- Las fuentes permitidas: sitios oficiales, documentos internos concretos o datos que tú adjuntaste.
- Lo que no debe hacer: enviar mensajes, crear registros, cambiar archivos o tomar decisiones externas.
- El punto de aprobación: antes de publicar, gastar, contactar a terceros o usar información sensible.

Pide que separe hechos, inferencias y preguntas abiertas. Para una decisión importante, conserva enlaces y fecha de consulta; las políticas, precios y capacidades cambian.

## 3. Codex: trabajar con un repositorio de forma revisable

Codex es apropiado cuando el resultado vive en código, configuración, pruebas o documentación versionada. Dale un encargo que se pueda revisar como cambio de repositorio.

```text
Objetivo: añadir un estado vacío a la lista de tareas.
Alcance: modifica solo componentes de la pantalla de tareas y sus pruebas.
No hagas: agregar dependencias, cambiar configuración de despliegue ni publicar.
Comportamiento: cuando no haya tareas, explica cómo crear la primera; debe ser legible con lector de pantalla.
Validación: ejecuta las pruebas existentes relacionadas; indica con precisión qué no se pudo probar.
Entrega: resume el cambio, los archivos tocados, las pruebas y cualquier supuesto.
```

Antes de solicitar una tarea grande, pide primero un plan. Antes de aprobar el resultado, inspecciona el cambio y ejecuta o reproduce las pruebas. Un agente no debe usar como pretexto una instrucción vaga para alterar archivos ajenos, cambiar dependencias o desplegar una aplicación.

En cada tarea, declara el nivel de permiso adecuado:

| Nivel | Ejemplo permitido | Ejemplo que requiere otro nivel |
| --- | --- | --- |
| Solo lectura | Examinar código, logs o documentación | Editar un archivo |
| Edición local | Corregir archivos dentro del repositorio | Subir cambios a un servidor |
| Propuesta externa | Preparar texto de una publicación o de un mensaje | Enviarlo |
| Acción externa aprobada | Crear una versión de prueba tras confirmación | Publicar en producción sin aprobación explícita |

Cuando trabajes con un repositorio compartido, acordar ramas, revisiones y pruebas evita que una tarea automática interfiera con el trabajo de otra persona.

## 4. Qué es una skill

Una **skill** es un flujo de trabajo reutilizable: reúne instrucciones, recursos de apoyo y, cuando hacen falta, scripts o herramientas para una tarea específica. Por ejemplo, una skill puede crear una minuta con un formato fijo, revisar documentación con una lista de verificación o preparar una compilación de prueba.

Una skill vale la pena si el proceso se repite y la calidad depende de seguir pasos concretos. No la crees para una única pregunta ocasional; empieza con un prompt normal y convierte el proceso en skill cuando ya conoces sus entradas, decisiones y formato de salida.

Una skill bien delimitada deja claro:

```text
Nombre: revision-de-documentacion
Se usa cuando: se revisa un capítulo Markdown antes de publicarlo.
Entradas: archivo objetivo y enlaces oficiales indicados por la persona solicitante.
Proceso: revisar estructura, enlaces, lenguaje claro y exposición de datos privados.
Salida: lista priorizada de hallazgos y propuesta de cambio; no publicar ni modificar enlaces externos.
No se usa cuando: se necesita una auditoría legal, médica o de seguridad especializada.
```

De acuerdo con la documentación oficial, las skills pueden activarse porque la tarea coincide con su descripción o porque se invocan explícitamente; en ChatGPT se seleccionan con `@` y en Codex con `$`. La descripción debe ser concreta para que no se active por error. [OpenAI Docs: Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins?translationFallback=es-419)

Para una skill local de Codex, el formato gira alrededor de un archivo `SKILL.md`. Puedes usar el creador de skills para crearla o escribirla de forma manual. Dentro de un repositorio, una skill solo debe contener reglas que realmente correspondan al proyecto; no guardes secretos ni instrucciones personales en ella. [OpenAI Docs: Build skills](https://learn.chatgpt.com/docs/build-skills?translationFallback=es-419)

## 5. Cuándo usar un plugin

Un **plugin** es un paquete instalable que puede incluir una o más skills y, opcionalmente, servidores MCP (Model Context Protocol) para ofrecer herramientas o contexto de otros servicios. Úsalo cuando quieras distribuir un flujo comprobado, instalar una capacidad ya preparada o agrupar instrucciones con una conexión necesaria. [OpenAI Docs: Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins?translationFallback=es-419)

Antes de instalar uno, responde estas preguntas:

1. ¿Qué problema concreto resuelve que no pueda resolver una skill local o un prompt?
2. ¿Qué permisos y servicios externos solicita?
3. ¿Qué datos verá, podrá crear, modificar o enviar?
4. ¿Quién mantiene el plugin y cómo se actualizará?
5. ¿Qué ocurre si falla, entrega datos incorrectos o deja de estar disponible?

Instala el mínimo necesario y prueba primero una tarea sin consecuencias. Un plugin que lee GitHub no obtiene automáticamente permiso para publicar versiones; verifica las autorizaciones reales de cada herramienta y del servicio conectado.

## 6. Conexiones: alcance mínimo y evidencia

Una conexión permite que una herramienta consulte o, si se autoriza, actúe sobre otro servicio: repositorios, documentos, calendario, correo o gestión de tareas. No trates ese acceso como una extensión inocua del chat. Es una autorización que debe tener propietario, propósito y fecha de revisión.

| Riesgo | Medida práctica |
| --- | --- |
| Acceso excesivo | Concede solo los permisos y repositorios imprescindibles. |
| Información privada en un resultado | Adjunta o consulta únicamente los documentos pertinentes; revisa antes de compartir. |
| Acción equivocada | Pide un borrador, una vista previa o confirmación humana antes de enviar, borrar o publicar. |
| Permiso olvidado | Revisa y revoca conexiones que ya no son necesarias. |
| Falta de trazabilidad | Registra qué se consultó, qué se cambió y con qué aprobación. |

Una automatización conectada debe ser aún más conservadora. Puede preparar un reporte, detectar una discrepancia o crear un borrador; enviar un correo, modificar una base de datos, activar una campaña o hacer un pago necesita reglas explícitas y una ruta para detenerla.

## 7. Un flujo seguro para ampliar capacidades

Sigue esta secuencia cada vez que incorpores una skill, plugin o conexión:

1. Describe la tarea repetible y el resultado esperado.
2. Empieza sin acceso externo o con modo de solo lectura.
3. Prueba con información no sensible y un caso pequeño.
4. Revisa resultados, permisos solicitados y registros disponibles.
5. Ajusta instrucciones, límites y punto de aprobación.
6. Solo entonces autoriza acciones externas concretas.
7. Revisa periódicamente si la capacidad y el acceso siguen siendo necesarios.

El objetivo no es evitar la automatización, sino hacerla confiable y reversible. La herramienta debe poder explicar qué hizo y la persona responsable debe poder detenerla.

## 8. Ejercicio: elegir la capacidad correcta

Toma una tarea de tu proyecto y responde:

1. ¿Necesitas una conversación, investigación, edición de código o una integración externa?
2. ¿Cuál es el resultado que revisarás antes de aceptar?
3. ¿Cuál es el permiso mínimo para obtener ese resultado?
4. ¿Qué acción debe detenerse para pedir aprobación?
5. ¿Se repetirá tanto que merece una skill?

Escribe la respuesta como un encargo corto. Si la tarea se repetirá, prueba el encargo tres veces con ejemplos distintos antes de convertirlo en una skill o instalar un plugin.

## Siguiente capítulo

El siguiente capítulo tratará Git y GitHub: cómo conservar historial, colaborar con ramas y pull requests, y recuperar cambios sin perder trabajo.
