# DescubreX Playbook

Manual vivo en espanol para documentar el aprendizaje practico alrededor de IA, ChatGPT, Codex, GitHub y la publicacion de aplicaciones moviles.

> Este repositorio es una guia educativa. No contiene codigo privado de las apps, llaves, tokens, certificados, perfiles de firma ni datos personales.

## Objetivo

Convertir lo aprendido al construir y publicar apps en un manual claro que otra persona con bases de programacion pueda leer, revisar y mejorar. El formato fuente es Markdown en GitHub: es facil de editar, mantiene historial y permite comentar cambios.

## Como usar este manual

1. Lee los capitulos en orden si empiezas desde cero.
2. Usa los ejemplos como referencia, pero adapta cada paso a tu proyecto.
3. Cuando resolvamos algo nuevo, agrega una nota breve: contexto, decision, pasos, resultado y precauciones.
4. No subas secretos. Usa nombres de variables como `API_KEY` o `IOS_TEAM_ID`, nunca sus valores.

## Ruta de aprendizaje

- [ ] Introduccion a IA: modelos, chat, contexto, prompts y limites.
- [ ] ChatGPT: conversaciones, proyectos, archivos y trabajo colaborativo.
- [ ] Codex: tareas, workspace, modelos, revisiones y pruebas.
- [ ] Skills y plugins: cuando usar flujos reutilizables y conexiones externas.
- [ ] Git y GitHub: repositorios, ramas, commits, tags, issues y pull requests.
- [ ] Seguridad: secretos, API keys, autenticacion, permisos, dependencias y escaneos.
- [ ] Android: build, firma, versionado, Google Play y pruebas internas.
- [ ] iOS: certificados, provisioning profiles, versionado, TestFlight y App Store Connect.
- [ ] Pipeline de releases: validacion, tag, compilacion, carga a tiendas y aprobacion explicita de produccion.
- [ ] Bitacora DescubreX: decisiones y aprendizajes aplicados al proyecto real, sin informacion sensible.

## Principios para las publicaciones

- El documento puede ser publico; la configuracion secreta y el codigo de las aplicaciones no.
- Un cambio pequeno no siempre amerita una version mayor: se usa versionado semantico como guia.
- Automatizar una carga a TestFlight o Google Play no debe equivaler a publicar en produccion. Produccion siempre lleva una aprobacion explicita.
- Antes de compartir, revisa texto, capturas y archivos para evitar tokens, correos privados, IDs de perfiles o rutas personales.

## Estructura prevista

`docs/` tendra los capitulos detallados; el README sera siempre la portada y el indice. Los PDF solo seran versiones de consulta ocasionales: Markdown es la fuente que se mantiene actualizada.

## Fuentes oficiales iniciales

- [Documentacion de Codex y OpenAI](https://platform.openai.com/docs)
- [GitHub Docs](https://docs.github.com)
- [Apple Developer](https://developer.apple.com/documentation/)
- [Google Play Console Help](https://support.google.com/googleplay/android-developer/)

## Estado

Creado el 16 de septiembre de 2026. Proximo paso: escribir el primer capitulo, **Introduccion a IA, ChatGPT y Codex**, y despues documentar el pipeline Android/iOS de forma segura.
