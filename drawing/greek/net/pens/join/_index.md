---
date: 2026-09-18
description: Μάθετε πώς να σχεδιάσετε διαδρομή και να ενώσετε διαδρομές με πένες στο
  Aspose.Drawing, στη συνέχεια αποθηκεύστε την εικόνα ως PNG χρησιμοποιώντας απλό
  κώδικα C#.
keywords:
- save image as png
- server side image rendering
- raster image from vector
- export graphics to png
- alternative to system drawing
lastmod: 2026-09-18
linktitle: Ένωση διαδρομών με πένες στο Aspose.Drawing
og_description: Αποθηκεύστε την εικόνα ως PNG με το Aspose.Drawing. Μάθετε να σχεδιάζετε
  διαδρομές, να εφαρμόζετε στυλ line‑join και να εξάγετε raster graphics υψηλής ποιότητας
  από διανυσματικά δεδομένα στον διακομιστή.
og_image_alt: Developer guide showing how to draw and join paths with pens, then save
  the result as a PNG file using Aspose.Drawing
og_title: Πώς να σχεδιάσετε διαδρομή, να ενώσετε διαδρομές με πένες και να αποθηκεύσετε
  την εικόνα ως PNG
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to draw path and join paths with pens in Aspose.Drawing,
    then save the image as PNG using simple C# code.
  headline: How to draw path, join paths with pens and save image as PNG
  type: TechArticle
- questions:
  - answer: Aspose.Drawing is a commercial product, but you can explore its capabilities
      with a **[free trial](https://releases.aspose.com/)**.
    question: Can I use Aspose.Drawing for free?
  - answer: Refer to the **[documentation](https://reference.aspose.com/drawing/net/)**
      for comprehensive guidance.
    question: Where can I find Aspose.Drawing documentation?
  - answer: Visit the **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)**
      for community help and official assistance.
    question: How can I get support for Aspose.Drawing?
  - answer: Yes, you can obtain a **[temporary license](https://purchase.aspose.com/temporary-license/)**
      for short‑term usage.
    question: Are temporary licenses available for Aspose.Drawing?
  - answer: Purchase Aspose.Drawing **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.
    question: Where can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- C# graphics
- save PNG
- vector to raster
- server side rendering
title: Πώς να σχεδιάσετε διαδρομή, να ενώσετε διαδρομές με πένες και να αποθηκεύσετε
  την εικόνα ως PNG
url: /el/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να σχεδιάσετε διαδρομή, να ενώσετε διαδρομές με πένες και να αποθηκεύσετε την εικόνα ως PNG

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε πώς να **draw path** αντικείμενα, να τα ενώσετε με διαφορετικά στυλ line‑join και να **save image as PNG** χρησιμοποιώντας το Aspose.Drawing για .NET. Είτε δημιουργείτε μια μηχανή αναφορών, έναν επεξεργαστή σχεδίου, είτε χρειάζεστε server‑side απόδοση εικόνας για μια web υπηρεσία, η εξοικείωση με το σχεδιασμό διαδρομών με πένες σας δίνει ακριβή έλεγχο της μετατροπής vector‑to‑raster.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “draw path”;** Δημιουργεί ορισμούς γραμμών ή σχημάτων βασισμένους σε διανύσματα που ένα αντικείμενο `Graphics` μπορεί να αποδώσει.  
- **Ποια line joins είναι διαθέσιμα;** `Bevel`, `Miter`, `Round`, και `BevelClipped`.  
- **Μπορώ να εξάγω το αποτέλεσμα ως PNG;** Ναι—χρησιμοποιήστε `Bitmap.Save` με επέκταση `.png`.  
- **Χρειάζομαι άδεια;** Μια δοκιμαστική έκδοση λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.6+, .NET Core 3.1+, και .NET 6+.

## Τι είναι το “draw path” στο Aspose.Drawing;

**Draw path** σημαίνει τη δημιουργία ενός `GraphicsPath` που περιέχει μια σειρά από γραμμές, καμπύλες ή σχήματα.  
`GraphicsPath` είναι το κοντέινερ του Aspose.Drawing για γεωμετρία διανύσματος· μπορείτε αργότερα να το αποδώσετε με ένα `Pen` ή να το γεμίσετε με πινέλο. Αυτή η προσέγγιση σας επιτρέπει να εφαρμόζετε μετασχηματισμούς, αποκοπή και συνεπή στυλ line‑join σε ολόκληρο το σχήμα αντί να σχεδιάζετε κάθε τμήμα ξεχωριστά.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για server side απόδοση εικόνας;

Το Aspose.Drawing παρέχει μια ισχυρή μηχανή απόδοσης server‑side που λειτουργεί σε οποιοδήποτε λειτουργικό σύστημα χωρίς εξάρτηση από το GDI+, καθιστώντας το ιδανικό για υπηρεσίες cloud, εφαρμογές σε containers και web APIs υψηλής απόδοσης όπου απαιτείται συμβατότητα μεταξύ πλατφορμών και λειτουργία headless, εξασφαλίζοντας κλιμακώσιμη απόδοση.

- **Πλήρης συμβατότητα .NET** – υποστηρίζει .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Πλούσιες επιλογές line‑join** – `Bevel`, `Miter`, `Round`, `BevelClipped`.  
- **Υψηλής ποιότητας raster έξοδος** – μπορεί να εξάγει σε **10+ raster μορφές** (PNG, JPEG, BMP, GIF, TIFF, κλπ.) απευθείας από δεδομένα διανύσματος.  
- **Χωρίς περιορισμούς GDI+** – ιδανικό για υπηρεσίες cloud, containers και περιβάλλοντα headless.

## Προαπαιτούμενα

1. **Aspose.Drawing Library** – κατεβάστε το από τη **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.  
2. **.NET Development Environment** – Visual Studio, VS Code ή οποιοδήποτε IDE που υποστηρίζει C#.

Τώρα που όλα είναι έτοιμα, ας περάσουμε από κάθε βήμα.

## Εισαγωγή namespaces

Τα namespaces `System.Drawing` και `System.Drawing.Drawing2D` περιέχουν τους βασικούς τύπους γραφικών που χρησιμοποιεί το Aspose.Drawing.  

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Βήμα 1: Δημιουργία bitmap και αντικειμένου graphics

`Bitmap` είναι το in‑memory raster καμβά του Aspose.Drawing. Αντιπροσωπεύει μια raster εικόνα στην οποία μπορείτε να σχεδιάσετε χρησιμοποιώντας μια επιφάνεια `Graphics`.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Ξεκινάμε με έναν κενό καμβά (`Bitmap`) μεγέθους 1000 × 800 pixel και λαμβάνουμε ένα αντικείμενο `Graphics` που θα αποδώσει τις εντολές σχεδίασής μας.

## Βήμα 2: Ορισμός της μεθόδου drawPath

`Pen` είναι το εργαλείο του Aspose.Drawing για το στίλβωση διανυσματικών περιγραμμάτων· ορίζει χρώμα, πάχος και στυλ line‑join.  

`LineJoin` ελέγχει πώς δύο τμήματα γραμμής συνδέονται σε μια γωνία.  

`GraphicsPath` είναι το διανυσματικό κοντέινερ που κρατά τη σειρά των γραμμών που θα ενώσουμε.  

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

Αυτή η βοηθητική μέθοδος περιλαμβάνει τη λογική σχεδίασης:

- **Pen** – ορίζει το χρώμα και το πάχος (30 px).  
- **GraphicsPath** – ορίζει δύο συνδεδεμένες γραμμές που σχηματίζουν σχήμα “L”.  
- **LineJoin** – ελέγχει πώς αποδίδεται η γωνία μεταξύ των δύο γραμμών (`Bevel`, `Round`, κλπ.).  

Μπορείτε να καλέσετε αυτή τη μέθοδο με οποιαδήποτε τιμή `LineJoin` για να δείτε τη διαφορά.

## Βήμα 3: Ένωση διαδρομών με line join τύπου bevel

`LineJoin.Bevel` δημιουργεί μια επίπεδη γωνία όπου συναντώνται οι δύο γραμμές, χρήσιμο όταν θέλετε μια καθαρή, μη επικαλυπτόμενη ένωση.

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

## Βήμα 4: Ένωση διαδρομών με line join τύπου round

`LineJoin.Round` παράγει μια ομαλή, στρογγυλεμένη γωνία—ιδανική για πιο επεξεργασμένη εμφάνιση.

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

## Βήμα 5: Αποθήκευση του αποτελέσματος ως PNG

Η κλήση `Save` γράφει το bitmap σε αρχείο σε μορφή PNG, ολοκληρώνοντας τη ροή εργασίας **save image as PNG**. Προσαρμόστε τη διαδρομή ώστε να ταιριάζει με το περιβάλλον σας.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

## Συχνά προβλήματα και λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Διόρθωση |
|----------|----------------|----------|
| **Η εικόνα εμφανίζεται κενή** | Το αντικείμενο `Graphics` δεν καθαρίστηκε ή το μέγεθος του bitmap είναι πολύ μικρό. | Καλέστε `graphics.Clear(Color.White);` πριν το σχεδιασμό, ή αυξήστε τις διαστάσεις του bitmap. |
| **Η γωνία φαίνεται δονισμένη** | Χρήση bitmap χαμηλής ανάλυσης με παχύ πέννα. | Αυξήστε το DPI του bitmap (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) ή μειώστε το πάχος του πέννα. |
| **Σφάλμα αρχείου δεν βρέθηκε** | Μη έγκυρη διαδρομή αποθήκευσης. | Χρησιμοποιήστε `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το Aspose.Drawing δωρεάν;**  
Α: Το Aspose.Drawing είναι εμπορικό προϊόν, αλλά μπορείτε να εξερευνήσετε τις δυνατότητές του με μια **[free trial](https://releases.aspose.com/)**.

**Ε: Πού μπορώ να βρω την τεκμηρίωση του Aspose.Drawing;**  
Α: Ανατρέξτε στην **[documentation](https://reference.aspose.com/drawing/net/)** για ολοκληρωμένη καθοδήγηση.

**Ε: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Drawing;**  
Α: Επισκεφθείτε το **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)** για βοήθεια της κοινότητας και επίσημη υποστήριξη.

**Ε: Διατίθενται προσωρινές άδειες για το Aspose.Drawing;**  
Α: Ναι, μπορείτε να αποκτήσετε μια **[temporary license](https://purchase.aspose.com/temporary-license/)** για βραχυπρόθεσμη χρήση.

**Ε: Πού μπορώ να αγοράσω το Aspose.Drawing;**  
Α: Αγοράστε το Aspose.Drawing από την **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.

## Συμπέρασμα

Σε αυτόν τον οδηγό καλύψαμε πώς να δημιουργήσετε αντικείμενα **draw path**, να εφαρμόσετε διαφορετικά στυλ `LineJoin`, και να **save image as PNG** χρησιμοποιώντας το Aspose.Drawing για .NET. Με την εξοικείωση με αυτά τα βήματα μπορείτε να παράγετε σύνθετα διανυσματικά γραφικά, προσαρμοσμένα εικονίδια ή δυναμικά διαγράμματα απευθείας από κώδικα server‑side, παρέχοντας μια αξιόπιστη λύση **export graphics to PNG** που λειτουργεί σε οποιαδήποτε πλατφόρμα.

---

**Last Updated:** 2026-09-18  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Πώς να Σχεδιάσετε Τόξο και να Αποθηκεύσετε Εικόνα PNG με Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-arc/)
- [Πώς να αποθηκεύσετε bitmap ως PNG ενώ σχεδιάζετε πολλαπλές γραμμές με Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [Πώς να αποθηκεύσετε ένα bitmap ως PNG χρησιμοποιώντας το Aspose.Drawing API για .NET](/drawing/net/image-editing/display/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}