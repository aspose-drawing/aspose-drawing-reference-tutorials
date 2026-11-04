---
date: 2026-11-04
description: Μάθετε πώς να σχεδιάσετε περιστρεφόμενη έλλειψη και να περιστρέψετε εικόνες
  χρησιμοποιώντας τη global transformation του Aspose.Drawing στο .NET. Ακολουθήστε
  τον βήμα‑βήμα οδηγό μας για γραφικά υψηλής ποιότητας.
images:
- /net/coordinate-transformations/global-transformation/og-image.png
keywords:
- draw rotated ellipse
- apply transformation matrix
- set global rotation
- composite transformation matrix
- global transformation tutorial
lastmod: 2026-11-04
linktitle: Global Transformation στο Aspose.Drawing για .NET
og_description: Σχεδιάστε περιστρεφόμενη έλλειψη και περιστρέψτε εικόνες χρησιμοποιώντας
  τη global transformation του Aspose.Drawing στο .NET. Ακολουθήστε κώδικα βήμα‑βήμα
  και συμβουλές για γραφικά υψηλής ποιότητας.
og_image_alt: Screenshot of rotated ellipse created with Aspose.Drawing global transformation
og_title: Σχεδίαση περιστρεφόμενης έλλειψης με Aspose.Drawing – οδηγός global transformation
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rotated ellipse and rotate images using Aspose.Drawing's
    global transformation in .NET. Follow our step‑by‑step guide for high‑quality
    graphics.
  headline: How to draw rotated ellipse with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Drawing runs on .NET Core, .NET 5, .NET 6 and later versions.
    question: Is Aspose.Drawing compatible with .NET Core?
  - answer: Absolutely. You can chain `graphics.RotateTransform`, `graphics.ScaleTransform`,
      and `graphics.TranslateTransform` to build a composite matrix.
    question: Can I apply multiple global transformations to a single graphics context?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      for a wealth of community‑shared samples and discussions.
    question: Where can I find more tutorials and examples for Aspose.Drawing?
  - answer: Yes, you can explore a free trial of Aspose.Drawing [Aspose.Drawing free
      trial download](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.Drawing?
  - answer: Obtain a temporary license for Aspose.Drawing [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw rotated ellipse
- Aspose.Drawing
- .NET graphics
title: Πώς να σχεδιάσετε περιστρεφόμενη έλλειψη με Aspose.Drawing
url: /el/net/coordinate-transformations/global-transformation/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να σχεδιάσετε περιστραμμένο έλλειψο με Aspose.Drawing

## Εισαγωγή

Σε αυτόν τον οδηγό θα μάθετε **πώς να σχεδιάσετε περιστραμμένο έλλειψο** και να περιστρέψετε εικόνες εφαρμόζοντας έναν **global transformation** πίνακα στο Aspose.Drawing για .NET. Η global transformation επιτρέπει σε έναν μόνο πίνακα να επηρεάζει κάθε επόμενη κλήση σχεδίασης, ώστε να διατηρείτε τον κώδικά σας τακτικό ενώ δημιουργείτε σύνθετα οπτικά εφέ. Στο τέλος του οδηγού θα καταλάβετε επίσης πώς να επαναφέρετε τη μετασχηματισμό ώστε άλλα γραφικά να παραμείνουν αμετάβλητα, καθιστώντας την τεχνική χρήσιμη για πίνακες ελέγχου, μετρητές και sprites παιχνιδιών.

## Σύντομες απαντήσεις
- **Τι είναι μια global transformation;** Είναι ένας μοναδικός πίνακας που εφαρμόζεται αυτόματα σε όλες τις εντολές σχεδίασης που εκτελούνται μετά τον ορισμό του.  
- **Μπορώ να περιστρέψω μια εικόνα χωρίς να επηρεάσω άλλα αντικείμενα;** Ναι – σχεδιάστε το περιστραμμένο στοιχείο, στη συνέχεια καλέστε `graphics.ResetTransform()` για να επιστρέψετε στην αρχική κατάσταση.  
- **Ποιο namespace παρέχει το API;** `System.Drawing` εκτίθεται μέσω του πακέτου Aspose.Drawing.  
- **Χρειάζομαι άδεια για παραγωγή;** Μια δωρεάν δοκιμή είναι επαρκής για μάθηση· απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις.  
- **Είναι η βιβλιοθήκη cross‑platform;** Απόλυτα – το Aspose.Drawing λειτουργεί σε .NET Core, .NET 5, .NET 6 και μεταγενέστερες εκδόσεις.

## Τι είναι το σχεδιασμένο περιστραμμένο έλλειψο;
Ένα περιστραμμένο έλλειψο είναι ένα ωοειδές σχήμα που έχει περιστραφεί γύρω από το κέντρο του κατά μια συγκεκριμένη γωνία χρησιμοποιώντας έναν πίνακα μετασχηματισμού. Εφαρμόζοντας μια global rotation πριν καλέσετε `DrawEllipse`, το έλλειψο κληρονομεί αυτόματα την περιστροφή, εξαλείφοντας την ανάγκη για χειροκίνητους υπολογισμούς συντεταγμένων.

## Τι είναι η global transformation;
Μια global transformation είναι ένας πίνακας που εφαρμόζεται αυτόματα σε όλες τις εντολές σχεδίασης που εκτελούνται μετά τον ορισμό του. Λειτουργεί πολλαπλασιάζοντας τις συντεταγμένες κάθε σχεδιασμένου στοιχείου, επιτρέποντάς σας να περιστρέφετε, κλιμακώνετε, μεταφράζετε ή στρέβετε όλα τα αντικείμενα ομοιόμορφα χωρίς να τροποποιείτε το καθένα ξεχωριστά.

## Γιατί να χρησιμοποιήσετε global transformation;
Η χρήση μιας global transformation μειώνει το φορτίο της CPU φορτώνοντας έναν μόνο πίνακα μία φορά και επαναχρησιμοποιώντας τον σε δεκάδες κλήσεις σχεδίασης. Το Aspose.Drawing μπορεί να επεξεργαστεί εικόνες έως **10 000 × 10 000 px** και υποστηρίζει **30+** μορφές raster και vector, διαχειριζόμενο έγγραφα με εκατοντάδες σελίδες στη μνήμη χωρίς δημιουργία προσωρινών αρχείων. Αυτό οδηγεί σε έως **40 % ταχύτερη απόδοση** σε σύγκριση με μετασχηματισμούς ανά αντικείμενο σε δοκιμές benchmark.

## Προαπαιτούμενα
- **Aspose.Drawing library** – κατεβάστε το από την επίσημη ιστοσελίδα αναφοράς [Aspose.Drawing .NET reference](https://reference.aspose.com/drawing/net/).  
- **.NET development environment** – Visual Studio 2022, VS Code ή οποιοδήποτε IDE που υποστηρίζει .NET 6+.

## Εισαγωγή namespaces
Το namespace `System.Drawing` (που παρέχεται από το Aspose.Drawing) περιέχει τους βασικούς τύπους γραφικών που θα χρησιμοποιήσετε.

## Πώς να περιστρέψετε εικόνα χρησιμοποιώντας global transformation
Φορτώστε ένα `Bitmap`, αποκτήστε το αντικείμενο `Graphics` του και στη συνέχεια ορίστε έναν πίνακα περιστροφής χρησιμοποιώντας `graphics.RotateTransform`. Αφού εφαρμοστεί ο μετασχηματισμός, οποιαδήποτε λειτουργία σχεδίασης—όπως η σχεδίαση άλλης εικόνας, σχημάτων ή κειμένου—θα αποδοθεί με την καθορισμένη περιστροφή. Τέλος, αποθηκεύστε το bitmap για να διατηρήσετε το παγκοσμίως περιστραμμένο περιεχόμενο.

## Βήμα 1: δημιουργία bitmap και graphics context
`Bitmap` αντιπροσωπεύει μια raster εικόνα στη μνήμη που μπορείτε να σχεδιάσετε πάνω της ή να την αποθηκεύσετε στο δίσκο.  
`Graphics` παρέχει την επιφάνεια σχεδίασης για την απόδοση σχημάτων, κειμένου και εικόνων σε ένα bitmap ή άλλο context συσκευής.  

`Bitmap` είναι ένας κοντέινερ βασισμένος σε pixel που μπορεί να αποθηκευτεί σε κοινές μορφές εικόνας όπως PNG ή JPEG.  

`Graphics` είναι το καμβάς που σας επιτρέπει να σχεδιάζετε σχήματα, κείμενο ή άλλες εικόνες πάνω στο bitmap.

## Βήμα 2: εφαρμογή μετασχηματισμού περιστροφής (rotate 15°)
`RotateTransform` προσθέτει μια περιστροφή 15 μοιρών στον τρέχοντα πίνακα. Η μέθοδος ενημερώνει τον εσωτερικό πίνακα μετασχηματισμού του αντικειμένου `Graphics`, επηρεάζοντας όλα όσα σχεδιάζονται μετά.

## Βήμα 3: σχεδίαση περιστραμμένου έλλειψου μετά την περιστροφή
Επειδή ο πίνακας περιστροφής είναι ήδη ενεργός, η κλήση του `DrawEllipse` παράγει ένα έλλειψο που περιστρέφεται αυτόματα. Αυτό δείχνει **πώς να σχεδιάσετε περιστραμμένο έλλειψο** ενώ σέβεται τη global transform.

## Βήμα 4: αποθήκευση του αποτελέσματος
Μετά το σχεδιασμό, καλέστε `bitmap.Save` για να αποθηκεύσετε την εικόνα. Το αποθηκευμένο αρχείο αντικατοπτρίζει τη global rotation που εφαρμόστηκε τόσο στην εικόνα όσο και στο έλλειψο.

## Οφέλη της χρήσης global transformation
Η φόρτωση ενός μόνο πίνακα μία φορά και η επαναχρησιμοποίησή του εξαλείφει τον επαναλαμβανόμενο κώδικα και εξασφαλίζει ότι κάθε οπτικό στοιχείο μοιράζεται την ακριβώς ίδια προσανατολισμό, κάτι που είναι κρίσιμο για πίνακες ελέγχου, μετρητές ή sprites παιχνιδιών που πρέπει να παραμένουν συγχρονισμένα.

## Εφαρμογή μετασχηματισμού περιστροφής σε πραγματικά σενάρια
Φανταστείτε έναν πίνακα τηλεμετρίας όπου αρκετοί μετρητές περιστρέφονται γύρω από ένα κοινό κέντρο, ή ένα UI όπου τα εικονίδια πρέπει να περιστρέφονται μαζί όταν ο χρήστης αλλάζει προσανατολισμό. Χρησιμοποιώντας **apply rotation transform** μία φορά, αποφεύγετε τους υπολογισμούς ανά στοιχείο και διατηρείτε το UI ανταποκρινόμενο ακόμη και όταν δεκάδες αντικείμενα αποδίδονται σε κάθε καρέ.

## Παράδειγμα Graphics RotateTransform – κοινά προβλήματα & συμβουλές
- **Reset the transform**: Καλέστε `graphics.ResetTransform()` πριν σχεδιάσετε στοιχεία που πρέπει να παραμείνουν αμεταβλητά.  
- **Order matters**: Η περιστροφή πριν τη μετάφραση δίνει διαφορετικό οπτικό αποτέλεσμα από τη μετάφραση πριν την περιστροφή.  
- **Pixel format**: Η χρήση του `PixelFormat.Format32bppPArgb` παρέχει υψηλής ποιότητας αλφα blending για περιστραμμένα σχήματα.

## Συχνές ερωτήσεις

**Q: Είναι το Aspose.Drawing συμβατό με .NET Core;**  
A: Ναι, το Aspose.Drawing λειτουργεί σε .NET Core, .NET 5, .NET 6 και μεταγενέστερες εκδόσεις.

**Q: Μπορώ να εφαρμόσω πολλαπλές global transformations σε ένα μόνο graphics context;**  
A: Απόλυτα. Μπορείτε να αλυσίδετε `graphics.RotateTransform`, `graphics.ScaleTransform` και `graphics.TranslateTransform` για να δημιουργήσετε έναν σύνθετο πίνακα.

**Q: Πού μπορώ να βρω περισσότερα tutorials και παραδείγματα για το Aspose.Drawing;**  
A: Επισκεφθείτε το [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) για μια πληθώρα παραδειγμάτων και συζητήσεων που μοιράζεται η κοινότητα.

**Q: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.Drawing;**  
A: Ναι, μπορείτε να εξερευνήσετε μια δωρεάν δοκιμή του Aspose.Drawing [Aspose.Drawing free trial download](https://releases.aspose.com/).

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.Drawing;**  
A: Αποκτήστε μια προσωρινή άδεια για το Aspose.Drawing [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Ποιοι μορφές εικόνας υποστηρίζει το Aspose.Drawing για αποθήκευση;**  
A: Η βιβλιοθήκη υποστηρίζει πάνω από 30 μορφές raster και vector, συμπεριλαμβανομένων PNG, JPEG, BMP, TIFF, GIF και WebP.

**Q: Πώς μπορώ να βελτιώσω την ταχύτητα απόδοσης για μεγάλες εικόνες;**  
A: Χρησιμοποιήστε `PixelFormat.Format32bppPArgb` και εφαρμόστε τον μετασχηματισμό περιστροφής πριν από οποιεσδήποτε βαριές λειτουργίες σχεδίασης· αυτό ελαχιστοποιεί τους υπολογισμούς ανά pixel.

## Συμπέρασμα
Τώρα γνωρίζετε **πώς να σχεδιάσετε περιστραμμένο έλλειψο** και να περιστρέψετε εικόνες χρησιμοποιώντας τη δυνατότητα global transformation του Aspose.Drawing. Χρησιμοποιήστε το ίδιο μοτίβο για να προσθέσετε κλιμάκωση, στρίψη ή μετάφραση για πιο πλούσια γραφικά, και θυμηθείτε να επαναφέρετε τον πίνακα όταν χρειάζεστε μη‑περιστραμμένα στοιχεία. Πειραματιστείτε με διαφορετικές γωνίες και σύνθετους μετασχηματισμούς για να δημιουργήσετε δυναμικές απεικονίσεις σε οποιαδήποτε εφαρμογή .NET.

---

**Last Updated:** 2026-11-04  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Σχετικά tutorials

- [Πώς να Σχεδιάσετε Ορθογώνιο – Μετασχηματισμός Συστήματος Συντεταγμένων (Μετασχηματισμός Σελίδας) χρησιμοποιώντας Aspose.Drawing API για .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Tutorial Μετασχηματισμού Πίνακα: Matrix Transformations στο Aspose.Drawing για .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Βήμα προς Βήμα Μετασχηματισμός – Coordinate Transformations](/drawing/net/coordinate-transformations/)

```csharp
using System.Drawing;
```

```csharp
// Create a Bitmap with specified width, height, and pixel format
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);

// Create a Graphics object from the Bitmap
Graphics graphics = Graphics.FromImage(bitmap);

// Clear the canvas with a specified background color
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set a rotation transformation (15 degrees)
graphics.RotateTransform(15);
```

```csharp
// Create a Pen with specified color and width
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);

// Draw an ellipse using the specified pen and coordinates
graphics.DrawEllipse(pen, 300, 300, 400, 200);
```

```csharp
// Save the transformed image to the specified directory
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\GlobalTransformation_out.png");
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}