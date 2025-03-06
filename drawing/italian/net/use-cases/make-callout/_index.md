---
title: Creazione di callout in Aspose.Drawing
linktitle: Creazione di callout in Aspose.Drawing
second_title: API Aspose.Drawing .NET alternativa a System.Drawing.Common
description: Migliora le illustrazioni dei tuoi documenti utilizzando Aspose.Drawing per .NET! Scopri passo dopo passo come aggiungere callout per immagini più chiare e informative.
weight: 10
url: /it/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Creazione di callout in Aspose.Drawing

## introduzione
Benvenuti nella nostra guida passo passo sulla creazione di callout in Aspose.Drawing per .NET! Se stai cercando di migliorare le illustrazioni dei tuoi documenti con i callout, sei nel posto giusto. In questo tutorial, suddivideremo il processo in passaggi gestibili utilizzando la libreria Aspose.Drawing.
## Prerequisiti
Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:
- Conoscenza base del linguaggio di programmazione C#.
-  Libreria Aspose.Drawing installata. Puoi scaricarlo[Qui](https://releases.aspose.com/drawing/net/).
- Un documento o un'immagine in cui desideri aggiungere callout.
## Importa spazi dei nomi
Assicurati di avere gli spazi dei nomi necessari inclusi nel tuo progetto:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Passaggio 1: caricare l'immagine
 Inizia caricando l'immagine in cui desideri aggiungere i callout. Sostituire`"Your Document Directory"` E`"gears.png"` con la directory effettiva e il nome del file immagine.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Il tuo codice qui
}
```
## Passaggio 2: crea un oggetto grafico
 Creare un`Graphics` oggetto dall'immagine per eseguire operazioni di disegno.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Passaggio 3: definire le posizioni dei callout
Definire i punti iniziale e finale per ogni didascalia insieme al valore e all'unità della didascalia.
```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```
## Passaggio 4: disegnare didascalie
 Implementare il`DrawCallOut` metodo per disegnare didascalie sull'immagine.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Passaggio 5: salva l'immagine
Salva l'immagine con i callout nella directory desiderata.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Disegna il codice sorgente del callout
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```
## Conclusione

Congratulazioni! Hai aggiunto con successo i callout alla tua immagine utilizzando Aspose.Drawing per .NET. Sentiti libero di sperimentare posizioni e valori diversi per personalizzare ulteriormente i tuoi callout.

## Domande frequenti

### Posso utilizzare Aspose.Drawing per altri tipi di illustrazioni?

Sì, Aspose.Drawing supporta un'ampia gamma di operazioni di disegno per vari tipi di illustrazioni.

### Aspose.Drawing è compatibile con diversi formati di immagine?

Assolutamente! Aspose.Drawing supporta i formati di immagine più diffusi come PNG, JPEG, GIF e altri.

### Dove posso trovare altri esempi e documentazione?

 Esplora la documentazione completa[Qui](https://reference.aspose.com/drawing/net/).

### Come posso ottenere supporto se riscontro problemi?

 Visitare il[Forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17) per il sostegno della comunità.

### Posso provare Aspose.Drawing prima dell'acquisto?

 Certamente! Inizia con una prova gratuita[Qui](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
