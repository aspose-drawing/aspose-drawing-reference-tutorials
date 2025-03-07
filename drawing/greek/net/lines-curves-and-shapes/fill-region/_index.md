---
title: Συμπλήρωση περιοχών στο Aspose.Drawing
linktitle: Συμπλήρωση περιοχών στο Aspose.Drawing
second_title: Aspose.Drawing .NET API - Εναλλακτική λύση στο System.Drawing.Common
description: Μάθετε πώς να γεμίζετε περιοχές στο Aspose.Drawing για .NET με αυτόν τον αναλυτικό οδηγό. Βελτιώστε τις δεξιότητές σας στο γραφικό σχεδιασμό χωρίς κόπο.
weight: 20
url: /el/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Συμπλήρωση περιοχών στο Aspose.Drawing

## Εισαγωγή

Η δημιουργία οπτικά ελκυστικών γραφικών συχνά περιλαμβάνει γέμισμα περιοχών με χρώματα, μοτίβα ή διαβαθμίσεις. Το Aspose.Drawing για .NET παρέχει ισχυρά εργαλεία για να επιτευχθεί αυτό αποτελεσματικά. Σε αυτό το σεμινάριο, θα εμβαθύνουμε στη διαδικασία πλήρωσης περιοχών χρησιμοποιώντας το Aspose.Drawing, μια ευέλικτη βιβλιοθήκη που απλοποιεί τις λειτουργίες γραφικών σε εφαρμογές .NET.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

1.  Aspose.Drawing Library: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης Aspose.Drawing. Μπορείτε να βρείτε τη βιβλιοθήκη και την τεκμηρίωσή της[εδώ](https://reference.aspose.com/drawing/net/).

2. Περιβάλλον ανάπτυξης: Ρυθμίστε ένα περιβάλλον ανάπτυξης .NET, όπως το Visual Studio, για να ενσωματώσετε το Aspose.Drawing στα έργα σας.

## Εισαγωγή χώρων ονομάτων

Ξεκινήστε εισάγοντας τους απαραίτητους χώρους ονομάτων στο έργο σας. Αυτοί οι χώροι ονομάτων παρέχουν πρόσβαση στις κλάσεις και τις μεθόδους που απαιτούνται για την εργασία με το Aspose.Drawing.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


Τώρα, ας αναλύσουμε τον κώδικα του παραδείγματος σε πολλά βήματα για μια σαφή και ολοκληρωμένη κατανόηση.

## Βήμα 1: Δημιουργήστε ένα αντικείμενο Bitmap και Graphics

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Σε αυτό το βήμα, αρχικοποιούμε ένα νέο bitmap και ένα αντικείμενο γραφικών για να το σχεδιάσουμε.

## Βήμα 2: Ορίστε ένα GraphicsPath και δημιουργήστε μια περιοχή

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

Καθορίστε μια διαδρομή γραφικών προσδιορίζοντας ένα πολύγωνο με ένα σύνολο σημείων. Δημιουργήστε μια περιοχή χρησιμοποιώντας αυτήν τη διαδρομή.

## Βήμα 3: Εξαιρέστε μια εσωτερική περιοχή

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

Δημιουργήστε μια άλλη διαδρομή γραφικών που αντιπροσωπεύει ένα εσωτερικό ορθογώνιο και αποκλείστε το από την κύρια περιοχή.

## Βήμα 4: Επιλέξτε μια βούρτσα και γεμίστε την περιοχή

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

Επιλέξτε ένα πινέλο (σε αυτή την περίπτωση, ένα σταθερό μπλε χρώμα) και γεμίστε την περιοχή που καθορίσατε προηγουμένως με την επιλεγμένη βούρτσα.

## Βήμα 5: Αποθηκεύστε την εικόνα που προκύπτει

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

Αποθηκεύστε την τελική εικόνα στον επιθυμητό κατάλογο.

## συμπέρασμα

Η συμπλήρωση περιοχών στο Aspose.Drawing για .NET είναι μια απλή διαδικασία, η οποία σας παρέχει την ευελιξία να δημιουργήσετε πολύπλοκα και οπτικά ελκυστικά γραφικά. Πειραματιστείτε με διαφορετικά σχήματα, χρώματα και μοτίβα για να απελευθερώσετε τη δημιουργικότητά σας.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.Drawing για εμπορικά έργα;

 A1: Ναι, το Aspose.Drawing μπορεί να χρησιμοποιηθεί τόσο για προσωπικά όσο και για εμπορικά έργα. Για λεπτομέρειες αδειοδότησης, επισκεφθείτε[εδώ](https://purchase.aspose.com/buy).

### Ε2: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

 A2: Ναι, μπορείτε να έχετε πρόσβαση σε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Drawing;

 A3: Επισκεφθείτε το[Aspose.Φόρουμ σχεδίασης](https://forum.aspose.com/c/diagram/17) να λάβετε βοήθεια από την κοινότητα και τους ειδικούς.

### Ε4: Μπορώ να δημιουργήσω δυναμικές εικόνες χρησιμοποιώντας το Aspose.Drawing;

Α4: Απολύτως. Το Aspose.Drawing σάς δίνει τη δυνατότητα να δημιουργείτε και να χειρίζεστε δυναμικά εικόνες στις εφαρμογές σας .NET.

### Ε5: Είναι διαθέσιμες προσωρινές άδειες;

 A5: Ναι, μπορούν να ληφθούν προσωρινές άδειες[εδώ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
