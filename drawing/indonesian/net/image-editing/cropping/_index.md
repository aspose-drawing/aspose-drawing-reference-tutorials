---
date: 2026-10-13
description: Pelajari cara memotong gambar secara batch ke PNG menggunakan Aspose.Drawing
  API, alternatif lintas‑platform untuk System.Drawing bagi pengembang .NET.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: Tutorial memotong gambar – Aspose.Drawing
og_description: Pelajari cara memotong gambar secara batch ke PNG dengan cepat menggunakan
  Aspose.Drawing, alternatif lintas‑platform untuk System.Drawing bagi pengembang
  .NET. Ikuti petunjuk langkah demi langkah untuk memproses banyak file secara efisien.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Cara memotong gambar secara batch ke PNG dengan Aspose.Drawing untuk .NET
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Cara memotong gambar secara batch ke PNG menggunakan Aspose.Drawing untuk .NET
url: /id/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara memotong gambar secara batch menjadi PNG menggunakan Aspose.Drawing untuk .NET

Jika Anda perlu **memotong gambar menjadi PNG** dengan cepat, andal, dan dalam skala besar di lingkungan .NET, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan menjelaskan langkah‑langkah tepat untuk memuat gambar, menentukan area pemotongan, dan menyimpan hasilnya sebagai file PNG—semua menggunakan Aspose.Drawing, **alternatif modern untuk System.Drawing** yang bekerja lintas‑platform. Anda juga akan melihat cara memperluas alur satu gambar menjadi **pipeline pemotongan batch** lengkap.

## Jawaban Cepat
- **Perpustakaan apa yang harus saya gunakan?** Aspose.Drawing untuk .NET (alternatif lengkap untuk System.Drawing.Common)  
- **Berapa lama pemotongan dasar berlangsung?** Biasanya kurang dari satu detik untuk satu gambar pada CPU modern  
- **Bisakah saya memotong menjadi PNG?** Ya – simpan bitmap yang dipotong sebagai file PNG (lihat Langkah 6)  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi  
- **Apakah pemrosesan batch memungkinkan?** Tentu – bungkus langkah‑langkah yang sama dalam loop untuk memproses banyak file dalam hitungan detik  

## Cara memotong gambar secara batch menjadi PNG?

Muat setiap file sumber dengan `new Bitmap(path)`, buat `Bitmap` kosong yang cocok untuk area pemotongan, gambar persegi panjang yang dipilih menggunakan `Graphics.DrawImage`, dan akhirnya panggil `Save("output.png", ImageFormat.Png)`. Bungkus enam baris ini dalam loop `foreach` yang mengiterasi sebuah direktori dan Anda akan memiliki solusi pemotongan batch lengkap yang memproses puluhan gambar dalam hitungan detik.

## Mengapa menggunakan Aspose.Drawing untuk pemotongan batch?

Aspose.Drawing berjalan di **Windows, Linux, dan macOS**, memproses **gambar lebih dari 500 piksel dalam kurang dari 0,5 detik** pada CPU kelas server tipikal, dan mendukung **lebih dari 50 format gambar** dengan preservasi saluran alfa penuh. Karena menghilangkan ketergantungan native GDI+, Anda dapat menyebarkan kode yang sama ke kontainer, Azure App Service, atau AWS Lambda tanpa perpustakaan tambahan, menjadikannya ideal untuk pipeline gambar berskala besar.

## Apa itu “crop image to PNG”?

Operasi `crop image to PNG` mengekstrak wilayah persegi panjang dari bitmap sumber dan menuliskan wilayah tersebut ke file PNG. PNG mempertahankan saluran alfa apa pun, memberikan kompresi lossless, yang membuat gambar hasilnya ideal untuk thumbnail, ikon, aset UI, atau situasi apa pun yang memerlukan kualitas dan transparansi.

## Mengapa Aspose.Drawing menjadi alternatif untuk System.Drawing?

Aspose.Drawing berfungsi sebagai pengganti langsung untuk System.Drawing dengan menawarkan kompatibilitas lintas‑platform penuh, menghilangkan kebutuhan akan perpustakaan native GDI+. Ia mendukung berbagai format piksel, memberikan manipulasi gambar berperforma tinggi, dan menyertakan fitur lanjutan seperti penanganan saluran alfa serta dukungan format yang luas, menjadikannya cocok untuk penyuntingan sederhana maupun pemrosesan batch berskala besar.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki:
- **Perpustakaan Aspose.Drawing** terintegrasi ke dalam proyek .NET Anda. Anda dapat mengunduhnya dari [halaman unduhan Aspose.Drawing](https://releases.aspose.com/drawing/net/).  
- Sebuah folder yang berisi gambar sumber yang ingin Anda potong. Ganti `"Your Document Directory"` dalam potongan kode dengan jalur sebenarnya di mesin Anda.

## Impor namespace

Namespace `System.Drawing` memberi kita akses ke `Bitmap`, `Graphics`, dan tipe terkait yang diperluas oleh Aspose.Drawing.

```csharp
using System.Drawing;
```

## Panduan langkah‑demi‑langkah

### Langkah 1: Buat kanvas bitmap

`Bitmap` adalah representasi gambar dalam memori Aspose.Drawing, menyediakan akses tingkat piksel dan kontrol format.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Kami memulai dengan kanvas kosong berukuran untuk menampung hasil pemotongan. Sesuaikan lebar dan tinggi agar cocok dengan dimensi area yang akan Anda ekstrak.

### Langkah 2: Buat objek graphics

`Graphics` adalah permukaan gambar yang memungkinkan Anda menggambar bentuk, teks, atau gambar lain ke dalam Bitmap.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Objek `Graphics` memungkinkan kita menggambar pada kanvas. `InterpolationMode` mengontrol bagaimana nilai piksel dihitung selama skala atau transformasi—`NearestNeighbor` bekerja baik untuk tepi yang tajam.

### Langkah 3: Muat gambar yang akan dipotong

`Image` (atau `Bitmap`) memuat file sumber ke dalam memori, siap untuk dimanipulasi.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Muat gambar sumber. Pastikan jalur mengarah ke file yang ada; jika tidak, akan terjadi pengecualian.

### Langkah 4: Tentukan persegi panjang sumber dan tujuan

Objek `Rectangle` menggambarkan wilayah gambar sumber yang akan dipertahankan dan dimana wilayah tersebut harus ditempatkan pada kanvas tujuan.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` memberi tahu API bagian mana dari gambar asli yang akan dipertahankan. Di sini kami memilih area 50 × 40 piksel di kiri‑atas. Dengan menetapkan persegi panjang yang sama ke `destinationRectangle`, kami menjaga wilayah yang dipotong pada ukuran aslinya.

### Langkah 5: Lakukan operasi pemotongan

`Graphics.DrawImage` menyalin bagian yang telah ditentukan dari `image` ke `bitmap` kosong kami.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

Ini adalah operasi inti **crop image to PNG**. Metode ini menghormati persegi panjang sumber dan menuliskan hanya piksel yang dipilih ke bitmap tujuan.

### Langkah 6: Simpan gambar yang dipotong (crop image to PNG)

`Bitmap.Save` menuliskan bitmap dalam memori ke sebuah file menggunakan format yang ditentukan.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Akhirnya, tulis kanvas ke disk sebagai file PNG. PNG mempertahankan saluran alfa apa pun dan memberikan kualitas lossless—ideal untuk aset UI.

## Cara memotong gambar secara batch dalam loop?

Iterasi setiap jalur file dengan `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, ulangi Langkah 1‑6 di dalam loop, dan simpan setiap hasil ke folder target. Pola ini berskala linear, dapat diparalelisasi dengan `Parallel.ForEach` untuk throughput yang lebih cepat, dan memproses gambar secara efisien dan cepat.

## Kesalahan umum & tips
- **Ketidaksesuaian format piksel** – pastikan gambar sumber dan bitmap kanvas memiliki format piksel yang kompatibel untuk menghindari pergeseran warna.  
- **Pembuangan objek GDI** – bungkus `Bitmap` dan `Graphics` dalam pernyataan `using` atau panggil `Dispose()` secara manual; jika tidak, Anda dapat mengalami kebocoran sumber daya yang tidak dikelola.  
- **Kesalahan koordinat** – koordinat persegi panjang berbasis nol. Memilih persegi panjang yang melebihi batas gambar sumber akan memicu pengecualian.  

## Pertanyaan yang sering diajukan

**Q: Bisakah saya memotong gambar dalam format apa pun menggunakan Aspose.Drawing?**  
A: Ya, Aspose.Drawing mendukung berbagai format (PNG, JPEG, BMP, GIF, TIFF, dll.), sehingga Anda dapat memotong hampir semua jenis gambar.

**Q: Apakah ada opsi pemotongan lanjutan yang tersedia?**  
A: Tentu. Anda dapat menggabungkan `GraphicsPath`, transformasi `Matrix`, atau menggunakan kelas `ImageProcessor` untuk seleksi yang lebih kompleks seperti pemotongan melingkar.

**Q: Bisakah saya menerapkan beberapa operasi pemotongan pada satu gambar?**  
A: Ya. Setelah pemotongan pertama, Anda dapat menggunakan bitmap hasil sebagai sumber baru dan mengulangi proses untuk menambahkan beberapa pemotongan.

**Q: Apakah Aspose.Drawing cocok untuk pemrosesan gambar batch?**  
A: Memang. API yang ringan dan tidak adanya ketergantungan native menjadikannya sempurna untuk memproses koleksi gambar besar di server.

**Q: Bagaimana saya dapat mendapatkan dukungan untuk pertanyaan terkait Aspose.Drawing?**  
A: Kunjungi [Forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) untuk mencari bantuan dan terhubung dengan komunitas.

---

**Terakhir Diperbarui:** 2026-10-13  
**Diuji Dengan:** Aspose.Drawing 24.11 untuk .NET  
**Penulis:** Aspose

## Tutorial Terkait

- [Muat, Konversi BMP ke PNG dan Format Lain dengan Aspose.Drawing](/drawing/net/image-editing/load-save/)
- [Cara Melisensikan Aspose.Drawing untuk .NET – cara melisensikan aspose.drawing](/drawing/net/licensing/)
- [Cara Menggambar Persegi Panjang – Transformasi Sistem Koordinat (Transformasi Halaman) menggunakan Aspose.Drawing API untuk .NET](/drawing/net/coordinate-transformations/page-transformation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}