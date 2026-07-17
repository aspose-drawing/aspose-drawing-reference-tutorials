---
date: 2026-03-02
description: Βελτιώστε τις εικονογραφήσεις των εγγράφων σας με το Aspose.Drawing για
  .NET! Μάθετε βήμα-βήμα πώς να προσθέτετε σημειώσεις εξήγησης για πιο καθαρές και
  ενημερωτικές απεικονίσεις.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Πώς να προσθέσετε επεξηγήσεις με το Aspose.Drawing για .NET
url: /el/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία Callouts στο Aspose.Drawing

## Εισαγωγή
Αν αναρωτιέστε **πώς να προσθέσετε callouts** στις εικόνες ή τα διαγράμματα σας χρησιμοποιώντας το Aspose.Drawing για .NET, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα περάσουμε από όλη τη διαδικασία—από τη φόρτωση μιας εικόνας μέχρι το σχεδιασμό όμορφα μορφοποιημένων callouts—ώστε να κάνετε τις εικονογραφήσεις σας πιο σαφείς και ενημερωτικές.

## Γρήγορες Απαντήσεις
- **Τι βιβλιοθήκη χρειάζομαι;** Aspose.Drawing for .NET (διαθέσιμη για λήψη από την επίσημη ιστοσελίδα).  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Πόσο διαρκεί η υλοποίηση;** Συνήθως λιγότερο από 10 λεπτά για ένα βασικό callout.  
- **Μπορώ να προσαρμόσω χρώματα και γραμματοσειρές;** Ναι—όλα ελέγχονται από τα τυπικά αντικείμενα GDI+ (Pen, Font, Brush).

## Πώς να Προσθέσετε Callouts στο Aspose.Drawing
Παρακάτω βρίσκεται ένας σύντομος, βήμα‑βήμα οδηγός που δείχνει ακριβώς **πώς να προσθέσετε callouts** σε μια εικόνα. Μπορείτε ελεύθερα να αντιγράψετε τον κώδικα, να πειραματιστείτε με τις θέσεις και να προσαρμόσετε το στυλ ώστε να ταιριάζει με το brand σας.

## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- Βασικές γνώσεις της γλώσσας προγραμματισμού C#.
- Εγκατεστημένη τη βιβλιοθήκη Aspose.Drawing. Μπορείτε να τη κατεβάσετε [εδώ](https://releases.aspose.com/drawing/net/).
- Ένα έγγραφο ή εικόνα όπου θέλετε να προσθέσετε callouts.

## Εισαγωγή Namespaces
Βεβαιωθείτε ότι έχετε συμπεριλάβει τα απαραίτητα namespaces στο project σας:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Βήμα 1: Φόρτωση της Εικόνας
Ξεκινήστε φορτώνοντας την εικόνα όπου θέλετε να προσθέσετε callouts. Αντικαταστήστε το `"Your Document Directory"` και το `"gears.png"` με τον πραγματικό σας φάκελο και το όνομα αρχείου της εικόνας.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Βήμα 2: Δημιουργία Αντικειμένου Graphics
Δημιουργήστε ένα αντικείμενο `Graphics` από την εικόνα για να εκτελέσετε λειτουργίες σχεδίασης.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Βήμα 3: Ορισμός Θέσεων Callout
Ορίστε τα σημεία εκκίνησης και λήξης για κάθε callout μαζί με την τιμή και τη μονάδα του callout.

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

## Βήμα 4: Σχεδίαση Callouts
Υλοποιήστε τη μέθοδο `DrawCallOut` για να σχεδιάσετε callouts στην εικόνα.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Βήμα 5: Αποθήκευση της Εικόνας
Αποθηκεύστε την εικόνα με τα callouts στον επιθυμητό φάκελό σας.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Πηγαίος Κώδικας Σχεδίασης Callout
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

## Κοινά Προβλήματα & Συμβουλές
- **Λανθασμένες συντεταγμένες άγκυρας** – βεβαιωθείτε ότι τα σημεία εκκίνησης και λήξης βρίσκονται εντός των ορίων της εικόνας· διαφορετικά το callout μπορεί να κοπεί.  
- **Επικάλυψη κειμένου** – προσαρμόστε το `spaceSize` ή το μέγεθος γραμματοσειράς αν η ετικέτα συγκρούεται με άλλα γραφικά.  
- **Απόδοση** – για πολύ μεγάλες εικόνες, σκεφτείτε να απελευθερώσετε (dispose) τα αντικείμενα `Pen`, `Font` και `Brush` μετά τη χρήση για να ελευθερώσετε πόρους.

## Συμπέρασμα
Συγχαρητήρια! Τώρα ξέρετε **πώς να προσθέσετε callouts** σε μια εικόνα χρησιμοποιώντας το Aspose.Drawing για .NET. Μη διστάσετε να πειραματιστείτε με διαφορετικές θέσεις, χρώματα και γραμματοσειρές ώστε να ταιριάζουν με το οπτικό σας στυλ.

## Συχνές Ερωτήσεις

### Μπορώ να χρησιμοποιήσω το Aspose.Drawing για άλλους τύπους εικονογραφήσεων;
Ναι, το Aspose.Drawing υποστηρίζει ένα ευρύ φάσμα λειτουργιών σχεδίασης για διάφορους τύπους εικονογραφήσεων.

### Το Aspose.Drawing είναι συμβατό με διαφορετικές μορφές εικόνας;
Απολύτως! Το Aspose.Drawing υποστηρίζει δημοφιλείς μορφές εικόνας όπως PNG, JPEG, GIF και άλλα.

### Πού μπορώ να βρω περισσότερα παραδείγματα και τεκμηρίωση;
Εξερευνήστε την ολοκληρωμένη τεκμηρίωση [εδώ](https://reference.aspose.com/drawing/net/).

### Πώς μπορώ να λάβω υποστήριξη αν αντιμετωπίσω προβλήματα;
Επισκεφθείτε το [φόρουμ Aspose.Drawing](https://forum.aspose.com/c/drawing/44) για υποστήριξη από την κοινότητα.

### Μπορώ να δοκιμάσω το Aspose.Drawing πριν την αγορά;
Φυσικά! Ξεκινήστε με μια δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

**Additional Q&A**

**Q: Μπορώ να αλλάξω το στυλ της γραμμής του callout (διακεκομμένη, με κουκκίδες);**  
A: Ναι—απλώς ρυθμίστε την ιδιότητα `Pen.DashStyle` πριν σχεδιάσετε τη γραμμή.

**Q: Είναι δυνατόν να προστεθεί χρώμα φόντου στην ετικέτα του callout;**  
A: Απολύτως. Δημιουργήστε ένα `SolidBrush` με το επιθυμητό χρώμα και γεμίστε ένα ορθογώνιο πίσω από το κείμενο πριν καλέσετε `DrawString`.

**Q: Πώς μπορώ να διασφαλίσω ότι το callout φαίνεται το ίδιο σε οθόνες υψηλής ανάλυσης (high‑DPI);**  
A: Ορίστε `graphics.PageUnit = GraphicsUnit.Pixel` (όπως φαίνεται) και χρησιμοποιήστε μετρήσεις βασισμένες σε διανύσματα για να διατηρήσετε τη σταθερή κλιμάκωση.

---

**Τελευταία ενημέρωση:** 2026-03-02  
**Δοκιμάστηκε με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}