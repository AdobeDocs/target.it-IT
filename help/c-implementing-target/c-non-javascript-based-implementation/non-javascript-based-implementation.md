---
keywords: Implementation;mbox.js non javascript;adbox;redirector;mbox
description: Informazioni sull’implementazione di Target in scenari non JavaScript, ad esempio l’utilizzo di un AdBox o di un redirector.
title: 'E-mail: implementare Target'
feature: email implementation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 82%

---


# E-mail: implementare Target{#email-implement-target}

Informazioni sull’implementazione di Target in scenari non JavaScript, ad esempio l’utilizzo di un AdBox o di un redirector.

È possibile tenere traccia delle visite agli annunci e ad altri contenuti fuori sito. Puoi inoltre identificare lo stesso utente sul sito e all&#39;esterno di esso, per fornirgli un&#39;esperienza web coerente. Utilizzando un&#39;unica URL, l&#39;AdBox consente il test senza JavaScript, [!DNL at.js] o [!DNL mbox.js].

Un AdBox è utile per i siti che non hanno [!DNL at.js] o [!DNL mbox.js], come gli affiliati. Se la tua attività richiede una creatività dinamica (ad esempio, nell&#39;annuncio è necessario mostrare un prodotto che è stato abbandonato nel carrello), non è possibile utilizzare un AdBox.

Gli annunci AdBox e i Redirector possono essere utilizzati con qualsiasi tipo di attività. La tabella seguente mette a confronto AdBox e Redirector, e il loro utilizzo:

|  | Finalità | Caso di utilizzo | Struttura URL | Tipo di offerta | Contenuto dell&#39;offerta |
|--- |--- |--- |--- |--- |--- |
| AdBox | Restituzione di immagini diverse all&#39;annuncio | Per modificare il contenuto di un annuncio | `clientcode&#x200B;.tt.&#x200B;omtrdc&#x200B;.net/&#x200B;m2&#x200B;/&#x200B;clientcode/ubox/&#x200B;image?` | Offerta di reindirizzamento | URL per un&#39;immagine |
| Redirector | Reindirizza un visitatore a una pagina Web diversa | Per modificare la pagina di destinazione di un annuncio | `clientcode&#x200B;.tt.omtrdc.net/&#x200B;m2/clientcode&#x200B;/ubox/page?` | Offerta di reindirizzamento | URL per una pagina |

## Best practice di protezione {#security}

Si noti che con Redirector, è possibile essere esposti al rischio di una vulnerabilità di reindirizzamento aperto. Per evitare l&#39;uso non autorizzato di collegamenti Redirector da parte di terzi, si consiglia di utilizzare &quot;host autorizzati&quot; per  inserire nell&#39;elenco Consentiti i domini URL di reindirizzamento predefiniti. In Target gli host vengono utilizzati per  i domini inserire nell&#39;elenco Consentiti cui si desidera consentire i reindirizzamenti. Per ulteriori informazioni, consultate [Creare Inserire nell&#39;elenco Consentiti di  che specificano gli host autorizzati a inviare chiamate mbox a Target](/help/administrating-target/hosts.md#allowlist) in *ospitanti*.

## Vincoli {#section_38F559DCF1324271926608BCD4AB1227}

* Non vi è timeout lato client come per le mbox standard. Se Target è completamente disattivato, i visitatori dell&#39;annuncio non vedranno il contenuto, nemmeno quello predefinito.
* I cookie di terze parti vengono utilizzati per tenere traccia delle visite. Se i PCId sono diversi, per impostazione predefinita lil profilo di terza parte del visitatore viene unito a eventuali profili di prima parte esistente.
* Per utilizzare i cookie di prima parte su AdBox, dovrai portare la sessione mBox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account.
* Per utilizzare i cookie di prima parte per tenere traccia dei clic sugli annunci, passa la sessione mbox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account.
* Per utilizzare più di un AdBox nella stessa pagina, devi passare la sessione mbox nell&#39;URL. A tale scopo, rivolgiti al rappresentante del tuo account. Potresti avere un AdBox e un link Redirector nella stessa pagina (perché il Redirector è in realtà su una seconda pagina).