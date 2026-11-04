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

L’application Mac 2.4.12 et l’extension Chrome 2.1.13 fournie prennent en charge les 12 langues du site. Les mises à jour du Chrome Web Store sont distribuées séparément après examen ; consultez la version affichée dans la boutique.

## Contourner une SWG ou exclure une connexion de l’inspection TLS ?

Le contournement d’une SWG change le trajet réseau de la connexion. Une exception d’inspection TLS peut laisser le trafic traverser la passerelle sans déchiffrement. Une chaîne de certificats publics ne suffit donc pas à prouver un changement de trajet.

Consultez la [comparaison entre contournement et exception TLS](https://swgbar.com/fr/guides/swg-bypass-vs-tls-exception/) et le [guide de détection de l’inspection HTTPS](https://swgbar.com/fr/guides/detect-https-inspection/).

Vérifié le 4 novembre 2026 : le paquet officiel 2.4.12 (build 42) correspond au SHA-256 publié et passe les contrôles de signature et de notarisation d’Apple. L’application et l’extension réseau native installées correspondent au paquet ; l’extension Chrome fournie reste en 2.1.13. Les tests réels d’activation, de désactivation, de fermeture et de redémarrage sont documentés ci-dessous.

[Tutoriel étape par étape](https://swgbar.com/fr/guides/how-to-bypass-swg/) · [Test complet et limites](https://swgbar.com/fr/guides/certificate-check-case-study/)

## Mesure documentée et assistance

[Test complet et limites](https://swgbar.com/fr/guides/certificate-check-case-study/)

Lors d’un test de six connexions à `www.doubao.com:443` avec SWG bar 2.4.12, la désactivation du contournement ou la fermeture de l’application a renvoyé une chaîne d’inspection ; son activation ou sa restauration a renvoyé une chaîne publique. Le cas documente de nouvelles vérifications TLS, le comportement au redémarrage et les limites de la vérification automatique de l’application. Ces résultats concernent les connexions testées sur ce réseau.

Ce dépôt est la présentation publique officielle du projet. Utilisez les [issues](https://github.com/nonbutAworker/swg-bar/issues) pour les questions publiques et suggestions de documentation. Pour une demande privée : [support@swgbar.com](mailto:support@swgbar.com). Ne publiez pas de clés de licence ni d’historique de navigation.

[À propos](https://swgbar.com/fr/about/) · [Confidentialité](https://swgbar.com/fr/privacy/) · [Conditions](https://swgbar.com/fr/terms/)
