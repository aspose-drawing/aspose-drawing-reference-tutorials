---
date: 2026-05-24
description: Scopri come impostare l'unità in Aspose.Drawing per .NET, convertire
  facilmente le unità grafiche e padroneggiare misurazioni precise per il rendering
  grafico.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Unità di misura in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Come impostare l'unità in Aspose.Drawing per .NET – Unità di misura
url: /it/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come impostare l'unità in Aspose.Drawing per .NET – Unità di misura

## Introduzione

Benvenuti nel mondo di Aspose.Drawing per .NET, dove precisione e flessibilità si incontrano nella manipolazione grafica. In questo tutorial scoprirete **come impostare l'unità** per i vostri disegni, imparerete a **convertire le unità grafiche** tra punti, millimetri e pollici, e vedrete esempi reali che rendono le vostre immagini pixel‑perfect. Che stiate creando report, miniature o grafici personalizzati, padroneggiare le unità di misura è essenziale per una resa coerente su tutti i dispositivi.

## Risposte rapide
- **Qual è il modo principale per cambiare le unità?** Chiamare `graphics.PageUnit = PageUnit.Point` (o `.Millimeter`, `.Inch`) sull'oggetto `Graphics`.  
- **Quale unità equivale a 1/72 di pollice?** Punti.  
- **Quanti millimetri ci sono in un pollice?** 25,4 mm = 1 pollice.  
- **Ho bisogno di librerie aggiuntive per usare le unità?** No, la libreria core di Aspose.Drawing fornisce tutte le costanti delle unità.  
- **Posso mescolare unità in un'unica immagine?** Impostare l'unità una sola volta per istanza `Graphics`; disegnare tutto usando quella unità per coerenza.

## Prerequisiti

Prima di immergerci nel tutorial, assicuratevi di avere i seguenti prerequisiti pronti:

- Aspose.Drawing per .NET: Assicuratevi di avere la libreria installata. Potete scaricarla [qui](https://releases.aspose.com/drawing/net/).
- Directory dei documenti: Disporre di una directory designata dove salvare i documenti creati.
- Conoscenza di base di C#: Una comprensione fondamentale di C# è consigliata per sfruttare al meglio questa guida.

## Importare gli spazi dei nomi

Prima di iniziare, importiamo gli spazi dei nomi necessari per utilizzare Aspose.Drawing in modo efficace:

```csharp
using System.Drawing;
```

Ora, suddividiamo ogni esempio in più passaggi:

## Come impostare l'unità in Punti?

La classe `Bitmap` rappresenta un'immagine in memoria che funge da tela di disegno. Caricate il vostro bitmap, create un oggetto `Graphics` e impostate l'unità di pagina su punti — questo indica ad Aspose.Drawing di interpretare tutte le coordinate come valori di 1/72 pollice. L'uso dei punti offre un controllo fine per grafica pronta per la stampa e consente di specificare spessori di linea con alta precisione.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Passo 1: Creare un Bitmap  
La classe `Bitmap` rappresenta un'immagine in memoria che funge da tela di disegno.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Passo 2: Creare un oggetto Graphics  
`Graphics` fornisce metodi di disegno per renderizzare forme e testo su un `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Passo 3: Impostare Page Unit su Punti  
`PageUnit` è un'enumerazione che specifica l'unità di misura per le coordinate della pagina. `PageUnit.Point` definisce i punti come unità di misura (1 punto = 1/72 pollice). Questa impostazione si applica a tutte le successive chiamate di disegno.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Passo 4: Disegnare un rettangolo in Punti  
Quando disegnate un rettangolo dopo aver impostato l'unità, le dimensioni specificate vengono interpretate come punti, garantendo una dimensione precisa.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Come impostare l'unità in Millimetri?

`PageUnit` è un'enumerazione che specifica l'unità di misura per le coordinate della pagina. Passare ai millimetri è utile quando servono dimensioni metriche, ad esempio nella generazione di diagrammi ingegneristici. Aspose.Drawing tratta 1 mm come 1/25,4 pollice, consentendo di allineare la grafica con le misurazioni fisiche usate nella produzione e nella documentazione tecnica.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Passo 1: Impostare Page Unit su Millimetri  
Assegnate `PageUnit.Millimeter` all'oggetto `Graphics`; tutte le coordinate ora corrispondono al sistema metrico.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Passo 2: Disegnare un rettangolo in Millimetri  
La larghezza e l'altezza del rettangolo sono ora espresse in millimetri, facilitando l'allineamento con le misurazioni fisiche e garantendo che l'output stampato corrisponda alle dimensioni reali.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Come impostare l'unità in Pollici?

`Graphics` fornisce metodi di disegno per renderizzare forme e testo su un `Bitmap`. I pollici sono l'unità predefinita per molti strumenti di progettazione statunitensi. Impostare l'unità su pollici permette di pensare in termini familiari quando si dispone di elementi UI, e semplifica la transizione dal design su schermo alla stampa dove i pollici sono comunemente usati.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Passo 1: Impostare Page Unit su Pollici  
`PageUnit.Inch` cambia il sistema di coordinate in modo che 1 unità corrisponda a 1 pollice, fornendo un modo semplice per dimensionare gli elementi per layout orientati alla stampa.

CODE_BLOCK_PLACEHOLDER_10_END

### Passo 2: Disegnare un rettangolo in Pollici  
Ora qualsiasi forma disegnata utilizza i pollici come base di misura, ideale per layout di stampa e per comunicare le dimensioni a stakeholder abituati alle unità imperiali.

CODE_BLOCK_PLACEHOLDER_11_END

## Salva il risultato

Dopo aver completato gli esempi, salvate l'immagine risultante nella vostra directory dei documenti. Il metodo `Bitmap.Save` scrive il file nel formato specificato (PNG, JPEG, ecc.).

CODE_BLOCK_PLACEHOLDER_12_END

Ora avete navigato con successo le diverse unità di misura in Aspose.Drawing per .NET, creando una rappresentazione visiva di rettangoli usando punti, millimetri e pollici.

## Perché usare il sistema di unità di Aspose.Drawing?

Aspose.Drawing supporta **oltre 30 formati di immagine** e può elaborare immagini fino a **5000 × 5000 pixel** senza caricare l'intero file in memoria, offrendo alte prestazioni per la generazione di grafica su larga scala. Impostando esplicitamente l'unità, si elimina l'incertezza, si riducono gli errori di conversione e si garantisce che l'output corrisponda a dimensioni fisiche esatte su tutte le piattaforme.

## Problemi comuni e soluzioni

- **Dimensione inaspettata dopo il salvataggio** – Verificate di aver impostato `graphics.PageUnit` **prima** di qualsiasi chiamata di disegno; modificare l'unità in seguito non ridimensiona retroattivamente le forme esistenti.  
- **Output sfocato su schermi ad alta DPI** – Incrementate la risoluzione del bitmap (ad es., `new Bitmap(width, height, 300)`) per corrispondere alla DPI target.  
- **Unità miste in un'unica immagine** – Create istanze separate di `Graphics` per ogni unità o eseguite conversioni manuali prima del disegno.

## Domande frequenti

### Q1: Posso usare Aspose.Drawing per .NET con altri framework .NET?
A1: Sì, Aspose.Drawing è compatibile con vari framework .NET, offrendo flessibilità nel vostro ambiente di sviluppo.

### Q2: È disponibile una versione di prova gratuita?
A2: Sì, potete provare Aspose.Drawing con una versione di prova gratuita [qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.Drawing per .NET?
A3: Visitate il [Forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) per supporto della community e discussioni.

### Q4: Posso acquistare una licenza temporanea per progetti a breve termine?
A4: Sì, potete ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare la documentazione dettagliata per Aspose.Drawing?
A5: La documentazione completa è disponibile [qui](https://reference.aspose.com/drawing/net/).

---

**Last Updated:** 2026-05-24  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
