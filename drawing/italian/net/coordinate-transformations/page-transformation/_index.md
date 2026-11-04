---
date: 2026-11-04
description: Scopri come disegnare grafica di rettangoli eseguendo la coordinate system
  transformation in .NET con l'API Aspose.Drawing. Questa guida passo‑passo mostra
  come convertire inches in pixels e impostare page units.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Coordinate system transformation in Aspose.Drawing
og_description: Scopri come disegnare grafica di rettangoli convertendo inches in
  pixels e impostando page units in Aspose.Drawing per .NET. Segui la guida passo‑passo
  per una page transformation precisa.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Come disegnare un rettangolo con page transformation usando Aspose.Drawing
  per .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Come disegnare un rettangolo – coordinate system transformation (page transformation)
  in Aspose.Drawing per .NET
url: /it/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare un rettangolo – trasformazione del sistema di coordinate (trasformazione della pagina) in Aspose.Drawing per .NET

## Introduzione

In questo tutorial imparerai **come disegnare un rettangolo** grafico mentre esegui una trasformazione del sistema di coordinate a livello di pagina usando Aspose.Drawing per .NET. Che tu stia costruendo un motore di reporting, uno strumento di schizzi in stile CAD o qualsiasi applicazione che richieda misurazioni precise del mondo reale, questa guida ti accompagna passo dopo passo—dalla creazione di un bitmap al salvataggio del PNG finale. Alla fine sarai a tuo agio nel convertire pollici in pixel, cancellare lo sfondo della tela e impostare le unità di pagina per un output pronto per la stampa.

## Risposte rapide
- **Che cos'è la trasformazione del sistema di coordinate?** Mappa le unità a livello di pagina (come i pollici) alle pixel a livello di dispositivo in modo che i disegni vengano scalati correttamente su qualsiasi dispositivo di output.  
- **Perché scegliere Aspose.Drawing?** Fornisce un'API grafica completamente gestita e cross‑platform che sostituisce System.Drawing.Common e supporta oltre 30 formati immagine.  
- **Quanto tempo richiede l'implementazione dell'esempio?** Circa 5‑10 minuti per un rettangolo di base con trasformazione della pagina.  
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza commerciale per le distribuzioni in produzione.  
- **Quali runtime .NET sono supportati?** .NET Framework 4.6+, .NET Core 3.1+ e .NET 5/6/7.

## Cos'è Aspose.Drawing?

Aspose.Drawing è una libreria grafica .NET che fornisce un'**API indipendente dal dispositivo** per creare e manipolare immagini raster, vettori e disegni a livello di pagina senza fare affidamento su GDI+. Supporta **oltre 30 formati immagine** e può elaborare immagini fino a **10.000 × 10.000 pixel** mantenendo un basso utilizzo di memoria.

## Perché utilizzare la trasformazione del sistema di coordinate con Aspose.Drawing?

La trasformazione del sistema di coordinate ti consente di progettare grafica in unità del mondo reale mentre la libreria gestisce automaticamente il ridimensionamento dei pixel per qualsiasi dispositivo di output. Questo approccio garantisce che un rettangolo di 5 pollici venga stampato esattamente a cinque pollici su una stampante a 300 DPI e appaia proporzionalmente su uno schermo a 96 DPI, eliminando errori di conversione manuale.

- **Progettazione indipendente dal dispositivo:** Scrivi il codice una sola volta; Aspose.Drawing lo scala per schermi, stampanti o PDF.  
- **Disegno di precisione:** Ideale per diagrammi tecnici, schemi ingegneristici o qualsiasi scenario in cui le misurazioni esatte sono importanti.  
- **Affidabilità cross‑platform:** Funziona in modo coerente su Windows, Linux e macOS senza le limitazioni GDI+ di System.Drawing.  
- **Prestazioni:** Su una CPU tipica da 2,5 GHz, disegnare un rettangolo di 5 pollici a 300 DPI richiede meno di **15 ms**, e la libreria può renderizzare **50 fotogrammi al secondo** in scenari di anteprima in tempo reale.

## Prerequisiti

- **Libreria Aspose.Drawing:** Scarica l'ultima versione dal sito ufficiale [qui](https://releases.aspose.com/drawing/net/).  
- **IDE:** Visual Studio, Rider o qualsiasi editor compatibile con .NET.  
- **Cartella di output:** Sostituisci `"Your Document Directory"` nel codice di esempio con la cartella in cui desideri salvare il PNG.  
- **Supporto ASP.NET opzionale:** Puoi aggiungere il pacchetto NuGet a un progetto ASP.NET Core e utilizzare la stessa API; il pattern segue l'approccio tipico **how to use aspnet** per le librerie .NET.

## Come disegnare un rettangolo con la trasformazione della pagina?

Carica un bitmap vuoto, imposta l'unità di pagina su pollici e disegna un rettangolo usando una penna sottile blu—questo completa il disegno del rettangolo in poche righe di codice. La proprietà `Graphics.PageUnit` indica al motore di interpretare tutte le coordinate come pollici, così puoi pensare in misure reali invece che in pixel grezzi, e la libreria converte automaticamente **pollici in pixel** in base al DPI del bitmap.

### Passo 1: importare gli spazi dei nomi

Le istruzioni `using` ti danno accesso alle classi di disegno principali.

```csharp
using System.Drawing;
```

### Passo 2: creare un bitmap

`Bitmap` è il contenitore immagine in memoria su cui disegni. Contiene il buffer di pixel e espone metodi per salvare su file. Creare un bitmap definisce le dimensioni della tela e il formato dei pixel.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Passo 3: creare un oggetto graphics

`Graphics` fornisce la superficie di disegno per il bitmap. Traduce i comandi di disegno ad alto livello (linee, forme, testo) in operazioni sui pixel del bitmap sottostante.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Passo 4: cancellare lo sfondo della tela

Cancellare la tela con un colore neutro garantisce che le tue forme risaltino. In questo esempio riempiamo lo sfondo con grigio chiaro, dimostrando anche la tecnica **clear canvas background**.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Passo 5: impostare la trasformazione (come impostare le unità)

`Graphics.PageUnit` specifica l'unità di misura usata per le coordinate di pagina. Impostandola su `GraphicsUnit.Inch` si dice ad Aspose.Drawing di **convertire pollici in pixel** automaticamente in base al DPI del bitmap (96 DPI di default, 300 DPI per stampa ad alta risoluzione). Puoi anche scegliere `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` o `GraphicsUnit.Pixel` a seconda delle esigenze del layout.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Passo 6: disegnare un rettangolo – disegnare grafica rettangolare

`Pen` definisce colore, larghezza e stile delle linee disegnate su una superficie graphics. Usando una penna sottile blu, disegniamo un rettangolo le cui dimensioni sono espresse in pollici, rendendo il codice più leggibile per layout orientati alla stampa.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Passo 7: salvare il bitmap come png

Infine, scrivi il bitmap in un file PNG nella cartella specificata in precedenza. Il salvataggio come PNG preserva la qualità lossless ed è ampiamente supportato su tutte le piattaforme.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Come scalare la grafica per una stampante?

Imposta il DPI del bitmap alla risoluzione della stampante di destinazione (ad esempio, 300 DPI) prima di disegnare. Questo ridimensiona automaticamente **scale graphics printer** l'output in modo che un pollice nel tuo codice corrisponda a un pollice sulla pagina stampata, mentre le dimensioni logiche del rettangolo rimangono inalterate. Dopo aver chiamato `bitmap.SetResolution(300, 300)`, lo stesso rettangolo apparirà più grande sulla carta ma manterrà le sue dimensioni esatte.

## Problemi comuni e soluzioni

| Problema | Perché succede | Soluzione |
|----------|----------------|-----------|
| **File di output non creato** | Percorso errato o cartella mancante | Assicurati che la directory di destinazione esista o chiama `Directory.CreateDirectory` prima di salvare. |
| **Il rettangolo appare distorto** | Unità `PageUnit` o DPI non corrispondenti | Verifica che `graphics.PageUnit` corrisponda all'unità desiderata e che il DPI del bitmap sia impostato correttamente (default 96 DPI, 300 DPI per stampa). |
| **Eccezione di licenza** | Esecuzione senza licenza valida in produzione | Applica la tua licenza temporanea o permanente di Aspose.Drawing prima di creare oggetti graphics. |

## Domande frequenti

**D: Posso usare Aspose.Drawing gratuitamente?**  
R: Sì, è disponibile una versione di prova gratuita [qui](https://releases.aspose.com/).

**D: Dove posso trovare la documentazione dettagliata per Aspose.Drawing?**  
R: Il riferimento completo dell'API si trova [qui](https://reference.aspose.com/drawing/net/).

**D: Come posso ottenere supporto per Aspose.Drawing?**  
R: Visita il [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) per aiuto della community e assistenza ufficiale.

**D: È disponibile una licenza temporanea per Aspose.Drawing?**  
R: Assolutamente—ottieni una [qui](https://purchase.aspose.com/temporary-license/).

**D: Dove posso acquistare una licenza completa di Aspose.Drawing?**  
R: Puoi acquistarla [qui](https://purchase.aspose.com/buy).

## Conclusione

Ora sai **come disegnare un rettangolo** grafico con trasformazione a livello di pagina usando Aspose.Drawing per .NET. Impostando l'unità di pagina su pollici, cancellando lo sfondo della tela e salvando il risultato come PNG, ottieni un output preciso e indipendente dal dispositivo, adatto sia alla visualizzazione su schermo sia alla stampa ad alta risoluzione. Sperimenta con altre unità, rotazioni o origini di coordinate personalizzate per sbloccare scenari di disegno ancora più potenti.

---

**Ultimo aggiornamento:** 2026-11-04  
**Testato con:** Aspose.Drawing 24.12 per .NET  
**Autore:** Aspose

## Tutorial correlati

- [Come impostare l'unità in Aspose.Drawing per .NET – Unità di misura](/drawing/net/coordinate-transformations/units-of-measure/)
- [Trasformazione globale](/drawing/net/coordinate-transformations/global-transformation/)
- [Trasformazione passo passo – Trasformazioni di coordinate](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}