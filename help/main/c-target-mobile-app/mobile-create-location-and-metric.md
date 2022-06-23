---
keywords: app mobile;posizione app mobile;target app mobile;posizioni target mobile;metriche di successo app mobile
description: Visualizza il codice di esempio per scoprire come creare posizioni e metriche di successo nelle app iOS in modo da poter utilizzare Adobe [!DNL Target] per personalizzare e ottimizzare l’app.
title: Come creare [!DNL Target] Posizioni e metriche di successo in un’app iOS?
feature: Implement Mobile
role: Developer
exl-id: c2f05478-b019-47a7-b1a5-3783929e6732
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 82%

---

# iOS - creare un [!DNL Target] posizione e metrica di successo

Per utilizzare Target nell’applicazione mobile, crea una posizione e una metrica di successo.

Questa sezione include il codice di esempio che può essere utilizzato come modello per l&#39;app. Gli esempi in questa sezione contengono il codice per iOS. Gli stessi modelli si applicano ad Android. La sintassi specifica per Android può essere trovata nel manuale [](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/target-main.html)Android SDK 4.x per Experience Cloud Solutions.

>[!NOTE]
>
>Consulta la sezione [Documentazione mobile](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-target-methods.html) per un elenco di tutti i metodi di Target disponibili.

Per creare una posizione di destinazione nell&#39;app e fare una richiesta, esistono due metodi principali:

* `targetCreateRequestWithName`
* `targetLoadRequest`

1. Crea una posizione di destinazione.

   Ecco una chiamata di esempio per creare una richiesta:

   ```
   // make your request 
   ADBTargetLocationRequest *myRequest = [ADBMobile targetCreateRequestWithName:@"heroBanner" 
                                                    defaultContent:@"default.png" 
                                                    parameters:nil];
   ```

   | Parametro | Descrizione |
   |---|---|
   | `ADBTargetLocationRequest *myRequest` | Sostituisci `myRequest` con il nome della tua `targetLocation` nell’app. |
   | `targetCreateRequestWithName:@"heroBanner"` | Sostituisci `heroBanner` con il nome della `targetLocation` in Target. È lo stesso del nome mbox. Il banner protagonista viene visualizzato nell&#39;interfaccia di Target. |
   | `defaultContent:@"default.png"` | Sostituisci `default.png` con il valore utilizzato dall&#39;app nel caso in cui Target non risponda. |
   | `parameters:nil` | Specifica il profilo o i parametri mbox. Per ulteriori informazioni, consulta la sezione “passaggio di dati personalizzati”. |

   Ecco una chiamata di esempio per caricare la richiesta:

   ```
   // load your request 
   [ADBMobile targetLoadRequest:myRequest callback:^(NSString *content) { 
                                        // do something with content 
                                        heroImage.image = [UIImage imageNamed:content]; 
   }];
   ```

   | Parametro | Descrizione |
   |---|---|
   | `targetLoadRequest:myRequest` | Sostituisci `myRequest` con il nome della tua `targetLocation` nell’app. |
   | `NSString *content` | Sostituisci contenuto della richiesta con il contenuto effettivo che ritorna da Adobe. La stringa può essere XML, JSON o semplice. Utilizza questa sezione del codice per definire le variabili, impostare i percorsi delle immagini, visualizzare i flussi di regolazione, i punti di transazione o qualsiasi altra operazione che desideri eseguire. Target restituirà il contenuto immesso nell&#39;interfaccia utente nello stesso formato. |
   | `heroImage.image = [UIImage imageNamed:content];` | Ad esempio: seleziona il contenuto e imposta il percorso per un&#39;immagine protagonista. |

1. Creare una metrica di successo.

   Il metodo `targetCreateOrderConfirmRequestWithName` può essere utilizzato per monitorare una metrica di conversione/successo nell&#39;app.

   ```
   ADBTargetLocationRequest *req = [ADBMobile targetCreateOrderConfirmRequestWithName: "orderConfirm" 
                                              orderId: orderId 
                                              orderTotal: @"39.95" 
                                              productPurchasedId: _galleryItem.title 
                                              parameters: nil]; 
   [ADBMobile targetLoadRequest: req callback: nil];
   ```

   | Parametro | Descrizione |
   |---|---|
   | `orderId` | Sostituisci con una variabile dinamica che rappresenta un ID ordine univoco. |
   | `@"39.95"` | Sostituisci con una variabile dinamica che rappresenta un totale di ordine univoco. |
   | `_galleryItem.title` | Sostituisci con una variabile dinamica che rappresenta un elenco delimitato da virgole dei prodotti acquistati. |
   | `parameters: nil` | Dizionario facoltativo di parametri addizionali. |

1. Genera l’app.

   Risultato passaggio: dopo aver creato correttamente una posizione di destinazione e aver applicato i tag a una metrica di successo, crea un test A/B. L&#39;attività può essere creata utilizzando il Compositore esperienza basato su moduli.
