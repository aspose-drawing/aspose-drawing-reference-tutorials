---
date: 2026-05-19
description: Tutorial passo‑passo su come ritagliare in batch le immagini in PNG usando
  Aspose.Drawing, l'alternativa a System.Drawing per gli sviluppatori .NET.
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: Tutorial di ritaglio immagini – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Come ritagliare in batch le immagini in PNG usando Aspose.Drawing per .NET
url: /it/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come eseguire il ritaglio batch di immagini in PNG usando Aspose.Drawing per .NET

Se hai bisogno di **ritagliare un'immagine in PNG** rapidamente, in modo affidabile e su larga scala in un ambiente .NET, sei nel posto giusto. In questo tutorial illustreremo i passaggi esatti per caricare un'immagine, definire l'area di ritaglio e salvare il risultato come file PNG—tutto usando Aspose.Drawing, una moderna **alternativa a System.Drawing** che funziona cross‑platform. Vedrai anche come estendere il flusso a immagine singola in una pipeline completa di **ritaglio batch**.

## Risposte rapide
- **Quale libreria dovrei usare?** Aspose.Drawing per .NET (un'alternativa completa a System.Drawing.Common)  
- **Quanto tempo richiede il ritaglio di base?** Di solito meno di un secondo per un'immagine singola su una CPU moderna  
- **Posso ritagliare in PNG?** Sì – salva il bitmap ritagliato come file PNG (vedi Step 6)  
- **Ho bisogno di una licenza?** Una prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione  
- **È possibile il processamento batch?** Assolutamente – avvolgi gli stessi passaggi in un ciclo per elaborare più file  

## Come eseguire il ritaglio batch di immagini in PNG?

Carica ogni file sorgente con `new Bitmap(path)`, crea un `Bitmap` vuoto corrispondente per l'area di ritaglio, disegna il rettangolo selezionato usando `Graphics.DrawImage` e infine chiama `Save("output.png", ImageFormat.Png)`. Avvolgi queste sei righe all'interno di un ciclo `foreach` che itera su una directory e avrai una soluzione completa di ritaglio batch che elabora decine di immagini in pochi secondi.

## Perché usare Aspose.Drawing per il ritaglio batch?

Aspose.Drawing supporta **3 principali sistemi operativi** (Windows, Linux, macOS) e può gestire **immagini di oltre 500 pixel in meno di 0,5 secondi** su una tipica CPU di classe server. La sua API evita dipendenze native da GDI+, il che significa che puoi distribuire lo stesso codice su container, Azure App Service o AWS Lambda senza librerie aggiuntive. La libreria offre anche **oltre 50 formati immagine** e **preservazione completa del canale alfa**, rendendola ideale per il ritaglio di PNG trasparenti su larga scala.

## Cos'è “ritagliare immagine in PNG”?

L'operazione `crop image to PNG` estrae una regione rettangolare da un bitmap sorgente e scrive quella regione in un file PNG. PNG preserva qualsiasi canale alfa, fornendo compressione senza perdita, il che rende l'immagine risultante ideale per miniature, icone, risorse UI o qualsiasi situazione in cui sono richieste qualità e trasparenza.

## Perché Aspose.Drawing è un'alternativa a System.Drawing?

Aspose.Drawing funge da sostituto drop‑in per System.Drawing offrendo piena compatibilità cross‑platform, eliminando la necessità di librerie native GDI+. Supporta un'ampia gamma di formati pixel, fornisce manipolazione di immagini ad alte prestazioni e include funzionalità avanzate come la gestione del canale alfa e un ampio supporto dei formati, rendendola adatta sia per modifiche semplici che per elaborazioni batch su larga scala.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Libreria Aspose.Drawing** integrata nel tuo progetto .NET. Puoi scaricarla [qui](https://releases.aspose.com/drawing/net/).  
- Una cartella che contiene le immagini sorgente che desideri ritagliare. Sostituisci `"Your Document Directory"` nei frammenti di codice con il percorso reale sul tuo computer.

## Importare gli spazi dei nomi

Lo spazio dei nomi `System.Drawing` ci dà accesso a `Bitmap`, `Graphics` e tipi correlati che Aspose.Drawing estende.

```csharp
using System.Drawing;
```

## Guida passo‑passo

### Passo 1: Creare una Canvas Bitmap

`Bitmap` è la rappresentazione in‑memoria di un'immagine di Aspose.Drawing, fornendo accesso a livello di pixel e controllo del formato.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Iniziamo con una canvas vuota dimensionata per contenere il risultato ritagliato. Regola larghezza e altezza per corrispondere alle dimensioni dell'area che intendi estrarre.

### Passo 2: Creare un oggetto Graphics

`Graphics` è la superficie di disegno che ti permette di renderizzare forme, testo o altre immagini su un Bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Un oggetto `Graphics` ci consente di disegnare sulla canvas. `InterpolationMode` controlla come i valori dei pixel vengono calcolati durante il ridimensionamento o la trasformazione—`NearestNeighbor` funziona bene per bordi nitidi.

### Passo 3: Caricare l'immagine da ritagliare

`Image` (o `Bitmap`) carica il file sorgente in memoria, pronto per la manipolazione.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Carica l'immagine sorgente. Assicurati che il percorso punti a un file esistente; altrimenti verrà generata un'eccezione.

### Passo 4: Definire i rettangoli sorgente e destinazione

Gli oggetti `Rectangle` descrivono la regione dell'immagine sorgente da mantenere e dove dovrebbe essere posizionata sulla canvas di destinazione.

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` indica all'API quale parte dell'immagine originale mantenere. Qui scegliamo l'area 50 × 40 pixel in alto a sinistra. Assegnando lo stesso rettangolo a `destinationRectangle`, manteniamo la regione ritagliata nella sua dimensione originale.

### Passo 5: Eseguire l'operazione di ritaglio

`Graphics.DrawImage` copia la porzione definita di `image` sul nostro `bitmap` vuoto.

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` copia la porzione definita di `image` sul nostro `bitmap` vuoto. Questa è l'operazione principale **crop image to PNG**.

### Passo 6: Salvare l'immagine ritagliata (Crop Image to PNG)

`Bitmap.Save` scrive il bitmap in memoria su un file usando il formato specificato.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Infine, scrivi la canvas su disco come file PNG. PNG preserva qualsiasi canale alfa e fornisce qualità senza perdita—ideale per le risorse UI.

## Come eseguire il ritaglio batch di immagini in un ciclo?

Itera su ogni percorso file con `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, ripeti i Passi 1‑6 all'interno del ciclo e salva ogni risultato in una cartella di destinazione. Questo modello scala linearmente, può essere parallelizzato con `Parallel.ForEach` per una velocità ancora maggiore, e elabora le immagini in modo efficiente e rapido.

## Problemi comuni e consigli

- **Mismatched pixel format** – assicurati che l'immagine sorgente e il bitmap della canvas condividano un formato pixel compatibile per evitare spostamenti di colore.  
- **Disposizione degli oggetti GDI** – avvolgi `Bitmap` e `Graphics` in istruzioni `using` o chiama manualmente `Dispose()`; altrimenti potresti perdere risorse non gestite.  
- **Errori di coordinate** – le coordinate del rettangolo sono basate su zero. Selezionare un rettangolo che supera i limiti dell'immagine sorgente genererà un'eccezione.  

## Domande frequenti

**Q:** Posso ritagliare immagini di qualsiasi formato usando Aspose.Drawing?  
**A:** Sì, Aspose.Drawing supporta un'ampia gamma di formati (PNG, JPEG, BMP, GIF, TIFF, ecc.), quindi puoi ritagliare praticamente qualsiasi tipo di immagine.

**Q:** Sono disponibili opzioni di ritaglio avanzate?  
**A:** Assolutamente. Puoi combinare `GraphicsPath`, trasformazioni `Matrix` o usare la classe `ImageProcessor` per selezioni più complesse come ritagli circolari.

**Q:** Posso applicare più operazioni di ritaglio a una singola immagine?  
**A:** Sì. Dopo il primo ritaglio, puoi riutilizzare il bitmap risultante come nuova sorgente e ripetere il processo per concatenare più ritagli.

**Q:** Aspose.Drawing è adatto per l'elaborazione batch di immagini?  
**A:** Certamente. La sua API leggera e l'assenza di dipendenze native la rendono perfetta per elaborare grandi collezioni di immagini sui server.

**Q:** Come posso ottenere supporto per le domande relative ad Aspose.Drawing?  
**A:** Visita il [Forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) per chiedere assistenza e connetterti con la community.

**Ultimo aggiornamento:** 2026-05-19  
**Testato con:** Aspose.Drawing 24.11 per .NET  
**Autore:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
