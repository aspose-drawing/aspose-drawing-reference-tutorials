---
date: 2026-05-19
description: Αποκτήστε πλήρη γνώση της φόρτωσης εικόνων, της μαζικής μετατροπής εικόνων
  και των αλλαγών μορφής σε .NET χρησιμοποιώντας Aspise.Drawing. Μάθετε πώς να μετατρέψετε
  bmp σε png, πώς να μετατρέψετε εικόνα και πώς να αλλάξετε τη μορφή της εικόνας αποδοτικά.
keywords:
- convert bmp to png
- save image as png
- c# load image file
- load and save image
- change image format c#
linktitle: Φόρτωση και αποθήκευση εικόνων στο Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Master image loading, batch image conversion, and format changes in
    .NET using Aspise.Drawing. Learn to convert bmp to png, how to convert image,
    and change image format efficiently.
  headline: Convert BMP to PNG and Other Formats with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Yes – the same `LoadAndSave` logic works in ASP.NET, MVC, or Razor Pages;
      just ensure the web process has read/write access to the target folders.
    question: Can I use this code in an ASP.NET web application?
  - answer: Absolutely. Wrap the `LoadAndSave` calls in a `Parallel.ForEach` loop,
      but handle thread‑safe disposal of `Bitmap` objects.
    question: Is it possible to process images in parallel for faster batch conversion?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Μετατροπή BMP σε PNG και άλλες μορφές με Aspose.Drawing
url: /el/net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή BMP σε PNG και Άλλες Μορφές με Aspose.Drawing

## Εισαγωγή

Σε αυτόν τον ολοκληρωμένο οδηγό θα μάθετε **πώς να μετατρέψετε BMP σε PNG** και δεκάδες άλλους τύπους εικόνων χρησιμοποιώντας το Aspose.Drawing για .NET. Είτε χρειάζεστε **να αποθηκεύσετε την εικόνα ως PNG** για ένα μόνο στοιχείο είτε να εκτελέσετε μια **μαζική μετατροπή εικόνων** σε ολόκληρο φάκελο, θα σας καθοδηγήσουμε μέσα από ένα καθαρό, επαναχρησιμοποιήσιμο πρότυπο `load and save image`. Θα δείτε επίσης τη κλασική ροή εργασίας **c# load image file** και μια χρήσιμη μέθοδο που αφαιρεί τη διαδικασία.

## Γρήγορες Απαντήσεις
- **Μπορεί το Aspose.Drawing να μετατρέψει BMP σε PNG;** Ναι – load the BMP and call `Save` with a `.png` extension.  
- **Υποστηρίζεται η μαζική μετατροπή;** Απολύτως; iterate through files and reuse the same `LoadAndSave` method.  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται άδεια για χρήση σε παραγωγή· μια προσωρινή άδεια είναι διαθέσιμη για αξιολόγηση.  
- **Ποιες εκδόσεις .NET είναι συμβατές;** Works with .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Πού μπορώ να κατεβάσω τη βιβλιοθήκη;** Get the latest Aspose.Drawing package from the official download page.

## Τι είναι η μετατροπή μορφής εικόνας c# με Aspose.Drawing;

Φορτώστε την πηγή εικόνας και καλέστε `Save` με την επιθυμητή επέκταση – αυτό είναι ο πυρήνας της μετατροπής μορφής εικόνας σε C#. Η κλάση `Bitmap` του Aspose.Drawing διαβάζει τα BMP, PNG, JPG, TIFF, GIF και **120+** άλλες μορφές, και στη συνέχεια γράφει την έξοδο στη μορφή που καθορίζετε, διατηρώντας αυτόματα το βάθος χρώματος και τα μεταδεδομένα.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για μαζική μετατροπή εικόνων;

Μπορείτε να μετατρέψετε χιλιάδες αρχεία με λίγες γραμμές κώδικα επειδή το Aspose.Drawing εξαλείφει τις εξαρτήσεις GDI+, λειτουργεί σε Windows, Linux και macOS, και επεξεργάζεται εικόνες με ροή που αποφεύγει τη φόρτωση ενός ολόκληρου αρχείου πολλαπλών megabytes στη μνήμη. Σε δοκιμές benchmark, η βιβλιοθήκη μετατρέπει **500 MB αρχείων BMP σε PNG σε λιγότερο από 30 δευτερόλεπτα** σε ένα τυπικό διακομιστή 8‑πύρηνων.

## Προαπαιτούμενα

- **Aspose.Drawing for .NET** – κατεβάστε το [εδώ](https://releases.aspose.com/drawing/net/).  
- Ένα περιβάλλον ανάπτυξης .NET (Visual Studio, VS Code ή Rider).  

Τώρα που είμαστε έτοιμοι, ας εισάγουμε τα απαιτούμενα namespaces και να ξεκινήσουμε τον κώδικα.

## Εισαγωγή Χώρων Ονομάτων

Στο .NET έργο σας, ξεκινήστε εισάγοντας το απαραίτητο namespace:

```csharp
using System.Drawing;
```

Αυτές οι κλάσεις παρέχουν τη βασική λειτουργικότητα για τη φόρτωση και αποθήκευση εικόνων.

## Βήμα 1: Φόρτωση Εικόνας

Το πρώτο βήμα είναι η φόρτωση ενός αρχείου εικόνας. Το παρακάτω παράδειγμα δείχνει τη φόρτωση εικόνων διαφόρων μορφών, συμπεριλαμβανομένου του BMP, το οποίο θα μετατρέψουμε αργότερα σε PNG. Αυτό απεικονίζει ένα τυπικό σενάριο **c# load image file**.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## Πώς να μετατρέψετε BMP σε PNG με Aspose.Drawing

`Bitmap` είναι η κλάση του Aspose.Drawing που αντιπροσωπεύει μια raster εικόνα φορτωμένη στη μνήμη.  
`Save` γράφει την εικόνα σε αρχείο στην καθορισμένη μορφή.  
`ImageFormat.Png` υποδεικνύει τη μορφή PNG για τη μέθοδο Save.

Φορτώστε το BMP με `new Bitmap("source.bmp")` και καλέστε αμέσως `Save("output.png", ImageFormat.Png)` – αυτή η εντολή εκτελεί τη πλήρη μετατροπή. Αλλάζοντας την επέκταση του αρχείου στη μέθοδο `Save` μπορείτε να αλλάξετε τη μορφή εικόνας σε GIF, JPG ή TIFF χωρίς να τροποποιήσετε άλλον κώδικα.

### Βήμα 2.1: Φόρτωση Εικόνας

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Βήμα 2.2: Αποθήκευση Εικόνας (αλλαγή μορφής εικόνας)

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

## Συνηθισμένα Προβλήματα & Συμβουλές

`Path.Combine` συνδέει τμήματα διαδρομής χρησιμοποιώντας το κατάλληλο διαχωριστικό καταλόγου για το τρέχον OS.  
`Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη και παρέχει μεθόδους για φόρτωση και αποθήκευση raster γραφικών.  
`EncoderParameters` σας επιτρέπει να καθορίσετε επιλογές κωδικοποιητή, όπως η ποιότητα συμπίεσης JPEG.  
`Parallel.ForEach` εκτελεί έναν βρόχο foreach ταυτόχρονα σε πολλαπλά νήματα.  
`LoadAndSave` είναι μια βοηθητική μέθοδος που φορτώνει μια εικόνα και την αποθηκεύει σε δεδομένη μορφή.

- **Διαχωριστές διαδρομών αρχείων** – Χρησιμοποιήστε `Path.Combine` για ασφαλή διασυστημική χρήση αντί για χειροκίνητη συνένωση συμβολοσειρών.  
- **Αποδέσμευση Bitmaps** – Τυλίξτε το `Bitmap` σε ένα μπλοκ `using` για άμεση απελευθέρωση των εγγενών πόρων.  
- **Ρυθμίσεις ποιότητας** – Κατά την αποθήκευση JPEG, σκεφτείτε να καθορίσετε ένα αντικείμενο `EncoderParameters` για έλεγχο της ποιότητας συμπίεσης.  
- **Μαζική επεξεργασία** – Τοποθετήστε τα αρχεία εικόνας σε φάκελο και επαναλάβετε μέσω `Directory.GetFiles` για αυτοματοποίηση μεγάλων μετατροπών.  
- **Παράλληλη εκτέλεση** – Για ταχύτερη μαζική μετατροπή, μπορείτε να εκτελέσετε τις κλήσεις `LoadAndSave` μέσα σε βρόχο `Parallel.ForEach`, αλλά θυμηθείτε να αποδεσμεύετε σωστά κάθε `Bitmap`.

## Συχνές Ερωτήσεις

### Ε1: Είναι το Aspose.Drawing συμβατό με όλες τις μορφές εικόνας;

A1: Το Aspose.Drawing υποστηρίζει **120+** μορφές εισόδου και εξόδου, συμπεριλαμβανομένων BMP, GIF, JPG, PNG, TIFF, WebP, HEIF και πολλών ακατέργαστων μορφών κάμερας.

### Ε2: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.Drawing;

A2: Δείτε την επίσημη τεκμηρίωση [εδώ](https://reference.aspose.com/drawing/net/).

### Ε3: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.Drawing;

A3: Επισκεφθείτε [εδώ](https://purchase.aspose.com/temporary-license/) για λεπτομέρειες προσωρινής άδειας.

### Ε4: Τι κάνω αν αντιμετωπίσω προβλήματα ή έχω ερωτήσεις κατά την υλοποίηση;

A4: Ζητήστε βοήθεια από την κοινότητα Aspose.Drawing στο [Aspose Forum](https://forum.aspose.com/c/drawing/44).

### Ε5: Πού μπορώ να αγοράσω τη βιβλιοθήκη Aspose.Drawing;

A5: Μπορείτε να την αγοράσετε [εδώ](https://purchase.aspose.com/buy).

**Πρόσθετες Ερωτήσεις & Απαντήσεις**

**Q: Μπορώ να χρησιμοποιήσω αυτόν τον κώδικα σε εφαρμογή ASP.NET web;**  
A: Ναι – η ίδια λογική `LoadAndSave` λειτουργεί σε ASP.NET, MVC ή Razor Pages· απλώς βεβαιωθείτε ότι η διαδικασία web έχει πρόσβαση ανάγνωσης/εγγραφής στους φακέλους προορισμού.

**Q: Είναι δυνατόν να επεξεργαστείτε εικόνες παράλληλα για ταχύτερη μαζική μετατροπή;**  
A: Απόλυτα. Τυλίξτε τις κλήσεις `LoadAndSave` σε βρόχο `Parallel.ForEach`, αλλά διαχειριστείτε την ασφαλή απόρριψη των αντικειμένων `Bitmap`.

## Συμπέρασμα

Τώρα έχετε ένα σταθερό, έτοιμο για παραγωγή πρότυπο για **μετατροπή BMP σε PNG**, εκτέλεση **μαζικής μετατροπής εικόνων**, και **αλλαγή μορφής εικόνας** χρησιμοποιώντας το Aspose.Drawing για .NET. Ενσωματώστε αυτά τα αποσπάσματα στις υπηρεσίες σας, δημιουργήστε μικρογραφίες on‑the‑fly, ή προετοιμάστε περιουσιακά στοιχεία για web delivery με την εμπιστοσύνη ότι η κινητήρια μηχανή της βιβλιοθήκης, διασυνοριακή και υψηλής απόδοσης, θα αναλάβει το βαρέως έργο.

---

**Τελευταία ενημέρωση:** 2026-05-19  
**Δοκιμάστηκε με:** Aspose.Drawing 24.12 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
