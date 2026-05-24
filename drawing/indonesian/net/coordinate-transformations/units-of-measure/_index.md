---
date: 2026-05-24
description: Pelajari cara menetapkan unit di Aspose.Drawing untuk .NET, mengonversi
  unit grafik dengan mudah, dan menguasai pengukuran presisi untuk rendering grafik.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Unit Pengukuran di Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cara Menetapkan Unit di Aspose.Drawing untuk .NET – Unit Pengukuran
url: /id/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengatur Unit di Aspose.Drawing untuk .NET – Satuan Ukuran

## Pendahuluan

Selamat datang di dunia Aspose.Drawing untuk .NET, di mana presisi dan fleksibilitas bertemu dalam manipulasi grafis. Dalam tutorial ini Anda akan menemukan **cara mengatur unit** untuk gambar Anda, belajar **mengonversi unit grafis** antara poin, milimeter, dan inci, serta melihat contoh dunia nyata yang membuat gambar Anda pixel‑perfect. Baik Anda membuat laporan, thumbnail, atau diagram khusus, menguasai satuan ukuran sangat penting untuk rendering yang konsisten di semua perangkat.

## Jawaban Cepat
- **Apa cara utama untuk mengubah unit?** Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`) on the `Graphics` object.  
- **Unit mana yang sama dengan 1/72 inci?** Points.  
- **Berapa milimeter dalam satu inci?** 25.4 mm = 1 inch.  
- **Apakah saya memerlukan perpustakaan tambahan untuk menggunakan unit?** No, the Aspose.Drawing core library provides all unit constants.  
- **Bisakah saya mencampur unit dalam satu gambar?** Set the unit once per `Graphics` instance; draw everything using that unit for consistency.

## Prasyarat

Sebelum kita memulai tutorial, pastikan Anda memiliki prasyarat berikut:

- Aspose.Drawing for .NET: Pastikan Anda telah menginstal perpustakaan tersebut. Anda dapat mengunduhnya [here](https://releases.aspose.com/drawing/net/).
- Document Directory: Miliki direktori yang ditentukan tempat Anda ingin menyimpan dokumen yang dibuat.
- Basic C# Knowledge: Pemahaman dasar tentang C# disarankan untuk memanfaatkan panduan ini secara maksimal.

## Impor Namespace

Sebelum kita mulai, mari impor namespace yang diperlukan untuk menggunakan Aspose.Drawing secara efektif:

```csharp
using System.Drawing;
```

Sekarang, mari kita uraikan setiap contoh menjadi beberapa langkah:

## Cara mengatur unit ke Points?

Class `Bitmap` mewakili gambar dalam memori yang berfungsi sebagai kanvas menggambar. Muat bitmap Anda, buat objek `Graphics`, dan atur unit halaman ke points — ini memberi tahu Aspose.Drawing untuk menafsirkan semua koordinat sebagai nilai 1/72 inci. Menggunakan points memberi Anda kontrol halus untuk grafis siap cetak dan memungkinkan Anda menentukan lebar garis dengan presisi tinggi.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Langkah 1: Buat Bitmap  
Class `Bitmap` mewakili gambar dalam memori yang berfungsi sebagai kanvas menggambar.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Langkah 2: Buat Objek Graphics  
`Graphics` menyediakan metode menggambar untuk merender bentuk dan teks ke `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Langkah 3: Atur Page Unit ke Points  
`PageUnit` adalah enumerasi yang menentukan satuan ukuran untuk koordinat halaman. `PageUnit.Point` mendefinisikan points sebagai satuan ukuran (1 point = 1/72 inci). Pengaturan ini berlaku untuk semua pemanggilan menggambar berikutnya.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Langkah 4: Gambar Persegi Panjang dalam Points  
Saat Anda menggambar persegi panjang setelah mengatur unit, dimensi yang Anda tentukan ditafsirkan sebagai points, memastikan ukuran yang tepat.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Cara mengatur unit ke Millimeters?

`PageUnit` adalah enumerasi yang menentukan satuan ukuran untuk koordinat halaman. Beralih ke milimeter berguna ketika Anda memerlukan dimensi metrik, misalnya saat menghasilkan diagram teknik. Aspose.Drawing memperlakukan 1 mm sebagai 1/25.4 inci, memungkinkan Anda menyelaraskan grafis dengan ukuran fisik yang digunakan dalam manufaktur dan dokumentasi teknis.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Langkah 1: Atur Page Unit ke Millimeters  
Tetapkan `PageUnit.Millimeter` ke objek `Graphics`; semua koordinat kini berhubungan dengan sistem metrik.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Langkah 2: Gambar Persegi Panjang dalam Millimeters  
Lebar dan tinggi persegi panjang kini dinyatakan dalam milimeter, memudahkan penyelarasan dengan ukuran fisik dan memastikan output cetak sesuai dengan ukuran dunia nyata.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Cara mengatur unit ke Inches?

`Graphics` menyediakan metode menggambar untuk merender bentuk dan teks ke `Bitmap`. Inches adalah unit default untuk banyak alat desain berbasis AS. Mengatur unit ke inches memungkinkan Anda berpikir dalam istilah yang familiar saat menata elemen UI, dan mempermudah transisi dari desain layar ke cetak dimana inches umum digunakan.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Langkah 1: Atur Page Unit ke Inches  
`PageUnit.Inch` mengubah sistem koordinat sehingga 1 unit sama dengan 1 inch, memberikan cara sederhana untuk mengukur elemen dalam tata letak yang berorientasi cetak.

CODE_BLOCK_PLACEHOLDER_10_END

### Langkah 2: Gambar Persegi Panjang dalam Inches  
Sekarang setiap bentuk yang Anda gambar menggunakan inches sebagai dasar pengukuran, yang ideal untuk tata letak cetak dan untuk mengkomunikasikan dimensi kepada pemangku kepentingan yang terbiasa dengan unit imperial.

CODE_BLOCK_PLACEHOLDER_11_END

## Simpan Hasil

Setelah menyelesaikan contoh, simpan gambar hasil ke direktori dokumen Anda. Metode `Bitmap.Save` menulis file dalam format yang Anda tentukan (PNG, JPEG, dll).

CODE_BLOCK_PLACEHOLDER_12_END

Sekarang, Anda telah berhasil menjelajahi berbagai satuan ukuran dalam Aspose.Drawing untuk .NET, membuat representasi visual persegi panjang menggunakan points, millimeters, dan inches.

## Mengapa menggunakan sistem unit Aspose.Drawing?

Aspose.Drawing mendukung **lebih dari 30 format gambar** dan dapat memproses gambar hingga **5000 × 5000 piksel** tanpa memuat seluruh file ke memori, memberikan kinerja tinggi untuk pembuatan grafis skala besar. Dengan secara eksplisit mengatur unit, Anda menghilangkan tebakan, mengurangi kesalahan konversi, dan memastikan output Anda cocok dengan dimensi fisik yang tepat di semua platform.

## Masalah Umum dan Solusinya

- **Ukuran tidak terduga setelah menyimpan** – Pastikan Anda mengatur `graphics.PageUnit` **sebelum** pemanggilan menggambar apa pun; mengubah unit kemudian tidak secara retroaktif mengubah ukuran bentuk yang sudah ada.  
- **Output buram pada layar high‑DPI** – Tingkatkan resolusi bitmap (mis., `new Bitmap(width, height, 300)`) untuk menyesuaikan DPI target.  
- **Unit campuran dalam satu gambar** – Buat instance `Graphics` terpisah untuk setiap unit atau lakukan konversi manual sebelum menggambar.

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.Drawing untuk .NET dengan kerangka kerja .NET lainnya?
A1: Ya, Aspose.Drawing kompatibel dengan berbagai kerangka kerja .NET, memberikan fleksibilitas dalam lingkungan pengembangan Anda.

### Q2: Apakah tersedia trial gratis?
A2: Ya, Anda dapat menjelajahi Aspose.Drawing dengan trial gratis [here](https://releases.aspose.com/).

### Q3: Bagaimana cara mendapatkan dukungan untuk Aspose.Drawing untuk .NET?
A3: Kunjungi [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) untuk dukungan komunitas dan diskusi.

### Q4: Bisakah saya membeli lisensi sementara untuk proyek jangka pendek?
A4: Ya, Anda dapat memperoleh lisensi sementara [here](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasi detail untuk Aspose.Drawing?
A5: Dokumentasi lengkap tersedia [here](https://reference.aspose.com/drawing/net/).

---

**Terakhir Diperbarui:** 2026-05-24  
**Diuji Dengan:** Aspose.Drawing 24.11 untuk .NET  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Transformasi Sistem Koordinat – Transformasi Halaman di Aspose.Drawing untuk .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Tutorial Transformasi Matriks: Transformasi Matriks di Aspose.Drawing untuk .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Cara Menerapkan Transformasi: Transformasi Lokal di Aspose.Drawing untuk .NET](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}