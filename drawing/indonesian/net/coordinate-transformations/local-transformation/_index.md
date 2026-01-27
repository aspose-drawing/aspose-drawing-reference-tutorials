---
date: 2026-01-27
description: Pelajari cara memutar elips dan mengonversi grafik ke PNG menggunakan
  Aspose.Drawing untuk .NET. Panduan langkah demi langkah dengan contoh kode.
linktitle: Local Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 'Cara Memutar Elips: Transformasi Lokal di Aspose.Drawing untuk .NET'
url: /id/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Memutar Elips: Transformasi Lokal di Aspose.Drawing untuk .NET

## Introduction

Jika Anda perlu **memutar sebuah elips** dalam aplikasi .NET, Aspose.Drawing menyediakan cara yang sederhana dan dapat diandalkan untuk melakukannya. Dalam tutorial ini Anda akan belajar **cara memutar elips** menggunakan matriks transformasi, merender hasilnya, dan akhirnya **mengonversi grafik ke PNG** untuk penyimpanan atau pemrosesan lebih lanjut. Pada akhirnya, Anda akan memiliki pola yang dapat digunakan kembali untuk skenario transformasi lokal apa pun.

## Quick Answers
- **What is a local transformation?** Ini adalah operasi berbasis matriks (rotate, scale, translate, skew) yang diterapkan pada elemen gambar tertentu tanpa memengaruhi seluruh kanvas.  
- **Which library supports it in .NET?** Aspose.Drawing untuk .NET menyediakan API lengkap yang bekerja pada semua versi .NET yang didukung.  
- **Can I save the result as PNG?** Ya—cukup panggil `Bitmap.Save` dengan nama file “.png”, dan Aspose.Drawing akan menangani konversinya.  
- **Do I need a license for development?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk penggunaan produksi.  
- **How long does the implementation take?** Sekitar 10‑15 menit untuk contoh dasar.

## How to rotate ellipse using Aspose.Drawing
Memutar sebuah elips pada dasarnya adalah **memutar sebuah bentuk menggunakan matriks**. Anda membuat sebuah `Matrix`, mengatur sudut rotasi, menentukan titik pusat elips, dan kemudian menerapkan matriks tersebut ke `GraphicsPath`. Ini menjaga rotasi tetap terlokalisasi pada elips sementara sisanya tetap tidak berubah.

## What is “how to apply transformation” in graphics programming?
Menerapkan transformasi berarti memodifikasi sistem koordinat sebuah objek gambar menggunakan **Matrix**. Matriks mendefinisikan bagaimana titik‑titik diputar, diskalakan, atau dipindahkan, memungkinkan Anda membuat efek visual yang canggih dengan kode yang minimal.

## Why use Aspose.Drawing to **convert graphics to PNG**?
- **Cross‑platform**: Berfungsi pada .NET Framework, .NET Core, dan .NET 5/6+.  
- **No GDI+ dependencies**: Menghindari masalah `System.Drawing.Common` pada platform non‑Windows.  
- **High‑quality rendering**: Anti‑aliasing dan output pixel‑perfect untuk file PNG.  
- **Rich API**: Dukungan penuh untuk path, pen, brush, dan matriks transformasi.

## Prerequisites

Sebelum Anda memulai, pastikan Anda memiliki:

1. **Aspose.Drawing for .NET** – unduh dan instal dari [download link](https://releases.aspose.com/drawing/net/).  
2. Sebuah folder di mesin Anda tempat gambar output akan disimpan (misalnya, `C:\MyImages\`).  
3. Familiaritas dasar dengan C# dan pengaturan proyek .NET.  

## Import Namespaces

Pertama, masukkan namespace yang diperlukan ke dalam file C# Anda:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Namespace ini memberi Anda akses ke kelas `Bitmap`, `Graphics`, `GraphicsPath`, dan `Matrix` yang dibutuhkan untuk alur kerja transformasi.

## Step‑by‑Step Guide

### Step 1: Create a Bitmap

Kami memulai dengan kanvas kosong. Ukuran bitmap dan format piksel dipilih untuk memberikan gambar 32‑bit berkualitas tinggi yang mendukung transparansi alfa.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Pro tip:** Menggunakan `Format32bppPArgb` memastikan gambar mempertahankan alfa yang telah dipremultiplikasi, yang ideal untuk output PNG.

### Step 2: Create a Graphics Object

Objek `Graphics` menyediakan metode menggambar yang beroperasi pada bitmap. Kami membersihkan latar belakang menjadi abu‑abu netral sehingga bentuk yang ditransformasi menonjol.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Step 3: Create a GraphicsPath

`GraphicsPath` memungkinkan Anda mendefinisikan bentuk kompleks. Di sini kami menambahkan sebuah elips yang diposisikan pada (300, 300) dengan lebar 400 dan tinggi 200.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### Step 4: Apply Local Transformation (rotate shape using matrix)

Sekarang kami menjawab pertanyaan inti: **cara memutar elips**. Kami membuat sebuah `Matrix`, memutarnya 45° di sekitar pusat elips (500, 400), dan menerapkan matriks tersebut ke path.

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **Why rotate at a point?** Memutar di sekitar pusat bentuk mencegahnya berorbit di sekitar asal, memberikan tampilan yang natural.

### Step 5: Draw the Transformed Path

Dengan transformasi yang sudah diterapkan, kami merender path menggunakan pena biru dengan ketebalan 2.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### Step 6: Save the Transformed Image (convert graphics to PNG)

Akhirnya, kami menyimpan bitmap sebagai file PNG. Path menggabungkan direktori pilihan Anda dengan sub‑folder untuk contoh transformasi.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **Note:** Baris ini juga menunjukkan cara **menyimpan bitmap sebagai PNG**. Ekstensi `.png` secara otomatis memicu encoder PNG Aspose.Drawing, memenuhi kebutuhan **convert graphics to PNG**.

## Common Issues & Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Blank output image** | Graphics tidak dibersihkan atau warna pena sama dengan latar belakang | Panggil `graphics.Clear` dengan warna kontras dan pastikan warna pena terlihat. |
| **Distorted rotation** | Menggunakan `Rotate` alih‑alih `RotateAt` | Gunakan `RotateAt` dan tentukan titik pusat bentuk. |
| **File not saved** | Path direktori tidak valid atau tidak ada izin menulis | Pastikan direktori ada dan aplikasi memiliki akses menulis. |
| **PNG appears fuzzy** | Pengaturan DPI bitmap terlalu rendah | Buat bitmap dengan resolusi lebih tinggi atau set `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Frequently Asked Questions

**Q:** Can I chain multiple transformations (e.g., scale then rotate)?  
**A:** Yes. Create a single `Matrix` and call methods like `Scale`, `RotateAt`, and `Translate` in the order you need, then apply it with `path.Transform(matrix);`.

**Q:** Is Aspose.Drawing suitable for high‑performance rendering?  
**A:** Absolutely. The library is optimized for both speed and quality, and it avoids the GDI+ limitations on non‑Windows platforms.

**Q:** What other transformation types are supported?  
**A:** Besides rotation, you can perform translation, scaling, and skewing using the same `Matrix` class.

**Q:** How do I handle exceptions during the transformation process?  
**A:** Wrap the drawing code in a `try‑catch` block and inspect `System.Drawing.Drawing2D` exceptions. Refer to the official [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/) for detailed error‑handling guidance.

**Q:** Can I try Aspose.Drawing before purchasing?  
**A:** Yes, a fully functional free trial is available via the [free trial](https://releases.aspose.com/) link.

## Conclusion

Dengan mengikuti panduan ini Anda kini mengetahui **cara memutar elips** menggunakan Aspose.Drawing untuk .NET dan **cara mengonversi grafik ke PNG** untuk penyimpanan permanen. Pola yang sama dapat digunakan kembali untuk scaling, translating, atau skewing bentuk apa pun, memungkinkan Anda membangun komponen visual interaktif yang kaya dalam aplikasi Anda.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-27  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose