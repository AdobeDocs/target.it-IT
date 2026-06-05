---
keywords: test modello;modello;stessa esperienza su pagine simili;test template
description: Scopri come utilizzare il Compositore esperienza visivo di Adobe [!DNL Target] per includere la stessa esperienza in più pagine con struttura simile o contenenti gli stessi elementi modello.
title: Posso includere la stessa esperienza in pagine simili?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
TQID: https://experienceleague.adobe.com/zk7U6g7gk7XkpWsEFQbwuCm7xbpIb1lCaZefxjn-39g
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 564
ht-degree: 22%

---

# Includere la stessa esperienza in pagine simili

Utilizzare un modello di pagina in [!DNL Adobe Target] per fornire una struttura alle pagine o, se le pagine contengono elementi simili, per testare le varianti di elementi di pagina con struttura simile o per l&#39;intero dominio.

Per funzionare correttamente, questa funzione deve essere utilizzata su pagine con una struttura simile o contenenti elementi modello strutturati allo stesso modo su tutte le pagine.

>[!IMPORTANT]
>
>L’utilizzo di questa funzione per modificare gli elementi su pagine dissimili può causare risultati imprevisti.

Ad esempio, si può utilizzare per eseguire una delle operazioni seguenti:

* Eseguire un test di una barra di navigazione globale ridisponendo o rimuovendo elementi
* Rimuovere un elemento da tutte le pagine di prodotto che utilizzano un particolare modello di pagina
* Aggiungere un banner a tutte le pagine di prodotto
* Modificare il layout del modello di articolo

Puoi specificare le pagine che includono gli elementi di modifica o applicare la modifica in tutto il sito o dominio.

1. Crea o modifica un&#39;attività come descritto in [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Per specificare le pagine in cui viene visualizzata l&#39;esperienza, nel [!UICONTROL Compositore esperienza visivo] (VEC) fai clic sull&#39;icona [!UICONTROL Configura] ( ![icona Configura](/help/main/assets/icons/Setting.svg) ), quindi seleziona **[!UICONTROL Consegna pagine]**.

1. Fai clic su **[!UICONTROL Aggiungi regola]**, quindi specifica i criteri per le pagine a cui aggiungere l&#39;esperienza.

1. Specifica l&#39;intervallo di pagine. L&#39;intervallo di pagine può essere uno tra i seguenti:

   * [!UICONTROL URL] (per ulteriori informazioni su come [!DNL Target] valuta gli URL, consulta [Domande frequenti su destinazioni e pubblico](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
   * [!UICONTROL Dominio]
   * [!UICONTROL Percorso]
   * [!UICONTROL Frammento hash (#)] (eseguire il targeting della parte di un URL che segue il simbolo #).
   * [!UICONTROL Query]
   * [!UICONTROL Personalizzato]

1. Scegli un operatore.

   L&#39;operatore specifica la correlazione tra gli elementi dopo l&#39;operatore e l&#39;intervallo di pagine. Gli operatori disponibili includono:

   * [!UICONTROL Contiene]
   * [!UICONTROL Non contiene]
   * [!UICONTROL È (distinzione maiuscole/minuscole)]
   * [!UICONTROL Non è]
   * [!UICONTROL Inizia con]
   * [!UICONTROL Termina con]

1. Digita le stringhe che definiscono dove viene aggiunta l&#39;esperienza, ad esempio il dominio o le stringhe contenute nel nome della pagina.

   Ad esempio, se selezioni **[!UICONTROL Dominio]** e **[!UICONTROL È (distinzione maiuscole/minuscole)]**, digita il dominio in cui desideri aggiungere l&#39;esperienza in tutte le pagine.

   È possibile includere più elementi.

   >[!IMPORTANT]
   >
   >Per gli elementi multipli viene utilizzato l’operatore OR, il che significa che ogni singolo elemento nell’elenco può soddisfare la condizione.

1. Se lo desideri, inserisci criteri aggiuntivi facendo clic su **[!UICONTROL Aggiungi regola]** e ripetendo la procedura di cui ai passaggi precedenti.

   I criteri multipli sono collegati mediante AND (E). [!DNL Target] aggiunge l&#39;esperienza a tutte le pagine che corrispondono ai criteri specificati.

>[!IMPORTANT]
>
> [!DNL Target] non è in grado di controllare le pagine per verificare che siano visualizzate come previsto, pertanto è sempre consigliabile utilizzare questa funzionalità per testare le pagine interessate prima di renderle pubbliche.

## Casi d’uso

Esamina i seguenti casi d’uso per scoprire come utilizzare le regole dei modelli sul sito:

### Esegui il rendering della stessa attività in tutto il dominio

Puoi considerare l’utilizzo delle regole dei modelli per eseguire il rendering della stessa attività in tutto il dominio per i seguenti casi d’uso:

* Per includere un&#39;intestazione o un piè di pagina globale
* Per includere un banner globale (ad esempio, annunci relativi alla COVID-19)
* Per includere una promozione di spedizione gratuita globale

1. Crea o modifica un&#39;attività come descritto in [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Per specificare il dominio in cui viene visualizzata l&#39;esperienza, nel [!UICONTROL Compositore esperienza visivo] fai clic sull&#39;icona [!UICONTROL Configura] ( ![icona Configura](/help/main/assets/icons/Setting.svg) ), quindi seleziona **[!UICONTROL Consegna pagine]**.

1. Fai clic su **[!UICONTROL Aggiungi regola]** > **[!UICONTROL Dominio]**.

1. Dall&#39;elenco a discesa **[!UICONTROL Scegli valutatore]**, seleziona **[!UICONTROL Contiene]**, quindi specifica il dominio.
