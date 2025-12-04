---
title: Δημιουργία μηνυμάτων στο Aspose.Drawing
linktitle: Δημιουργία μηνυμάτων στο Aspose.Drawing
second_title: Aspose.Drawing .NET API - Εναλλακτική λύση στο System.Drawing.Common
description: Βελτιώστε τις εικόνες των εγγράφων σας χρησιμοποιώντας το Aspose.Drawing για .NET! Μάθετε βήμα προς βήμα πώς να προσθέτετε μηνύματα προώθησης για πιο καθαρά και κατατοπιστικά γραφικά.
weight: 10
url: /el/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία μηνυμάτων στο Aspose.Drawing

## Εισαγωγή
Καλώς ορίσατε στον αναλυτικό οδηγό μας για τη δημιουργία μηνυμάτων στο Aspose.Drawing για .NET! Αν θέλετε να βελτιώσετε τις εικόνες των εγγράφων σας με μηνύματα προώθησης, βρίσκεστε στο σωστό μέρος. Σε αυτό το σεμινάριο, θα αναλύσουμε τη διαδικασία σε διαχειρίσιμα βήματα χρησιμοποιώντας τη βιβλιοθήκη Aspose.Drawing.
## Προαπαιτούμενα
Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
- Βασικές γνώσεις γλώσσας προγραμματισμού C#.
-  Εγκαταστάθηκε η βιβλιοθήκη Aspose.Drawing. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/drawing/net/).
- Ένα έγγραφο ή μια εικόνα όπου θέλετε να προσθέσετε μηνύματα προώθησης.
## Εισαγωγή χώρων ονομάτων
Βεβαιωθείτε ότι έχετε συμπεριλάβει τους απαραίτητους χώρους ονομάτων στο έργο σας:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Βήμα 1: Φορτώστε την εικόνα
 Ξεκινήστε φορτώνοντας την εικόνα όπου θέλετε να προσθέσετε μηνύματα προώθησης. Αντικαθιστώ`"Your Document Directory"` και`"gears.png"` με τον πραγματικό σας κατάλογο και το όνομα αρχείου εικόνας.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Ο κωδικός σας εδώ
}
```
## Βήμα 2: Δημιουργία αντικειμένου γραφικών
 Δημιουργώ ένα`Graphics` αντικείμενο από την εικόνα για να εκτελέσετε εργασίες σχεδίασης.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Βήμα 3: Καθορισμός θέσεων προώθησης
Καθορίστε τα σημεία έναρξης και λήξης για κάθε επεξήγηση μαζί με την τιμή και τη μονάδα προώθησης.
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
## Βήμα 4: Σχεδιάστε επεξηγήσεις
 Εφαρμόστε το`DrawCallOut` μέθοδος σχεδίασης μηνυμάτων στην εικόνα.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Βήμα 5: Αποθηκεύστε την εικόνα
Αποθηκεύστε την εικόνα με επεξηγήσεις στον κατάλογο που επιθυμείτε.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Σχεδιάστε τον πηγαίο κώδικα προώθησης
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
## συμπέρασμα

Συγχαρητήρια! Προσθέσατε με επιτυχία μηνύματα προώθησης στην εικόνα σας χρησιμοποιώντας το Aspose.Drawing για .NET. Μη διστάσετε να πειραματιστείτε με διαφορετικές θέσεις και τιμές για να προσαρμόσετε περαιτέρω τα μηνύματά σας.

## Συχνές ερωτήσεις

### Μπορώ να χρησιμοποιήσω το Aspose.Drawing για άλλους τύπους εικονογραφήσεων;

Ναι, το Aspose.Drawing υποστηρίζει ένα ευρύ φάσμα λειτουργιών σχεδίασης για διάφορους τύπους εικονογραφήσεων.

### Είναι το Aspose.Drawing συμβατό με διαφορετικές μορφές εικόνας;

Απολύτως! Το Aspose.Drawing υποστηρίζει δημοφιλείς μορφές εικόνας όπως PNG, JPEG, GIF και άλλα.

### Πού μπορώ να βρω περισσότερα παραδείγματα και τεκμηρίωση;

 Εξερευνήστε την πλήρη τεκμηρίωση[εδώ](https://reference.aspose.com/drawing/net/).

### Πώς μπορώ να λάβω υποστήριξη εάν αντιμετωπίσω προβλήματα;

 Επισκέψου το[Aspose.Φόρουμ σχεδίασης](https://forum.aspose.com/c/drawing/44) για κοινοτική υποστήριξη.

### Μπορώ να δοκιμάσω το Aspose.Drawing πριν από την αγορά;

 Σίγουρα! Ξεκινήστε με μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
