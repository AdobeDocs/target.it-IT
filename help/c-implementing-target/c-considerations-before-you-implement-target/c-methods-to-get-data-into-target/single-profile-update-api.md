---
keywords: implementare;implementazione;configurazione;configurazione;aggiornamento profilo singolo
description: Ottieni i dati in  [!DNL Target] utilizzando l'API di aggiornamento del singolo profilo.
title: Come posso inserire i dati in [!DNL Target] utilizzando l'API di aggiornamento del singolo profilo?
feature: Implementazione
role: Developer
exl-id: 8331866c-0b84-4d08-83b4-f7f82c67cd21
source-git-commit: 18b9a56b8aef2fdfb8a4431fec4ae3a65adcf067
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 59%

---

# Aggiornamento di singolo profilo API

Quasi identico all&#39;API di aggiornamento del profilo bulk, ma un solo profilo visitatore alla volta viene aggiornato, in linea con la chiamata API anziché con un file .csv.

## Formato

Il visitatore deve essere identificato tramite il valore mboxPC di Target o il valore mboxThirdPartyId. Experience Cloud ID (ECID) non è supportato.

## Esempi di casi d&#39;uso

Vuoi aggiornare Target in tempo reale quando un visitatore esegue alcune azioni offline. Le azioni possono includere il raggiungimento di un call center, un prestito è finanziato, utilizzando una carta fedeltà in negozio, l&#39;accesso a un chiosco e così via.

## Vantaggi del metodo

Nessun limite al numero di attributi del profilo.

Gli attributi del profilo inviati tramite il sito possono essere aggiornati tramite l&#39;API e viceversa.

## Avvertenze

Limite delle chiamate API di 1 milione per 24 ore

Aggiorna solo i profili. Impossibile creare un profilo per un potenziale utente che Target non ha ancora visto.

## Esempi di codice

GET e POST supportati. `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

>[!MORELIKETHIS]
>
>* [Aggiornamento di profili](https://developers.adobetarget.com/api/#updating-profiles)

