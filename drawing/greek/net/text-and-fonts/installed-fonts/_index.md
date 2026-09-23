---
date: 2026-09-23
description: Μάθετε πώς να αποθηκεύσετε εικόνα PNG σε C# χρησιμοποιώντας Aspose.Drawing,
  να εμφανίσετε τη λίστα των installed fonts, να σχεδιάσετε κείμενο με custom fonts,
  και να προσαρμόσετε την bitmap resolution για high‑quality graphics.
keywords:
- save png image c#
- installed fonts aspnet
- aspose.drawing bitmap graphics
- c# font collection
- png export .net
lastmod: 2026-09-23
linktitle: Αποθήκευση εικόνας PNG σε C# με Aspose.Drawing και installed fonts
og_description: Αποθήκευση εικόνας PNG σε C# χρησιμοποιώντας Aspose.Drawing. Αυτός
  ο οδηγός δείχνει πώς να εμφανίσετε τη λίστα των installed fonts, να σχεδιάσετε κείμενο,
  και να ελέγξετε την bitmap resolution για professional graphics.
og_image_alt: Developer guide showing C# code that creates a bitmap, lists system
  fonts, and saves a PNG file with Aspose.Drawing
og_title: Αποθήκευση εικόνας PNG σε C# με Aspose.Drawing και installed fonts
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  headline: Save PNG image in C# with Aspose.Drawing and installed fonts
  type: TechArticle
- description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  name: Save PNG image in C# with Aspose.Drawing and installed fonts
  steps:
  - name: Create a bitmap (the canvas)
    text: '`Bitmap` is the raster image object that holds pixel data for the canvas.'
  - name: Create graphics from bitmap
    text: '`Graphics` is the object that supplies drawing functions such as drawing
      shapes and text onto a bitmap.'
  - name: Set up brush and font (draw text with fonts)
    text: '`Brush` defines how shapes and text are filled with colour, while `Font`
      specifies the typeface, size, and style for text rendering.'
  - name: List installed fonts and show font families
    text: '`InstalledFontCollection` provides access to all font families installed
      on the host system.'
  - name: Save PNG image
    text: '`bitmap.Save` writes the bitmap to a file in the chosen image format, such
      as PNG. > **Pro tip:** Use `Path.Combine` for building file paths to avoid issues
      with directory separators on different operating systems.'
  type: HowTo
- questions:
  - answer: Yes. Load the font file into a `PrivateFontCollection` and create a `Font`
      from that collection, then draw it the same way as system fonts.
    question: Can I use custom fonts that are not installed on the machine?
  - answer: Wrap font creation in a `try/catch` block and inspect `ArgumentException`
      for missing families; provide a fallback font such as `Arial`.
    question: How do I handle font‑related exceptions?
  - answer: Absolutely. The library works in ASP.NET Core, Azure Functions, and other
      server‑side .NET environments without needing GDI+.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify
      the `FontStyle` enum to apply bold, italic, or underline.
    question: Can I change the text colour or style?
  - answer: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – bitmap graphics and font handling
tags:
- save png
- aspose.drawing
- c# graphics
- installed fonts
- bitmap
title: Αποθήκευση εικόνας PNG σε C# με Aspose.Drawing και installed fonts
url: /el/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση εικόνας PNG σε C# με Aspose.Drawing και εγκατεστημένες γραμματοσειρές

## Εισαγωγή

Αν χρειάζεστε **αποθήκευση εικόνας PNG σε C#** ενώ επίσης **δημιουργία bitmap γραφικών**, το Aspose.Drawing για .NET σας παρέχει έναν καθαρό, δια‑πλατφορμικό τρόπο για να το κάνετε. Σε αυτό το tutorial θα περάσουμε από την καταγραφή των εγκατεστημένων γραμματοσειρών, την εμφάνιση των οικογενειών γραμματοσειρών, τη δημιουργία γραφικών από ένα bitmap και τη σχεδίαση κειμένου με γραμματοσειρές — όλα ενώ τελικά αποθηκεύουμε το αποτέλεσμα ως εικόνα PNG. Στο τέλος θα έχετε ένα επαναχρησιμοποιήσιμο κομμάτι κώδικα που μπορείτε να ενσωματώσετε σε οποιοδήποτε .NET project, είτε τρέχει σε Windows, Linux ή macOS.

## Γρήγορες απαντήσεις
- **Τι δημιουργεί αυτό το tutorial;** Μια εικόνα PNG που καταγράφει τις εγκατεστημένες οικογένειες γραμματοσειρών στο μηχάνημα φιλοξενίας.  
- **Ποια βιβλιοθήκη απαιτείται;** Aspose.Drawing για .NET (χωρίς εξάρτηση από System.Drawing.Common).  
- **Μπορώ να χρησιμοποιήσω προσαρμοσμένες γραμματοσειρές;** Ναι – φορτώστε τις σε ένα `InstalledFontCollection` ή `PrivateFontCollection`.  
- **Μπορεί η ανάλυση εξόδου να ρυθμιστεί;** Απόλυτα – αλλάξτε το μέγεθος του bitmap ή τη μορφή pixel για να ελέγξετε την ανάλυση.  
- **Χρειάζομαι άδεια για να τρέξω τον κώδικα;** Μια προσωρινή άδεια λειτουργεί για αξιολόγηση· απαιτείται πλήρης άδεια για παραγωγή.

## Τι σημαίνει “αποθήκευση εικόνας PNG” στο πλαίσιο του Aspose.Drawing;

`Bitmap` είναι ο κοντέινερ ραστερ εικόνας του Aspose.Drawing που αποθηκεύει τα δεδομένα pixel.  
Η αποθήκευση μιας εικόνας PNG σημαίνει την απόδοση της επιφάνειας σχεδίασής σας — ένα `Bitmap` — σε ένα αρχείο με την επέκταση `.png`. Το Aspose.Drawing εκτελεί συμπίεση PNG χωρίς απώλειες και μπορεί να διαχειριστεί εικόνες έως **10 000 × 10 000 pixel** χωρίς εξάντληση μνήμης, καθιστώντας το κατάλληλο για γραφικά υψηλής ανάλυσης. Το παραγόμενο αρχείο μπορεί να χρησιμοποιηθεί σε ιστοσελίδες, αναφορές ή περαιτέρω αλυσίδες επεξεργασίας εικόνας.

## Γιατί να καταγράψετε τις εγκατεστημένες γραμματοσειρές και να εμφανίσετε τις οικογένειες γραμματοσειρών;

Η καταγραφή των εγκατεστημένων γραμματοσειρών επιτρέπει στην εφαρμογή σας να προσαρμοστεί στο περιβάλλον του τελικού χρήστη, διασφαλίζοντας ότι τα παραγόμενα γραφικά ταιριάζουν με την εταιρική ταυτότητα ή τις προτιμήσεις του χρήστη χωρίς να χρειάζεται να διανείμετε επιπλέον αρχεία γραμματοσειρών. Το `InstalledFontCollection` απαριθμεί τις γραμματοσειρές που είναι εγκατεστημένες στο λειτουργικό σύστημα. Αυτό είναι ιδιαίτερα χρήσιμο για αυτοματοποιημένη δημιουργία αναφορών, πιστοποιητικών ή οποιοδήποτε οπτικό περιεχόμενο που πρέπει να σέβεται την τυπογραφία του συστήματος.

## Πώς να δημιουργήσετε bitmap γραφικά σε C# με Aspose.Drawing;

`Bitmap` αντιπροσωπεύει έναν καμβά εικόνας· `Graphics` παρέχει μεθόδους σχεδίασης για αυτόν τον καμβά· `Font` περιγράφει την γραμματοσειρά που χρησιμοποιείται για την απόδοση κειμένου. Μπορείτε να παραγάγετε ένα πλήρες PNG σε λίγες μόνο γραμμές: δημιουργήστε ένα `Bitmap`, αποκτήστε ένα αντικείμενο `Graphics`, σχεδιάστε κείμενο χρησιμοποιώντας ένα `Font` από την εγκατεστημένη συλλογή και, τέλος, καλέστε `bitmap.Save`. Ο παρακάτω οδηγός βήμα‑βήμα επεκτείνει κάθε μέρος και προσθέτει πρακτικές συμβουλές.

## Προαπαιτούμενα

- **Βιβλιοθήκη Aspose.Drawing** – κατεβάστε την πιο πρόσφατη έκδοση από τη [σελίδα λήψης Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider ή οποιονδήποτε επεξεργαστή συμβατό με .NET.  
- **Βασικές γνώσεις C#** – πρέπει να είστε άνετοι με κλάσεις, αντικείμενα και απλούς βρόχους.  
- **.NET runtime** – .NET 6+ ή .NET Core 3.1+ συνιστάται για πλήρη δια‑πλατφορμική υποστήριξη.

## Εισαγωγή χώρων ονομάτων

Προσθέστε τις παρακάτω δηλώσεις `using` στην κορυφή του αρχείου C# ώστε ο μεταγλωττιστής να μπορεί να εντοπίσει τους τύπους γραφικών και γραμματοσειρών:

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Text;
using System.IO;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Δημιουργία bitmap (καμβάς)

`Bitmap` είναι το αντικείμενο ραστερ εικόνας που κρατά τα δεδομένα pixel για τον καμβά.  

```csharp
using System.Drawing;
using System.Drawing.Text;
```

### Βήμα 2: Δημιουργία graphics από bitmap

`Graphics` είναι το αντικείμενο που παρέχει λειτουργίες σχεδίασης όπως η σχεδίαση σχημάτων και κειμένου πάνω σε ένα bitmap.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Βήμα 3: Ρύθμιση brush και font (σχεδίαση κειμένου με γραμματοσειρές)

`Brush` ορίζει πώς γεμίζονται τα σχήματα και το κείμενο με χρώμα, ενώ `Font` καθορίζει την γραμματοσειρά, το μέγεθος και το στυλ για την απόδοση κειμένου.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Βήμα 4: Καταγραφή εγκατεστημένων γραμματοσειρών και εμφάνιση οικογενειών γραμματοσειρών

`InstalledFontCollection` παρέχει πρόσβαση σε όλες τις οικογένειες γραμματοσειρών που είναι εγκατεστημένες στο σύστημα φιλοξενίας.  

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Βήμα 5: Αποθήκευση εικόνας PNG

`bitmap.Save` γράφει το bitmap σε ένα αρχείο στην επιλεγμένη μορφή εικόνας, όπως PNG.  

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

> **Συμβουλή:** Χρησιμοποιήστε `Path.Combine` για τη δημιουργία διαδρομών αρχείων ώστε να αποφύγετε προβλήματα με τους διαχωριστές καταλόγων σε διαφορετικά λειτουργικά συστήματα.

## Κοινά προβλήματα και λύσεις
| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Δεν εμφανίζονται γραμματοσειρές** | `InstalledFontCollection` δεν είναι γεμάτο (π.χ., εκτέλεση σε server χωρίς γραμματοσειρές). | Εγκαταστήστε τις απαιτούμενες γραμματοσειρές στον server ή ενσωματώστε προσαρμοσμένες γραμματοσειρές στην εφαρμογή σας. |
| **Το αποθηκευμένο αρχείο είναι κατεστραμμένο** | Λανθασμένη μορφή pixel ή έλλειψη δικαιωμάτων εγγραφής. | Βεβαιωθείτε ότι ο φάκελος προορισμού υπάρχει και η εφαρμογή έχει δικαιώματα εγγραφής· διατηρήστε `PixelFormat.Format32bppPArgb`. |
| **Το κείμενο φαίνεται θολό** | Χαμηλές ρυθμίσεις DPI ή μικρές διαστάσεις bitmap. | Αυξήστε τις διαστάσεις του bitmap ή ορίστε `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω προσαρμοσμένες γραμματοσειρές που δεν είναι εγκατεστημένες στο μηχάνημα;**  
Α: Ναι. Φορτώστε το αρχείο γραμματοσειράς σε ένα `PrivateFontCollection` και δημιουργήστε ένα `Font` από αυτή τη συλλογή, έπειτα σχεδιάστε το με τον ίδιο τρόπο όπως οι συστημικές γραμματοσειρές.

**Ε: Πώς να διαχειριστώ εξαιρέσεις σχετικές με γραμματοσειρές;**  
Α: Τυλίξτε τη δημιουργία γραμματοσειράς σε ένα μπλοκ `try/catch` και ελέγξτε το `ArgumentException` για ελλιπείς οικογένειες· παρέχετε εναλλακτική γραμματοσειρά όπως `Arial`.

**Ε: Είναι το Aspose.Drawing κατάλληλο για web εφαρμογές;**  
Α: Απόλυτα. Η βιβλιοθήκη λειτουργεί σε ASP.NET Core, Azure Functions και άλλα server‑side .NET περιβάλλοντα χωρίς την ανάγκη GDI+.

**Ε: Μπορώ να αλλάξω το χρώμα ή το στυλ του κειμένου;**  
Α: Ναι. Χρησιμοποιήστε διαφορετικούς τύπους `Brush` (π.χ., `LinearGradientBrush`) και τροποποιήστε το enum `FontStyle` για να εφαρμόσετε έντονη, πλάγια ή υπογράμμιση.

**Ε: Από πού μπορώ να λάβω προσωρινή άδεια για δοκιμή;**  
Α: Κατεβάστε μια δοκιμαστική άδεια από τη [σελίδα προσωρινής άδειας Aspose](https://purchase.aspose.com/temporary-license/).

## Συμπέρασμα

Ακολουθώντας αυτά τα βήματα μάθατε πώς να **αποθηκεύσετε εικόνα PNG σε C#** που καταγράφει δυναμικά **τις εγκατεστημένες γραμματοσειρές**, **εμφανίζει τις οικογένειες γραμματοσειρών**, **δημιουργεί γραφικά από bitmap** και **σχεδιάζει κείμενο με γραμματοσειρές** χρησιμοποιώντας το Aspose.Drawing για .NET. Τώρα γνωρίζετε πώς να **δημιουργήσετε bitmap γραφικά σε C#**, να ρυθμίσετε την ανάλυση του bitmap και να ενσωματώσετε προσαρμοσμένες γραμματοσειρές όταν χρειάζεται. Πειραματιστείτε με διαφορετικά χρώματα, μεγέθη γραμματοσειρών και διαστάσεις bitmap για να ταιριάζουν στις οπτικές απαιτήσεις του έργου σας, και εξερευνήστε άλλες δυνατότητες του Aspose.Drawing όπως η σχεδίαση σχημάτων και η επεξεργασία εικόνας για πιο πλούσια γραφικά.

---

**Τελευταία ενημέρωση:** 2026-09-23  
**Δοκιμή με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose








```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

## Σχετικά μαθήματα

- [Πώς να σχεδιάσετε κείμενο με Aspose.Drawing για .NET](/drawing/net/text-and-fonts/draw-text/)
- [Βελτιώστε την ποιότητα εικόνας με Antialiasing στο Aspose.Drawing](/drawing/net/rendering/antialiasing/)
- [Πώς να αποθηκεύσετε PNG με Aspose.Drawing – Μετασχηματισμός κόσμου](/drawing/net/coordinate-transformations/world-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}