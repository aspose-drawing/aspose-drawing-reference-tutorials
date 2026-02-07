---
date: 2026-02-07
description: Tutorial passo‑passo per ritagliare un’immagine in PNG usando Aspose.Drawing,
  l’alternativa a System.Drawing per gli sviluppatori .NET. Include il ritaglio batch
  e le tecniche essenziali.
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Come ritagliare un'immagine in PNG con Aspose.Drawing per .NET
url: /it/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come ritagliare un'immagine in PNG con Aspose.Drawing per .NET

Se hai bisogno di **ritagliare un'immagine in PNG** rapidamente e in modo affidabile in un ambiente .NET, sei nel posto giusto. In questo tutorial ti guideremo passo passo nel caricare un'immagine, definire l'area di ritaglio e salvare il risultato come file PNG—tutto usando Aspose.Drawing, una moderna **alternativa a System.Drawing** che funziona cross‑platform.

## Risposte rapide
- **Quale libreria devo usare?** Aspose.Drawing per .NET (un'alternativa completa a System.Drawing.Common)  
- **Quanto tempo richiede il ritaglio base?** Di solito meno di un secondo per un'immagine singola su una CPU moderna  
- **Posso ritagliare in PNG?** Sì – salva il bitmap ritagliato come file PNG (vedi Passo 6)  
- **Ho bisogno di una licenza?** Una prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza commerciale per la produzione  
- **È possibile l'elaborazione batch?** Assolutamente – avvolgi gli stessi passaggi in un ciclo per elaborare più file  

## Cos'è “ritagliare un'immagine in PNG”?

Ritagliare un'immagine significa estrarre una regione rettangolare dal bitmap originale. Quando salvi quella regione come PNG, mantieni la trasparenza e ottieni una compressione senza perdita—perfetta per miniature, icone o qualsiasi risorsa UI.

## Perché Aspose.Drawing è un'alternativa a System.Drawing?

- **Supporto cross‑platform** – funziona su Windows, Linux e macOS senza dipendenze native da GDI+.  
- **Gestione avanzata dei formati pixel** – 32‑bit, 24‑bit, indicizzati e altro.  
- **API orientata alle prestazioni** – ideale sia per modifiche a immagine singola sia per lavori batch su larga scala.  

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Libreria Aspose.Drawing** integrata nel tuo progetto .NET. Puoi scaricarla [qui](https://releases.aspose.com/drawing/net/).  
- Una cartella che contiene le immagini sorgente che desideri ritagliare. Sostituisci `"Your Document Directory"` nei frammenti di codice con il percorso reale sul tuo computer.

## Importa gli spazi dei nomi

```csharp
using System.Drawing;
```

Lo spazio dei nomi `System.Drawing` ci fornisce l'accesso a `Bitmap`, `Graphics` e tipi correlati che Aspose.Drawing estende.

## Guida passo‑passo

### Passo 1: Crea una canvas Bitmap

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Iniziamo con una canvas vuota dimensionata per contenere il risultato ritagliato. Regola larghezza e altezza per corrispondere alle dimensioni dell'area che intendi estrarre.

### Passo 2: Crea un oggetto Graphics

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Un oggetto `Graphics` ci permette di disegnare sulla canvas. `InterpolationMode` controlla come i valori dei pixel vengono calcolati durante lo scaling o la trasformazione—`NearestNeighbor` funziona bene per bordi nitidi.

### Passo 3: Carica l'immagine da ritagliare

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Carica l'immagine sorgente. Assicurati che il percorso punti a un file esistente; altrimenti verrà generata un'eccezione.

### Passo 4: Definisci i rettangoli di origine e destinazione

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

Il `sourceRectangle` indica all'API quale parte dell'immagine originale conservare. Qui scegliamo l'area 50 × 40 pixel in alto a sinistra. Assegnando lo stesso rettangolo a `destinationRectangle`, manteniamo la regione ritagliata nella sua dimensione originale.

### Passo 5: Esegui l'operazione di ritaglio

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` copia la porzione definita di `image` sul nostro `bitmap` vuoto. Questa è l'operazione principale di **ritaglio immagine in PNG**.

### Passo 6: Salva l'immagine ritagliata (Ritaglia immagine in PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Infine, scrivi la canvas su disco come file PNG. PNG conserva eventuali canali alfa e fornisce qualità senza perdita—ideale per risorse UI.

## Come ritagliare immagini in uno scenario batch

Quando hai decine o centinaia di immagini, basta inserire l'intero frammento all'interno di un ciclo `foreach` che itera su una collezione di percorsi file. La stessa logica di `Graphics.DrawImage` si applica, rendendo il **ritaglio batch di immagini** un'estensione banale di questo tutorial.

## Problemi comuni e consigli

- **Mancata corrispondenza del formato pixel** – assicurati che l'immagine sorgente e il bitmap della canvas condividano un formato pixel compatibile per evitare spostamenti di colore.  
- **Rilascio degli oggetti GDI** – avvolgi `Bitmap` e `Graphics` in istruzioni `using` o chiama manualmente `Dispose()`; altrimenti potresti perdere risorse non gestite.  
- **Errori di coordinate** – le coordinate dei rettangoli partono da zero. Selezionare un rettangolo che supera i limiti dell'immagine sorgente genererà un'eccezione.  

## Domande frequenti

**D: Posso ritagliare immagini di qualsiasi formato usando Aspose.Drawing?**  
R: Sì, Aspose.Drawing supporta un'ampia gamma di formati (PNG, JPEG, BMP, GIF, TIFF, ecc.), quindi puoi ritagliare praticamente qualsiasi tipo di immagine.

**D: Sono disponibili opzioni di ritaglio avanzate?**  
R: Assolutamente. Puoi combinare `GraphicsPath`, trasformazioni `Matrix`, o usare la classe `ImageProcessor` per selezioni più complesse come ritagli circolari.

**D: Posso applicare più operazioni di ritaglio a una singola immagine?**  
R: Sì. Dopo il primo ritaglio, puoi riutilizzare il bitmap risultante come nuova sorgente e ripetere il processo per concatenare più ritagli.

**D: Aspose.Drawing è adatto per l'elaborazione batch di immagini?**  
R: Sì. La sua API leggera e l'assenza di dipendenze native la rendono perfetta per elaborare grandi collezioni di immagini sui server.

**D: Come posso ottenere supporto per domande relative ad Aspose.Drawing?**  
R: Visita il [Forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) per chiedere assistenza e connetterti con la community.

---

**Ultimo aggiornamento:** 2026-02-07  
**Testato con:** Aspose.Drawing 24.11 for .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}