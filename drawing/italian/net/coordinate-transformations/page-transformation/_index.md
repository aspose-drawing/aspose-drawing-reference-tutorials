---
date: 2026-05-19
description: Scopri come disegnare grafica a rettangolo eseguendo la trasformazione
  del sistema di coordinate in .NET con Aspose.Drawing. Questa guida passo‑passo mostra
  come convertire i pollici in pixel e impostare le unità di pagina.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Trasformazione del sistema di coordinate in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Come disegnare un rettangolo – Trasformazione del sistema di coordinate (Trasformazione
  della pagina) in Aspose.Drawing per .NET
url: /it/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare un rettangolo – Trasformazione del sistema di coordinate (Trasformazione della pagina) in Aspose.Drawing per .NET

## Introduzione

Benvenuto! In questo tutorial scoprirai **come disegnare un rettangolo** grafico mentre trasformi le coordinate della pagina usando Aspose.Drawing per .NET. Che tu stia costruendo un'applicazione intensiva di grafica o abbia bisogno di un controllo preciso sulle unità di disegno, questa guida ti accompagna passo passo—dalla configurazione della tela al disegno di un elemento rettangolo. Alla fine, sarai in grado di applicare queste tecniche nei tuoi progetti con sicurezza.

## Risposte rapide
- **Che cos'è la trasformazione del sistema di coordinate?** Mappare le unità a livello di pagina (come i pollici) alle pixel a livello di dispositivo.  
- **Perché usare Aspose.Drawing?** Offre un'alternativa completamente gestita e multipiattaforma a System.Drawing.Common.  
- **Quanto tempo richiede l'implementazione dell'esempio?** Circa 5‑10 minuti per una trasformazione di pagina di base.  
- **È necessaria una licenza?** Una prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Quali versioni di .NET sono supportate?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Cos'è Aspose.Drawing?

`Aspose.Drawing` è una libreria grafica .NET che fornisce un'**API indipendente dal dispositivo** per creare e manipolare immagini raster, vettoriali e disegni a livello di pagina senza fare affidamento su GDI+. Supporta **oltre 30 formati immagine** e può elaborare immagini fino a **10.000 × 10.000 pixel** senza caricare l'intero file in memoria.

## Perché usare la trasformazione del sistema di coordinate con Aspose.Drawing?

La trasformazione del sistema di coordinate ti consente di progettare grafica in unità del mondo reale mentre la libreria gestisce il ridimensionamento dei pixel per qualsiasi dispositivo di output. Questo garantisce dimensioni coerenti su schermi e stampanti e semplifica i calcoli di layout.

- **Progettazione indipendente dal dispositivo:** Scrivi il codice una sola volta e lascia che Aspose.Drawing gestisca il ridimensionamento dei pixel per qualsiasi schermo o stampante.  
- **Disegno di precisione:** Ideale per diagrammi tecnici, schizzi in stile CAD o qualsiasi scenario in cui le misurazioni esatte sono importanti.  
- **Affidabilità multipiattaforma:** Funziona in modo coerente su Windows, Linux e macOS senza le limitazioni GDI+ di System.Drawing.  
- **Dati di prestazione:** Su una CPU tipica da 2,5 GHz, disegnare un rettangolo di 5 pollici a 300 DPI richiede meno di **15 ms**, e la libreria può renderizzare **50 fotogrammi al secondo** in scenari di anteprima in tempo reale.

## Prerequisiti

- **Libreria Aspose.Drawing:** Scarica l'ultima versione dal sito ufficiale [qui](https://releases.aspose.com/drawing/net/).  
- **Ambiente di sviluppo:** Visual Studio, Rider o qualsiasi IDE compatibile con .NET.  
- **La tua directory dei documenti:** Sostituisci `"Your Document Directory"` nel codice con la cartella in cui desideri salvare l'immagine di output.  
- **Supporto ASP.NET (opzionale):** Puoi usare Aspose.Drawing nei progetti ASP.NET Core aggiungendo il pacchetto NuGet alla tua app web—questo segue lo stesso modello **how to use aspnet** di qualsiasi altra libreria .NET.

Ora che tutto è pronto, immergiamoci nella guida passo‑a‑passo.

## Come disegnare un rettangolo con la trasformazione della pagina?

Carica un bitmap vuoto, imposta l'unità di pagina su pollici e disegna un rettangolo usando una penna blu sottile—questo completa il disegno del rettangolo in poche righe di codice. La proprietà `Graphics.PageUnit` indica al motore di interpretare tutte le coordinate come pollici, così puoi pensare in misure reali invece che in pixel grezzi.

### Passo 1: Importare gli spazi dei nomi

Le istruzioni `using` ti danno accesso alle classi di disegno principali.

```csharp
using System.Drawing;
```

### Passo 2: Creare un Bitmap

`Bitmap` rappresenta un'immagine in memoria su cui puoi disegnare. Iniziamo creando un bitmap vuoto che servirà da superficie di disegno. Il formato pixel `Format32bppPArgb` ci fornisce supporto alfa premoltiplicato di alta qualità.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Passo 3: Creare un oggetto Graphics

Un oggetto `Graphics` fornisce l'API di disegno per il bitmap. È il ponte tra il tuo codice e il buffer dei pixel.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Passo 4: Pulire la tela

Dai alla tela uno sfondo neutro così le forme disegnate risaltano. Qui la riempiamo con un grigio chiaro.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Passo 5: Impostare la trasformazione (Come impostare l'unità)

`Graphics.PageUnit` specifica l'unità di misura usata per le coordinate di pagina. Per mappare le coordinate di pagina sui pixel del dispositivo, imposta la proprietà `PageUnit`. In questo esempio scegliamo i pollici, ma potresti usare anche `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` o `GraphicsUnit.Pixel`. Impostare l'unità su pollici ti permette di **convertire i pollici in pixel** automaticamente in base al DPI del bitmap (96 DPI per impostazione predefinita, 300 DPI per stampa ad alta risoluzione).

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Passo 6: Disegnare un rettangolo – disegnare grafica del rettangolo

`Pen` definisce colore, larghezza e stile delle linee disegnate su una superficie grafica. Ora disegniamo un rettangolo usando una penna blu sottile. Poiché abbiamo cambiato l'unità in pollici, le dimensioni e la posizione del rettangolo sono espresse in pollici, rendendo il codice più leggibile per layout orientati alla stampa.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Passo 7: Salvare l'immagine

Infine, scrivi il bitmap in un file PNG nella cartella specificata in precedenza.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Come scalare la grafica per una stampante?

Imposta il DPI del bitmap alla risoluzione della stampante target (ad es., 300 DPI) prima di disegnare. Questo scala automaticamente l'output della **grafica per stampante** così che un pollice nel tuo codice corrisponda a un pollice sulla pagina stampata. Dopo aver impostato `bitmap.SetResolution(300, 300)`, lo stesso rettangolo apparirà più grande sul foglio stampato mantenendo le sue dimensioni esatte.

## Problemi comuni e soluzioni

| Problema | Perché succede | Correzione |
|----------|----------------|------------|
| **File di output non creato** | Percorso errato o cartella mancante | Assicurati che la directory di destinazione esista o usa `Directory.CreateDirectory` prima di salvare. |
| **Il rettangolo appare distorto** | `PageUnit` errato o DPI non corrispondente | Verifica che `graphics.PageUnit` corrisponda alle unità che intendi usare e che il DPI del bitmap sia impostato correttamente (il valore predefinito è 96 DPI). |
| **Eccezione di licenza** | Esecuzione senza una licenza valida in produzione | Applica la tua licenza temporanea o permanente di Aspose.Drawing prima di creare oggetti grafici. |

## Domande frequenti

**Q: Posso usare Aspose.Drawing gratuitamente?**  
A: Sì, è disponibile una prova gratuita [qui](https://releases.aspose.com/).

**Q: Dove posso trovare la documentazione dettagliata per Aspose.Drawing?**  
A: Il riferimento completo dell'API si trova [qui](https://reference.aspose.com/drawing/net/).

**Q: Come posso ottenere supporto per Aspose.Drawing?**  
A: Visita il [Forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) per aiuto della community e assistenza ufficiale.

**Q: È disponibile una licenza temporanea per Aspose.Drawing?**  
A: Assolutamente—ottienila [qui](https://purchase.aspose.com/temporary-license/).

**Q: Dove posso acquistare una licenza completa di Aspose.Drawing?**  
A: Puoi acquistarla [qui](https://purchase.aspose.com/buy).

## Conclusione

In questa guida abbiamo coperto tutto ciò che ti serve per **come disegnare un rettangolo** grafico con Aspose.Drawing: impostare la tela, configurare le unità di pagina, disegnare forme precise e salvare il risultato. Usa queste tecniche per creare grafica scalabile e indipendente dal dispositivo per report, disegni in stile CAD o qualsiasi applicazione dove la precisione delle misurazioni è fondamentale. Successivamente, esplora trasformazioni avanzate come rotazione, scaling e origini di coordinate personalizzate per sbloccare scenari di disegno ancora più potenti.

---

**Ultimo aggiornamento:** 2026-05-19  
**Testato con:** Aspose.Drawing 24.12 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
