---
keywords: pubblico;regole del pubblico;creare pubblico;creazione pubblico
description: Scopri come creare tipi di pubblico personalizzati e salvarli in [!DNL Adobe Target] [!UICONTROL Tipi di pubblico] libreria da utilizzare nelle attività.
title: Come Si Creano I Tipi Di Pubblico?
feature: Audiences
exl-id: 59057461-d958-4d38-9725-53aacbe1f7eb
source-git-commit: a185edee86f6d07b488cf5dd3fe7e5dc3f4e87b3
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 59%

---

# Creare tipi di pubblico in [!DNL Target]

Puoi creare tipi di pubblico personalizzati e salvarli in [!DNL Adobe Target] [!UICONTROL Tipi di pubblico] da utilizzare nelle attività. Puoi anche copiare un pubblico esistente da modificare per crearne uno simile e combinare più tipi di pubblico.

## Panoramica sul pubblico

I tipi di pubblico sono definiti da regole che determinano chi è incluso o escluso da un&#39;attività di [!DNL Target]. Una definizione di pubblico può includere più regole e ogni regola può includere più parametri. Le definizioni di pubblico complesse utilizzano gli operatori booleani AND e OR (E/O) per combinare regole e parametri per poter controllare in modo dettagliato quali visitatori del sito vengono conteggiati come partecipanti all&#39;attività.

Quando combini regole o parametri con AND, qualsiasi potenziale membro del pubblico deve soddisfare *tutto* condizioni definite da includere come partecipante. Ad esempio, se si definisce una regola del sistema operativo e una regola del browser, solo i visitatori che utilizzano il sistema operativo definito *e* il browser definito sono inclusi nell&#39;attività.

Quando si combinano regole o parametri con OR, qualsiasi membro potenziale del pubblico deve soddisfare solo una singola condizione definita per essere incluso come partecipante. Ad esempio, se si definiscono più regole mobili connesse da OR, i visitatori che soddisfano *uno* dei criteri definiti sono inclusi nell&#39;attività.

È possibile combinare entrambi gli operatori booleani per creare regole complesse. Tuttavia, gli operatori allo stesso livello di regola devono corrispondere. L&#39;interfaccia utente applica automaticamente l&#39;operatore corretto.

Ad esempio, la regola seguente è destinata ai visitatori che utilizzano Chrome *oppure* Firefox su un computer Windows:

![Creare un pubblico](assets/audience_create.png)

>[!NOTE]
>
>Fai attenzione a evitare la creazione di regole che escludano tutti i potenziali membri del pubblico. Ad esempio, non è possibile che qualcuno visiti una pagina utilizzando contemporaneamente i browser Chrome *e* Firefox.

## Creazione di un pubblico

1. Fai clic su **[!UICONTROL Tipi di pubblico]** nella barra superiore del menu.

   ![immagine audiences_list](assets/audiences_list.png)

1. Dalla sezione [!UICONTROL Tipi di pubblico] , fare clic su **[!UICONTROL Crea pubblico]**.

   Oppure

   Per copiare un pubblico esistente, da [!UICONTROL Tipi di pubblico] , fare clic sul pulsante **[!UICONTROL Altre azioni]** (icona con i puntini di sospensione), quindi fai clic su **[!UICONTROL Duplica]**. Ora puoi modificare il pubblico per crearne uno simile.

1. Digita un nome descrittivo e univoco per il pubblico e una descrizione facoltativa.

   I nomi del pubblico non possono iniziare con i seguenti caratteri:

   `=  +  -  !  @`

   I nomi del pubblico non possono contenere nessuna delle seguenti sequenze di caratteri:

   `;=  ;+  ;-  ;@  ,=  ,+  ,-  ,@  ["  "]  ['  ]'`

1. Trascina e rilascia gli attributi desiderati dal menu **[!UICONTROL Attributi]** a destra del riquadro audience builder.

   ![Trascinare gli attributi](assets/drag-attribute.png)

   Ogni tipo di regola ha i propri parametri. Consulta [Categorie di pubblico](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) per ulteriori informazioni su come configurare ogni tipo di regola per la definizione del pubblico.

1. Definisci i parametri della regola.

   Ad esempio, il pubblico seguente include i visitatori dello Utah che utilizzano il sistema operativo Macintosh.

   ![Pubblico Utah/Macintosh](assets/adience-builder.png)

1. (Condizionale) Continua ad aggiungere e definire gli attributi desiderati.

   Per creare un altro contenitore, fai clic su **[!UICONTROL Aggiungi contenitore]** o semplicemente trascina un altro attributo nel riquadro Audience Builder. È quindi possibile regolare l’operatore (AND o OR) utilizzando l’elenco a discesa.

1. Fai clic su **[!UICONTROL Fine]**.

   Il pubblico appena creato viene visualizzato nell&#39;elenco dopo alcuni secondi di ritardo dovuti all&#39;elaborazione. Se il pubblico non viene visualizzato immediatamente nell&#39;elenco, prova a cercarlo o ad aggiornare l&#39;elenco.

## Video di formazione: Creazione di tipi di pubblico ![Icona Panoramica](/help/main/assets/overview.png)

Questo video include informazioni su come creare i tipi di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
