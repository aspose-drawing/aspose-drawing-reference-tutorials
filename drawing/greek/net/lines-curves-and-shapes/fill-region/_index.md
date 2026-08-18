---
date: 2026-08-16
description: Μάθετε πώς να γεμίσετε περιοχή χρησιμοποιώντας το Aspose.Drawing για
  .NET, να δημιουργήσετε dynamic images, και να δημιουργήσετε μια περιοχή από polygon
  με step‑by‑step code.
keywords:
- how to fill region
- server side image generation
- create dynamic images
- fill shape gradient
- region filling graphics
lastmod: 2026-08-16
linktitle: Πώς να γεμίσετε περιοχή στο Aspose.Drawing
og_description: Μάθετε πώς να γεμίσετε περιοχή με Aspose.Drawing για .NET. Αυτός ο
  οδηγός καλύπτει server‑side image generation, δημιουργία dynamic images, και χρήση
  gradients για το γέμισμα περιοχής.
og_image_alt: Screenshot of a filled polygon region created with Aspose.Drawing in
  .NET
og_title: Πώς να γεμίσετε περιοχή στο Aspose.Drawing – Server‑Side Image Generation
schemas:
- author: Aspose
  dateModified: '2026-08-16'
  description: Learn how to fill region using Aspose.Drawing for .NET, generate dynamic
    images, and create a region from polygon with step‑by‑step code.
  headline: How to Fill Region in Aspose.Drawing
  type: TechArticle
- description: Learn how to fill region using Aspose.Drawing for .NET, generate dynamic
    images, and create a region from polygon with step‑by‑step code.
  name: How to Fill Region in Aspose.Drawing
  steps:
  - name: Create a bitmap and graphics object
    text: '`Graphics` is Aspose.Drawing’s primary drawing surface that provides methods
      for rendering shapes, text, and images onto a bitmap. We first allocate a bitmap
      that will act as our canvas and obtain a `Graphics` object to draw on it. >
      **Pro tip:** Using `Format32bppPArgb` gives you premultiplied alph'
  - name: Define a graphics path and create a region
    text: '`GraphicsPath` represents a series of connected lines and curves that can
      describe any shape. Here we add a polygon that forms a diamond‑like shape, then
      wrap it in a `Region` object. > This is the **region from polygon** you were
      looking for. The `Region` object now represents the interior of that '
  - name: Exclude an inner region
    text: '`Region.Exclude` removes the pixels of a supplied shape from the current
      region, effectively creating a “hole.” We create a rectangle and exclude it
      from the main region.'
  - name: Choose a brush and fill the region
    text: '`Brush` is the abstract base for all fill styles. In this example we use
      a solid blue brush, but you could swap in a `LinearGradientBrush` or `TextureBrush`
      to generate richer visuals.'
  - name: Save the resulting image
    text: '`Bitmap.Save` writes the image to disk in the format you specify. Adjust
      the path to point to a folder that exists on your machine.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing can be used for both personal and commercial projects.
      For licensing details, visit the [Aspose.Drawing purchase page](https://purchase.aspose.com/buy).
    question: Can I use Aspose.Drawing for commercial projects?
  - answer: Yes, you can access a free trial [Aspose.Drawing free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      to get assistance from the community and experts.
    question: How can I get support for Aspose.Drawing?
  - answer: Absolutely. Aspose.Drawing enables you to dynamically create and manipulate
      images in your .NET applications.
    question: Can I generate dynamic images using Aspose.Drawing?
  - answer: Yes, temporary licenses can be obtained [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- fill region
- Aspose.Drawing
- .NET graphics
- server‑side image generation
- dynamic image creation
title: Πώς να γεμίσετε περιοχή στο Aspose.Drawing
url: /el/net/lines-curves-and-shapes/fill-region/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να γεμίσετε περιοχή στο Aspose.Drawing

Δημιουργώντας οπτικά ελκυστικά γραφικά συχνά περιλαμβάνει **how to fill region** με χρώματα, μοτίβα ή διαβαθμίσεις. Το Aspose.Drawing για .NET σας παρέχει ένα καθαρό, υψηλής απόδοσης API για να αντιμετωπίσετε αυτήν την εργασία, είτε δημιουργείτε μηχανή αναφορών, εργαλείο σχεδίασης ή παράγετε δυναμικές εικόνες σε πραγματικό χρόνο. Σε αυτό το tutorial θα δείτε ακριβώς **how to fill region** βήμα προς βήμα, από τη ρύθμιση του bitmap μέχρι την αποθήκευση της τελικής εικόνας.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται το γέμισμα περιοχής;** Aspose.Drawing for .NET  
- **Κύρια μέθοδος;** `Graphics.FillRegion` with a `Brush` and a `Region`  
- **Μπορώ να δημιουργήσω δυναμικές εικόνες;** Yes – the same API lets you create images at runtime  
- **Χρειάζομαι άδεια για παραγωγή;** A commercial license is required; a free trial is available  
- **Υποστηριζόμενες εκδόσεις .NET;** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+

## Τι είναι το “fill region” στον προγραμματισμό γραφικών;
Το γέμισμα μιας περιοχής σημαίνει τη βαφή κάθε pixel που ανήκει σε ένα καθορισμένο σχήμα (πολύγωνο, έλλειψη ή προσαρμοσμένη διαδρομή) με μια πινέλο. Η πινέλο μπορεί να είναι ένα στερεό χρώμα, μια διαβάθμιση ή μια υφή, δίνοντάς σας πλήρη έλεγχο πάνω στην οπτική εμφάνιση της περιοχής. Το `Graphics.FillRegion` είναι η κύρια μέθοδος που εκτελεί αυτήν τη λειτουργία στο Aspose.Drawing.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για γέμισμα περιοχής;
Το Aspose.Drawing επεξεργάζεται **πάνω από 30 μορφές εικόνας** και μπορεί να αποδώσει γραφικά πολλαπλών εκατοντάδων σελίδων χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, προσφέροντας έως και 2× μεγαλύτερη απόδοση σε σχέση με το GDI+ σε τυπικό εξοπλισμό διακομιστή. Η βιβλιοθήκη λειτουργεί σταθερά σε .NET Framework, .NET Core και .NET 5/6, εξαλείφοντας τις ιδιαιτερότητες πλατφόρμας και αφαιρώντας την ανάγκη για εγγενείς εξαρτήσεις GDI+ σε servers χωρίς οθόνη.

## Προαπαιτούμενα

Πριν προχωρήσουμε, βεβαιωθείτε ότι έχετε:

1. **Aspose.Drawing Library** – κατεβάστε και εγκαταστήστε την τελευταία έκδοση από την επίσημη ιστοσελίδα. Μπορείτε να βρείτε τη βιβλιοθήκη και την τεκμηρίωσή της [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/).  
2. **Development environment** – Visual Studio (οποιαδήποτε έκδοση) ή το προτιμώμενο .NET IDE σας.  
3. **A .NET project** που στοχεύει σε .NET Framework 4.6+ ή .NET Core 3.1+.

## Εισαγωγή namespaces

Ξεκινήστε εισάγοντας τα namespaces που περιέχουν τις κλάσεις γραφικών που θα χρησιμοποιήσουμε.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Τώρα ας περάσουμε από το πλήρες παράδειγμα, χωρίζοντάς το σε εύκολα κατανοητά βήματα.

## Οδηγός βήμα‑βήμα

### Βήμα 1: Δημιουργία bitmap και αντικειμένου graphics
`Graphics` είναι η κύρια επιφάνεια σχεδίασης του Aspose.Drawing που παρέχει μεθόδους για απόδοση σχημάτων, κειμένου και εικόνων σε ένα bitmap. Πρώτα δημιουργούμε ένα bitmap που θα λειτουργήσει ως καμβάς μας και λαμβάνουμε ένα αντικείμενο `Graphics` για να σχεδιάσουμε πάνω του.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

> **Pro tip:** Η χρήση του `Format32bppPArgb` παρέχει προπολλαπλασιασμένο άλφα, το οποίο δίνει ομαλότερο μίξη όταν αργότερα εφαρμόζετε ημιδιαφανείς πινέλα.

### Βήμα 2: Ορισμός graphics path και δημιουργία περιοχής
`GraphicsPath` αντιπροσωπεύει μια σειρά συνδεδεμένων γραμμών και καμπυλών που μπορούν να περιγράψουν οποιοδήποτε σχήμα. Εδώ προσθέτουμε ένα πολύγωνο που σχηματίζει ένα σχήμα διαμαντιού και στη συνέχεια το τυλίγουμε σε ένα αντικείμενο `Region`.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

> Αυτό είναι το **region from polygon** που ψάχνατε. Το αντικείμενο `Region` τώρα αντιπροσωπεύει το εσωτερικό αυτού του πολυγώνου.

### Βήμα 3: Εξαίρεση εσωτερικής περιοχής
`Region.Exclude` αφαιρεί τα pixel ενός δοσμένου σχήματος από την τρέχουσα περιοχή, δημιουργώντας ουσιαστικά μια «τρύπα». Δημιουργούμε ένα ορθογώνιο και το εξαιρούμε από την κύρια περιοχή.

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

### Βήμα 4: Επιλογή πινέλου και γέμισμα της περιοχής
`Brush` είναι η αφηρημένη βάση για όλα τα στυλ γεμίσματος. Σε αυτό το παράδειγμα χρησιμοποιούμε ένα στερεό μπλε πινέλο, αλλά μπορείτε να το αντικαταστήσετε με ένα `LinearGradientBrush` ή `TextureBrush` για πιο πλούσια οπτικά αποτελέσματα.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

### Βήμα 5: Αποθήκευση της προκύπτουσας εικόνας
`Bitmap.Save` γράφει την εικόνα στο δίσκο στη μορφή που καθορίζετε. Προσαρμόστε τη διαδρομή ώστε να δείχνει σε έναν φάκελο που υπάρχει στον υπολογιστή σας.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

## Συχνά προβλήματα και λύσεις
| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Η εικόνα εμφανίζεται κενή** | Το bitmap δεν αποθηκεύτηκε σε φάκελο με δικαιώματα εγγραφής ή το `Graphics` δεν εκκαθαρίστηκε. | Βεβαιωθείτε ότι ο φάκελος υπάρχει και καλέστε `graphics.Dispose()` μετά το σχεδιασμό. |
| **Η περιοχή δεν εξαιρεί το εσωτερικό σχήμα** | Χρήση του `Exclude` πριν οριστεί πλήρως η περιοχή. | Καλέστε `region.Exclude(innerPath);` **μετά** τη δημιουργία της εξωτερικής περιοχής, όπως φαίνεται. |
| **Καθυστέρηση απόδοσης σε μεγάλες εικόνες** | Χρήση του `PixelFormat.Format32bppArgb` (μη προπολλαπλασιασμένο). | Αλλάξτε σε `Format32bppPArgb` για ταχύτερη αλφα-μίξη. |

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.Drawing για εμπορικά έργα;**  
A: Ναι, το Aspose.Drawing μπορεί να χρησιμοποιηθεί τόσο για προσωπικά όσο και για εμπορικά έργα. Για λεπτομέρειες αδειοδότησης, επισκεφθείτε τη [Aspose.Drawing purchase page](https://purchase.aspose.com/buy).

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
A: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή στη [Aspose.Drawing free trial page](https://releases.aspose.com/).

**Q: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Drawing;**  
A: Επισκεφθείτε το [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) για βοήθεια από την κοινότητα και τους ειδικούς.

**Q: Μπορώ να δημιουργήσω δυναμικές εικόνες χρησιμοποιώντας το Aspose.Drawing;**  
A: Απόλυτα. Το Aspose.Drawing σας επιτρέπει να δημιουργείτε και να επεξεργάζεστε δυναμικά εικόνες στις .NET εφαρμογές σας.

**Q: Υπάρχουν διαθέσιμες προσωρινές άδειες;**  
A: Ναι, οι προσωρινές άδειες μπορούν να ληφθούν από τη [temporary license page](https://purchase.aspose.com/temporary-license/).

## Συμπέρασμα

Το γέμισμα περιοχών με το Aspose.Drawing είναι μια απλή αλλά ισχυρή τεχνική που ανοίγει το δρόμο για **generate dynamic images**, δημιουργία προσαρμοσμένων σχημάτων και παραγωγή επαγγελματικών γραφικών προγραμματιστικά. Πειραματιστείτε με διαφορετικά πινέλα, διαβαθμίσεις και σύνθετες διαδρομές για να αξιοποιήσετε πλήρως τις δυνατότητες της βιβλιοθήκης.

---

**Τελευταία ενημέρωση:** 2026-08-16  
**Δοκιμάστηκε με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά μαθήματα

- [Ορισμός περιοχής αποκοπής στο Aspose.Drawing – Οδηγός .NET](/drawing/net/rendering/clipping/)
- [Πώς να σχεδιάσετε τόξα και άλλα σχήματα με το Aspose.Drawing για .NET](/drawing/net/lines-curves-and-shapes/)
- [Πώς να σχεδιάσετε ορθογώνιο – Μετασχηματισμός συστήματος συντεταγμένων (Μετασχηματισμός σελίδας) χρησιμοποιώντας το API Aspose.Drawing για .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}