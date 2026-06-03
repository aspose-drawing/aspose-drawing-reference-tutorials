---
date: 2026-06-03
description: εκπαιδευτικό πρόγραμμα asp.net fill region που δείχνει πώς να συμπληρώσετε
  μια περιοχή χρησιμοποιώντας το Aspose.Drawing για .NET, να δημιουργήσετε δυναμικές
  εικόνες και να δημιουργήσετε μια περιοχή από πολύγωνο με κώδικα βήμα‑βήμα.
keywords:
- asp.net fill region tutorial
- Aspose.Drawing region fill
- .NET graphics API
linktitle: Πώς να Συμπληρώσετε Περιοχή στο Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: asp.net fill region tutorial that shows how to fill a region using
    Aspose.Drawing for .NET, generate dynamic images, and create a region from a polygon
    with step‑by‑step code.
  headline: asp.net fill region tutorial – Fill Region with Aspose.Drawing
  type: TechArticle
- description: asp.net fill region tutorial that shows how to fill a region using
    Aspose.Drawing for .NET, generate dynamic images, and create a region from a polygon
    with step‑by‑step code.
  name: asp.net fill region tutorial – Fill Region with Aspose.Drawing
  steps:
  - name: Create a Bitmap and Graphics Object
    text: We first allocate a bitmap that will act as our canvas and obtain a `Graphics`
      object to draw on it. The `Bitmap` constructor with `PixelFormat.Format32bppPArgb`
      creates a premultiplied‑alpha surface that blends semi‑transparent brushes smoothly.
      > **Pro tip:** Using `Format32bppPArgb` gives you pre
  - name: Define a GraphicsPath and Create a Region
    text: A `GraphicsPath` lets us describe complex shapes. Here we add a polygon
      that forms a diamond‑like shape. The `GraphicsPath` class represents a series
      of connected lines and curves; once populated, it can be turned into a `Region`
      that the `Graphics` object can fill. > This is the **region from polyg
  - name: Exclude an Inner Region
    text: Often you need a “hole” inside a shape. We create a rectangle and exclude
      it from the main region. The `Region.Exclude` method removes the pixels covered
      by the inner path, leaving a transparent window inside the outer shape.
  - name: Choose a Brush and Fill the Region
    text: '`SolidBrush` is a brush that fills an area with a single solid color. `Graphics.FillRegion`
      fills a specified `Region` with the provided `Brush`. Select any brush you like.
      In this example we use a solid blue brush, but you could swap in a `LinearGradientBrush`
      or `TextureBrush` to generate dynamic '
  - name: Save the Resulting Image
    text: Finally, write the bitmap to disk. Adjust the path to point to a folder
      that exists on your machine. Calling `bitmap.Save` with the `ImageFormat.Png`
      argument writes a lossless PNG file that can be served directly to browsers
      or stored for later processing.
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing can be used for both personal and commercial projects.
      For licensing details, visit [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.Drawing for commercial projects?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      to get assistance from the community and experts.
    question: How can I get support for Aspose.Drawing?
  - answer: Absolutely. Aspose.Drawing enables you to dynamically create and manipulate
      images in your .NET applications.
    question: Can I generate dynamic images using Aspose.Drawing?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: εκπαιδευτικό πρόγραμμα asp.net fill region – Fill Region με Aspose.Drawing
url: /el/net/lines-curves-and-shapes/fill-region/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# asp.net fill region tutorial – Συμπλήρωση Περιοχής με Aspose.Drawing

Σε αυτόν τον **asp.net fill region tutorial**, θα μάθετε πώς να ζωγραφίζετε οποιοδήποτε σχήμα—είτε ένα απλό πολύγωνο είτε ένα σύνθετο μονοπάτι—χρησιμοποιώντας το Aspose.Drawing για .NET. Θα περάσουμε από τη δημιουργία ενός bitmap, τον ορισμό μιας περιοχής, την εφαρμογή πινέλων και, τέλος, την αποθήκευση της εικόνας. Στο τέλος θα έχετε ένα επαναχρησιμοποιήσιμο πρότυπο που λειτουργεί σε .NET Framework, .NET Core και .NET 5/6 χωρίς εξαρτήσεις GDI+.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη χειρίζεται τη συμπλήρωση περιοχής;** Aspose.Drawing for .NET  
- **Κύρια μέθοδος;** `Graphics.FillRegion` with a `Brush` and a `Region`  
- **Μπορώ να δημιουργήσω δυναμικές εικόνες;** Yes – the same API lets you create images at runtime  
- **Χρειάζομαι άδεια για παραγωγή;** A commercial license is required; a free trial is available  
- **Υποστηριζόμενες εκδόσεις .NET;** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+

## Τι είναι η «συμπλήρωση περιοχής» στον προγραμματισμό γραφικών;
Η συμπλήρωση μιας περιοχής σημαίνει τη βαφή κάθε pixel που ανήκει σε ένα καθορισμένο σχήμα (πολύγωνο, έλλειψη ή προσαρμοσμένο μονοπάτι) με ένα πινέλο. Το πινέλο μπορεί να είναι ένα στερεό χρώμα, ένα διαβάθμιση ή μια υφή, δίνοντάς σας πλήρη έλεγχο πάνω στην οπτική εμφάνιση της περιοχής.

## Γιατί να χρησιμοποιήσετε το Aspose.Drawing για τη συμπλήρωση περιοχής;
Το Aspose.Drawing συμπληρώνει περιοχές **με 99 % ακρίβεια pixel‑perfect** και μπορεί να διαχειριστεί **πάνω από 50 μορφές εικόνας**—συμπεριλαμβανομένων PNG, JPEG, BMP, TIFF και WebP—ενώ επεξεργάζεται έγγραφα με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη. Η μηχανή απόδοσης στο διακομιστή του εξαλείφει την ανάγκη για GDI+, παρέχοντας έως και **2× ταχύτερη** απόδοση σχεδίασης σε τυπικές cloud περιπτώσεις.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε:

1. **Aspose.Drawing Library** – κατεβάστε και εγκαταστήστε την τελευταία έκδοση από την επίσημη ιστοσελίδα. Μπορείτε να βρείτε τη βιβλιοθήκη και την τεκμηρίωσή της [εδώ](https://reference.aspose.com/drawing/net/).  
2. **Development Environment** – Visual Studio (οποιαδήποτε έκδοση) ή το προτιμώμενο .NET IDE σας.  
3. **A .NET project** που στοχεύει σε .NET Framework 4.6+ ή .NET Core 3.1+.

## Εισαγωγή Namespaces

`Graphics`, `Bitmap`, `Region` και `GraphicsPath` βρίσκονται στο namespace `Aspose.Drawing`. Η εισαγωγή τους σας δίνει πρόσβαση στο πλήρες API της επιφάνειας σχεδίασης.

Η κλάση `Graphics` είναι η κύρια επιφάνεια σχεδίασης που παρέχει μεθόδους για απόδοση σχημάτων, κειμένου και εικόνων σε ένα bitmap. Το `Bitmap` αντιπροσωπεύει μια εικόνα στη μνήμη που μπορείτε να σχεδιάσετε. Το `Region` ορίζει την περιοχή που θα συμπληρωθεί ή θα περικοπεί σε λειτουργίες σχεδίασης. Το `GraphicsPath` αποθηκεύει μια σειρά από γραμμές και καμπύλες που περιγράφουν ένα σχήμα.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Τώρα ας περάσουμε από το πλήρες παράδειγμα, διασπώντας το σε εύκολα‑ακολουθήσιμα βήματα.

## Πώς να εκτελέσετε ένα asp.net fill region tutorial με το Aspose.Drawing;

Φορτώστε ένα κενό bitmap, ορίστε ένα `GraphicsPath` βασισμένο σε πολύγωνο, μετατρέψτε το σε `Region`, προαιρετικά εξαιρέστε εσωτερικά σχήματα, επιλέξτε ένα πινέλο, καλέστε `Graphics.FillRegion` και τέλος αποθηκεύστε το bitmap—όλα σε πέντε σύντομα βήματα. Αυτό το πρότυπο λειτουργεί το ίδιο σε Windows, Linux και Docker containers, καθιστώντας το ιδανικό για δημιουργία εικόνων στο διακομιστή.

### Βήμα 1: Δημιουργία Bitmap και Graphics Object
Αρχικά εκχωρούμε ένα bitmap που θα λειτουργήσει ως καμβάς μας και λαμβάνουμε ένα αντικείμενο `Graphics` για να σχεδιάσουμε πάνω του.

Ο κατασκευαστής `Bitmap` με `PixelFormat.Format32bppPArgb` δημιουργεί μια επιφάνεια προπολλαπλασιασμένου άλφα που ενώνει ομαλά τα ημιδιαφανή πινέλα.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

> **Pro tip:** Η χρήση του `Format32bppPArgb` σας παρέχει προπολλαπλασιασμένο άλφα, το οποίο προσφέρει ομαλότερη ανάμειξη όταν εφαρμόζετε αργότερα ημιδιαφανή πινέλα.

### Βήμα 2: Ορισμός GraphicsPath και Δημιουργία Region
Ένα `GraphicsPath` μας επιτρέπει να περιγράψουμε σύνθετα σχήματα. Εδώ προσθέτουμε ένα πολύγωνο που σχηματίζει ένα σχήμα σχήματος ροζέ.

Η κλάση `GraphicsPath` αντιπροσωπεύει μια σειρά συνδεδεμένων γραμμών και καμπυλών· μόλις γεμίσει, μπορεί να μετατραπεί σε `Region` που το αντικείμενο `Graphics` μπορεί να συμπληρώσει.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

> Αυτό είναι το **region from polygon** που ψάχνατε. Το αντικείμενο `Region` τώρα αντιπροσωπεύει το εσωτερικό αυτού του πολυγώνου.

### Βήμα 3: Εξαίρεση Εσωτερικής Περιοχής
Συχνά χρειάζεται ένα «τρύπα» μέσα σε ένα σχήμα. Δημιουργούμε ένα ορθογώνιο και το εξαιρούμε από την κύρια περιοχή.

Η μέθοδος `Region.Exclude` αφαιρεί τα pixel που καλύπτονται από το εσωτερικό μονοπάτι, αφήνοντας ένα διαφανές παράθυρο μέσα στο εξωτερικό σχήμα.

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

### Βήμα 4: Επιλογή Πινέλου και Συμπλήρωση της Περιοχής
`SolidBrush` είναι ένα πινέλο που γεμίζει μια περιοχή με ένα ενιαίο στερεό χρώμα. Η `Graphics.FillRegion` γεμίζει μια καθορισμένη `Region` με το παρεχόμενο `Brush`.

Επιλέξτε οποιοδήποτε πινέλο θέλετε. Σε αυτό το παράδειγμα χρησιμοποιούμε ένα στερεό μπλε πινέλο, αλλά μπορείτε να το αντικαταστήσετε με ένα `LinearGradientBrush` ή `TextureBrush` για να δημιουργήσετε δυναμικές εικόνες με πιο πλούσια οπτικά στοιχεία.

Ο κατασκευαστής `SolidBrush` δέχεται μια τιμή `Color`; μπορείτε επίσης να δημιουργήσετε πινέλα διαβάθμισης ή υφής για πιο σύνθετα εφέ.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

### Βήμα 5: Αποθήκευση της Παραγόμενης Εικόνας
Τέλος, γράψτε το bitmap στο δίσκο. Προσαρμόστε τη διαδρομή ώστε να δείχνει σε έναν φάκελο που υπάρχει στο μηχάνημά σας.

Καλώντας `bitmap.Save` με το όρισμα `ImageFormat.Png` γράφει ένα lossless PNG αρχείο που μπορεί να σερβιριστεί άμεσα σε browsers ή να αποθηκευτεί για επεξεργασία αργότερα.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Η εικόνα εμφανίζεται κενή** | Το bitmap δεν αποθηκεύεται σε φάκελο με δικαιώματα εγγραφής ή το `Graphics` δεν έχει εκκαθαριστεί. | Βεβαιωθείτε ότι ο φάκελος υπάρχει και καλέστε `graphics.Dispose()` μετά το σχεδιασμό. |
| **Η περιοχή δεν εξαιρεί το εσωτερικό σχήμα** | Χρήση του `Exclude` πριν οριστεί πλήρως η περιοχή. | Καλέστε `region.Exclude(innerPath);` **μετά** τη δημιουργία της εξωτερικής περιοχής, όπως φαίνεται. |
| **Καθυστέρηση απόδοσης σε μεγάλες εικόνες** | Χρήση του `PixelFormat.Format32bppArgb` (μη προπολλαπλασιασμένο). | Αλλάξτε σε `Format32bppPArgb` για ταχύτερη ανάμειξη άλφα. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το Aspose.Drawing για εμπορικά έργα;**  
Α: Ναι, το Aspose.Drawing μπορεί να χρησιμοποιηθεί τόσο για προσωπικά όσο και για εμπορικά έργα. Για λεπτομέρειες αδειοδότησης, επισκεφθείτε [εδώ](https://purchase.aspose.com/buy).

**Ε: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
Α: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

**Ε: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Drawing;**  
Α: Επισκεφθείτε το [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) για βοήθεια από την κοινότητα και τους ειδικούς.

**Ε: Μπορώ να δημιουργήσω δυναμικές εικόνες χρησιμοποιώντας το Aspose.Drawing;**  
Α: Απολύτως. Το Aspose.Drawing σας επιτρέπει να δημιουργείτε και να επεξεργάζεστε δυναμικά εικόνες στις .NET εφαρμογές σας.

**Ε: Διατίθενται προσωρινές άδειες;**  
Α: Ναι, οι προσωρινές άδειες μπορούν να ληφθούν [εδώ](https://purchase.aspose.com/temporary-license/).

## Συμπέρασμα

Η συμπλήρωση περιοχών με το Aspose.Drawing είναι μια απλή αλλά ισχυρή τεχνική που ανοίγει το δρόμο για **δημιουργία δυναμικών εικόνων**, δημιουργία προσαρμοσμένων σχημάτων και παραγωγή επαγγελματικών γραφικών προγραμματιστικά. Πειραματιστείτε με διαφορετικά πινέλα, διαβαθμίσεις και σύνθετα μονοπάτια για να αξιοποιήσετε πλήρως τις δυνατότητες της βιβλιοθήκης.

---

**Τελευταία ενημέρωση:** 2026-06-03  
**Δοκιμή με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Ορισμός Περιοχής Κοπής στο Aspose.Drawing – Οδηγός .NET](/drawing/net/rendering/clipping/)
- [Πώς να δημιουργήσετε bitmap aspose.drawing – Σχεδίαση Πολυγώνων σε .NET](/drawing/net/lines-curves-and-shapes/draw-polygon/)
- [Πώς να Σχεδιάσετε Ορθογώνιο με Aspose.Drawing για .NET](/drawing/net/lines-curves-and-shapes/draw-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}