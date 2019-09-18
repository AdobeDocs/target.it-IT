---
description: Per utilizzare Target nell’applicazione mobile, crea una posizione e una metrica di successo.
keywords: app mobile;posizione app mobile;target app mobile;posizioni target mobile;metriche di successo app mobile
seo-description: Per utilizzare Target nell’applicazione mobile, crea una posizione e una metrica di successo.
seo-title: iOS - Creare una posizione di destinazione e una metrica di successo
title: iOS - Creare una posizione di destinazione e una metrica di successo
topic: Target
uuid: dc39260c-8222-42b3-9f6b-f83be30e3210
translation-type: tm+mt
source-git-commit: ce8a890d0d662c0eec4d7fe254da371694811822

---


# iOS - Creare una posizione di destinazione e una metrica di successo{#ios-create-a-target-location-and-success-metric}

Per utilizzare Target nell’applicazione mobile, crea una posizione e una metrica di successo.

Questa sezione include il codice di esempio che può essere utilizzato come modello per l'app. Gli esempi in questa sezione contengono il codice per iOS. Gli stessi modelli si applicano ad Android. La sintassi specifica per Android può essere trovata nel manuale [](https://docs.adobe.com/content/help/en/mobile-services/android/target-android/target-main.html)Android SDK 4.x per Experience Cloud Solutions.

>[!NOTE]
>
>See the [Mobile documentation](https://docs.adobe.com/content/help/en/mobile-services/ios/target-ios/c-target-methods.html) for a list of all the available Target methods.

Per creare una posizione di destinazione nell'app e fare una richiesta, esistono due metodi principali:

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
   | `targetCreateRequestWithName:@"heroBanner"` | Sostituisci `heroBanner` con il nome della `targetLocation` in Target. È lo stesso del nome mbox. Il banner protagonista viene visualizzato nell'interfaccia di Target. |
   | `defaultContent:@"default.png"` | Sostituisci `default.png` con il valore utilizzato dall'app nel caso in cui Target non risponda. |
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
   | `NSString *content` | Sostituisci contenuto della richiesta con il contenuto effettivo che ritorna da Adobe. La stringa può essere XML, JSON o semplice. Utilizza questa sezione del codice per definire le variabili, impostare i percorsi delle immagini, visualizzare i flussi di regolazione, i punti di transazione o qualsiasi altra operazione che desideri eseguire. Target restituirà il contenuto immesso nell'interfaccia utente nello stesso formato. |
   | `heroImage.image = [UIImage imageNamed:content];` | Ad esempio: seleziona il contenuto e imposta il percorso per un'immagine protagonista. |

1. Creare una metrica di successo.

   Il metodo `targetCreateOrderConfirmRequestWithName` può essere utilizzato per monitorare una metrica di conversione/successo nell'app.

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

   Risultato passaggio: dopo aver creato correttamente una posizione di destinazione e aver applicato i tag a una metrica di successo, crea un test A/B. L'attività può essere creata utilizzando il Compositore esperienza basato su moduli.
