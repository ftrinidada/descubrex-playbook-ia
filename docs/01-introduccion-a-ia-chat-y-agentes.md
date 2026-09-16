# Introducción a IA, modelos, chat y agentes

## 1. ¿Qué es la IA?

La **inteligencia artificial (IA)** es tecnología que ayuda a una computadora a reconocer patrones y realizar tareas que normalmente hacemos las personas. Por ejemplo, puede resumir un texto largo, responder preguntas, traducir, recomendar una canción, identificar objetos en una imagen o ayudarte a escribir código.

No es magia ni una mente que lo sabe todo. La IA aprende de muchos ejemplos y usa esos patrones para producir una respuesta que parece adecuada. Cuando le escribes una pregunta, no «busca una verdad» como lo haría una enciclopedia: interpreta tus palabras, calcula qué respuesta podría ser útil y la construye paso a paso.

Imagina que trabajas con una persona muy rápida que ha leído mucho, puede redactar en segundos y conoce muchos ejemplos, pero que a veces confunde detalles o responde con seguridad aunque no tenga toda la información. Esa es una buena forma de entender la IA: puede ser una gran colaboradora, pero necesita instrucciones claras y una revisión humana.

La **IA generativa** es la parte de la IA que crea contenido nuevo a partir de una instrucción. En lugar de limitarse a clasificar algo que ya existe —por ejemplo, decidir si una foto muestra un perro o un gato— puede ayudarte a producir una primera versión de algo: un texto, código, una imagen, audio, una presentación o una combinación de estos elementos.

Funciona como una persona que te ayuda a crear un borrador muy rápido. Si le pides «Escribe tres ideas para un juego de aventuras dirigido a niñas y niños», no recupera un juego guardado en una caja: combina patrones que aprendió para proponer posibilidades nuevas. Si le das más detalles, como la edad de las personas jugadoras, el tema y las reglas que debe respetar, el resultado suele acercarse más a lo que imaginabas.

Puedes usar la IA generativa para muchas cosas cotidianas: proponer el texto de una página para una cafetería, resumir tus apuntes, convertir una lista de ideas en un plan, explicar un error de programación con palabras sencillas, crear una imagen de referencia o generar opciones para el nombre de un proyecto. También puede ayudarte a revisar y mejorar un trabajo que ya empezaste.

La palabra importante es **borrador**. El resultado puede ser útil como punto de partida, pero no es automáticamente correcto, original, completo ni apropiado para publicar. Léelo, comprueba los datos, ajusta el tono y asegúrate de que representa tu intención. Tú aportas la idea, el criterio y la decisión final; la IA generativa te ayuda a avanzar más rápido.

## 2. Conceptos esenciales para empezar

Al comenzar a usar IA aparecen muchas palabras nuevas. No necesitas aprenderlas todas de memoria. Esta es una lista de los conceptos que verás con más frecuencia y que te ayudarán a entender qué estás haciendo cuando hablas con una IA.

### Modelo

Un **modelo** es el sistema de IA que recibe lo que escribes y genera una respuesta. Piensa en él como el motor que está detrás del chat. Algunos modelos son mejores para conversar o escribir; otros entienden imágenes, ayudan con programación o resuelven problemas más complejos. Por eso una misma pregunta puede recibir respuestas distintas según el modelo elegido.

No siempre necesitas escoger un modelo. Cuando sí puedas hacerlo, elige según la tarea: uno rápido suele bastar para una pregunta breve o una lluvia de ideas; una tarea difícil, como analizar muchos archivos o revisar una aplicación, puede necesitar uno con mayor capacidad. Lo importante es revisar el resultado, sin importar el modelo usado.

**Ejemplo:** en Codex puedes encontrar modelos con nombres como **GPT-6 Astra**, **GPT-5.6 Sol**, **GPT-5.6 Terra** y **GPT-5.6 Luna**. Son modelos de la misma familia, pero están pensados para necesidades distintas: Sol se orienta a problemas complejos, Terra al trabajo cotidiano de producción y Luna a tareas rápidas o de gran volumen. Astra es otra opción disponible para algunas tareas y planes. La disponibilidad cambia según tu plan y la aplicación que uses.

Otras compañías también tienen sus propias familias de modelos. Por ejemplo, **Claude** es el nombre de una familia de modelos de Anthropic. Los nombres pueden sonar técnicos, pero la idea es sencilla: elige uno más rápido para una petición breve y uno con más capacidad para un problema complejo. No necesitas conocerlos todos para empezar.

### Prompt o instrucción

Un **prompt** es lo que le dices o escribes a la IA para pedirle algo. Puede ser una pregunta sencilla, como «Explícame qué es una página web», o una instrucción detallada, como «Escribe el texto de inicio para una cafetería; usa un tono cercano, no inventes precios y entrégalo en tres párrafos».

El prompt no es una fórmula mágica. Es una explicación clara de lo que necesitas. Cuanto mejor describas el objetivo, el público, los datos disponibles y el resultado esperado, más fácil será que la IA te ayude. El punto 4 muestra cómo escribirlos paso a paso.

**Ejemplo:** «Dame ideas para un negocio» es un prompt muy abierto. «Dame cinco ideas de nombres para una cafetería mexicana, con un tono cálido y familiar» da a la IA una dirección mucho más clara.

### Respuesta o resultado

La **respuesta** es lo que la IA te devuelve: texto, código, una imagen, una tabla, un plan o una explicación. Es un borrador o una propuesta, no una verdad automática. Léela, comprueba lo importante y pide cambios si algo no cumple tu objetivo.

**Ejemplo:** si pides un menú para tu cafetería y la respuesta incluye un precio que no existe, no lo publiques. Corrige ese dato y pide una nueva versión con los precios confirmados.

### Contexto

El **contexto** es la información que la IA puede usar para responder: tu prompt, los mensajes anteriores, los archivos que adjuntaste, las instrucciones del proyecto y, si le diste permiso, los resultados de herramientas o fuentes externas. Es como el material que entregas a alguien antes de pedirle una tarea.

Si le das el horario correcto de un negocio y explicas que no debe inventar datos, podrá ayudarte mejor. Si le faltan datos, puede hacer suposiciones. Por eso, al retomar un trabajo largo, repite lo esencial: qué quieres lograr, qué ya está decidido y qué no se debe cambiar.

**Ejemplo:** este mensaje da a la IA el contexto necesario antes de pedirle una mejora:

```text
Estamos creando una página para una cafetería.
El menú y el horario ya están confirmados en este archivo.
No agregues pagos ni pedidos en línea todavía.
Necesito que revises que se vea bien en un teléfono.
```

### Tokens

Los **tokens** son las piezas pequeñas en las que el modelo divide el texto para poder procesarlo. No son exactamente palabras: una palabra puede ocupar uno o varios tokens. Tu mensaje, los archivos que adjuntas, el historial de la conversación, los resultados de herramientas y la respuesta de la IA consumen tokens.

Hay dos límites distintos que conviene conocer:

1. **Límite de contexto:** es la cantidad de información que la IA puede tener presente en una conversación al mismo tiempo. Si la conversación es muy larga o adjuntas muchos archivos, algunos detalles antiguos pueden perder importancia o dejar de estar disponibles. Cuando ocurra, resume las decisiones principales o vuelve a adjuntar el archivo importante.
2. **Límite de uso de tu plan:** es la cantidad de trabajo que tu cuenta puede usar durante un periodo. Las tareas grandes, los archivos extensos, las respuestas largas, el uso de herramientas y los modelos más capaces suelen consumir más de ese límite que una pregunta breve.

**Ejemplo:** preguntar «Dame tres nombres para una cafetería» usa poco. En cambio, adjuntar un documento de 200 páginas, pedir que la IA lo analice, consulte fuentes y cree una presentación puede usar mucho más. Si alcanzas el límite de tu plan, la aplicación te indicará cuándo podrás continuar. Según tu plan y las opciones disponibles, puedes esperar a que se renueve el límite, elegir un modelo más pequeño, reducir el tamaño de la tarea o usar créditos adicionales. No es necesario cambiar de plan de inmediato.

Puedes revisar el uso disponible en el panel de tu cuenta. Los límites y las opciones cambian según el plan, el modelo y el tipo de tarea. [OpenAI Docs: uso, tokens y límites](https://learn.chatgpt.com/docs/pricing)

### Chat o conversación

Un **chat** es el espacio donde conversas con la IA. Cada mensaje que envías y cada respuesta que recibes construyen una conversación. Es útil para aprender, hacer preguntas, mejorar un texto o explorar una idea. Un chat no es una carpeta de archivos ni una memoria perfecta: guarda fuera del chat las decisiones que no quieras perder.

**Ejemplo:** abre un chat para preguntar «¿Cómo funciona una página web?» y otro diferente para crear el contenido de tu negocio. Separarlos hará más fácil encontrar cada conversación después.

### Proyecto o espacio de trabajo

Un **proyecto** o espacio de trabajo agrupa conversaciones, archivos e instrucciones sobre un mismo tema. Por ejemplo, puedes crear uno para una página web, un juego o una aplicación móvil. Ayuda a mantener el orden y evita repetir el mismo contexto en cada conversación, pero sigue siendo buena idea tener una nota corta con las decisiones importantes.

**Ejemplo:** en un proyecto llamado «Juego de laberinto» puedes reunir el dibujo de los niveles, las reglas del juego, las conversaciones sobre sonidos y la lista de tareas pendientes.

### Archivos y datos de entrada

Los **archivos** o **datos de entrada** son materiales que entregas a la IA para que trabaje mejor: una imagen, una hoja de cálculo, un documento, un fragmento de código o una lista de requisitos. Antes de adjuntarlos, comprueba que no contengan contraseñas, datos personales innecesarios o información que no tengas permiso de compartir.

**Ejemplo:** si quieres que la IA mejore un texto, adjunta el documento o pega solo el párrafo relevante; no necesitas compartir toda tu carpeta personal.

### Multimodal

**Multimodal** significa que la IA puede trabajar con más de un tipo de información. Además de texto, puede entender o generar imágenes, audio, video, documentos o código, según las capacidades disponibles. Por ejemplo, podrías adjuntar una foto de un boceto y pedir una descripción para una página web; aun así, debes revisar que la interpretación sea correcta.

**Ejemplo:** toma una foto de un menú escrito a mano y pide una versión ordenada en texto. Después compara el resultado con la foto para confirmar que no cambió nombres, precios ni ingredientes.

### Herramientas y conexiones

Normalmente, una IA puede leer tu instrucción y escribir una respuesta. Una **herramienta** le permite hacer algo adicional dentro de un entorno controlado: buscar información en la web, leer un archivo que autorizaste, ejecutar una prueba, generar una imagen, calcular datos o revisar código. La herramienta tiene una función concreta; la IA decide cuándo usarla solo si está disponible y permitida.

Una **conexión** es el acceso controlado a otro servicio o fuente de información. Por ejemplo, una conexión puede permitir que la IA consulte un repositorio de GitHub, una carpeta de documentos, un calendario o una lista de tareas. La conexión no debería dar acceso a todo por defecto: debe respetar la cuenta con la que iniciaste sesión y los permisos que concediste en ese servicio.

La diferencia es sencilla: una herramienta es la acción que la IA puede realizar; una conexión es la puerta que le permite usar información o acciones de otro sistema. A menudo trabajan juntas. Por ejemplo, la conexión da acceso a un repositorio y la herramienta permite buscar archivos dentro de él o ejecutar sus pruebas.

Estas capacidades pueden ahorrar mucho tiempo, pero también aumentan la responsabilidad. Antes de activarlas, pregúntate: «¿Qué datos podrá ver?», «¿Podrá cambiar algo?», «¿Necesita este acceso para completar la tarea?» y «¿Qué debe pasar antes de enviar, publicar o borrar algo?». Empieza con acceso de solo lectura siempre que sea posible.

**Ejemplo 1: investigar sin cambiar nada.** Pides: «Busca en la documentación oficial cómo instalar esta biblioteca y resume los pasos. No modifiques archivos». La IA puede usar una herramienta de búsqueda para encontrar la fuente y entregarte un resumen. Tú decides si los pasos se aplican al proyecto.

**Ejemplo 2: revisar un repositorio.** Con una conexión a GitHub, puedes pedir: «Revisa los archivos de este repositorio y dime qué enlaces están rotos. Trabaja en modo lectura y no abras un pull request». La IA puede leer los archivos autorizados y devolver una lista de hallazgos, pero no debe cambiar ni publicar nada.

**Ejemplo 3: preparar, pero no enviar.** Si una conexión tiene acceso a un calendario o correo, puedes pedir: «Prepara un borrador de invitación para esta reunión usando los datos del calendario; no envíes nada». El resultado debe quedarse como borrador para que tú lo revises antes de compartirlo.

Una regla fácil de recordar es esta: permite a la IA **leer** para investigar, **preparar** para ayudarte y **actuar** solo cuando hayas revisado qué hará y estés listo para aprobarlo. Los permisos y las conexiones se explican con más detalle en el capítulo sobre ChatGPT, Codex, skills, plugins y conexiones.

### Permisos y aprobación

Los **permisos** indican qué puede hacer la IA: quizá solo pueda leer archivos, quizá pueda editar archivos locales o quizá pueda preparar un borrador de correo. La **aprobación** es tu confirmación antes de una acción importante, como enviar, publicar, borrar, cobrar o modificar datos externos. Un permiso limitado protege tu trabajo mientras aprendes.

**Ejemplo:** puedes permitir que la IA lea tu código y sugiera una corrección, pero pedirle que se detenga antes de borrar archivos, enviar un correo o subir cambios a Internet.

### Iteración

Una **iteración** es una vuelta de mejora. Pides un primer resultado, lo revisas, señalas lo que falta y pides una nueva versión. Trabajar así es normal: la primera respuesta rara vez es la versión final. Una buena iteración tiene un comentario concreto, por ejemplo: «La explicación es correcta, pero usa ejemplos más cotidianos y elimina palabras técnicas».

**Ejemplo:** primero pides el texto para la portada; luego dices «Hazlo más corto y menciona el horario», y finalmente corriges el horario con el dato real. Cada mejora es una iteración.

### Alucinación o información inventada

Una **alucinación** es una respuesta que parece creíble, pero contiene información incorrecta o inventada. Puede ser una fecha, una fuente, un precio, una explicación o código que parece funcionar sin hacerlo. No es una mentira intencional: es una limitación de la tecnología. Verifica los datos importantes antes de tomar una decisión.

**Ejemplo:** la IA puede recomendar un restaurante que ya cerró o citar un artículo que no existe. Antes de confiar en esa información, abre la fuente o comprueba el dato en un sitio confiable.

### Agente

Un **agente** es una IA que, además de responder, puede avanzar por varios pasos con un objetivo, instrucciones y herramientas autorizadas. Por ejemplo, puede revisar archivos, preparar un plan y ejecutar una prueba. Como puede tener más capacidad de acción que un chat normal, necesita límites claros y revisión humana. Lo veremos con detalle en el punto 7.

**Ejemplo:** un agente puede revisar todos los archivos de una página web y entregarte una lista de enlaces rotos. Debe limitarse a reportarlos hasta que tú autorices cualquier corrección.

La calidad de una respuesta depende principalmente del modelo, del contexto disponible, de qué tan clara sea tu instrucción y de los límites configurados, como tiempo, permisos y herramientas. Conocer estos términos te permite pedir mejor ayuda y mantener el control.

## 3. Chat, proyectos y contexto persistente

Para entender esta parte, imagina que trabajas con una persona que te ayuda durante varias conversaciones. Necesitas un lugar para hablar de una pregunta concreta y otro lugar para guardar todo lo que pertenece a un proyecto. ChatGPT y herramientas similares suelen organizarse de una forma parecida.

Un **chat** es una conversación individual con la IA. Es como abrir un cuaderno para hablar de un solo tema. Puedes usarlo para hacer preguntas, pedir una explicación, ordenar ideas, mejorar un texto o resolver una tarea pequeña. Dentro de ese chat, la IA puede tener en cuenta los mensajes anteriores y los archivos que agregaste allí.

**Ejemplo:** abre un chat llamado mentalmente «Ideas para mi cafetería» y pide nombres, colores y textos para una página web. Si después quieres aprender a programar un juego, abre otro chat. Separar los temas evita mezclar instrucciones y hace más fácil volver a encontrar lo que hiciste.

Un **proyecto** o espacio de trabajo es como una carpeta grande para un objetivo que llevará varios días o semanas. Puede reunir varios chats, archivos, imágenes, instrucciones y notas que pertenecen al mismo trabajo. No es necesario usar un proyecto para una pregunta rápida, pero ayuda mucho cuando estás creando algo más grande.

**Ejemplo:** crea un proyecto llamado «Página de la cafetería». Dentro puedes guardar el horario confirmado, el menú, las fotos autorizadas y varios chats: uno para escribir el texto, otro para diseñar la página y otro para revisar los enlaces. Así, cada chat puede usar la información del proyecto sin que tengas que copiarla una y otra vez.

El **contexto persistente** es la información que se conserva para seguir trabajando después: los mensajes de un chat, los archivos de un proyecto o las instrucciones que hayas configurado. La palabra «persistente» no significa «recuerdo perfecto para siempre». Significa que esa información puede seguir disponible mientras trabajas, según la herramienta, el proyecto y la configuración que uses.

Por eso, si hay una decisión importante, no confíes solo en que apareció en un mensaje antiguo. Guárdala también en una nota corta dentro del proyecto. Esa nota funciona como una brújula para ti y para la IA:

```text
Proyecto: Página de la cafetería La Esquina.
Objetivo: mostrar horario, ubicación y menú confirmado.
No incluye: pedidos ni pagos en línea.
Datos confiables: el archivo horario-y-menu.md.
Prueba: comprobar la página en teléfono y computadora.
```

Un proyecto ordenado ayuda, pero no reemplaza tu revisión. La IA no debe adivinar requisitos, entrar por sí sola a sistemas privados ni conocer cambios recientes si no tiene una fuente actual y autorizada. Para un precio, una regla, una noticia o un dato importante, comparte la fuente correcta y pídele que la revise o cite.

La idea principal es sencilla: usa un **chat** para conversar sobre una tarea; usa un **proyecto** para reunir todo lo necesario para un objetivo mayor; y conserva las decisiones importantes en una nota clara para no depender de la memoria de la IA.

## 4. Prompts que dan resultados revisables

Un **prompt** es lo que le pides a la IA. Puede ser una sola pregunta o una instrucción detallada. No necesitas usar palabras especiales: habla con claridad, como si le explicaras la tarea a una persona que acaba de incorporarse al proyecto.

Un prompt útil no tiene que ser largo; tiene que evitar confusiones importantes. En lugar de «haz una página bonita», explica para quién es, qué información debe mostrar y cómo sabrás que está lista. Esta estructura funciona para casi cualquier tarea:

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

Después de la primera respuesta, mejora paso a paso. Señala el problema observado, aporta el archivo o dato correcto, fija una decisión y pide una verificación. Pedir «hazlo mejor» deja demasiado espacio a la interpretación. Es más útil decir: «El formulario no explica qué campo falta; añade un mensaje claro y prueba qué ocurre cuando el nombre está vacío».

También puedes pedir que la IA haga preguntas antes de actuar: «Si falta información importante, enumera tus dudas y no inventes la respuesta». Esto es especialmente útil cuando el resultado afectará dinero, personas, datos privados o una publicación pública.

## 5. Límites que hay que entender

Los límites son las cosas que la IA no puede garantizar por sí sola. Conocerlos no significa que la IA sea mala o inútil; significa que sabes cuándo confiar en ella como ayuda y cuándo debes revisar con más cuidado.

- **Puede sonar segura y aun así estar equivocada.** La IA puede responder con mucha seguridad y dar una fecha falsa, un enlace que no existe, un cálculo incorrecto o código que parece funcionar sin hacerlo. **Qué hacer:** comprueba los datos importantes y prueba el código antes de usarlo.
- **Puede adivinar lo que no le dijiste.** Si le pides una página para un negocio pero no le das el horario, podría inventar uno para completar la respuesta. **Qué hacer:** comparte los datos confirmados y dile: «Si falta información, pregúntame; no inventes nada».
- **No siempre tiene la información más reciente.** Los precios, leyes, horarios, versiones de programas y noticias pueden cambiar de un día a otro. **Qué hacer:** para temas actuales, entrega una fuente reciente y pide que indique de dónde obtuvo cada dato importante.
- **No debes compartir información privada sin necesidad.** Una contraseña, un código de acceso, una clave secreta que permite a una aplicación usar un servicio en línea o datos personales pueden causar problemas si se comparten. **Qué hacer:** comparte solo lo necesario y usa datos de ejemplo, como `CLAVE_DEL_SERVICIO` o `NOMBRE_DEL_NEGOCIO`, cuando estés escribiendo documentación.
- **No debe actuar más allá de tu permiso.** Que una IA pueda sugerir un comando, redactar un correo o modificar un archivo no significa que deba ejecutarlo, enviarlo o publicarlo. **Qué hacer:** define qué puede hacer y pídele que se detenga antes de cualquier acción externa.
- **La decisión final es tuya.** La IA puede preparar opciones y borradores, pero no conoce todas las consecuencias para ti, tu negocio o las personas afectadas. **Qué hacer:** revisa y aprueba explícitamente antes de publicar, borrar datos, cobrar, desplegar una aplicación, enviar algo a clientes o tomar una decisión legal, médica, financiera o de seguridad.

Una regla fácil de recordar es: usa la IA para **pensar, crear y preparar**; usa tu criterio para **verificar, decidir y aprobar**.

## 6. Chat, Work y Codex: cuál usar

Chat, Work y Codex son tres formas de trabajar con IA dentro del mismo ecosistema. No son tres inteligencias diferentes: son maneras de presentar la ayuda y las herramientas según el tipo de trabajo que quieras hacer.

La pregunta más útil no es «¿cuál es mejor?», sino «¿qué necesito lograr ahora?». Si necesitas conversar y pensar, usa Chat. Si necesitas un trabajo más largo con un resultado listo para revisar, usa Work. Si necesitas crear o modificar software, usa Codex.

Las funciones disponibles pueden cambiar según el plan, el dispositivo, la región y la configuración de tu espacio de trabajo. Esta guía te ayuda a elegir sin tener que memorizar todos los detalles técnicos:

| Opción | Úsala para | Aporta | Revisión humana necesaria |
| --- | --- | --- | --- |
| **Chat** | Preguntas, ideas, aprendizaje y borradores | Conversación rápida y explicación | Comprobar datos y aplicar el resultado |
| **Work** | Investigar, analizar fuentes, preparar entregables o dar seguimiento a trabajo estructurado | Tarea enfocada con fuentes y, cuando se configura, conexiones o seguimiento | Definir alcance y aprobar acciones externas |
| **Codex** | Construir o cambiar software en un repositorio | Contexto de código, edición, pruebas y herramientas de desarrollo | Revisar cambios, pruebas, secretos y publicación |

### Chat: para conversar, aprender y explorar

**Chat** es como hablar con una persona que te ayuda a pensar. Es el mejor lugar para comenzar cuando tienes una duda, una idea poco clara o quieres aprender sin necesidad de modificar archivos ni producir algo final de inmediato.

Úsalo para:

- Preguntar qué significa una palabra o cómo funciona una tecnología.
- Lluvia de ideas para un negocio, una app, un juego o una herramienta.
- Comparar opciones y entender sus ventajas y desventajas.
- Redactar o mejorar un texto corto.
- Pedir que una idea confusa se convierta en una lista de pasos.

**Ejemplo:** tienes la idea de crear una página para una cafetería, pero no sabes qué debe incluir. En Chat puedes preguntar: «Quiero una página sencilla para una cafetería local. ¿Qué información necesita una persona antes de visitarla? Hazme preguntas si falta algo». La respuesta te ayuda a pensar; todavía no está construyendo la página.

También puedes adjuntar un documento de Word o un PDF y hacer preguntas sobre él. Por ejemplo: «Lee este PDF de 12 páginas y explícame con palabras sencillas cuáles son las tres fechas importantes». En este caso, Chat te ayuda a comprender el archivo; no reemplaza leerlo ni comprobar las fechas antes de tomar una decisión.

Chat es una buena primera opción porque puedes avanzar hablando de forma natural. No necesitas escribir una instrucción perfecta desde el primer mensaje: puedes responder «hazlo más corto», «dame tres opciones» o «explícamelo con un ejemplo». Aun así, revisa datos importantes, porque una conversación clara no garantiza que toda la información sea correcta.

### Work: para convertir un objetivo en un resultado revisable

**Work** sirve cuando ya sabes qué resultado quieres y la tarea requiere varios pasos, archivos, investigación o una entrega más completa. En vez de pedir una respuesta corta, le das a la IA un objetivo y materiales para que prepare algo que puedas revisar.

Piensa en Work como encargar un proyecto pequeño a una persona colaboradora: explicas el resultado esperado, entregas los archivos o fuentes necesarias y después revisas el trabajo antes de usarlo o compartirlo.

Úsalo para:

- Investigar un tema y comparar fuentes.
- Analizar una hoja de cálculo o varios documentos.
- Preparar un reporte, una presentación, un plan o una propuesta.
- Convertir notas dispersas en un documento ordenado.
- Dar seguimiento a una tarea que necesita varios pasos y un resultado final claro.

**Ejemplo: entregar un documento.** Tienes las notas de una reunión en Word, una lista de ventas en Excel y comentarios de clientes en un PDF. En Work podrías pedir: «Analiza estos tres archivos y prepara un reporte de una página con los problemas más repetidos, tres oportunidades y las fuentes usadas. Entrégalo como documento de Word o PDF si esa opción está disponible. No lo compartas». La IA puede organizar el material y prepararte un borrador; tú abres el archivo, compruebas los datos y decides si está listo.

**Ejemplo: preparar un correo.** Tienes un PDF con los acuerdos de una reunión. Puedes pedir: «Resume los acuerdos y prepara un correo para el equipo con los próximos pasos. Usa un tono amable; déjalo como borrador y no lo envíes». La IA puede redactar el correo, pero tú revisas nombres, fechas, destinatarios y el mensaje antes de enviarlo desde tu cuenta.

Cuando uses Work, define tres cosas: qué debe entregar, qué fuentes puede usar y qué acciones no debe realizar sin permiso. Por ejemplo: «Entrega una presentación de cinco diapositivas; usa solo estos documentos; prepara un borrador, pero no lo compartas». Work puede utilizar archivos, herramientas y conexiones autorizadas, pero debes revisar el resultado y aprobar cualquier acción que tenga consecuencias.

En algunas configuraciones, Work puede ejecutarse en la nube o, desde la aplicación de escritorio cuando esté habilitado, trabajar con archivos o aplicaciones locales. Esto no significa que tenga acceso automático a todo tu equipo: revisa siempre los permisos que aparecen en pantalla. [OpenAI Docs: usar ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt)

### Codex: para construir, cambiar y probar software

**Codex** está pensado para el trabajo de desarrollo. Úsalo cuando el resultado sea un cambio en un repositorio: una página web, una aplicación móvil, un juego, una herramienta, una automatización, una prueba o documentación técnica.

Codex puede leer archivos del proyecto, entender cómo están relacionados, proponer cambios, editar código y ejecutar pruebas o comandos dentro de los permisos que tenga. También muestra detalles útiles para desarrollo, como los archivos modificados, diferencias entre versiones y resultados de pruebas.

**Ejemplo: sitio web.** Ya tienes una página web con HTML, CSS y JavaScript en un repositorio y quieres agregar un formulario de contacto. En Codex puedes pedir: «Añade un formulario de contacto en la página principal. Modifica solo los archivos de la interfaz; no agregues servicios externos ni publiques nada. Comprueba que el formulario muestre un mensaje claro cuando falte el correo y dime qué pruebas ejecutaste». Codex puede realizar el cambio, pero tú revisas el resultado antes de aceptarlo.

**Ejemplo: proyecto de Node.js.** Node.js es una forma popular de crear sitios web, servidores y herramientas con JavaScript. Si tu proyecto tiene un archivo llamado `package.json`, podrías pedir: «En este proyecto de Node.js, agrega una ruta que muestre una lista de productos de ejemplo. No agregues paquetes nuevos. Ejecuta las pruebas existentes y explícame qué archivos cambiaste». Codex puede leer el proyecto, modificar el código y ejecutar pruebas dentro de los permisos que autorices.

**Ejemplo: aplicación Swift para iPhone.** Swift es el lenguaje usado para muchas apps de Apple, y SwiftUI se usa para construir sus pantallas. Si tienes un proyecto abierto en Xcode, podrías pedir: «En esta app de SwiftUI, añade una pantalla de perfil con nombre, foto de ejemplo y botón de cerrar sesión. No cambies la configuración de publicación ni subas la app a App Store Connect. Compila el proyecto y dime si hubo errores». Así, Codex trabaja en los archivos de la app, mientras tú decides cuándo una versión está lista para compartir o publicar.

**Ejemplo: juego o herramienta.** También puedes usar Codex en un juego hecho con JavaScript, Unity, Godot u otra tecnología, o en una herramienta escrita en Python. Empieza con un cambio pequeño: «Añade una pantalla que muestre la puntuación actual; no modifiques los niveles ni publiques una versión». Un encargo pequeño es más fácil de revisar que «haz todo el juego».

No tienes que ser una persona experta en programación para pedir ayuda a Codex, pero sí necesitas definir el objetivo, el alcance y los límites. Antes de aceptar un cambio, revisa qué archivos modificó, qué dependencias agregó, qué pruebas se ejecutaron y qué no se pudo comprobar. Nunca supongas que un cambio está listo para producción solo porque la IA dijo que terminó.

### Una forma rápida de decidir

Usa estas preguntas como una guía:

1. **¿Quiero entender algo, ordenar una idea o conversar?** Empieza con Chat.
2. **¿Quiero un documento, análisis o entregable que combine varios archivos o pasos?** Usa Work.
3. **¿Quiero cambiar archivos de código o probar un proyecto?** Usa Codex.
4. **¿No estoy seguro?** Empieza con Chat. Cuando la idea esté clara, pasa a Work o Codex según el resultado que necesites.

### Puedes combinarlos en un mismo proyecto

No tienes que elegir una sola opción para siempre. Un flujo práctico podría ser:

1. En **Chat**, explicas tu idea: «Quiero una app para registrar tareas».
2. En **Chat**, conviertes la idea en requisitos: crear, completar y eliminar tareas; sin cuentas ni pagos en la primera versión.
3. En **Work**, reúnes ejemplos, comparas opciones o preparas un plan del proyecto si necesitas investigar más.
4. En **Codex**, construyes la primera versión dentro del repositorio y ejecutas pruebas.
5. De vuelta en **Chat** o Work, redactas las instrucciones de uso, reúnes comentarios y decides la siguiente mejora.

La misma regla de seguridad se aplica a las tres opciones: la IA puede investigar, proponer y preparar; tú revisas, decides y apruebas. Según la documentación oficial de OpenAI, Work puede reunir contexto y herramientas autorizadas para completar tareas de varios pasos, mientras Codex ofrece vistas y herramientas orientadas al desarrollo de software. [OpenAI Docs: elegir Chat, Work o Codex](https://learn.chatgpt.com/docs/use-chatgpt)

## 7. Qué es un agente

Un **agente** es una IA a la que le das un objetivo, instrucciones y herramientas para que avance por varios pasos. En vez de responder solamente una pregunta, puede revisar información, preparar un plan, editar archivos o usar herramientas autorizadas para llegar a un resultado.

Piensa en un agente como un colaborador nuevo al que le encargas una tarea concreta. Si solo le preguntas «¿qué mejorarías de mi página?», obtienes una respuesta. Si le dices «revisa estos archivos, encuentra enlaces rotos, prepara una lista y detente antes de modificar algo», le das un objetivo de varios pasos: eso es trabajar con un agente.

Un agente no es una persona ni tiene criterio propio sobre lo que es importante para ti. Puede ser muy útil y rápido, pero necesita saber qué debe lograr, dónde puede trabajar y qué cosas no puede tocar. No es autónomo por definición: tú eliges sus permisos, los límites y el momento en que debe detenerse para pedir tu aprobación.

La diferencia más fácil de recordar es esta:

- Un **chat** responde y conversa contigo sobre una petición.
- Un **agente** puede organizar una secuencia de tareas para cumplir un objetivo: leer, comparar, preparar, probar y reportar.

Por ejemplo, un chat puede explicarte cómo revisar una lista de productos. Un agente podría leer la lista que le autorizaste, comparar los precios con una hoja de cálculo, señalar los que faltan y entregarte un reporte. Aun así, no debería cambiar precios, enviar el reporte ni publicarlo sin que tú lo autorices.

Trátalo como a un colaborador con acceso limitado. Antes de usarlo, define este contrato mínimo:

- Resultado esperado y forma de medirlo.
- Alcance y elementos explícitamente fuera de alcance.
- Fuentes permitidas y qué información es privada.
- Acciones autorizadas: solo lectura, editar archivos, crear una rama, enviar un borrador, publicar, etc.
- Punto de alto: cuándo debe pedir aprobación.
- Evidencia de cierre: pruebas, enlaces, lista de archivos o reporte de cambios.

**Ejemplo 1: revisar un sitio web sin modificarlo.** Imagina que tienes una página para un negocio y quieres saber si funciona bien antes de compartirla. En lugar de decir «arregla mi página», puedes pedir que el agente primero revise y te entregue un diagnóstico:

```text
Revisa los archivos de esta página web y busca enlaces que no funcionen,
errores de texto y elementos que puedan ser difíciles de usar en un teléfono.
Trabaja solo en modo lectura: no modifiques archivos ni publiques nada.
Entrega una lista con el problema, el archivo donde está y una sugerencia sencilla.
Si para revisar algo necesitas abrir una página externa, avísame primero.
```

Cuando recibas el reporte, léelo y elige qué cambios sí quieres hacer. Después puedes pedir otro paso: «Corrige únicamente los tres enlaces rotos que aprobamos y vuelve a comprobarlos». Separar revisión y cambio evita que la IA toque más de lo necesario.

**Ejemplo 2: preparar un reporte de documentos.** Si tienes un Word con notas de una reunión y un PDF con comentarios de clientes, un agente puede ayudarte sin enviar nada por ti:

```text
Lee estos dos documentos y prepara un resumen de una página.
Incluye los tres problemas que más se repiten y los próximos pasos sugeridos.
Usa solo la información de los archivos adjuntos; si falta un dato, indícalo.
Prepara el resultado como borrador. No envíes correos ni compartas archivos.
```

Aquí el resultado esperado es un borrador revisable, no una acción automática. Antes de enviarlo, comprueba que los nombres, fechas y conclusiones sean correctos.

En Work, un agente puede reunir archivos y fuentes autorizadas para preparar un entregable; en Codex puede revisar un repositorio, modificar código y ejecutar pruebas dentro de los permisos concedidos. La documentación oficial de OpenAI describe Codex como una herramienta para comprender proyectos de código, construir y probar funciones y revisar cambios. [OpenAI Docs: ChatGPT y Codex](https://learn.chatgpt.com/)

Empieza siempre con tareas pequeñas y permisos de solo lectura cuando todavía estás aprendiendo. Una buena primera tarea es «encuentra y reporta»; la siguiente puede ser «corrige solo esto que aprobé». Nunca concedas permisos amplios solo para ahorrar unos minutos, especialmente si el agente puede borrar archivos, enviar correos, publicar contenido o cambiar información de otras personas.

## 8. Ejercicio: llevar una idea a una tarea controlada

Elige un proyecto pequeño: una página para un negocio, un minijuego, una herramienta que renombre archivos o un reporte a partir de una hoja de cálculo. La meta no es terminarlo en un día ni construir algo perfecto. El objetivo es practicar cómo convertir una idea en una tarea clara, pedir ayuda a la IA y revisar el resultado antes de usarlo.

Usaremos como ejemplo una página sencilla para una cafetería. Puedes cambiar el ejemplo por el proyecto que te interese.

### Paso 1: convierte la idea en algo concreto

Escribe cinco líneas simples. No te preocupes por usar términos técnicos:

```text
Proyecto: página web para la cafetería La Esquina.
Personas que la usarán: clientes que buscan horario, ubicación y menú.
Primera versión: una sola página con esa información y un botón para abrir el mapa.
Límites: no habrá pedidos, pagos ni cuentas de usuario.
Estará lista si se lee bien en teléfono y todos los enlaces funcionan.
```

Esto se llama definir el **alcance**: decidir qué sí harás ahora y qué dejarás para después. Es importante porque una idea como «haz la web de mi negocio» es demasiado grande. En cambio, una primera versión pequeña se puede construir, probar y mejorar.

### Paso 2: usa Chat para descubrir lo que falta

Pega tus cinco líneas en Chat y pide ayuda para encontrar dudas antes de construir:

```text
Esta es la primera versión de mi proyecto. Hazme una lista de la información
que todavía necesito confirmar. No inventes datos. Después propón una lista
pequeña de secciones para la página.
```

La IA podría preguntarte por la dirección, el horario, los precios confirmados, el teléfono o las fotos que tienes permiso de usar. Anota las respuestas reales. Si no conoces un dato, deja un espacio marcado como pendiente; no permitas que la IA lo invente solo para terminar rápido.

### Paso 3: guarda una instrucción corta del proyecto

Cuando ya tengas las decisiones principales, crea o guarda una nota dentro del proyecto. Puede llamarse `README.md`, `notas-del-proyecto.md` o como prefieras. Esa nota te ayudará a recordar el objetivo y también dará contexto a Codex cuando trabajes con el código.

```text
Objetivo: mostrar el horario, menú y ubicación confirmados de La Esquina.
No incluye: pedidos, pagos, registro de usuarios ni datos inventados.
Archivos permitidos: los de la página principal.
Prueba esperada: abrir la página en una computadora y un teléfono.
Antes de publicar: revisar todos los textos, precios y enlaces.
```

No necesita ser un documento largo. Una nota clara evita que tú o la IA agreguen funciones que todavía no has decidido.

### Paso 4: pide una tarea pequeña a Codex

No le encargues toda la aplicación de una vez. Elige un cambio que puedas revisar, por ejemplo la primera estructura de la página:

```text
Crea la estructura inicial de una página para esta cafetería usando los
archivos que ya existen en este repositorio. Incluye secciones para horario,
menú y ubicación, con texto de ejemplo claramente marcado como pendiente.
No agregues pagos, formularios, servicios externos ni publiques nada.
Indica qué archivos modificaste y cómo puedo comprobar la página.
```

Si tu proyecto es Node.js, Swift, Python u otra tecnología, la misma idea se mantiene: menciona el archivo o pantalla que debe cambiar, qué no debe tocar y cómo quieres comprobar el resultado. Por ejemplo, en una app Swift puedes pedir una sola pantalla; en Node.js, una sola ruta; en un juego, una pantalla de inicio. Los cambios pequeños son más fáciles de entender y corregir.

### Paso 5: revisa y prueba como si fueras una persona usuaria

Cuando Codex termine, no aceptes el resultado sin mirarlo. Haz estas comprobaciones:

1. Abre los archivos modificados y confirma que solo cambió lo que pediste.
2. Ejecuta la página o la aplicación y prueba el caso principal: ¿se ve el horario?, ¿abre el mapa?, ¿funciona el botón?
3. Prueba algo que pueda fallar: abre la página en un teléfono, deja un campo vacío o usa un enlace que no existe.
4. Lee los textos y reemplaza cualquier dato de ejemplo por información confirmada.
5. Guarda una nota breve: qué hizo la IA, qué corregiste tú y qué queda pendiente.

Por ejemplo: «Codex creó las secciones de horario, menú y ubicación. Cambié el horario porque era texto de ejemplo. Falta agregar las fotos cuando tenga permiso para usarlas». Esta nota te permite retomar el proyecto después sin empezar de cero.

El hábito clave es conservar las decisiones y la evidencia. Así podrás recordar por qué tomaste una decisión, corregir un error y explicarle a otra persona qué hizo la IA y qué decidiste tú. La IA acelera el trabajo sin volverlo opaco cuando mantienes ese control.

## Fuentes para seguir aprendiendo

- [Inicio rápido de ChatGPT](https://learn.chatgpt.com/docs/quickstart?translationFallback=es-419)
- [Configura un compañero de equipo para el proyecto en ChatGPT Work](https://learn.chatgpt.com/es-419/use-cases/project-teammate)
- [Habilidades y complementos de ChatGPT](https://learn.chatgpt.com/es-419/docs/skills-and-plugins)
- [Generative AI for Beginners, en español](https://github.com/microsoft/generative-ai-for-beginners/blob/main/translations/es/README.md)
