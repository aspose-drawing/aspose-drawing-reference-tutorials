---
title: Menggambar Jalur di Aspose.Menggambar
linktitle: Menggambar Jalur di Aspose.Menggambar
second_title: Aspose.Drawing .NET API - Alternatif untuk System.Drawing.Common
description: Pelajari cara menggambar jalur di Aspose.Drawing untuk .NET dengan panduan langkah demi langkah ini. Buat grafik yang menakjubkan dengan mudah.
weight: 17
url: /id/net/lines-curves-and-shapes/draw-path/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menggambar Jalur di Aspose.Menggambar

## Perkenalan

Selamat datang di panduan komprehensif kami tentang menggambar jalur di Aspose.Drawing untuk .NET. Baik Anda seorang pengembang berpengalaman atau pendatang baru dalam pemrograman grafis, tutorial ini akan memandu Anda melalui proses pembuatan jalur rumit menggunakan Aspose.Drawing. Aspose.Drawing adalah perpustakaan canggih yang menyederhanakan operasi grafis dalam aplikasi .NET, menawarkan berbagai fungsi untuk membuat, mengedit, dan memanipulasi gambar.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Perpustakaan Aspose.Drawing: Unduh dan instal perpustakaan Aspose.Drawing. Anda dapat menemukan perpustakaan[Di Sini](https://releases.aspose.com/drawing/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET Anda dengan alat yang diperlukan.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan dalam proyek Anda:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Langkah 1: Buat Bitmap dan Grafik

Mulailah dengan membuat Bitmap dan objek Grafik untuk digunakan:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Langkah 2: Tentukan Pena dan GraphicsPath

Selanjutnya, tentukan Pen untuk menentukan atribut gambar dan GraphicsPath untuk mewakili jalur:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## Langkah 3: Tambahkan Garis dan Bentuk

Tambahkan garis, persegi panjang, dan elips ke GraphicsPath untuk membuat jalur yang kompleks:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## Langkah 4: Gambar Jalur

Gambarkan jalur ke objek Grafik menggunakan Pena yang ditentukan:

```csharp
graphics.DrawPath(pen, path);
```

## Langkah 5: Simpan Gambar

Terakhir, simpan gambar yang dihasilkan ke direktori yang Anda inginkan:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

Ulangi langkah-langkah ini seperlunya untuk membuat jalur yang rumit dan menarik secara visual.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menggambar jalur menggunakan Aspose.Drawing untuk .NET. Tutorial ini membahas dasar-dasar membuat Bitmap, mendefinisikan Pena, membuat GraphicsPath, dan menggambar berbagai bentuk. Bereksperimenlah dengan berbagai parameter dan bentuk untuk mengeluarkan potensi penuh Aspose.Drawing.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.Drawing dengan perpustakaan .NET lainnya?

A1: Ya, Aspose.Drawing terintegrasi secara mulus dengan pustaka .NET lainnya, memberikan keserbagunaan dalam proyek pengembangan Anda.

### Q2: Apakah ada versi uji coba yang tersedia?

 A2: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dukungan untuk Aspose.Drawing?

 A3: Kunjungi Aspose.Gambar[forum](https://forum.aspose.com/c/diagram/17) untuk bantuan dan dukungan masyarakat.

### Q4: Bagaimana cara mendapatkan lisensi sementara?

 A4: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Bisakah saya membeli Aspose.Gambar?

 A5: Ya, Anda dapat membeli Aspose.Drawing[Di Sini](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
