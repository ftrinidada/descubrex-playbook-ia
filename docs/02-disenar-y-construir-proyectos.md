# Diseñar y construir proyectos con IA

Una idea no se vuelve un producto útil por pedir a una IA que «haga una app». Antes de escribir código, hay que decidir qué problema se resolverá, para quién, qué debe ocurrir en la primera versión y cómo se comprobará. Este proceso sirve para un sitio web, una aplicación móvil, un juego, una automatización o una herramienta interna.

La IA acelera la exploración, el diseño, la implementación y las pruebas. La responsabilidad de elegir el problema, aceptar los cambios y proteger a las personas sigue siendo humana.

## 1. De la idea al problema concreto

Empieza con una frase que describa una necesidad observable, no una solución ni una lista de tecnologías.

| Idea inicial | Problema concreto |
| --- | --- |
| «Quiero una app de tareas» | «Una persona pierde tareas pequeñas entre mensajes y notas; necesita registrar, ordenar y completar una tarea desde el teléfono en pocos segundos.» |
| «Quiero una web para mi negocio» | «Quien busca el negocio no encuentra con rapidez qué ofrece, dónde está ni cuándo abre.» |
| «Quiero automatizar reportes» | «Cada semana alguien copia los mismos datos a un resumen; necesita detectar datos faltantes y preparar un borrador revisable.» |
| «Quiero hacer un juego» | «El jugador necesita entender la meta y recibir una recompensa clara durante los primeros minutos.» |

Después escribe una ficha corta. Puede vivir en un `README`, una issue o un archivo de planificación del repositorio.

```text
Proyecto: Lista de tareas personal
Usuario principal: Persona que organiza pendientes diarios desde el teléfono.
Problema: Registrar y completar un pendiente debe requerir pocos pasos.
Primera versión: Crear, ver, marcar como completada y eliminar una tarea local.
No incluye: Cuentas, pagos, colaboración ni sincronización.
Éxito: Una persona puede completar esas cuatro acciones sin instrucciones.
Riesgos: Borrado accidental y pérdida de datos al actualizar.
```

Esta ficha es más valiosa que una especificación larga pero ambigua. Da a la IA contexto suficiente para proponer alternativas sin inventar el objetivo.

## 2. Define la primera versión comprobable

La primera versión viable no es «la aplicación completa». Es la porción más pequeña que permite probar una hipótesis con personas o con un flujo real. Debe tener un resultado visible y una forma de verificarlo.

Divide los requisitos en tres grupos:

- **Imprescindible:** sin esto, el flujo principal no funciona.
- **Deseable:** mejora la experiencia, pero puede esperar.
- **Fuera de alcance:** se anota para no olvidarlo, pero no se construye ahora.

Para una página de un restaurante, por ejemplo, lo imprescindible puede ser nombre, propuesta, menú confirmado, horario, ubicación y una forma de contacto. Animaciones, reseñas inventadas, pedidos en línea y una aplicación nativa pueden esperar. Para una automatización, conserva una revisión humana antes de enviar correos, modificar registros o ejecutar pagos.

Escribe también criterios de aceptación. Son afirmaciones que una persona puede comprobar:

```text
- Al abrir la página desde un teléfono, se puede leer el horario sin hacer zoom.
- El enlace de ubicación abre el mapa con la dirección correcta.
- Si falta un dato en el reporte, el borrador lo señala y no se envía automáticamente.
- Al reiniciar el juego, el jugador vuelve a un estado conocido.
```

Evita criterios como «que se vea profesional» o «que sea rápido» si no explicas qué significan. Puedes transformarlos en medidas: «el texto tiene contraste suficiente», «la pantalla principal aparece en menos de dos segundos en la prueba acordada» o «no hay errores en la consola durante este flujo».

## 3. Elige un camino técnico con intención

No existe una tecnología correcta para todos los proyectos. Elige la opción más sencilla que cubra los requisitos actuales y que puedas mantener.

| Tipo de proyecto | Primera opción razonable | Decide después si necesitas |
| --- | --- | --- |
| Sitio informativo | HTML, CSS y JavaScript o un generador de sitios | Servidor, base de datos o cuentas |
| Herramienta interna | Interfaz web sencilla y datos de prueba | Integraciones, permisos por rol o auditoría |
| Aplicación móvil | Una plataforma objetivo y almacenamiento local | Sincronización, notificaciones o pagos |
| Juego pequeño | Un motor o biblioteca apropiada para su mecánica | Multijugador, tienda o servicios en línea |
| Automatización | Script con entradas y salidas explícitas | Ejecución programada y acceso a sistemas externos |

Antes de aceptar una propuesta de la IA, pide que compare dos o tres alternativas usando tus restricciones: plataforma, experiencia del equipo, presupuesto, tiempo, privacidad, mantenimiento y compatibilidad. No adoptes una dependencia, servicio de pago o integración externa solo porque aparece en un ejemplo.

Toda decisión técnica importante merece una nota breve:

```text
Decisión: Guardar las tareas solo en el dispositivo en la primera versión.
Motivo: Permite validar el flujo sin cuentas ni servidor.
Consecuencia: Las tareas no se comparten entre dispositivos.
Cuándo revisarla: Si las personas usuarias piden sincronización.
```

## 4. Convierte el trabajo en partes pequeñas

Un proyecto se vuelve manejable cuando cada cambio tiene un propósito, un límite y una prueba. Una secuencia habitual es:

1. Crear la estructura mínima y explicar cómo ejecutar el proyecto.
2. Construir un flujo visible de extremo a extremo con datos de ejemplo.
3. Añadir validaciones, mensajes de error y estados vacíos.
4. Guardar datos o conectar servicios solo cuando el flujo básico ya está claro.
5. Mejorar accesibilidad, rendimiento, seguridad y diseño.
6. Preparar pruebas, publicación y mantenimiento.

No hace falta terminar cada capa antes de ver algo funcionando. Un recorrido vertical pequeño —por ejemplo, crear y completar una tarea— revela más problemas que construir durante semanas una arquitectura sin interfaz.

Para cada parte, una tarea útil para Codex incluye archivos permitidos y una comprobación:

```text
Implementa el flujo de alta de tareas en este repositorio.
Alcance: solo la pantalla principal y el almacenamiento local; no agregues cuentas ni paquetes nuevos.
Condiciones: valida que el título no esté vacío y muestra un mensaje accesible cuando falle.
Pruebas: ejecuta las pruebas existentes y describe una prueba manual para crear, completar y reiniciar.
Antes de modificar configuraciones de publicación o usar servicios externos, detente y pide aprobación.
```

Revisa el plan antes de permitir cambios grandes. Si la tarea afecta datos, autenticación, pagos, permisos, infraestructura o publicación, pide primero una propuesta y un análisis de riesgos.

## 5. Trabaja con IA sin perder el control

La IA puede servir en cada etapa, con peticiones distintas:

| Etapa | Petición útil | Revisión humana |
| --- | --- | --- |
| Descubrimiento | «Enumera preguntas abiertas y supuestos de esta ficha.» | Elegir el problema y los límites. |
| Diseño | «Propón tres flujos para esta pantalla y explica sus ventajas.» | Validar que el flujo representa necesidades reales. |
| Implementación | «Aplica este cambio acotado y ejecuta estas pruebas.» | Leer el cambio y probar el comportamiento. |
| Diagnóstico | «Investiga este error; separa hechos, hipótesis y próximos pasos.» | Confirmar la causa antes de una corrección arriesgada. |
| Documentación | «Explica cómo ejecutar el proyecto según sus archivos actuales.» | Ejecutar las instrucciones desde una copia limpia. |

Da a la IA información verificable: el error completo, el comportamiento esperado, los archivos relevantes y los comandos permitidos. Pide que distinga observaciones de suposiciones. Una respuesta útil puede decir «no encontré una prueba para este caso»; no debe fingir que la ejecutó.

Cuando Codex edite un repositorio, revisa especialmente:

- Archivos cambiados y archivos nuevos.
- Dependencias, licencias y scripts agregados.
- Variables de entorno, permisos y configuración de despliegue.
- Datos de ejemplo que puedan parecer datos reales.
- Resultado de pruebas y cualquier prueba que no se pudo ejecutar.

Conserva cambios pequeños y coherentes. Eso hace más fácil revisar, revertir y entender el historial con Git.

## 6. Diseña para casos reales, no solo para la demostración

El flujo feliz es aquel donde todo sale bien: hay conexión, los datos son válidos y la persona entiende la interfaz. Un proyecto útil también explica qué ocurre cuando no es así.

Incluye desde temprano estos estados:

- Carga: la persona sabe que el sistema está trabajando.
- Vacío: se explica qué hacer cuando aún no hay contenido.
- Error: se describe el problema sin culpar a la persona y se ofrece una acción posible.
- Éxito: se confirma qué cambió.
- Sin conexión o permiso denegado: se conserva el trabajo cuando sea posible y se indica el siguiente paso.

La accesibilidad no es un ajuste final. Usa etiquetas claras, navegación con teclado cuando aplique, texto legible, contraste suficiente y mensajes que no dependan solo del color. Prueba en una pantalla pequeña, con tamaño de texto aumentado y con los controles disponibles para la plataforma.

No inventes contenido para llenar espacios: precios, direcciones, reseñas, políticas o datos de contacto deben venir de una fuente confirmada. Marca los datos pendientes como pendientes.

## 7. Prueba antes de ampliar el alcance

Prueba los criterios de aceptación después de cada cambio relevante. Combina tres niveles:

1. **Prueba manual:** recorre el flujo como lo haría una persona; incluye errores y datos vacíos.
2. **Pruebas automatizadas:** codifican comportamientos repetibles y previenen regresiones.
3. **Revisión:** otra persona o una IA puede detectar incoherencias, pero no sustituye ejecutar el producto.

Un reporte de cierre sencillo deja evidencia:

```text
Cambio: Formulario para crear tareas.
Probado: título válido, título vacío, tarea completada y reinicio de la aplicación.
Resultado: los cuatro casos funcionan en navegador y teléfono de prueba.
Pendiente: confirmar comportamiento al agotar almacenamiento local.
```

Si algo no se pudo probar, dilo de forma explícita. «No probado» es mejor que «funciona probablemente».

## 8. Ejercicio: plan de una primera versión

Elige una idea y prepara una ficha de una página con:

1. El problema, la persona usuaria y el resultado esperado.
2. Un flujo principal de tres a cinco pasos.
3. Requisitos imprescindibles, deseables y fuera de alcance.
4. Dos riesgos y cómo evitarás que causen daño.
5. Tres criterios de aceptación comprobables.
6. La primera tarea que entregarías a Codex, indicando archivos permitidos y prueba esperada.

Pide a Chat o Codex que encuentre ambigüedades y supuestos en la ficha. Decide cuáles conservar, corrige el documento y solo entonces empieza la implementación. Ese pequeño ciclo de pensar, construir, probar y registrar decisiones es la base para proyectos más grandes.

## Siguiente capítulo

El siguiente capítulo explicará cómo elegir entre ChatGPT, Codex, agentes, skills, plugins y conexiones, y cómo otorgarles solo los permisos necesarios.
