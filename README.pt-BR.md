# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · **Português (BR)** · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**Detecte a inspeção HTTPS. Contorne o SWG com um clique.**

[Site oficial](https://swgbar.com/pt-BR/) · [Baixar para Mac](https://swgbar.com/pt-BR/#pricing) · [Guias](https://swgbar.com/pt-BR/guides/) · [CLI](https://swgbar.com/pt-BR/cli/) · [MCP](https://swgbar.com/pt-BR/mcp/)

O SWG bar é um aplicativo nativo para a barra de menus do macOS projetado para detectar **inspeção HTTPS/SSL (break-and-inspect)** realizada por gateways web seguros (SWG) corporativos — como Zscaler, Netskope e Cloudflare Gateway — e gerenciar o **bypass de SWG por domínio com um clique**. Consulte resultados de domínios e evidências de certificados no Mac, veja os resultados locais registrados pela extensão do Chrome ou automatize verificações e regras pelo Terminal e por agentes de programação com IA.

## Recursos

- **Inspeção HTTPS/SSL e evidências de certificados:** identifique domínios inspecionados, examine emissores, prazos de validade, impressões digitais SHA-256 e nomes de host associados, e compare a avaliação de confiança das Chaves do macOS (incluindo CAs raiz instaladas via MDM) com uma verificação independente de raízes públicas.
- **Bypass de SWG por domínio com um clique:** direcione nomes de host selecionados no macOS sem descriptografia HTTPS no gateway em redes autorizadas, pela barra de menus, CLI ou MCP.
- **Extensão do Chrome (`2.1.13`):** veja diretamente na barra de ferramentas do navegador o resultado local já registrado pelo aplicativo do Mac para o domínio atual.
- **CLI `swgbar` nativa e servidor MCP:** consulte dados de inspeção, execute sondagens TLS sob demanda e alterne o bypass por domínio pelo Terminal ([guia da CLI](https://swgbar.com/pt-BR/cli/)) ou por clientes de IA compatíveis com MCP, como Claude Desktop, Cursor, Windsurf e Claude Code ([guia do MCP](https://swgbar.com/pt-BR/mcp/)).

Os dados de detecção são analisados e armazenados localmente no Mac. As verificações abrem conexões TLS IPv4 separadas; a extensão do Chrome é somente leitura via Chrome Native Messaging e consulta os resultados locais existentes. Veja [como o SWG bar funciona](https://swgbar.com/pt-BR/how-it-works/), a [política de privacidade](https://swgbar.com/pt-BR/privacy/) e a [privacidade da extensão](https://swgbar.com/pt-BR/extension-privacy/).

## Primeiros passos

Requer **macOS 14 ou posterior e Apple silicon** (`arm64`). O teste gratuito inclui **14 dias de uso efetivo** sem cartão de crédito; os planos individuais e para equipes atuais estão no [site oficial](https://swgbar.com/pt-BR/#pricing).

1. Baixe o instalador `.pkg` assinado e notarizado (`2.4.12`, compilação `42`) no [site oficial](https://swgbar.com/pt-BR/#pricing) e siga o [guia de instalação](https://swgbar.com/pt-BR/install/).
2. Abra o SWG bar na barra de menus para examinar nomes de host, CAs raiz e controles de bypass por domínio.
3. Se desejar, conecte a [extensão do Chrome](https://swgbar.com/pt-BR/chrome-extension/), configure a [CLI `swgbar`](https://swgbar.com/pt-BR/cli/) ou registre o [servidor MCP](https://swgbar.com/pt-BR/mcp/) no seu cliente de IA.

O aplicativo para Mac `2.4.12` e a extensão do Chrome `2.1.13` incluída oferecem suporte aos 12 idiomas do site. As atualizações da Chrome Web Store são publicadas separadamente após análise; confira a versão exibida na loja.

## Guias: inspeção HTTPS, bypass de SWG e erros TLS em CLI e IA

Ao investigar conexões no macOS, separe **roteamento de rede** de **descriptografia TLS**. Contornar uma SWG altera a rota de rede de um nome de host para fora da descriptografia do gateway; uma exceção de inspeção TLS pode manter o tráfego passando pelo gateway sem descriptografá-lo, portanto uma cadeia de certificados públicos, por si só, não comprova mudança de rota.

- [Como detectar inspeção HTTPS e SSL no Mac](https://swgbar.com/pt-BR/guides/detect-https-inspection/) — verifique cadeias de certificados e CAs raiz locais no macOS.
- [Inspeção HTTPS de SWG corporativa e MDM no Mac](https://swgbar.com/pt-BR/guides/enterprise-swg-https-inspection-macos/) — por que Zscaler, Netskope e Cloudflare Gateway mantêm o cadeado do navegador intacto com CAs raiz via MDM.
- [Como contornar uma SWG no Mac](https://swgbar.com/pt-BR/guides/how-to-bypass-swg/) — configuração passo a passo por domínio, aprovação da extensão de rede do macOS, comportamento ao reiniciar e limites de rede.
- [Bypass de SWG vs. exceção de inspeção TLS (break-and-inspect)](https://swgbar.com/pt-BR/guides/swg-bypass-vs-tls-exception/) — diferenças entre roteamento por domínio e exceções de descriptografia no gateway.
- [Corrigir erros de certificado TLS e SSL de SWG em CLI e IA no Mac](https://swgbar.com/pt-BR/guides/swg-tls-certificate-errors-macos/) — resolva `CERTIFICATE_VERIFY_FAILED` e erros de emissor local no `git`, `npm`, `Python`, `Claude Code` e `Cursor`.

**Status da versão, verificado em 18 de novembro de 2026:** a versão publicada é o **SWG bar 2.4.12** (compilação `42`), com extensão de rede nativa assinada para bypass por domínio, CLI `swgbar` e servidor MCP, além da extensão do Chrome `2.1.13`. O checksum SHA-256, a assinatura da Apple e a notarização do pacote foram verificados. Consulte as [informações de versões](https://swgbar.com/pt-BR/releases/) e os [guias oficiais](https://swgbar.com/pt-BR/guides/).

## Perguntas e comentários

Este é o repositório oficial de apresentação pública do projeto. Use as [issues](https://github.com/nonbutAworker/swg-bar/issues) para perguntas públicas e sugestões de documentação. Para instalação, pedidos ou assuntos privados, escreva para [support@swgbar.com](mailto:support@swgbar.com). Não publique chaves de licença ou histórico de navegação.

[Sobre o SWG bar](https://swgbar.com/pt-BR/about/) · [Privacidade](https://swgbar.com/pt-BR/privacy/) · [Privacidade da extensão](https://swgbar.com/pt-BR/extension-privacy/) · [Termos](https://swgbar.com/pt-BR/terms/)
