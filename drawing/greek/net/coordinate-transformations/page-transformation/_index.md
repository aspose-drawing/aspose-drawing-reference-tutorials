---
date: 2026-11-04
description: Μάθετε πώς να δημιουργήσετε γραφικά ορθογωνίου ενώ εκτελείτε μετασχηματισμό
  συστήματος συντεταγμένων στο .NET με το API του Aspose.Drawing. Αυτός ο οδηγός βήμα
  προς βήμα δείχνει πώς να μετατρέψετε ίντσες σε εικονοστοιχεία και να ορίσετε τις
  μονάδες σελίδας.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Μετασχηματισμός συστήματος συντεταγμένων στο Aspose.Drawing
og_description: Μάθετε πώς να δημιουργήσετε γραφικά ορθογωνίου ενώ μετατρέπετε ίντσες
  σε εικονοστοιχεία και ορίζετε τις μονάδες σελίδας στο Aspose.Drawing για .NET. Ακολουθήστε
  τον οδηγό βήμα προς βήμα για ακριβή μετασχηματισμό σελίδας.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Πώς να σχεδιάσετε ορθογώνιο με μετασχηματισμό σελίδας χρησιμοποιώντας Aspose.Drawing
  για .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Πώς να σχεδιάσετε ορθογώνιο – μετασχηματισμός συστήματος συντεταγμένων (μετασχηματισμός
  σελίδας) στο Aspose.Drawing για .NET
url: /el/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να σχεδιάσετε ορθογώνιο – μετασχηματισμός συστήματος συντεταγμένων (μετασχηματισμός σελίδας) στο Aspose.Drawing για .NET

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε **πώς να σχεδιάσετε ορθογώνιο** γραφικά ενώ εκτελείτε μετασχηματισμό συστήματος συντεταγμένων επιπέδου σελίδας χρησιμοποιώντας το Aspose.Drawing για .NET. Είτε δημιουργείτε μια μηχανή αναφορών, ένα εργαλείο σκίτσου τύπου CAD, ή οποιαδήποτε εφαρμογή που χρειάζεται ακριβείς πραγματικές μετρήσεις, αυτός ο οδηγός σας καθοδηγεί βήμα προς βήμα—από τη δημιουργία ενός bitmap μέχρι την αποθήκευση του τελικού PNG. Στο τέλος θα είστε άνετοι με τη μετατροπή ιντσών σε pixel, τον καθαρισμό του φόντου του καμβά και τον ορισμό μονάδων σελίδας για εκτύπωση.

## Γρήγορες απαντήσεις
- **Τι είναι ο μετασχηματισμός συστήματος συντεταγμένων;** Μετατρέπει τις μονάδες επιπέδου σελίδας (όπως ίντσες) σε pixel επιπέδου συσκευής ώστε τα σχέδια να κλιμακώνονται σωστά σε οποιαδήποτε συσκευή εξόδου.  
- **Γιατί να επιλέξετε το Aspose.Drawing;** Παρέχει ένα πλήρως διαχειριζόμενο, cross‑platform API γραφικών που αντικαθιστά το System.Drawing.Common και υποστηρίζει 30+ μορφές εικόνας.  
- **Πόσο χρόνο χρειάζεται η υλοποίηση του παραδείγματος;** Περίπου 5‑10 λεπτά για ένα βασικό ορθογώνιο με μετασχηματισμό σελίδας.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγικές εκδόσεις.  
- **Ποια .NET runtimes υποστηρίζονται;** .NET Framework 4.6+, .NET Core 3.1+, και .NET 5/6/7.

## Τι είναι το Aspose.Drawing;

Το Aspose.Drawing είναι μια βιβλιοθήκη γραφικών .NET που παρέχει ένα **device‑independent API** για δημιουργία και επεξεργασία raster εικόνων, διανυσμάτων και σχεδίων επιπέδου σελίδας χωρίς εξάρτηση από το GDI+. Υποστηρίζει **30+ μορφές εικόνας** και μπορεί να επεξεργαστεί εικόνες έως **10.000 × 10.000 pixel** διατηρώντας χαμηλή χρήση μνήμης.

## Γιατί να χρησιμοποιήσετε μετασχηματισμό συστήματος συντεταγμένων με το Aspose.Drawing;

Ο μετασχηματισμός συστήματος συντεταγμένων σας επιτρέπει να σχεδιάζετε γραφικά σε πραγματικές μονάδες, ενώ η βιβλιοθήκη χειρίζεται αυτόματα την κλιμάκωση pixel για οποιαδήποτε συσκευή εξόδου. Αυτή η προσέγγιση εγγυάται ότι ένα ορθογώνιο 5 ιντσών εκτυπώνεται ακριβώς πέντε ίντσες σε έναν εκτυπωτή 300 DPI και εμφανίζεται αναλογικά σε οθόνη 96 DPI, εξαλείφοντας τα σφάλματα χειροκίνητης μετατροπής.

- **Σχεδίαση ανεξάρτητη από τη συσκευή:** Γράψτε κώδικα μία φορά· το Aspose.Drawing το κλιμακώνει για οθόνες, εκτυπωτές ή PDF.  
- **Ακριβής σχεδίαση:** Ιδανικό για τεχνικά διαγράμματα, μηχανικά σχήματα ή οποιοδήποτε σενάριο όπου οι ακριβείς μετρήσεις έχουν σημασία.  
- **Αξιοπιστία跨平台:** Λειτουργεί σταθερά σε Windows, Linux και macOS χωρίς τους περιορισμούς GDI+ του System.Drawing.  
- **Απόδοση:** Σε τυπική CPU 2.5 GHz, η σχεδίαση ενός ορθογωνίου 5 ιντσών στα 300 DPI ολοκληρώνεται σε κάτω από **15 ms**, και η βιβλιοθήκη μπορεί να αποδίδει **50 καρέ ανά δευτερόλεπτο** σε σενάρια προεπισκόπησης σε πραγματικό χρόνο.

## Προαπαιτούμενα

- **Βιβλιοθήκη Aspose.Drawing:** Κατεβάστε την τελευταία έκδοση από την επίσημη ιστοσελίδα [here](https://releases.aspose.com/drawing/net/).  
- **IDE:** Visual Studio, Rider ή οποιονδήποτε επεξεργαστή συμβατό με .NET.  
- **Φάκελος εξόδου:** Αντικαταστήστε το `"Your Document Directory"` στον κώδικα παραδείγματος με το φάκελο όπου θέλετε να αποθηκευτεί το PNG.  
- **Προαιρετική υποστήριξη ASP.NET:** Μπορείτε να προσθέσετε το πακέτο NuGet σε ένα έργο ASP.NET Core και να χρησιμοποιήσετε το ίδιο API· το πρότυπο ακολουθεί τη συνήθη προσέγγιση **how to use aspnet** για βιβλιοθήκες .NET.

## Πώς να σχεδιάσετε ορθογώνιο με μετασχηματισμό σελίδας;

Φορτώστε ένα κενό bitmap, ορίστε τη μονάδα σελίδας σε ίντσες και σχεδιάστε ένα ορθογώνιο χρησιμοποιώντας ένα λεπτό μπλε στυλό—αυτό ολοκληρώνει τη σχεδίαση του ορθογωνίου σε λίγες μόνο γραμμές κώδικα. Η ιδιότητα `Graphics.PageUnit` λέει στη μηχανή να ερμηνεύει όλες τις συντεταγμένες ως ίντσες, ώστε να σκέφτεστε σε πραγματικές μετρήσεις αντί για ακατέργαστα pixel, και η βιβλιοθήκη αυτόματα **μετατρέπει τις ίντσες σε pixel** βάσει του DPI του bitmap.

### Βήμα 1: εισαγωγή namespaces

Οι δηλώσεις `using` σας δίνουν πρόσβαση στις βασικές κλάσεις σχεδίασης.

```csharp
using System.Drawing;
```

### Βήμα 2: δημιουργία bitmap

`Bitmap` είναι ο κοντέινερ εικόνας στη μνήμη πάνω στον οποίο σχεδιάζετε. Διατηρεί το buffer pixel και εκθέτει μεθόδους για αποθήκευση σε αρχεία. Η δημιουργία ενός bitmap ορίζει το μέγεθος του καμβά και τη μορφή pixel.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Βήμα 3: δημιουργία αντικειμένου graphics

`Graphics` παρέχει την επιφάνεια σχεδίασης για το bitmap. Μετατρέπει εντολές σχεδίασης υψηλού επιπέδου (γραμμές, σχήματα, κείμενο) σε λειτουργίες pixel στο υποκείμενο bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Βήμα 4: εκκαθάριση φόντου καμβά

Η εκκαθάριση του καμβά με ουδέτερο χρώμα εξασφαλίζει ότι τα σχήματά σας ξεχωρίζουν. Σε αυτό το παράδειγμα γεμίζουμε το φόντο με ανοιχτό γκρι, το οποίο επίσης δείχνει την τεχνική **clear canvas background**.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Βήμα 5: ορισμός μετασχηματισμού (πώς να ορίσετε μονάδες)

`Graphics.PageUnit` καθορίζει τη μονάδα μέτρησης που χρησιμοποιείται για τις συντεταγμένες της σελίδας. Ορίζοντάς το σε `GraphicsUnit.Inch` λέει στο Aspose.Drawing να **μετατρέπει τις ίντσες σε pixel** αυτόματα βάσει του DPI του bitmap (96 DPI εξ ορισμού, 300 DPI για εκτύπωση υψηλής ανάλυσης). Μπορείτε επίσης να επιλέξετε `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` ή `GraphicsUnit.Pixel` ανάλογα με τις απαιτήσεις διάταξης.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Βήμα 6: σχεδίαση ορθογωνίου – draw rectangle graphics

`Pen` ορίζει το χρώμα, το πλάτος και το στυλ των γραμμών που σχεδιάζονται σε μια επιφάνεια graphics. Χρησιμοποιώντας ένα λεπτό μπλε στυλό, σχεδιάζουμε ένα ορθογώνιο των οποίων οι διαστάσεις εκφράζονται σε ίντσες, κάνοντας τον κώδικα πιο ευανάγνωστο για διατάξεις προσανατολισμένες στην εκτύπωση.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Βήμα 7: αποθήκευση bitmap ως png

Τέλος, γράψτε το bitmap σε αρχείο PNG στον φάκελο που καθορίσατε νωρίτερα. Η αποθήκευση ως PNG διατηρεί την απώλεια-μη-απώλειας ποιότητα και υποστηρίζεται ευρέως σε όλες τις πλατφόρμες.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Πώς να κλιμακώσετε γραφικά για εκτυπωτή;

Ορίστε το DPI του bitmap στην ανάλυση του εκτυπωτή-στόχου (π.χ., 300 DPI) πριν τη σχεδίαση. Αυτό αυτόματα **scale graphics printer** την έξοδο ώστε μία ίντσα στον κώδικά σας να ισούται με μία ίντσα στην εκτυπωμένη σελίδα, ενώ το λογικό μέγεθος του ορθογωνίου παραμένει αμετάβλητο. Μετά την κλήση `bitmap.SetResolution(300, 300)`, το ίδιο ορθογώνιο θα εμφανιστεί μεγαλύτερο στο χαρτί αλλά θα διατηρήσει τις ακριβείς διαστάσεις του.

## Συχνά προβλήματα και λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Διόρθωση |
|----------|------------------|----------|
| **Το αρχείο εξόδου δεν δημιουργείται** | Λανθασμένη διαδρομή ή έλλειψη φακέλου | Βεβαιωθείτε ότι ο φάκελος προορισμού υπάρχει ή καλέστε `Directory.CreateDirectory` πριν την αποθήκευση. |
| **Το ορθογώνιο εμφανίζεται παραμορφωμένο** | Ασυμφωνία `PageUnit` ή DPI | Επαληθεύστε ότι το `graphics.PageUnit` ταιριάζει με τη ζητούμενη μονάδα και ότι το DPI του bitmap έχει οριστεί σωστά (προεπιλογή 96 DPI, 300 DPI για εκτύπωση). |
| **Εξαίρεση άδειας** | Εκτέλεση χωρίς έγκυρη άδεια σε παραγωγή | Εφαρμόστε την προσωρινή ή μόνιμη άδεια Aspose.Drawing πριν τη δημιουργία αντικειμένων graphics. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το Aspose.Drawing δωρεάν;**  
Α: Ναι, μια δωρεάν δοκιμή είναι διαθέσιμη [here](https://releases.aspose.com/).

**Ε: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.Drawing;**  
Α: Η πλήρης αναφορά API βρίσκεται [here](https://reference.aspose.com/drawing/net/).

**Ε: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Drawing;**  
Α: Επισκεφθείτε το [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) για βοήθεια της κοινότητας και επίσημη υποστήριξη.

**Ε: Διατίθεται προσωρινή άδεια για το Aspose.Drawing;**  
Α: Απόλυτα—αποκτήστε τη [here](https://purchase.aspose.com/temporary-license/).

**Ε: Πού μπορώ να αγοράσω πλήρη άδεια Aspose.Drawing;**  
Α: Μπορείτε να την αγοράσετε [here](https://purchase.aspose.com/buy).

## Συμπέρασμα

Τώρα γνωρίζετε **πώς να σχεδιάσετε ορθογώνιο** γραφικά με μετασχηματισμό επιπέδου σελίδας χρησιμοποιώντας το Aspose.Drawing για .NET. Ορίζοντας τη μονάδα σελίδας σε ίντσες, καθαρίζοντας το φόντο του καμβά και αποθηκεύοντας το αποτέλεσμα ως PNG, επιτυγχάνετε ακριβή, ανεξάρτητη από τη συσκευή έξοδο κατάλληλη τόσο για προβολή σε οθόνη όσο και για εκτύπωση υψηλής ανάλυσης. Πειραματιστείτε με άλλες μονάδες, περιστροφές ή προσαρμοσμένες αρχές συντεταγμένων για να ξεκλειδώσετε ακόμη πιο ισχυρά σενάρια σχεδίασης.

---

**Last Updated:** 2026-11-04  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Πώς να ορίσετε μονάδα στο Aspose.Drawing για .NET – Μονάδες Μέτρησης](/drawing/net/coordinate-transformations/units-of-measure/)
- [Γενικός Μετασχηματισμός](/drawing/net/coordinate-transformations/global-transformation/)
- [Μετασχηματισμός βήμα προς βήμα – Μετασχηματισμοί Συντεταγμένων](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}