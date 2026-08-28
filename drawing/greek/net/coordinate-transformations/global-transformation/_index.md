---
date: 2026-08-28
description: Μάθετε πώς να σχεδιάζετε περιστρεφόμενη έλλειψη και να περιστρέφετε εικόνες
  χρησιμοποιώντας το global transformation του Aspose.Drawing στο .NET. Ακολουθήστε
  τον οδηγό βήμα‑βήμα για γραφικά υψηλής ποιότητας.
keywords:
- draw rotated ellipse
- set global rotation
- transformation matrix graphics
- global transformation .net
- rotate image without affecting
lastmod: 2026-08-28
linktitle: Global Transformation στο Aspose.Drawing για .NET
og_description: Σχεδιάστε περιστρεφόμενη έλλειψη και περιστρέψτε εικόνες χρησιμοποιώντας
  το global transformation του Aspose.Drawing στο .NET. Αυτό το σεμινάριο παρουσιάζει
  κώδικα βήμα‑βήμα και συμβουλές για γραφικά υψηλής ποιότητας.
og_image_alt: Screenshot of rotated ellipse created with Aspose.Drawing global transformation
og_title: Σχεδίαση περιστρεφόμενης έλλειψης με το Aspose.Drawing – οδηγός για global
  transformation
schemas:
- author: Aspose
  dateModified: '2026-08-28'
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
title: Πώς να σχεδιάσετε περιστρεφόμενη έλλειψη με το Aspose.Drawing
url: /el/net/coordinate-transformations/global-transformation/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να σχεδιάσετε περιστρεφόμενο έλλειψο με το Aspose.Drawing

## Εισαγωγή

Σε αυτόν τον οδηγό θα μάθετε **how to draw rotated ellipse** και θα περιστρέψετε εικόνες εφαρμόζοντας έναν **global transformation** πίνακα στο Aspose.Drawing για .NET. Ο global transformation επιτρέπει σε έναν μόνο πίνακα να επηρεάζει κάθε επόμενη κλήση σχεδίασης, ώστε να διατηρείτε τον κώδικά σας τακτικό ενώ δημιουργείτε σύνθετα οπτικά εφέ. Στο τέλος του οδηγού θα κατανοήσετε επίσης πώς να επαναφέρετε τον μετασχηματισμό ώστε άλλα γραφικά να παραμείνουν αμετάβλητα.

## Γρήγορες απαντήσεις
- **Τι είναι ένας global transformation;** Είναι ένας μοναδικός πίνακας που εφαρμόζεται αυτόματα σε όλες τις εντολές σχεδίασης που εκτελούνται μετά τη ρύθμισή του.  
- **Μπορώ να περιστρέψω μια εικόνα χωρίς να επηρεάσω άλλα αντικείμενα;** Ναι – σχεδιάστε το περιστρεφόμενο στοιχείο, έπειτα καλέστε `graphics.ResetTransform()` για να επιστρέψετε στην αρχική κατάσταση.  
- **Ποιο namespace παρέχει το API;** `System.Drawing` εκτίθεται μέσω του πακέτου Aspose.Drawing.  
- **Χρειάζομαι άδεια για παραγωγή;** Μια δωρεάν δοκιμή είναι επαρκής για μάθηση· απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις.  
- **Είναι η βιβλιοθήκη cross‑platform;** Απόλυτα – το Aspose.Drawing λειτουργεί σε .NET Core, .NET 5, .NET 6 και μεταγενέστερες εκδόσεις.

## Τι είναι ο global transformation;

Ένας **global transformation** είναι ένας πίνακας μετασχηματισμού που, αφού εφαρμοστεί σε ένα αντικείμενο `Graphics`, επηρεάζει κάθε επόμενη λειτουργία σχεδίασης μέχρι να αλλάξει ή να επαναφερθεί ο πίνακας. Λειτουργεί πολλαπλασιάζοντας τις συντεταγμένες κάθε σχεδιασμένου στοιχείου, επιτρέποντάς σας να περιστρέφετε, κλιμακώνετε, μεταφράζετε ή παραμορφώνετε όλα τα αντικείμενα ομοιόμορφα χωρίς να τροποποιείτε καθένα ξεχωριστά.

## Γιατί να χρησιμοποιήσετε global transformation;

Η εφαρμογή ενός global rotation σας επιτρέπει να περιστρέφετε πολλά αντικείμενα με μία κλήση, βελτιώνοντας την **συνέπεια**, μειώνοντας το **CPU overhead** (λιγότερους υπολογισμούς πινάκων) και επιτρέποντας **ευέλικτη σύνθεση** κλιμάκωσης, μετάφρασης και παραμόρφωσης. Το Aspose.Drawing μπορεί να διαχειριστεί εικόνες έως **10 000 × 10 000 px** και υποστηρίζει **30+** μορφές raster και vector, επεξεργαζόμενος τις στη μνήμη χωρίς ανάγκη προσωρινών αρχείων.

## Προαπαιτούμενα

- **Aspose.Drawing library** – κατεβάστε το από τον επίσημο ιστότοπο αναφοράς [Aspose.Drawing .NET reference](https://reference.aspose.com/drawing/net/).  
- **.NET development environment** – Visual Studio 2022, VS Code ή οποιοδήποτε IDE που υποστηρίζει .NET 6+.

## Εισαγωγή namespaces

Το namespace `System.Drawing` (παρέχεται από το Aspose.Drawing) περιέχει τους βασικούς τύπους γραφικών που θα χρησιμοποιήσετε.

```csharp
using System.Drawing;
```

## Πώς να περιστρέψετε εικόνα χρησιμοποιώντας global transformation

Φορτώστε ένα `Bitmap`, αποκτήστε το αντικείμενο `Graphics` του και στη συνέχεια ορίστε έναν πίνακα περιστροφής χρησιμοποιώντας `graphics.RotateTransform`. Αφού εφαρμοστεί ο μετασχηματισμός, οποιαδήποτε λειτουργία σχεδίασης—όπως η σχεδίαση άλλης εικόνας, σχημάτων ή κειμένου—θα αποδοθεί με την καθορισμένη περιστροφή. Τέλος, αποθηκεύστε το bitmap για να διατηρήσετε το παγκοσμίως περιστρεφόμενο περιεχόμενο.

```csharp
// Create a Bitmap with specified width, height, and pixel format
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);

// Create a Graphics object from the Bitmap
Graphics graphics = Graphics.FromImage(bitmap);

// Clear the canvas with a specified background color
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Βήμα 1: δημιουργία bitmap και graphics context

`Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη, ενώ `Graphics` παρέχει την επιφάνεια σχεδίασης.  

`Bitmap` είναι ένας κοντέινερ βασισμένος σε pixel που μπορεί να αποθηκευτεί σε κοινές μορφές εικόνας όπως PNG ή JPEG.  

`Graphics` είναι ο καμβάς που σας επιτρέπει να σχεδιάζετε σχήματα, κείμενο ή άλλες εικόνες πάνω στο bitmap.

```csharp
// Set a rotation transformation (15 degrees)
graphics.RotateTransform(15);
```

## Βήμα 2: εφαρμογή μετασχηματισμού περιστροφής (περιστροφή 15°)

`RotateTransform` προσθέτει μια περιστροφή 15 μοιρών στον τρέχοντα πίνακα. Η μέθοδος ενημερώνει τον εσωτερικό πίνακα μετασχηματισμού του αντικειμένου `Graphics`, επηρεάζοντας όλα όσα σχεδιάζονται μετά.

```csharp
// Create a Pen with specified color and width
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);

// Draw an ellipse using the specified pen and coordinates
graphics.DrawEllipse(pen, 300, 300, 400, 200);
```

## Βήμα 3: σχεδίαση περιστρεφόμενου έλλειψου μετά την περιστροφή

Επειδή ο πίνακας περιστροφής είναι ήδη ενεργός, η κλήση του `DrawEllipse` παράγει ένα έλλειψο που περιστρέφεται αυτόματα. Αυτό δείχνει **how to draw rotated ellipse** ενώ τηρεί τον global transform.

```csharp
// Save the transformed image to the specified directory
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\GlobalTransformation_out.png");
```

## Βήμα 4: αποθήκευση του αποτελέσματος

Μετά το σχεδιασμό, καλέστε `bitmap.Save` για να αποθηκεύσετε την εικόνα. Το αποθηκευμένο αρχείο αντικατοπτρίζει την global rotation που εφαρμόστηκε τόσο στην εικόνα όσο και στο έλλειψο.

## Οφέλη της χρήσης global transformation

Η φόρτωση ενός μοναδικού πίνακα μία φορά και η επαναχρησιμοποίησή του εξαλείφει τον επαναλαμβανόμενο κώδικα και εξασφαλίζει ότι κάθε οπτικό στοιχείο μοιράζεται την ακριβώς ίδια προσανατολισμό, κάτι που είναι κρίσιμο για πίνακες ελέγχου, μετρητές ή sprites παιχνιδιών που πρέπει να παραμένουν συγχρονισμένα.

## Εφαρμογή μετασχηματισμού περιστροφής σε πραγματικά σενάρια

Φανταστείτε έναν πίνακα τηλεμετρίας όπου πολλοί μετρητές περιστρέφονται γύρω από ένα κοινό κέντρο, ή ένα UI όπου τα εικονίδια πρέπει να περιστρέφονται μαζί όταν ο χρήστης αλλάζει προσανατολισμό. Χρησιμοποιώντας **apply rotation transform** μία φορά, αποφεύγετε υπολογισμούς ανά στοιχείο και διατηρείτε το UI ανταποκρινόμενο ακόμη και όταν δεκάδες αντικείμενα αποδίδονται σε κάθε καρέ.

## Παράδειγμα Graphics RotateTransform – κοινά λάθη & συμβουλές

- **Επαναφορά του μετασχηματισμού**: Καλέστε `graphics.ResetTransform()` πριν σχεδιάσετε στοιχεία που πρέπει να παραμείνουν μη περιστραμμένα.  
- **Η σειρά έχει σημασία**: Η περιστροφή πριν τη μετάφραση δίνει διαφορετικό οπτικό αποτέλεσμα από τη μετάφραση πριν την περιστροφή.  
- **Μορφή pixel**: Η χρήση του `PixelFormat.Format32bppPArgb` παρέχει υψηλής ποιότητας αλφα blending για περιστρεφόμενα σχήματα.

## Συχνές ερωτήσεις

**Ε: Είναι το Aspose.Drawing συμβατό με .NET Core;**  
**Α:** Ναι, το Aspose.Drawing λειτουργεί σε .NET Core, .NET 5, .NET 6 και μεταγενέστερες εκδόσεις.

**Ε: Μπορώ να εφαρμόσω πολλαπλούς global transformations σε ένα μόνο graphics context;**  
**Α:** Απόλυτα. Μπορείτε να αλυσίδετε `graphics.RotateTransform`, `graphics.ScaleTransform` και `graphics.TranslateTransform` για να δημιουργήσετε έναν σύνθετο πίνακα.

**Ε: Πού μπορώ να βρω περισσότερα tutorials και παραδείγματα για το Aspose.Drawing;**  
**Α:** Επισκεφθείτε το [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) για μια πληθώρα παραδειγμάτων και συζητήσεων που μοιράζεται η κοινότητα.

**Ε: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.Drawing;**  
**Α:** Ναι, μπορείτε να εξερευνήσετε μια δωρεάν δοκιμή του Aspose.Drawing [Aspose.Drawing free trial download](https://releases.aspose.com/).

**Ε: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.Drawing;**  
**Α:** Αποκτήστε μια προσωρινή άδεια για το Aspose.Drawing [temporary license page](https://purchase.aspose.com/temporary-license/).

## Συμπέρασμα

Τώρα γνωρίζετε **how to draw rotated ellipse** και πώς να περιστρέφετε εικόνες χρησιμοποιώντας τη δυνατότητα global transformation του Aspose.Drawing. Χρησιμοποιήστε το ίδιο μοτίβο για να προσθέσετε κλιμάκωση, παραμόρφωση ή μετάφραση για πιο πλούσια γραφικά, και θυμηθείτε να επαναφέρετε τον πίνακα όταν χρειάζεστε μη περιστραμμένα στοιχεία. Πειραματιστείτε με διαφορετικές γωνίες και σύνθετους μετασχηματισμούς για να δημιουργήσετε δυναμικές απεικονίσεις σε οποιαδήποτε εφαρμογή .NET.

---

**Last Updated:** 2026-08-28  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Σχετικά Tutorials

- [Πώς να Σχεδιάσετε Ορθογώνιο – Μετασχηματισμός Συστήματος Συντεταγμένων (Μετασχηματισμός Σελίδας) χρησιμοποιώντας το Aspose.Drawing API για .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Μάθημα Μετασχηματισμού Πίνακα: Μετασχηματισμοί Πίνακα στο Aspose.Drawing για .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Βήμα προς Βήμα Μετασχηματισμός – Μετασχηματισμοί Συντεταγμένων](/drawing/net/coordinate-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}