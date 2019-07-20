---
description: Target Standard e Premium utilizzano una versione modificata del file mbox.js di Adobe Target.
keywords: Implementazione;mbox;mbox.js;scaricare mbox. js;configurare mbox.js
seo-description: Target Standard e Premium utilizzano una versione modificata del file mbox.js di Adobe Target.
seo-title: Scaricare mbox.js
solution: Target
subtopic: Introduzione
title: Scaricare mbox.js
topic: Standard
uuid: b2a46321-cac7-4924-92dd-a80b50e27cee
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Scaricare mbox.js{#download-mbox-js}

Target Standard e Premium utilizzano una versione modificata del file mbox.js di Adobe Target.

Per utilizzare l'[!DNL Adobe Target]Editor di esperienza visiva[!UICONTROL  di ], è necessario includere una riga aggiuntiva di JavaScript all'interno del file [!DNL mbox.js].

1. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]** in [!DNL Target Standard].
1. Fai clic su **[!UICONTROL Scarica mbox.js]** e segui le istruzioni per salvare il file.
1. (Opzione d'uso) Se si utilizza la versione 60 o successiva di [!DNL mbox.js], è possibile configurare la libreria per nascondere automaticamente il contenuto della pagina per impostazione predefinita durante il caricamento degli elementi mbox per ridurre la visualizzazione momentanea di altro contenuto sui siti reattivi.

   Per ulteriori informazioni, consulta “Eliminare visualizzazione momentanea di altri contenuti al caricamento della pagina” in [Impostazioni avanzate di mbox.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/advanced-mboxjs-settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C).

1. Crea il riferimento a [!DNL mbox.js] sul sito web.

   A partire dalla versione 57 di [!DNL mbox.js], il riferimento [!DNL mbox.js] può essere posizionato ovunque all’interno della sezione `<head>` della pagina.

   >[!IMPORTANT]
   >
   >Se utilizzi una versione di [!DNL mbox.js] precedente alla versione 57, il riferimento deve essere l’ultimo elemento della sezione `<head>` delle tue pagine. Se il riferimento non è l'ultimo elemento, possono verificarsi gravi problemi di visualizzazione o di prestazioni. Per ulteriori informazioni, consulta [Dettagli tecnici sull'implementazione](https://marketing.adobe.com/resources/help/en_US/target/ov/c_mbox_technical.html).

1. Carica il file [!DNL mbox.js] salvato nella posizione all'interno dell'ambiente di hosting specificata nel codice.
