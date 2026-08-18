---
date: 2026-08-01
description: Μάθετε πώς να δημιουργήσετε εικόνα bitmap C# και να σχεδιάσετε ορθογώνιο
  σε bitmap χρησιμοποιώντας Aspose.Drawing. Οδηγός βήμα‑βήμα για προγραμματιστές .NET.
keywords:
- create bitmap image c#
- draw rectangle on bitmap
- replace system.drawing
lastmod: 2026-08-01
linktitle: Σχεδίαση ορθογωνίων με Aspose.Drawing
og_description: Δημιουργήστε εικόνα bitmap C# και σχεδιάστε ορθογώνιο σε bitmap χρησιμοποιώντας
  Aspose.Drawing. Αυτό το tutorial δείχνει πώς να δημιουργήσετε, να μορφοποιήσετε
  και να αποθηκεύσετε γραφικά ορθογωνίου στο .NET.
og_image_alt: Guide to drawing rectangles on a bitmap with Aspose.Drawing for .NET
og_title: Δημιουργία εικόνας bitmap C# – Σχεδίαση ορθογωνίου με Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to create bitmap image C# and draw rectangle on bitmap using
    Aspose.Drawing. Step‑by‑step guide for .NET developers.
  headline: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)`
      before or after drawing the outline.
    question: Can I fill the rectangle with a solid color?
  - answer: Loop through a collection of `Rectangle` structs and call `DrawRectangle`
      for each iteration.
    question: How do I draw multiple rectangles?
  - answer: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform
      after.
    question: Is there a way to rotate the rectangle?
  - answer: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat`
      parameter.
    question: What image formats are supported for saving?
  - answer: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and
      later versions.
    question: Does Aspose.Drawing work on .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- create bitmap image
- Aspose.Drawing
- .NET graphics
- draw rectangle
title: Δημιουργία εικόνας bitmap C# – Σχεδίαση ορθογωνίου με Aspose.Drawing για .NET
url: /el/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Σχεδιάσετε Ορθογώνιο με το Aspose.Drawing για .NET

## Εισαγωγή

Σε αυτό το σεμινάριο θα μάθετε **πώς να σχεδιάζετε ορθογώνια** σχήματα ενώ θα εξοικειωθείτε επίσης με το **δημιουργία bitmap εικόνας C#** χρησιμοποιώντας το Aspose.Drawing. Είτε χρειάζεστε ένα απλό στοιχείο UI είτε ένα υψηλής ανάλυσης γραφικό για μια αναφορά, θα περάσουμε από τη δημιουργία ενός bitmap, τη διαμόρφωση ενός αντικειμένου graphics, το σχεδιασμό του ορθογωνίου και την αποθήκευση της τελικής εικόνας. Η προσέγγιση λειτουργεί σε Windows, Linux και macOS, και αντικαθιστά το παλαιότερο API `System.Drawing.Common` με μια πλήρως διασυνοριακή λύση.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη απαιτείται;** Aspose.Drawing for .NET  
- **Ποια μέθοδος σχεδιάζει το σχήμα;** `Graphics.DrawRectangle`  
- **Χρειάζομαι άδεια;** Μια δοκιμαστική έκδοση είναι δωρεάν· απαιτείται εμπορική άδεια για παραγωγή.  
- **Μπορώ να αλλάξω το μέγεθος του ορθογωνίου;** Ναι – προσαρμόστε τις παραμέτρους πλάτους, ύψους και θέσης.  
- **Είναι ο κώδικας συμβατός με .NET 6+;** Απόλυτα, το Aspose.Drawing υποστηρίζει σύγχρονες εκδόσεις .NET.

## Τι σημαίνει «πώς να σχεδιάσετε ορθογώνιο» στο πλαίσιο του Aspose.Drawing;

Το σχεδιασμό ενός ορθογωνίου με το Aspose.Drawing χρησιμοποιεί την κλάση `Graphics` για να αποδώσει ένα ορθογώνιο περίγραμμα ή γεμάτο σχήμα πάνω σε έναν bitmap καμβά. Αυτό παρέχει πλήρη έλεγχο στο μέγεθος, το χρώμα, το πάχος της γραμμής και τη μορφή εικόνας, καθιστώντας το ιδανικό για γραφικά εν κινήσει. Επειδή το Aspose.Drawing εκτελείται σε καθαρό διαχειριζόμενο κινητήρα, αποφεύγει τα περιοριστικά όρια του GDI+ του `System.Drawing.Common`.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για δημιουργία ορθογωνίου;

Το Aspose.Drawing σας επιτρέπει **να σχεδιάσετε ορθογώνιο σε bitmap** χωρίς καμία πλατφόρμα‑συγκεκριμένη DLL, και υποστηρίζει **30+ μορφές εξόδου** (συμπεριλαμβανομένων PNG, JPEG, BMP, GIF και TIFF). Μπορεί να επεξεργαστεί εικόνες έως **10.000 × 10.000 pixel** διατηρώντας τη χρήση μνήμης κάτω από **100 MB**, κάτι που είναι 2‑3× πιο αποδοτικό από την κληρονομική υλοποίηση System.Drawing.

## Προαπαιτούμενα

Πριν προχωρήσουμε στον κώδικα, βεβαιωθείτε ότι έχετε τα εξής:

- **Βιβλιοθήκη Aspose.Drawing** – κατεβάστε την από την επίσημη ιστοσελίδα [εδώ](https://releases.aspose.com/drawing/net/).  
- **Περιβάλλον Ανάπτυξης** – Visual Studio 2022 ή οποιοδήποτε IDE συμβατό με .NET.  
- **Βασικές Γνώσεις .NET** – εξοικείωση με τη σύνταξη C# και τη δομή του έργου.

## Εισαγωγή Ονομάτων Χώρων

Οι οδηγίες `using` φέρνουν τις απαραίτητες κλάσεις στο πεδίο ορατότητας. Απαιτούνται για οποιαδήποτε λειτουργία σχεδίασης.

```csharp
using System.Drawing;
```

## Βήμα 1: Δημιουργία Bitmap Εικόνας

`Bitmap` αντιπροσωπεύει μια εσωτερική ραστερική εικόνα στη μνήμη πάνω στην οποία μπορείτε να σχεδιάζετε. Η δημιουργία της ορίζει το μέγεθος του καμβά και τη μορφή pixel.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Βήμα 2: Δημιουργία Αντικειμένου Graphics

`Graphics` είναι η μηχανή που εκτελεί όλες τις εντολές σχεδίασης στην επιφάνεια του bitmap. Μόλις το αποκτήσετε, μπορείτε να αποδώσετε σχήματα, κείμενο και εικόνες.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Βήμα 3: Ορισμός Pen για το Ορθογώνιο

`Pen` καθορίζει το χρώμα περιγράμματος και το πάχος για το ορθογώνιο. Επίσης ελέγχει τα στυλ παύλας και τις ενώσεις γραμμών.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## Βήμα 4: Σχεδίαση Ορθογωνίου στο Bitmap

`Graphics.DrawRectangle` σχεδιάζει το ορθογώνιο χρησιμοποιώντας το προηγουμένως ορισμένο pen. Παρέχετε τις συντεταγμένες X, Y καθώς και το πλάτος και το ύψος για να τοποθετήσετε το σχήμα ακριβώς όπου το χρειάζεστε.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## Βήμα 5: Αποθήκευση της Σχεδιασμένης Εικόνας

Η μέθοδος `Bitmap.Save` γράφει την εικόνα στο δίσκο στη μορφή που επιλέγετε (π.χ., PNG, JPEG). Αυτό το βήμα δείχνει τη δυνατότητα **αποθήκευσης σχεδιασμένης εικόνας** και ολοκληρώνει το bitmap για επαναχρησιμοποίηση.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

Συγχαρητήρια! Ολοκληρώσατε με επιτυχία **πώς να σχεδιάσετε ορθογώνιο** χρησιμοποιώντας το Aspose.Drawing για .NET και μάθατε πώς να **δημιουργήσετε bitmap εικόνα C#** στη διαδικασία.

## Συνηθισμένα Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Λύση |
|----------|-------|------|
| Κενή έξοδος εικόνας | Το Bitmap δεν έχει αποδεσμευτεί ή το graphics δεν έχει αδειάσει | Καλέστε `graphics.Dispose();` πριν από την αποθήκευση, ή χρησιμοποιήστε ένα μπλοκ `using`. |
| Χαμηλής ποιότητας άκρα | Προεπιλεγμένη λειτουργία εξομάλυνσης | Ορίστε `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`. |
| Σφάλματα διαδρομής αρχείου | Μη έγκυρος φάκελος | Βεβαιωθείτε ότι ο φάκελος προορισμού υπάρχει ή χρησιμοποιήστε `Path.Combine` για να δημιουργήσετε ασφαλή διαδρομή. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να γεμίσω το ορθογώνιο με σταθερό χρώμα;**  
Α: Ναι, δημιουργήστε ένα `SolidBrush` και καλέστε `graphics.FillRectangle(brush, …)` πριν ή μετά το σχεδιασμό του περιγράμματος.

**Ε: Πώς μπορώ να σχεδιάσω πολλαπλά ορθογώνια;**  
Α: Κάντε βρόχο σε μια συλλογή από δομές `Rectangle` και καλέστε `DrawRectangle` για κάθε επανάληψη.

**Ε: Υπάρχει τρόπος να περιστρέψετε το ορθογώνιο;**  
Α: Χρησιμοποιήστε `graphics.RotateTransform(angle)` πριν το σχεδιασμό, και στη συνέχεια επαναφέρετε τον μετασχηματισμό.

**Ε: Ποιοι μορφές εικόνας υποστηρίζονται για αποθήκευση;**  
Α: PNG, JPEG, BMP, GIF και TIFF υποστηρίζονται όλες μέσω της κατάλληλης παραμέτρου `ImageFormat`.

**Ε: Λειτουργεί το Aspose.Drawing σε .NET Core;**  
Α: Ναι, η βιβλιοθήκη είναι πλήρως συμβατή με .NET Core, .NET 5, .NET 6 και μεταγενέστερες εκδόσεις.

---

**Τελευταία Ενημέρωση:** 2026-08-01  
**Δοκιμάστηκε Με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose  

---

## Σχετικά Σεμινάρια

- [Πώς να Σχεδιάσετε Έλλειψη με το Aspose.Drawing για .NET](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [Σχεδίαση πολλαπλών γραμμών με το Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [Πώς να δημιουργήσετε bitmap aspose.drawing – Σχεδίαση Πολυγώνων σε .NET](/drawing/net/lines-curves-and-shapes/draw-polygon/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}