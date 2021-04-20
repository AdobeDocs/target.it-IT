---
keywords: implementare;implementazione;configurazione;configurazione;attributi del cliente
description: Inserire dati in Target utilizzando gli attributi del cliente.
title: Come posso inserire dati in Target utilizzando gli attributi del cliente?
feature: Implementation
role: Developer
exl-id: b6c4a286-7994-492d-bde9-346af7aa314f
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 51%

---

# Attributi del cliente

Gli attributi del cliente consentono di caricare i dati del profilo del visitatore tramite FTP su [!DNL Adobe Experience Cloud]. Una volta effettuato l’aggiornamento, utilizza i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

I clienti Target Standard possono applicare cinque attributi, i clienti Target Premium possono applicare 200 attributi.

## Formato

Un file con estensione .csv con gli ID di Experience Cloud ID (ECID) e coppie di nome attributo e valore viene caricato tramite FTP o manualmente nell’interfaccia utente di Experience Cloud.

## Esempi di casi d’uso

Il tuo CRM o altro sistema interno memorizza informazioni preziose che desideri condividere con Adobe Experience Cloud, inclusi Target e Analytics.

## Vantaggi del metodo

Il caricamento dei dati del cliente crea una voce di profilo per il visitatore in Target, anche se Target non ha ancora visto il visitatore.

Gli stessi dati sono automaticamente disponibili in Target e Analytics.

FTP può essere un metodo di implementazione più semplice rispetto all&#39;API.

## Avvertenze

I clienti Target Standard possono applicare cinque attributi, i clienti Target Premium possono applicare 200 attributi

Può solo aggiornare i valori tramite gli attributi del cliente, non sulla pagina.

Richiede l&#39;implementazione di Experience Cloud ID (ECID).

## Esempi di codice

I dettagli sono disponibili in [Crea un&#39;origine attributo del cliente e carica il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).

### Link a informazioni rilevanti

[Crea un&#39;origine attributo del cliente e carica il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
