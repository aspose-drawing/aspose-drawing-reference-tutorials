---
date: 2026-05-19
description: Μάθετε πώς να σχεδιάζετε γραφικά ορθογωνίου ενώ εκτελείτε coordinate
  system transformation στο .NET με Aspose.Drawing. Αυτός ο οδηγός βήμα‑βήμα δείχνει
  πώς να μετατρέψετε ίντσες σε pixel και να ορίσετε τις μονάδες σελίδας.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Coordinate System Transformation στο Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Πώς να Σχεδιάσετε Ορθογώνιο – Coordinate System Transformation (Page Transformation)
  στο Aspose.Drawing για .NET
url: /el/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Σχεδιάσετε Ορθογώνιο – Μετασχηματισμός Συντεταγμένων (Μετασχηματισμός Σελίδας) στο Aspose.Drawing για .NET

## Εισαγωγή

Καλώς ήρθατε! Σε αυτό το σεμινάριο θα ανακαλύψετε **πώς να σχεδιάσετε ορθογώνιο** γραφικά ενώ μετασχηματίζετε τις συντεταγμένες της σελίδας χρησιμοποιώντας το Aspose.Drawing για .NET. Είτε δημιουργείτε μια εφαρμογή με έντονη χρήση γραφικών είτε χρειάζεστε ακριβή έλεγχο των μονάδων σχεδίασης, αυτός ο οδηγός σας καθοδηγεί βήμα‑βήμα—from την προετοιμασία του καμβά μέχρι το σχεδιασμό ενός ορθογώνιου στοιχείου. Στο τέλος, θα μπορείτε να εφαρμόσετε αυτές τις τεχνικές στα δικά σας έργα με σιγουριά.

## Γρήγορες Απαντήσεις
- **Τι είναι ο μετασχηματισμός συστήματος συντεταγμένων;** Αντιστοίχιση μονάδων επιπέδου σελίδας (όπως ίντσες) σε εικονοστοιχεία επιπέδου συσκευής.  
- **Γιατί να χρησιμοποιήσω το Aspose.Drawing;** Προσφέρει μια πλήρως διαχειριζόμενη,跨平台 εναλλακτική λύση στο System.Drawing.Common.  
- **Πόσο χρόνο παίρνει η υλοποίηση του παραδείγματος;** Περίπου 5‑10 λεπτά για έναν βασικό μετασχηματισμό σελίδας.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Τι είναι το Aspose.Drawing;

`Aspose.Drawing` είναι μια βιβλιοθήκη γραφικών .NET που παρέχει ένα **API ανεξάρτητο από τη συσκευή** για δημιουργία και επεξεργασία raster εικόνων, διανυσμάτων και σχεδίων επιπέδου σελίδας χωρίς εξάρτηση από το GDI+. Υποστηρίζει **πάνω από 30 μορφές εικόνας** και μπορεί να επεξεργαστεί εικόνες έως **10.000 × 10.000 pixel** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη.

## Γιατί να χρησιμοποιήσω μετασχηματισμό συστήματος συντεταγμένων με το Aspose.Drawing;

Ο μετασχηματισμός συστήματος συντεταγμένων σας επιτρέπει να σχεδιάζετε γραφικά σε πραγματικές μονάδες μέτρησης ενώ η βιβλιοθήκη διαχειρίζεται την κλιμάκωση σε εικονοστοιχεία για οποιαδήποτε συσκευή εξόδου. Αυτό εξασφαλίζει συνεπή μεγέθη σε οθόνες και εκτυπωτές και απλοποιεί τους υπολογισμούς διάταξης.

- **Σχεδίαση ανεξάρτητη από τη συσκευή:** Γράψτε τον κώδικα μία φορά και αφήστε το Aspose.Drawing να χειριστεί την κλιμάκωση εικονοστοιχείων για οποιαδήποτε οθόνη ή εκτυπωτή.  
- **Ακριβής σχεδίαση:** Ιδανικό για τεχνικά διαγράμματα, σκίτσα τύπου CAD ή οποιοδήποτε σενάριο όπου η ακριβής μέτρηση είναι κρίσιμη.  
- **Αξιοπιστία跨平台:** Λειτουργεί σταθερά σε Windows, Linux και macOS χωρίς τους περιορισμούς του GDI+ του System.Drawing.  
- **Αριθμοί απόδοσης:** Σε τυπικό CPU 2.5 GHz, το σχεδιασμό ενός 5‑inch ορθογωνίου στα 300 DPI διαρκεί κάτω από **15 ms**, και η βιβλιοθήκη μπορεί να αποδώσει **50 frames per second** σε σενάρια πραγματικού‑χρόνου προεπισκόπησης.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε:

- **Βιβλιοθήκη Aspose.Drawing:** Κατεβάστε την πιο πρόσφατη έκδοση από την επίσημη ιστοσελίδα [εδώ](https://releases.aspose.com/drawing/net/).  
- **Περιβάλλον Ανάπτυξης:** Visual Studio, Rider ή οποιοδήποτε IDE συμβατό με .NET.  
- **Κατάλογος Εγγράφου:** Αντικαταστήστε το `"Your Document Directory"` στον κώδικα με το φάκελο όπου θέλετε να αποθηκευτεί η εικόνα εξόδου.  
- **Υποστήριξη ASP.NET (προαιρετικό):** Μπορείτε να χρησιμοποιήσετε το Aspose.Drawing σε έργα ASP.NET Core προσθέτοντας το πακέτο NuGet στην εφαρμογή web· ακολουθεί το ίδιο **πρότυπο how to use aspnet** όπως κάθε άλλη βιβλιοθήκη .NET.

Τώρα που όλα είναι έτοιμα, ας βουτήξουμε στον οδηγό βήμα‑βήμα.

## Πώς να Σχεδιάσετε Ορθογώνιο με Μετασχηματισμό Σελίδας;

Φορτώστε ένα κενό bitmap, ορίστε τη μονάδα σελίδας σε ίντσες και σχεδιάστε ένα ορθογώνιο με λεπτό μπλε στυλό—αυτό ολοκληρώνει το σχεδιασμό του ορθογωνίου σε λίγες μόνο γραμμές κώδικα. Η ιδιότητα `Graphics.PageUnit` λέει στη μηχανή να ερμηνεύει όλες τις συντεταγμένες ως ίντσες, ώστε να σκέφτεστε σε πραγματικές μετρήσεις αντί για ακατέργαστα εικονοστοιχεία.

### Βήμα 1: Εισαγωγή Χώρων Ονομάτων

Οι δηλώσεις `using` σας δίνουν πρόσβαση στις βασικές κλάσεις σχεδίασης.

```csharp
using System.Drawing;
```

### Βήμα 2: Δημιουργία Bitmap

`Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη στην οποία μπορείτε να σχεδιάσετε. Ξεκινάμε δημιουργώντας ένα κενό bitmap που θα λειτουργήσει ως επιφάνεια σχεδίασης. Η μορφή εικονοστοιχείων `Format32bppPArgb` παρέχει υψηλής ποιότητας, προπολλαπλασιασμένη υποστήριξη άλφα.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Βήμα 3: Δημιουργία Αντικειμένου Graphics

Ένα αντικείμενο `Graphics` παρέχει το API σχεδίασης για το bitmap. Είναι η γέφυρα μεταξύ του κώδικά σας και του buffer εικονοστοιχείων.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Βήμα 4: Καθαρισμός Καμβά

Δώστε στον καμβά ένα ουδέτερο φόντο ώστε τα σχεδιασμένα σχήματα να ξεχωρίζουν. Εδώ το γεμίζουμε με ανοιχτό γκρι.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Βήμα 5: Ορισμός Μετασχηματισμού (Πώς να ορίσετε μονάδα)

`Graphics.PageUnit` καθορίζει τη μονάδα μέτρησης που χρησιμοποιείται για τις συντεταγμένες της σελίδας. Για να αντιστοιχίσετε τις συντεταγμένες της σελίδας σε εικονοστοιχεία συσκευής, ορίστε την ιδιότητα `PageUnit`. Στο παράδειγμά μας επιλέγουμε ίντσες, αλλά μπορείτε επίσης να χρησιμοποιήσετε `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` ή `GraphicsUnit.Pixel`. Ο ορισμός της μονάδας σε ίντσες σας επιτρέπει να **μετατρέπετε αυτόματα τις ίντσες σε εικονοστοιχεία** βάσει του DPI του bitmap (96 DPI εξ ορισμού, 300 DPI για υψηλής ανάλυσης εκτύπωση).

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Βήμα 6: Σχεδίαση Ορθογωνίου – draw rectangle graphics

`Pen` ορίζει το χρώμα, το πλάτος και το στυλ των γραμμών που σχεδιάζονται στην επιφάνεια γραφικών. Τώρα σχεδιάζουμε ένα ορθογώνιο με λεπτό μπλε στυλό. Επειδή μεταβήκαμε σε ίντσες, το μέγεθος και η θέση του ορθογωνίου εκφράζονται σε ίντσες, καθιστώντας τον κώδικα πιο αναγνώσιμο για διατάξεις προσανατολισμένες στην εκτύπωση.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Βήμα 7: Αποθήκευση Εικόνας

Τέλος, γράψτε το bitmap σε αρχείο PNG στον φάκελο που καθορίσατε νωρίτερα.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Πώς να Κλιμακώσετε Γραφικά για Εκτυπωτή;

Ορίστε το DPI του bitmap στην επιθυμητή ανάλυση εκτυπωτή (π.χ., 300 DPI) πριν το σχεδιάσετε. Αυτό κλιμακώνει αυτόματα την **έξοδο γραφικών εκτυπωτή** ώστε μία ίντσα στον κώδικά σας να ισούται με μία ίντσα στην εκτυπωμένη σελίδα. Μετά την κλήση `bitmap.SetResolution(300, 300)`, το ίδιο ορθογώνιο θα εμφανίζεται μεγαλύτερο στο εκτυπωμένο φύλλο διατηρώντας τις ακριβείς διαστάσεις του.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Διόρθωση |
|----------|----------------|----------|
| **Το αρχείο εξόδου δεν δημιουργείται** | Λάθος διαδρομή ή λείπει ο φάκελος | Βεβαιωθείτε ότι ο προορισμός υπάρχει ή χρησιμοποιήστε `Directory.CreateDirectory` πριν την αποθήκευση. |
| **Το ορθογώνιο εμφανίζεται παραμορφωμένο** | Λάθος `PageUnit` ή μη αντιστοιχισμένο DPI | Επαληθεύστε ότι το `graphics.PageUnit` ταιριάζει με τις μονάδες που θέλετε να χρησιμοποιήσετε και ότι το DPI του bitmap έχει οριστεί σωστά (προεπιλογή 96 DPI). |
| **Απόρριψη άδειας** | Εκτέλεση χωρίς έγκυρη άδεια σε παραγωγή | Εφαρμόστε την προσωρινή ή μόνιμη άδεια Aspose.Drawing πριν δημιουργήσετε αντικείμενα γραφικών. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το Aspose.Drawing δωρεάν;**  
Α: Ναι, διαθέσιμη είναι μια δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

**Ε: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.Drawing;**  
Α: Η πλήρης αναφορά API βρίσκεται [εδώ](https://reference.aspose.com/drawing/net/).

**Ε: Πώς λαμβάνω υποστήριξη για το Aspose.Drawing;**  
Α: Επισκεφθείτε το [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) για βοήθεια από την κοινότητα και επίσημη υποστήριξη.

**Ε: Υπάρχει προσωρινή άδεια για το Aspose.Drawing;**  
Α: Απολύτως—αποκτήστε την [εδώ](https://purchase.aspose.com/temporary-license/).

**Ε: Πού μπορώ να αγοράσω πλήρη άδεια Aspose.Drawing;**  
Α: Μπορείτε να την αγοράσετε [εδώ](https://purchase.aspose.com/buy).

## Συμπέρασμα

Σε αυτόν τον οδηγό καλύψαμε όλα όσα χρειάζεστε για **πώς να σχεδιάσετε ορθογώνιο** γραφικά με το Aspose.Drawing: ρύθμιση καμβά, διαμόρφωση μονάδων σελίδας, σχεδίαση ακριβών σχημάτων και αποθήκευση του αποτελέσματος. Χρησιμοποιήστε αυτές τις τεχνικές για να δημιουργήσετε κλιμακώσιμα, ανεξάρτητα από τη συσκευή γραφικά για αναφορές, σχέδια τύπου CAD ή οποιαδήποτε εφαρμογή όπου η ακρίβεια των μετρήσεων είναι σημαντική. Στη συνέχεια, εξερευνήστε προχωρημένους μετασχηματισμούς όπως περιστροφή, κλιμάκωση και προσαρμοσμένες αρχικές συντεταγμένες για ακόμη πιο ισχυρά σενάρια σχεδίασης.

---

**Τελευταία Ενημέρωση:** 2026-05-19  
**Δοκιμάστηκε Με:** Aspose.Drawing 24.12 για .NET  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Σεμινάρια

- [Μονάδες Μέτρησης στο Aspose.Drawing για .NET](/drawing/net/coordinate-transformations/units-of-measure/)
- [Πώς να Εφαρμόσετε Μετασχηματισμό: Τοπικός Μετασχηματισμός στο Aspose.Drawing για .NET](/drawing/net/coordinate-transformations/local-transformation/)
- [Σεμινάριο Μετασχηματισμού Πίνακα: Μετασχηματισμοί Πίνακα στο Aspose.Drawing για .NET](/drawing/net/coordinate-transformations/matrix-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}