---
description: 'Informazioni sulla funzione registerExtension() per at.js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione registerExtension() per la libreria JavaScript at.js di Adobe Target.
seo-title: Informazioni sulla funzione registerExtension() per la libreria JavaScript at.js di Adobe Target.
solution: Target
subtopic: Introduzione
title: registerExtension()
topic: Standard
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# registerExtension() - at.js 1.x

Fornisce un metodo standard per registrare un’estensione specifica.

>[!NOTE]
>
>Questa funzione è disponibile per at.js versione 1.Solo *x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x.

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
