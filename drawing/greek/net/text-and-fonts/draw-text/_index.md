---
date: 2026-09-23
description: Μάθετε πώς να σχεδιάζετε κείμενο σε εικόνα χρησιμοποιώντας το Aspose.Drawing
  για .NET. Δημιουργήστε εικόνα με κείμενο, προσθέστε κείμενο σε bitmap και αποθηκεύστε
  το bitmap ως PNG με προσαρμοσμένες γραμματοσειρές.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Πώς να σχεδιάσετε κείμενο με Aspose.Drawing
og_description: Μάθετε πώς να σχεδιάζετε κείμενο σε εικόνα χρησιμοποιώντας το Aspose.Drawing
  για .NET. Αυτό το tutorial σας δείχνει πώς να δημιουργήσετε εικόνα με κείμενο, να
  προσθέσετε κείμενο σε bitmap και να αποθηκεύσετε το bitmap ως PNG με προσαρμοσμένες
  γραμματοσειρές.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Σχεδίαση κειμένου σε εικόνα με Aspose.Drawing για .NET – Σύντομος οδηγός
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Πώς να σχεδιάσετε κείμενο σε εικόνα με Aspose.Drawing για .NET
url: /el/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να σχεδιάσετε κείμενο σε εικόνα με Aspose.Drawing για .NET

## Εισαγωγή

Σε αυτόν τον οδηγό βήμα‑βήμα θα μάθετε **πώς να σχεδιάζετε κείμενο σε εικόνα** χρησιμοποιώντας το Aspose.Drawing για .NET. Είτε χρειάζεστε να δημιουργήσετε μια *δυναμική εικόνα κειμένου*, να προσθέσετε κείμενο σε ένα υπάρχον bitmap, είτε να δημιουργήσετε ένα γραφικό με προσαρμοσμένες γραμματοσειρές, αυτό το μάθημα σας οδηγεί σε κάθε λεπτομέρεια ώστε να μπορείτε να ξεκινήσετε τη σχεδίαση κειμένου σε λίγα λεπτά. Η βιβλιοθήκη υποστηρίζει πάνω από 30 μεθόδους GDI+, λειτουργεί σε Windows, Linux και macOS, και έχει **μηδενικές εξωτερικές εξαρτήσεις**, καθιστώντας την αξιόπιστη επιλογή για δημιουργία εικόνων από τον διακομιστή.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη χρησιμοποιείται;** Aspose.Drawing for .NET  
- **Κύρια εργασία;** Σχεδίαση κειμένου σε εικόνα (δημιουργία εικόνας με κείμενο)  
- **Κύρια μέθοδος;** `Graphics.DrawString` (σχεδίαση συμβολοσειράς σε εικόνα)  
- **Μορφή εξόδου;** PNG (αποθήκευση bitmap ως PNG)  
- **Προαπαιτούμενα;** Περιβάλλον ανάπτυξης .NET και βιβλιοθήκη Aspose.Drawing  

## Τι σημαίνει η σχεδίαση κειμένου με Aspose.Drawing;

Η σχεδίαση κειμένου με το Aspose.Drawing σημαίνει χρήση του API συμβατού με GDI+ της βιβλιοθήκης για την απόδοση Unicode συμβολοσειρών σε ένα raster καμβά. Η μέθοδος `Graphics.DrawString` γράφει το κείμενο σε ένα bitmap, επιτρέποντάς σας να ελέγχετε τη γραμματοσειρά, το χρώμα, την ευθυγράμμιση και το anti‑aliasing. Αυτή η προσέγγιση σας επιτρέπει να δημιουργείτε εικόνες υψηλής ποιότητας χωρίς την εγκατάσταση του System.Drawing.Common.

## Γιατί να χρησιμοποιήσετε Aspose.Drawing για την προσθήκη κειμένου σε εικόνες;

Το Aspose.Drawing προσφέρει έναν αξιόπιστο, cross‑platform τρόπο απόδοσης κειμένου σε εικόνες χωρίς την ανάγκη εγγενών βιβλιοθηκών GDI+, παρέχοντας συνεπή ποιότητα και απόδοση σε οποιοδήποτε λειτουργικό σύστημα. Υποστηρίζει προηγμένο anti‑aliasing, χαρακτήρες Unicode και προσαρμοσμένες γραμματοσειρές, και ενσωματώνεται άψογα με εφαρμογές .NET, καθιστώντας το ιδανικό για δημιουργία εικόνων από τον διακομιστή και εργαλεία επιφάνειας εργασίας.

- **Cross‑platform reliability** – λειτουργεί σε Windows, Linux και macOS.  
- **Advanced rendering** – anti‑aliasing και εξομάλυνση κειμένου sub‑pixel για καθαρό αποτέλεσμα.  
- **No external dependencies** – η βιβλιοθήκη περιλαμβάνει όλα όσα χρειάζεστε για *create image with text*.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Aspose.Drawing for .NET** – κατεβάστε το από την [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/).  
- **Ένα .NET IDE** όπως το Visual Studio ή το VS Code.  

## Εισαγωγή ονομάτων χώρων

Ξεκινήστε εισάγοντας τα απαιτούμενα ονόματα χώρων:

Αυτά τα ονόματα χώρων παρέχουν τους βασικούς τύπους GDI+ όπως `Bitmap`, `Graphics` και εργαλεία απόδοσης κειμένου.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Βήμα 1: δημιουργία αντικειμένων bitmap και graphics

`Bitmap` είναι ο κοντέινερ raster εικόνας του Aspose.Drawing για δεδομένα pixel, και το `Graphics` παρέχει μεθόδους σχεδίασης για την απόδοση σχημάτων και κειμένου πάνω του.  

`Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη, ενώ το `Graphics` παρέχει μεθόδους σχεδίασης για την απόδοση πάνω σε αυτό το bitmap.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Εδώ δημιουργούμε ένα `Bitmap` που θα κρατήσει την τελική εικόνα και ένα `Graphics` αντικείμενο που μας επιτρέπει να σχεδιάζουμε πάνω του. Η υπόδειξη anti‑aliasing εξασφαλίζει ότι το κείμενο φαίνεται ομαλό.

## Βήμα 2: ρύθμιση brush, pen και font

`Brush` ορίζει το χρώμα γεμίσματος, `Pen` περιγράμματα σχημάτων, και `Font` καθορίζει τη γραμματοσειρά, το μέγεθος και το στυλ για την απόδοση κειμένου.  

`Brush` γεμίζει σχήματα με χρώμα, `Pen` περιγράμματα σχημάτων, και `Font` ορίζει τη γραμματοσειρά και το μέγεθος για την απόδοση κειμένου.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** ορίζει το χρώμα του κειμένου.  
- **Pen** χρησιμοποιείται αργότερα για να σχεδιάσει ένα rectangle γύρω από το κείμενο (προαιρετικό).  
- **Font** καθορίζει τη γραμματοσειρά, το μέγεθος και το στυλ για τη λειτουργία *draw string on image*.

## Βήμα 3: ορισμός κειμένου και rectangle

`Rectangle` ορίζει το πλαίσιο περιορισμού όπου θα τοποθετηθεί το κείμενο, καθορίζοντας τις συντεταγμένες X/Y και το πλάτος/ύψος.  

`Rectangle` καθορίζει τη θέση και το μέγεθος μιας ορθογώνιας περιοχής, που χρησιμοποιείται εδώ για να περιορίσει το σχεδιασμένο κείμενο.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

Το `Rectangle` καθορίζει πού θα τοποθετηθεί το κείμενο. Προσαρμόστε τις συντεταγμένες και το μέγεθος ώστε να ταιριάζουν με τη διάταξή σας.

## Βήμα 4: σχεδίαση rectangle και κειμένου

`Graphics.DrawString` αποδίδει το καθορισμένο κείμενο μέσα στο δοσμένο rectangle χρησιμοποιώντας τη δοθείσα γραμματοσειρά και brush.  

`Graphics.DrawString` αποδίδει μια συμβολοσειρά κειμένου μέσα σε ένα καθορισμένο rectangle χρησιμοποιώντας τη δοθείσα γραμματοσειρά και brush.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Αρχικά περιγράμμουμε την περιοχή με ένα μπλε rectangle, στη συνέχεια **προσθέτουμε κείμενο στο bitmap** καλώντας το `DrawString`. Αυτό είναι ο πυρήνας του *drawing text* στην εικόνα.

## Βήμα 5: αποθήκευση του αποτελέσματος

Η εικόνα αποθηκεύεται ως αρχείο PNG, καλύπτοντας την απαίτηση *save bitmap as PNG*. Αντικαταστήστε τη διαδρομή placeholder με το πραγματικό φάκελο όπου θέλετε να αποθηκευτεί το αρχείο.  

`bitmap.Save` γράφει την εικόνα σε ένα αρχείο στην επιλεγμένη μορφή, όπως PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Συνηθισμένες περιπτώσεις χρήσης

- **Δημιουργία πιστοποιητικών** με εξατομικευμένα ονόματα.  
- **Δημιουργία μικρογραφιών με υδατογράφημα** για γκαλερί ιστού.  
- **Κατασκευή δυναμικών γραφημάτων** που περιλαμβάνουν ετικέτες ή σημειώσεις.  

## Επίλυση προβλημάτων & συμβουλές

- **Font not found;** Βεβαιωθείτε ότι η γραμματοσειρά είναι εγκατεστημένη στον υπολογιστή ή χρησιμοποιήστε μια ιδιωτική συλλογή γραμματοσειρών.  
- **Text clipped;** Αυξήστε το μέγεθος του rectangle ή μειώστε το μέγεθος της γραμματοσειράς.  
- **Performance concerns;** Επαναχρησιμοποιήστε το ίδιο αντικείμενο `Graphics` για πολλαπλές λειτουργίες σχεδίασης όταν είναι δυνατόν.  

## Συχνές ερωτήσεις

**Q: Πώς αλλάζω τη μορφή εξόδου σε JPEG;**  
A: Αντικαταστήστε την επέκταση `.png` με `.jpg` στη μέθοδο `Save` και προαιρετικά καθορίστε ένα `ImageCodecInfo` για την ποιότητα JPEG.

**Q: Μπορώ να σχεδιάσω κείμενο πολλαπλών γραμμών;**  
A: Ναι, συμπεριλάβετε χαρακτήρες αλλαγής γραμμής (`\n`) στη συμβολοσειρά ή χρησιμοποιήστε `StringFormat` με `FormatFlags.LineLimit`.

**Q: Υπάρχει τρόπος να μετρήσω το μέγεθος του κειμένου πριν το σχεδιάσω;**  
A: Χρησιμοποιήστε `Graphics.MeasureString` για να λάβετε τις ακριβείς διαστάσεις του αποδοθέντος κειμένου.

**Q: Υποστηρίζει το Aspose.Drawing χαρακτήρες Unicode;**  
A: Απόλυτα. Παρέχετε μια γραμματοσειρά που περιέχει τα απαιτούμενα γλύφους και η βιβλιοθήκη θα τους αποδώσει σωστά.

**Q: Ποια έκδοση του Aspose.Drawing χρησιμοποιήθηκε για τις δοκιμές;**  
A: Τα παραδείγματα δοκιμάστηκαν με το Aspose.Drawing 24.11 για .NET.

---

**Τελευταία ενημέρωση:** 2026-09-23  
**Δοκιμάστηκε με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Δημιουργία Bitmap Graphics C# – Αποθήκευση PNG εικόνας και εργασία με εγκατεστημένες γραμματοσειρές στο Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Πώς να αποθηκεύσετε ένα bitmap ως PNG χρησιμοποιώντας το Aspose.Drawing API για .NET](/drawing/net/image-editing/display/)
- [Κείμενο σε εικόνα](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}