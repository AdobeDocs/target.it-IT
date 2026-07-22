---
title: Creazione e utilizzo dei set di regole
description: Scopri come creare un set di regole riutilizzabile di criteri contestuali per il pubblico in Flag e importarlo in flag di funzioni e gruppi di funzioni.
badge: label="Beta" type="Informative"
hide: true
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 1%

---

# Creazione e utilizzo dei set di regole {#creating-and-using-rule-sets}

Un set di regole è una raccolta riutilizzabile di criteri contestuali di pubblico. Crea un set di regole quando più flag di funzionalità o gruppi di funzionalità richiedono lo stesso pubblico. Puoi quindi importare il set di regole invece di ricreare i criteri di pubblico per ogni funzione.

## Requisiti del set di regole {#requirements}

| Etichetta interfaccia utente | Utilizzo | Obbligatorio |
| --- | --- | --- |
| **Inserisci set di regole** | Immettere un nome per il set di regole. | Sì |
| **Descrizione set regole** | Descrivi lo scopo del set di regole. | No |
| **Contesto** | Definisci almeno un criterio di pubblico. Gli attributi di contesto sono campi denominati come il livello di abbonamento, la versione dell’applicazione o l’area geografica. | Sì |

## Creare un set di regole {#create-rule-set}

### Passaggio 1: avviare un nuovo set di regole {#step-1-start}

In Flag, selezionare **Set di regole** dal menu di navigazione a sinistra, quindi selezionare **Nuovo set di regole**.

Nella scheda **Set di regole personali** sono visualizzati i set di regole creati dall&#39;utente. Nella scheda **Set di regole team** sono visualizzati i set di regole disponibili per il team.

![Elenco set di regole senza set di regole ancora creato](assets/rule-set-list-empty.png)

### Passaggio 2: aggiungere i dettagli e i criteri del set di regole {#step-2-details}

1. Immettere un nome per il set di regole.
1. È possibile inserire una descrizione.
1. In **Contesto**, definisci i criteri di pubblico da riutilizzare.
1. Utilizza **And** o **Or** per combinare più criteri.
1. Per creare un&#39;espressione più complessa, selezionare **Abilita logica nidificata**.

![Modulo di creazione set di regole con criteri di contesto di esempio](assets/rule-set-create-context.png)

### Passaggio 3: salvare il set di regole {#step-3-save}

Seleziona **Salva impostazioni**. Il set di regole salvato viene visualizzato in **Set di regole personale**.

![Elenco set di regole che mostra un set di regole appena salvato](assets/rule-set-list-created.png)

## Utilizzare un set di regole in un flag di funzione o in un gruppo di funzioni {#use-rule-set}

### Passaggio 1: aprire e abilitare le impostazioni relative al pubblico {#step-1-open}

Apri il flag di funzione o il gruppo di funzioni in cui desideri utilizzare il set di regole, seleziona la scheda **Pubblico**, quindi attiva **Regola pubblico** per abilitare i criteri di pubblico.

### Passaggio 2: selezionare il set di regole {#step-2-select}

Apri il menu a discesa **Seleziona set di regole**. Scegli il set di regole da **Set di regole personale** o **Set di regole personale**.

![Seleziona set di regole aperto a discesa nella scheda Pubblico](assets/rule-set-select-in-audience.png)

### Passaggio 3: rivedere i criteri importati {#step-3-review}

I criteri di contesto dal set di regole selezionato vengono importati nel pubblico. Esaminate i criteri e salvate il flag di feature o il gruppo di feature.

![Scheda Pubblico con flag di funzionalità che mostra i criteri del set di regole importato](assets/rule-set-imported-audience.png)

È possibile utilizzare lo stesso set di regole in più flag di funzionalità e gruppi di funzionalità che richiedono lo stesso pubblico.

### Passaggio 4: salvare il flag di funzione o il gruppo di funzioni {#step-4-save}

Dopo aver esaminato i criteri di pubblico importati, seleziona **Salva impostazioni**.

>[!NOTE]
>
>L’importazione di un set di regole copia i relativi criteri di pubblico nel flag di funzione o nel gruppo di funzioni. Se i criteri di pubblico devono essere aggiornati in un secondo momento, aggiornali separatamente in ogni flag di funzione e gruppo di funzioni in cui è stato importato il set di regole. L’aggiornamento del set di regole originale non aggiorna automaticamente i tipi di pubblico importati in precedenza.

## Creare un set di regole da un flag di feature o da un gruppo di feature {#create-from-feature}

Puoi anche creare un set di regole direttamente dalla schermata Pubblico di un flag di funzione o di un gruppo di funzioni:

1. Apri il flag di funzionalità o il gruppo di funzionalità, quindi seleziona la scheda **Pubblico**.
1. Attiva **Regola pubblico**.
1. Definisci i criteri contestuali da riutilizzare.
1. Seleziona il pulsante **+** nell&#39;angolo superiore destro, accanto al menu a discesa **Seleziona set di regole**.
1. Nella finestra di dialogo **Salva set di regole**, inserisci un nome per il set di regole.
1. Seleziona **Salva set di regole**.

## Vedi anche {#see-also}

* [Creazione degli attributi di contesto](creating-your-context-attributes.md)
* [Usa contesto nelle regole del pubblico](using-context-in-audience-rules.md)
* [Pubblico nei flag di funzione e nei gruppi di funzioni](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
