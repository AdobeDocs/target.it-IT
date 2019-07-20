---
description: Informazioni su Target e standard samesite IETF utilizzati a partire da Google Chrome versione 76.
keywords: google; samesite
seo-description: Informazioni su Adobe Target e sullo standard samesite IETF introdotto con Google Chrome versione 76.
seo-title: Criteri per cookie Adobe Target e samesite
solution: Target
subtopic: Introduzione
title: Criteri cookie Google Chrome samesite
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Criteri cookie Google Chrome samesite

Google ha recentemente annunciato che a partire da Chrome 76 (slata a partire dal 30 luglio 2019), gli sviluppatori devono specificare esplicitamente quali cookie funzionano tra i siti Web e quali cookie possono tracciare gli utenti.

## Panoramica samesite

Per fornire protezione quando i cookie possono essere inviati tra siti in modo che gli utenti siano protetti, Google aggiunge il supporto per uno standard IETF chiamato "samesite" in Google Chrome 76 (e versioni successive). SameSite requires web developers to manage cookies with the SameSite attribute component in the `Set-Cookie` header.

Esistono tre valori diversi che possono essere passati nell'attributo samesite: Rigida, Lax o Nessuno.

| Valore | Descrizione |
| --- | --- |
| Rigoroso | I cookie con questa impostazione sono accessibili solo quando si visita il dominio in cui è stato inizialmente impostato. In altre parole, Narrow blocca completamente il cookie da utilizzare tra siti. Questa opzione è ideale per le applicazioni che richiedono una protezione elevata, ad esempio le banche. |
| Lax | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, such as `HTTP GET`. Therefore, this option should be used if the cookie can be used by third-parties, but with an added security benefit that protects users from being victimized by [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery) (Cross-Site Request Forgery) attacks. |
| Nessuno | I cookie con questa impostazione funzionano allo stesso modo dei cookie che funzionano oggi stesso. |

Tenendo a mente quanto sopra, Chrome 76 (e versioni successive) introduce due impostazioni: " Samesite per cookie predefiniti "e" Cookie senza samesite devono essere protetti ". Gli utenti possono abilitare entrambe le impostazioni o entrambe.

| Impostazione | Descrizione |
| --- | --- |
| Samesite per cookie predefiniti | When set, all cookies that don't specify the SameSite attribute are automatically forced with `SameSite = Lax`. |
| I cookie senza samesite devono essere protetti | When set, cookies without the SameSite attribute or with `SameSite = None`, must be Secure. Protetto in questo contesto significa che tutte le richieste del browser devono seguire il protocollo HTTPS. I cookie che non aderiscono a questo requisito vengono rifiutati. |

![Samesite, pagina delle impostazioni](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

## Target segue le best practice di sicurezza di Google

Con Target desideriamo assicurarti di avere successo, supportando sempre le best practice ottimali del settore per la sicurezza. Siamo lieti di annunciare che Target supporta le nuove impostazioni di sicurezza introdotte in Google Chrome 76.

Quando i visitatori hanno attivato l'impostazione "samesite by default cookies" (Impostazione dei cookie predefiniti), Target continua a distribuire la personalizzazione senza alcun impatto e senza alcun intervento da parte dell'utente. Target uses first-party cookies and will continue to function properly as the flag `SameSite = Lax` is applied by Google Chrome.

Quando i visitatori abilitano i "Cookie senza samesite", e non effettui l'accesso per la funzionalità di tracciamento interdominio di Target, i cookie di prime parti di Target continuano a funzionare. However, when you opt-in to using cross-domain tracking to leverage Target across multiple domains, Google Chrome 76 (and later) requires `SameSite = None` and `Secure` flags to be used for third-party cookies. È quindi necessario garantire che i siti utilizzino il protocollo HTTPS. Target's client-side libraries automatically use the HTTPS protocol and, in addition to that, attach the `SameSite = None` and `Secure` flags to Target’s third-party cookie to ensure all activities continue to deliver.

## Cosa dovete fare?

Leggi la tabella seguente per capire cosa devi fare affinché Target continui a funzionare per gli utenti di Google Chrome 76 +.

La tabella contiene le colonne seguenti:

* **Libreria lato client di Target**: Che utilizzi mbox. js, at. js 1.*x*, o at. js 2.*x* sui siti e sulle impostazioni di Google Chrome
* **Samesite by default cookies = Enabled**: Se i visitatori hanno "samesite by default cookie enabled" su Chrome 76 +, how does it impact you and there there anything to do to fare in modo che Target continui a funzionare
* **I cookie senza samesite devono essere protetti = Enabled**: Se i visitatori hanno "Cookie senza samesite" devono essere protetti su Chrome 76 +, come influisce su di esso ed è presente tutto ciò che devi fare per fare in modo che Target continui a funzionare
* **Tracciamento interdominio di Adobe Target = abilitato**: Se i visitatori hanno lo stesso sito per cookie predefiniti abilitato e «Cookie senza samesite devono essere protetti» su Chrome 76 +, e stai utilizzando Target per il monitoraggio tra più domini, come ti interessa ed è presente tutto ciò che serve per fare in modo che Target continui a funzionare

| Eseguire il targeting della libreria lato client | Samesite per cookie predefiniti = attivato | I cookie senza samesite devono essere protetti = Enabled | Tracciamento interdominio di Adobe Target = abilitato |
| --- | --- | --- | --- |
| mbox.js | Nessun impatto perché mbox. js utilizza un cookie di prime parti | Nessun impatto perché i clienti non utilizzano il tracciamento tra domini | I clienti devono abilitare il protocollo HTTPS del proprio sito.<br>In Target viene utilizzato un cookie di terze parti per tenere traccia degli utenti e Google richiede che i cookie di terze parti siano disponibili `SameSite = None` e che i siti utilizzino il protocollo HTTPS. |
| at.js 1.*x* | Nessun impatto perché at. js 1.*x* utilizza un cookie first-party | Nessun impatto perché i clienti non utilizzano il tracciamento tra domini | I clienti devono abilitare il protocollo HTTPS del proprio sito.<br>In Target viene utilizzato un cookie di terze parti per tenere traccia degli utenti e Google richiede che i cookie di terze parti dispongano `SameSite = None` e che i siti utilizzino il protocollo HTTPS |
| at.js 2.*x* | Nessun impatto perché at. js 2.*x* utilizza un cookie first-party | Nessun impatto perché i clienti non utilizzano il tracciamento tra domini | Il monitoraggio tra più domini non è supportato in at. js 2.*x* , quindi non ha alcun impatto sui clienti |

## Cosa devo fare Adobe?

| Eseguire il targeting della libreria lato client | Samesite per cookie predefiniti = attivato | I cookie senza samesite devono essere protetti = Enabled | Tracciamento interdominio di Adobe Target = abilitato |
| --- | --- | --- | --- |
| mbox.js | Nessun impatto perché mbox. js utilizza un cookie di prime parti | Nessun impatto perché i clienti non utilizzano il tracciamento tra domini | Target adds `SameSite = None` and `Secure` flag to third-party cookie when the Target backend is called. |
| at.js 1.*x* | Nessun impatto perché at. js 1.*x* utilizza un cookie first-party | Nessun impatto perché i clienti non utilizzano il tracciamento tra domini | Target adds `SameSite = None` and `Secure` flag to third-party cookie when the Target backend is called. |
| at.js 2.*x* | Nessun impatto perché at. js 2.*x* utilizza un cookie first-party | Nessun impatto perché i clienti non utilizzano il tracciamento tra domini | Il monitoraggio tra più domini non è supportato in at. js 2.*x* |

## Conclusione

Poiché il settore si occupa della creazione di un Web più sicuro per i consumatori, Target si impegna costantemente a distribuire esperienze personalizzate durante la riunione e superare le aspettative sulla privacy dei visitatori.
