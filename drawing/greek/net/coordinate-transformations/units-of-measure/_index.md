---
date: 2026-05-24
description: Μάθετε πώς να ορίσετε τη μονάδα στο Aspose.Drawing for .NET, να μετατρέψετε
  εύκολα τις μονάδες γραφικών και να κατακτήσετε ακριβείς μετρήσεις για την απόδοση
  γραφικών.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Units of Measure στο Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Πώς να ορίσετε τη μονάδα στο Aspose.Drawing for .NET – Units of Measure
url: /el/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να ορίσετε μονάδα στο Aspose.Drawing για .NET – Μονάδες μέτρησης

## Εισαγωγή

Καλώς ήρθατε στον κόσμο του Aspose.Drawing για .NET, όπου η ακρίβεια και η ευελιξία συναντώνται στη διαχείριση γραφικών. Σε αυτό το tutorial θα ανακαλύψετε **πώς να ορίσετε μονάδα** για τα σχέδιά σας, θα μάθετε να **μετατρέπετε μονάδες γραφικών** μεταξύ σημείων, χιλιοστών και ιντσών, και θα δείτε παραδείγματα από την πραγματική ζωή που κάνουν τις εικόνες σας τέλειες σε pixel. Είτε δημιουργείτε αναφορές, μικρογραφίες ή προσαρμοσμένα διαγράμματα, η κατανόηση των μονάδων μέτρησης είναι απαραίτητη για συνεπή απόδοση σε όλες τις συσκευές.

## Σύντομες Απαντήσεις
- **Ποιος είναι ο κύριος τρόπος αλλαγής μονάδων;** Καλέστε `graphics.PageUnit = PageUnit.Point` (ή `.Millimeter`, `.Inch`) στο αντικείμενο `Graphics`.  
- **Ποια μονάδα ισούται με 1/72 ίντσα;** Points.  
- **Πόσα χιλιοστά υπάρχουν σε μια ίντσα;** 25.4 mm = 1 inch.  
- **Χρειάζομαι επιπλέον βιβλιοθήκες για τη χρήση μονάδων;** Όχι, η βασική βιβλιοθήκη Aspose.Drawing παρέχει όλες τις σταθερές μονάδων.  
- **Μπορώ να αναμείξω μονάδες σε μία εικόνα;** Ορίστε τη μονάδα μία φορά ανά αντικείμενο `Graphics`; σχεδιάστε όλα χρησιμοποιώντας αυτή τη μονάδα για συνέπεια.

## Προαπαιτούμενα

Πριν βυθιστούμε στο tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:

- Aspose.Drawing for .NET: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη. Μπορείτε να τη κατεβάσετε [εδώ](https://releases.aspose.com/drawing/net/).
- Φάκελος Εγγράφων: Έχετε έναν καθορισμένο φάκελο όπου θέλετε να αποθηκεύσετε τα δημιουργημένα έγγραφα.
- Βασικές Γνώσεις C#: Συνιστάται μια θεμελιώδης κατανόηση της C# για να αξιοποιήσετε πλήρως αυτόν τον οδηγό.

## Εισαγωγή Ονομάτων Χώρων

Πριν ξεκινήσουμε, ας εισάγουμε τα απαραίτητα ονόματα χώρων για να χρησιμοποιήσουμε το Aspose.Drawing αποτελεσματικά:

```csharp
using System.Drawing;
```

Τώρα, ας αναλύσουμε κάθε παράδειγμα σε πολλαπλά βήματα:

## Πώς να ορίσετε μονάδα σε Σημεία;

Η κλάση `Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη που λειτουργεί ως καμβάς σχεδίασης. Φορτώστε το bitmap σας, δημιουργήστε ένα αντικείμενο `Graphics` και ορίστε τη μονάδα σε σημεία — αυτό λέει στο Aspose.Drawing να ερμηνεύει όλες τις συντεταγμένες ως τιμές 1/72 ίντσας. Η χρήση σημείων σας δίνει λεπτομερή έλεγχο για γραφικά έτοιμα για εκτύπωση και σας επιτρέπει να καθορίζετε το πλάτος των γραμμών με υψηλή ακρίβεια.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Βήμα 1: Δημιουργία Bitmap  
Η κλάση `Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη που λειτουργεί ως καμβάς σχεδίασης.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Βήμα 2: Δημιουργία Αντικειμένου Graphics  
`Graphics` παρέχει μεθόδους σχεδίασης για την απόδοση σχημάτων και κειμένου πάνω σε ένα `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Βήμα 3: Ορισμός Μονάδας Σελίδας σε Σημεία  
`PageUnit` είναι μια απαρίθμηση που καθορίζει τη μονάδα μέτρησης για τις συντεταγμένες της σελίδας. `PageUnit.Point` ορίζει τα σημεία ως μονάδα μέτρησης (1 σημείο = 1/72 ίντσα). Αυτή η ρύθμιση εφαρμόζεται σε όλες τις επόμενες κλήσεις σχεδίασης.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Βήμα 4: Σχεδίαση Ορθογωνίου σε Σημεία  
Όταν σχεδιάζετε ένα ορθογώνιο μετά τον ορισμό της μονάδας, οι διαστάσεις που καθορίζετε ερμηνεύονται ως σημεία, εξασφαλίζοντας ακριβή μέγεθος.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Πώς να ορίσετε μονάδα σε Χιλιοστά;

`PageUnit` είναι μια απαρίθμηση που καθορίζει τη μονάδα μέτρησης για τις συντεταγμένες της σελίδας. Η αλλαγή σε χιλιοστά είναι χρήσιμη όταν χρειάζεστε μετρικές διαστάσεις, για παράδειγμα κατά τη δημιουργία διαγραμμάτων μηχανικής. Το Aspose.Drawing αντιμετωπίζει το 1 mm ως 1/25.4 ίντσα, επιτρέποντάς σας να ευθυγραμμίζετε τα γραφικά με φυσικές μετρήσεις που χρησιμοποιούνται στην παραγωγή και την τεχνική τεκμηρίωση.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Βήμα 1: Ορισμός Μονάδας Σελίδας σε Χιλιοστά  
Αναθέστε `PageUnit.Millimeter` στο αντικείμενο `Graphics`; όλες οι συντεταγμένες τώρα αντιστοιχούν στο μετρικό σύστημα.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Βήμα 2: Σχεδίαση Ορθογωνίου σε Χιλιοστά  
Το πλάτος και το ύψος του ορθογωνίου εκφράζονται τώρα σε χιλιοστά, καθιστώντας εύκολη την ευθυγράμμιση με φυσικές μετρήσεις και εξασφαλίζοντας ότι η εκτυπωμένη έξοδος ταιριάζει με τις πραγματικές διαστάσεις.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Πώς να ορίσετε μονάδα σε Ίντσες;

`Graphics` παρέχει μεθόδους σχεδίασης για την απόδοση σχημάτων και κειμένου πάνω σε ένα `Bitmap`. Οι ίντσες είναι η προεπιλεγμένη μονάδα για πολλά αμερικανικά εργαλεία σχεδίασης. Ορίζοντας τη μονάδα σε ίντσες, μπορείτε να σκέφτεστε με γνωστούς όρους κατά την τοποθέτηση στοιχείων UI, και απλοποιεί τη μετάβαση από το σχεδιασμό οθόνης στην εκτύπωση όπου οι ίντσες χρησιμοποιούνται συνήθως.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Βήμα 1: Ορισμός Μονάδας Σελίδας σε Ίντσες  
`PageUnit.Inch` αλλάζει το σύστημα συντεταγμένων ώστε 1 μονάδα να ισούται με 1 ίντσα, παρέχοντας έναν απλό τρόπο για να διαμορφώσετε στοιχεία για διατάξεις προσανατολισμένες στην εκτύπωση.

CODE_BLOCK_PLACEHOLDER_10_END

### Βήμα 2: Σχεδίαση Ορθογωνίου σε Ίντσες  
Τώρα οποιοδήποτε σχήμα σχεδιάζετε χρησιμοποιεί τις ίντσες ως βάση μέτρησης, κάτι που είναι ιδανικό για διατάξεις εκτύπωσης και για την επικοινωνία διαστάσεων σε ενδιαφερόμενους που είναι εξοικειωμένοι με τις αυτοκρατορικές μονάδες.

CODE_BLOCK_PLACEHOLDER_11_END

## Αποθήκευση του Αποτελέσματος

Μετά την ολοκλήρωση των παραδειγμάτων, αποθηκεύστε την προκύπτουσα εικόνα στον φάκελο εγγράφων σας. Η μέθοδος `Bitmap.Save` γράφει το αρχείο στη μορφή που καθορίζετε (PNG, JPEG, κ.λπ.).

CODE_BLOCK_PLACEHOLDER_12_END

Τώρα, έχετε πλοηγηθεί επιτυχώς στις διάφορες μονάδες μέτρησης στο Aspose.Drawing για .NET, δημιουργώντας μια οπτική αναπαράσταση ορθογωνίων χρησιμοποιώντας σημεία, χιλιοστά και ίντσες.

## Γιατί να χρησιμοποιήσετε το σύστημα μονάδων του Aspose.Drawing;

Το Aspose.Drawing υποστηρίζει **πάνω από 30 μορφές εικόνας** και μπορεί να επεξεργαστεί εικόνες έως **5000 × 5000 pixel** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, παρέχοντας υψηλή απόδοση για δημιουργία γραφικών μεγάλης κλίμακας. Ορίζοντας ρητά τη μονάδα, εξαλείφετε τις εικασίες, μειώνετε τα σφάλματα μετατροπής και εξασφαλίζετε ότι η έξοδός σας ταιριάζει με ακριβείς φυσικές διαστάσεις σε όλες τις πλατφόρμες.

## Συνηθισμένα Προβλήματα και Λύσεις

- **Απρόσμενο μέγεθος μετά την αποθήκευση** – Βεβαιωθείτε ότι έχετε ορίσει `graphics.PageUnit` **πριν** από οποιεσδήποτε κλήσεις σχεδίασης· η αλλαγή της μονάδας αργότερα δεν αλλάζει ρετροακτιβικά τα υπάρχοντα σχήματα.  
- **Θολή έξοδος σε οθόνες υψηλής ανάλυσης DPI** – Αυξήστε την ανάλυση του bitmap (π.χ., `new Bitmap(width, height, 300)`) ώστε να ταιριάζει με το επιθυμητό DPI.  
- **Αναμικτές μονάδες σε μία εικόνα** – Δημιουργήστε ξεχωριστά αντικείμενα `Graphics` για κάθε μονάδα ή πραγματοποιήστε χειροκίνητη μετατροπή πριν τη σχεδίαση.

## Συχνές Ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.Drawing για .NET με άλλα .NET frameworks;
Α1: Ναι, το Aspose.Drawing είναι συμβατό με διάφορα .NET frameworks, παρέχοντας ευελιξία στο περιβάλλον ανάπτυξής σας.

### Ε2: Υπάρχει διαθέσιμη δωρεάν δοκιμή;
Α2: Ναι, μπορείτε να εξερευνήσετε το Aspose.Drawing με δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Ε3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Drawing για .NET;
Α3: Επισκεφθείτε το [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) για υποστήριξη κοινότητας και συζητήσεις.

### Ε4: Μπορώ να αγοράσω προσωρινή άδεια για βραχυπρόθεσμα έργα;
Α4: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.Drawing;
Α5: Η πλήρης τεκμηρίωση είναι διαθέσιμη [εδώ](https://reference.aspose.com/drawing/net/).

---

**Τελευταία ενημέρωση:** 2026-05-24  
**Δοκιμή με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
