---
keywords: Targeting;categorie di targeting;condizioni di targeting;Audience Manager;parametri di profilo personalizzati;profilo visitatore;parametri utente personalizzati;regole di targeting
description: Scopri come utilizzare le categorie (come Browser, Geo, Rete, Sistema operativo, Profilo visitatore) per eseguire il targeting del contenuto.
title: Quali sono le categorie di pubblico?
feature: Audiences
exl-id: 37d6435d-4139-47c5-a871-6595e089d052
TQID: https://experienceleague.adobe.com/gdwPSImsbXfvaX2Z4bL9-hGyLwo0b0q-At0fokUfYN8
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 385
ht-degree: 50%

---

# Categorie di pubblico

È possibile eseguire il targeting su uno qualsiasi degli attributi di categoria utilizzando [!DNL Adobe Target]. Per creare regole di targeting (o gruppi) per ciascun attributo, trascina e rilascia gli attributi desiderati nel riquadro Audience Builder.

![Attributi per il pubblico](/help/main/c-target/c-audiences/assets/attributes.png)

Quando viene selezionata una particolare categoria, puoi applicare una o più condizioni di targeting. Ad esempio, nella categoria Geo, puoi definire una regola come Città=San Francisco. Lʼaggiunta di più valori consente di creare una condizione O. Per soddisfare la condizione di targeting, il visitatore deve corrispondere solo a uno dei valori. Per condizioni E sullo stesso parametro, crea un target con espressione personalizzato.

Dopo aver creato una regola, fate clic su **[!UICONTROL Done (Fine)]**. Un riepilogo della regola viene visualizzato accanto al collegamento di targeting per il livello oggetto del targeting.

Puoi perfezionare ulteriormente una regola aggiungendo più condizioni o creando regole aggiuntive in altre categorie. Ad esempio, puoi eseguire il targeting solo degli utenti Firefox di San Francisco che accedono al tuo sito da Google. Imposta la categoria [!UICONTROL Geo] per il targeting degli utenti di San Francisco, la categoria [!UICONTROL Browser] per il targeting degli utenti che utilizzano Firefox e la categoria [!UICONTROL Origini traffico] per il targeting degli utenti provenienti da [!UICONTROL Da Google]. Le regole create tra le categorie vengono combinate con l’operatore AND.

Per creare regole di targeting complesse che includono operazioni OR tra le categorie, crea un target di espressione.

Puoi inoltre eseguire il targeting di parametri di profilo personalizzati e parametri `user.`. Quando aggiungi un pubblico, trascina e rilascia **[!UICONTROL Profilo visitatore]**, quindi scegli il parametro da utilizzare per eseguire il targeting dell&#39;attività. Se il parametro desiderato non viene visualizzato, significa che non è stato attivato da una mbox.

Utilizza la casella di ricerca per cercare nellʼelenco [!UICONTROL Tipi di pubblico]. Puoi cercare qualsiasi parte del nome di un pubblico, oppure racchiudere tra virgolette una stringa specifica.

Puoi ordinare l&#39;elenco [!UICONTROL Pubblico] in base al nome del pubblico o alla data dell&#39;ultima modifica. Per ordinare in base al nome o alla data, fai clic sull’intestazione di colonna, quindi seleziona la visualizzazione dei tipi di pubblico in ordine crescente o decrescente.

## Video di formazione: Creazione di tipi di pubblico ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
