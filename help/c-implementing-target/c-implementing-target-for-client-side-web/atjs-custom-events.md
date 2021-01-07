---
keywords: custom events;at.js;request failed;request succeeded;content rendering failed;content rendering succeeded;library loaded;request start;content rendering start;content rendering no offers;content rendering rediret
description: Informazioni sugli eventi personalizzati per libreria JavaScript at.js di Adobe Target.
title: Eventi personalizzati at.js
feature: at.js
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 96%

---


# Eventi personalizzati at.js

Informazioni su `at.js custom events`, che consente di sapere quando una richiesta o un’offerta mbox ha esito negativo o positivo.

Storicamente, mbox.js non ha permesso di sapere ad altri codici JavaScript in esecuzione sulla pagina cosa succede dietro le quinte. Con l&#39;avanzamento di at.js, abbiamo avuto un&#39;occasione unica per risolvere questo problema.

I nostri clienti richiedono di essere informati in diversi scenari, tra cui:

* Una richiesta mbox non riuscita a causa di timeout, codice di stato errato, errore di analisi JSON, ecc.
* Una richiesta mbox riuscita.
* Offerta di rendering fallita a causa di elemento mbox di wrapping mancante, selettore che non può essere trovato, ecc.
* Offerta di rendering riuscita. Sono state applicate modifiche DOM.

Gli eventi predefiniti hanno una struttura che consente di estrarre i dati necessari, in base al tipo di evento.

Per assicurarti che gli eventi possano essere usati in scenari diversi, gli eventi personalizzati hanno un oggetto payload che viene assegnato alla proprietà di dettaglio dell&#39;oggetto evento (che viene passato al gestore). Anche per evitare di passare stringhe come nomi di eventi, gli eventi sono esposti come costanti usando lo spazio dei nomi `adobe.target.event`.

## Struttura {#section_0E5C9A13DE234A5DAECBCBF9F23F94FE}

| Chiave | Tipo | Descrizione |
|--- |--- |--- |
| type | Stringa | Ci sono diversi scenari per cui si desidera ricevere notifica per contribuire a monitorare, eseguire il debug e personalizzare l&#39;interazione con at.js.<br>Ogni evento personalizzato elencato di seguito contiene due formati: una “costante” e un “valore stringa”.<ul><li>**Costanti**: aggiunte a `adobe.target.event.`, includono trattini bassi e lettere solo maiuscole. Per abbonarti a eventi personalizzati *dopo* i carichi di at.js ma *prima* che la risposta mbox sia stata ricevuta, utilizza la costante.</li><li>**Valori stringa**: in minuscolo e contengono trattini. Per abbonarti a eventi personalizzati *prima* dei carichi at.js, utilizza il valore stringa.</li></ul>**Richiesta non riuscita**<br> Costante: `adobe.target.event.REQUEST_FAILED`<br>Valore stringa: `at-request-failed`<br>Descrizione: Richiesta mbox non riuscita a causa di timeout, codice di stato errato, errore di analisi JSON e così via.<br>**Richiesta riuscita**<br> Costante: `adobe.target.event.REQUEST_SUCCEEDED`<br>Valore stringa: `at-request-succeeded`<br>Descrizione: una richiesta mbox ha avuto esito positivo.<br>**Rendering contenuto fallito**<br> Costante: `adobe.target.event.CONTENT_RENDERING_FAILED`<br>Valore stringa: `at-content-rendering-failed`<br>Descrizione: rendering dell’offerta fallito a causa di elemento mbox di wrapping mancante, selettore che non può essere trovato, ecc.<br>**Rendering contenuto riuscito**<br> Costante: `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`<br>Valore stringa: `at-content-rendering-succeeded`<br>Descrizione: rendering dell’offerta eseguito correttamente. Sono state applicate modifiche DOM.<br>**Libreria caricata**<br> Costante: `adobe.target.event.LIBRARY_LOADED`<br>Valore stringa: `at-library-loaded`<br>Descrizione: questo evento è ideale per il tracciamento dopo il caricamento completo di at.js. È possibile utilizzare questo evento per personalizzare l&#39;esecuzione della mbox globale. È anche possibile utilizzare questo evento per disattivare la mbox globale e quindi ascoltare l&#39;attivazione della mbox globale da parte dell&#39;evento in un secondo momento.<br>**Inizio richiesta**<br> Costante: `adobe.target.event.REQUEST_START`<br>Valore stringa: `at-request-start`<br>Descrizione: questo evento si attiva prima dell’esecuzione di una richiesta HTTP. È possibile utilizzare questo evento per le misurazioni delle prestazioni utilizzando l&#39;API di timing delle risorse.<br>**Inizio rendering contenuto**<br> Costante: `adobe.target.event.CONTENT_RENDERING_START`<br>Valore stringa: `at-content-rendering-start`<br>Descrizione: questo si attiva prima dell’avvio del polling del selettore e dell’esecuzione del rendering del contenuto sulla pagina. È possibile utilizzare questo evento per tenere traccia dello stato di rendering del contenuto.<br>**Rendering contenuto senza offerte**<br> Costante: `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`<br>Valore stringa: `at-content-rendering-no-offers`<br>Descrizione: questo evento si attiva quando non sono presenti offerte.<br>**Contenuto rendering redirect**<br> Costante: `adobe.target.event.CONTENT_RENDERING_REDIRECT`<br>Valore stringa: `at-content-rendering-redirect`<br>Descrizione: questo evento si attiva quando un’offerta è un redirect e Target reindirizzerà a un altro URL. |
| mbox | Stringa | Nome Mbox |
| message | Stringa | Contiene una descrizione leggibile, come l&#39;accaduto, il messaggio di errore, ecc. |
| tracking | Oggetto | Contiene `sessionId` e `deviceId`. In alcuni casi, `deviceId` potrebbe mancare perché [!DNL Target] non è riuscito a recuperarlo dal server Edge. |

## Utilizzo {#section_0500FF09D3A04450B5DC8F85C6F793E0}

```javascript
document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(event) { 
  console.log('Event', event); 
});
```

## Video di formazione: Token di risposta ed eventi personalizzati at. js ![Etichetta esercitazione](/help/assets/tutorial.png) {#section_ED304A7137DC42A4BDCD6D57C989F1FA}

Guarda il video seguente e scopri come utilizzare i token di risposta e gli eventi personalizzati at.js per condividere le informazioni del profilo da Target a sistemi di terze parti.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)