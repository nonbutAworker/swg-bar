# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · **Français** · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**Détectez l’inspection HTTPS. Contournez la SWG en un clic.**

[Site officiel](https://swgbar.com/fr/) · [Télécharger pour Mac](https://swgbar.com/fr/#pricing) · [Guides](https://swgbar.com/fr/guides/) · [CLI](https://swgbar.com/fr/cli/) · [MCP](https://swgbar.com/fr/mcp/)

SWG bar est une application native de la barre des menus de macOS permettant de détecter l’**inspection HTTPS/SSL (break-and-inspect)** effectuée par les passerelles web sécurisées (SWG) d’entreprise — telles que Zscaler, Netskope et Cloudflare Gateway — et de gérer le **contournement de SWG par domaine en un clic**. Examinez les résultats par domaine et les preuves de certificats sur votre Mac, consultez les résultats locaux enregistrés dans Chrome grâce à l’extension compagnon, ou pilotez vos vérifications et règles depuis le Terminal et vos agents de développement IA.

## Fonctionnalités

- **Inspection HTTPS/SSL et preuves de certificats :** identifiez les domaines inspectés, examinez les émetteurs, dates de validité, empreintes SHA-256 et noms d’hôtes associés, et comparez l’évaluation du trousseau macOS (y compris les CA racines déployées par MDM) à une vérification indépendante des racines publiques.
- **Contournement de SWG par domaine en un clic :** acheminez les noms d’hôtes sélectionnés sur macOS sans déchiffrement HTTPS par la passerelle lorsque vous y êtes autorisé, depuis la barre des menus, la CLI ou MCP.
- **Extension compagnon Chrome (`2.1.13`) :** consultez directement dans la barre d’outils du navigateur le résultat local enregistré par l’application Mac pour le domaine actif.
- **CLI `swgbar` native et serveur MCP :** interrogez la télémétrie d’inspection, lancez des sondes TLS à la demande et gérez le contournement par domaine depuis le Terminal ([guide CLI](https://swgbar.com/fr/cli/)) ou des clients IA compatibles MCP tels que Claude Desktop, Cursor, Windsurf et Claude Code ([guide MCP](https://swgbar.com/fr/mcp/)).

Les données de détection sont analysées et stockées localement sur le Mac. Les sondes ouvrent des connexions TLS IPv4 distinctes ; l’extension Chrome fonctionne en lecture seule via Chrome Native Messaging et lit les résultats locaux existants. Consultez le [fonctionnement](https://swgbar.com/fr/how-it-works/), la [politique de confidentialité](https://swgbar.com/fr/privacy/) et la [confidentialité de l’extension](https://swgbar.com/fr/extension-privacy/).

## Bien démarrer

Nécessite **macOS 14 ou version ultérieure et une puce Apple silicon** (`arm64`). L’essai gratuit comprend **14 jours d’utilisation effective** sans carte bancaire ; les formules individuelles et d’équipe figurent sur le [site officiel](https://swgbar.com/fr/#pricing).

1. Téléchargez l’installateur `.pkg` signé et notarié (`2.4.12`, build `42`) sur le [site officiel](https://swgbar.com/fr/#pricing) et suivez le [guide d’installation](https://swgbar.com/fr/install/).
2. Ouvrez SWG bar dans la barre des menus pour examiner les noms d’hôtes, les autorités racines (CA) et les commandes de contournement par domaine.
3. Configurez, selon vos besoins, l’[extension Chrome](https://swgbar.com/fr/chrome-extension/), la [CLI `swgbar`](https://swgbar.com/fr/cli/) ou le [serveur MCP](https://swgbar.com/fr/mcp/) dans votre client IA.

L’application Mac `2.4.12` et l’extension Chrome `2.1.13` fournie prennent en charge les 12 langues du site. Les mises à jour du Chrome Web Store sont publiées séparément après examen ; vérifiez la version affichée dans la boutique.

## Guides : inspection HTTPS, contournement SWG et erreurs TLS (CLI / IA)

Sur macOS, distinguez le **routage réseau** du **déchiffrement TLS**. Contourner une SWG consiste à emprunter un trajet hors déchiffrement de la passerelle pour un nom d’hôte ; une exception d’inspection TLS peut laisser le trafic traverser la passerelle sans déchiffrement, de sorte qu’une chaîne de certificats publics ne suffit pas à prouver un changement de trajet.

- [Comment détecter l’inspection HTTPS et SSL sur un Mac](https://swgbar.com/fr/guides/detect-https-inspection/) — vérifier les chaînes de certificats et les CA racines locales sur macOS.
- [Inspection HTTPS par SWG d’entreprise et MDM sur Mac](https://swgbar.com/fr/guides/enterprise-swg-https-inspection-macos/) — pourquoi Zscaler, Netskope et Cloudflare Gateway conservent le cadenas du navigateur via des CA racines MDM.
- [Comment contourner une SWG sur Mac](https://swgbar.com/fr/guides/how-to-bypass-swg/) — configuration étape par étape par domaine, approbation de l’extension réseau macOS, redémarrage et limites réseau.
- [Contournement de SWG vs exception d’inspection TLS (break-and-inspect)](https://swgbar.com/fr/guides/swg-bypass-vs-tls-exception/) — différences entre routage par domaine et exceptions de déchiffrement sur la passerelle.
- [Corriger les erreurs de certificats TLS et SSL liés à une SWG dans les outils CLI et IA sur Mac](https://swgbar.com/fr/guides/swg-tls-certificate-errors-macos/) — résoudre `CERTIFICATE_VERIFY_FAILED` et les erreurs d’émetteur local dans `git`, `npm`, `Python`, `Claude Code` et `Cursor`.

**État de la version, vérifié le 18 novembre 2026 :** la version publiée est **SWG bar 2.4.12** (build `42`), incluant l’extension réseau native signée pour le contournement par domaine, la CLI `swgbar` et le serveur MCP, ainsi que l’extension Chrome `2.1.13`. La somme SHA-256, la signature Apple et la notarisation du paquet ont été vérifiées. Consultez les [informations de version](https://swgbar.com/fr/releases/) et les [guides officiels](https://swgbar.com/fr/guides/).

## Questions et commentaires

Ce dépôt est la présentation publique officielle du projet. Utilisez les [issues](https://github.com/nonbutAworker/swg-bar/issues) pour les questions publiques et suggestions de documentation. Pour l’installation, les commandes ou une demande privée : [support@swgbar.com](mailto:support@swgbar.com). Ne publiez pas de clés de licence ni d’historique de navigation.

[À propos](https://swgbar.com/fr/about/) · [Confidentialité](https://swgbar.com/fr/privacy/) · [Confidentialité de l’extension](https://swgbar.com/fr/extension-privacy/) · [Conditions](https://swgbar.com/fr/terms/)
