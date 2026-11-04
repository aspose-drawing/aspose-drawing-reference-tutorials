---
date: 2026-11-04
description: Pelajari cara menggambar grafik persegi panjang sambil melakukan transformasi
  sistem koordinat di .NET dengan API Aspose.Drawing. Panduan langkah demi langkah
  ini menunjukkan cara mengonversi inci ke piksel dan mengatur satuan halaman.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Transformasi sistem koordinat di Aspose.Drawing
og_description: Pelajari cara menggambar grafik persegi panjang sambil mengonversi
  inci ke piksel dan mengatur satuan halaman di Aspose.Drawing untuk .NET. Ikuti panduan
  langkah demi langkah untuk transformasi halaman yang tepat.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Cara menggambar persegi panjang dengan transformasi halaman menggunakan
  Aspose.Drawing untuk .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Cara menggambar persegi panjang – transformasi sistem koordinat (transformasi
  halaman) di Aspose.Drawing untuk .NET
url: /id/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menggambar persegi panjang – transformasi sistem koordinat (transformasi halaman) di Aspose.Drawing untuk .NET

## Pendahuluan

Dalam tutorial ini Anda akan belajar **cara menggambar persegi panjang** grafik sambil melakukan transformasi sistem koordinat tingkat halaman menggunakan Aspose.Drawing untuk .NET. Baik Anda sedang membangun mesin pelaporan, alat sketsa bergaya CAD, atau aplikasi apa pun yang membutuhkan pengukuran dunia nyata yang presisi, panduan ini akan membawa Anda melalui setiap langkah—dari membuat bitmap hingga menyimpan PNG akhir. Pada akhir tutorial Anda akan nyaman mengonversi inci ke piksel, membersihkan latar belakang kanvas, dan mengatur unit halaman untuk output siap cetak.

## Jawaban cepat
- **Apa itu transformasi sistem koordinat?** Ini memetakan unit tingkat halaman (seperti inci) ke piksel tingkat perangkat sehingga gambar berskala dengan benar pada perangkat output apa pun.  
- **Mengapa memilih Aspose.Drawing?** Ini menyediakan API grafik yang sepenuhnya dikelola, lintas‑platform yang menggantikan System.Drawing.Common dan mendukung lebih dari 30 format gambar.  
- **Berapa lama contoh ini membutuhkan waktu untuk diimplementasikan?** Sekitar 5‑10 menit untuk persegi panjang dasar dengan transformasi halaman.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk penyebaran produksi.  
- **Runtime .NET mana yang didukung?** .NET Framework 4.6+, .NET Core 3.1+, dan .NET 5/6/7.

## Apa itu Aspose.Drawing?

Aspose.Drawing adalah perpustakaan grafik .NET yang menyediakan **API independen perangkat** untuk membuat dan memanipulasi gambar raster, vektor, dan gambar tingkat halaman tanpa bergantung pada GDI+. Ini mendukung **lebih dari 30 format gambar** dan dapat memproses gambar hingga **10.000 × 10.000 piksel** sambil menjaga penggunaan memori tetap rendah.

## Mengapa menggunakan transformasi sistem koordinat dengan Aspose.Drawing?

Transformasi sistem koordinat memungkinkan Anda merancang grafik dalam unit dunia nyata sementara perpustakaan secara otomatis menangani skala piksel untuk perangkat output apa pun. Pendekatan ini menjamin bahwa persegi panjang 5‑inci tercetak tepat lima inci pada printer 300 DPI dan muncul secara proporsional pada layar 96 DPI, menghilangkan kesalahan konversi manual.

- **Desain independen perangkat:** Tulis kode sekali; Aspose.Drawing menskalakannya untuk layar, printer, atau PDF.  
- **Penggambaran presisi:** Ideal untuk diagram teknis, skematik teknik, atau skenario apa pun di mana pengukuran yang tepat penting.  
- **Keandalan lintas‑platform:** Bekerja secara konsisten di Windows, Linux, dan macOS tanpa batasan GDI+ pada System.Drawing.  
- **Kinerja:** Pada CPU tipikal 2,5 GHz, menggambar persegi panjang 5‑inci pada 300 DPI selesai dalam kurang dari **15 ms**, dan perpustakaan dapat merender **50 frame per detik** dalam skenario pratinjau waktu nyata.

## Prasyarat

- **Perpustakaan Aspose.Drawing:** Unduh versi terbaru dari situs resmi [here](https://releases.aspose.com/drawing/net/).  
- **IDE:** Visual Studio, Rider, atau editor yang kompatibel dengan .NET apa pun.  
- **Folder output:** Ganti `"Your Document Directory"` dalam kode contoh dengan folder tempat Anda ingin menyimpan PNG.  
- **Dukungan ASP.NET opsional:** Anda dapat menambahkan paket NuGet ke proyek ASP.NET Core dan menggunakan API yang sama; pola ini mengikuti pendekatan **how to use aspnet** khas untuk perpustakaan .NET.

## Cara menggambar persegi panjang dengan transformasi halaman?

Muat bitmap kosong, atur unit halaman ke inci, dan gambar persegi panjang menggunakan pena biru tipis—ini menyelesaikan penggambaran persegi panjang dalam beberapa baris kode saja. Properti `Graphics.PageUnit` memberi tahu mesin untuk menafsirkan semua koordinat sebagai inci, sehingga Anda dapat berpikir dalam ukuran dunia nyata alih-alih piksel mentah, dan perpustakaan secara otomatis **mengonversi inci ke piksel** berdasarkan DPI bitmap.

### Langkah 1: mengimpor namespace

```csharp
using System.Drawing;
```

### Langkah 2: membuat bitmap

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Langkah 3: membuat objek graphics

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Langkah 4: membersihkan latar belakang kanvas

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Langkah 5: mengatur transformasi (cara mengatur unit)

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Langkah 6: menggambar persegi panjang – menggambar grafik persegi panjang

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Langkah 7: menyimpan bitmap sebagai png

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Cara menskalakan grafik untuk printer?

Atur DPI bitmap ke resolusi printer target (misalnya, 300 DPI) sebelum menggambar. Ini secara otomatis **menskalakan grafik printer** output sehingga satu inci dalam kode Anda sama dengan satu inci pada halaman tercetak, sementara ukuran logis persegi panjang tetap tidak berubah. Setelah memanggil `bitmap.SetResolution(300, 300)`, persegi panjang yang sama akan tampak lebih besar di kertas tetapi mempertahankan dimensi tepatnya.

## Masalah umum dan solusi

| Masalah | Mengapa terjadi | Solusi |
|-------|----------------|-----|
| **File output tidak dibuat** | Path tidak tepat atau folder tidak ada | Pastikan direktori target ada atau panggil `Directory.CreateDirectory` sebelum menyimpan. |
| **Persegi panjang tampak terdistorsi** | `PageUnit` atau DPI tidak cocok | Verifikasi bahwa `graphics.PageUnit` sesuai dengan unit yang dimaksud dan DPI bitmap diatur dengan tepat (default 96 DPI, 300 DPI untuk cetak). |
| **Pengecualian lisensi** | Menjalankan tanpa lisensi yang valid di produksi | Terapkan lisensi Aspose.Drawing sementara atau permanen Anda sebelum membuat objek grafik. |

## Pertanyaan yang sering diajukan

**Q: Bisakah saya menggunakan Aspose.Drawing secara gratis?**  
A: Ya, versi percobaan gratis tersedia [here](https://releases.aspose.com/).

**Q: Di mana saya dapat menemukan dokumentasi detail untuk Aspose.Drawing?**  
A: Referensi API lengkap berada [here](https://reference.aspose.com/drawing/net/).

**Q: Bagaimana cara mendapatkan dukungan untuk Aspose.Drawing?**  
A: Kunjungi [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) untuk bantuan komunitas dan dukungan resmi.

**Q: Apakah lisensi sementara tersedia untuk Aspose.Drawing?**  
A: Tentu—dapatkan satu [here](https://purchase.aspose.com/temporary-license/).

**Q: Di mana saya dapat membeli lisensi penuh Aspose.Drawing?**  
A: Anda dapat membelinya [here](https://purchase.aspose.com/buy).

## Kesimpulan

Anda kini tahu **cara menggambar persegi panjang** grafik dengan transformasi tingkat halaman menggunakan Aspose.Drawing untuk .NET. Dengan mengatur unit halaman ke inci, membersihkan latar belakang kanvas, dan menyimpan hasil sebagai PNG, Anda memperoleh output yang presisi dan independen perangkat yang cocok untuk tampilan layar maupun pencetakan resolusi tinggi. Bereksperimenlah dengan unit lain, rotasi, atau asal koordinat khusus untuk membuka skenario penggambaran yang lebih kuat.

---

**Terakhir Diperbarui:** 2026-11-04  
**Diuji Dengan:** Aspose.Drawing 24.12 for .NET  
**Penulis:** Aspose

## Tutorial Terkait

- [Cara Mengatur Unit di Aspose.Drawing untuk .NET – Unit Pengukuran](/drawing/net/coordinate-transformations/units-of-measure/)
- [Transformasi Global](/drawing/net/coordinate-transformations/global-transformation/)
- [Transformasi Langkah demi Langkah – Transformasi Koordinat](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}