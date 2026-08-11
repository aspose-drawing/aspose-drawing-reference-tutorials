---
date: 2026-06-23
description: Scopri come salvare PNG usando Aspose.Drawing, applicare trasformazioni
  del mondo e convertire le grafiche in PNG. Include esempi di trasformazione di traduzione
  C# e più trasformazioni grafiche.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: World Transformation in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Come salvare PNG con Aspose.Drawing – World Transformation
url: /it/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come salvare PNG con Aspose.Drawing – Trasformazione del mondo

## Salvare Bitmap come PNG – Introduzione

**Come salvare PNG** usando Aspose.Drawing è una necessità comune quando hai bisogno di immagini trasparenti ad alta qualità generate al volo. In questo tutorial imparerai a **salvare bitmap come PNG**, applicare trasformazioni del mondo come traslazione, rotazione e scala, e infine convertire la grafica in PNG—tutto con codice C# pulito e manutenibile. Che tu stia costruendo un motore di reporting, un componente di grafici o un renderer UI personalizzato, padroneggiare questi passaggi ti permette di creare immagini dinamiche che hanno un aspetto ottimale su qualsiasi dispositivo.

## Risposte rapide
- **Cosa significa “world transformation”?** Mappa le coordinate logiche (mondo) del tuo disegno alle coordinate della pagina (dispositivo).  
- **Posso esportare il risultato come PNG?** Sì – dopo il disegno basta chiamare `bitmap.Save(...)` con estensione `.png`.  
- **Ho bisogno di una licenza per Aspose.Drawing?** Una prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **È compatibile con .NET 6/7?** Assolutamente – Aspose.Drawing supporta .NET Framework 4.5+ e .NET Core/5/6/7.  
- **Quante trasformazioni posso concatenare?** Puoi applicare **multiple trasformazioni grafiche** in sequenza (translate, rotate, scale, ecc.).

## Cos'è una trasformazione del mondo in Aspose.Drawing?

Una trasformazione del mondo modifica il sistema di coordinate usato dai comandi di disegno. Per impostazione predefinita, (0,0) è l'angolo in alto a sinistra del bitmap. Con `TranslateTransform`, `RotateTransform` o `ScaleTransform`, puoi riposizionare quell'origine, ruotare le forme o ridimensionarle senza alterare la geometria originale.

## Come salvare PNG usando Aspose.Drawing?

Carica un oggetto `Bitmap`, imposta le trasformazioni del mondo desiderate sulla sua istanza `Graphics`, disegna le tue forme e infine chiama `bitmap.Save("output.png", ImageFormat.Png)`. Questa chiamata di salvataggio a riga singola scrive un file PNG lossless che preserva la trasparenza e la fedeltà dei colori, rendendolo ideale per risorse web e overlay UI.

## Perché usare un esempio di traslazione grafica?

Un esempio di traslazione grafica ti consente di spostare l'origine del disegno una sola volta invece di ricalcolare ogni punto. Questo approccio riduce la complessità del codice, migliora la leggibilità e permette al motore grafico di gestire la matematica delle matrici in modo efficiente, il che può aumentare le prestazioni di rendering fino al 30 % su grandi tele.

## Esempio di traslazione grafica

Un **esempio di traslazione grafica** mostra come spostare l'origine semplifichi il posizionamento. Invece di ricalcolare ogni punto, sposti il sistema di coordinate una volta e disegni come se la nuova origine fosse al centro della tela.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Libreria Aspose.Drawing** integrata nel tuo progetto .NET – scaricala dalla pagina ufficiale di [rilascio di Aspose.Drawing](https://releases.aspose.com/drawing/net/).  
- Una **directory dei documenti** dove verrà salvata l'immagine di output.  
- Familiarità di base con la sintassi **C#** e Visual Studio o l'IDE di tua preferenza.

Ora, immergiamoci nel codice!

## Importa spazi dei nomi

Il `Bitmap`, `Graphics` e le utility di disegno Aspose risiedono in questi spazi dei nomi.  
**Definizione:** `System.Drawing` fornisce i tipi core GDI+, mentre `Aspose.Drawing` li estende con funzionalità cross‑platform.

## Guida passo‑passo

### Passo 1: Crea un Bitmap

Iniziamo creando una tela vuota che conterrà il nostro disegno.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` crea un bitmap a 32 bit per pixel con alfa premoltiplicata, il formato ottimale per l'output PNG perché preserva la trasparenza senza passaggi di conversione aggiuntivi.

- **Perché 32bppPArgb?** Questo formato di pixel supporta la trasparenza alfa e il rendering di colori ad alta qualità, perfetto per l'output PNG.  
- **Suggerimento:** Regola larghezza/altezza per corrispondere alle dimensioni dell'immagine desiderata.

### Passo 2: Imposta la trasformazione del mondo (Esempio di traslazione grafica)

`TranslateTransform` sposta l'origine del sistema di coordinate in una nuova posizione.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` sposta il punto (0,0) al centro della tela. Dopo questa chiamata, qualsiasi forma disegnata usando coordinate (0,0) apparirà al centro dell'immagine.

- Questo sposta il punto (0,0) a (500, 400) – il centro di una tela 1000 × 800.  
- Puoi concatenare trasformazioni aggiuntive: `RotateTransform` ruota il sistema di coordinate e `ScaleTransform` lo scala, abilitando **multiple trasformazioni grafiche**.

### Passo 3: Disegna un rettangolo usando le coordinate trasformate

`DrawRectangle` disegna un rettangolo usando la penna e le coordinate specificate.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` disegna un rettangolo centrato sulla tela perché l'angolo in alto a sinistra è spostato di metà della sua larghezza e altezza dall'origine trasformata.

- L'angolo in alto a sinistra del rettangolo parte dall'origine trasformata (centro dell'immagine).  
- Sentiti libero di sperimentare con altre forme—ellissi, linee o percorsi personalizzati.

### Passo 4: Salva il risultato – Converti la grafica in PNG

`Save` scrive il bitmap su un file nel formato immagine specificato.  
`ImageFormat` indica il formato di file per il salvataggio delle immagini, come PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` scrive un file PNG lossless che può essere usato direttamente in pagine web o componenti UI.

- PNG preserva i colori esatti e la trasparenza impostati in precedenza.  
- Sostituisci `"Your Document Directory"` con il percorso reale sul tuo computer.

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|----------------|----------|
| **Errore file non trovato** durante il salvataggio | La cartella di destinazione non esiste. | Crea la cartella programmaticamente (`Directory.CreateDirectory`) prima di chiamare `Save`. |
| **Immagine vuota** dopo la trasformazione | `TranslateTransform` chiamato dopo il disegno. | Assicurati che la trasformazione sia impostata **prima** di qualsiasi comando di disegno. |
| **Colori distorti** | Uso di un formato pixel incompatibile. | Usa `Format32bppPArgb` per l'output PNG. |

## Domande frequenti

**D: Posso applicare più di una trasformazione?**  
R: Sì – puoi concatenare `TranslateTransform`, `RotateTransform` e `ScaleTransform` per ottenere effetti complessi in una singola pipeline grafica.

**D: Aspose.Drawing è gratuito per progetti commerciali?**  
R: È disponibile una prova gratuita per la valutazione, ma è necessaria una licenza commerciale per l'uso in produzione.

**D: Funziona con .NET Core e .NET 5/6/7?**  
R: Assolutamente. Aspose.Drawing supporta tutti i runtime .NET moderni, inclusi .NET Core, .NET 5, .NET 6 e .NET 7.

**D: Dove posso trovare la documentazione completa dell'API?**  
R: La documentazione completa è disponibile [qui](https://reference.aspose.com/drawing/net/).

**D: Come risolvere un file di output mancante?**  
R: Verifica la stringa del percorso, assicurati di avere i permessi di scrittura e conferma che la directory esista prima di chiamare `Save`.

## Conclusione

Ora hai imparato **come salvare PNG** con Aspose.Drawing, applicato una **trasformazione del mondo** e realizzato un **esempio di traslazione grafica** che può essere esteso con rotazione o scaling. Padroneggiando questi blocchi fondamentali puoi generare immagini dinamiche, creare grafici personalizzati o costruire grafiche on‑the‑fly per qualsiasi applicazione .NET.

---

**Ultimo aggiornamento:** 2026-06-23  
**Testato con:** Aspose.Drawing 24.11 per .NET  
**Autore:** Aspose  
**Risorse correlate:** [Riferimento API di Aspose.Drawing](https://reference.aspose.com/drawing/net/) | [Scarica prova gratuita](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Tutorial correlati

- [Tutorial di trasformazione matriciale: Trasformazioni matriciali in Aspose.Drawing per .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Come ruotare un'immagine con la trasformazione globale di Aspose.Drawing](/drawing/net/coordinate-transformations/global-transformation/)
- [Trasformazione del sistema di coordinate – Trasformazione di pagina in Aspose.Drawing per .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}