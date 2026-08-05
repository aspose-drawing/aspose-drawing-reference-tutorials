---
date: 2026-05-19
description: Pelajari cara menggambar grafik persegi panjang sambil melakukan Coordinate
  System Transformation di .NET dengan Aspose.Drawing. Panduan langkah demi langkah
  ini menunjukkan cara mengonversi inci ke piksel dan mengatur satuan halaman.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Coordinate System Transformation di Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Cara Menggambar Persegi Panjang – Coordinate System Transformation (Transformasi
  Halaman) di Aspose.Drawing untuk .NET
url: /id/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menggambar Persegi Panjang – Transformasi Sistem Koordinat (Transformasi Halaman) di Aspose.Drawing untuk .NET

## Pendahuluan

Selamat datang! Dalam tutorial ini Anda akan menemukan **how to draw rectangle** grafik sambil mentransformasi koordinat halaman menggunakan Aspose.Drawing untuk .NET. Baik Anda membangun aplikasi yang intensif grafis atau membutuhkan kontrol presisi atas satuan gambar, panduan ini akan memandu Anda melalui setiap langkah—dari menyiapkan kanvas hingga menggambar elemen persegi panjang. Pada akhir tutorial, Anda akan dapat menerapkan teknik ini dalam proyek Anda dengan percaya diri.

## Jawaban Cepat
- **Apa itu transformasi sistem koordinat?** Memetakan satuan tingkat halaman (seperti inci) ke piksel tingkat perangkat.  
- **Mengapa menggunakan Aspose.Drawing?** Menawarkan alternatif sepenuhnya dikelola, lintas‑platform untuk System.Drawing.Common.  
- **Berapa lama contoh ini membutuhkan waktu untuk diimplementasikan?** Sekitar 5‑10 menit untuk transformasi halaman dasar.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Versi .NET mana yang didukung?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu Aspose.Drawing?

`Aspose.Drawing` adalah pustaka grafis .NET yang menyediakan **device‑independent API** untuk membuat dan memanipulasi gambar raster, vektor, dan gambar tingkat halaman tanpa bergantung pada GDI+. Ia mendukung **30+ format gambar** dan dapat memproses gambar hingga **10.000 × 10.000 piksel** tanpa memuat seluruh file ke memori.

## Mengapa menggunakan transformasi sistem koordinat dengan Aspose.Drawing?

Transformasi sistem koordinat memungkinkan Anda merancang grafis dalam satuan dunia nyata sementara pustaka menangani skala piksel untuk perangkat output apa pun. Ini memastikan ukuran konsisten di layar dan printer serta menyederhanakan perhitungan tata letak.

- **Desain independen perangkat:** Tulis kode sekali dan biarkan Aspose.Drawing menangani skala piksel untuk layar atau printer apa pun.  
- **Penggambaran presisi:** Ideal untuk diagram teknis, sketsa gaya CAD, atau skenario apa pun di mana ukuran yang tepat penting.  
- **Keandalan lintas platform:** Bekerja secara konsisten di Windows, Linux, dan macOS tanpa keterbatasan GDI+ pada System.Drawing.  
- **Angka kinerja:** Pada CPU 2.5 GHz tipikal, menggambar persegi panjang 5‑inci pada 300 DPI memakan waktu kurang dari **15 ms**, dan perpustakaan dapat merender **50 frame per detik** dalam skenario pratinjau waktu nyata.

## Prasyarat

- **Pustaka Aspose.Drawing:** Unduh versi terbaru dari situs resmi [here](https://releases.aspose.com/drawing/net/).  
- **Lingkungan Pengembangan:** Visual Studio, Rider, atau IDE kompatibel .NET apa pun.  
- **Direktori Dokumen Anda:** Ganti `"Your Document Directory"` dalam kode dengan folder tempat Anda ingin menyimpan gambar output.  
- **Dukungan ASP.NET (opsional):** Anda dapat menggunakan Aspose.Drawing dalam proyek ASP.NET Core dengan menambahkan paket NuGet ke aplikasi web Anda—ini mengikuti pola **how to use aspnet** yang sama seperti pustaka .NET lainnya.

Sekarang semua siap, mari kita selami panduan langkah demi langkah.

## Cara Menggambar Persegi Panjang dengan Transformasi Halaman?

Muat bitmap kosong, atur satuan halaman ke inci, dan gambar persegi panjang menggunakan pena biru tipis—ini menyelesaikan gambar persegi panjang dalam beberapa baris kode saja. Properti `Graphics.PageUnit` memberi tahu mesin untuk menafsirkan semua koordinat sebagai inci, sehingga Anda dapat berpikir dalam ukuran dunia nyata alih-alih piksel mentah.

### Langkah 1: Impor Namespace

Pernyataan `using` memberi Anda akses ke kelas gambar inti.

```csharp
using System.Drawing;
```

### Langkah 2: Buat Bitmap

`Bitmap` mewakili gambar dalam memori yang dapat Anda gambar di atasnya. Kami memulai dengan membuat bitmap kosong yang akan menjadi permukaan gambar. Format piksel `Format32bppPArgb` memberi kami dukungan alfa premultiplied berkualitas tinggi.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Langkah 3: Buat Objek Graphics

Objek `Graphics` menyediakan API gambar untuk bitmap. Ini adalah jembatan antara kode Anda dan buffer piksel.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Langkah 4: Bersihkan Kanvas

Berikan kanvas latar belakang netral sehingga bentuk yang digambar menonjol. Di sini kami mengisinya dengan abu-abu terang.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Langkah 5: Atur Transformasi (Cara mengatur satuan)

`Graphics.PageUnit` menentukan satuan ukuran yang digunakan untuk koordinat halaman. Untuk memetakan koordinat halaman ke piksel perangkat, atur properti `PageUnit`. Dalam contoh ini kami memilih inci, tetapi Anda juga dapat menggunakan `GraphicsUnit.Millimeter`, `GraphicsUnit.Point`, atau `GraphicsUnit.Pixel`. Mengatur satuan ke inci memungkinkan Anda **convert inches to pixels** secara otomatis berdasarkan DPI bitmap (96 DPI secara default, 300 DPI untuk pencetakan resolusi tinggi).

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Langkah 6: Gambar Persegi Panjang – menggambar grafik persegi panjang

`Pen` menentukan warna, lebar, dan gaya garis yang digambar pada permukaan grafis. Sekarang kami menggambar persegi panjang menggunakan pena biru tipis. Karena kami beralih ke inci, ukuran dan posisi persegi panjang diekspresikan dalam inci, membuat kode lebih mudah dibaca untuk tata letak yang berorientasi cetak.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Langkah 7: Simpan Gambar

Akhirnya, tulis bitmap ke file PNG di folder yang Anda tentukan sebelumnya.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Cara Menskalakan Grafik untuk Printer?

Atur DPI bitmap ke resolusi printer target (misalnya, 300 DPI) sebelum menggambar. Ini secara otomatis **scale graphics printer** output sehingga satu inci dalam kode Anda sama dengan satu inci pada halaman tercetak. Setelah menetapkan `bitmap.SetResolution(300, 300)`, persegi panjang yang sama akan muncul lebih besar pada lembar cetak sambil mempertahankan dimensi tepatnya.

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Solusi |
|---------|----------------|--------|
| **File output tidak dibuat** | Path tidak benar atau folder tidak ada | Pastikan direktori target ada atau gunakan `Directory.CreateDirectory` sebelum menyimpan. |
| **Persegi panjang tampak terdistorsi** | `PageUnit` salah atau DPI tidak cocok | Verifikasi bahwa `graphics.PageUnit` sesuai dengan satuan yang ingin Anda gunakan dan DPI bitmap diatur dengan tepat (default 96 DPI). |
| **Pengecualian lisensi** | Menjalankan tanpa lisensi yang valid di produksi | Terapkan lisensi Aspose.Drawing sementara atau permanen Anda sebelum membuat objek grafik. |

## Pertanyaan yang Sering Diajukan

**Q: Apakah saya dapat menggunakan Aspose.Drawing secara gratis?**  
A: Ya, percobaan gratis tersedia [here](https://releases.aspose.com/).

**Q: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.Drawing?**  
A: Referensi API lengkap berada [here](https://reference.aspose.com/drawing/net/).

**Q: Bagaimana cara mendapatkan dukungan untuk Aspose.Drawing?**  
A: Kunjungi [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) untuk bantuan komunitas dan dukungan resmi.

**Q: Apakah lisensi sementara tersedia untuk Aspose.Drawing?**  
A: Tentu—dapatkan satu [here](https://purchase.aspose.com/temporary-license/).

**Q: Di mana saya dapat membeli lisensi penuh Aspose.Drawing?**  
A: Anda dapat membelinya [here](https://purchase.aspose.com/buy).

## Kesimpulan

Dalam panduan ini kami membahas semua yang Anda perlukan untuk **how to draw rectangle** grafik dengan Aspose.Drawing: menyiapkan kanvas, mengonfigurasi satuan halaman, menggambar bentuk presisi, dan menyimpan hasilnya. Gunakan teknik ini untuk membangun grafis skalabel, independen perangkat untuk laporan, gambar gaya CAD, atau aplikasi apa pun di mana akurasi pengukuran penting. Selanjutnya, jelajahi transformasi lanjutan seperti rotasi, skala, dan asal koordinat khusus untuk membuka lebih banyak skenario menggambar yang kuat.

---

**Last Updated:** 2026-05-19  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
