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

La aplicación Mac 2.4.12 y su extensión Chrome 2.1.13 incluida admiten los 12 idiomas del sitio web. Las actualizaciones de Chrome Web Store se distribuyen por separado después de su revisión; comprueba la versión de la tienda.

## Cómo evitar una SWG: ruta y excepción TLS

Evitar una SWG implica utilizar otra ruta de red para la conexión. Una excepción de inspección TLS puede mantener el tráfico en la puerta de enlace sin descifrarlo. Una cadena de certificados públicos no demuestra por sí sola que haya cambiado la ruta.

Consulta la [comparación entre bypass de SWG y excepción TLS](https://swgbar.com/es/guides/swg-bypass-vs-tls-exception/) y la [guía para detectar la inspección HTTPS](https://swgbar.com/es/guides/detect-https-inspection/).

Verificada el 4 de noviembre de 2026: el paquete oficial 2.4.12 (compilación 42) coincide con el SHA-256 publicado y supera las comprobaciones de firma y notarización de Apple. La aplicación y la extensión de red nativa instaladas coinciden con el paquete; la extensión Chrome incluida sigue siendo 2.1.13. Las pruebas reales de activación, desactivación, cierre y reinicio se documentan a continuación.

[Tutorial paso a paso](https://swgbar.com/es/guides/how-to-bypass-swg/) · [Prueba completa y limitaciones](https://swgbar.com/es/guides/certificate-check-case-study/)

## Medición documentada y ayuda

[Prueba completa y limitaciones](https://swgbar.com/es/guides/certificate-check-case-study/)

En una prueba de seis conexiones a `www.doubao.com:443` con SWG bar 2.4.12, al desactivar la omisión o cerrar la aplicación se obtuvo una cadena de inspección; al activarla o restaurarla se obtuvo una cadena pública. El caso documenta comprobaciones TLS nuevas, el comportamiento tras reiniciar y los límites de la verificación automática de la aplicación. Los resultados se aplican a las conexiones probadas en esta red.

Esta es la presentación pública oficial del proyecto. Utiliza los [issues](https://github.com/nonbutAworker/swg-bar/issues) para preguntas públicas y sugerencias de documentación. Para consultas privadas, escribe a [support@swgbar.com](mailto:support@swgbar.com). No publiques claves de licencia ni historial de navegación.

[Acerca de SWG bar](https://swgbar.com/es/about/) · [Privacidad](https://swgbar.com/es/privacy/) · [Condiciones](https://swgbar.com/es/terms/)
