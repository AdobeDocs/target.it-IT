---
keywords: Implementazione;mbox.js non JavaScript;adbox;redirector;mbox
description: Scopri come implementare Adobe [!DNL Target] in scenari non JavaScript, ad esempio l’utilizzo di un AdBox o di un redirector.
title: Come si implementa [!DNL Target] per e-mail?
feature: Implementa e-mail
role: Developer
exl-id: 3287cf3d-3ed4-471f-aa06-25bb12e23ead
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 77%

---

# E-mail: implementare Target

Informazioni sull’implementazione di Target in scenari non JavaScript, ad esempio l’utilizzo di un AdBox o di un redirector.

È possibile tenere traccia delle visite agli annunci e ad altri contenuti fuori sito. Puoi inoltre identificare lo stesso utente sul sito e all&#39;esterno di esso, per fornirgli un&#39;esperienza web coerente. Utilizzando un&#39;unica URL, l&#39;AdBox consente il test senza JavaScript, [!DNL at.js] o [!DNL mbox.js].

Un AdBox è utile per i siti che non hanno [!DNL at.js] o [!DNL mbox.js], come gli affiliati. Se la tua attività richiede una creatività dinamica (ad esempio, nell&#39;annuncio è necessario mostrare un prodotto che è stato abbandonato nel carrello), non è possibile utilizzare un AdBox.

Gli annunci AdBox e i Redirector possono essere utilizzati con qualsiasi tipo di attività. La tabella seguente mette a confronto AdBox e Redirector, e il loro utilizzo:

|  | Finalità | Caso di utilizzo | Struttura URL | Tipo di offerta | Contenuto dell&#39;offerta |
|--- |--- |--- |--- |--- |--- |
| AdBox | Restituzione di immagini diverse all&#39;annuncio | Per modificare il contenuto di un annuncio | `clientcode&#x200B;.tt.&#x200B;omtrdc&#x200B;.net/&#x200B;m2&#x200B;/&#x200B;clientcode/ubox/&#x200B;image?` | Offerta di reindirizzamento | URL per un&#39;immagine |
| Redirector | Reindirizza un visitatore a una pagina Web diversa | Per modificare la pagina di destinazione di un annuncio | `clientcode&#x200B;.tt.omtrdc.net/&#x200B;m2/clientcode&#x200B;/ubox/page?` | Offerta di reindirizzamento | URL per una pagina |

## Best practice sulla sicurezza {#security}

Tieni presente che con Redirector puoi essere esposto a un rischio di vulnerabilità di reindirizzamento aperto. Per evitare l’uso non autorizzato di collegamenti redirector da parte di terze parti, si consiglia di utilizzare &quot;host autorizzati&quot; per inserire nell&#39;elenco Consentiti i domini URL di reindirizzamento predefiniti. Target utilizza gli host per inserire nell&#39;elenco Consentiti i domini a cui desideri consentire i reindirizzamenti. Per ulteriori informazioni, consulta [Creare Inseriti nell&#39;elenco Consentiti che specificano gli host autorizzati per l’invio di chiamate mbox a Target](/help/administrating-target/hosts.md#allowlist) in *Host*.

## Vincoli {#section_38F559DCF1324271926608BCD4AB1227}

* Non vi è timeout lato client come per le mbox standard. Se Target è completamente disattivato, i visitatori dell&#39;annuncio non vedranno il contenuto, nemmeno quello predefinito.
* I cookie di terze parti vengono utilizzati per tenere traccia delle visite. Se i PCId sono diversi, per impostazione predefinita lil profilo di terza parte del visitatore viene unito a eventuali profili di prima parte esistente.
* Per utilizzare i cookie di prima parte su AdBox, dovrai portare la sessione mBox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account.
* Per utilizzare i cookie di prima parte per tenere traccia dei clic sugli annunci, passa la sessione mbox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account.
* Per utilizzare più di un AdBox nella stessa pagina, devi passare la sessione mbox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account. Potresti avere un AdBox e un link Redirector nella stessa pagina (perché il Redirector è in realtà su una seconda pagina).
