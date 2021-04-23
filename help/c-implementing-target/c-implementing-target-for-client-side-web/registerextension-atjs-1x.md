---
keywords: registerExtension;registerextension;registra estensione;at.js;funzioni;funzione;clientCode;serverDomain;globalMboxName;globalMboxAutoCreate;timeout
description: Utilizza la funzione registerExtension() per la libreria JavaScript Adobe [!DNL Target] at.js per registrare un'estensione specifica. (at.js 1.x)
title: Come si utilizza la funzione registerExtension()?
feature: at.js
role: Developer
exl-id: 7f0898b4-ddd5-425c-99dc-94f9b30f8ba7
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 90%

---

# registerExtension() - at.js 1.x

Fornisce un metodo standard per registrare un’estensione specifica.

>[!NOTE]
>
>Questa funzione è disponibile per at.js versione 1.*x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x.

Il parametro delle opzioni è obbligatorio e ha la seguente struttura:

| Chiave | Tipo | Obbligatorio | Descrizione |
|--- |--- |--- |--- |
| name | Stringa | Sì | Nome di estensione. |
| modules | Array[Stringa] | Sì | Array di stringhe che rappresentano i nomi dei moduli richiesti. |
| register | Funzione | Sì | Una funzione utilizzata per inizializzare e compilare l&#39;estensione. Questa funzione riceve argomenti basati sull’array dei moduli. |

Note:

* se uno dei parametri non viene fornito, viene generata un&#39;eccezione.
* Se l’array dei moduli è vuoto, viene generata un&#39;eccezione.

Per ulteriori informazioni ed esempi sull’utilizzo di `registerExtension`, consulta la pagina [Estensioni atjs di Adobe Experience Cloud](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions) su GitHub.

## Metodi del modulo impostazioni {#section_8501CDD4B0624FA2B10532C98C5F4328}

| Chiave | Tipo | Descrizione |
|--- |--- |--- |
| clientCode | Stringa | Codice cliente |
| serverDomain | Stringa | Dominio server Edge |
| globalMboxName | Stringa | Nome mbox globale di Target |
| globalMboxAutoCreate | Booleano | Indica se la creazione automatica è abilitata o meno |
| timeout | Numero | Timeout richiesta |

## Metodi del modulo logger {#section_10AF62B49AEF48F981E950D26E176138}

| Chiave | Tipo | Descrizione |
|--- |--- |--- |
| log | Funzione | Registra l&#39;elenco di variabili di argomenti nella console del browser, se esiste. Viene attivato solo quando `mboxDebug=true` viene passato all&#39;URL. |
| error | Funzione | Registra l&#39;elenco delle variabili degli argomenti nella console del browser. Viene attivato solo quando sono presenti errori gravi, ad esempio timeout di rete, nodo HTML non trovato, ecc. |
