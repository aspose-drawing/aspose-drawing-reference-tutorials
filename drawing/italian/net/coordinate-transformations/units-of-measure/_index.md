---
title: Unità di misura in Aspose.Drawing per .NET
linktitle: Unità di misura in Aspose.Drawing
second_title: API Aspose.Drawing .NET alternativa a System.Drawing.Common
description: Esplora la versatilità di Aspose.Drawing per .NET in questo tutorial approfondito, padroneggiando le unità di misura per la grafica di precisione.
weight: 14
url: /it/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unità di misura in Aspose.Drawing per .NET

## introduzione

Benvenuti nel mondo di Aspose.Drawing per .NET, dove precisione e flessibilità si incontrano nella manipolazione grafica. In questo tutorial, approfondiremo la complessità delle unità di misura all'interno di Aspose.Drawing, fornendoti una guida passo passo per sfruttare la potenza di questa straordinaria libreria.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.Drawing per .NET: assicurati di avere la libreria installata. Puoi scaricarlo[Qui](https://releases.aspose.com/drawing/net/).

- Directory dei documenti: disponi di una directory designata in cui desideri salvare i documenti creati.

- Conoscenza di base di C#: si consiglia una conoscenza di base di C# per sfruttare al meglio questa guida.

## Importa spazi dei nomi

Prima di iniziare, importiamo gli spazi dei nomi necessari per utilizzare Aspose.Drawing in modo efficace:

```csharp
using System.Drawing;
```

Ora suddividiamo ciascun esempio in più passaggi:

## Punti come unità di misura

1. Crea una bitmap: inizializza una bitmap con una larghezza e un'altezza specificate.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Crea grafica: genera un oggetto grafico dalla bitmap per disegnarci sopra.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Imposta unità pagina su punti: definisce i punti come unità di misura (1 punto = 1/72 di pollice).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Disegna rettangolo: disegna un rettangolo utilizzando i punti come unità.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Millimetri come unità di misura

1. Imposta unità pagina su millimetri: modifica l'unità di misura in millimetri (1 mm = 1/25,4 pollici).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Disegna un rettangolo in millimetri: disegna un altro rettangolo utilizzando i millimetri come unità.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Pollici come unità di misura

1. Imposta unità pagina su pollici: cambia l'unità di misura in pollici.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Disegna un rettangolo in pollici: disegna un rettangolo utilizzando i pollici come unità.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Salva il risultato

Dopo aver completato gli esempi, salva l'immagine risultante nella directory dei documenti:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Ora hai esplorato con successo le diverse unità di misura in Aspose.Drawing per .NET, creando una rappresentazione visiva di rettangoli utilizzando punti, millimetri e pollici.

## Conclusione

In questo tutorial, abbiamo esplorato come Aspose.Drawing per .NET gestisce diverse unità di misura. Manipolando punti, millimetri e pollici, puoi ottenere precisione e adattabilità nelle tue creazioni grafiche. Sperimenta questi concetti per sbloccare tutto il potenziale di Aspose.Drawing.

## Domande frequenti

### Q1: posso utilizzare Aspose.Drawing per .NET con altri framework .NET?

A1: Sì, Aspose.Drawing è compatibile con vari framework .NET, fornendo flessibilità nel tuo ambiente di sviluppo.

### Q2: È disponibile una prova gratuita?

 A2: Sì, puoi esplorare Aspose.Drawing con una prova gratuita[Qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.Drawing per .NET?

 A3: Visita il[Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17) per il supporto e le discussioni della comunità.

### Q4: Posso acquistare una licenza temporanea per progetti a breve termine?

 R4: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare la documentazione dettagliata per Aspose.Drawing?

 A5: La documentazione completa è disponibile[Qui](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
