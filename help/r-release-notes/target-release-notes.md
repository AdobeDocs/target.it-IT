---
description: Queste note sulla versione contengono informazioni su funzioni, miglioramenti, correzioni di problemi e problemi noti per le versioni più recenti o in arrivo di Target.
keywords: note sulla versione
seo-description: Queste note sulla versione contengono informazioni su funzioni, miglioramenti, correzioni di problemi e problemi noti per le versioni più recenti o in arrivo di Adobe Target
seo-title: Note sulla versione di Target (pre-rilascio)
solution: Target
title: Note sulla versione di Target (pre-rilascio)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: fe022b641580e33afdac446f71cec85fd232b275

---


# Note sulla versione di Target (pre-rilascio){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 28 maggio 2019**

>[!NOTE]
>
>Queste sulla versione contengono delle informazioni in anteprima. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti. Per visualizzare le informazioni sulla versione corrente, vedi [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.

## at. js versione 2.1.0 (3 giugno 2019)

Siamo entusiasti di annunciare le seguenti funzionalità entusiasmanti in at. js 2.1.0:

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Assistenza Adobe Consenso | Adobe Opt-in è un metodo per semplificare le integrazioni delle soluzioni Adobe con le piattaforme di gestione del consenso.<br>Per ulteriori informazioni su Adobe Opt-in, consulta [Privacy e Regolamento generale sulla protezione dei dati (RGPD)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md). |
| Conformità standard di settore CSP | at. js no uses eval () to execute javascript. |
| Registrazione analisi lato client | Offre ai clienti il controllo completo su come desiderano inviare dati analitici ad Adobe Analytics, sia sul lato client che sul lato server. |
| Inviare notifiche | Consente agli sviluppatori di inviare notifiche quando un&#39;esperienza viene sottoposta a rendering dal codice anziché utilizzare `applyOffer()` o `applyOffers()`. |
| Dimensioni file ridotte | La dimensione di at. js viene ridotta di ~ 24%. Le dimensioni del file più piccole migliorano le prestazioni di caricamento delle pagine e riducono il tempo di download su. js sulla pagina. |

## [!DNL Target] Standard/Premium 19.5.1 (21 maggio 2019) {#release-19-5-1-prerelease}

Questa versione include le seguenti funzionalità, modifiche e miglioramenti:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

### Aggiornamenti delle funzioni

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo per app a pagina singola (SPA di SPA) | Il Compositore di esperienze visive SPA include i seguenti miglioramenti per permetterti di lavorare in modo più rapido ed efficiente:<ul><li>Facendo clic su un&#39;azione in SPA viene evidenziata l&#39;elemento sul sito in cui verrà applicata l&#39;azione. Ogni azione VEC creata in una vista presenta quattro icone corrispondenti: Informazioni, Modifica, Sposta ed Elimina. La nuova funzionalità Sposta di questa versione consente di spostare l&#39;azione in un evento di caricamento pagina o in qualsiasi altra visualizzazione già esistente nel pannello delle modifiche. (TGT-33746)</li><li>Potrai eseguire molte azioni prima che la pagina si carichi nel VEC, anche nel caso in cui la pagina non riesca a caricarsi completamente (per esempio, il codice personalizzato non è più operativo). Nell’interfaccia utente di Target, le azioni che possono essere modificate solo dopo il caricamento del sito risultano disabilitate. (TGT-33851 e TGT-34149)</li></ul>Per ulteriori informazioni, consulta [Compositore esperienza visivo per app a pagina singola](/help/c-experiences/spa-visual-experience-composer.md). |

### Miglioramenti, correzioni e modifiche

* Le icone della barra degli strumenti vengono visualizzate correttamente dopo aver annullato il caricamento di una pagina nel Compositore esperienza visivo. Se non è possibile eseguire azioni specifiche finché non è stato completato il caricamento della pagina, le icone della barra degli strumenti associate sono disattivate. (TGT-33811)

## Mobile App Visual Experience Composer (14 maggio 2019) {mobile-vec-may 14}

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Mobile App Visual Experience Composer (VEC) | La VEC App mobile consente di creare attività e personalizzare il contenuto su app native per dispositivi mobili in modo autonomo senza continuità di sviluppo e cicli di rilascio delle app.<br>Per ulteriori informazioni, consulta:<ul><li>[Compositore esperienza visivo per app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android: configurare l&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS: configurare l&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Configurare il tracciamento dei clic nel Compositore esperienza visivo mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li><li>[Video: Mobile App Visual Experience Composer (Compositore esperienza visivo)](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#video)</li></ul> |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche anticipate sui miglioramenti dei prodotti in arrivo a Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
