---
keywords: scene7;dynamic media classic;gestione risorse digitali;digital asset management;risorse;assets;dam;libreria contenuti;cambiare immagine
description: Connetti Adobe Target a Adobe Dynamic Media Classic (Scene7) per consentire agli autori di utilizzare le offerte di immagini e scambiare immagini dalle risorse Experience Cloud nelle attività.
landing-page-description: Configura la configurazione Scene7 in Amministrazione per abilitare le offerte di immagini, i flussi di lavoro DAM della libreria dei contenuti e le azioni di scambio delle immagini nel Compositore esperienza visivo e nel Compositore esperienza basato su moduli.
short-description: Configura la configurazione Scene7 in Amministrazione per abilitare le offerte di immagini, i flussi di lavoro DAM della libreria dei contenuti e le azioni di scambio delle immagini nel Compositore esperienza visivo e nel Compositore esperienza basato su moduli.
title: Come si configura l’integrazione Dynamic Media Classic (Scene7)?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
TQID: 'https://experienceleague.adobe.com/LKbjwlGIxrgaU-2i6Ddn1wi-VjsSmpQPAxYkFHRNOYQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: da3860b0-d637-47df-bef0-273751180266
    internal-label: Digital asset management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 553aa8fb523a62f72f0e2be7d7fd1b4eb663da6b
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 5%
---
# Configurare Dynamic Media Classic (Scene7)

Utilizzare la scheda **[!UICONTROL Configurazione Scene7]** in **[!UICONTROL Amministrazione]** per connettere [!DNL Adobe Target] a [!DNL Adobe Dynamic Media Classic] (in precedenza [!DNL Scene7]). L&#39;integrazione porta Digital Asset Management (DAM) nella [!UICONTROL Libreria contenuti] e abilita i flussi di lavoro di scambio immagini nelle attività.

Per informazioni su come questa scheda si adatta ad altre attività di amministrazione, vedere [Come posso amministrare Target?](/help/main/administrating-target/administrating-target.md). Per individuare **[!UICONTROL Amministrazione]** nell&#39;interfaccia, vedere [Comprendere l&#39;interfaccia utente [!DNL Target] 4}.](/help/main/c-intro/understand-the-target-ui.md)

**Panoramica**

1. [Funzionalità dell&#39;integrazione](#what-it-enables): offerte di immagini, scambio di immagini e risorse idonee.
1. [Account e credenziali](#account-and-credentials): account [!DNL Dynamic Media] esistenti e tipi di account supportati.
1. [Linee guida per l&#39;utilizzo](#usage-guidelines): URL, consegna e ciò che non è supportato.
1. [Configura Scene7 in Target](#configure-scene7): impostazioni di accesso e area geografica.

{{permissions-update}}

## Funzionalità dell&#39;integrazione {#what-it-enables}

Quando è configurata la configurazione **[!UICONTROL Scene7]**, gli autori possono utilizzare le immagini caricate nella cartella delle risorse [!DNL Adobe Experience Cloud] nelle attività [!DNL Target]. L&#39;opzione **[!UICONTROL Scambia offerta immagine]** viene visualizzata nel flusso di lavoro dell&#39;attività, incluso nel [Compositore esperienza visivo e Compositore esperienza basato su moduli](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Per informazioni sul comportamento di scambio nel Compositore esperienza visivo, consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

Se questa impostazione non è configurata, **[!UICONTROL L&#39;offerta di scambio immagine]** non è disponibile durante la creazione dell&#39;attività.

L’integrazione distribuisce le risorse che fanno parte delle attività dalla cartella risorse di Experience Cloud. **not** espone ogni risorsa in [!DNL Dynamic Media Classic] per l&#39;utilizzo in [!DNL Target] attività.

Dopo la configurazione, gestisci le offerte di immagini nella libreria [!UICONTROL Offerte]. Vedi [Gestione contenuto](/help/main/c-experiences/c-manage-content/manage-content.md).

## Account e credenziali {#account-and-credentials}

Se disponi già di un account [!DNL Dynamic Media], immetti tali credenziali nella pagina **[!UICONTROL Configurazione Scene7]**.

Adobe non esegue più il provisioning degli account [!DNL Dynamic Media Classic] con utilizzo limitato e senza addebiti per i nuovi clienti [!DNL Target] o i nuovi utenti. Se la tua organizzazione dispone già delle credenziali di accesso per questa integrazione, continuerà a funzionare. Per domande sull&#39;account, contattare il rappresentante [!DNL Adobe].

## Linee guida sull’utilizzo {#usage-guidelines}

Quando utilizzi le immagini con questa integrazione, tieni presenti i seguenti vincoli:

* **Offerte immagine, non URL di archiviazione.** [!DNL Dynamic Media] gli URL di archiviazione e gli URL di consegna pubblicati sono diversi. Non creare offerte dai collegamenti di archiviazione; la consegna non riesce. Utilizza invece [offerte immagine](/help/main/c-experiences/c-manage-content/manage-content.md) e flussi di lavoro di scambio immagini.
* **URL pubblici nel codice personalizzato.** Per fare riferimento a un URL di immagine pubblica direttamente in un’offerta o in un codice personalizzato, ospita l’immagine sui tuoi server web e utilizza tale URL. Impossibile ottenere un URL pubblicato per un&#39;immagine caricata da Experience Cloud da utilizzare al di fuori dei flussi di lavoro di targeting [!DNL Target]. L&#39;utilizzo non è consentito dal contratto.
* **Risorse idonee.** Solo le risorse caricate nella cartella delle risorse di Experience Cloud (e i flussi di lavoro supportati da questa integrazione) sono nell&#39;ambito, non l&#39;intero catalogo [!DNL Dynamic Media Classic].

## Configurare Scene7 in Target {#configure-scene7}

Utilizzare i passaggi seguenti per connettere [!DNL Dynamic Media Classic] ([!DNL Scene7]):

1. Fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazione Scene7]**.
1. Immettere le informazioni sull&#39;account [!DNL Dynamic Media Classic]:

   | Campo | Descrizione |
   | --- | --- |
   | **Area** | Area geografica del tuo account [!DNL Dynamic Media]: Nord America, Europa o Asia. |
   | **Cartella ad hoc** | Percorso del contenuto esterno alla cartella di destinazione caricato manualmente in [!DNL Dynamic Media]. |
   | **Indirizzo e-mail** | Indirizzo e-mail utilizzato per accedere a [!DNL Dynamic Media Classic] ([!DNL Scene7]). |
   | **Password** | Password utilizzata per accedere a [!DNL Dynamic Media Classic] ([!DNL Scene7]). |

   ![Campi di configurazione Scene7](/help/main/administrating-target/assets/scene7-1.png)

1. Fate clic su **[!UICONTROL Submit]** (Invia).
