# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · **Português (BR)** · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

[Site oficial](https://swgbar.com/pt-BR/) · [Baixar para Mac](https://swgbar.com/pt-BR/#pricing) · [Guias](https://swgbar.com/pt-BR/guides/)

SWG bar é um aplicativo nativo para a barra de menus do macOS que permite examinar a inspeção HTTPS feita por um gateway web seguro (SWG). Consulte os resultados dos domínios e os certificados no Mac e veja os resultados locais disponíveis na extensão do Chrome.

## Recursos

- Pesquise os domínios observados e consulte os resultados das últimas verificações.
- Examine emissores, prazos de validade, impressões digitais e domínios associados aos certificados.
- Compare a avaliação de confiança do macOS com uma verificação independente de raízes públicas.
- Veja no Chrome os resultados que já estão armazenados no aplicativo do Mac.

Os dados de detecção são analisados e armazenados no Mac. As verificações abrem conexões TLS separadas; a extensão lê resultados locais existentes. Consulte [como funciona](https://swgbar.com/pt-BR/how-it-works/) e a [política de privacidade](https://swgbar.com/pt-BR/privacy/).

## Primeiros passos

Requer **macOS 14 ou posterior e Apple silicon**. O teste gratuito inclui **14 dias de uso efetivo**; os planos atuais estão no site.

1. Baixe o instalador no [site oficial](https://swgbar.com/pt-BR/#pricing) e siga o [guia de instalação](https://swgbar.com/pt-BR/install/).
2. Abra o SWG bar na barra de menus e examine um domínio e seus certificados.
3. Se desejar, configure a [extensão do Chrome](https://swgbar.com/pt-BR/chrome-extension/).

O aplicativo para Mac oferece inglês, chinês simplificado e tradicional, japonês e coreano. A extensão do Chrome 2.1.13, incluída no aplicativo para Mac 2.3.7, oferece os 12 idiomas do site. As atualizações da Chrome Web Store são publicadas separadamente após a análise; confira a versão exibida na loja.

## Bypass de SWG ou exceção de inspeção TLS?

O bypass de um SWG altera o caminho de rede da conexão. Uma exceção de inspeção TLS pode manter o tráfego passando pelo gateway sem descriptografá-lo. Uma cadeia de certificados públicos, por si só, não comprova que o caminho mudou.

Leia a [comparação entre bypass de SWG e exceção TLS](https://swgbar.com/pt-BR/guides/swg-bypass-vs-tls-exception/) e o [guia para detectar inspeção HTTPS](https://swgbar.com/pt-BR/guides/detect-https-inspection/).

**Verificado em 24 de outubro de 2026:** o instalador publicado é o 2.3.7. O bypass de domínios com um clique está previsto para a versão 2.4.0. Consulte as [informações de versão](https://swgbar.com/pt-BR/releases/) e os [guias oficiais](https://swgbar.com/pt-BR/guides/) para instruções verificadas.

## Medição documentada e suporte

O [estudo de verificação de certificados](https://swgbar.com/pt-BR/guides/certificate-check-case-study/) apresenta uma medição datada de `swgbar.com:443`, comandos OpenSSL que você pode repetir, resultados do macOS e uma observação separada com o código de verificação do SWG bar. Os resultados descrevem as conexões medidas e não comprovam o bypass de um gateway.

Este é o repositório oficial de apresentação pública do projeto. Use as [issues](https://github.com/nonbutAworker/swg-bar/issues) para perguntas públicas e sugestões de documentação. Para assuntos privados, escreva para [support@swgbar.com](mailto:support@swgbar.com). Não publique chaves de licença ou histórico de navegação.

[Sobre o SWG bar](https://swgbar.com/pt-BR/about/) · [Privacidade](https://swgbar.com/pt-BR/privacy/) · [Termos](https://swgbar.com/pt-BR/terms/)
