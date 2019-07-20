---
description: Target Standard può essere integrato con Adobe Dynamic Media Classic (già Scene 7) per fornire Digital Asset Management (DAM) nella libreria Contenuto.
seo-description: Target Standard può essere integrato con Adobe Dynamic Media Classic (già Scene 7) per fornire Digital Asset Management (DAM) nella libreria Contenuto.
seo-title: Integrazione Dynamic Media Classic
solution: Target
subtopic: Introduzione
title: Integrazione Dynamic Media Classic
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: c6a59843c80017e6f072f65ffad822fe198ebb55

---


# Dynamic Media Classic integration{#scene-settings}

Target Standard può essere integrato con Adobe Dynamic Media Classic (già Scene 7) per fornire Digital Asset Management (DAM) nella libreria Contenuto.

>[!NOTE]
>
>L'integrazione di Target con Dynamic Media Classic consente di distribuire le risorse (come parte delle attività) caricate nella cartella Risorse di Adobe Experience Cloud. Questa integrazione non consente l'accesso a tutte le risorse caricate in Dynamic Media Classic per la distribuzione in attività Target.

Se disponete già di un account Dynamic Media, potete fornire le credenziali esistenti. Se non disponete di un account, potete richiedere un account Dynamic Media Classic limitato, senza alcun costo aggiuntivo dal rappresentante Adobe. Questo account può essere utilizzato per scopi limitati solo in Target. Questo servizio viene reso disponibile ai clienti per i flussi di lavoro che necessitano di funzionalità di scambio immagini.

Se questa impostazione non è configurata, l'opzione di offerta Scambio immagine all'interno del flusso di lavoro di creazione attività non è disponibile. Una volta configurata, l’opzione di offerte di scambio/cambiamento immagine è disponibile sia nel [Compositore esperienza visivo che nel Compositore esperienza basato su moduli](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Puoi quindi sfruttare le offerte di immagine con le immagini che sono state caricate da Adobe Experience Cloud e usarle in attività di Target.

Se desideri fare riferimento a un URL di immagine pubblica direttamente in un'offerta o codice personalizzato durante la creazione di attività, devi distribuire l'immagine ai server web e utilizzare il tuo URL nel codice. Non è possibile ottenere l'URL pubblicato di un'immagine caricata su Experience Cloud per utilizzarlo direttamente o all'esterno dei flussi di lavoro di targeting utilizzando Adobe Target. Questa funzionalità non è consentita, secondo il contratto.

L'URL di archiviazione e gli URL di pubblicazione finali delle immagini da Contenuti multimediali dinamici sono diversi e NON devono creare offerte con il collegamento di archiviazione delle immagini come distribuzione in tali casi. Devi usare la capacità offerte di immagini come spiegato nella nostra documentazione di aiuto.

Per poter essere integrato con Dynamic Media Classic (Scene 7), dovete specificare alcune delle seguenti informazioni.

1. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Impostazioni di Scene7]**.
1. Specificate le seguenti informazioni sull'account Dynamic Media Classic:

   **Regione:** Regione dell'account Dynamic Media: Nord America, Europa o Asia.

   **Cartella Adhoc:** Posizione per il contenuto che risiede all'esterno della cartella di destinazione e che viene caricata manualmente su Dynamic Media.

   **Indirizzo e-mail:** Indirizzo e-mail usato per accedere a Dynamic Media Classic (Scene 7).

   **Password:** Password utilizzata per accedere a Dynamic Media Classic (Scene 7).
1. Fai clic su **[!UICONTROL Invia]**.
