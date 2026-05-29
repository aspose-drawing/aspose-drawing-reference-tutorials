---
date: 2026-05-29
description: Μάθετε πώς να ορίσετε την άδεια Aspose.Drawing σε .NET και να αφαιρέσετε
  το υδατογράφημα Aspose. Κατακτήστε τις μεθόδους αδειοδότησης για να ξεκλειδώσετε
  όλες τις δυνατότητες χωρίς υδατογραφήματα.
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
linktitle: Αδειοδότηση στο Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  headline: Remove Aspose Watermark – Set Aspose.Drawing License
  type: TechArticle
- description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  name: Remove Aspose Watermark – Set Aspose.Drawing License
  steps:
  - name: Confirm Success
    text: '> **Pro tip:** Place the `.lic` file in the same folder as your executable
      or provide an absolute path to avoid “file not found” errors.'
  - name: Confirm Success
    text: '> **Warning:** Remember to dispose the `FileStream` (or use a `using` block)
      to free file handles.'
  - name: Display the Consumption Details
    text: '> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will
      fall back to trial mode and you’ll see watermarks in the output.'
  type: HowTo
- questions:
  - answer: Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.
    question: What is the primary way to activate Aspose.Drawing?
  - answer: Yes, you can load the license from a `Stream` for dynamic scenarios.
    question: Can I apply a license at runtime?
  - answer: Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable
      consumption‑based billing.
    question: Is a metered license supported?
  - answer: A trial works for testing, but a valid license removes watermarks and
      unlocks all APIs.
    question: Do I need a license for development builds?
  - answer: Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.
    question: Which .NET versions are compatible?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Αφαίρεση Υδατογραφήματος Aspose – Ορισμός Άδειας Aspose.Drawing
url: /el/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός Άδειας Aspose.Drawing

## Εισαγωγή

Αν δημιουργείτε εφαρμογές .NET που βασίζονται σε ισχυρά γραφικά και επεξεργασία εικόνων, **η ρύθμιση μιας άδειας Aspose.Drawing** είναι το πρώτο βήμα για την αφαίρεση του υδατογραφήματος Aspose και την πρόσβαση στο πλήρες σύνολο λειτουργιών. Σε αυτό το tutorial θα μάθετε τρεις πρακτικούς τρόπους για να ορίσετε την άδεια Aspose.Drawing — φόρτωση από αρχείο, φόρτωση από ροή και χρήση του μοντέλου χρέωσης ανά χρήση — ώστε να ενσωματώσετε τη βιβλιοθήκη με σιγουριά και να διατηρήσετε το αποτέλεσμα σας καθαρό.

## Γρήγορες Απαντήσεις
- **Ποιος είναι ο κύριος τρόπος ενεργοποίησης του Aspose.Drawing;** Φορτώστε ένα αρχείο άδειας χρησιμοποιώντας `License.SetLicense("Aspose.Drawing.lic")`.  
- **Μπορώ να εφαρμόσω άδεια κατά την εκτέλεση;** Ναι, μπορείτε να φορτώσετε την άδεια από ένα `Stream` για δυναμικά σενάρια.  
- **Υποστηρίζεται άδεια χρέωσης ανά χρήση;** Απόλυτα· χρησιμοποιήστε `Metered.SetMeteredKey(publicKey, privateKey)` για να ενεργοποιήσετε τη χρέωση βάσει κατανάλωσης.  
- **Χρειάζομαι άδεια για εκδόσεις ανάπτυξης;** Η δοκιμαστική έκδοση λειτουργεί για δοκιμές, αλλά μια έγκυρη άδεια αφαιρεί τα υδατογραφήματα και ξεκλειδώνει όλες τις API.  
- **Ποιες εκδόσεις .NET είναι συμβατές;** Το Aspose.Drawing υποστηρίζει .NET Framework 4.x, .NET Core 3.1+ και .NET 5/6+.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Aspose.Drawing Library** – κατεβάστε το τελευταίο πακέτο από [here](https://releases.aspose.com/drawing/net/).  
- **License File** – αποκτήστε ένα έγκυρο αρχείο `.lic` από [Aspose](https://purchase.aspose.com/buy).  
- **.NET Development Environment** – Visual Studio, Rider ή οποιοδήποτε IDE που στοχεύει σε .NET Framework/.NET Core.

## Εισαγωγή Χώρων Ονομάτων

Χρειαζόμαστε τους τυπικούς χώρους ονομάτων .NET καθώς και τον χώρο ονομάτων Aspose.Drawing για την άδεια. Προσθέστε τις ακόλουθες δηλώσεις `using` στην αρχή του αρχείου C# σας:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Πώς να Φορτώσετε Άδεια από Αρχείο;

Η κλάση `License` αντιπροσωπεύει το στοιχείο αδειοδότησης του Aspose.Drawing που, όταν δημιουργείται, σας επιτρέπει να εφαρμόσετε μια άδεια στη βιβλιοθήκη. Η φόρτωση μιας άδειας από αρχείο είναι η πιο απλή προσέγγιση· απλώς κατευθύνετε τη μέθοδο `SetLicense` σε ένα αρχείο `.lic` και η βιβλιοθήκη αφαιρεί όλα τα υδατογραφήματα δοκιμής για το υπόλοιπο της συνεδρίας της εφαρμογής. Αυτή η μέθοδος λειτουργεί τόσο σε περιβάλλοντα επιφάνειας εργασίας όσο και σε διακομιστές και δεν απαιτεί πρόσθετη διαμόρφωση πέραν του να εξασφαλιστεί ότι το αρχείο είναι προσβάσιμο κατά την εκτέλεση.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## Πώς να Φορτώσετε Άδεια από Ροή;

Όταν το αρχείο άδειας είναι ενσωματωμένο ως πόρος ή λαμβάνεται μέσω δικτύου, η φόρτωσή του από ένα `Stream` σας προσφέρει ευελιξία ενώ εξακολουθεί να εγγυάται την αφαίρεση του υδατογραφήματος. Με τη μεταβίβαση ενός αντικειμένου `Stream` στη μέθοδο `SetLicense`, διατηρείτε την άδεια εκτός του φακέλου ανάπτυξης, κάτι που μπορεί να βελτιώσει την ασφάλεια και να απλοποιήσει τη διανομή σε περιβάλλοντα κοντέινερ ή σύννεφο. Η διαδικασία είναι ίδια με τη φόρτωση από αρχείο, εκτός από το ότι διαχειρίζεστε εσείς τον κύκλο ζωής του ρεύματος.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## Πώς να Ενεργοποιήσετε Άδεια Χρέωσης ανά Χρήση;

Η κλάση `Metered` διαχειρίζεται την ενεργοποίηση χρέωσης ανά χρήση για το Aspose.Drawing, επιτρέποντας τη χρέωση βάσει κατανάλωσης. Η άδεια χρέωσης ανά χρήση σας επιτρέπει να πληρώνετε μόνο για τις λειτουργίες που πραγματικά εκτελείτε, κάτι που είναι ιδανικό για σενάρια SaaS ή πληρωμής ανά χρήση. Αφού παρέχετε τα δημόσια και ιδιωτικά κλειδιά, κάθε κλήση επεξεργασίας εικόνας παρακολουθείται και χρεώνεται αυτόματα, και η βιβλιοθήκη λειτουργεί σε πλήρη λειτουργικότητα χωρίς υδατογραφήματα για τη διάρκεια της συνεδρίας.

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## Γιατί να Ορίσετε Σωστά την Άδεια Aspose.Drawing;

Η σωστή ρύθμιση της άδειας εξασφαλίζει ότι η βιβλιοθήκη λειτουργεί σε πλήρη λειτουργικότητα, αφαιρεί τα υδατογραφήματα δοκιμής και συμμορφώνεται με τους όρους αδειοδότησης της Aspose. Μια σωστά εφαρμοσμένη άδεια ενεργοποιεί επίσης premium APIs, βελτιώνει την απόδοση απενεργοποιώντας τους ελέγχους αξιολόγησης, και σας επιτρέπει να χρησιμοποιήσετε χρέωση ανά χρήση εάν το επιθυμείτε. Η αποτυχία φόρτωσης της άδειας πριν από την πρώτη κλήση API θα κάνει τη βιβλιοθήκη να επιστρέψει σε λειτουργία δοκιμής, με αποτέλεσμα υδατογραφήματα σε όλες τις παραγόμενες εικόνες.

- **Αφαιρεί τα υδατογραφήματα** που εμφανίζονται σε λειτουργία δοκιμής.  
- **Ξεκλειδώνει premium APIs** όπως προχωρημένα φίλτρα εικόνας και μετατροπή PDF.  
- **Εξασφαλίζει τη συμμόρφωση** με τους όρους αδειοδότησης της Aspose για εμπορική διανομή.  
- **Ενεργοποιεί χρέωση ανά χρήση**, επιτρέποντάς σας να πληρώνετε μόνο για ό,τι χρησιμοποιείτε.  

Το Aspose.Drawing υποστηρίζει **πάνω από 30 μορφές εικόνας** (συμπεριλαμβανομένων PNG, JPEG, BMP, TIFF και WebP) και μπορεί να επεξεργαστεί **PDF έγγραφα με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη**, παρέχοντας υψηλής απόδοσης μετατροπή σε μέτριο υλικό.

## Φόρτωση Άδειας από Αρχείο

Η φόρτωση μιας άδειας από αρχείο είναι η πιο απλή προσέγγιση. Ακολουθήστε αυτά τα τρία βήματα:

### Βήμα 1: Αρχικοποίηση του Αντικειμένου License

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Βήμα 2: Ορισμός της Άδειας από το Αρχείο `.lic`

```csharp
Console.WriteLine("License set successfully.");
```

### Βήμα 3: Επιβεβαίωση Επιτυχίας

```csharp
Console.WriteLine("License set successfully.");
```

> **Συμβουλή:** Τοποθετήστε το αρχείο `.lic` στον ίδιο φάκελο με το εκτελέσιμο σας ή δώστε απόλυτη διαδρομή για να αποφύγετε σφάλματα «αρχείο δεν βρέθηκε».

## Φόρτωση Άδειας από Ροή

Όταν το αρχείο άδειας είναι ενσωματωμένο ως πόρος ή λαμβάνεται από απομακρυσμένη τοποθεσία, η φόρτωσή του από ένα `Stream` σας προσφέρει ευελιξία.

### Βήμα 1: Αρχικοποίηση του Αντικειμένου License

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Βήμα 2: Φόρτωση της Άδειας Χρησιμοποιώντας `FileStream`

```csharp
Console.WriteLine("License set successfully.");
```

### Βήμα 3: Επιβεβαίωση Επιτυχίας

```csharp
Console.WriteLine("License set successfully.");
```

> **Προειδοποίηση:** Θυμηθείτε να απελευθερώσετε το `FileStream` (ή χρησιμοποιήστε ένα μπλοκ `using`) για να ελευθερώσετε τους χειριστές αρχείων.

## Χρήση Άδειας Χρέωσης ανά Χρήση

Η άδεια χρέωσης ανά χρήση είναι ιδανική για σενάρια SaaS ή πληρωμής ανά χρήση. Παρακολουθεί την κατανάλωση και σας χρεώνει βάσει της πραγματικής χρήσης.

### Βήμα 1: Αρχικοποίηση του Αντικειμένου Metered

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Βήμα 2: Ορισμός Δημόσιου και Ιδιωτικού Κλειδιού

```csharp
// Your image processing logic here
```

### Βήμα 3: Εκτελέστε την Επεξεργασία Εικόνας

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Βήμα 4: Ανάκτηση Πληροφοριών Κατανάλωσης

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### Βήμα 5: Εμφάνιση των Λεπτομερειών Κατανάλωσης

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Συνηθισμένο λάθος:** Εάν ξεχάσετε να καλέσετε το `SetMeteredKey`, το API θα επιστρέψει σε λειτουργία δοκιμής και θα δείτε υδατογραφήματα στο αποτέλεσμα.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| “License file not found” error | Λάθος διαδρομή ή έλλειψη αρχείου στο φάκελο εξόδου | Χρησιμοποιήστε απόλυτη διαδρομή ή ορίστε την ιδιότητα *Copy to Output Directory* του αρχείου σε *Copy always*. |
| Watermark still appears after setting license | Η άδεια δεν φορτώθηκε πριν από την πρώτη κλήση API | Φορτώστε την άδεια **πριν** από οποιαδήποτε λειτουργία Aspose.Drawing. |
| Metered consumption always zero | Τα κλειδιά δεν έχουν οριστεί ή είναι λανθασμένες μεταβλητές περιβάλλοντος | Επαληθεύστε τα δημόσια/ιδιωτικά κλειδιά και εξασφαλίστε σύνδεση στο διαδίκτυο για τον διακομιστή χρέωσης ανά χρήση της Aspose. |

## Συχνές Ερωτήσεις

**Q1: Μπορώ να χρησιμοποιήσω το Aspose.Drawing χωρίς άδεια;**  
A1: Ναι, μια δοκιμαστική άδεια λειτουργεί για ανάπτυξη και αξιολόγηση, αλλά προσθέτει υδατογραφήματα και περιορίζει ορισμένες λειτουργίες.

**Q2: Πόσο συχνά πρέπει να ανανεώνω την άδεια Aspose.Drawing;**  
A2: Οι άδειες είναι διαρκείς για την αγορασμένη έκδοση. Η ανανέωση απαιτείται μόνο για υποστήριξη και ενημερώσεις.

**Q3: Τι είναι η άδεια χρέωσης ανά χρήση και πότε πρέπει να τη χρησιμοποιήσω;**  
A3: Η άδεια χρέωσης ανά χρήση χρεώνει βάσει της χρήσης (λειτουργίες ή επεξεργασμένα δεδομένα). Είναι ιδανική για υπηρεσίες cloud ή μοντέλα πληρωμής ανά χρήση.

**Q4: Μπορώ να χρησιμοποιήσω το Aspose.Drawing σε εμπορικά έργα;**  
A4: Απόλυτα—αφού έχετε μια έγκυρη άδεια, μπορείτε να ενσωματώσετε το Aspose.Drawing σε οποιαδήποτε εμπορική εφαρμογή.

**Q5: Πού μπορώ να βρω υποστήριξη κοινότητας για το Aspose.Drawing;**  
A5: Επισκεφθείτε το [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) για βοήθεια από την κοινότητα, παραδείγματα και συζητήσεις.

## Συμπέρασμα

Η κατανόηση του πώς να **ορίσετε την άδεια Aspose.Drawing**—είτε από αρχείο, ροή ή μέσω χρέωσης ανά χρήση—σας εξασφαλίζει ότι αξιοποιείτε στο έπακρο αυτή τη δυνατή βιβλιοθήκη γραφικών .NET, αφαιρώντας πλήρως το **υδατογράφημα Aspose**. Ακολουθήστε τα παραπάνω βήματα, προσέξτε τα κοινά λάθη, και θα είστε έτοιμοι να δημιουργήσετε ισχυρές λύσεις επεξεργασίας εικόνας χωρίς εμπόδια αδειοδότησης.

---

**Τελευταία Ενημέρωση:** 2026-05-29  
**Δοκιμάστηκε Με:** Aspose.Drawing 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Πώς να Αδειοδοτήσετε το Aspose.Drawing για .NET – πώς να αδειοδοτήσετε aspose.drawing](/drawing/net/licensing/)
- [Πώς να Κλιμακώσετε Εικόνες με το Aspose.Drawing για .NET](/drawing/net/image-editing/scale/)
- [Πώς να Σχεδιάσετε Κείμενο και Γραμματοσειρές με το Aspose.Drawing για .NET](/drawing/net/text-and-fonts/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}