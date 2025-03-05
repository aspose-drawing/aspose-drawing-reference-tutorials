---
title: Hinzufügen von Text zu Bildern in Aspose.Drawing
linktitle: Hinzufügen von Text zu Bildern in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative zu System.Drawing.Common
description: Entdecken Sie die nahtlose Integration von Text in Bilder mit Aspose.Drawing für .NET. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine mühelose Bildbearbeitung. Jetzt downloaden!
type: docs
weight: 12
url: /de/net/use-cases/text-on-image/
---
## Einführung
In der dynamischen Welt der .NET-Entwicklung sticht Aspose.Drawing als leistungsstarkes Werkzeug zur einfachen Bearbeitung von Bildern hervor. Das Hinzufügen von Text zu Bildern ist eine häufige Anforderung, sei es für Wasserzeichen, Anmerkungen oder die Erstellung personalisierter Grafiken. In diesem Tutorial erfahren Sie, wie Sie Aspose.Drawing nutzen können, um Text mithilfe von C# nahtlos in Ihre Bilder zu integrieren.
## Voraussetzungen
Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Folgendes vorhanden ist:
1.  Aspose.Drawing-Bibliothek: Laden Sie die Aspose.Drawing-Bibliothek von herunter und installieren Sie sie[Aspose.Drawing für .NET-Dokumentation](https://reference.aspose.com/drawing/net/).
2. Entwicklungsumgebung: Verfügen Sie über eine funktionierende .NET-Entwicklungsumgebung, einschließlich Visual Studio oder einer anderen kompatiblen IDE.
Beginnen wir nun mit der Schritt-für-Schritt-Anleitung.
## Namespaces importieren
Beginnen Sie mit dem Importieren der erforderlichen Namespaces in Ihr C#-Projekt:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## Schritt 1: Laden Sie das Bild
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Hier laden wir das Bild aus dem angegebenen Dateipfad und initialisieren das Grafikobjekt für die weitere Verarbeitung.
## Schritt 2: Texteigenschaften festlegen
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Definieren Sie die Texteigenschaften wie Farbe, Schriftart und Abstand. Passen Sie diese Parameter nach Ihren Wünschen an.
## Schritt 3: Messen Sie die Textgröße
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Berechnen Sie die erforderliche Textgröße, indem Sie jedes Wort einzeln messen. Dies gewährleistet die richtige Platzierung und vermeidet Textüberlappungen.
## Schritt 4: Zeichnen Sie Text auf das Bild
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Positionieren Sie nun den Text anhand der berechneten Größe auf dem Bild und zeichnen Sie ihn mit der angegebenen Schriftart und Farbe.
## Schritt 5: Speichern Sie das Bild
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Speichern Sie das geänderte Bild im gewünschten Verzeichnis.
Diese Schritt-für-Schritt-Anleitung zeigt einen unkomplizierten Prozess zum Hinzufügen von Text zu Bildern mit Aspose.Drawing für .NET. Experimentieren Sie mit verschiedenen Schriftarten, Farben und Textinhalten, um den gewünschten visuellen Effekt zu erzielen.
## Abschluss
Aspose.Drawing vereinfacht Bildbearbeitungsaufgaben in .NET und stellt Entwicklern ein robustes Toolkit zur Verfügung. Das Hinzufügen von Text zu Bildern ist nur ein Beispiel für ihre Möglichkeiten und zeigt die Vielseitigkeit der Bibliothek bei der Handhabung grafischer Elemente.
## Häufig gestellte Fragen
### Ist Aspose.Drawing mit allen Bildformaten kompatibel?
 Aspose.Drawing unterstützt eine Vielzahl von Bildformaten, darunter beliebte wie JPEG, PNG und GIF. Siehe die[Dokumentation](https://reference.aspose.com/drawing/net/) für eine vollständige Liste.
### Kann ich Aspose.Drawing für kommerzielle Projekte verwenden?
Ja, Aspose.Drawing eignet sich sowohl für persönliche als auch für kommerzielle Projekte. Einzelheiten zur Lizenzierung finden Sie unter[Kaufseite](https://purchase.aspose.com/buy).
### Sind temporäre Lizenzen zu Testzwecken verfügbar?
 Ja, Sie können eine temporäre Lizenz zum Testen erhalten, indem Sie hier vorbeischauen[Temporäre Lizenz](https://purchase.aspose.com/temporary-license/).
### Wo finde ich Community-Unterstützung für Aspose.Drawing?
 Treten Sie mit der Community in Kontakt und erhalten Sie Unterstützung[Aspose.Drawing-Forum](https://forum.aspose.com/c/diagram/17).
### Wie fange ich mit Aspose.Drawing an?
 Beginnen Sie mit dem Herunterladen der Bibliothek von[Hier](https://releases.aspose.com/drawing/net/) und das umfassende erkunden[Dokumentation](https://reference.aspose.com/drawing/net/).