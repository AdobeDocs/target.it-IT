---
keywords: Implementazione;mbox;mbox.js;scaricare mbox. js;configurare mbox.js
description: Scopri l’implementazione legacy di mbox.js di Adobe Target. Esegui la migrazione a Adobe Experience Platform Web SDK (AEP Web SDK) o all’ultima versione di at.js.
title: Come si scarica la libreria [!DNL Target] mbox.js?
feature: at.js
role: Developer
exl-id: 92096b1b-a8a5-435b-8e62-24b5d15d392f
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 74%

---

# Scaricare mbox.js

Target Standard e Premium utilizzano una versione modificata del file mbox.js di Adobe Target.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

Per utilizzare l&#39;[!DNL Adobe Target]Editor di esperienza visiva[!UICONTROL  di ], è necessario includere una riga aggiuntiva di JavaScript all&#39;interno del file [!DNL mbox.js].

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** in [!DNL Target Standard].
1. Fai clic su **[!UICONTROL Scarica mbox.js]** e segui le istruzioni per salvare il file.
1. (Opzione d&#39;uso) Se si utilizza la versione 60 o successiva di [!DNL mbox.js], è possibile configurare la libreria per nascondere automaticamente il contenuto della pagina per impostazione predefinita durante il caricamento degli elementi mbox per ridurre la visualizzazione momentanea di altro contenuto sui siti reattivi.

1. Crea il riferimento a [!DNL mbox.js] sul sito web.

   A partire dalla versione 57 di [!DNL mbox.js], il riferimento [!DNL mbox.js] può essere posizionato ovunque all’interno della sezione `<head>` della pagina.

   >[!IMPORTANT]
   >
   >Se utilizzi una versione di [!DNL mbox.js] precedente alla versione 57, il riferimento deve essere l’ultimo elemento della sezione `<head>` delle tue pagine. Se il riferimento non è l&#39;ultimo elemento, possono verificarsi gravi problemi di visualizzazione o di prestazioni.

1. Carica il file [!DNL mbox.js] salvato nella posizione all&#39;interno dell&#39;ambiente di hosting specificata nel codice.
