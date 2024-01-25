---
title: Menggambar Persegi Panjang di Aspose.Drawing
linktitle: Menggambar Persegi Panjang di Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternatif untuk System.Drawing.Common
description: Pelajari cara menggambar persegi panjang di .NET menggunakan Aspose.Drawing. Panduan langkah demi langkah dengan contoh kode.
type: docs
weight: 19
url: /id/net/lines-curves-and-shapes/draw-rectangle/
---
## Perkenalan

Selamat datang di tutorial komprehensif tentang menggambar persegi panjang menggunakan Aspose.Drawing untuk .NET. Baik Anda seorang pengembang berpengalaman atau pendatang baru di Aspose.Drawing, panduan ini akan memandu Anda melalui proses membuat dan memanipulasi persegi panjang di aplikasi .NET Anda.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

- Perpustakaan Aspose.Drawing: Pastikan Anda telah menginstal perpustakaan Aspose.Drawing untuk .NET. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/drawing/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET yang berfungsi, seperti Visual Studio, di mesin Anda.

- Pengetahuan Dasar .NET: Biasakan diri Anda dengan dasar-dasar pemrograman .NET.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan ke dalam proyek Anda. Namespace berikut penting untuk bekerja dengan operasi grafik dan gambar:

```csharp
using System.Drawing;
```

## Langkah 1: Buat Bitmap

Mulailah dengan membuat objek Bitmap, yang akan berfungsi sebagai permukaan gambar. Atur dimensi dan format piksel sesuai kebutuhan aplikasi Anda.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Langkah 2: Buat Objek Grafik

Selanjutnya, buat objek Grafik dari Bitmap. Objek ini memungkinkan Anda melakukan berbagai operasi menggambar.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Langkah 3: Tentukan Pena untuk Persegi Panjang

Tentukan objek Pena untuk menentukan warna dan ketebalan garis persegi panjang.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## Langkah 4: Gambar Persegi Panjang

Sekarang, gunakan objek Graphics untuk menggambar persegi panjang pada Bitmap menggunakan Pena yang ditentukan. Tentukan posisi dan dimensi persegi panjang.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## Langkah 5: Simpan Gambar

Simpan persegi panjang yang digambar ke file di direktori dokumen Anda atau lokasi mana pun yang diinginkan.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

Selamat! Anda telah berhasil menggambar persegi panjang menggunakan Aspose.Drawing untuk .NET.

## Kesimpulan

Dalam tutorial ini, kita menjelajahi langkah-langkah dasar menggambar persegi panjang di Aspose.Drawing untuk .NET. Pustaka ini menyediakan alat canggih untuk manipulasi grafis, menjadikannya aset berharga bagi pengembang .NET.

 Jika Anda menghadapi tantangan atau memiliki pertanyaan, silakan mencari bantuan di[Aspose.Forum Menggambar](https://forum.aspose.com/c/diagram/17).

## FAQ

### Q1: Bisakah saya menggunakan Aspose.Drawing secara gratis?

 A1: Aspose.Drawing adalah perpustakaan komersial, tetapi Anda dapat menjelajahi fitur-fiturnya dengan a[uji coba gratis](https://releases.aspose.com/).

### Q2: Di mana saya dapat menemukan dokumentasi terperinci?

 A2: Lihat[dokumentasi](https://reference.aspose.com/drawing/net/) untuk informasi mendalam.

### Q3: Bagaimana saya bisa mendapatkan lisensi sementara?

 A3: Dapatkan a[izin sementara](https://purchase.aspose.com/temporary-license/) untuk tujuan pengujian.

### Q4 :. Apakah Aspose.Drawing cocok untuk tugas grafis yang kompleks?

A4: Tentu saja! Aspose.Drawing menyediakan fitur-fitur canggih untuk menangani operasi grafis yang rumit.

### Q5: Dimana saya bisa membeli Aspose.Drawing?

 A5: Kunjungi[Di Sini](https://purchase.aspose.com/buy) untuk membeli lisensi.