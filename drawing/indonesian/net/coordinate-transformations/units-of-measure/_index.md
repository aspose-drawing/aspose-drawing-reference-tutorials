---
title: Satuan Ukuran di Aspose.Drawing untuk .NET
linktitle: Satuan Ukuran dalam Aspose.Gambar
second_title: Aspose.Drawing .NET API - Alternatif untuk System.Drawing.Common
description: Jelajahi keserbagunaan Aspose.Drawing untuk .NET dalam tutorial mendalam ini, kuasai satuan ukuran untuk grafik presisi.
weight: 14
url: /id/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Satuan Ukuran di Aspose.Drawing untuk .NET

## Perkenalan

Selamat datang di dunia Aspose.Drawing untuk .NET, tempat presisi dan fleksibilitas bertemu dalam manipulasi grafis. Dalam tutorial ini, kita akan mempelajari seluk-beluk satuan ukuran dalam Aspose.Drawing, memberi Anda panduan langkah demi langkah untuk memanfaatkan kekuatan perpustakaan yang luar biasa ini.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.Drawing untuk .NET: Pastikan Anda telah menginstal perpustakaan. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/drawing/net/).

- Direktori Dokumen: Miliki direktori khusus tempat Anda ingin menyimpan dokumen yang Anda buat.

- Pengetahuan Dasar C#: Pemahaman mendasar tentang C# disarankan untuk memanfaatkan panduan ini semaksimal mungkin.

## Impor Namespace

Sebelum kita mulai, mari impor namespace yang diperlukan untuk menggunakan Aspose.Drawing secara efektif:

```csharp
using System.Drawing;
```

Sekarang, mari kita bagi setiap contoh menjadi beberapa langkah:

## Poin sebagai Satuan Ukuran

1. Buat Bitmap: Inisialisasi bitmap dengan lebar dan tinggi tertentu.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Buat Grafik: Hasilkan objek Grafik dari bitmap untuk digambar di atasnya.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Atur Satuan Halaman ke Poin: Tetapkan titik sebagai satuan ukuran (1 poin = 1/72 inci).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Menggambar Persegi Panjang: Menggambar persegi panjang menggunakan titik sebagai satuannya.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Milimeter sebagai Satuan Ukuran

1. Atur Satuan Halaman ke Milimeter: Ubah satuan ukuran menjadi milimeter (1 mm = 1/25,4 inci).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Menggambar Persegi Panjang dalam Milimeter: Gambarlah persegi panjang lain menggunakan milimeter sebagai satuannya.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Inci sebagai Satuan Ukuran

1. Atur Satuan Halaman ke Inci: Mengubah satuan ukuran menjadi inci.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Gambar Persegi Panjang dalam Inci: Gambarlah persegi panjang menggunakan inci sebagai satuannya.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Simpan Hasilnya

Setelah menyelesaikan contoh, simpan gambar yang dihasilkan ke direktori dokumen Anda:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Sekarang, Anda telah berhasil menavigasi beragam satuan ukuran di Aspose.Drawing untuk .NET, membuat representasi visual persegi panjang menggunakan titik, milimeter, dan inci.

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi bagaimana Aspose.Drawing untuk .NET menangani satuan ukuran yang berbeda. Dengan memanipulasi titik, milimeter, dan inci, Anda dapat mencapai presisi dan kemampuan beradaptasi dalam kreasi grafis Anda. Bereksperimenlah dengan konsep-konsep ini untuk membuka potensi penuh Aspose.Drawing.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.Drawing untuk .NET dengan kerangka .NET lainnya?

A1: Ya, Aspose.Drawing kompatibel dengan berbagai kerangka .NET, memberikan fleksibilitas dalam lingkungan pengembangan Anda.

### Q2: Apakah tersedia uji coba gratis?

 A2: Ya, Anda dapat menjelajahi Aspose.Drawing dengan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana cara mendapatkan dukungan untuk Aspose.Drawing untuk .NET?

 A3: Kunjungi[Aspose.Forum Menggambar](https://forum.aspose.com/c/drawing/44) untuk dukungan dan diskusi komunitas.

### Q4: Dapatkah saya membeli lisensi sementara untuk proyek jangka pendek?

 A4: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.Drawing?

 A5: Dokumentasi lengkap tersedia[Di Sini](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
