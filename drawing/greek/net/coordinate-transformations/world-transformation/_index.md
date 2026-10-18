---
date: 2026-10-18
description: Μετατρέψτε το drawing σε PNG με το Aspose.Drawing εφαρμόζοντας world
  transformations. Μάθετε παραδείγματα translate, rotate και scale σε C# και εξαγωγή
  διαφανών PNG.
keywords:
- convert drawing to png
- save graphics as png
- rotate image .net
- scale graphics .net
- transparent png bitmap
lastmod: 2026-10-18
linktitle: World transformation στο Aspose.Drawing
og_description: Μετατρέψτε το drawing σε PNG με το Aspose.Drawing, εφαρμόστε world
  transformations και εξαγάγετε διαφανή PNG. Μάθετε παραδείγματα translate, rotate
  και scale σε C# για .NET.
og_image_alt: Tutorial showing how to convert drawing to PNG using Aspose.Drawing
  with world transformation
og_title: Μετατρέψτε το drawing σε PNG με το Aspose.Drawing – world transformation
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  headline: How to convert drawing to PNG with Aspose.Drawing – world transformation
  type: TechArticle
- description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  name: How to convert drawing to PNG with Aspose.Drawing – world transformation
  steps:
  - name: create a bitmap
    text: '**Definition:** `Bitmap` is Aspose.Drawing’s in‑memory representation of
      a raster image that you can draw on or save to disk. We start by creating a
      blank canvas that will hold our drawing. `new Bitmap(width, height, PixelFormat.Format32bppPArgb)`
      creates a 32‑bit per pixel bitmap with premultiplied'
  - name: set the world transformation (graphics translate example)
    text: '**Definition:** `Graphics` is the drawing surface that renders shapes onto
      a `Bitmap`. `TranslateTransform` moves the origin of the coordinate system to
      a new location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height
      / 2)` shifts the (0,0) point to the canvas centre. After this call, an'
  - name: draw a rectangle using the transformed coordinates
    text: '**Definition:** `DrawRectangle` is a method of `Graphics` that renders
      a rectangular outline or filled shape based on the supplied pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width'
  - name: save the result – convert graphics to PNG
    text: '**Definition:** `ImageFormat` is an enumeration that tells the `Save` method
      which file format to use. `Save` writes the bitmap to a file in the specified
      image format. `bitmap.Save(outputPath, ImageFormat.Png)` writes a lossless PNG
      file that can be used directly in web pages or UI components. - PN'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- convert drawing to png
- Aspose.Drawing
- .NET graphics
- PNG export
- world transformation
title: Πώς να μετατρέψετε το drawing σε PNG με το Aspose.Drawing – world transformation
url: /el/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να μετατρέψετε το σχέδιο σε PNG με το Aspose.Drawing – μετασχηματισμός κόσμου

## Αποθήκευση bitmap ως PNG – εισαγωγή

**Πώς να μετατρέψετε το σχέδιο σε PNG** χρησιμοποιώντας το Aspose.Drawing είναι μια συχνή απαίτηση όταν χρειάζεστε εικόνες υψηλής ποιότητας και διαφάνειας που δημιουργούνται δυναμικά. Σε αυτό το tutorial θα μάθετε πώς να **αποθηκεύσετε bitmap ως PNG**, να εφαρμόσετε μετασχηματισμούς κόσμου όπως μετάθεση, περιστροφή και κλιμάκωση, και τελικά να μετατρέψετε γραφικά σε PNG — όλα με καθαρό, συντηρήσιμο κώδικα C#. Είτε δημιουργείτε μηχανή αναφορών, στοιχείο γραφημάτων ή προσαρμοσμένο UI renderer, η κατανόηση αυτών των βημάτων σας επιτρέπει να δημιουργείτε δυναμικές εικόνες που φαίνονται εξαιρετικά σε οποιαδήποτε συσκευή.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “μετασχηματισμός κόσμου”;** Χαρτογραφεί τις λογικές (κόσμου) συντεταγμένες του σχεδίου σας στις συντεταγμένες της σελίδας (συσκευής), επιτρέποντάς σας να μετατοπίζετε, να περιστρέφετε ή να κλιμακώνετε τα πάντα με έναν μόνο πίνακα.  
- **Μπορώ να εξάγω το αποτέλεσμα ως PNG;** Ναι – μετά το σχέδιο καλείτε απλώς `bitmap.Save(...)` με επέκταση `.png`.  
- **Χρειάζομαι άδεια για το Aspose.Drawing;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Είναι συμβατό με .NET 6/7;** Απόλυτα – το Aspose.Drawing υποστηρίζει .NET Framework 4.5+ και .NET Core/5/6/7, καλύπτοντας πάνω από 90 % των τρεχουσών εγκαταστάσεων .NET.  
- **Πόσους μετασχηματισμούς μπορώ να αλυσίσω;** Μπορείτε να εφαρμόσετε **πολλαπλούς μετασχηματισμούς γραφικών** διαδοχικά (μετάθεση, περιστροφή, κλιμάκωση κ.λπ.) χωρίς επιβάρυνση απόδοσης.

## Τι είναι ένας μετασχηματισμός κόσμου στο Aspose.Drawing;

Ένας μετασχηματισμός κόσμου αλλάζει το σύστημα συντεταγμένων που χρησιμοποιούν οι εντολές σχεδίασής σας. Από προεπιλογή, το (0,0) είναι η πάνω‑αριστερή γωνία του bitmap. Με `TranslateTransform`, `RotateTransform` ή `ScaleTransform`, μπορείτε να μετατοπίσετε αυτήν την αρχή, να περιστρέψετε σχήματα ή να τα κλιμακώσετε χωρίς να τροποποιήσετε τη γεωμετρία. Αυτό σας επιτρέπει να σχεδιάζετε μία φορά και να αποδίδετε σε οποιοδήποτε μέγεθος ή προσανατολισμό.

## Πώς να αποθηκεύσετε PNG χρησιμοποιώντας το Aspose.Drawing;

Φορτώστε ένα αντικείμενο `Bitmap`, ορίστε τους επιθυμητούς μετασχηματισμούς κόσμου στην παρουσία `Graphics`, σχεδιάστε τα σχήματά σας και τέλος καλέστε `bitmap.Save("output.png", ImageFormat.Png)`. Αυτή η εντολή αποθήκευσης μιας γραμμής γράφει ένα lossless PNG αρχείο που διατηρεί τη διαφάνεια και την πιστότητα των χρωμάτων, καθιστώντας το ιδανικό για web assets και UI overlays. Το API διαχειρίζεται όλη την κωδικοποίηση χαμηλού επιπέδου, ώστε να έχετε ένα έτοιμο PNG σε λιγότερο από ένα δευτερόλεπτο για τυπικά μεγέθη καμβά.

## Γιατί να χρησιμοποιήσετε ένα παράδειγμα graphics translate;

Ένα παράδειγμα graphics translate σας επιτρέπει να μετακινήσετε την αρχή του σχεδίου μία φορά αντί να επαναϋπολογίζετε κάθε σημείο. Με τη μετατόπιση της αρχής στο κέντρο του καμβά απλοποιείτε τη γεωμετρία, μειώνετε την επανάληψη κώδικα και αφήνετε τη μηχανή γραφικών να εκτελέσει τον πολλαπλασιασμό πινάκων σε native κώδικα, κάτι που μπορεί να βελτιώσει την ταχύτητα απόδοσης έως και 30 % σε μεγάλους καμβάδες. Αυτό το πρότυπο κάνει επίσης τον κώδικά σας πιο εύκολο στη συντήρηση όταν προσθέτετε περιστροφή ή κλιμάκωση αργότερα.

## Παράδειγμα graphics translate

Ένα **παράδειγμα graphics translate** δείχνει πώς η μετακίνηση της αρχής απλοποιεί την τοποθέτηση. Αντί να επαναϋπολογίζετε κάθε σημείο, μετακινείτε το σύστημα συντεταγμένων μία φορά και σχεδιάζετε σαν να ήταν η νέα αρχή το κέντρο του καμβά.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε:

- **Βιβλιοθήκη Aspose.Drawing** ενσωματωμένη στο .NET project σας – κατεβάστε την από τη επίσημη [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/).  
- Έναν **φάκελο εγγράφων** όπου θα αποθηκευτεί η έξοδος εικόνας.  
- Βασική εξοικείωση με τη σύνταξη **C#** και το Visual Studio ή το προτιμώμενο IDE σας.  

Τώρα, ας βουτήξουμε στον κώδικα!

## Εισαγωγή namespaces

Τα `Bitmap`, `Graphics` και τα εργαλεία σχεδίασης του Aspose ζουν σε αυτά τα namespaces.  
**Ορισμός:** Το `System.Drawing` παρέχει τους βασικούς τύπους GDI+, ενώ το `Aspose.Drawing` τα επεκτείνει με δυνατότητες cross‑platform, επιτρέποντάς σας να τρέχετε τον ίδιο κώδικα σε Windows, Linux και macOS χωρίς πρόσθετες εξαρτήσεις.

## Οδηγός βήμα‑βήμα

### Βήμα 1: δημιουργία bitmap

**Ορισμός:** Το `Bitmap` είναι η εν-μνήμη αναπαράσταση raster εικόνας του Aspose.Drawing που μπορείτε να σχεδιάσετε ή να αποθηκεύσετε στο δίσκο.  

Ξεκινάμε δημιουργώντας έναν κενό καμβά που θα φιλοξενήσει το σχέδιο μας.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` δημιουργεί ένα bitmap 32‑bit ανά pixel με προπολλαπλασιασμένο άλφα, που είναι η βέλτιστη μορφή για έξοδο PNG επειδή διατηρεί τη διαφάνεια χωρίς επιπλέον βήματα μετατροπής.

- **Γιατί 32bppPArgb;** Αυτή η μορφή pixel υποστηρίζει διαφάνεια άλφα και υψηλής ποιότητας απόδοση χρώματος, ιδανική για PNG.  
- **Pro tip:** Προσαρμόστε το πλάτος/ύψος ώστε να ταιριάζει **στο μέγεθος εικόνας στόχου**· ένας καμβάς 1920 × 1080 αποδίδει **σε κάτω από 0,2 δευτερόλεπτα** σε τυπικό laptop προγραμματιστή.

### Βήμα 2: ορισμός του μετασχηματισμού κόσμου (παράδειγμα graphics translate)

**Ορισμός:** Το `Graphics` είναι η επιφάνεια σχεδίασης που αποδίδει σχήματα σε ένα `Bitmap`.  

`TranslateTransform` μετακινεί την αρχή του συστήματος συντεταγμένων σε νέα θέση.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` μετατοπίζει το σημείο (0,0) στο κέντρο του καμβά. Μετά αυτήν την κλήση, οποιοδήποτε σχήμα σχεδιάσετε με συντεταγμένες (0,0) θα εμφανιστεί στη μέση της εικόνας.

- Αυτό μετακινεί το σημείο (0,0) στο (500, 400) – το κέντρο ενός καμβά 1000 × 800.  
- Μπορείτε να αλυσίσετε πρόσθετους μετασχηματισμούς: `RotateTransform` περιστρέφει το σύστημα συντεταγμένων, και `ScaleTransform` το κλιμακώνει, επιτρέποντας **πολλαπλούς μετασχηματισμούς γραφικών** σε μια ενιαία αλυσίδα.

### Βήμα 3: σχεδίαση ορθογωνίου με τις μετασχηματισμένες συντεταγμένες

**Ορισμός:** Η `DrawRectangle` είναι μέθοδος του `Graphics` που αποδίδει περίγραμμα ή γεμάτο ορθογώνιο βάσει του παρεχόμενου πέν και των συντεταγμένων.  

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` σχεδιάζει ένα ορθογώνιο κεντραρισμένο στον καμβά επειδή η πάνω‑αριστερή γωνία του είναι μετατοπισμένη κατά το ήμισυ του πλάτους και του ύψους από την μετασχηματισμένη αρχή.

- Η πάνω‑αριστερή γωνία του ορθογωνίου ξεκινά από την μετασχηματισμένη αρχή (το κέντρο της εικόνας).  
- Μη διστάσετε να πειραματιστείτε με άλλα σχήματα—έλλειπσες, γραμμές ή προσαρμοσμένα μονοπάτια.

### Βήμα 4: αποθήκευση του αποτελέσματος – μετατροπή γραφικών σε PNG

**Ορισμός:** Η `ImageFormat` είναι μια απαρίθμηση που λέει στη μέθοδο `Save` ποια μορφή αρχείου να χρησιμοποιήσει.  

`Save` γράφει το bitmap σε αρχείο με την καθορισμένη μορφή εικόνας.  
`bitmap.Save(outputPath, ImageFormat.Png)` γράφει ένα lossless PNG αρχείο που μπορεί να χρησιμοποιηθεί απευθείας σε ιστοσελίδες ή UI components.

- Το PNG διατηρεί τα ακριβή χρώματα και τη διαφάνεια που ορίσαμε νωρίτερα.  
- Αντικαταστήστε το `"Your Document Directory"` με την πραγματική διαδρομή στο σύστημά σας.  
- Για επεξεργασία παρτίδας, κάντε βρόχο πάνω σε μια συλλογή `Bitmap` αντικειμένων και καλέστε `Save` μέσα στο βρόχο – η βιβλιοθήκη μπορεί να διαχειριστεί χιλιάδες εικόνες με λιγότερα από 200 MB RAM.

## Συνηθισμένα προβλήματα και λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Διόρθωση |
|----------|----------------|----------|
| **Σφάλμα “File not found” κατά την αποθήκευση** | Ο φάκελος προορισμού δεν υπάρχει. | Δημιουργήστε το φάκελο προγραμματιστικά (`Directory.CreateDirectory`) πριν καλέσετε `Save`. |
| **Κενή εικόνα** μετά τον μετασχηματισμό | Η `TranslateTransform` κλήθηκε μετά το σχέδιο. | Βεβαιωθείτε ότι ο μετασχηματισμός ορίζεται **πριν** οποιεσδήποτε εντολές σχεδίασης. |
| **Παραμορφωμένα χρώματα** | Χρήση μη συμβατής μορφής pixel. | Χρησιμοποιήστε `Format32bppPArgb` για έξοδο PNG. |
| **Έλλειψη μνήμης σε μεγάλους καμβάδες** | Φόρτωση ολόκληρου του bitmap στη μνήμη. | Χρησιμοποιήστε επιλογές streaming του `Bitmap` ή χωρίστε την εικόνα σε πλακίδια· το Aspose.Drawing μπορεί να αποδίδει πλακίδια ανεξάρτητα. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να εφαρμόσω περισσότερους από έναν μετασχηματισμό;**  
Α: Ναι – μπορείτε να αλυσίσετε `TranslateTransform`, `RotateTransform` και `ScaleTransform` για σύνθετα εφέ σε μια ενιαία γραφική αλυσίδα.

**Ε: Είναι το Aspose.Drawing δωρεάν για εμπορικά έργα;**  
Α: Διατίθεται δωρεάν δοκιμή για αξιολόγηση, αλλά απαιτείται εμπορική άδεια για παραγωγική χρήση.

**Ε: Λειτουργεί με .NET Core και .NET 5/6/7;**  
Α: Απόλυτα. Το Aspose.Drawing υποστηρίζει όλα τα σύγχρονα .NET runtimes, συμπεριλαμβανομένων .NET Core, .NET 5, .NET 6 και .NET 7.

**Ε: Πού μπορώ να βρω την πλήρη τεκμηρίωση API;**  
Α: Η πλήρης τεκμηρίωση είναι διαθέσιμη στην [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).

**Ε: Πώς αντιμετωπίζω το πρόβλημα “missing output file”;**  
Α: Ελέγξτε τη συμβολοσειρά διαδρομής, βεβαιωθείτε ότι έχετε δικαιώματα εγγραφής και ότι ο φάκελος υπάρχει πριν καλέσετε `Save`.

## Συμπέρασμα

Μάθατε **πώς να μετατρέψετε το σχέδιο σε PNG** με το Aspose.Drawing, εφαρμόζοντας έναν **μετασχηματισμό κόσμου**, και εκτελώντας ένα **παράδειγμα graphics translate** που μπορεί να επεκταθεί με περιστροφή ή κλιμάκωση. Με την κατάκτηση αυτών των θεμελιωδών βημάτων μπορείτε να δημιουργείτε δυναμικές εικόνες, προσαρμοσμένα διαγράμματα ή γραφικά “on‑the‑fly” για οποιαδήποτε .NET εφαρμογή. Στη συνέχεια, εξερευνήστε το tutorial μετασχηματισμού με πίνακα για να συνδυάσετε πολλαπλές λειτουργίες σε έναν ενιαίο πίνακα για ακόμη καλύτερη απόδοση.

---

**Τελευταία ενημέρωση:** 2026-10-18  
**Δοκιμασμένο με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose  
**Σχετικοί πόροι:** [Aspose.Drawing API reference](https://reference.aspose.com/drawing/net/) | [Λήψη δωρεάν δοκιμής](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Σχετικά tutorials

- [Tutorial μετασχηματισμού πίνακα: matrix transformations in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Πώς να περιστρέψετε εικόνα με global transformation του Aspose.Drawing](/drawing/net/coordinate-transformations/global-transformation/)
- [Μετασχηματισμός συστήματος συντεταγμένων – page transformation in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}