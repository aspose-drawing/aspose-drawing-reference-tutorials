---
date: 2026-05-24
description: Μάθετε πώς να κλιμακώνετε εικόνες με το Aspose.Drawing για .NET. Αυτός
  ο οδηγός δείχνει βήμα‑βήμα πώς να αλλάξετε το μέγεθος bitmap C# χρησιμοποιώντας
  nearest neighbor interpolation και να αποθηκεύσετε scaled image files.
keywords:
- how to scale images
- nearest neighbor scaling
- change image size
- high performance scaling
- resize bitmap c#
linktitle: Κλιμάκωση εικόνων στο Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to scale images with Aspose.Drawing for .NET. This guide
    shows step‑by‑step how to resize bitmap C# using nearest neighbor interpolation
    and save scaled image files.
  headline: How to Scale Images with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to scale images with Aspose.Drawing for .NET. This guide
    shows step‑by‑step how to resize bitmap C# using nearest neighbor interpolation
    and save scaled image files.
  name: How to Scale Images with Aspose.Drawing for .NET
  steps:
  - name: 'Aspose.Drawing for .NET - Ensure that you have the Aspose.Drawing library
      installed in your project. You can download it [here](https://releases.aspose.com/drawing/net/).'
    text: 'Aspose.Drawing for .NET - Ensure that you have the Aspose.Drawing library
      installed in your project. You can download it [here](https://releases.aspose.com/drawing/net/).'
  - name: 'Development Environment - Set up a .NET development environment, such as
      Visual Studio.'
    text: 'Development Environment - Set up a .NET development environment, such as
      Visual Studio.'
  - name: 'Basic Understanding of C# - Familiarity with the C# programming language
      is essential for implementing the examples.'
    text: 'Basic Understanding of C# - Familiarity with the C# programming language
      is essential for implementing the examples.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing is fully compatible with ASP.NET, ASP.NET Core, WPF,
      WinForms, and console applications.
    question: Can I use Aspose.Drawing for .NET in both web and desktop applications?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for testing and evaluation purposes.
    question: Is a temporary license available for Aspose.Drawing?
  - answer: For any queries or assistance, visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).
    question: Where can I find additional support for Aspose.Drawing?
  - answer: Aspose.Drawing supports a wide range of formats, including JPEG, PNG,
      GIF, BMP, TIFF, WebP, and SVG. See the full list in the [documentation](https://reference.aspose.com/drawing/net/).
    question: Are there any limitations on the image formats supported by Aspose.Drawing?
  - answer: Yes, Aspose.Drawing provides `NearestNeighbor`, `Bilinear`, `Bicubic`,
      and `HighQualityBicubic` modes, allowing you to balance speed and quality.
    question: Can I apply custom interpolation modes for image scaling?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Πώς να κλιμακώσετε εικόνες με το Aspose.Drawing για .NET
url: /el/net/image-editing/scale/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να κλιμακώσετε εικόνες με το Aspose.Drawing για .NET

## Εισαγωγή

Σε αυτό το ολοκληρωμένο μάθημα θα ανακαλύψετε **πώς να κλιμακώσετε εικόνες** αποδοτικά χρησιμοποιώντας το Aspose.Drawing για .NET. Είτε δημιουργείτε μια υπηρεσία web που παράγει μικρογραφίες είτε ένα εργαλείο επιφάνειας εργασίας που μεγαλώνει πόρους pixel‑art, η κλιμάκωση εικόνας είναι μια βασική απαίτηση. Θα περάσουμε από κάθε βήμα — από τη δημιουργία καμβά μέχρι την εφαρμογή παρεμβολής nearest‑neighbor και τελικά την αποθήκευση του αποτελέσματος — ώστε να μπορείτε να υλοποιήσετε κλιμάκωση υψηλής απόδοσης σε λίγα λεπτά.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη πρέπει να χρησιμοποιήσω;** Aspose.Drawing for .NET  
- **Ποια παρεμβολή δίνει το πιο ευκρινές αποτέλεσμα;** NearestNeighbor interpolation  
- **Μπορώ να αλλάξω το μέγεθος της εικόνας σε C#;** Yes – use the `Bitmap` and `Graphics` classes  
- **Πώς αποθηκεύω μια κλιμακωμένη εικόνα;** Call `bitmap.Save(...)` with the desired path  
- **Απαιτείται άδεια;** A temporary license is available for evaluation  

## Τι είναι η κλιμάκωση εικόνας στο Aspose.Drawing;
Η κλιμάκωση εικόνας είναι η διαδικασία αλλαγής μεγέθους ενός bitmap σε μεγαλύτερες ή μικρότερες διαστάσεις διατηρώντας την οπτική ποιότητα. Το Aspose.Drawing παρέχει ένα απλό API που επιτρέπει στους προγραμματιστές C# να ελέγχουν κάθε βήμα — από τη δημιουργία του καμβά μέχρι τη σχεδίαση της πηγαίας εικόνας μέσα σε ένα ορθογώνιο προορισμού.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για κλιμάκωση;
Το Aspose.Drawing προσφέρει **υψηλής απόδοσης κλιμάκωση** για απαιτητικά φορτία: υποστηρίζει **30+ μορφές εικόνας** (συμπεριλαμβανομένων PNG, JPEG, BMP, TIFF και WebP) και μπορεί να επεξεργαστεί αρχεία έως **500 MB** χωρίς να φορτώνει ολόκληρη την εικόνα στη μνήμη. Η βιβλιοθήκη προσφέρει επίσης **τέσσερις τρόπους παρεμβολής**, με το **NearestNeighbor** να παρέχει pixel‑perfect αποτελέσματα ιδανικά για εικονίδια και γραφικά παιχνιδιών. Επειδή είναι ένα ενιαίο πακέτο NuGet, δεν υπάρχουν **εξωτερικές εξαρτήσεις native**, καθιστώντας την ανάπτυξη σε Linux containers ή Azure Functions απρόσκοπτη.

## Προαπαιτούμενα

Πριν ξεκινήσετε το μάθημα, βεβαιωθείτε ότι έχετε τα παρακάτω:

1. Aspose.Drawing για .NET: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.Drawing στο έργο σας. Μπορείτε να την κατεβάσετε [εδώ](https://releases.aspose.com/drawing/net/).  
2. Περιβάλλον Ανάπτυξης: Ρυθμίστε ένα περιβάλλον ανάπτυξης .NET, όπως το Visual Studio.  
3. Βασική Κατανόηση της C#: Η εξοικείωση με τη γλώσσα προγραμματισμού C# είναι απαραίτητη για την υλοποίηση των παραδειγμάτων.

## Εισαγωγή Ονομάτων Χώρων

Στο έργο C# σας, ξεκινήστε εισάγοντας τα απαραίτητα namespaces. Αυτό το βήμα είναι κρίσιμο για την απρόσκοπτη πρόσβαση στις λειτουργίες του Aspose.Drawing.

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Drawing2D;
```

## Βήμα 1: Δημιουργία Bitmap (καμβάς)

Η κλάση `Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη που μπορείτε να σχεδιάσετε ή να επεξεργαστείτε.  
Ξεκινήστε δημιουργώντας ένα αντικείμενο `Bitmap` που θα λειτουργήσει ως καμβάς για την εικόνα σας. Καθορίστε το πλάτος, το ύψος και τη μορφή pixel σύμφωνα με τις απαιτήσεις σας. Αυτή είναι η κλασική προσέγγιση *resize bitmap C#*.

```csharp
using System.Drawing;
```

## Βήμα 2: Δημιουργία αντικειμένου Graphics

Η κλάση `Graphics` παρέχει μεθόδους σχεδίασης για την απόδοση σχημάτων, κειμένου και εικόνων σε ένα bitmap.  
Στη συνέχεια, δημιουργήστε ένα αντικείμενο `Graphics` από το προηγουμένως δημιουργημένο `Bitmap`. Αυτό το αντικείμενο παρέχει τις δυνατότητες σχεδίασης που απαιτούνται για την επεξεργασία εικόνας, συμπεριλαμβανομένης της δυνατότητας **drawimage with rectangle** αργότερα.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Βήμα 3: Ορισμός Κατάστασης Παρεμβολής

`InterpolationMode` καθορίζει πώς υπολογίζονται οι τιμές pixel όταν μια εικόνα αλλάζει μέγεθος.  
Για να βελτιώσετε την ποιότητα της κλιμακωμένης εικόνας, ορίστε τη κατάσταση παρεμβολής. Σε αυτό το παράδειγμα, χρησιμοποιούμε τη λειτουργία **NearestNeighbor**, η οποία είναι ιδανική όταν χρειάζεστε μια καθαρή, pixel‑art κλιμάκωση.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Βήμα 4: Φόρτωση της Εικόνας

Η μέθοδος `Image.FromFile` φορτώνει ένα υπάρχον αρχείο εικόνας στη μνήμη ως `Bitmap`.  
Φορτώστε την εικόνα που θέλετε να κλιμακώσετε σε ένα αντικείμενο `Bitmap`. Αντικαταστήστε `"Your Document Directory" + @"Images\aspose_logo.png"` με τη διαδρομή της εικόνας σας.

```csharp
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

## Βήμα 5: Κλιμάκωση της Εικόνας

Ένα `Rectangle` ορίζει την περιοχή προορισμού όπου θα σχεδιαστεί η πηγαία εικόνα.  
Ορίστε ένα ορθογώνιο που αντιπροσωπεύει την επέκταση της εικόνας. Σε αυτό το παράδειγμα, η εικόνα κλιμακώνεται 5 ×  τόσο σε πλάτος όσο και σε ύψος, δείχνοντας την τεχνική **drawimage with rectangle**.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

## Βήμα 6: Αποθήκευση της Κλιμακωμένης Εικόνας

`Bitmap.Save` αποθηκεύει το bitmap στη μνήμη σε ένα αρχείο με μορφή που προκύπτει από την επέκταση του αρχείου.  
Αποθηκεύστε την κλιμακωμένη εικόνα στην επιθυμητή θέση. Προσαρμόστε τη διαδρομή αρχείου σύμφωνα με τη δομή του έργου σας. Αυτό το βήμα δείχνει πώς να **αποθηκεύσετε κλιμακωμένες εικόνες** σε κοινές μορφές όπως PNG.

```csharp
Rectangle expansionRectangle = new Rectangle(0, 0, image.Width * 5, image.Height * 5);
graphics.DrawImage(image, expansionRectangle);
```

Συγχαρητήρια! Έχετε μάθει με επιτυχία **πώς να κλιμακώσετε εικόνες** χρησιμοποιώντας το Aspose.Drawing για .NET.

## Κοινά Προβλήματα και Λύσεις

- **Η εικόνα εμφανίζεται θολή μετά την κλιμάκωση** – Βεβαιωθείτε ότι χρησιμοποιείτε `InterpolationMode.NearestNeighbor` για pixel‑perfect αποτελέσματα· αλλάξτε σε `Bilinear` ή `HighQualityBicubic` για πιο ομαλή κλιμάκωση φωτογραφιών.  
- **Εξαιρέσεις έλλειψης μνήμης σε μεγάλα αρχεία** – Το Aspose.Drawing επεξεργάζεται εικόνες σε πλακίδια· αυξήστε την ιδιότητα `MemoryLimit` εάν χρειάζεται να διαχειριστείτε αρχεία μεγαλύτερα από 500 MB.  
- **Λανθασμένη αναλογία διαστάσεων** – Χρησιμοποιήστε τον ίδιο συντελεστή κλιμάκωσης για πλάτος και ύψος, ή υπολογίστε το ορθογώνιο βάσει της αρχικής αναλογίας για να αποφύγετε παραμόρφωση.

## Συχνές Ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.Drawing για .NET τόσο σε web όσο και σε desktop εφαρμογές;**  
A: Ναι, το Aspose.Drawing είναι πλήρως συμβατό με ASP.NET, ASP.NET Core, WPF, WinForms και εφαρμογές κονσόλας.

**Q: Διατίθεται προσωρινή άδεια για το Aspose.Drawing;**  
A: Ναι, μπορείτε να αποκτήσετε μια προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/) για δοκιμή και αξιολόγηση.

**Q: Πού μπορώ να βρω επιπλέον υποστήριξη για το Aspose.Drawing;**  
A: Για οποιεσδήποτε ερωτήσεις ή βοήθεια, επισκεφθείτε το [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).

**Q: Υπάρχουν περιορισμοί στις μορφές εικόνας που υποστηρίζει το Aspose.Drawing;**  
A: Το Aspose.Drawing υποστηρίζει ένα ευρύ φάσμα μορφών, συμπεριλαμβανομένων JPEG, PNG, GIF, BMP, TIFF, WebP και SVG. Δείτε τη πλήρη λίστα στην [documentation](https://reference.aspose.com/drawing/net/).

**Q: Μπορώ να εφαρμόσω προσαρμοσμένες λειτουργίες παρεμβολής για κλιμάκωση εικόνας;**  
A: Ναι, το Aspose.Drawing παρέχει λειτουργίες `NearestNeighbor`, `Bilinear`, `Bicubic` και `HighQualityBicubic`, επιτρέποντάς σας να ισορροπήσετε την ταχύτητα και την ποιότητα.

## Συμπέρασμα

Σε αυτό το μάθημα εξερευνήσαμε τη διαδικασία από άκρη σε άκρη για **πώς να κλιμακώσετε εικόνες** χρησιμοποιώντας το Aspose.Drawing. Τώρα ξέρετε πώς να δημιουργήσετε έναν bitmap καμβά, να διαμορφώσετε ένα αντικείμενο graphics, να επιλέξετε την βέλτιστη κατάσταση παρεμβολής, να φορτώσετε μια πηγαία εικόνα, να τη σχεδιάσετε σε ένα κλιμακωμένο ορθογώνιο και τέλος να αποθηκεύσετε το αποτέλεσμα. Εκμεταλλευόμενοι την **υψηλής απόδοσης κλιμάκωση** και την **υποστήριξη 30+ μορφών** του Aspose.Drawing, μπορείτε να δημιουργήσετε αξιόπιστες γραμμές επεξεργασίας εικόνας που λειτουργούν αποδοτικά σε οποιαδήποτε πλατφόρμα .NET.

Μη διστάσετε να πειραματιστείτε με διαφορετικές λειτουργίες παρεμβολής, να επεξεργαστείτε μαζικά πολλά αρχεία σε βρόχο ή να συνδυάσετε την κλιμάκωση με άλλες δυνατότητες του Aspose.Drawing όπως υδατογράφημα ή μετατροπή χρωματικού χώρου.

---

**Τελευταία Ενημέρωση:** 2026-05-24  
**Δοκιμή Με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Scale_out.png");
```


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
