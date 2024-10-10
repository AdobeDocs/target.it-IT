---
keywords: più tipi di pubblico;versioni esperienza;versioni esperienza target
description: Scopri come eseguire il targeting di diversi segmenti di pubblico con versioni della stessa esperienza nelle attività A/B.
title: Posso utilizzare più versioni di esperienza in un'attività A/B?
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: ec35109b5d668a96f7e71149df7c965ce2bf3ceb
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 52%

---

# Esperienza con più tipi di pubblico un testo A/B

È possibile indirizzare le versioni della stessa esperienza a tipi di pubblico diversi nelle attività A/B di [!DNL Adobe Target]. È possibile impostare più tipi di pubblico per un&#39;esperienza nel [!UICONTROL Visual Experience Composer] (VEC) o nel Compositore esperienza basato su moduli.

I visitatori possono passare da un pubblico all’altro con la modifica del loro profilo. I visitatori non rimangono bloccati nella stessa esperienza per tutta la durata dell’attività.

Ad esempio, se il sito utilizza una progettazione coerente tra pagine o prodotti e si desidera utilizzare la stessa esperienza per più destinatari (ad esempio, i visitatori che utilizzano browser in diverse lingue), è possibile impostare più versioni dell&#39;esperienza. È presentare la stessa esperienza a inglesi e giapponesi, l&#39;unica differenza è che il testo è nella lingua del visitatore. Vengono raccolti i dati dell&#39;esperienza, a prescindere dalla lingua; in questo modo, il rapporto mostra le prestazioni dell&#39;esperienza, anziché della versione.

Senza la possibilità di impostare le versioni dell&#39;esperienza, è necessario impostare diversi test per ogni lingua (in questo esempio), quindi aggregare manualmente i risultati per cercare di ottenere un quadro delle prestazioni di una singola esperienza con entrambe le lingue. Tale metodo produce risultati meno accurati. Per alcuni test, questi calcoli potrebbero persino non essere utili per via della casualizzazione dei visitatori.

Con la creazione di diverse versioni di un&#39;esperienza, si ricevono informazioni più accurate senza la necessità di calcoli manuali e ipotesi.

## Scenario

Stai testando due esperienze, un banner con targeting geografico rispetto a un banner generico. Il banner per ogni area geografica deve essere diverso, ma il test generale consiste nel determinare se il geotargeting è migliore della visualizzazione di contenuti generici. Se imposti un’esperienza separata per ogni posizione, in realtà misurerai le prestazioni di ogni area geografica rispetto alle altre, anziché stabilire se il geotargeting aiuta a raggiungere gli obiettivi di successo quando viene misurato rispetto al banner generico.

In questo caso, sono necessarie versioni specifiche per l’area geografica dell’esperienza, in modo da poter testare l’esperienza con targeting geografico rispetto a un controllo non con targeting geografico.

1. [Crea un&#39;attività A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) come si farebbe normalmente.

   Al momento di configurare l’esperienza che avrà più versioni, seleziona il pubblico per ogni versione, come illustrato nei passaggi seguenti.

1. Seleziona l&#39;esperienza, quindi fai clic su **[!UICONTROL Configure]** > **[!UICONTROL Multiple Audiences]**.

1. Fai clic sull&#39;icona **[!UICONTROL Add Audience]** ( ![Icona Aggiungi](/help/main/assets/icons/Add.svg) ) nel riquadro Pubblico esperienza, quindi seleziona il primo pubblico a cui desideri rivolgerti. Ripeti per ogni pubblico.

   Se il pubblico non esiste ancora, fai clic su [Crea pubblico](/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558) e configuralo.

   Se un visitatore è adeguato per più di un pubblico, il contenuto viene respinto per tutti i tipi di pubblico e l&#39;ultimo nell&#39;elenco esegue effettivamente il rendering sulla pagina.

1. Continua a configurare l’attività.

## Best practice

* Scegli tipi di pubblico reciprocamente esclusivi. Se l’attività è stata creata nel Compositore esperienza visivo e un visitatore corrisponde a più di un pubblico, viene restituito il contenuto di ciascun pubblico e il contenuto del pubblico elencato per ultimo viene visualizzato nella pagina.
* Il pubblico di accesso all&#39;attività definito nel diagramma viene combinato con il pubblico di esperienza utilizzando una condizione E. Per accedere all&#39;attività, un visitatore deve essere idoneo al pubblico di attività e uno dei tipi di pubblico dell&#39;esperienza.
* Aggiungi gli stessi tipi di pubblico come segmenti per i rapporti. Questo consente di esaminare i risultati del test ai livelli elevati dell’esperienza A rispetto a B e al livello inferiore dell’esperienza A rispetto a B solo per &quot;browser lang ja_JP&quot;. Funziona solo per i report basati su [!DNL Target], non per i report basati su [!DNL Analytics].