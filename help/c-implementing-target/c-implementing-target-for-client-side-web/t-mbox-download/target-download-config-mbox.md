---
keywords: Implementation;Mbox;mbox.js;download mbox.js;configure mbox.js
description: Target Standard e Premium utilizzano una versione modificata del file mbox.js di Adobe Target.
title: Scaricare mbox.js
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 94%

---


# Scaricare mbox.js{#download-mbox-js}

Target Standard e Premium utilizzano una versione modificata del file mbox.js di Adobe Target.

Per utilizzare l&#39;[!DNL Adobe Target]Editor di esperienza visiva[!UICONTROL  di ], è necessario includere una riga aggiuntiva di JavaScript all&#39;interno del file [!DNL mbox.js].

1. Fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** in [!DNL Target Standard].
1. Fai clic su **[!UICONTROL Scarica mbox.js]** e segui le istruzioni per salvare il file.
1. (Opzione d&#39;uso) Se si utilizza la versione 60 o successiva di [!DNL mbox.js], è possibile configurare la libreria per nascondere automaticamente il contenuto della pagina per impostazione predefinita durante il caricamento degli elementi mbox per ridurre la visualizzazione momentanea di altro contenuto sui siti reattivi.

   Per ulteriori informazioni, consulta “Eliminare visualizzazione momentanea di altri contenuti al caricamento della pagina” in [Impostazioni avanzate di mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/advanced-mboxjs-settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C).

1. Crea il riferimento a [!DNL mbox.js] sul sito web.

   A partire dalla versione 57 di [!DNL mbox.js], il riferimento [!DNL mbox.js] può essere posizionato ovunque all’interno della sezione `<head>` della pagina.

   >[!IMPORTANT]
   >
   >Se utilizzi una versione di [!DNL mbox.js] precedente alla versione 57, il riferimento deve essere l’ultimo elemento della sezione `<head>` delle tue pagine. Se il riferimento non è l&#39;ultimo elemento, possono verificarsi gravi problemi di visualizzazione o di prestazioni. Per ulteriori informazioni, consultate [What mbox.js does](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-technical.md).

1. Carica il file [!DNL mbox.js] salvato nella posizione all&#39;interno dell&#39;ambiente di hosting specificata nel codice.
