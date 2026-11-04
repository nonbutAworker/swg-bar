# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · **Italiano** · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

[Sito ufficiale](https://swgbar.com/it/) · [Scarica per Mac](https://swgbar.com/it/#pricing) · [Guide](https://swgbar.com/it/guides/)

SWG bar è un’app nativa per la barra dei menu di macOS che permette di esaminare l’ispezione HTTPS effettuata da un Secure Web Gateway (SWG). Consulta i risultati dei domini e i certificati sul Mac e visualizza i risultati locali disponibili tramite l’estensione per Chrome.

## Funzionalità

- Cerca i domini osservati e consulta i risultati delle ultime verifiche.
- Esamina emittenti, date di validità, impronte e domini associati ai certificati.
- Confronta la verifica di attendibilità di macOS con una verifica indipendente delle radici pubbliche.
- Visualizza in Chrome i risultati già presenti nell’app del Mac.

I dati di rilevamento vengono analizzati e conservati sul Mac. Le verifiche aprono connessioni TLS separate; l’estensione legge risultati locali esistenti. Consulta [come funziona](https://swgbar.com/it/how-it-works/) e l’[informativa sulla privacy](https://swgbar.com/it/privacy/).

## Per iniziare

Richiede **macOS 14 o successivo e Apple silicon**. La prova comprende **14 giorni di utilizzo effettivo**; i piani aggiornati sono sul sito.

1. Scarica il programma di installazione dal [sito ufficiale](https://swgbar.com/it/#pricing) e segui la [guida all’installazione](https://swgbar.com/it/install/).
2. Apri SWG bar dalla barra dei menu ed esamina un dominio e i suoi certificati.
3. Se lo desideri, configura l’[estensione per Chrome](https://swgbar.com/it/chrome-extension/).

L’app Mac 2.4.12 e l’estensione Chrome 2.1.13 inclusa supportano tutte le 12 lingue del sito. Gli aggiornamenti del Chrome Web Store vengono distribuiti separatamente dopo la revisione; controlla la versione indicata nello store.

## Bypass SWG ed eccezioni all’ispezione TLS

Il bypass di un SWG modifica il percorso di rete della connessione. Un’eccezione all’ispezione TLS può invece lasciare il traffico sulla stessa passerella senza decifrarlo. Una catena di certificati pubblici, da sola, non dimostra che il percorso sia cambiato.

Leggi il [confronto tra bypass SWG ed eccezione TLS](https://swgbar.com/it/guides/swg-bypass-vs-tls-exception/) e la [guida per rilevare l’ispezione HTTPS](https://swgbar.com/it/guides/detect-https-inspection/).

Verificato il 4 novembre 2026: il pacchetto ufficiale 2.4.12 (build 42) corrisponde allo SHA-256 pubblicato e supera i controlli Apple di firma e autenticazione notarile. L’app e l’estensione di rete nativa installate corrispondono al pacchetto; l’estensione Chrome inclusa resta alla versione 2.1.13. I test reali di attivazione, disattivazione, chiusura e riavvio sono documentati di seguito.

[Guida passo per passo](https://swgbar.com/it/guides/how-to-bypass-swg/) · [Test completo e limiti](https://swgbar.com/it/guides/certificate-check-case-study/)

## Misurazione documentata e assistenza

[Test completo e limiti](https://swgbar.com/it/guides/certificate-check-case-study/)

In un test di sei connessioni a `www.doubao.com:443` con SWG bar 2.4.12, con il bypass disattivato o l’app chiusa è stata restituita una catena d’ispezione; con il bypass attivato o ripristinato è stata restituita una catena pubblica. Il caso documenta nuove verifiche TLS, il comportamento al riavvio e i limiti della verifica automatica dell’app. I risultati si riferiscono alle connessioni testate su questa rete.

Questo è il repository ufficiale di presentazione pubblica del progetto. Usa gli [issue](https://github.com/nonbutAworker/swg-bar/issues) per domande pubbliche e suggerimenti sulla documentazione. Per richieste private: [support@swgbar.com](mailto:support@swgbar.com). Non pubblicare chiavi di licenza o cronologia di navigazione.

[Informazioni](https://swgbar.com/it/about/) · [Privacy](https://swgbar.com/it/privacy/) · [Termini](https://swgbar.com/it/terms/)
