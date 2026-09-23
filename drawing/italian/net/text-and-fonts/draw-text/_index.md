---
date: 2026-09-23
description: Scopri come disegnare testo su un'immagine usando Aspose.Drawing per
  .NET. Genera un'immagine con testo, aggiungi testo a un bitmap e salva il bitmap
  come PNG con font personalizzati.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Come disegnare testo con Aspose.Drawing
og_description: Scopri come disegnare testo su un'immagine usando Aspose.Drawing per
  .NET. Questo tutorial ti mostra come generare un'immagine con testo, aggiungere
  testo a un bitmap e salvare il bitmap come PNG con font personalizzati.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Disegna testo su immagine con Aspose.Drawing per .NET – Guida rapida
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Come disegnare testo su immagine con Aspose.Drawing per .NET
url: /it/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare testo su immagine con Aspose.Drawing per .NET

## Introduzione

In questa guida passo‑a‑passo imparerai **come disegnare testo su immagine** usando Aspose.Drawing per .NET. Che tu abbia bisogno di creare un *immagine di testo dinamico*, aggiungere testo a un bitmap esistente, o generare una grafica con font personalizzati, questo tutorial ti accompagna in ogni dettaglio così potrai iniziare a disegnare testo in pochi minuti. La libreria supporta oltre 30 metodi GDI+, funziona su Windows, Linux e macOS, e ha **zero dipendenze esterne**, rendendola una scelta affidabile per la generazione di immagini lato server.

## Risposte rapide
- **Quale libreria è usata?** Aspose.Drawing per .NET  
- **Compito principale?** Disegnare testo su un'immagine (creare immagine con testo)  
- **Metodo chiave?** `Graphics.DrawString` (disegnare stringa su immagine)  
- **Formato di output?** PNG (salvare bitmap come PNG)  
- **Prerequisiti?** ambiente di sviluppo .NET e libreria Aspose.Drawing  

## Cos'è disegnare testo con Aspose.Drawing?

Disegnare testo con Aspose.Drawing significa usare l'API compatibile GDI+ della libreria per renderizzare stringhe Unicode su una tela raster. Il metodo `Graphics.DrawString` scrive il testo in un bitmap, consentendoti di controllare font, colore, allineamento e anti‑aliasing. Questo approccio ti permette di generare immagini ad alta qualità senza installare System.Drawing.Common.

## Perché usare Aspose.Drawing per aggiungere testo alle immagini?

Aspose.Drawing offre un modo affidabile e cross‑platform per renderizzare testo su immagini senza necessità di librerie GDI+ native, garantendo qualità e prestazioni costanti su qualsiasi sistema operativo. Supporta anti‑aliasing avanzato, caratteri Unicode e font personalizzati, e si integra perfettamente con le applicazioni .NET, rendendola ideale per la generazione di immagini lato server e per strumenti desktop.

- **Affidabilità cross‑platform** – funziona su Windows, Linux e macOS.  
- **Rendering avanzato** – anti‑aliasing e smoothing del testo sub‑pixel per un output nitido.  
- **Nessuna dipendenza esterna** – la libreria include tutto il necessario per *creare immagine con testo*.

## Prerequisiti

Prima di immergerti, assicurati di avere:

- **Aspose.Drawing per .NET** – scaricala dalla [documentazione di Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **Un IDE .NET** come Visual Studio o VS Code.  

## Importare i namespace

Inizia importando i namespace richiesti:

Questi namespace forniscono i tipi core GDI+ come `Bitmap`, `Graphics` e le utility di rendering del testo.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Passo 1: creare oggetti bitmap e graphics

`Bitmap` è il contenitore di immagine raster di Aspose.Drawing per i dati pixel, e `Graphics` fornisce metodi di disegno per renderizzare forme e testo su di esso.

`Bitmap` rappresenta un'immagine in memoria, mentre `Graphics` fornisce metodi di disegno per renderizzare su quel bitmap.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Qui creiamo un `Bitmap` che conterrà l'immagine finale e un oggetto `Graphics` che ci permette di disegnarci sopra. L'indicazione di anti‑aliasing garantisce che il testo appaia liscio.

## Passo 2: impostare brush, pen e font

`Brush` definisce il colore di riempimento, `Pen` delinea le forme, e `Font` specifica il tipo di carattere, la dimensione e lo stile per il rendering del testo.

`Brush` riempie le forme con colore, `Pen` delinea le forme, e `Font` definisce il tipo di carattere e la dimensione per il rendering del testo.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** definisce il colore del testo.  
- **Pen** viene usato più tardi per disegnare un rettangolo attorno al testo (opzionale).  
- **Font** specifica il tipo di carattere, la dimensione e lo stile per l'operazione di *disegnare stringa su immagine*.

## Passo 3: definire testo e rettangolo

`Rectangle` definisce il riquadro di delimitazione dove verrà posizionato il testo, specificando le coordinate X/Y e larghezza/altezza.

`Rectangle` specifica la posizione e la dimensione di un'area rettangolare, usata qui per delimitare il testo disegnato.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

Il `Rectangle` determina dove verrà posizionato il testo. Regola le coordinate e le dimensioni per adattarle al tuo layout.

## Passo 4: disegnare rettangolo e testo

`Graphics.DrawString` renderizza il testo specificato all'interno del rettangolo fornito usando il font e il brush indicati.

`Graphics.DrawString` renderizza una stringa di testo all'interno di un rettangolo specificato usando il font e il brush forniti.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Prima delineiamo l'area con un rettangolo blu, poi **aggiungiamo testo al bitmap** chiamando `DrawString`. Questo è il fulcro del *disegnare testo* sull'immagine.

## Passo 5: salvare il risultato

L'immagine viene salvata come file PNG, soddisfacendo il requisito di *salvare bitmap come PNG*. Sostituisci il percorso segnaposto con la cartella reale dove desideri memorizzare il file.

`bitmap.Save` scrive l'immagine su un file nel formato scelto, ad esempio PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Casi d'uso comuni

- **Generare certificati** con nomi personalizzati.  
- **Creare miniature con filigrana** per gallerie web.  
- **Costruire grafici dinamici** che includono etichette o annotazioni.  

## Risoluzione dei problemi e consigli

- **Font non trovato?** Assicurati che il font sia installato sulla macchina host o usa una collezione di font privata.  
- **Testo troncato?** Aumenta le dimensioni del rettangolo o riduci la dimensione del font.  
- **Problemi di prestazioni?** Riutilizza lo stesso oggetto `Graphics` per più operazioni di disegno quando possibile.  

## Domande frequenti

**D: Come cambio il formato di output in JPEG?**  
R: Sostituisci l'estensione `.png` con `.jpg` nel metodo `Save` e opzionalmente specifica un `ImageCodecInfo` per la qualità JPEG.

**D: Posso disegnare testo multilinea?**  
R: Sì, includi caratteri di interruzione di riga (`\n`) nella stringa o usa `StringFormat` con `FormatFlags.LineLimit`.

**D: C'è un modo per misurare la dimensione del testo prima di disegnarlo?**  
R: Usa `Graphics.MeasureString` per ottenere le dimensioni esatte del testo renderizzato.

**D: Aspose.Drawing supporta i caratteri Unicode?**  
R: Assolutamente. Fornisci un font che contenga i glifi richiesti e la libreria li renderizzerà correttamente.

**D: Quale versione di Aspose.Drawing è stata usata per i test?**  
R: Gli esempi sono stati testati con Aspose.Drawing 24.11 per .NET.

---

**Ultimo aggiornamento:** 2026-09-23  
**Testato con:** Aspose.Drawing 24.11 per .NET  
**Autore:** Aspose

## Tutorial correlati

- [Creare grafica bitmap C# – Salvare immagine PNG e lavorare con i font installati in Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Come salvare un bitmap come PNG usando l'API Aspose.Drawing per .NET](/drawing/net/image-editing/display/)
- [Testo su immagine](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}