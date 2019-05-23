---
description: Target Standard può essere integrato con Adobe Scene7 per fornire Gestione delle risorse digitali (DAM) nella libreria dei contenuti.
seo-description: Target Standard può essere integrato con Adobe Scene7 per fornire Gestione delle risorse digitali (DAM) nella libreria dei contenuti.
seo-title: Impostazioni di Scene7
solution: Target
subtopic: Introduzione
title: Impostazioni di Scene7
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: 761771a48c0ae957d455974b1f04fa3a8350a8a0

---


# Impostazioni di Scene7{#scene-settings}

Target Standard può essere integrato con Adobe Scene7 per fornire Gestione delle risorse digitali (DAM) nella libreria dei contenuti.

>[!NOTE]
>
>L’integrazione di Target con Scene7 consente la trasmissione delle risorse (come parte delle attività) caricate nella cartella risorse di Adobe Experience Cloud. Tale integrazione non consente l&#39;accesso a tutte le risorse caricate in Scene7 per la trasmissione alle attività di Target.

Se disponi di un account Scene7, puoi fornire le credenziali Scene7. Se non hai un account Scene7, contatta il tuo rappresentante Adobe il quale può configurare questa funzionalità con un account gratuito Scene7 dedicato al tuo account di Target. Questo account può essere utilizzato per scopi limitati solo in Target. Questo servizio viene reso disponibile ai clienti per i flussi di lavoro che necessitano di funzionalità di scambio immagini.

Se questa impostazione non è configurata, l&#39;opzione di offerta Scambio immagine all&#39;interno del flusso di lavoro di creazione attività non è disponibile. Una volta configurata, l&#39;opzione di offerte di scambio/cambiamento immagine è disponibile sia nel  [Compositore esperienza visivo che nel Compositore esperienza basato su moduli](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Puoi quindi sfruttare le offerte di immagine con le immagini che sono state caricate da Adobe Experience Cloud e usarle in attività di Target.

Se desideri fare riferimento a un URL di immagine pubblica direttamente in un&#39;offerta o codice personalizzato durante la creazione di attività, devi distribuire l&#39;immagine ai server web e utilizzare il tuo URL nel codice. Non è possibile ottenere l&#39;URL pubblicato di un&#39;immagine caricata su Experience Cloud per utilizzarlo direttamente o all&#39;esterno dei flussi di lavoro di targeting utilizzando Adobe Target. Questa funzionalità non è consentita, secondo il contratto.

Ti raccomandiamo di notare che l&#39;URL di archiviazione e gli URL di pubblicazione finali di Scene7 delle immagini sono diversi e non devi creare offerte utilizzando il collegamento di archiviazione delle immagini, poiché in tali casi la consegna non funzionerà. Devi usare la capacità offerte di immagini come spiegato nella nostra documentazione di aiuto.

Per eseguire l&#39;integrazione con Scene7, devi precisare alcune informazioni specifiche di Scene7.

1. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Impostazioni di Scene7]**.
1. Specifica le informazioni seguenti sull&#39;account Scene7:

   **Regione Scene7:** la regione per il tuo account Scene7 (Nord America, Europa o Asia).

   **Cartella ad hoc Scene7:** la posizione del contenuto che si trova al di fuori della cartella di Target e viene caricato manualmente in Scene7.

   **Indirizzo e-mail Scene7:** l&#39;indirizzo e-mail utilizzato per accedere a Scene7.

   **Password Scene7:** la password utilizzata per accedere a Scene7.
1. Fai clic su **[!UICONTROL Invia]**.
