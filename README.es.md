# SWG bar

[English](README.md) · [Deutsch](README.de.md) · **Español** · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

[Sitio oficial](https://swgbar.com/es/) · [Descargar para Mac](https://swgbar.com/es/#pricing) · [Guías](https://swgbar.com/es/guides/)

SWG bar es una app nativa para la barra de menús de macOS que permite examinar la inspección HTTPS realizada por una puerta de enlace web segura (SWG). Consulta los resultados de los dominios y sus certificados en tu Mac y accede a los resultados locales disponibles desde la extensión de Chrome.

## Funciones

- Buscar dominios observados y consultar sus últimas comprobaciones.
- Examinar emisores, fechas de validez, huellas digitales y dominios asociados a los certificados.
- Comparar la confianza de certificados de macOS con una comprobación independiente de raíces públicas.
- Ver en Chrome los resultados que ya tiene la app del Mac.

Los datos de detección se analizan y almacenan en el Mac. Las comprobaciones abren conexiones TLS independientes; la extensión lee resultados locales existentes. Consulta [cómo funciona](https://swgbar.com/es/how-it-works/) y la [política de privacidad](https://swgbar.com/es/privacy/).

## Primeros pasos

Requiere **macOS 14 o posterior y Apple silicon**. La prueba incluye **14 días de uso efectivo**; los planes actuales están en el sitio web.

1. Descarga el instalador desde el [sitio oficial](https://swgbar.com/es/#pricing) y sigue la [guía de instalación](https://swgbar.com/es/install/).
2. Abre SWG bar desde la barra de menús y examina un dominio y sus certificados.
3. Configura, si lo deseas, la [extensión de Chrome](https://swgbar.com/es/chrome-extension/).

La app para Mac admite inglés, chino simplificado, chino tradicional, japonés y coreano. La extensión de Chrome 2.1.13, incluida con la app para Mac 2.3.7, admite los 12 idiomas del sitio web. Las actualizaciones de Chrome Web Store se publican por separado tras la revisión; comprueba la versión indicada en la tienda.

## Cómo evitar una SWG: ruta y excepción TLS

Evitar una SWG implica utilizar otra ruta de red para la conexión. Una excepción de inspección TLS puede mantener el tráfico en la puerta de enlace sin descifrarlo. Una cadena de certificados públicos no demuestra por sí sola que haya cambiado la ruta.

Consulta la [comparación entre bypass de SWG y excepción TLS](https://swgbar.com/es/guides/swg-bypass-vs-tls-exception/) y la [guía para detectar la inspección HTTPS](https://swgbar.com/es/guides/detect-https-inspection/).

**Estado comprobado el 24 de octubre de 2026:** la versión publicada es la 2.3.7. El bypass de dominios con un clic está previsto para la 2.4.0. Consulta las [versiones](https://swgbar.com/es/releases/) y las [guías oficiales](https://swgbar.com/es/guides/) para obtener instrucciones verificadas.

## Medición documentada y ayuda

El [caso de comprobación de certificados](https://swgbar.com/es/guides/certificate-check-case-study/) incluye una medición fechada de `swgbar.com:443`, comandos de OpenSSL que puedes repetir, resultados de macOS y una observación independiente con el código de comprobación de SWG bar. Los resultados describen esas conexiones y no demuestran que se haya evitado una puerta de enlace.

Esta es la presentación pública oficial del proyecto. Utiliza los [issues](https://github.com/nonbutAworker/swg-bar/issues) para preguntas públicas y sugerencias de documentación. Para consultas privadas, escribe a [support@swgbar.com](mailto:support@swgbar.com). No publiques claves de licencia ni historial de navegación.

[Acerca de SWG bar](https://swgbar.com/es/about/) · [Privacidad](https://swgbar.com/es/privacy/) · [Condiciones](https://swgbar.com/es/terms/)
