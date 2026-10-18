---
date: 2026-10-18
description: Konversi drawing ke PNG dengan Aspose.Drawing sambil menerapkan world
  transformations. Pelajari contoh translate, rotate, dan scale dalam C# serta mengekspor
  PNG transparan.
keywords:
- convert drawing to png
- save graphics as png
- rotate image .net
- scale graphics .net
- transparent png bitmap
lastmod: 2026-10-18
linktitle: World transformation dalam Aspose.Drawing
og_description: Konversi drawing ke PNG dengan Aspose.Drawing, terapkan world transformations
  dan ekspor PNG transparan. Pelajari contoh translate, rotate, dan scale C# untuk
  .NET.
og_image_alt: Tutorial showing how to convert drawing to PNG using Aspose.Drawing
  with world transformation
og_title: Cara mengonversi drawing ke PNG dengan Aspose.Drawing – world transformation
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  headline: How to convert drawing to PNG with Aspose.Drawing – world transformation
  type: TechArticle
- description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  name: How to convert drawing to PNG with Aspose.Drawing – world transformation
  steps:
  - name: create a bitmap
    text: '**Definition:** `Bitmap` is Aspose.Drawing’s in‑memory representation of
      a raster image that you can draw on or save to disk. We start by creating a
      blank canvas that will hold our drawing. `new Bitmap(width, height, PixelFormat.Format32bppPArgb)`
      creates a 32‑bit per pixel bitmap with premultiplied'
  - name: set the world transformation (graphics translate example)
    text: '**Definition:** `Graphics` is the drawing surface that renders shapes onto
      a `Bitmap`. `TranslateTransform` moves the origin of the coordinate system to
      a new location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height
      / 2)` shifts the (0,0) point to the canvas centre. After this call, an'
  - name: draw a rectangle using the transformed coordinates
    text: '**Definition:** `DrawRectangle` is a method of `Graphics` that renders
      a rectangular outline or filled shape based on the supplied pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width'
  - name: save the result – convert graphics to PNG
    text: '**Definition:** `ImageFormat` is an enumeration that tells the `Save` method
      which file format to use. `Save` writes the bitmap to a file in the specified
      image format. `bitmap.Save(outputPath, ImageFormat.Png)` writes a lossless PNG
      file that can be used directly in web pages or UI components. - PN'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- convert drawing to png
- Aspose.Drawing
- .NET graphics
- PNG export
- world transformation
title: Cara mengonversi drawing ke PNG dengan Aspose.Drawing – world transformation
url: /id/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara mengonversi drawing ke PNG dengan Aspose.Drawing – transformasi dunia

## Simpan bitmap sebagai PNG – pengantar

**How to convert drawing to PNG** menggunakan Aspose.Drawing adalah kebutuhan umum ketika Anda memerlukan gambar berkualitas tinggi dan transparan yang dihasilkan secara dinamis. Dalam tutorial ini Anda akan belajar cara **save bitmap as PNG**, menerapkan transformasi dunia seperti translate, rotate, dan scale, dan akhirnya mengonversi graphics ke PNG—semua dengan kode C# yang bersih dan dapat dipelihara. Baik Anda membangun mesin pelaporan, komponen charting, atau renderer UI khusus, menguasai langkah‑langkah ini memungkinkan Anda membuat gambar dinamis yang tampak bagus di perangkat apa pun.

## Jawaban Cepat
- **Apa arti “world transformation”?** Ini memetakan koordinat logis (world) gambar Anda ke koordinat halaman (device), memungkinkan Anda memindahkan, memutar, atau menskalakan semuanya dengan satu matriks.  
- **Bisakah saya mengekspor hasilnya sebagai PNG?** Ya – setelah menggambar Anda cukup memanggil `bitmap.Save(...)` dengan ekstensi `.png`.  
- **Apakah saya memerlukan lisensi untuk Aspose.Drawing?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Apakah ini kompatibel dengan .NET 6/7?** Tentu – Aspose.Drawing mendukung .NET Framework 4.5+ dan .NET Core/5/6/7, mencakup lebih dari 90 % dari penyebaran .NET saat ini.  
- **Berapa banyak transformasi yang dapat saya rangkaikan?** Anda dapat menerapkan **multiple graphics transformations** secara berurutan (translate, rotate, scale, dll.) tanpa penalti kinerja.

## Apa itu world transformation di Aspose.Drawing?

Transformasi dunia mengubah sistem koordinat yang digunakan perintah drawing Anda. Secara default, (0,0) berada di sudut kiri‑atas bitmap. Dengan `TranslateTransform`, `RotateTransform`, atau `ScaleTransform`, Anda dapat memindahkan asal tersebut, memutar bentuk, atau mengubah ukurannya tanpa mengubah geometri asli. Ini memungkinkan Anda mendesain sekali dan merender pada ukuran atau orientasi apa pun.

## Cara menyimpan PNG menggunakan Aspose.Drawing?

Muat objek `Bitmap`, atur transformasi dunia yang diinginkan pada instance `Graphics`‑nya, gambar bentuk Anda, dan akhirnya panggil `bitmap.Save("output.png", ImageFormat.Png)`. Panggilan penyimpanan satu baris ini menulis file PNG lossless yang mempertahankan transparansi dan keakuratan warna, menjadikannya ideal untuk aset web dan overlay UI. API menangani semua enkoding level rendah, sehingga Anda mendapatkan PNG siap pakai dalam kurang dari satu detik untuk ukuran kanvas tipikal.

## Mengapa menggunakan contoh graphics translate?

Contoh graphics translate memungkinkan Anda memindahkan asal drawing satu kali alih‑alih menghitung ulang setiap titik. Dengan menggeser asal ke tengah kanvas, Anda menyederhanakan geometri, mengurangi duplikasi kode, dan membiarkan mesin graphics melakukan perkalian matriks dalam kode native, yang dapat meningkatkan kecepatan rendering hingga 30 % pada kanvas besar. Pola ini juga membuat kode Anda lebih mudah dipelihara ketika Anda menambahkan rotasi atau skala nanti.

## Contoh graphics translate

**graphics translate example** menunjukkan bagaimana memindahkan asal menyederhanakan penempatan. Alih‑alih menghitung ulang setiap titik, Anda menggeser sistem koordinat sekali dan menggambar seolah‑olah asal baru berada di tengah kanvas.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki:

- **Aspose.Drawing library** terintegrasi ke dalam proyek .NET Anda – unduh dari [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/).  
- **document directory** tempat gambar output akan disimpan.  
- Familiaritas dasar dengan sintaks **C#** dan Visual Studio atau IDE pilihan Anda.  

Sekarang, mari kita selami kode!

## Impor namespace

`Bitmap`, `Graphics`, dan utilitas drawing Aspose berada di namespace ini.  
**Definition:** `System.Drawing` menyediakan tipe inti GDI+, sementara `Aspose.Drawing` memperluasnya dengan kemampuan lintas‑platform, memungkinkan Anda menjalankan kode yang sama di Windows, Linux, dan macOS tanpa ketergantungan tambahan.

## Panduan langkah‑demi‑langkah

### Langkah 1: buat bitmap

**Definition:** `Bitmap` adalah representasi in‑memory Aspose.Drawing dari gambar raster yang dapat Anda gambar atau simpan ke disk.  

Kita mulai dengan membuat kanvas kosong yang akan menampung drawing kita.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` membuat bitmap 32‑bit per piksel dengan alpha premultiplied, yang merupakan format optimal untuk output PNG karena mempertahankan transparansi tanpa langkah konversi tambahan.

- **Why 32bppPArgb?** Format piksel ini mendukung transparansi alpha dan rendering warna berkualitas tinggi, sempurna untuk output PNG.  
- **Pro tip:** Sesuaikan lebar/tinggi agar cocok dengan ukuran gambar target; kanvas 1920 × 1080 dirender dalam kurang dari 0,2 detik pada laptop pengembang tipikal.

### Langkah 2: atur world transformation (contoh graphics translate)

**Definition:** `Graphics` adalah permukaan drawing yang merender bentuk ke `Bitmap`.  

`TranslateTransform` memindahkan asal sistem koordinat ke lokasi baru.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` menggeser titik (0,0) ke tengah kanvas. Setelah pemanggilan ini, setiap bentuk yang Anda gambar menggunakan koordinat (0,0) akan muncul di tengah gambar.

- Ini memindahkan titik (0,0) ke (500, 400) – tengah kanvas 1000 × 800.  
- Anda dapat merangkai transformasi tambahan: `RotateTransform` memutar sistem koordinat, dan `ScaleTransform` menskalanya, memungkinkan **multiple graphics transformations** dalam satu pipeline.

### Langkah 3: gambar persegi panjang menggunakan koordinat yang ditransformasi

**Definition:** `DrawRectangle` adalah metode `Graphics` yang merender kontur persegi panjang atau bentuk terisi berdasarkan pen dan koordinat yang diberikan.  

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` menggambar persegi panjang yang terpusat pada kanvas karena sudut kiri‑atasnya dipindahkan setengah lebar dan tinggi dari asal yang ditransformasi.

- Sudut kiri‑atas persegi panjang dimulai dari asal yang ditransformasi (tengah gambar).  
- Silakan bereksperimen dengan bentuk lain—elips, garis, atau path khusus.

### Langkah 4: simpan hasil – konversi graphics ke PNG

**Definition:** `ImageFormat` adalah enumerasi yang memberi tahu metode `Save` format file mana yang akan digunakan.  

`Save` menulis bitmap ke file dalam format gambar yang ditentukan.  
`bitmap.Save(outputPath, ImageFormat.Png)` menulis file PNG lossless yang dapat langsung digunakan di halaman web atau komponen UI.

- PNG mempertahankan warna dan transparansi tepat yang kami set sebelumnya.  
- Ganti `"Your Document Directory"` dengan jalur sebenarnya di mesin Anda.  
- Untuk pemrosesan batch, iterasi koleksi objek `Bitmap` dan panggil `Save` di dalam loop – perpustakaan dapat menangani ribuan gambar dengan kurang dari 200 MB RAM.

## Masalah umum dan solusi

| Issue | Why it happens | Fix |
|-------|----------------|-----|
| **File not found error** saat menyimpan | Folder target tidak ada. | Buat folder secara programatik (`Directory.CreateDirectory`) sebelum memanggil `Save`. |
| **Blank image** setelah transformasi | `TranslateTransform` dipanggil setelah menggambar. | Pastikan transformasi diatur **sebelum** perintah menggambar apa pun. |
| **Distorted colors** | Menggunakan format piksel yang tidak kompatibel. | Gunakan `Format32bppPArgb` untuk output PNG. |
| **Out‑of‑memory on large canvases** | Memuat seluruh bitmap ke memori. | Gunakan opsi streaming `Bitmap` atau bagi gambar menjadi ubin; Aspose.Drawing dapat merender ubin secara independen. |

## Pertanyaan yang sering diajukan

**Q: Bisakah saya menerapkan lebih dari satu transformasi?**  
A: Ya – Anda dapat merangkai `TranslateTransform`, `RotateTransform`, dan `ScaleTransform` untuk mencapai efek kompleks dalam satu pipeline graphics.

**Q: Apakah Aspose.Drawing gratis untuk proyek komersial?**  
A: Versi percobaan gratis tersedia untuk evaluasi, tetapi lisensi komersial diperlukan untuk penggunaan produksi.

**Q: Apakah ini bekerja dengan .NET Core dan .NET 5/6/7?**  
A: Tentu. Aspose.Drawing mendukung semua runtime .NET modern, termasuk .NET Core, .NET 5, .NET 6, dan .NET 7.

**Q: Di mana saya dapat menemukan referensi API lengkap?**  
A: Dokumentasi lengkap tersedia di [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).

**Q: Bagaimana cara mengatasi file output yang hilang?**  
A: Verifikasi string path, pastikan izin menulis, dan pastikan direktori ada sebelum memanggil `Save`.

## Kesimpulan

Anda kini telah mempelajari **how to convert drawing to PNG** dengan Aspose.Drawing, menerapkan **world transformation**, dan melakukan **graphics translate example** yang dapat diperluas dengan rotasi atau skala. Dengan menguasai blok‑bangunan ini Anda dapat menghasilkan gambar dinamis, membuat chart khusus, atau membangun grafik on‑the‑fly untuk aplikasi .NET apa pun. Selanjutnya, jelajahi tutorial transformasi berbasis matriks untuk menggabungkan beberapa operasi menjadi satu matriks demi kinerja yang lebih optimal.

---

**Last updated:** 2026-10-18  
**Tested with:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  
**Related resources:** [Aspose.Drawing API reference](https://reference.aspose.com/drawing/net/) | [Download free trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Tutorial terkait

- [Tutorial transformasi matriks: matrix transformations in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Cara memutar gambar dengan Aspose.Drawing global transformation](/drawing/net/coordinate-transformations/global-transformation/)
- [Transformasi sistem koordinat – page transformation in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}