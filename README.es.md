# SWG bar

[English](README.md) · [Deutsch](README.de.md) · **Español** · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**Detecta la inspección HTTPS. Evita el SWG con un clic.**

[Sitio oficial](https://swgbar.com/es/) · [Descargar para Mac](https://swgbar.com/es/#pricing) · [Guías](https://swgbar.com/es/guides/) · [CLI](https://swgbar.com/es/cli/) · [MCP](https://swgbar.com/es/mcp/)

SWG bar es una aplicación nativa para la barra de menús de macOS que permite detectar la **inspección HTTPS/SSL (break-and-inspect)** realizada por puertas de enlace web seguras (SWG) corporativas —como Zscaler, Netskope y Cloudflare Gateway— y gestionar el **bypass de SWG por dominio con un clic**. Consulta resultados de dominios y pruebas de certificados en tu Mac, revisa los resultados locales registrados desde la extensión de Chrome o automatiza comprobaciones y reglas desde Terminal y agentes de programación con IA.

## Funciones

- **Inspección HTTPS/SSL y pruebas de certificados:** identifica dominios inspeccionados, examina emisores, fechas de validez, huellas SHA-256 y nombres de host asociados, y compara la confianza del llavero de macOS (incluidas las CA raíz instaladas por MDM) con una verificación independiente de raíces públicas.
- **Bypass de SWG por dominio en un clic:** enruta nombres de host seleccionados en macOS sin descifrado HTTPS en la pasarela cuando estés autorizado, desde la barra de menús, la CLI o MCP.
- **Extensión de Chrome (`2.1.13`):** consulta en la barra de herramientas del navegador el resultado local registrado por la aplicación del Mac para el dominio actual.
- **CLI `swgbar` nativa y servidor MCP:** consulta métricas de inspección, ejecuta sondeos TLS bajo demanda y gestiona reglas de bypass desde Terminal ([guía de CLI](https://swgbar.com/es/cli/)) o clientes de IA compatibles con MCP como Claude Desktop, Cursor, Windsurf y Claude Code ([guía de MCP](https://swgbar.com/es/mcp/)).

Los datos de detección se analizan y almacenan localmente en tu Mac. Las comprobaciones abren conexiones TLS IPv4 independientes; la extensión de Chrome es de solo lectura y consulta los resultados locales mediante Chrome Native Messaging. Consulta [cómo funciona](https://swgbar.com/es/how-it-works/), la [política de privacidad](https://swgbar.com/es/privacy/) y la [privacidad de la extensión](https://swgbar.com/es/extension-privacy/).

## Primeros pasos

Requiere **macOS 14 o posterior y Apple silicon** (`arm64`). La prueba gratuita incluye **14 días de uso efectivo** sin tarjeta de crédito; los planes individuales y para equipos actuales están en el [sitio oficial](https://swgbar.com/es/#pricing).

1. Descarga el instalador `.pkg` firmado y notarizado (`2.4.12`, compilación `42`) desde el [sitio oficial](https://swgbar.com/es/#pricing) y sigue la [guía de instalación](https://swgbar.com/es/install/).
2. Abre SWG bar desde la barra de menús para examinar nombres de host, CA raíz y controles de bypass por dominio.
3. Opcionalmente, conecta la [extensión de Chrome](https://swgbar.com/es/chrome-extension/), configura la [CLI `swgbar`](https://swgbar.com/es/cli/) o registra el [servidor MCP](https://swgbar.com/es/mcp/) en tu cliente de IA.

La aplicación para Mac `2.4.12` y la extensión de Chrome `2.1.13` incluida admiten los 12 idiomas del sitio web. Las actualizaciones de Chrome Web Store se publican por separado tras su revisión; comprueba la versión indicada en la tienda.

## Guías: inspección HTTPS, bypass de SWG y errores TLS en CLI e IA

Al analizar una red en macOS, distingue el **enrutamiento de red** del **descifrado TLS**. Evitar una SWG implica usar una ruta fuera del descifrado de la pasarela para un nombre de host; una excepción de inspección TLS puede mantener el tráfico pasando por la pasarela sin descifrarlo, por lo que una cadena de certificados públicos no demuestra por sí sola un cambio de ruta.

- [Cómo detectar la inspección HTTPS y SSL en un Mac](https://swgbar.com/es/guides/detect-https-inspection/) — comprueba cadenas de certificados y CA raíz locales en macOS.
- [Inspección HTTPS de SWG corporativa y MDM en un Mac](https://swgbar.com/es/guides/enterprise-swg-https-inspection-macos/) — por qué Zscaler, Netskope y Cloudflare Gateway mantienen el candado del navegador mediante CA raíz desplegadas con MDM.
- [Cómo evitar una SWG en Mac](https://swgbar.com/es/guides/how-to-bypass-swg/) — configuración paso a paso por dominio, aprobación de la extensión de red de macOS, comportamiento al reiniciar y límites de red.
- [Bypass de SWG frente a excepción de inspección TLS (break-and-inspect)](https://swgbar.com/es/guides/swg-bypass-vs-tls-exception/) — diferencias entre enrutamiento por dominio y excepciones de descifrado en la pasarela.
- [Solucionar errores de certificados TLS y SSL de SWG en herramientas CLI y de IA en Mac](https://swgbar.com/es/guides/swg-tls-certificate-errors-macos/) — resuelve errores `CERTIFICATE_VERIFY_FAILED` y de emisor local en `git`, `npm`, `Python`, `Claude Code` y `Cursor`.

**Estado de la versión, comprobado el 18 de noviembre de 2026:** la versión publicada es **SWG bar 2.4.12** (compilación `42`), que incluye la extensión de red nativa firmada para bypass por dominio, la CLI `swgbar` con servidor MCP y la extensión de Chrome `2.1.13`. La suma SHA-256, la firma de Apple y la notarización del paquete están verificadas. Consulta la [información de versiones](https://swgbar.com/es/releases/) y las [guías oficiales](https://swgbar.com/es/guides/).

## Preguntas y comentarios

Esta es la presentación pública oficial del proyecto. Utiliza los [issues](https://github.com/nonbutAworker/swg-bar/issues) para preguntas públicas y sugerencias de documentación. Para instalación, pedidos o consultas privadas, escribe a [support@swgbar.com](mailto:support@swgbar.com). No publiques claves de licencia ni historial de navegación.

[Acerca de SWG bar](https://swgbar.com/es/about/) · [Privacidad](https://swgbar.com/es/privacy/) · [Privacidad de la extensión](https://swgbar.com/es/extension-privacy/) · [Condiciones](https://swgbar.com/es/terms/)
