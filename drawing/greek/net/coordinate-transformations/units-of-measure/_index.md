---
date: 2026-02-04
description: Μάθετε πώς να δημιουργείτε bitmap με το Aspose.Drawing για .NET, να σχεδιάζετε
  ορθογώνιο με σημεία και να εξοικειωθείτε με τις μονάδες μέτρησης για ακριβή γραφικά.
linktitle: Units of Measure in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Δημιουργία Bitmap με το Aspose.Drawing – Μονάδες Μέτρησης
url: /el/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία Bitmap με Aspose.Drawing – Μονάδες Μέτρησης

## Εισαγωγή

Σε αυτό το tutorial θα **δημιουργήσετε bitmap Aspose.Drawing** για .NET και θα εξερευνήσετε πώς διαφορετικές μονάδες μέτρησης επηρεάζουν τα σχέδιά σας. Θα περάσουμε από τη σχεδίαση ορθογωνίων χρησιμοποιώντας points, χιλιοστά και ίντσες, ώστε να μπορείτε να επιλέξετε τη σωστή μονάδα για οποιοδήποτε σενάριο με έντονη γραφική απεικόνιση. Στο τέλος θα είστε άνετοι με την εναλλαγή μεταξύ μονάδων και τη δημιουργία εικόνων pixel‑perfect.

## Γρήγορες Απαντήσεις
- **Ποιος είναι ο κύριος σκοπός αυτού του οδηγού;** Για να δείξει πώς να δημιουργήσετε ένα bitmap με Aspose.Drawing και να σχεδιάσετε σχήματα χρησιμοποιώντας διάφορες μονάδες μέτρησης.  
- **Ποιες μονάδες παρουσιάζονται;** Points, χιλιοστά και ίντσες.  
- **Χρειάζομαι άδεια για να εκτελέσω τα παραδείγματα;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποιες εκδόσεις του .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Πού μπορώ να κατεβάσω το Aspose.Drawing;** Από τη επίσημη σελίδα λήψης που συνδέεται παρακάτω.

## Τι είναι το “create bitmap Aspose.Drawing”;
Η δημιουργία ενός bitmap με το Aspose.Drawing σημαίνει την δημιουργία ενός αντικειμένου `Bitmap` στο οποίο μπορείτε να σχεδιάσετε χρησιμοποιώντας το API γραφικών του Aspose.Drawing. Σε αντίθεση με το System.Drawing, το Aspose.Drawing λειτουργεί σταθερά σε όλες τις πλατφόρμες .NET.

## Γιατί να χρησιμοποιήσετε διαφορετικές μονάδες μέτρησης;
Η επιλογή της σωστής μονάδας (points, χιλιοστά, ίντσες) σας επιτρέπει να ευθυγραμμίσετε τα γραφικά με πραγματικές μετρήσεις, καθιστώντας πιο εύκολη την ενσωμάτωση των σχεδίων σε έντυπα, PDF ή διατάξεις UI όπου οι φυσικές διαστάσεις έχουν σημασία.

## Προαπαιτούμενα

- **Aspose.Drawing for .NET** – κατεβάστε το [εδώ](https://releases.aspose.com/drawing/net/).  
- **Document Directory** – ένας φάκελος στον υπολογιστή σας όπου θα αποθηκευτεί η παραγόμενη εικόνα.  
- **Basic C# Knowledge** – εξοικείωση με κλάσεις, αντικείμενα και κλήσεις μεθόδων.

## Εισαγωγή Namespaces

Πρώτα, εισάγετε το απαραίτητο namespace ώστε να μπορείτε να εργάζεστε με τα αντικείμενα σχεδίασης:

```csharp
using System.Drawing;
```

## Δημιουργία Bitmap με Aspose.Drawing – Κατανόηση Μονάδων Μέτρησης

### Βήμα 1: Δημιουργία Bitmap

Ξεκινάμε δημιουργώντας ένα bitmap 1000 × 800 pixel που θα λειτουργήσει ως καμβάς μας.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Βήμα 2: Δημιουργία αντικειμένου Graphics

Το αντικείμενο `Graphics` μας παρέχει δυνατότητες σχεδίασης στο bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Σχεδίαση Ορθογωνίου με Points

Τα points είναι μια παραδοσιακή μονάδα εκτύπωσης (1 point = 1/72 inch). Ορίζοντας τη μονάδα σελίδας σε points μπορείτε να εργαστείτε με γνωστές τυπογραφικές μετρήσεις.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

Τώρα σχεδιάστε ένα ορθογώνιο χρησιμοποιώντας points. Το πάχος της πένας ορίζεται σε 36 points (½ inch) για σαφή ορατότητα.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

**Συμβουλή:** Οι συντεταγμένες `(72,72)` αντιστοιχούν σε μετατόπιση 1‑inch από την επάνω‑αριστερή γωνία επειδή 72 points = 1 inch.

## Σχεδίαση Ορθογωνίου σε Χιλιοστά

Τα χιλιοστά είναι ιδανικά για τεχνικά σχέδια ή όταν χρειάζεστε μετρική ακρίβεια.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

Το παρακάτω ορθογώνιο χρησιμοποιεί πένα 6.35 mm (ισοδύναμη με 0.25 inch) και πλευρά 25.4 mm (1 inch).

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Σχεδίαση Ορθογωνίου σε Ίντσες

Οι ίντσες είναι κοινές στην αμερικανική εκτύπωση και το UI design. Η εναλλαγή σε ίντσες διευκολύνει την ευθυγράμμιση με τις ρυθμίσεις DPI της οθόνης.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

Εδώ σχεδιάζουμε ένα μπλε ορθογώνιο με λεπτή πένα 0.125 inch.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Αποθήκευση του Αποτελέσματος

Αφού σχεδιάσετε όλα τα σχήματα, αποθηκεύστε το bitmap στο σύστημα αρχείων. Προσαρμόστε τη διαδρομή ώστε να ταιριάζει με το φάκελο εγγράφων σας.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Όταν ανοίξετε το αποθηκευμένο PNG, θα δείτε τρία ορθογώνια—κάθε ένα αποδοθέν με διαφορετική μονάδα μέτρησης.

## Κοινά Προβλήματα & Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Η εικόνα εμφανίζεται κενή** | Το αντικείμενο Graphics δεν έχει εκκαθαριστεί πριν την αποθήκευση. | Κλήστε `graphics.Dispose();` πριν το `bitmap.Save()`. |
| **Λανθασμένες διαστάσεις** | Λανθασμένη τιμή `PageUnit`. | Επαληθεύστε ότι έχετε ορίσει το `graphics.PageUnit` στην επιθυμητή `GraphicsUnit`. |
| **Σφάλματα διαδρομής αρχείου** | Απουσία φακέλου ή μη έγκυροι χαρακτήρες. | Βεβαιωθείτε ότι ο φάκελος προορισμού υπάρχει και χρησιμοποιήστε `Path.Combine`. |

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.Drawing για .NET με άλλα .NET frameworks;
A1: Ναι, το Aspose.Drawing είναι συμβατό με διάφορα .NET frameworks, παρέχοντας ευελιξία στο περιβάλλον ανάπτυξής σας.

### Q2: Υπάρχει διαθέσιμη δωρεάν δοκιμή;
A2: Ναι, μπορείτε να εξερευνήσετε το Aspose.Drawing με δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Q3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Drawing για .NET;
A3: Επισκεφθείτε το [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) για υποστήριξη της κοινότητας και συζητήσεις.

### Q4: Μπορώ να αγοράσω προσωρινή άδεια για βραχυπρόθεσμα έργα;
A4: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

### Q5: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.Drawing;
A5: Η πλήρης τεκμηρίωση είναι διαθέσιμη [εδώ](https://reference.aspose.com/drawing/net/).

## Συχνές Ερωτήσεις

**Q: Υποστηρίζει το Aspose.Drawing απόδοση υψηλής DPI;**  
A: Απόλυτα. Η βιβλιοθήκη σέβεται τις ρυθμίσεις DPI του bitmap, επιτρέποντας καθαρή έξοδο σε οθόνες υψηλής ανάλυσης.

**Q: Μπορώ να συνδυάσω πολλαπλές μονάδες σε ένα μόνο σχέδιο;**  
A: Μπορείτε να αλλάξετε το `Graphics.PageUnit` ανά πάσα στιγμή, αλλά παρακολουθείτε τη τρέχουσα μονάδα ώστε να αποφύγετε ασυμφωνίες διαστάσεων.

**Q: Είναι ενεργοποιημένο το anti‑aliasing εξ ορισμού;**  
A: Ναι, το Aspose.Drawing εφαρμόζει anti‑aliasing σε σχήματα και κείμενο εκτός εάν το απενεργοποιήσετε ρητά μέσω του `graphics.SmoothingMode`.

**Q: Πώς απελευθερώνω πόρους μετά το σχεδιασμό;**  
A: Κλήστε `graphics.Dispose();` και `bitmap.Dispose();` όταν τελειώσετε για να ελευθερώσετε μη διαχειριζόμενη μνήμη.

**Q: Μπορώ να εξάγω το bitmap σε μορφές εκτός του PNG;**  
A: Η μέθοδος `Bitmap.Save` υποστηρίζει JPEG, BMP, GIF και TIFF—απλώς αλλάξτε την επέκταση του αρχείου.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2026-02-04  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

---