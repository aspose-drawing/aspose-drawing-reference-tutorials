---
date: 2026-08-22
description: Μάθετε πώς να αποθηκεύσετε bitmap ως png χρησιμοποιώντας Aspose.Drawing
  για .NET με ένα παράδειγμα μετασχηματισμού πίνακα. Οδηγός βήμα‑βήμα με θέσεις κώδικα.
keywords:
- save bitmap as png
- matrix transformation example
- draw rotated ellipse
- convert graphics to png
- high quality png output
lastmod: 2026-08-22
linktitle: Τοπικός μετασχηματισμός στο Aspose.Drawing
og_description: Αποθήκευση bitmap ως png με Aspose.Drawing εφαρμόζοντας μετασχηματισμό
  πίνακα. Μάθετε μια βήμα‑βήμα ροή εργασίας που αποδίδει μια περιστρεφόμενη έλλειψη
  και παράγει PNG υψηλής ποιότητας.
og_image_alt: Screenshot of a rotated ellipse saved as a high‑quality PNG using Aspose.Drawing
og_title: Αποθήκευση bitmap ως png χρησιμοποιώντας μετασχηματισμό στο Aspose.Drawing
  – οδηγός .NET
schemas:
- author: Aspose
  dateModified: '2026-08-22'
  description: Learn how to save bitmap as png using Aspose.Drawing for .NET with
    a matrix transformation example. Step‑by‑step guide with code placeholders.
  headline: Save bitmap as png using transformation in Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as png using Aspose.Drawing for .NET with
    a matrix transformation example. Step‑by‑step guide with code placeholders.
  name: Save bitmap as png using transformation in Aspose.Drawing
  steps:
  - name: create a bitmap
    text: '`Bitmap` represents an in‑memory image with a defined pixel format and
      dimensions. > **Pro tip:** Using `Format32bppPArgb` ensures that the image retains
      premultiplied alpha, which is ideal for png output.'
  - name: create a graphics object
    text: '`Graphics` provides drawing methods that render shapes onto a bitmap.'
  - name: create a graphicspath
    text: '`GraphicsPath` allows you to define complex vector shapes such as ellipses,
      lines, and curves.'
  - name: apply local transformation (matrix transformation example)
    text: '`Matrix` encapsulates a 3×3 affine transformation matrix used for scaling,
      rotation, translation, and skewing. > **Why rotate around the centre?** Rotating
      around the shape’s centre prevents it from orbiting around the origin, giving
      a natural look.'
  - name: draw the transformed path
    text: '`Pen` defines the color, width, and style used to outline shapes when drawing.'
  - name: save the transformed image (convert graphics to png)
    text: '`Bitmap.Save` writes the image to a file in the specified format, such
      as PNG. > **Note:** The `.png` extension automatically triggers Aspose.Drawing’s
      PNG encoder, fulfilling the **save bitmap as png** requirement.'
  type: HowTo
- questions:
  - answer: Yes. Create a single `Matrix` and call methods like `Scale`, `RotateAt`,
      and `Translate` in the order you need, then apply it with `path.Transform(matrix);`.
    question: Can I chain multiple transformations (e.g., scale then rotate)?
  - answer: Absolutely. The library processes 200‑page images in under 2 seconds on
      typical server hardware and avoids the GDI+ limitations on non‑Windows platforms.
    question: Is Aspose.Drawing suitable for high‑performance rendering?
  - answer: Besides rotation, you can perform translation, scaling, and skewing using
      the same `Matrix` class.
    question: What other transformation types are supported?
  - answer: Wrap the drawing code in a `try‑catch` block and inspect `System.Drawing.Drawing2D`
      exceptions. Refer to the official [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/)
      for detailed error‑handling guidance.
    question: How do I handle exceptions during the transformation process?
  - answer: Yes, a fully functional free trial is available via the [download link](https://releases.aspose.com/drawing/net/).
    question: Can I try Aspose.Drawing before purchasing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics transformation
- PNG rendering
- matrix transformation
title: Αποθήκευση bitmap ως png χρησιμοποιώντας μετασχηματισμό στο Aspose.Drawing
url: /el/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση bitmap ως png χρησιμοποιώντας μετασχηματισμό στο Aspose.Drawing

## Εισαγωγή

Εάν χρειάζεστε **save bitmap as png** ενώ εφαρμόζετε έναν τοπικό μετασχηματισμό σε γραφικά μέσα σε μια εφαρμογή .NET, το Aspose.Drawing κάνει τη διαδικασία απλή και αξιόπιστη. Σε αυτό το tutorial θα δείτε ακριβώς πώς να εφαρμόσετε έναν πίνακα μετασχηματισμού σε ένα σχήμα, να αποδώσετε το αποτέλεσμα και τελικά **convert graphics to png** για αποθήκευση ή περαιτέρω επεξεργασία. Στο τέλος, θα έχετε ένα επαναχρησιμοποιήσιμο πρότυπο κώδικα που μπορείτε να προσαρμόσετε σε οποιοδήποτε σενάριο τοπικού μετασχηματισμού.

## Γρήγορες απαντήσεις
- **Τι είναι ένας τοπικός μετασχηματισμός;** Είναι μια λειτουργία βασισμένη σε πίνακα (rotate, scale, translate, skew) που εφαρμόζεται σε ένα συγκεκριμένο στοιχείο σχεδίασης χωρίς να επηρεάζει ολόκληρο το καμβά.  
- **Ποια βιβλιοθήκη το υποστηρίζει στο .NET;** Aspose.Drawing for .NET παρέχει ένα πλήρες API που λειτουργεί σε όλες τις υποστηριζόμενες εκδόσεις .NET.  
- **Μπορώ να αποθηκεύσω το αποτέλεσμα ως png;** Ναι—καλέστε `Bitmap.Save` με όνομα αρχείου “.png” και το Aspose.Drawing διαχειρίζεται τη μετατροπή αυτόματα.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για χρήση σε παραγωγή.  
- **Πόσο διαρκεί η υλοποίηση;** Περίπου 10‑15 λεπτά για ένα βασικό παράδειγμα.

## Πώς να αποθηκεύσετε bitmap ως png

Παρακάτω θα βρείτε έναν πλήρη, βήμα‑βήμα οδηγό που παρουσιάζει ένα **matrix transformation example** και καταλήγει σε ένα **high quality png output**.

## Τι σημαίνει «πώς να εφαρμόσετε μετασχηματισμό» στον προγραμματισμό γραφικών;

Η εφαρμογή ενός μετασχηματισμού σημαίνει την τροποποίηση του συστήματος συντεταγμένων ενός αντικειμένου σχεδίασης χρησιμοποιώντας μια **Matrix**. Η μήτρα (matrix) ορίζει πώς τα σημεία περιστρέφονται, κλιμακώνονται ή μετακινούνται, επιτρέποντάς σας να δημιουργήσετε σύνθετα οπτικά εφέ με ελάχιστο κώδικα ενώ διατηρείτε την ακρίβεια των εικονοστοιχείων. Λειτουργεί ομοιόμορφα σε όλες τις πλατφόρμες .NET, εξασφαλίζοντας συνεπή αποτελέσματα.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για μετατροπή γραφικών σε png;

Το Aspose.Drawing παρέχει μια δια‑πλατφορμική, χωρίς GDI μηχανή που αποδίδει αρχεία PNG στα 300 dpi με βάθος χρώματος 32‑bit, εγγυώντας απώλεστική, υψηλής ποιότητας png έξοδο. Η βιβλιοθήκη υποστηρίζει **50+ input and output formats** και λειτουργεί σε .NET Framework, .NET Core, και .NET 5/6+, εξαλείφοντας εξαρτήσεις ειδικές για πλατφόρμα.

## Προαπαιτούμενα

1. **Aspose.Drawing for .NET** – κατεβάστε και εγκαταστήστε από το [σύνδεσμος λήψης](https://releases.aspose.com/drawing/net/).  
2. Ένας φάκελος στον υπολογιστή σας όπου θα αποθηκευτεί η εικόνα εξόδου (π.χ., `C:\MyImages\`).  
3. Βασική εξοικείωση με τη C# και τη ρύθμιση έργου .NET.  

## Εισαγωγή namespaces

Πρώτα, φέρτε τα απαιτούμενα namespaces στο αρχείο C# σας:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Αυτά τα namespaces σας δίνουν πρόσβαση στις κλάσεις `Bitmap`, `Graphics`, `GraphicsPath` και `Matrix` που απαιτούνται για τη ροή εργασίας του μετασχηματισμού.

## Οδηγός βήμα‑βήμα

### Βήμα 1: δημιουργία bitmap

`Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη με καθορισμένη μορφή εικονοστοιχείων και διαστάσεις.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Συμβουλή:** Η χρήση του `Format32bppPArgb` εξασφαλίζει ότι η εικόνα διατηρεί αλφα προ‑πολλαπλασιασμένο, κάτι που είναι ιδανικό για έξοδο png.

### Βήμα 2: δημιουργία αντικειμένου graphics

`Graphics` παρέχει μεθόδους σχεδίασης που αποδίδουν σχήματα σε ένα bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Βήμα 3: δημιουργία graphicspath

`GraphicsPath` σας επιτρέπει να ορίσετε σύνθετα διανυσματικά σχήματα όπως έλλειψη, γραμμές και καμπύλες.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### Βήμα 4: εφαρμογή τοπικού μετασχηματισμού (matrix transformation example)

`Matrix` ενσωματώνει μια 3×3 affine μήτρα μετασχηματισμού που χρησιμοποιείται για κλιμάκωση, περιστροφή, μετάφραση και παραμόρφωση.

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **Γιατί να περιστρέφετε γύρω από το κέντρο;** Η περιστροφή γύρω από το κέντρο του σχήματος αποτρέπει την περιφορά γύρω από το αρχικό σημείο, δίνοντας φυσική εμφάνιση.

### Βήμα 5: σχεδίαση του μετασχηματισμένου path

`Pen` ορίζει το χρώμα, το πλάτος και το στυλ που χρησιμοποιούνται για το περίγραμμα των σχημάτων κατά τη σχεδίαση.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### Βήμα 6: αποθήκευση της μετασχηματισμένης εικόνας (convert graphics to png)

`Bitmap.Save` γράφει την εικόνα σε αρχείο στην καθορισμένη μορφή, όπως PNG.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **Σημείωση:** Η επέκταση `.png` ενεργοποιεί αυτόματα τον κωδικοποιητή PNG του Aspose.Drawing, ικανοποιώντας την απαίτηση **save bitmap as png**.

## Κοινά προβλήματα & λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Κενή εικόνα εξόδου** | Το Graphics δεν έχει καθαριστεί ή το χρώμα του pen ταιριάζει με το φόντο | Καλέστε `graphics.Clear` με ένα αντίθετο χρώμα και βεβαιωθείτε ότι το χρώμα του pen είναι ορατό. |
| **Παραμορφωμένη περιστροφή** | Χρήση του `Rotate` αντί του `RotateAt` | Χρησιμοποιήστε `RotateAt` και καθορίστε το κεντρικό σημείο του σχήματος. |
| **Το αρχείο δεν αποθηκεύτηκε** | Μη έγκυρη διαδρομή φακέλου ή έλλειψη δικαιωμάτων εγγραφής | Επαληθεύστε ότι ο φάκελος υπάρχει και η εφαρμογή έχει δικαιώματα εγγραφής. |
| **Το PNG φαίνεται θολό** | Χαμηλή ρύθμιση DPI στο bitmap | Δημιουργήστε το bitmap με υψηλότερη ανάλυση ή ορίστε `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Συχνές ερωτήσεις

**Q: Μπορώ να συνδυάσω πολλαπλούς μετασχηματισμούς (π.χ., κλιμάκωση και μετά περιστροφή);**  
A: Ναι. Δημιουργήστε ένα μόνο `Matrix` και καλέστε μεθόδους όπως `Scale`, `RotateAt` και `Translate` με τη σειρά που χρειάζεστε, έπειτα εφαρμόστε το με `path.Transform(matrix);`.

**Q: Είναι το Aspose.Drawing κατάλληλο για υψηλής απόδοσης rendering;**  
A: Απόλυτα. Η βιβλιοθήκη επεξεργάζεται εικόνες 200‑σελίδων σε λιγότερο από 2 δευτερόλεπτα σε τυπικό εξοπλισμό διακομιστή και αποφεύγει τους περιορισμούς του GDI+ σε μη‑Windows πλατφόρμες.

**Q: Τι άλλους τύπους μετασχηματισμού υποστηρίζει;**  
A: Εκτός από την περιστροφή, μπορείτε να εκτελέσετε μετάφραση, κλιμάκωση και παραμόρφωση χρησιμοποιώντας την ίδια κλάση `Matrix`.

**Q: Πώς να διαχειριστώ εξαιρέσεις κατά τη διαδικασία του μετασχηματισμού;**  
A: Τυλίξτε τον κώδικα σχεδίασης σε ένα μπλοκ `try‑catch` και εξετάστε τις εξαιρέσεις του `System.Drawing.Drawing2D`. Ανατρέξτε στην επίσημη [τεκμηρίωση Aspose.Drawing](https://reference.aspose.com/drawing/net/) για λεπτομερείς οδηγίες διαχείρισης σφαλμάτων.

**Q: Μπορώ να δοκιμάσω το Aspose.Drawing πριν την αγορά;**  
A: Ναι, μια πλήρως λειτουργική δωρεάν δοκιμή είναι διαθέσιμη μέσω του [σύνδεσμου λήψης](https://releases.aspose.com/drawing/net/).

## Συμπέρασμα

Ακολουθώντας αυτόν τον οδηγό, τώρα γνωρίζετε **how to save bitmap as png** μετά την εφαρμογή ενός τοπικού μετασχηματισμού με το Aspose.Drawing για .NET. Το ίδιο πρότυπο μπορεί να επαναχρησιμοποιηθεί για κλιμάκωση, μετάφραση ή παραμόρφωση οποιουδήποτε σχήματος, δίνοντάς σας τη δυνατότητα να δημιουργήσετε πλούσια, διαδραστικά οπτικά στοιχεία στις εφαρμογές σας ενώ παρέχετε υψηλής ποιότητας PNG έξοδο.

---

**Last Updated:** 2026-08-22  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Σχετικές οδηγίες

- [Οδηγός Μετασχηματισμού Μήτρας: Matrix Transformations στο Aspose.Drawing για .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Πώς να αποθηκεύσετε PNG με Aspose.Drawing – World Transformation](/drawing/net/coordinate-transformations/world-transformation/)
- [Φόρτωση, Μετατροπή BMP σε PNG και άλλες μορφές με Aspose.Drawing](/drawing/net/image-editing/load-save/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}