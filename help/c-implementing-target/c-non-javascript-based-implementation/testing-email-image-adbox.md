---
description: Esegui un test dinamico delle immagini in un’e-mail, e cambiale al volo quando qualcuno apre l’e-mail.
keywords: email;adbox
seo-description: Esegui un test dinamico delle immagini in un’e-mail, e cambiale al volo quando qualcuno apre l’e-mail.
seo-title: Test AdBox di un'immagine per e-mail
solution: Target
title: Test AdBox di un'immagine per e-mail
topic: Consigli
uuid: d0710adb-4649-4b57-9b70-4b49d43fa591
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Test AdBox di un'immagine per e-mail{#test-an-email-image-adbox}

Esegui un test dinamico delle immagini in un’e-mail, e cambiale al volo quando qualcuno apre l’e-mail.

I redirector possono essere utilizzati nelle e-mail per monitorare i clic e controllare dinamicamente quale pagina di destinazione viene raggiunta dagli utenti.

Il test dell'immagine di una e-mail si ottiene attraverso l'utilizzo di versioni modificate di AdBox. Poiché i client di posta elettronica non consentono l'impostazione dei cookie, per ogni messaggio di posta elettronica deve essere generato un identificatore univoco. Questo numero viene aggiunto all'URL dell'AdBox e a qualsiasi redirector utilizzato nell'email per tenere traccia dei clic dall'e-mail.

>[!NOTE]
>
>Sebbene Target possa distribuire tecnicamente l’ottimizzazione dell’immagine in fase di apertura, ogni client e-mail gestisce la memorizzazione nella cache in modo diverso, quindi il risultato potrà variare. Indipendentemente dal provider del servizio e-mail utilizzato, il client e-mail utilizzato dall'utente finale per aprire l'e-mail (app Gmail, Outlook, Hotmail e così via) determina se l'immagine è effettivamente racchiusa in fase di apertura. Ad esempio, Gmail memorizza nella cache la maggior parte degli elementi, quindi l'immagine che l'utente finale visualizza è legata al momento in cui Gmail sceglie di richiamarla e memorizzarla nella cache dell'immagine.

**Codice di esempio per un'AdBox dell'immagine di un'e-mail:**

```
<img src=“https://{clientcode}.tt.omtrdc.net/m2/​{clientcode}/ubox/​image?
mbox={email_header}&
mboxDefault=​{http%3A%2F%2Fwww.domain.com%2Fheader.jpg}&
mboxXDomain=disabled&
mboxSession={123456}&
mboxPC={123456}” border=“0"/>
```

I valori qui di seguito sono specifici per il tuo caso:

| Valore | Descrizione |
|--- |--- |
| clientcode | Il codice cliente della tua azienda. Si trova in at.js o in mbox.js elencato come `clientCode='yourclientcode'`. Tutto minuscolo e senza caratteri speciali. |
| image | Tipo di offerta. È sempre “image” per gli annunci grafici e “page” per i redirector. |
| email_header | Il nome della AdBox. |
| `mboxDefault=http%3A%2F%2Fwww.domain.com%2Fheader.jpg` | Obbligatorio. Sostituisci l’URL con il contenuto predefinito appropriato per la AdBox. Deve essere un riferimento assoluto e deve essere codificato nell’URL. |
| `mboxXDomain=disabled` | Indica a Target di non tentare di impostare un cookie. |
| `mboxSession=123456` e `mboxPC=123456` | Due valori richiesti da Target per unire il profilo di questo utente con il profilo esistente per il sito. 123456 è l'identificatore univoco generato per e-mail. Inserire in modo dinamico questo valore in ogni URL AdBox e redirector. Questo numero deve essere univoco per ogni e-mail inviata a ciascuna persona. Se un'e-mail settimanale viene inviata a 1000 persone, è necessario generare 1000 ID univoche.<br>L'identificatore univoco per ogni e-mail deve essere assegnato a mboxSession e mboxPC in ciascun URL della AdBox e del redirector. Il formato consigliato per l’identificatore è timestamp-NNNNN, dove NNNNN è un numero casuale di 5 cifre, ma funziona qualsiasi formato alfanumerico. Alcuni servizi e-mail di massa e qualsiasi linguaggio di programmazione sono in grado di generare questo identificatore univoco. |
