# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · **Français** · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

[Site officiel](https://swgbar.com/fr/) · [Télécharger pour Mac](https://swgbar.com/fr/#pricing) · [Guides](https://swgbar.com/fr/guides/)

SWG bar est une application native de la barre des menus de macOS pour examiner l’inspection HTTPS effectuée par une passerelle web sécurisée (SWG). Consultez les résultats des domaines et les certificats sur votre Mac, puis retrouvez les résultats locaux disponibles dans l’extension Chrome.

## Fonctionnalités

- Rechercher les domaines observés et consulter leurs derniers résultats de vérification.
- Examiner les émetteurs, les dates de validité, les empreintes et les domaines associés aux certificats.
- Comparer la confiance des certificats de macOS à une vérification indépendante des racines publiques.
- Afficher dans Chrome les résultats déjà présents dans l’application Mac.

Les données de détection sont analysées et stockées sur le Mac. Les vérifications ouvrent des connexions TLS distinctes ; l’extension lit les résultats locaux existants. Consultez le [fonctionnement](https://swgbar.com/fr/how-it-works/) et la [politique de confidentialité](https://swgbar.com/fr/privacy/).

## Bien démarrer

Nécessite **macOS 14 ou version ultérieure et une puce Apple silicon**. L’essai comprend **14 jours d’utilisation effective** ; les offres actuelles figurent sur le site.

1. Téléchargez l’installateur sur le [site officiel](https://swgbar.com/fr/#pricing) et suivez le [guide d’installation](https://swgbar.com/fr/install/).
2. Ouvrez SWG bar dans la barre des menus et examinez un domaine et ses certificats.
3. Configurez, si vous le souhaitez, l’[extension Chrome](https://swgbar.com/fr/chrome-extension/).

L’application et l’extension prennent en charge l’anglais, le chinois simplifié et traditionnel, le japonais et le coréen. Le site et cette présentation sont disponibles en 12 langues.

## Contourner une SWG ou exclure une connexion de l’inspection TLS ?

Le contournement d’une SWG change le trajet réseau de la connexion. Une exception d’inspection TLS peut laisser le trafic traverser la passerelle sans déchiffrement. Une chaîne de certificats publics ne suffit donc pas à prouver un changement de trajet.

Consultez la [comparaison entre contournement et exception TLS](https://swgbar.com/fr/guides/swg-bypass-vs-tls-exception/) et le [guide de détection de l’inspection HTTPS](https://swgbar.com/fr/guides/detect-https-inspection/).

**État vérifié le 23 octobre 2026 :** la version publiée est la 2.3.5. Le contournement par domaine en un clic est prévu pour la version 2.4.0. Consultez les [informations de version](https://swgbar.com/fr/releases/) et les [guides officiels](https://swgbar.com/fr/guides/) pour les procédures vérifiées.

## Mesure documentée et assistance

L’[étude de vérification des certificats](https://swgbar.com/fr/guides/certificate-check-case-study/) présente une mesure datée de `swgbar.com:443`, des commandes OpenSSL reproductibles, les résultats de macOS et une observation distincte avec le code de vérification de SWG bar. Ces résultats décrivent les connexions mesurées et ne prouvent pas le contournement d’une passerelle.

Ce dépôt est la présentation publique officielle du projet. Utilisez les [issues](https://github.com/nonbutAworker/swg-bar/issues) pour les questions publiques et suggestions de documentation. Pour une demande privée : [support@swgbar.com](mailto:support@swgbar.com). Ne publiez pas de clés de licence ni d’historique de navigation.

[À propos](https://swgbar.com/fr/about/) · [Confidentialité](https://swgbar.com/fr/privacy/) · [Conditions](https://swgbar.com/fr/terms/)
