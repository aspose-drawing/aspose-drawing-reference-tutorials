---
date: 2026-10-29
description: Μάθετε πώς να αποθηκεύσετε bitmap ως png χρησιμοποιώντας το Aspose.Drawing
  για .NET με παράδειγμα μετασχηματισμού πίνακα. Οδηγός βήμα‑βήμα με code placeholders.
images:
- /net/coordinate-transformations/local-transformation/og-image.png
keywords:
- save bitmap as png
- affine transformation matrix
- draw rotated ellipse
- convert graphics to png
- define vector shapes
lastmod: 2026-10-29
linktitle: Τοπικός μετασχηματισμός στο Aspose.Drawing
og_description: Αποθήκευση bitmap ως png με το Aspose.Drawing εφαρμόζοντας μετασχηματισμό
  πίνακα. Αυτός ο οδηγός δείχνει πώς να αποδώσετε μια περιστραμμένη ellipse και να
  παραγάγετε ένα PNG υψηλής ποιότητας σε .NET.
og_image_alt: Screenshot of a rotated ellipse saved as a high‑quality PNG using Aspose.Drawing
og_title: Αποθήκευση bitmap ως png με μετασχηματισμό χρησιμοποιώντας το Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-10-29'
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
  - answer: Absolutely. The library processes 200‑page images in under 2 seconds on
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

Αν χρειάζεστε να **save bitmap as png** εφαρμόζοντας έναν τοπικό μετασχηματισμό στα γραφικά μέσα σε μια εφαρμογή .NET, το Aspose.Drawing καθιστά τη διαδικασία απλή και αξιόπιστη. Σε αυτό το tutorial θα δείτε ακριβώς πώς να εφαρμόσετε έναν πίνακα μετασχηματισμού σε ένα σχήμα, να αποδώσετε το αποτέλεσμα και τελικά να **convert graphics to png** για αποθήκευση ή περαιτέρω επεξεργασία. Στο τέλος, θα έχετε ένα επαναχρησιμοποιήσιμο πρότυπο κώδικα που μπορείτε να προσαρμόσετε σε οποιοδήποτε σενάριο τοπικού μετασχηματισμού.

## Γρήγορες απαντήσεις
- **Τι είναι ένας τοπικός μετασχηματισμός;** Είναι μια λειτουργία βασισμένη σε πίνακα (rotate, scale, translate, skew) που εφαρμόζεται σε ένα συγκεκριμένο στοιχείο σχεδίασης χωρίς να επηρεάζει ολόκληρο το καμβά.  
- **Ποια βιβλιοθήκη το υποστηρίζει στο .NET;** Aspose.Drawing for .NET παρέχει μια πλήρη API που λειτουργεί σε όλες τις υποστηριζόμενες εκδόσεις .NET.  
- **Μπορώ να αποθηκεύσω το αποτέλεσμα ως png;** Ναι—καλέστε `Bitmap.Save` με όνομα αρχείου “.png” και το Aspose.Drawing διαχειρίζεται αυτόματα τη μετατροπή.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγική χρήση.  
- **Πόσο χρόνο διαρκεί η υλοποίηση;** Περίπου 10‑15 λεπτά για ένα βασικό παράδειγμα.

## Πώς να αποθηκεύσετε bitmap ως png

Φορτώστε ένα `Bitmap`, εφαρμόστε ένα `Matrix` σε ένα `GraphicsPath`, σχεδιάστε το μετασχηματισμένο μονοπάτι με ένα `Pen` και τελικά καλέστε `Bitmap.Save("output.png", ImageFormat.Png)`. Αυτή η σύντομη ροή εργασίας παράγει ένα PNG υψηλής ποιότητας με λίγες μόνο γραμμές κώδικα και λειτουργεί σε Windows, Linux και macOS επειδή το Aspose.Drawing είναι εντελώς GDI‑free.

`Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη.  
`Matrix` ορίζει έναν αφαιρετικό (affine) μετασχηματισμό που χρησιμοποιείται για κλιμάκωση, περιστροφή, μετάφραση και παραμόρφωση.  
`GraphicsPath` περιέχει μια σειρά από γραμμές και καμπύλες που ορίζουν ένα σχήμα.  
`Pen` καθορίζει πώς σχεδιάζονται τα περιγράμματα, συμπεριλαμβανομένου του χρώματος και του πλάτους.  
`Bitmap.Save` γράφει την εικόνα σε ένα αρχείο σε καθορισμένη μορφή.

## Τι σημαίνει “πώς να εφαρμόσετε μετασχηματισμό” στον προγραμματισμό γραφικών;

Η εφαρμογή ενός μετασχηματισμού σημαίνει την τροποποίηση του συστήματος συντεταγμένων ενός αντικειμένου σχεδίασης χρησιμοποιώντας ένα **Matrix**. Ο πίνακας ορίζει πώς τα σημεία περιστρέφονται, κλιμακώνονται ή μετακινούνται, επιτρέποντάς σας να δημιουργήσετε σύνθετα οπτικά εφέ με ελάχιστο κώδικα ενώ διατηρείτε την ακρίβεια των pixel. Λειτουργεί ομοιόμορφα σε όλες τις πλατφόρμες .NET, εξασφαλίζοντας συνεπή αποτελέσματα.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για να μετατρέψετε γραφικά σε png;

Το Aspose.Drawing παρέχει μια跨平台, GDI‑free μηχανή που αποδίδει αρχεία PNG σε 300 dpi με βάθος χρώματος 32‑bit, εξασφαλίζοντας απώλεια‑απαλλαγή, υψηλής ποιότητας έξοδο. Υποστηρίζει **50+ formats** και λειτουργεί σε .NET Framework, .NET Core και .NET 5/6+, αφαιρώντας εξαρτήσεις ειδικές για πλατφόρμα. Τα benchmarks δείχνουν ότι μια εικόνα 4 K × 4 K επεξεργάζεται σε λιγότερο από 120 ms, κατάλληλη για σενάρια υψηλής απόδοσης.

## Προαπαιτούμενα

1. **Aspose.Drawing for .NET** – κατεβάστε και εγκαταστήστε από το [download link](https://releases.aspose.com/drawing/net/).  
2. Ένας φάκελος στον υπολογιστή σας όπου θα αποθηκευτεί η εικόνα εξόδου (π.χ., `C:\MyImages\`).  
3. Βασική εξοικείωση με τη C# και τη ρύθμιση έργου .NET.  

## Εισαγωγή ονομάτων χώρων

Πρώτα, εισάγετε τα απαιτούμενα namespaces στο αρχείο C# σας:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Αυτά τα namespaces σας δίνουν πρόσβαση στις κλάσεις `Bitmap`, `Graphics`, `GraphicsPath` και `Matrix` που απαιτούνται για τη ροή εργασίας του μετασχηματισμού.

## Οδηγός βήμα‑βήμα

### Βήμα 1: δημιουργία bitmap

`Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη με ορισμένη μορφή pixel και διαστάσεις.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Συμβουλή:** Η χρήση του `Format32bppPArgb` εξασφαλίζει ότι η εικόνα διατηρεί το προ-πολλαπλασιασμένο άλφα, κάτι που είναι ιδανικό για έξοδο png.

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

### Βήμα 4: εφαρμογή τοπικού μετασχηματισμού (παράδειγμα μετασχηματισμού matrix)

`Matrix` ενσωματώνει έναν 3×3 αφαιρετικό (affine) πίνακα μετασχηματισμού που χρησιμοποιείται για κλιμάκωση, περιστροφή, μετάφραση και παραμόρφωση.

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **Γιατί να περιστρέφετε γύρω από το κέντρο;** Η περιστροφή γύρω από το κέντρο του σχήματος αποτρέπει την περιφορά γύρω από το αρχικό σημείο, δίνοντας μια φυσική εμφάνιση.

### Βήμα 5: σχεδίαση του μετασχηματισμένου μονοπατιού

`Pen` ορίζει το χρώμα, το πλάτος και το στυλ που χρησιμοποιείται για το περίγραμμα των σχημάτων κατά τη σχεδίαση.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### Βήμα 6: αποθήκευση της μετασχηματισμένης εικόνας (μετατροπή γραφικών σε png)

`Bitmap.Save` γράφει την εικόνα σε ένα αρχείο στην καθορισμένη μορφή, όπως PNG.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **Σημείωση:** Η επέκταση `.png` ενεργοποιεί αυτόματα τον κωδικοποιητή PNG του Aspose.Drawing, ικανοποιώντας την απαίτηση **save bitmap as png**.

## Κοινά προβλήματα & λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Κενή εικόνα εξόδου** | Graphics not cleared or pen color matches background | Call `graphics.Clear` with a contrasting color and ensure the pen color is visible. |
| **Παραμορφωμένη περιστροφή** | Using `Rotate` instead of `RotateAt` | Use `RotateAt` and specify the centre point of the shape. |
| **Το αρχείο δεν αποθηκεύτηκε** | Invalid directory path or missing write permissions | Verify the directory exists and the application has write access. |
| **Το PNG φαίνεται θολό** | Low DPI setting on the bitmap | Create the bitmap with a higher resolution or set `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να συνδυάσω πολλαπλούς μετασχηματισμούς (π.χ., κλιμάκωση και μετά περιστροφή);**  
Α: Ναι. Δημιουργήστε ένα ενιαίο `Matrix` και καλέστε μεθόδους όπως `Scale`, `RotateAt` και `Translate` με τη σειρά που χρειάζεστε, στη συνέχεια εφαρμόστε το με `path.Transform(matrix);`.

**Ε: Είναι το Aspose.Drawing κατάλληλο για υψηλής απόδοσης απόδοση;**  
Α: Απόλυτα. Η βιβλιοθήκη επεξεργάζεται εικόνες 200‑σελίδων σε λιγότερο από 2 δευτερόλεπτα σε τυπικό εξοπλισμό διακομιστή και αποφεύγει τους περιορισμούς του GDI+ σε πλατφόρμες εκτός Windows.

**Ε: Τι άλλοι τύποι μετασχηματισμού υποστηρίζονται;**  
Α: Εκτός από την περιστροφή, μπορείτε να εκτελέσετε μετάφραση, κλιμάκωση και παραμόρφωση χρησιμοποιώντας την ίδια κλάση `Matrix`.

**Ε: Πώς να διαχειριστώ εξαιρέσεις κατά τη διάρκεια της διαδικασίας μετασχηματισμού;**  
Α: Τυλίξτε τον κώδικα σχεδίασης σε ένα μπλοκ `try‑catch` και εξετάστε τις εξαιρέσεις `System.Drawing.DrawingD2`. Ανατρέξτε στην επίσημη [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/) για λεπτομερείς οδηγίες διαχείρισης σφαλμάτων.

**Ε: Μπορώ να δοκιμάσω το Aspose.Drawing πριν το αγοράσω;**  
Α: Ναι, μια πλήρως λειτουργική δωρεάν δοκιμή είναι διαθέσιμη μέσω του [download link](https://releases.aspose.com/drawing/net/).

## Συμπέρασμα

Ακολουθώντας αυτόν τον οδηγό, τώρα γνωρίζετε **how to save bitmap as png** μετά την εφαρμογή ενός τοπικού μετασχηματισμού με το Aspose.Drawing για .NET. Το ίδιο πρότυπο μπορεί να επαναχρησιμοποιηθεί για κλιμάκωση, μετάφραση ή παραμόρφωση οποιουδήποτε σχήματος, δίνοντάς σας τη δυνατότητα να δημιουργήσετε πλούσια, διαδραστικά οπτικά στοιχεία στις εφαρμογές σας ενώ παρέχετε έξοδο PNG υψηλής ποιότητας.

---

**Τελευταία ενημέρωση:** 2026-10-29  
**Δοκιμή με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose

## Σχετικές οδηγίες

- [Μάθημα Μετασχηματισμού Πίνακα: Matrix Transformations στο Aspose.Drawing για .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Πώς να αποθηκεύσετε PNG με το Aspose.Drawing – Παγκόσμιος Μετασχηματισμός](/drawing/net/coordinate-transformations/world-transformation/)
- [Φόρτωση, Μετατροπή BMP σε PNG και Άλλες Μορφές με το Aspose.Drawing](/drawing/net/image-editing/load-save/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}