---
title: Mengisi Wilayah di Aspose.Gambar
linktitle: Mengisi Wilayah di Aspose.Gambar
second_title: Aspose.Drawing .NET API - Alternatif untuk System.Drawing.Common
description: Pelajari cara mengisi wilayah di Aspose.Drawing untuk .NET dengan tutorial langkah demi langkah ini. Tingkatkan keterampilan desain grafis Anda dengan mudah.
weight: 20
url: /id/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengisi Wilayah di Aspose.Gambar

## Perkenalan

Membuat grafik yang menarik secara visual sering kali melibatkan pengisian area dengan warna, pola, atau gradien. Aspose.Drawing for .NET menyediakan alat canggih untuk mencapai hal ini secara efisien. Dalam tutorial ini, kita akan mempelajari proses pengisian wilayah menggunakan Aspose.Drawing, perpustakaan serbaguna yang menyederhanakan operasi grafis dalam aplikasi .NET.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1.  Perpustakaan Aspose.Drawing: Unduh dan instal perpustakaan Aspose.Drawing. Anda dapat menemukan perpustakaan dan dokumentasinya[Di Sini](https://reference.aspose.com/drawing/net/).

2. Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET, seperti Visual Studio, untuk mengintegrasikan Aspose.Drawing ke dalam proyek Anda.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan ke dalam proyek Anda. Namespace ini menyediakan akses ke kelas dan metode yang diperlukan untuk bekerja dengan Aspose.Drawing.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


Sekarang, mari kita pecahkan kode contoh menjadi beberapa langkah untuk pemahaman yang jelas dan komprehensif.

## Langkah 1: Buat Bitmap dan Objek Grafik

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Pada langkah ini, kita menginisialisasi bitmap baru dan objek grafis untuk digambar.

## Langkah 2: Tentukan GraphicsPath dan Buat Wilayah

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

Tentukan jalur grafik dengan menentukan poligon dengan sekumpulan titik. Buat wilayah menggunakan jalur ini.

## Langkah 3: Kecualikan Wilayah Dalam

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

Buat jalur grafik lain yang mewakili persegi panjang bagian dalam dan kecualikan dari wilayah utama.

## Langkah 4: Pilih Kuas dan Isi Wilayahnya

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

Pilih kuas (dalam hal ini, warna biru solid) dan isi wilayah yang telah ditentukan sebelumnya dengan kuas yang dipilih.

## Langkah 5: Simpan Gambar yang Dihasilkan

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

Simpan gambar akhir ke direktori yang Anda inginkan.

## Kesimpulan

Mengisi wilayah di Aspose.Drawing untuk .NET adalah proses yang mudah, memberi Anda fleksibilitas untuk membuat grafik yang kompleks dan menarik secara visual. Bereksperimenlah dengan berbagai bentuk, warna, dan pola untuk melepaskan kreativitas Anda.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.Drawing untuk proyek komersial?

 A1: Ya, Aspose.Drawing dapat digunakan untuk proyek pribadi dan komersial. Untuk detail lisensi, kunjungi[Di Sini](https://purchase.aspose.com/buy).

### Q2: Apakah tersedia uji coba gratis?

 A2: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.Drawing?

 A3: Kunjungi[Aspose.Forum menggambar](https://forum.aspose.com/c/diagram/17) mendapatkan bantuan dari masyarakat dan para ahli.

### Q4: Bisakah saya menghasilkan gambar dinamis menggunakan Aspose.Drawing?

A4: Tentu saja. Aspose.Drawing memungkinkan Anda membuat dan memanipulasi gambar secara dinamis dalam aplikasi .NET Anda.

### Q5: Apakah lisensi sementara tersedia?

 A5: Ya, izin sementara dapat diperoleh[Di Sini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
