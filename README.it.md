# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · **Italiano** · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [Bahasa Indonesia](README.id.md)

**Rileva l’ispezione HTTPS. Aggira lo SWG con un clic.**

[Sito ufficiale](https://swgbar.com/it/) · [Scarica per Mac](https://swgbar.com/it/#pricing) · [Guide](https://swgbar.com/it/guides/) · [CLI](https://swgbar.com/it/cli/) · [MCP](https://swgbar.com/it/mcp/)

SWG bar è un’app nativa per la barra dei menu di macOS progettata per rilevare l’**ispezione HTTPS/SSL (break-and-inspect)** effettuata dai Secure Web Gateway (SWG) aziendali — come Zscaler, Netskope e Cloudflare Gateway — e gestire il **bypass SWG per singolo dominio con un clic**. Esamina i risultati dei domini e le prove dei certificati sul Mac, consulta i risultati locali registrati tramite l’estensione per Chrome oppure automatizza verifiche e regole dal Terminale e dagli agenti di sviluppo IA.

## Funzionalità

- **Ispezione HTTPS/SSL e prove dei certificati:** identifica i domini ispezionati, esamina emittenti, date di validità, impronte SHA-256 e nomi host associati, e confronta l’attendibilità del portachiavi macOS (incluse le CA radice distribuite tramite MDM) con una verifica indipendente delle radici pubbliche.
- **Bypass SWG per dominio con un clic:** instrada i nomi host selezionati su macOS senza decifratura HTTPS sul gateway sulle reti autorizzate, dalla barra dei menu, dalla CLI o tramite MCP.
- **Estensione Chrome (`2.1.13`):** visualizza direttamente nella barra degli strumenti del browser il risultato locale già registrato dall’app Mac per il dominio corrente.
- **CLI nativa `swgbar` e server MCP:** interroga i dati di ispezione, avvia sonde TLS su richiesta e gestisci il bypass per dominio dal Terminale ([guida CLI](https://swgbar.com/it/cli/)) o da client IA compatibili con MCP come Claude Desktop, Cursor, Windsurf e Claude Code ([guida MCP](https://swgbar.com/it/mcp/)).

I dati di rilevamento vengono analizzati e archiviati localmente sul Mac. Le sonde aprono connessioni TLS IPv4 separate; l’estensione Chrome opera in sola lettura tramite Chrome Native Messaging e legge i risultati locali esistenti. Consulta [come funziona](https://swgbar.com/it/how-it-works/), l’[informativa sulla privacy](https://swgbar.com/it/privacy/) e la [privacy dell’estensione](https://swgbar.com/it/extension-privacy/).

## Per iniziare

Richiede **macOS 14 o successivo e Apple silicon** (`arm64`). La prova gratuita comprende **14 giorni di utilizzo effettivo** senza carta di credito; i piani individuali e per team aggiornati sono disponibili sul [sito ufficiale](https://swgbar.com/it/#pricing).

1. Scarica il pacchetto di installazione `.pkg` firmato e autenticato (`2.4.12`, build `42`) dal [sito ufficiale](https://swgbar.com/it/#pricing) e segui la [guida all’installazione](https://swgbar.com/it/install/).
2. Apri SWG bar dalla barra dei menu per esaminare nomi host, CA radice e controlli di bypass per dominio.
3. Se lo desideri, collega l’[estensione per Chrome](https://swgbar.com/it/chrome-extension/), configura la [CLI `swgbar`](https://swgbar.com/it/cli/) o registra il [server MCP](https://swgbar.com/it/mcp/) nel tuo client IA.

L’app per Mac `2.4.12` e l’estensione Chrome `2.1.13` inclusa supportano tutte le 12 lingue del sito. Gli aggiornamenti del Chrome Web Store vengono pubblicati separatamente dopo la revisione; verifica la versione indicata nello store.

## Guide: ispezione HTTPS, bypass SWG ed errori dei certificati in CLI e IA

Quando analizzi le connessioni su macOS, distingui l’**instradamento di rete** dalla **decifratura TLS**. Il bypass di uno SWG instrada il nome host fuori dalla decifratura del gateway; un’eccezione all’ispezione TLS può invece lasciare il traffico sulla stessa passerella senza decifrarlo, quindi una catena di certificati pubblici da sola non dimostra un cambio di percorso.

- [Come rilevare l’ispezione HTTPS e SSL su Mac](https://swgbar.com/it/guides/detect-https-inspection/) — verificare catene di certificati e CA radice locali su macOS.
- [Ispezione HTTPS di SWG aziendali e MDM su Mac](https://swgbar.com/it/guides/enterprise-swg-https-inspection-macos/) — perché Zscaler, Netskope e Cloudflare Gateway mantengono intatto il lucchetto del browser tramite CA radice MDM.
- [Come aggirare una SWG su Mac](https://swgbar.com/it/guides/how-to-bypass-swg/) — configurazione passo per passo per dominio, approvazione dell’estensione di rete macOS, comportamento al riavvio e limiti di rete.
- [Bypass SWG vs eccezione all’ispezione TLS (break-and-inspect)](https://swgbar.com/it/guides/swg-bypass-vs-tls-exception/) — differenze tra instradamento per dominio ed eccezioni di decifratura sul gateway.
- [Risolvere gli errori dei certificati TLS e SSL di SWG negli strumenti CLI e IA su Mac](https://swgbar.com/it/guides/swg-tls-certificate-errors-macos/) — risolvere `CERTIFICATE_VERIFY_FAILED` e gli errori di emittente locale in `git`, `npm`, `Python`, `Claude Code` e `Cursor`.

**Stato della versione, verificato il 18 novembre 2026:** la versione pubblicata è **SWG bar 2.4.12** (build `42`), comprensiva dell’estensione di rete nativa firmata per il bypass per dominio, della CLI `swgbar` con server MCP e dell’estensione Chrome `2.1.13`. Checksum SHA-256, firma Apple e notarizzazione del pacchetto sono stati verificati. Consulta le [informazioni sulle versioni](https://swgbar.com/it/releases/) e le [guide ufficiali](https://swgbar.com/it/guides/).

## Domande e feedback

Questo è il repository ufficiale di presentazione pubblica del progetto. Usa gli [issue](https://github.com/nonbutAworker/swg-bar/issues) per domande pubbliche e suggerimenti sulla documentazione. Per installazione, ordini o richieste private: [support@swgbar.com](mailto:support@swgbar.com). Non pubblicare chiavi di licenza o cronologia di navigazione.

[Informazioni su SWG bar](https://swgbar.com/it/about/) · [Privacy](https://swgbar.com/it/privacy/) · [Privacy dell’estensione](https://swgbar.com/it/extension-privacy/) · [Termini](https://swgbar.com/it/terms/)
