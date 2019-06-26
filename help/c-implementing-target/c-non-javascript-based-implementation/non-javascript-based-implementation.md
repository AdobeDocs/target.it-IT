---
description: Informazioni sull’implementazione di Target in scenari non JavaScript, ad esempio l’utilizzo di un AdBox o di un redirector.
keywords: Implementazione;mbox.js non JavaScript;adbox;redirector;mbox
seo-description: Informazioni sull’implementazione di Target in scenari non JavaScript, ad esempio l’utilizzo di un AdBox o di un redirector.
seo-title: 'E-mail: implementare Target'
solution: Target
subtopic: Introduzione
title: 'E-mail: implementare Target'
topic: Standard
uuid: 07abc419-0253-47c6-80b8-0bd0734d2c9d
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# E-mail: implementare Target{#email-implement-target}

Informazioni sull’implementazione di Target in scenari non JavaScript, ad esempio l’utilizzo di un AdBox o di un redirector.

È possibile tenere traccia delle visite agli annunci e ad altri contenuti fuori sito. Puoi inoltre identificare lo stesso utente sul sito e all&#39;esterno di esso, per fornirgli un&#39;esperienza web coerente. Utilizzando un&#39;unica URL, l&#39;AdBox consente il test senza JavaScript, [!DNL at.js] o [!DNL mbox.js].

Un AdBox è utile per i siti che non hanno [!DNL at.js] o [!DNL mbox.js], come gli affiliati. Se la tua attività richiede una creatività dinamica (ad esempio, nell&#39;annuncio è necessario mostrare un prodotto che è stato abbandonato nel carrello), non è possibile utilizzare un AdBox.

Gli annunci AdBox e i Redirector possono essere utilizzati con qualsiasi tipo di attività. La tabella seguente mette a confronto AdBox e Redirector, e il loro utilizzo:

|  | Finalità | Caso di utilizzo | Struttura URL | Tipo di offerta | Contenuto dell&#39;offerta |
|--- |--- |--- |--- |--- |--- |
| AdBox | Restituzione di immagini diverse all&#39;annuncio | Per modificare il contenuto di un annuncio | `clientcode​.tt.​omtrdc​.net/​m2​/​clientcode/ubox/​image?` | Offerta di reindirizzamento | URL per un&#39;immagine |
| Redirector | Reindirizza un visitatore a una pagina Web diversa | Per modificare la pagina di destinazione di un annuncio | `clientcode​.tt.omtrdc.net/​m2/clientcode​/ubox/page?` | Offerta di reindirizzamento | URL per una pagina |

## Vincoli {#section_38F559DCF1324271926608BCD4AB1227}

* Non vi è timeout lato client come per le mbox standard. Se Target è completamente disattivato, i visitatori dell&#39;annuncio non vedranno il contenuto, nemmeno quello predefinito.
* I cookie di terze parti vengono utilizzati per tenere traccia delle visite. Se i PCId sono diversi, per impostazione predefinita lil profilo di terza parte del visitatore viene unito a eventuali profili di prima parte esistente.
* Per utilizzare i cookie di prima parte su AdBox, dovrai portare la sessione mBox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account.
* Per utilizzare i cookie di prima parte per tenere traccia dei clic sugli annunci, passa la sessione mbox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account.
* Per utilizzare più di un AdBox nella stessa pagina, devi passare la sessione mbox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account. Potresti avere un AdBox e un link Redirector nella stessa pagina (perché il Redirector è in realtà su una seconda pagina).

