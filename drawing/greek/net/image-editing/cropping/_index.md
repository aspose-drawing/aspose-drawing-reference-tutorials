---
date: 2026-10-13
description: Μάθετε πώς να κόψετε μαζικά εικόνες σε PNG χρησιμοποιώντας το Aspose.Drawing
  API, την εναλλακτική λύση cross‑platform του System.Drawing για προγραμματιστές
  .NET.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: Εκπαιδευτικό οδηγό περικοπής εικόνων – Aspose.Drawing
og_description: Μάθετε πώς να κόψετε μαζικά εικόνες σε PNG γρήγορα χρησιμοποιώντας
  το Aspose.Drawing, την εναλλακτική λύση cross‑platform του System.Drawing για προγραμματιστές
  .NET. Ακολουθήστε βήμα‑βήμα οδηγίες για την αποδοτική επεξεργασία πολλαπλών αρχείων.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Πώς να κόψετε μαζικά εικόνες σε PNG με το Aspose.Drawing για .NET
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Πώς να κόψετε μαζικά εικόνες σε PNG χρησιμοποιώντας το Aspose.Drawing για .NET
url: /el/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να κόψετε μαζικά εικόνες σε PNG χρησιμοποιώντας το Aspose.Drawing για .NET

Αν χρειάζεστε να **κοψετε εικόνα σε PNG** γρήγορα, αξιόπιστα και σε κλίμακα σε περιβάλλον .NET, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα περάσουμε βήμα προς βήμα τις ακριβείς διαδικασίες για να φορτώσετε μια εικόνα, να ορίσετε την περιοχή κοπής και να αποθηκεύσετε το αποτέλεσμα ως αρχείο PNG — χρησιμοποιώντας το Aspose.Drawing, μια σύγχρονη **εναλλακτική του System.Drawing** που λειτουργεί δια‑πλατφόρμα. Θα δείτε επίσης πώς να επεκτείνετε τη ροή μιας μόνο εικόνας σε μια πλήρη **μαζική περικοπή** pipeline.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη πρέπει να χρησιμοποιήσω;** Aspose.Drawing for .NET (μια πλήρης εναλλακτική του System.Drawing.Common)  
- **Πόσο χρόνο διαρκεί η βασική περικοπή;** Συνήθως κάτω από ένα δευτερόλεπτο για μια μοναδική εικόνα σε σύγχρονο CPU  
- **Μπορώ να κόψω σε PNG;** Ναι – αποθηκεύστε το περικομμένο bitmap ως αρχείο PNG (δείτε το Βήμα 6)  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή  
- **Είναι δυνατή η μαζική επεξεργασία;** Απόλυτα – τυλίξτε τα ίδια βήματα σε βρόχο για να επεξεργαστείτε πολλά αρχεία σε δευτερόλεπτα  

## Πώς να κόψετε μαζικά εικόνες σε PNG;

Φορτώστε κάθε αρχείο πηγής με `new Bitmap(path)`, δημιουργήστε ένα αντίστοιχο κενό `Bitmap` για την περιοχή κοπής, σχεδιάστε το επιλεγμένο ορθογώνιο χρησιμοποιώντας `Graphics.DrawImage` και τέλος καλέστε `Save("output.png", ImageFormat.Png)`. Τυλίξτε αυτές τις έξι γραμμές μέσα σε έναν βρόχο `foreach` που διατρέχει έναν φάκελο και θα έχετε μια πλήρη λύση μαζικής περικοπής που επεξεργάζεται δεκάδες εικόνες σε δευτερόλεπτα.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για μαζική περικοπή;

Το Aspose.Drawing λειτουργεί σε **Windows, Linux και macOS**, επεξεργάζεται **εικόνες άνω των 500 pixel σε κάτω από 0,5 δευτερόλεπτα** σε τυπική CPU server‑class και υποστηρίζει **πάνω από 50 μορφές εικόνας** με πλήρη διατήρηση του καναλιού άλφα. Επειδή εξαλείφει τις εξαρτήσεις του native GDI+, μπορείτε να αναπτύξετε τον ίδιο κώδικα σε containers, Azure App Service ή AWS Lambda χωρίς πρόσθετες βιβλιοθήκες, καθιστώντας το ιδανικό για μεγάλες pipelines εικόνων.

## Τι είναι η “crop image to PNG”; 

Η λειτουργία `crop image to PNG` εξάγει μια ορθογώνια περιοχή από ένα bitmap πηγής και γράφει αυτήν την περιοχή σε αρχείο PNG. Το PNG διατηρεί οποιοδήποτε κανάλι άλφα, παρέχοντας ασυμπίεστη συμπίεση, κάτι που κάνει την προκύπτουσα εικόνα ιδανική για μικρογραφίες, εικονίδια, στοιχεία UI ή οποιαδήποτε κατάσταση όπου απαιτούνται ποιότητα και διαφάνεια.

## Γιατί το Aspose.Drawing είναι εναλλακτική του System.Drawing; 

Το Aspose.Drawing λειτουργεί ως αντικατάσταση του System.Drawing προσφέροντας πλήρη δια‑πλατφορμική συμβατότητα, εξαλείφοντας την ανάγκη για native βιβλιοθήκες GDI+. Υποστηρίζει μια ευρεία γκάμα μορφών pixel, παρέχει υψηλής απόδοσης επεξεργασία εικόνας και περιλαμβάνει προχωρημένα χαρακτηριστικά όπως διαχείριση καναλιού άλφα και εκτεταμένη υποστήριξη μορφών, καθιστώντας το κατάλληλο τόσο για απλές επεξεργασίες όσο και για μαζική επεξεργασία μεγάλης κλίμακας.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε:

- **Βιβλιοθήκη Aspose.Drawing** ενσωματωμένη στο .NET project σας. Μπορείτε να τη κατεβάσετε από τη [Aspose.Drawing download page](https://releases.aspose.com/drawing/net/).  
- Έναν φάκελο που περιέχει τις εικόνες πηγής που θέλετε να κόψετε. Αντικαταστήστε το `"Your Document Directory"` στα αποσπάσματα κώδικα με την πραγματική διαδρομή στο μηχάνημά σας.

## Εισαγωγή ονομάτων χώρου

Το namespace `System.Drawing` μας δίνει πρόσβαση στα `Bitmap`, `Graphics` και σχετικούς τύπους που επεκτείνει το Aspose.Drawing.

```csharp
using System.Drawing;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Δημιουργία καμβά bitmap

`Bitmap` είναι η αναπαράσταση σε μνήμη του Aspose.Drawing για μια εικόνα, παρέχοντας πρόσβαση σε επίπεδο pixel και έλεγχο μορφής.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Ξεκινάμε με έναν κενό καμβά με μέγεθος ώστε να χωρέσει το περικομμένο αποτέλεσμα. Προσαρμόστε το πλάτος και το ύψος ώστε να ταιριάζουν με τις διαστάσεις της περιοχής που σκοπεύετε να εξάγετε.

### Βήμα 2: Δημιουργία αντικειμένου graphics

`Graphics` είναι η επιφάνεια σχεδίασης που σας επιτρέπει να αποδίδετε σχήματα, κείμενο ή άλλες εικόνες πάνω σε ένα Bitmap.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Ένα αντικείμενο `Graphics` μας επιτρέπει να σχεδιάζουμε πάνω στον καμβά. Το `InterpolationMode` ελέγχει πώς υπολογίζονται οι τιμές pixel κατά τη κλιμάκωση ή μετασχηματισμό — το `NearestNeighbor` λειτουργεί καλά για έντονα άκρα.

### Βήμα 3: Φόρτωση της εικόνας προς περικοπή

`Image` (ή `Bitmap`) φορτώνει το αρχείο πηγής στη μνήμη, έτοιμο για επεξεργασία.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Φορτώστε την εικόνα πηγής. Βεβαιωθείτε ότι η διαδρομή δείχνει σε υπάρχον αρχείο· διαφορετικά θα ριχτεί εξαίρεση.

### Βήμα 4: Ορισμός ορθογωνίων πηγής και προορισμού

Τα αντικείμενα `Rectangle` περιγράφουν την περιοχή της εικόνας πηγής που θα διατηρηθεί και πού θα τοποθετηθεί στον καμβά προορισμού.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

Το `sourceRectangle` λέει στο API ποιο μέρος της αρχικής εικόνας να διατηρήσει. Εδώ επιλέγουμε την περιοχή 50 × 40 pixel στην επάνω‑αριστερή γωνία. Αναθέτοντας το ίδιο ορθογώνιο στο `destinationRectangle`, διατηρούμε την περικομμένη περιοχή στο αρχικό της μέγεθος.

### Βήμα 5: Εκτέλεση της λειτουργίας περικοπής

`Graphics.DrawImage` αντιγράφει το καθορισμένο τμήμα του `image` στο κενό `bitmap` μας.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

Αυτή είναι η βασική λειτουργία **crop image to PNG**. Η μέθοδος σέβεται το ορθογώνιο πηγής και γράφει μόνο τα επιλεγμένα pixel στο bitmap προορισμού.

### Βήμα 6: Αποθήκευση της περικομμένης εικόνας (crop image to PNG)

`Bitmap.Save` γράφει το bitmap στη μνήμη σε αρχείο χρησιμοποιώντας τη συγκεκριμένη μορφή.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Τέλος, γράψτε τον καμβά στο δίσκο ως αρχείο PNG. Το PNG διατηρεί οποιοδήποτε κανάλι άλφα και παρέχει ασυμπίεστη ποιότητα — ιδανικό για στοιχεία UI.

## Πώς να κόψετε μαζικά εικόνες σε βρόχο;

Επανάληψη σε κάθε διαδρομή αρχείου με `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, επαναλάβετε τα Βήματα 1‑6 μέσα στον βρόχο και αποθηκεύστε κάθε αποτέλεσμα σε φάκελο προορισμού. Αυτό το μοτίβο κλιμακώνεται γραμμικά, μπορεί να παραλληλοποιηθεί με `Parallel.ForEach` για ακόμη πιο γρήγορη απόδοση, και επεξεργάζεται εικόνες αποδοτικά και γρήγορα.

## Συνηθισμένα προβλήματα & συμβουλές

- **Ασυμφωνίες μορφής pixel** – βεβαιωθείτε ότι η εικόνα πηγής και το bitmap του καμβά μοιράζονται συμβατή μορφή pixel για να αποφύγετε μεταβολές χρώματος.  
- **Απόρριψη αντικειμένων GDI** – τυλίξτε τα `Bitmap` και `Graphics` σε δηλώσεις `using` ή καλέστε το `Dispose()` χειροκίνητα· διαφορετικά μπορεί να διαρρεύσουν μη διαχειριζόμενοι πόροι.  
- **Σφάλματα συντεταγμένων** – οι συντεταγμένες του ορθογωνίου είναι μηδενικής βάσης. Η επιλογή ορθογωνίου που υπερβαίνει τα όρια της εικόνας πηγής θα προκαλέσει εξαίρεση.  

## Συχνές ερωτήσεις

**Q: Μπορώ να κόψω εικόνες οποιασδήποτε μορφής χρησιμοποιώντας το Aspose.Drawing;**  
A: Ναι, το Aspose.Drawing υποστηρίζει μια ευρεία γκάμα μορφών (PNG, JPEG, BMP, GIF, TIFF κ.λπ.), ώστε να μπορείτε να κόψετε πρακτικά οποιοδήποτε τύπο εικόνας.

**Q: Υπάρχουν προχωρημένες επιλογές περικοπής διαθέσιμες;**  
A: Απόλυτα. Μπορείτε να συνδυάσετε `GraphicsPath`, μετασχηματισμούς `Matrix`, ή να χρησιμοποιήσετε την κλάση `ImageProcessor` για πιο σύνθετες επιλογές όπως κυκλικές περικοπές.

**Q: Μπορώ να εφαρμόσω πολλαπλές λειτουργίες περικοπής σε μία εικόνα;**  
A: Ναι. Μετά την πρώτη περικοπή, μπορείτε να επαναχρησιμοποιήσετε το προκύπτον bitmap ως νέα πηγή και να επαναλάβετε τη διαδικασία για να αλυσίδετε πολλαπλές περικοπές.

**Q: Είναι το Aspose.Drawing κατάλληλο για μαζική επεξεργασία εικόνων;**  
A: Σίγουρα. Το ελαφρύ API του και η έλλειψη εγγενών εξαρτήσεων το καθιστούν ιδανικό για επεξεργασία μεγάλων συλλογών εικόνων σε διακομιστές.

**Q: Πώς μπορώ να λάβω υποστήριξη για ερωτήματα σχετικά με το Aspose.Drawing;**  
A: Μεταβείτε στο [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) για να ζητήσετε βοήθεια και να συνδεθείτε με την κοινότητα.

---

**Τελευταία ενημέρωση:** 2026-10-13  
**Δοκιμάστηκε με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Φόρτωση, Μετατροπή BMP σε PNG και Άλλες Μορφές με Aspose.Drawing](/drawing/net/image-editing/load-save/)
- [Πώς να Αδειοδοτήσετε το Aspose.Drawing για .NET – πώς να αδειοδοτήσετε το aspose.drawing](/drawing/net/licensing/)
- [Πώς να Σχεδιάσετε Ορθογώνιο – Μετασχηματισμός Συστήματος Συντεταγμένων (Μετασχηματισμός Σελίδας) χρησιμοποιώντας το Aspose.Drawing API για .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}