---
date: 2026-07-17
description: Scopri come prevenire il traboccamento del testo impostando l'allineamento
  del testo in Aspose.Drawing for .NET e aggiungere testo alle immagini. Guida passo‑passo
  con esempi.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Imposta l'allineamento del testo con Aspose.Drawing for .NET
og_description: Previeni il traboccamento del testo impostando l'allineamento del
  testo in Aspose.Drawing for .NET. Scopri come draw string su un'immagine, center
  text in rectangle e sostituire System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Prevenire il traboccamento del testo – Impostare l'allineamento del testo
  con Aspose.Drawing for .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Prevenire il traboccamento del testo – Impostare l'allineamento del testo con
  Aspose.Drawing for .NET
url: /it/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Prevenire il traboccamento del testo – Impostare l'allineamento del testo con Aspose.Drawing

## Introduzione

Quando è necessario **prevenire il traboccamento del testo** durante il rendering di grafica in .NET, Aspose.Drawing offre un controllo dettagliato sul posizionamento, l'allineamento e il wrapping del testo. Che tu stia creando un generatore di badge, un report dinamico o qualsiasi output basato su immagine, padroneggiare l'allineamento del testo garantisce che il tuo testo rimanga all'interno del rettangolo previsto e abbia un aspetto curato. In questa guida vedremo come creare una canvas bitmap, configurare `StringFormat`, disegnare un rettangolo con testo centrato, gestire il traboccamento e infine salvare l'immagine.

## Risposte rapide
- **Che cosa significa “impostare l'allineamento del testo”?** Definisce come il testo è posizionato orizzontalmente e verticalmente all'interno di un rettangolo di disegno.  
- **Quale classe controlla l'allineamento?** `StringFormat` consente di impostare `Alignment` e `LineAlignment`.  
- **Posso disegnare una stringa e un rettangolo insieme?** Sì—usa `Graphics.DrawRectangle` seguito da `Graphics.DrawString`.  
- **Come prevenire il traboccamento del testo?** Regola la dimensione del rettangolo o suddividi manualmente il testo in più righe.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale di Aspose.Drawing per l'uso non‑valutativo.

## Che cos'è **impostare l'allineamento del testo** in Aspose.Drawing?

`impostare l'allineamento del testo` configura il posizionamento orizzontale (`StringAlignment`) e verticale (`LineAlignment`) del testo all'interno di un `Rectangle` o di una regione di disegno. Regolando queste proprietà controlli se il testo appare allineato a sinistra, centrato, allineato a destra, in alto, al centro o in basso, consentendo layout precisi in grafica, badge e report generati con Aspose.Drawing.

## Perché usare Aspose.Drawing per l'allineamento del testo?

Aspose.Drawing elimina le limitazioni di GDI+ che affliggono `System.Drawing.Common`. Supporta **5 principali runtime .NET** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 e .NET 7 – e può renderizzare immagini fino a **4000 × 4000 px** (≈ 100 MB) senza esaurire la memoria. Anti‑aliasing, scaling ad alta DPI e piena compatibilità con container Linux ti permettono di generare grafica pixel‑perfect in qualsiasi scenario di distribuzione.

## Prerequisiti

1. **Libreria Aspose.Drawing** – scaricala [qui](https://releases.aspose.com/drawing/net/).  
2. **Ambiente di sviluppo** – Visual Studio 2022 (o qualsiasi IDE C#).  
3. **Conoscenze di base di .NET** – dovresti sentirti a tuo agio con progetti C# e pacchetti NuGet.

## Importare gli spazi dei nomi

Per iniziare, porta gli spazi dei nomi necessari nello scope. Questi ti danno accesso a grafica, rendering del testo e primitive di disegno.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Come prevenire il traboccamento del testo con Aspose.Drawing?

`Bitmap` è una classe che rappresenta un'immagine memorizzata in memoria, mentre `RectangleF` definisce un'area rettangolare a virgola mobile per il disegno. Utilizzando un `StringFormat` con `Trimming` impostato su `StringTrimming.EllipsisCharacter`, i caratteri in eccesso vengono automaticamente sostituiti da un'ellissi, garantendo che il testo non superi i limiti del rettangolo. Misurare la stringa prima ti permette di decidere se ridurre il rettangolo o suddividere il testo in più righe, assicurando un layout pulito senza fuoriuscite.

Carica il tuo bitmap, definisci un `RectangleF` di dimensioni adeguate e usa un `StringFormat` con `Trimming` impostato su `StringTrimming.EllipsisCharacter` per tagliare automaticamente i caratteri in eccesso. Per un controllo totale, misura la stringa con `Graphics.MeasureString` e riduci il rettangolo o suddividi il testo in righe prima del disegno. Questo approccio garantisce che nessun carattere fuoriesca dai limiti visivi.

## Passo 1: Creare oggetti Bitmap e Graphics  

`Bitmap` rappresenta un'immagine in memoria, mentre `Graphics` fornisce i metodi di disegno per quella bitmap. Creare una bitmap fornisce una canvas su cui disegnare. L'oggetto `Graphics` è la superficie di disegno e abilitiamo il rendering di testo ad alta qualità con `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Passo 2: Definire **StringFormat** e lo stile  

`StringFormat` specifica le opzioni di layout del testo come allineamento, interlinea e trimming. Qui **impostiamo l'allineamento del testo** configurando un'istanza di `StringFormat`. Prepariamo anche pennelli, penne e un font che saranno usati durante il disegno della stringa.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Passo 3: Creare e formattare il testo – **come disegnare una stringa** e **disegnare un rettangolo con testo**

`Graphics.DrawString` rende il testo sulla canvas, e `Graphics.DrawRectangle` disegna una forma rettangolare. Compiliamo il testo, definiamo il rettangolo che lo conterrà e poi disegniamo sia il bordo del rettangolo sia la stringa stessa.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Come gestire il traboccamento del testo

Se il `text` fornito supera i limiti del rettangolo, hai due opzioni comuni:

1. **Ridimensionare il rettangolo** – aumenta `rectangle.Width` o `rectangle.Height`.  
2. **Suddividere il testo** – spezza la stringa in righe che entrano, poi chiama `DrawString` per ogni riga con coordinate Y aggiustate.

## Come disegnare una stringa su un'immagine usando Aspose.Drawing?

`Graphics.DrawString` disegna il testo specificato usando un font e opzioni di formattazione. Istanzia un oggetto `Graphics` dalla tua bitmap, poi chiama `DrawString` con il `StringFormat` preparato. Questa chiamata singola rende il testo esattamente dove lo desideri, rispettando allineamento, trimming e qualsiasi matrice di trasformazione applicata. Aggiungere un hint di rendering di alta qualità assicura che l'output rimanga nitido su display ad alta DPI.

## Come centrare il testo in un rettangolo?

`StringAlignment` determina l'allineamento orizzontale del testo all'interno di un rettangolo di layout. Imposta `stringFormat.Alignment = StringAlignment.Center` e `stringFormat.LineAlignment = StringAlignment.Center`. Questo centra il testo orizzontalmente e verticalmente dentro il rettangolo, rendendolo ideale per badge, pulsanti o sovrapposizioni di etichette. Il posizionamento centrato funziona in modo coerente su diverse dimensioni di immagine e impostazioni DPI, fornendo un aspetto visivo equilibrato.

## Come ottenere l'allineamento verticale del testo?

`LineAlignment` controlla il posizionamento verticale del testo dentro il rettangolo. Usa `stringFormat.LineAlignment` con i valori `StringAlignment.Near`, `Center` o `Far` per posizionare il testo rispettivamente in alto, al centro o in basso del rettangolo. Combina questo con `Graphics.TranslateTransform` se devi ruotare il testo mantenendo l'allineamento verticale. Regolare l'allineamento di linea assicura che blocchi di testo multilinea si allineino esattamente dove ti aspetti, anche dopo trasformazioni.

## Passo 4: Salvare l'output – **aggiungere testo all'immagine**

Infine, scrivi la bitmap su disco. Questo passo dimostra **aggiungere testo all'immagine** in una singola chiamata.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **Il testo appare sfocato** | Assicurati che `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` sia impostato. |
| **Il testo è tagliato** | Aumenta le dimensioni del rettangolo o abilita la logica di word‑wrap misurando la dimensione della stringa (`Graphics.MeasureString`). |
| **Font non trovato** | Verifica che il font sia installato sulla macchina host o incorpora un font privato usando `PrivateFontCollection`. |
| **Colori inaspettati** | Ricontrolla i colori di pennello e penna; ricorda che `Color.FromKnownColor` utilizza colori definiti dal sistema. |

## Domande frequenti

**Q1: Aspose.Drawing è compatibile con tutte le versioni .NET?**  
A1: Sì, Aspose.Drawing è progettato per essere compatibile con un'ampia gamma di versioni .NET, garantendo flessibilità agli sviluppatori.

**Q2: Posso personalizzare ulteriormente lo stile del font?**  
A2: Assolutamente! Regola i parametri dell'oggetto `Font` per ottenere la dimensione, lo stile e la famiglia desiderati.

**Q3: Come posso gestire il traboccamento del testo all'interno del rettangolo definito?**  
A3: Puoi gestire il traboccamento regolando le dimensioni del rettangolo o implementando una logica personalizzata per gestire testi lunghi.

**Q4: Ci sono altre opzioni di formattazione disponibili in Aspose.Drawing?**  
A4: Sì, Aspose.Drawing fornisce un set completo di strumenti per la manipolazione grafica, incluse varie opzioni di formattazione per testo, forme e altro.

**Q5: Dove posso trovare supporto aggiuntivo per Aspose.Drawing?**  
A5: Esplora il forum di Aspose.Drawing [qui](https://forum.aspose.com/c/drawing/44) per supporto della community e discussioni.

**Domande aggiuntive**

**Q: Come disegno una stringa senza un rettangolo circostante?**  
A: Ometti la chiamata `DrawRectangle` e passa la posizione `PointF` desiderata a `Graphics.DrawString`.

**Q: Posso ruotare il testo mantenendo l'allineamento?**  
A: Sì—applica una trasformazione `Matrix` all'oggetto `Graphics` prima del disegno, poi reimposta la trasformazione successivamente.

**Q: È possibile esportare l'immagine come JPEG invece di PNG?**  
A: Cambia semplicemente l'estensione del file in `bitmap.Save` e, se necessario, specifica `ImageFormat.Jpeg`.

---

**Ultimo aggiornamento:** 2026-07-17  
**Testato con:** Aspose.Drawing 24.11 per .NET  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Come disegnare testo con Aspose.Drawing per .NET](/drawing/net/text-and-fonts/draw-text/)
- [Aggiungere testo su immagini in Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [Come disegnare testo e font con Aspose.Drawing per .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}