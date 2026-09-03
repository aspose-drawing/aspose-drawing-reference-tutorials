---
date: 2026-09-03
description: Μάθετε πώς να δημιουργήσετε text overlay σε εικόνες χρησιμοποιώντας Aspose.Drawing
  για .NET. Αυτός ο οδηγός βήμα‑βήμα σας δείχνει πώς να προσθέσετε κείμενο σε εικόνα,
  draw text σε εικόνα, και measure string size αποδοτικά.
keywords:
- create text overlay
- add text to image
- draw text on image
- measure string size
- calculate text dimensions
lastmod: 2026-09-03
linktitle: Προσθήκη κειμένου σε εικόνες στο Aspose.Drawing
og_description: Μάθετε πώς να δημιουργήσετε text overlay σε εικόνες χρησιμοποιώντας
  Aspose.Drawing για .NET. Αυτός ο οδηγός καλύπτει την προσθήκη κειμένου σε εικόνα,
  drawing text σε εικόνα, και measuring string size σε λίγα εύκολα βήματα.
og_image_alt: Tutorial showing how to create text overlay on images using Aspose.Drawing
  in .NET
og_title: Πώς να δημιουργήσετε text overlay σε εικόνες με Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create text overlay on images using Aspose.Drawing for
    .NET. This step‑by‑step guide shows you how to add text to image, draw text on
    image, and measure string size efficiently.
  headline: How to create text overlay on images with Aspose.Drawing
  type: TechArticle
- description: Learn how to create text overlay on images using Aspose.Drawing for
    .NET. This step‑by‑step guide shows you how to add text to image, draw text on
    image, and measure string size efficiently.
  name: How to create text overlay on images with Aspose.Drawing
  steps:
  - name: import namespaces
    text: 'Begin by importing the necessary namespaces into your C# project:'
  - name: load the image
    text: Here, we load the image from the specified file path and initialize the
      graphics object for further processing.
  - name: set text properties
    text: Define the text properties such as color, font, and padding. Adjust these
      parameters according to your preferences.
  - name: measure text size
    text: Calculate the required size for the text by measuring each word individually.
      This ensures proper placement and avoids text overlap.
  - name: draw text on image
    text: Now, position the text on the image based on the calculated size and draw
      it using the specified font and color.
  - name: save the image
    text: Save the modified image to your desired directory. This step‑by‑step guide
      demonstrates a straightforward process of adding text to images using Aspose.Drawing
      for .NET. Experiment with different fonts, colors, and text content to achieve
      the desired visual effect.
  type: HowTo
- questions:
  - answer: Measure the string width with `Graphics.MeasureString`, subtract it from
      the image width, divide by two, and use that X coordinate when calling `DrawString`.
    question: How do I center text horizontally on the image?
  - answer: Yes—use `StringFormat` with `FormatFlags.LineLimit` and pass a string
      containing `\n` to `DrawString`.
    question: Can I add multi‑line text with line breaks?
  - answer: Absolutely. Set the brush color using `Color.FromArgb(alpha, r, g, b)`
      where `alpha` controls opacity.
    question: Does Aspose.Drawing support transparent text?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- image processing
- Aspose.Drawing
- .NET graphics
title: Πώς να δημιουργήσετε text overlay σε εικόνες με Aspose.Drawing
url: /el/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να δημιουργήσετε επικάλυψη κειμένου σε εικόνες με Aspose.Drawing

## Εισαγωγή
Το Aspose.Drawing είναι ένα .NET API που παρέχει προηγμένες δυνατότητες επεξεργασίας εικόνας χωρίς να εξαρτάται από το System.Drawing.Common. Στον δυναμικό κόσμο της ανάπτυξης .NET, η δημιουργία επικάλυψης κειμένου σε εικόνες είναι συχνή ανάγκη—είτε προσθέτετε υδατογράφημα σε φωτογραφίες, είτε προσθέτετε λεζάντες, είτε δημιουργείτε προσαρμοσμένα γραφικά. Αυτό το σεμινάριο σας καθοδηγεί μέσα από τη διαδικασία προσθήκης κειμένου σε εικόνες χρησιμοποιώντας C# και Aspose.Drawing, ώστε να μπορείτε να εφαρμόσετε τη λύση σε λίγα λεπτά.

## Γρήγορες απαντήσεις
- **Ποια είναι η κύρια κλάση για σχεδίαση;** `Graphics` από το Aspose.Drawing διαχειρίζεται όλες τις λειτουργίες σχεδίασης.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν προσωρινή άδεια λειτουργεί για δοκιμές· απαιτείται πλήρης άδεια για παραγωγή.  
- **Ποιοι μορφές εικόνας υποστηρίζονται;** Πάνω από 30 μορφές, συμπεριλαμβανομένων JPEG, PNG, BMP και GIF.  
- **Μπορώ να μετρήσω το μέγεθος του κειμένου πριν τη σχεδίαση;** Ναι—χρησιμοποιήστε `Graphics.MeasureString` για να υπολογίσετε ακριβείς διαστάσεις.  
- **Είναι το API συμβατό με .NET 6;** Απόλυτα, το Aspose.Drawing στοχεύει στο .NET Framework 4.5+ και .NET 5/6+.

## Τι είναι η δημιουργία επικάλυψης κειμένου;
Η δημιουργία επικάλυψης κειμένου αναφέρεται στη διαδικασία απόδοσης κειμενικού περιεχομένου πάνω σε υπάρχουσα bitmap εικόνα, παράγοντας ένα ενιαίο οπτικό στοιχείο που μπορεί να αποθηκευτεί ή να εμφανιστεί. Στην πράξη, το κείμενο γίνεται μέρος των δεδομένων pixel, επιτρέποντας στην προκύπτουσα εικόνα να χρησιμοποιηθεί όπου γίνονται αποδεκτές τυπικές εικόνες, όπως ιστοσελίδες, αναφορές ή έντυπο υλικό. Η επικάλυψη μπορεί να περιλαμβάνει στυλ, θέση και διαφάνεια για την επίτευξη του επιθυμητού οπτικού αποτελέσματος.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για αυτήν την εργασία;
Το Aspose.Drawing υποστηρίζει περισσότερες από 30 μορφές εικόνας και μπορεί να επεξεργαστεί αρχεία μεγαλύτερα από 500 MB χωρίς να φορτώνει ολόκληρη την εικόνα στη μνήμη, παρέχοντας έως και 2× ταχύτερη απόδοση σε σύγκριση με το System.Drawing σε μεγάλες δέσμες. Το API του είναι πλήρως διαχειριζόμενο, εξαλείφοντας τις εξαρτήσεις κώδικα native και απλοποιώντας την ανάπτυξη σε Windows, Linux και macOS.

## Προαπαιτούμενα
Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τα παρακάτω:

1. **Βιβλιοθήκη Aspose.Drawing** – κατεβάστε και εγκαταστήστε από την [τεκμηρίωση Aspose.Drawing για .NET](https://reference.aspose.com/drawing/net/).  
2. **Περιβάλλον ανάπτυξης** – Visual Studio 2022, Rider ή οποιοδήποτε IDE που υποστηρίζει .NET 6+.  
3. **Δειγματική εικόνα** – οποιοδήποτε αρχείο JPEG/PNG που θέλετε να σχολιάσετε.

Τώρα, ας περάσουμε βήμα προς βήμα στην υλοποίηση.

## Πώς να δημιουργήσετε επικάλυψη κειμένου σε μια εικόνα;
Θα ξεκινήσετε φορτώνοντας το bitmap πηγής σε ένα αντικείμενο `Graphics`, στη συνέχεια ορίζετε τη γραμματοσειρά, το πινέλο και το περιθώριο. Αφού μετρήσετε τις διαστάσεις του κειμένου για να αποφύγετε την αποκοπή, τοποθετείτε το ορθογώνιο και αποδίδετε τη συμβολοσειρά. Τέλος, αποθηκεύετε την τροποποιημένη εικόνα στο δίσκο. Η παρακάτω σύντομη περιγραφή δείχνει τη πλήρη ακολουθία που θα ακολουθήσετε στα αναλυτικά βήματα παρακάτω.

### Βήμα 1: εισαγωγή χώρων ονομάτων
Ξεκινήστε εισάγοντας τους απαραίτητους χώρους ονομάτων στο έργο C# σας:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

### Βήμα 2: φόρτωση της εικόνας
Εδώ, φορτώνουμε την εικόνα από τη συγκεκριμένη διαδρομή αρχείου και αρχικοποιούμε το αντικείμενο graphics για περαιτέρω επεξεργασία.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```

### Βήμα 3: ορισμός ιδιοτήτων κειμένου
Ορίστε τις ιδιότητες του κειμένου όπως χρώμα, γραμματοσειρά και περιθώριο. Προσαρμόστε αυτές τις παραμέτρους σύμφωνα με τις προτιμήσεις σας.
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```

### Βήμα 4: μέτρηση μεγέθους κειμένου
Υπολογίστε το απαιτούμενο μέγεθος για το κείμενο μετρώντας κάθε λέξη ξεχωριστά. Αυτό εξασφαλίζει σωστή τοποθέτηση και αποτρέπει την επικάλυψη κειμένου.
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```

### Βήμα 5: σχεδίαση κειμένου στην εικόνα
Τώρα, τοποθετήστε το κείμενο στην εικόνα βάσει του υπολογισμένου μεγέθους και σχεδιάστε το χρησιμοποιώντας τη συγκεκριμένη γραμματοσειρά και χρώμα.
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```

### Βήμα 6: αποθήκευση της εικόνας
Αποθηκεύστε την τροποποιημένη εικόνα στον επιθυμητό φάκελο.
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```

Αυτός ο οδηγός βήμα‑βήμα δείχνει μια απλή διαδικασία προσθήκης κειμένου σε εικόνες χρησιμοποιώντας το Aspose.Drawing για .NET. Πειραματιστείτε με διαφορετικές γραμματοσειρές, χρώματα και περιεχόμενο κειμένου για να πετύχετε το επιθυμητό οπτικό αποτέλεσμα.

## Κοινά προβλήματα και λύσεις
- **Το κείμενο εμφανίζεται θολό** – βεβαιωθείτε ότι η ανάλυση της εικόνας (DPI) ταιριάζει με το μέγεθος της γραμματοσειράς· χρησιμοποιήστε `Graphics.SmoothingMode = SmoothingMode.AntiAlias`.  
- **Απροσδόκητη αποκοπή** – ελέγξτε ότι το πλάτος της μετρημένης συμβολοσειράς δεν υπερβαίνει τα όρια της εικόνας· προσθέστε περιθώριο ή μειώστε το μέγεθος της γραμματοσειράς όπως απαιτείται.  
- **Η άδεια δεν βρέθηκε** – τοποθετήστε το αρχείο άδειας στον φάκελο εκτελέσιμου ή ορίστε το προγραμματιστικά με `new License().SetLicense("Aspose.Drawing.lic")`.

## Συχνές ερωτήσεις
### Είναι το Aspose.Drawing συμβατό με όλες τις μορφές εικόνας;
Το Aspose.Drawing υποστηρίζει ένα ευρύ φάσμα μορφών εικόνας, συμπεριλαμβανομένων των δημοφιλών όπως JPEG, PNG και GIF. Ανατρέξτε στην [τεκμηρίωση](https://reference.aspose.com/drawing/net/) για πλήρη λίστα.

### Μπορώ να χρησιμοποιήσω το Aspose.Drawing για εμπορικά έργα;
Ναι, το Aspose.Drawing είναι κατάλληλο τόσο για προσωπικά όσο και για εμπορικά έργα. Για λεπτομέρειες άδειας, επισκεφθείτε τη [σελίδα αγοράς](https://purchase.aspose.com/buy).

### Υπάρχουν προσωρινές άδειες για δοκιμαστικούς σκοπούς;
Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια για δοκιμές επισκεπτόμενοι το [Temporary License](https://purchase.aspose.com/temporary-license/).

### Πού μπορώ να βρω υποστήριξη κοινότητας για το Aspose.Drawing;
Συμμετέχετε στην κοινότητα και λάβετε υποστήριξη στο [φόρουμ Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

### Πώς μπορώ να ξεκινήσω με το Aspose.Drawing;
Ξεκινήστε κατεβάζοντας τη βιβλιοθήκη από τη [σελίδα λήψης Aspose.Drawing](https://releases.aspose.com/drawing/net/) και εξερευνήστε την εκτενή [τεκμηρίωση](https://reference.aspose.com/drawing/net/).

**Πρόσθετες ερωτήσεις & απαντήσεις**

**Q: Πώς κεντράρω το κείμενο οριζόντια στην εικόνα;**  
A: Μετρήστε το πλάτος της συμβολοσειράς με `Graphics.MeasureString`, αφαιρέστε το από το πλάτος της εικόνας, διαιρέστε δια δύο και χρησιμοποιήστε αυτήν τη συντεταγμένη X όταν καλείτε το `DrawString`.

**Q: Μπορώ να προσθέσω κείμενο πολλών γραμμών με αλλαγές γραμμής;**  
A: Ναι—χρησιμοποιήστε `StringFormat` με `FormatFlags.LineLimit` και περάστε μια συμβολοσειρά που περιέχει `\n` στο `DrawString`.

**Q: Υποστηρίζει το Aspose.Drawing διαφανές κείμενο;**  
A: Απόλυτα. Ορίστε το χρώμα του πινέλου χρησιμοποιώντας `Color.FromArgb(alpha, r, g, b)` όπου το `alpha` ελέγχει τη διαφάνεια.

## Συμπέρασμα
Το Aspose.Drawing απλοποιεί τις εργασίες επεξεργασίας εικόνας στο .NET, προσφέροντας ένα ισχυρό σύνολο εργαλείων που μπορεί να **επεξεργαστεί πάνω από 30 μορφές εικόνας** και **χειριστεί αρχεία μεγαλύτερα από 500 MB** χωρίς πλήρη φόρτωση στη μνήμη. Η προσθήκη επικάλυψης κειμένου είναι μόνο ένα παράδειγμα της ευελιξίας του, επιτρέποντάς σας να δημιουργείτε υδατογραφήματα, λεζάντες και προσαρμοσμένα γραφικά αποδοτικά.

---

**Τελευταία ενημέρωση:** 2026-09-03  
**Δοκιμή με:** Aspose.Drawing 24.12 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά σεμινάρια

- [Πώς να σχεδιάσετε κείμενο και γραμματοσειρές με το Aspose.Drawing για .NET](/drawing/net/text-and-fonts/)
- [Πώς να σχεδιάσετε κείμενο με το Aspose.Drawing για .NET](/drawing/net/text-and-fonts/draw-text/)
- [Πώς να σχεδιάσετε ορθογώνιο – Μετασχηματισμός συστήματος συντεταγμένων (Μετασχηματισμός σελίδας) χρησιμοποιώντας το Aspose.Drawing API για .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}