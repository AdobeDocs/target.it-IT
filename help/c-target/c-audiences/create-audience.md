---
description: Puoi creare tipi di pubblico personalizzati e salvarli nella libreria di Target per utilizzarli nelle attività. Puoi copiare un pubblico esistente, modificarlo per crearne uno simile e combinare più tipi di pubblico.
keywords: pubblico;regole del pubblico;creare pubblico;creazione pubblico
seo-description: Puoi creare tipi di pubblico personalizzati e salvarli nella libreria di Target per utilizzarli nelle attività. Puoi copiare un pubblico esistente, modificarlo per crearne uno simile e combinare più tipi di pubblico.
seo-title: Creare tipi di pubblico in Target
solution: Target
title: Creare tipi di pubblico in Target
topic: Advanced,Standard,Classic
uuid: 496dbb9d-cb13-47ee-88bd-ba5920b2ca1c
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Creare tipi di pubblico in Target{#build-audiences-in-target}

Puoi creare tipi di pubblico personalizzati e salvarli nella libreria di Target per utilizzarli nelle attività. Puoi copiare un pubblico esistente, modificarlo per crearne uno simile e combinare più tipi di pubblico.

## Panoramica sul pubblico

I tipi di pubblico sono definiti da regole che determinano chi è incluso o escluso da un'attività di [!DNL Target]. Una definizione di pubblico può includere più regole e ogni regola può includere più parametri. Le definizioni di pubblico complesse utilizzano gli operatori booleani AND e OR (E/O) per combinare regole e parametri per poter controllare in modo dettagliato quali visitatori del sito vengono conteggiati come partecipanti all'attività.

Quando si combinano regole o parametri con AND (E), qualsiasi membro potenziale del pubblico deve soddisfare *tutte* le condizioni definite per essere incluso come partecipante. Ad esempio, se si definisce una regola del sistema operativo e una regola del browser, solo i visitatori che utilizzano il sistema operativo definito *e* il browser definito sono inclusi nell'attività.

Quando si combinano regole o parametri con OR, qualsiasi membro potenziale del pubblico deve soddisfare solo una singola condizione definita per essere incluso come partecipante. Ad esempio, se si definiscono più regole mobili connesse da OR, i visitatori che soddisfano *uno* dei criteri definiti sono inclusi nell'attività.

È possibile combinare entrambi gli operatori booleani per creare regole complesse. Tuttavia, gli operatori allo stesso livello di regola devono corrispondere. L'interfaccia utente applica automaticamente l'operatore corretto.

For example, the following rule targets visitors who use either Chrome *or* Firefox on a Windows computer:

![Creare audience](assets/audience_create.png)

>[!NOTE]
>
>Fai attenzione a evitare la creazione di regole che escludano tutti i potenziali membri del pubblico. For example, it is not possible for someone to visit a page using Chrome *and* Firefox simultaneously.

## Creare un nuovo pubblico

1. Fai clic su **[!UICONTROL Tipi di pubblico]** nella barra superiore del menu.

   ![](assets/audiences_list.png)

1. Nellʼelenco [!UICONTROL Tipi di pubblico], fai clic su **[!UICONTROL + Crea pubblico]**.

   Oppure

   Per copiare un pubblico esistente, porta il cursore del mouse sul pubblico desiderato nellʼelenco [!UICONTROL Tipi di pubblico], quindi fai clic sullʼicona **[!UICONTROL Copia]**. Ora puoi modificare il pubblico per crearne uno simile.

1. Inserisci un nome descrittivo e univoco per il pubblico.
1. Fai clic su **[!UICONTROL + Aggiungi regola]**.

   Le regole consentono di limitare il pubblico a un sottoinsieme di visitatori del sito.
1. Seleziona un tipo di regola.

   Ogni tipo di regola ha i propri parametri. Consulta [Categorie di pubblico](../../c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) per ulteriori informazioni su come configurare ogni tipo di regola per la definizione del pubblico.
1. Definisci i parametri della regola.
1. Fai clic su **[!UICONTROL Salva]**.

   Il pubblico appena creato viene visualizzato nell'elenco dopo alcuni secondi di ritardo dovuti all'elaborazione. Se il pubblico non viene visualizzato immediatamente nell'elenco, prova a cercarlo o ad aggiornare l'elenco.

## Video di formazione: Creazione di tipi di pubblico

Questo video include informazioni su come creare i tipi di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392?captions=ita)