---
date: 2026-03-02
description: Migliora le illustrazioni dei tuoi documenti con Aspose.Drawing per .NET!
  Impara passo dopo passo come aggiungere annotazioni per visuali più chiare e informative.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Come aggiungere i callout con Aspose.Drawing per .NET
url: /it/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Creare Callout in Aspose.Drawing

## Introduzione
Se ti stai chiedendo **come aggiungere callout** alle tue immagini o diagrammi usando Aspose.Drawing per .NET, sei nel posto giusto. In questo tutorial ti guideremo attraverso l'intero processo—dal caricamento di un'immagine al disegno di callout elegantemente stilizzati—così potrai rendere le tue illustrazioni più chiare e informative.

## Risposte Rapide
- **Quale libreria è necessaria?** Aspose.Drawing per .NET (scaricabile dal sito ufficiale).  
- **Quali versioni .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **È necessaria una licenza?** Una versione di prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per un callout di base.  
- **Posso personalizzare colori e font?** Sì—tutto è gestito da oggetti standard GDI+ (Pen, Font, Brush).

## Come Aggiungere Callout in Aspose.Drawing
Di seguito trovi una guida concisa, passo‑passo, che mostra esattamente **come aggiungere callout** a un'immagine. Sentiti libero di copiare il codice, sperimentare con le posizioni e adattare lo stile per corrispondere al tuo brand.

## Prerequisiti
Prima di iniziare, assicurati di avere:

- Conoscenza di base del linguaggio di programmazione C#.
- Libreria Aspose.Drawing installata. Puoi scaricarla [qui](https://releases.aspose.com/drawing/net/).
- Un documento o un'immagine dove desideri aggiungere i callout.

## Importare Namespace
Assicurati di includere i namespace necessari nel tuo progetto:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Passo 1: Caricare l'Immagine
Inizia caricando l'immagine dove vuoi aggiungere i callout. Sostituisci `"Your Document Directory"` e `"gears.png"` con la tua directory reale e il nome del file immagine.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Passo 2: Creare l'Oggetto Graphics
Crea un oggetto `Graphics` dall'immagine per eseguire operazioni di disegno.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Passo 3: Definire le Posizioni del Callout
Definisci i punti di inizio e fine per ogni callout insieme al valore e all'unità del callout.

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

## Passo 4: Disegnare i Callout
Implementa il metodo `DrawCallOut` per disegnare i callout sull'immagine.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Passo 5: Salvare l'Immagine
Salva l'immagine con i callout nella directory desiderata.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Codice Sorgente del Callout
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

## Problemi Comuni & Suggerimenti
- **Coordinate di ancoraggio errate** – assicurati che i punti di inizio e fine siano entro i limiti dell'immagine; altrimenti il callout potrebbe essere ritagliato.  
- **Sovrapposizione del testo** – regola `spaceSize` o la dimensione del font se l'etichetta collide con altri elementi grafici.  
- **Prestazioni** – per immagini molto grandi, considera di rilasciare gli oggetti `Pen`, `Font` e `Brush` dopo l'uso per liberare risorse.

## Conclusione
Congratulazioni! Ora sai **come aggiungere callout** a un'immagine usando Aspose.Drawing per .NET. Sentiti libero di sperimentare con diverse posizioni, colori e font per adattarli al tuo stile visivo.

## FAQ

### Posso usare Aspose.Drawing per altri tipi di illustrazioni?
Sì, Aspose.Drawing supporta un'ampia gamma di operazioni di disegno per vari tipi di illustrazioni.

### Aspose.Drawing è compatibile con diversi formati immagine?
Assolutamente! Aspose.Drawing supporta formati immagine popolari come PNG, JPEG, GIF e altri.

### Dove posso trovare più esempi e documentazione?
Esplora la documentazione completa [qui](https://reference.aspose.com/drawing/net/).

### Come ottengo supporto se incontro problemi?
Visita il [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) per il supporto della community.

### Posso provare Aspose.Drawing prima di acquistare?
Certamente! Inizia con una prova gratuita [qui](https://releases.aspose.com/).

**Additional Q&A**

**Q: Posso cambiare lo stile della linea del callout (tratteggiata, puntinata)?**  
A: Sì—basta configurare la proprietà `Pen.DashStyle` prima di disegnare la linea.

**Q: È possibile aggiungere un colore di sfondo all'etichetta del callout?**  
A: Assolutamente. Crea un `SolidBrush` con il colore desiderato e riempi un rettangolo dietro il testo prima di chiamare `DrawString`.

**Q: Come posso garantire che il callout abbia lo stesso aspetto su display ad alta DPI?**  
A: Imposta `graphics.PageUnit = GraphicsUnit.Pixel` (come mostrato) e utilizza misurazioni basate su vettori per mantenere la scala coerente.

---

**Ultimo aggiornamento:** 2026-03-02  
**Testato con:** Aspose.Drawing 24.11 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}