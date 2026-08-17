---
date: 2026-07-17
description: Μάθετε πώς να αποτρέψετε την υπερχείλιση κειμένου ορίζοντας τη στοίχιση
  κειμένου στο Aspose.Drawing για .NET και να προσθέτετε κείμενο σε εικόνες. Οδηγός
  βήμα προς βήμα με παραδείγματα.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Ορισμός Στοίχισης Κειμένου με Aspose.Drawing για .NET
og_description: Αποτρέψτε την υπερχείλιση κειμένου ορίζοντας τη στοίχιση κειμένου
  στο Aspose.Drawing για .NET. Μάθετε πώς να σχεδιάζετε συμβολοσειρά σε εικόνα, να
  κεντράρετε το κείμενο σε ορθογώνιο και να αντικαταστήσετε το System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Αποτροπή Υπερχείλισης Κειμένου – Ορισμός Στοίχισης Κειμένου με Aspose.Drawing
  για .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Αποτροπή Υπερχείλισης Κειμένου – Ορισμός Στοίχισης Κειμένου με Aspose.Drawing
  για .NET
url: /el/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποτροπή Υπέρβασης Κειμένου – Ορισμός Στοίχισης Κειμένου με Aspose.Drawing

## Εισαγωγή

Όταν χρειάζεται να **αποτρέψετε την υπέρβαση κειμένου** κατά την απόδοση γραφικών σε .NET, το Aspose.Drawing σας παρέχει λεπτομερή έλεγχο της τοποθέτησης, της στοίχισης και της αναδίπλωσης του κειμένου. Είτε δημιουργείτε έναν γεννήτρια καρτών, μια δυναμική αναφορά ή οποιαδήποτε έξοδο βασισμένη σε εικόνα, η καλή διαχείριση της στοίχισης κειμένου εξασφαλίζει ότι το κείμενο παραμένει εντός του προβλεπόμενου ορθογωνίου και φαίνεται επαγγελματικό. Σε αυτόν τον οδηγό θα περάσουμε από τη δημιουργία ενός bitmap καμβά, τη διαμόρφωση του `StringFormat`, τη σχεδίαση ενός ορθογωνίου με κεντραρισμένο κείμενο, τη διαχείριση της υπέρβασης και, τέλος, την αποθήκευση της εικόνας.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “ορισμός στοίχισης κειμένου”;** Ορίζει πώς το κείμενο τοποθετείται οριζόντια και κάθετα μέσα σε ένα ορθογώνιο σχεδίασης.  
- **Ποια κλάση ελέγχει τη στοίχιση;** Η `StringFormat` σας επιτρέπει να ορίσετε `Alignment` και `LineAlignment`.  
- **Μπορώ να σχεδιάσω ένα κείμενο και ένα ορθογώνιο μαζί;** Ναι—χρησιμοποιήστε `Graphics.DrawRectangle` και στη συνέχεια `Graphics.DrawString`.  
- **Πώς αποτρέπω την υπέρβαση κειμένου;** Προσαρμόστε το μέγεθος του ορθογωνίου ή χωρίστε το κείμενο σε πολλές γραμμές χειροκίνητα.  
- **Χρειάζεται άδεια για παραγωγική χρήση;** Απαιτείται εμπορική άδεια Aspose.Drawing για χρήση εκτός αξιολόγησης.

## Τι είναι **ορισμός στοίχισης κειμένου** στο Aspose.Drawing;

`set text alignment` ρυθμίζει την οριζόντια (`StringAlignment`) και κάθετη (`LineAlignment`) τοποθέτηση του κειμένου μέσα σε ένα `Rectangle` ή περιοχή σχεδίασης. Με την προσαρμογή αυτών των ιδιοτήτων ελέγχετε αν το κείμενο εμφανίζεται αριστερά, κεντραρισμένο, δεξιά, στην κορυφή, στο κέντρο ή στο κάτω μέρος, επιτρέποντας ακριβή διάταξη σε γραφικά, ετικέτες και αναφορές που δημιουργούνται με Aspose.Drawing.

## Γιατί να χρησιμοποιήσω το Aspose.Drawing για στοίχιση κειμένου;

Το Aspose.Drawing εξαλείφει τους περιορισμούς του GDI+ που επηρεάζουν το `System.Drawing.Common`. Υποστηρίζει **5 κύριες εκδόσεις .NET** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 και .NET 7 – και μπορεί να αποδώσει εικόνες έως **4000 × 4000 px** (≈ 100 MB) χωρίς εξάντληση μνήμης. Η αντι-αποκοπή (anti‑aliasing), η κλιμάκωση υψηλής DPI και η πλήρης συμβατότητα με Linux containers σας επιτρέπουν να δημιουργείτε pixel‑perfect γραφικά σε οποιοδήποτε σενάριο ανάπτυξης.

## Προαπαιτούμενα

1. **Βιβλιοθήκη Aspose.Drawing** – κατεβάστε την [εδώ](https://releases.aspose.com/drawing/net/).  
2. **Περιβάλλον Ανάπτυξης** – Visual Studio 2022 (ή οποιοδήποτε IDE C#).  
3. **Βασικές γνώσεις .NET** – πρέπει να είστε άνετοι με έργα C# και πακέτα NuGet.

## Εισαγωγή Ονομάτων Χώρου

Για να ξεκινήσετε, φέρτε τα απαιτούμενα ονόματα χώρου στο πεδίο σας. Αυτά σας δίνουν πρόσβαση σε γραφικά, απόδοση κειμένου και primitives σχεδίασης.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Πώς να αποτρέψετε την υπέρβαση κειμένου με Aspose.Drawing;

Το Bitmap είναι μια κλάση που αντιπροσωπεύει μια εικόνα αποθηκευμένη στη μνήμη, ενώ το `RectangleF` ορίζει μια περιοχή ορθογωνίου με δεκαδικές τιμές για σχεδίαση. Χρησιμοποιώντας ένα `StringFormat` με `Trimming` ορισμένο σε `StringTrimming.EllipsisCharacter`, οι επιπλέον χαρακτήρες αντικαθίστανται αυτόματα με ελλειπτικό (… ), εξασφαλίζοντας ότι το κείμενο δεν υπερβαίνει τα όρια του ορθογωνίου. Η μέτρηση του κειμένου πρώτα σας επιτρέπει να αποφασίσετε αν θα μειώσετε το ορθογώνιο ή θα χωρίσετε το κείμενο σε πολλές γραμμές, εξασφαλίζοντας καθαρή διάταξη χωρίς υπερβολές.

Φορτώστε το bitmap, ορίστε ένα κατάλληλο `RectangleF` και χρησιμοποιήστε ένα `StringFormat` με `Trimming` σε `StringTrimming.EllipsisCharacter` για αυτόματη αποκοπή των επιπλέον χαρακτήρων. Για πλήρη έλεγχο, μετρήστε το κείμενο με `Graphics.MeasureString` και μειώστε το ορθογώνιο ή χωρίστε το κείμενο σε γραμμές πριν το σχεδιάσετε. Αυτή η προσέγγιση εγγυάται ότι κανένας χαρακτήρας δεν θα ξεφύγει από τα οπτικά όρια.

## Βήμα 1: Δημιουργία Αντικειμένων Bitmap και Graphics  

Το Bitmap αντιπροσωπεύει μια εικόνα στη μνήμη, ενώ το Graphics παρέχει μεθόδους σχεδίασης για αυτό το bitmap. Η δημιουργία ενός bitmap παρέχει έναν καμβά πάνω στον οποίο μπορείτε να σχεδιάσετε. Το αντικείμενο `Graphics` είναι η επιφάνεια σχεδίασης και ενεργοποιούμε την υψηλής ποιότητας απόδοση κειμένου με `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Βήμα 2: Ορισμός **StringFormat** και Στυλ  

Η StringFormat καθορίζει επιλογές διάταξης κειμένου όπως στοίχιση, απόσταση γραμμών και αποκοπή. Εδώ **ορίζουμε τη στοίχιση κειμένου** διαμορφώνοντας ένα αντικείμενο `StringFormat`. Επίσης προετοιμάζουμε πινέλα, στυλό και μια γραμματοσειρά που θα χρησιμοποιηθούν κατά τη σχεδίαση του κειμένου.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Βήμα 3: Δημιουργία και Μορφοποίηση Κειμένου – **πώς να σχεδιάσετε string** και **σχεδίαση ορθογωνίου με κείμενο**

Η `Graphics.DrawString` αποδίδει κείμενο στον καμβά, ενώ η `Graphics.DrawRectangle` σχεδιάζει ένα σχήμα ορθογωνίου. Συνθέτουμε το κείμενο, ορίζουμε το ορθογώνιο που θα το περιέχει και στη συνέχεια σχεδιάζουμε τόσο το περίγραμμα του ορθογωνίου όσο και το ίδιο το κείμενο.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Πώς να διαχειριστείτε την υπέρβαση κειμένου

Αν το παρεχόμενο `text` υπερβαίνει τα όρια του ορθογωνίου, έχετε δύο κοινές επιλογές:

1. **Αλλαγή μεγέθους του ορθογωνίου** – αυξήστε το `rectangle.Width` ή το `rectangle.Height`.  
2. **Διαίρεση του κειμένου** – χωρίστε το string σε γραμμές που χωράνε, έπειτα καλέστε `DrawString` για κάθε γραμμή με προσαρμοσμένες συντεταγμένες Y.

## Πώς να σχεδιάσετε string σε εικόνα χρησιμοποιώντας Aspose.Drawing;

Η `Graphics.DrawString` σχεδιάζει το καθορισμένο κείμενο χρησιμοποιώντας μια γραμματοσειρά και επιλογές μορφοποίησης. Δημιουργήστε ένα αντικείμενο `Graphics` από το bitmap σας, στη συνέχεια καλέστε `DrawString` με το προετοιμασμένο `StringFormat`. Αυτή η ενιαία κλήση αποδίδει το κείμενο ακριβώς εκεί που το θέλετε, τηρώντας τη στοίχιση, την αποκοπή και τυχόν μετασχηματισμό που έχετε εφαρμόσει. Η προσθήκη μιας υψηλής ποιότητας υπόδειξης απόδοσης εξασφαλίζει ότι το αποτέλεσμα παραμένει καθαρό σε οθόνες υψηλής DPI.

## Πώς να κεντράρετε κείμενο σε ορθογώνιο;

Η `StringAlignment` καθορίζει την οριζόντια στοίχιση του κειμένου μέσα σε ένα ορθογώνιο διάταξης. Ορίστε `stringFormat.Alignment = StringAlignment.Center` και `stringFormat.LineAlignment = StringAlignment.Center`. Αυτό κεντράρει το κείμενο οριζόντια και κάθετα μέσα στο ορθογώνιο, καθιστώντας το ιδανικό για ετικέτες, κουμπιά ή επικάλυψη κειμένου. Η κεντραρισμένη τοποθέτηση λειτουργεί σταθερά σε διαφορετικά μεγέθη εικόνας και ρυθμίσεις DPI, παρέχοντας ισορροπημένη οπτική εμφάνιση.

## Πώς να επιτύχετε κάθετη στοίχιση κειμένου;

Η `LineAlignment` ελέγχει την κάθετη τοποθέτηση του κειμένου μέσα στο ορθογώνιο. Χρησιμοποιήστε το `stringFormat.LineAlignment` με τιμές `StringAlignment.Near`, `Center` ή `Far` για να τοποθετήσετε το κείμενο στην κορυφή, στο κέντρο ή στο κάτω μέρος του ορθογωνίου. Συνδυάστε το με `Graphics.TranslateTransform` εάν χρειάζεται να περιστρέψετε το κείμενο διατηρώντας την κάθετη στοίχιση. Η προσαρμογή της στοίχισης γραμμής εξασφαλίζει ότι τα μπλοκ πολλαπλών γραμμών ευθυγραμμίζονται ακριβώς όπως αναμένετε, ακόμη και μετά από μετασχηματισμούς.

## Βήμα 4: Αποθήκευση του Αποτελέσματος – **προσθήκη κειμένου σε εικόνα**

Τέλος, γράψτε το bitmap στο δίσκο. Αυτό το βήμα επιδεικνύει **προσθήκη κειμένου σε εικόνα** με μία μόνο κλήση.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Λύση |
|----------|------|
| **Το κείμενο εμφανίζεται θολό** | Βεβαιωθείτε ότι έχει οριστεί `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`. |
| **Το κείμενο κόβεται** | Αυξήστε το μέγεθος του ορθογωνίου ή ενεργοποιήστε λογική αναδίπλωσης με μέτρηση του μεγέθους του κειμένου (`Graphics.MeasureString`). |
| **Η γραμματοσειρά δεν βρέθηκε** | Επαληθεύστε ότι η γραμματοσειρά είναι εγκατεστημένη στο σύστημα ή ενσωματώστε ιδιωτική γραμματοσειρά με `PrivateFontCollection`. |
| **Απρόσμενα χρώματα** | Ελέγξτε ξανά τα χρώματα πινέλου και στυλό· θυμηθείτε ότι το `Color.FromKnownColor` χρησιμοποιεί χρώματα ορισμένα από το σύστημα. |

## Συχνές Ερωτήσεις

**Ε1: Είναι το Aspose.Drawing συμβατό με όλες τις εκδόσεις .NET;**  
Α1: Ναι, το Aspose.Drawing έχει σχεδιαστεί ώστε να είναι συμβατό με ένα ευρύ φάσμα εκδόσεων .NET, εξασφαλίζοντας ευελιξία για τους προγραμματιστές.

**Ε2: Μπορώ να προσαρμόσω περαιτέρω το στυλ της γραμματοσειράς;**  
Α2: Απόλυτα! Ρυθμίστε τις παραμέτρους του αντικειμένου `Font` για να πετύχετε το επιθυμητό μέγεθος, στυλ και οικογένεια γραμματοσειράς.

**Ε3: Πώς μπορώ να διαχειριστώ την υπέρβαση κειμένου μέσα στο ορισμένο ορθογώνιο;**  
Α3: Μπορείτε να διαχειριστείτε την υπέρβαση προσαρμόζοντας το μέγεθος του ορθογωνίου ή υλοποιώντας προσαρμοσμένη λογική για τη διαχείριση μεγάλου κειμένου.

**Ε4: Υπάρχουν άλλες επιλογές μορφοποίησης διαθέσιμες στο Aspose.Drawing;**  
Α4: Ναι, το Aspose.Drawing παρέχει ένα ολοκληρωμένο σύνολο εργαλείων για τη διαχείριση γραφικών, συμπεριλαμβανομένων διαφόρων επιλογών μορφοποίησης κειμένου, σχημάτων και άλλων.

**Ε5: Πού μπορώ να βρω επιπλέον υποστήριξη για το Aspose.Drawing;**  
Α5: Εξερευνήστε το φόρουμ Aspose.Drawing [εδώ](https://forum.aspose.com/c/drawing/44) για υποστήριξη κοινότητας και συζητήσεις.

**Επιπλέον Ε&Α**

**Ε: Πώς να σχεδιάσω ένα string χωρίς περιβάλλον ορθογώνιο;**  
Α: Παραλείψτε την κλήση `DrawRectangle` και περάστε την επιθυμητή θέση `PointF` στη `Graphics.DrawString`.

**Ε: Μπορώ να περιστρέψω το κείμενο διατηρώντας τη στοίχιση;**  
Α: Ναι—εφαρμόστε έναν μετασχηματισμό `Matrix` στο αντικείμενο `Graphics` πριν τη σχεδίαση, έπειτα επαναφέρετε τον μετά.

**Ε: Είναι δυνατόν να εξάγω την εικόνα ως JPEG αντί για PNG;**  
Α: Απλώς αλλάξτε την επέκταση αρχείου στην κλήση `bitmap.Save` και, προαιρετικά, ορίστε `ImageFormat.Jpeg`.

---

**Τελευταία Ενημέρωση:** 2026-07-17  
**Δοκιμή Με:** Aspose.Drawing 24.11 για .NET  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [How to Draw Text with Aspose.Drawing for .NET](/drawing/net/text-and-fonts/draw-text/)
- [Adding Text on Images in Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [How to Draw Text and Fonts with Aspose.Drawing for .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}