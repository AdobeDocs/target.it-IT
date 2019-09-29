---
description: Target Standard può essere integrato con Adobe Dynamic Media Classic (già Scene7) per fornire Digital Asset Management (DAM) nella libreria dei contenuti.
seo-description: Target Standard può essere integrato con Adobe Dynamic Media Classic (già Scene7) per fornire Digital Asset Management (DAM) nella libreria dei contenuti.
seo-title: Integrazione Dynamic Media Classic
solution: Target
subtopic: Introduzione
title: Integrazione Dynamic Media Classic
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: c6a59843c80017e6f072f65ffad822fe198ebb55

---


# Integrazione Dynamic Media Classic{#scene-settings}

Target Standard può essere integrato con Adobe Dynamic Media Classic (già Scene7) per fornire Digital Asset Management (DAM) nella libreria dei contenuti.

>[!NOTE]
>
>L’integrazione di Target con Dynamic Media Classic consente la trasmissione delle risorse (come parte delle attività) caricate nella cartella risorse di Adobe Experience Cloud. Tale integrazione non consente l’accesso a tutte le risorse caricate in Dynamic Media Classic per la trasmissione alle attività di Target.

Se disponi già di un account Dynamic Media, puoi fornirne le tue credenziali. In caso contrario, puoi richiedere un account Dynamic Media Classic limitato, senza alcun costo aggiuntivo, rivolgendoti al tuo rappresentante Adobe. Questo account può essere utilizzato per scopi limitati solo in Target. Questo servizio viene reso disponibile ai clienti per i flussi di lavoro che necessitano di funzionalità di scambio immagini.

Se questa impostazione non è configurata, l'opzione di offerta Scambio immagine all'interno del flusso di lavoro di creazione attività non è disponibile. Una volta configurata, l’opzione di offerte di scambio/cambiamento immagine è disponibile sia nel [Compositore esperienza visivo che nel Compositore esperienza basato su moduli](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Puoi quindi sfruttare le offerte di immagine con le immagini che sono state caricate da Adobe Experience Cloud e usarle in attività di Target.

Se desideri fare riferimento a un URL di immagine pubblica direttamente in un'offerta o codice personalizzato durante la creazione di attività, devi distribuire l'immagine ai server web e utilizzare il tuo URL nel codice. Non è possibile ottenere l'URL pubblicato di un'immagine caricata su Experience Cloud per utilizzarlo direttamente o all'esterno dei flussi di lavoro di targeting utilizzando Adobe Target. Questa funzionalità non è consentita, secondo il contratto.

Tieni presente che l’URL di archiviazione e gli URL di pubblicazione finali delle immagini di Dynamic Media sono diversi; fai attenzione a NON creare offerte utilizzando il collegamento di archiviazione delle immagini, poiché in tal caso la consegna non funzionerà. Utilizza la funzionalità per offerte di immagini descritta nella documentazione.

Per l’integrazione con Dynamic Media Classic (Scene7), devi specificare alcune delle seguenti informazioni.

1. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Impostazioni di Scene7]**.
1. Specifica le seguenti informazioni relative all’account Dynamic Media Classic:

   **Regione:** l’area geografica del tuo account (Nord America, Europa o Asia).

   **Adhoc folder** (Cartella ad hoc): posizione del contenuto che si trova al di fuori della cartella di Target e viene caricato manualmente in Dynamic Media.

   **Email address (Indirizzo e-mail):** indirizzo e-mail utilizzato per accedere a Dynamic Media Classic (Scene7).

   **Password**: password utilizzata per accedere a Dynamic Media Classic (Scene7).
1. Fai clic su **[!UICONTROL Invia]**.
