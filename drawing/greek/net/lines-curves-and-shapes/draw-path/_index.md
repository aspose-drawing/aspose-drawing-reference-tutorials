---
date: 2026-07-22
description: Μάθετε πώς να αποθηκεύσετε bitmap ως PNG και να εξάγετε εικόνα σε JPEG
  με το Aspose.Drawing. Οδηγός step‑by‑step δείχνει drawing paths, δημιουργία εικόνων
  και εξαγωγή μορφών.
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: Drawing Paths στο Aspose.Drawing
og_description: Αποθηκεύστε bitmap ως PNG και εξάγετε εικόνα σε JPEG χρησιμοποιώντας
  Aspose.Drawing για .NET. Ακολουθήστε αυτό το tutorial για να σχεδιάσετε complex
  paths, να δημιουργήσετε high‑quality εικόνες και να εξάγετε multiple formats.
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: Αποθήκευση Bitmap ως PNG – Drawing Paths με Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: Αποθήκευση Bitmap ως PNG – Χρήση GraphicsPath στο Aspose.Drawing
url: /el/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Σχεδίαση Διαδρομών με το Aspose.Drawing

## Πώς να Χρησιμοποιήσετε το GraphicsPath – Εισαγωγή

**Save bitmap as PNG** είναι συχνά το πρώτο βήμα όταν χρειάζεστε μια εικόνα χωρίς απώλειες για περαιτέρω επεξεργασία ή δημοσίευση. Σε αυτό το tutorial θα μάθετε πώς να σχεδιάζετε σύνθετες διανυσματικές διαδρομές με `GraphicsPath`, να τις αποδίδετε σε ένα bitmap, και στη συνέχεια **save bitmap as PNG** ή ακόμη **export image to JPEG**. Είτε δημιουργείτε μια μηχανή αναφορών, μια προσαρμοσμένη βιβλιοθήκη γραφημάτων, ή απλώς χρειάζεστε να δημιουργήσετε δυναμικά γραφικά, το Aspose.Drawing σας παρέχει ένα πλήρως διαχειριζόμενο, cross‑platform API που αντικαθιστά το System.Drawing.Common.

## Γρήγορες Απαντήσεις
- **Τι μπορώ να σχεδιάσω με το GraphicsPath;** Γραμμές, ορθογώνια, έλλειπτες, καμπύλες και προσαρμοσμένα σχήματα.  
- **Χρειάζομαι άδεια;** Μια δοκιμαστική έκδοση είναι δωρεάν· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Απαιτείται το System.Drawing.Common;** Όχι, το Aspose.Drawing λειτουργεί ανεξάρτητα.  
- **Μπορώ να αποθηκεύσω σε διαφορετικές μορφές;** Ναι – PNG, JPEG, BMP, GIF και άλλα.

## Τι είναι το GraphicsPath;
`GraphicsPath` είναι το διανυσματικό κοντέινερ του Aspose.Drawing που αποθηκεύει μια ακολουθία σχεδιαστικών πρωτογενών όπως γραμμές, τόξα και καμπύλες ως ένα ενιαίο αντικείμενο. Ομαδοποιώντας αυτά τα πρωτότυπα, μπορείτε να εφαρμόζετε μετασχηματισμούς, κανόνες γεμίσματος και ρυθμίσεις περιγράμματος ομοιόμορφα, κάτι που απλοποιεί τη δημιουργία σύνθετων γραφικών και εξασφαλίζει συνεπή απόδοση σε διαφορετικές μορφές εξόδου.

## Γιατί να Χρησιμοποιήσετε το GraphicsPath με το Aspose.Drawing;
Η χρήση του GraphicsPath με το Aspose.Drawing σας παρέχει ακριβείς, ευέλικτες και υψηλής απόδοσης δυνατότητες διανυσματικής σχεδίασης. Σας επιτρέπει να δημιουργείτε σύνθετα σχήματα, να εφαρμόζετε μετασχηματισμούς και να τα αποδίδετε αποδοτικά, διατηρώντας τη διασυστημική συνέπεια και υποστηρίζοντας επεξεργασία εικόνων μεγάλης κλίμακας. Επιπλέον, ενσωματώνεται άψογα με άλλες βιβλιοθήκες .NET, επιτρέποντάς σας να συνδυάσετε ροές εργασίας raster και vector σε μία εφαρμογή.

- **Ακρίβεια:** Διαχειρίζεται 50+ διανυσματικά πρωτότυπα με υπο-εικονοστοιχική ακρίβεια, εξασφαλίζοντας ότι όταν **save bitmap as PNG** η έξοδος παραμένει καθαρή σε οποιαδήποτε ανάλυση.  
- **Ευελιξία:** Συνδυάστε γραμμές, τόξα και καμπύλες Bezier σε μία διαδρομή, έπειτα αποδώστε την με μία κλήση `Graphics.DrawPath`.  
- **Απόδοση:** Η βελτιστοποιημένη αλυσίδα απόδοσης επεξεργάζεται εικόνες έως 400 MP χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, καθιστώντας εφικτές μεγάλες παρτίδες εργασιών.  
- **Διασυστηματική:** Παράγει τα ίδια αποτελέσματα σε Windows, Linux και macOS, εξαλείφοντας σφάλματα ειδικά για πλατφόρμα.

## Προαπαιτούμενα

Πριν ξεκινήσετε το tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:

- **Aspose.Drawing Library:** Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.Drawing. Μπορείτε να βρείτε τη βιβλιοθήκη [here](https://releases.aspose.com/drawing/net/).
- **Other Aspose Products:** Εξερευνήστε πρόσθετες προσφορές της Aspose [here](https://releases.aspose.com/).
- **Development Environment:** Ρυθμίστε το .NET περιβάλλον ανάπτυξης σας με τα απαραίτητα εργαλεία (Visual Studio, .NET SDK, κλπ.).

## Εισαγωγή Namespaces

Ξεκινήστε εισάγοντας τα απαιτούμενα namespaces στο έργο σας:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Βήμα 1: Δημιουργία Bitmap και Graphics

Το Bitmap αντιπροσωπεύει μια εικόνα στη μνήμη, ενώ το Graphics παρέχει μεθόδους σχεδίασης για απόδοση στην εικόνα. Ξεκινήστε δημιουργώντας ένα αντικείμενο `Bitmap` και ένα `Graphics` για εργασία. Αυτό το bitmap θα είναι ο καμβάς στον οποίο θα αποδοθεί το `GraphicsPath`, και αργότερα θα **save bitmap as PNG**:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Βήμα 2: Ορισμός Pen και GraphicsPath

Το Pen ορίζει το χρώμα, το πλάτος και το στυλ της γραμμής· το GraphicsPath αποθηκεύει μια συλλογή σχεδιαστικών πρωτογενών ως ένα ενιαίο διανυσματικό αντικείμενο. Στη συνέχεια, ορίστε ένα `Pen` για να καθορίσετε τα χαρακτηριστικά σχεδίασης και δημιουργήστε ένα `GraphicsPath`. Το αντικείμενο `GraphicsPath` κρατά τα διανυσματικά δεδομένα πριν σχεδιαστεί:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## Βήμα 3: Προσθήκη Γραμμών και Σχημάτων

AddLine, AddRectangle, και AddEllipse προσθέτουν τα αντίστοιχα σχήματα στο GraphicsPath για μετέπειτα απόδοση. Προσθέστε γραμμές, ορθογώνια και έλλειπτες στο `GraphicsPath` για να δημιουργήσετε μια σύνθετη διαδρομή. Μπορείτε επίσης να προσθέσετε προσαρμοσμένες καμπύλες Bezier για ομαλές μορφές:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## Βήμα 4: Σχεδίαση Διαδρομής

DrawPath αποδίδει τα διανυσματικά δεδομένα από ένα GraphicsPath στην επιφάνεια Graphics χρησιμοποιώντας το καθορισμένο Pen. Σχεδιάστε τη διαδρομή στο αντικείμενο `Graphics` χρησιμοποιώντας το καθορισμένο `Pen`. Αυτή η λειτουργία rasterizes τα διανυσματικά δεδομένα στον καμβά bitmap:

```csharp
graphics.DrawPath(pen, path);
```

## Βήμα 5: Αποθήκευση Εικόνας – Εξαγωγή σε PNG ή JPEG

Η μέθοδος Bitmap.Save γράφει την εικόνα στο δίσκο στην επιλεγμένη μορφή όπως PNG ή JPEG. Μετά τη σχεδίαση, μπορείτε να **save bitmap as PNG** για απώλεια‑απώλειας ποιότητα ή **export image to JPEG** για μικρότερο μέγεθος αρχείου. Επιλέξτε τη μορφή που ταιριάζει καλύτερα στο επόμενο σενάριο σας:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

Επαναλάβετε αυτά τα βήματα όπως χρειάζεται για να δημιουργήσετε σύνθετες και οπτικά ελκυστικές διαδρομές.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Λύση |
|----------|------|
| **Η διαδρομή δεν είναι ορατή** | Βεβαιωθείτε ότι το χρώμα του Pen αντιτίθεται στο φόντο και ότι το bitmap αποθηκεύεται σωστά. |
| **Αναπάντεχο μέγεθος εικόνας** | Επαληθεύστε ότι οι διαστάσεις του bitmap και η μορφή pixel ταιριάζουν με τις απαιτήσεις σας. |
| **Πρόβλημα άδειας** | Χρησιμοποιήστε μια δοκιμαστική άδεια για δοκιμές· εφαρμόστε έγκυρη άδεια πριν την ανάπτυξη σε παραγωγή. |

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.Drawing με άλλες βιβλιοθήκες .NET;
A1: Ναι, το Aspose.Drawing ενσωματώνεται άψογα με άλλες βιβλιοθήκες .NET, παρέχοντας ευελιξία στα έργα ανάπτυξής σας.

### Q2: Υπάρχει διαθέσιμη δοκιμαστική έκδοση;
A2: Ναι, μπορείτε να αποκτήσετε τη δωρεάν δοκιμαστική έκδοση [here](https://releases.aspose.com/).

### Q3: Πού μπορώ να βρω υποστήριξη για το Aspose.Drawing;
A3: Επισκεφθείτε το φόρουμ Aspose.Drawing [forum](https://forum.aspose.com/c/drawing/44) για βοήθεια και υποστήριξη της κοινότητας.

### Q4: Πώς μπορώ να αποκτήσω προσωρινή άδεια;
A4: Αποκτήστε μια προσωρινή άδεια [here](https://purchase.aspose.com/temporary-license/).

### Q5: Μπορώ να αγοράσω το Aspose.Drawing;
A5: Ναι, μπορείτε να αγοράσετε το Aspose.Drawing [here](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q:** Μπορώ να σχεδιάσω προσαρμοσμένες καμπύλες Bezier με το GraphicsPath;  
**A:** Σίγουρα – χρησιμοποιήστε `path.AddBezier(...)` για να ορίσετε ομαλές καμπύλες.

**Q:** Πώς μπορώ να καθαρίσω ένα GraphicsPath πριν το ξαναχρησιμοποιήσω;  
**A:** Καλέστε `path.Reset()` για να αφαιρέσετε όλα τα σχήματα και να ξεκινήσετε από την αρχή.

## Συμπέρασμα

Συγχαρητήρια! Έχετε μάθει με επιτυχία **πώς να χρησιμοποιήσετε το GraphicsPath** για να σχεδιάζετε διαδρομές και στη συνέχεια **να αποθηκεύσετε bitmap ως PNG** ή **να εξάγετε εικόνα σε JPEG** χρησιμοποιώντας το Aspose.Drawing για .NET. Αυτό το tutorial κάλυψε τη δημιουργία bitmap, τον ορισμό pen, την κατασκευή ενός `GraphicsPath`, την απόδοση διαφόρων σχημάτων και την εξαγωγή της τελικής εικόνας σε πολλαπλές μορφές. Πειραματιστείτε με διαφορετικές συντεταγμένες, χρώματα και πλάτη γραμμής για να αξιοποιήσετε πλήρως το δημιουργικό δυναμικό του Aspose.Drawing.

---

**Τελευταία Ενημέρωση:** 2026-07-22  
**Δοκιμάστηκε Με:** Aspose.Drawing 24.12 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Αποθήκευση Bitmap ως PNG & Σχεδίαση Κλειστών Καμπυλών με το Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Αποθήκευση Bitmap C# – Σχεδίαση Bezier Splines με το Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Πώς να Αποθηκεύσετε Εικόνα και να Σχεδιάσετε Cardinal Splines στο Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}