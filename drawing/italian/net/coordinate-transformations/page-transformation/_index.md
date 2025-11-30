---
date: 2025-11-30
description: Scopri come applicare la trasformazione del sistema di coordinate, disegnare
  bitmap di rettangoli e trasformare le pagine usando Aspose.Drawing per .NET.
language: it
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Trasformazione del Sistema di Coordinate (Trasformazione della Pagina) in Aspose.Drawing
  per .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Trasformazione del Sistema di Coordinate (Trasformazione della Pagina) in Aspose.Drawing per .NET

## Introduction

Benvenuti! In questo tutorial scoprirete **come eseguire una trasformazione del sistema di coordinate** su una pagina usando Aspose.Drawing per .NET. Che dobbiate **disegnare oggetti bitmap rettangolari**, scalare i disegni o semplicemente mappare le unità di pagina a quelle del dispositivo, i passaggi seguenti vi guideranno attraverso l'intero processo—chiaro, conciso e pronto per il copia‑incolla nel vostro progetto.

## Quick Answers
- **Qual è la classe principale per il disegno?** `Graphics` da Aspose.Drawing.
- **Come impostare le unità di pagina?** Usa `graphics.PageUnit = GraphicsUnit.Inch;`.
- **Posso disegnare un rettangolo su una pagina trasformata?** Sì—crea un `Pen` e chiama `DrawRectangle`.
- **Dove viene salvato l'output?** Nella cartella che specificate in `bitmap.Save`.
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.Drawing per l'uso commerciale.

## What is coordinate system transformation?

Una **trasformazione del sistema di coordinate** cambia il modo in cui le coordinate logiche della pagina (come pollici o millimetri) vengonoate alle coordinate fisiche del dispositivo (pixel). Regolando la trasformazione, controllate la scala, la rotazione e la traslazione di tutte le operazioni di disegno, rendendo più semplice progettare grafica indipendente dalla risoluzione.

## Why use Aspose.Drawing for page transformations?

- **Compatibilità completa con .NET** – funziona con .NET Framework, .NET Core e .NET 5/6.
- **API grafica ricca** – offre la stessa funzionalità di System.Drawing.Common senza restrizioni di piattaforma.
- **Gestione semplice delle unità** – passate da pollici, millimetri, punti, ecc., con una singola proprietà.
- **Output ad alta qualità** – generate PNG, JPEG, BMP e altri formati con controllo preciso.

## Prerequisites

Prima di iniziare, assicuratevi di avere:

- **Libreria Aspose.Drawing** – scaricate l'ultima versione dal sito ufficiale [qui](https://releases.aspose.com/drawing/net/).
- **Ambiente di sviluppo** – Visual Studio (qualsiasi edizione) o un altro IDE .NET.
- **Accesso in scrittura** – una cartella sul vostro computer dove l'immagine trasformata sarà salvata (sostituite `"Your Document Directory"` nel codice con il percorso reale).

Ora che siamo pronti, procediamo passo passo.

## Import Namespaces

Prima, importate lo spazio dei nomi necessario:

```csharp
using System.Drawing;
```

> *Perché è importante*: `System.Drawing` contiene le strutture `Bitmap`, `Graphics`, `Pen` e i colori che utilizzeremo durante tutto il tutorial.

## Step 1: Create a Bitmap

Crea una tela vuota che ospiterà il disegno trasformato. Specifichiamo una dimensione di **1000 × 800 pixel** e un formato pixel che supporta la trasparenza alfa.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> Questo bitmap funge da superficie di disegno. Il formato pixel scelto (`Format32bppPArgb`) garantisce un rendering ad alta qualità con alfa premoltiplicato.

## Step 2: Create a Graphics Object

Un oggetto `Graphics` fornisce i metodi di disegno (linee, forme, testo). Lo otteniamo dal bitmap appena creato.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> L'oggetto `Graphics` è il cuore di tutte le operazioni di rendering; rispetta le impostazioni di trasformazione che applicheremo successivamente.

## Step 3: Clear the Canvas

Prima di disegnare qualsiasi cosa, cancellate la tela con un colore di sfondo neutro (grigio in questo esempio). Questo passaggio dimostra anche come riempire l'intero bitmap con un colore solido.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Step 4: Set Transformation (Apply Page Transformation)

Qui **applichiamo la trasformazione della pagina** impostando `PageUnit` su pollici. Questo indica al motore grafico di interpretare tutte le coordinate successive come pollici anziché pixel.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *Suggerimento*: Cambiare `PageUnit` è un modo semplice per **come trasformare le coordinate della pagina** senza calcolare manualmente i valori in pixel.

## Step 5: Draw a Rectangle (Draw rectangle bitmap)

Ora disegniamo un rettangolo che misura **1 pollice × 1 pollice** nella posizione (1, 1) pollici. La larghezza del `Pen` è impostata a `0.1f` pollici, fornendo una linea sottile ma visibile.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> Questo dimostra **draw rectangle bitmap** dopo che la trasformazione è stata applicata—osservate come la dimensione del rettangolo è definita in pollici, non in pixel.

## Step 6: Save the Image

Infine, salvate il bitmap trasformato su disco. Sostituite `"Your Document Directory"` con il percorso reale della cartella sul vostro computer.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> Il file di output (`PageTransformation_out.png`) conterrà il rettangolo disegnato usando la trasformazione del sistema di coordinate che abbiamo impostato in precedenza.

## Common Issues and Solutions

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **L'immagine appare vuota** | Canvas non cancellato o disegno eseguito al di fuori dell'area visibile. | Verificate `graphics.PageUnit` e i valori delle coordinate; assicuratevi che il rettangolo sia entro i limiti del bitmap. |
| **Scala errata** | Uso del `GraphicsUnit` sbagliato. | Controllate che `graphics.PageUnit` corrisponda all'unità desiderata (ad esempio `GraphicsUnit.Inch`). |
| **Errori nel percorso del file** | Directory mancante o caratteri non validi. | Create la cartella di destinazione in anticipo o usate `Path.Combine` per costruire il percorso in modo sicuro. |

## Frequently Asked Questions

**D: Posso usare Aspose.Drawing gratuitamente?**  
R: Aspose.Drawing offre una prova gratuita che potete accedere [qui](https://releases.aspose.com/).

**D: Dove posso trovare la documentazione dettagliata per Aspose.Drawing?**  
R: La documentazione è disponibile [qui](https://reference.aspose.com/drawing/net/).

**D: Come posso ottenere supporto per Aspose.Drawing?**  
R: Per supporto, visitate il [Forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17).

**D: È disponibile una licenza temporanea per Aspose.Drawing?**  
R: Sì, potete ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

**D: Dove posso acquistare Aspose.Drawing?**  
R: Potete acquistare Aspose.Drawing [qui](https://purchase.aspose.com/buy).

## Conclusion

Ora avete imparato come **applicare una trasformazione del sistema di coordinate**, **disegnare oggetti bitmap rettangolari** e **salvare il risultato** usando Aspose.Drawing per .NET. Questi blocchi fondamentali vi permettono di creare grafica indipendente dalla risoluzione, perfetta per report, elementi UI o qualsiasi scenario in cui le dimensioni precise sono importanti. Sperimentate con altri valori di `GraphicsUnit` (come `Millimeter` o `Point`) per vedere come influenzano i vostri disegni.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-11-30  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose