---
title: Memuat dan Menyimpan Gambar di Aspose.Drawing
linktitle: Memuat dan Menyimpan Gambar di Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternatif untuk System.Drawing.Common
description: Kuasai pemuatan dan penyimpanan gambar di .NET dengan Aspose.Drawing. Jelajahi format BMP, GIF, JPG, PNG, TIFF dengan mudah.
weight: 13
url: /id/net/image-editing/load-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Memuat dan Menyimpan Gambar di Aspose.Drawing

## Perkenalan

Selamat datang di panduan langkah demi langkah kami dalam menguasai pemuatan dan penyimpanan gambar menggunakan Aspose.Drawing untuk .NET! Jika Anda ingin meningkatkan keterampilan Anda dalam memanipulasi berbagai format gambar dengan mudah, Anda berada di tempat yang tepat. Aspose.Drawing for .NET adalah perpustakaan canggih yang menyederhanakan proses bekerja dengan gambar, dan dalam tutorial ini, kita akan mendalami cara memuat dan menyimpan gambar dalam berbagai format.

## Prasyarat

Sebelum kita memulai perjalanan pembelajaran ini, pastikan Anda memiliki prasyarat berikut:

-  Aspose.Drawing untuk .NET: Pastikan Anda telah menginstal perpustakaan. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/drawing/net/).

- Lingkungan .NET: Tutorial ini mengasumsikan Anda memiliki pengetahuan tentang pengembangan .NET.

Sekarang kita sudah siap, mari jelajahi namespace penting dan pelajari panduan langkah demi langkah.

## Impor Namespace

Di proyek .NET Anda, mulailah dengan mengimpor namespace yang diperlukan:

```csharp
using System.Drawing;
```

Namespace ini menyediakan kelas dan metode dasar yang diperlukan untuk manipulasi gambar.

## Langkah 1: Memuat Gambar

Mari kita mulai dengan memuat gambar. Contoh ini memuat gambar dalam berbagai format seperti BMP, GIF, JPG, PNG, dan TIFF.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## Langkah 2: Menerapkan Metode LoadAndSave

 Sekarang, uraikan`LoadAndSave` metode menjadi beberapa langkah:

### Langkah 2.1: Muat Gambar

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Langkah 2.2: Simpan Gambar

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Simpan gambarnya
    loadedImage.Save(outputPath);
}
```

Ulangi langkah-langkah ini untuk setiap format gambar yang ingin Anda dukung.

## Kesimpulan

Selamat! Anda telah menguasai seni memuat dan menyimpan gambar menggunakan Aspose.Drawing untuk .NET. Keterampilan ini sangat berharga bagi pengembang yang bekerja dengan beragam format gambar. Eksperimen, jelajahi, dan integrasikan pengetahuan ini ke dalam proyek Anda.

## FAQ

### Q1: Apakah Aspose.Drawing kompatibel dengan semua format gambar?

A1: Aspose.Drawing mendukung berbagai format, termasuk BMP, GIF, JPG, PNG, dan TIFF.

### Q2: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.Drawing?

A2: Lihat dokumentasi resminya[Di Sini](https://reference.aspose.com/drawing/net/).

### Q3: Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.Drawing?

 A3: Kunjungi[Di Sini](https://purchase.aspose.com/temporary-license/) untuk rincian lisensi sementara.

### Q4: Bagaimana jika saya menemui masalah atau memiliki pertanyaan selama penerapan?

 A4: Carilah bantuan dari komunitas Aspose.Drawing di[Asumsikan Forum](https://forum.aspose.com/c/diagram/17).

### Q5: Di mana saya dapat membeli perpustakaan Aspose.Drawing?

 A5: Anda bisa membelinya[Di Sini](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
