---
date: 2026-02-25
description: Scopri come disegnare testo e creare immagini di testo dinamiche usando
  Aspose.Drawing per .NET. Questa guida passo passo ti mostra come aggiungere testo
  a un bitmap, disegnare una stringa sull'immagine e salvare il bitmap come PNG.
linktitle: How to Draw Text with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Come disegnare testo con Aspose.Drawing per .NET
url: /it/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare testo con Aspise.Drawing per .NET

## Introduzione

In questa guida passo‑a‑passo imparerai **come disegnare testo** sulle immagini usando Aspose.Drawing per .NET. Che tu abbia bisogno di creare un *immagine di testo dinamico*, aggiungere testo a un bitmap esistente, o generare una grafica con font personalizzati, questo tutorial ti accompagna in ogni dettaglio così potrai iniziare a disegnare testo in pochi minuti.

## Risposte rapide
- **Quale libreria è usata?** Aspose.Drawing for .NET  
- **Compito principale?** Draw text on an image (create image with text)  
- **Metodo chiave?** `Graphics.DrawString` (draw string on image)  
- **Formato di output?** PNG (save bitmap as PNG)  
- **Prerequisiti?** .NET development environment and Aspose.Drawing library  

## Che cosa è disegnare testo con Aspose.Drawing?
Aspose.Drawing fornisce un'API completamente gestita che rispecchia il modello classico GDI+ aggiungendo il supporto cross‑platform. Ti consente di renderizzare testo, forme e immagini di alta qualità senza fare affidamento su System.Drawing.Common.

## Perché usare Aspose.Drawing per aggiungere testo alle immagini?
- **Affidabilità cross‑platform** – funziona su Windows, Linux e macOS.  
- **Rendering avanzato** – anti‑aliasing e smoothing del testo sub‑pixel per un output nitido.  
- **Nessuna dipendenza esterna** – la libreria include tutto il necessario per *create image with text*.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Aspose.Drawing for .NET** – scaricalo dalla [documentazione di Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **Un IDE .NET** come Visual Studio o VS Code.  

## Importare gli spazi dei nomi

Inizia importando gli spazi dei nomi richiesti:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Passo 1: Creare oggetti Bitmap e Graphics

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Qui creiamo un `Bitmap` che conterrà l'immagine finale e un oggetto `Graphics` che ci permette di disegnare su di esso. L'indicazione di anti‑aliasing garantisce che il testo appaia liscio.

## Passo 2: Configurare Brush, Pen e Font

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** definisce il colore del testo.  
- **Pen** viene usato più tardi per disegnare un rettangolo attorno al testo (opzionale).  
- **Font** specifica il tipo di carattere, la dimensione e lo stile per l'operazione *draw string on image*.

## Passo 3: Definire testo e rettangolo

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

Il `Rectangle` determina dove verrà posizionato il testo. Regola le coordinate e le dimensioni per adattarle al tuo layout.

## Passo 4: Disegnare rettangolo e testo

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Prima delineiamo l'area con un rettangolo blu, poi **aggiungiamo testo al bitmap** chiamando `DrawString`. Questo è il cuore del *drawing text* sull'immagine.

## Passo 5: Salvare il risultato

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

L'immagine viene salvata come file PNG, soddisfacendo il requisito *save bitmap as PNG*. Sostituisci il percorso segnaposto con la cartella reale dove desideri memorizzare il file.

## Casi d'uso comuni

- **Generare certificati** con nomi personalizzati.  
- **Creare miniature con filigrana** per gallerie web.  
- **Costruire grafici dinamici** che includono etichette o annotazioni.  

## Risoluzione dei problemi e consigli

- **Font non trovato?** Assicurati che il font sia installato sulla macchina host o utilizza una collezione di font privata.  
- **Testo troncato?** Aumenta le dimensioni del rettangolo o riduci la dimensione del font.  
- **Preoccupazioni sulle prestazioni?** Riutilizza lo stesso oggetto `Graphics` per più operazioni di disegno quando possibile.

## FAQ's

### Q1: Posso usare font personalizzati con Aspose.Drawing per .NET?

A1: Sì, puoi specificare font personalizzati quando crei l'oggetto `Font` nel tuo codice.

### Q2: Come posso aggiungere effetti di testo come grassetto o corsivo?

A2: Modifica la proprietà `FontStyle` dell'oggetto `Font`. Ad esempio, usa `FontStyle.Bold` per il testo in grassetto.

### Q3: Aspose.Drawing è compatibile con .NET Core?

A3: Sì, Aspose.Drawing supporta .NET Core, consentendoti di usarlo in applicazioni cross‑platform.

### Q4: Posso disegnare testo su un'immagine esistente?

A4: Certamente! Carica l'immagine esistente usando `Bitmap.FromFile()` e poi procedi con i passaggi di disegno del testo.

### Q5: Esiste un forum della community per il supporto di Aspose.Drawing?

A5: Sì, puoi trovare supporto e discutere problemi sul [forum di Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

## Domande frequenti

**Q: Come cambio il formato di output in JPEG?**  
A: Sostituisci l'estensione `.png` con `.jpg` nel metodo `Save` e, opzionalmente, specifica un `ImageCodecInfo` per la qualità JPEG.

**Q: Posso disegnare testo multilinea?**  
A: Sì, includi i caratteri di interruzione di linea (`\n`) nella stringa o usa `StringFormat` con `FormatFlags.LineLimit`.

**Q: Esiste un modo per misurare la dimensione del testo prima di disegnarlo?**  
A: Usa `Graphics.MeasureString` per ottenere le dimensioni esatte del testo renderizzato.

**Q: Aspose.Drawing supporta i caratteri Unicode?**  
A: Assolutamente. Fornisci un font che contenga i glifi richiesti e la libreria li renderizzerà correttamente.

**Q: Quale versione di Aspose.Drawing è stata usata per i test?**  
A: Gli esempi sono stati testati con Aspose.Drawing 24.11 per .NET.

---

**Ultimo aggiornamento:** 2026-02-25  
**Testato con:** Aspose.Drawing 24.11 for .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}