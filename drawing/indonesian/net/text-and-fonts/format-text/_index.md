---
date: 2026-07-17
description: Pelajari cara mencegah text overflow dengan mengatur text alignment di
  Aspose.Drawing for .NET dan menambahkan teks ke images. Panduan langkah demi langkah
  dengan contoh.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Atur Text Alignment dengan Aspose.Drawing for .NET
og_description: Mencegah text overflow dengan mengatur text alignment di Aspose.Drawing
  for .NET. Pelajari cara draw string pada image, memusatkan teks dalam rectangle,
  dan menggantikan System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Mencegah Text Overflow – Mengatur Text Alignment dengan Aspose.Drawing for
  .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Mencegah Text Overflow – Mengatur Text Alignment dengan Aspose.Drawing for
  .NET
url: /id/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mencegah Teks Meluap – Mengatur Perataan Teks dengan Aspose.Drawing

## Pendahuluan

Ketika Anda perlu **mencegah teks meluap** saat merender grafik di .NET, Aspose.Drawing memberi Anda kontrol halus atas penempatan teks, perataan, dan pembungkusannya. Baik Anda membangun generator lencana, laporan dinamis, atau output berbasis gambar apa pun, menguasai perataan teks memastikan teks Anda tetap berada di dalam persegi panjang yang dimaksud dan terlihat rapi. Dalam panduan ini kami akan menelusuri pembuatan kanvas bitmap, mengonfigurasi `StringFormat`, menggambar persegi panjang dengan teks terpusat, menangani meluap, dan akhirnya menyimpan gambar.

## Jawaban Cepat
- **Apa arti “set text alignment”?** Ini mendefinisikan bagaimana teks diposisikan secara horizontal dan vertikal di dalam sebuah rectangle gambar.  
- **Kelas mana yang mengontrol perataan?** `StringFormat` memungkinkan Anda mengatur `Alignment` dan `LineAlignment`.  
- **Bisakah saya menggambar string dan rectangle secara bersamaan?** Ya—gunakan `Graphics.DrawRectangle` diikuti dengan `Graphics.DrawString`.  
- **Bagaimana cara mencegah teks meluap?** Sesuaikan ukuran rectangle atau bagi teks menjadi beberapa baris secara manual.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial Aspose.Drawing diperlukan untuk penggunaan non‑evaluasi.

## Apa itu **set text alignment** dalam Aspose.Drawing?

`set text alignment` mengonfigurasi penempatan horizontal (`StringAlignment`) dan vertikal (`LineAlignment`) teks dalam `Rectangle` atau wilayah gambar. Dengan menyesuaikan properti ini Anda mengontrol apakah teks muncul rata kiri, terpusat, rata kanan, rata atas, tengah, atau rata bawah, memungkinkan tata letak yang tepat dalam grafik, lencana, dan laporan yang dihasilkan dengan Aspose.Drawing.

## Mengapa menggunakan Aspose.Drawing untuk perataan teks?

Aspose.Drawing menghilangkan keterbatasan GDI+ yang mengganggu `System.Drawing.Common`. Ia mendukung **5 runtime .NET utama** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6, dan .NET 7 – dan dapat merender gambar hingga **4000 × 4000 px** (≈ 100 MB) tanpa menghabiskan memori. Anti‑aliasing, penskalaan DPI tinggi, dan kompatibilitas penuh dengan kontainer Linux memungkinkan Anda menghasilkan grafik pixel‑perfect dalam skenario penyebaran apa pun.

## Prasyarat

1. **Aspose.Drawing Library** – unduh di [sini](https://releases.aspose.com/drawing/net/).  
2. **Development Environment** – Visual Studio 2022 (atau IDE C# apa pun).  
3. **Basic .NET knowledge** – Anda harus nyaman dengan proyek C# dan paket NuGet.

## Mengimpor Namespace

Untuk memulai, bawa namespace yang diperlukan ke dalam ruang lingkup. Ini memberi Anda akses ke grafik, perenderan teks, dan primitif menggambar.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Cara mencegah teks meluap dengan Aspose.Drawing?

Bitmap adalah kelas yang mewakili gambar yang disimpan dalam memori, sementara `RectangleF` mendefinisikan area persegi panjang titik mengambang untuk menggambar. Dengan menggunakan `StringFormat` yang memiliki `Trimming` diatur ke `StringTrimming.EllipsisCharacter`, karakter berlebih secara otomatis diganti dengan elipsis, memastikan teks tidak pernah melampaui batas persegi panjang. Mengukur string terlebih dahulu memungkinkan Anda memutuskan apakah akan memperkecil rectangle atau membagi teks menjadi beberapa baris, menjamin tata letak bersih tanpa tumpahan.

Muat bitmap Anda, definisikan `RectangleF` dengan ukuran yang tepat, dan gunakan `StringFormat` dengan `Trimming` diatur ke `StringTrimming.EllipsisCharacter` untuk secara otomatis memotong karakter berlebih. Untuk kontrol penuh, ukur string dengan `Graphics.MeasureString` dan perkecil rectangle atau bagi teks menjadi baris sebelum menggambar. Pendekatan ini menjamin tidak ada karakter yang meluber di luar batas visual.

## Langkah 1: Buat Objek Bitmap dan Graphics  

Bitmap mewakili gambar dalam memori, sementara Graphics menyediakan metode menggambar untuk bitmap tersebut. Membuat bitmap memberikan kanvas yang dapat Anda gambar. Objek `Graphics` adalah permukaan menggambar, dan kami mengaktifkan perenderan teks berkualitas tinggi dengan `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Langkah 2: Definisikan **StringFormat** dan Styling  

StringFormat menentukan opsi tata letak teks seperti perataan, spasi baris, dan pemotongan. Di sini kami **set text alignment** dengan mengonfigurasi instance `StringFormat`. Kami juga menyiapkan brush, pen, dan font yang akan digunakan saat menggambar string.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Langkah 3: Buat dan Format Teks – **how to draw string** dan **draw rectangle with text**

Graphics.DrawString merender teks ke kanvas, dan Graphics.DrawRectangle menggambar bentuk persegi panjang. Kami menyusun teks, mendefinisikan rectangle yang akan menampungnya, dan kemudian menggambar baik batas rectangle maupun string itu sendiri.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Cara menangani teks meluap

Jika `text` yang diberikan melampaui batas rectangle, Anda memiliki dua opsi umum:

1. **Ubah ukuran rectangle** – tingkatkan `rectangle.Width` atau `rectangle.Height`.  
2. **Bagi teks** – pecah string menjadi baris yang sesuai, lalu panggil `DrawString` untuk setiap baris dengan koordinat Y yang disesuaikan.

## Cara menggambar string pada gambar menggunakan Aspose.Drawing?

Graphics.DrawString menggambar teks yang ditentukan menggunakan font dan opsi pemformatan. Instansiasi objek `Graphics` dari bitmap Anda, lalu panggil `DrawString` dengan `StringFormat` yang telah dipersiapkan. Pemanggilan tunggal ini merender teks tepat di tempat yang Anda inginkan, menghormati perataan, pemotongan, dan matriks transformasi apa pun yang telah Anda terapkan. Menambahkan petunjuk perenderan berkualitas tinggi memastikan output tetap tajam pada tampilan DPI tinggi.

## Cara memusatkan teks dalam rectangle?

StringAlignment menentukan perataan horizontal teks dalam rectangle tata letak. Atur `stringFormat.Alignment = StringAlignment.Center` dan `stringFormat.LineAlignment = StringAlignment.Center`. Ini memusatkan teks secara horizontal dan vertikal di dalam rectangle, menjadikannya ideal untuk lencana, tombol, atau overlay label. Penempatan terpusat berfungsi konsisten di berbagai ukuran gambar dan pengaturan DPI, memberikan tampilan visual yang seimbang.

## Cara mencapai perataan teks vertikal?

LineAlignment mengontrol penempatan vertikal teks di dalam rectangle. Gunakan `stringFormat.LineAlignment` dengan nilai `StringAlignment.Near`, `Center`, atau `Far` untuk menempatkan teks di atas, tengah, atau bawah rectangle. Gabungkan ini dengan `Graphics.TranslateTransform` jika Anda perlu memutar teks sambil mempertahankan perataan vertikal. Menyesuaikan line alignment memastikan blok multi‑baris berbaris tepat di tempat yang Anda harapkan, bahkan setelah transformasi.

## Langkah 4: Simpan Output – **add text to image**

Akhirnya, tulis bitmap ke disk. Langkah ini mendemonstrasikan **add text to image** dalam satu panggilan.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Teks terlihat buram** | Pastikan `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` sudah diatur. |
| **Teks terpotong** | Perbesar ukuran rectangle atau aktifkan logika word‑wrap dengan mengukur ukuran string (`Graphics.MeasureString`). |
| **Font tidak ditemukan** | Verifikasi font terpasang di mesin host atau sematkan font pribadi menggunakan `PrivateFontCollection`. |
| **Warna tidak terduga** | Periksa kembali warna brush dan pen; ingat bahwa `Color.FromKnownColor` menggunakan warna yang didefinisikan sistem. |

## Pertanyaan yang Sering Diajukan

**Q1: Apakah Aspose.Drawing kompatibel dengan semua versi .NET?**  
A1: Ya, Aspose.Drawing dirancang untuk kompatibel dengan berbagai versi .NET, memastikan fleksibilitas bagi pengembang.

**Q2: Bisakah saya menyesuaikan gaya font lebih lanjut?**  
A2: Tentu! Sesuaikan parameter objek `Font` untuk mendapatkan ukuran, gaya, dan keluarga font yang diinginkan.

**Q3: Bagaimana saya dapat menangani teks meluap dalam rectangle yang ditentukan?**  
A3: Anda dapat mengelola teks meluap dengan menyesuaikan ukuran rectangle atau menerapkan logika khusus untuk menangani teks yang panjang.

**Q4: Apakah ada opsi pemformatan lain yang tersedia di Aspose.Drawing?**  
A4: Ya, Aspose.Drawing menyediakan rangkaian lengkap alat untuk manipulasi grafis, termasuk berbagai opsi pemformatan untuk teks, bentuk, dan lainnya.

**Q5: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.Drawing?**  
A5: Jelajahi forum Aspose.Drawing [di sini](https://forum.aspose.com/c/drawing/44) untuk dukungan komunitas dan diskusi.

**Pertanyaan Tambahan**

**Q: Bagaimana cara menggambar string tanpa rectangle di sekitarnya?**  
A: Hilangkan pemanggilan `DrawRectangle` dan berikan lokasi `PointF` yang diinginkan ke `Graphics.DrawString`.

**Q: Bisakah saya memutar teks sambil mempertahankan perataan?**  
A: Ya—terapkan transformasi `Matrix` pada objek `Graphics` sebelum menggambar, kemudian reset setelahnya.

**Q: Apakah memungkinkan mengekspor gambar sebagai JPEG bukan PNG?**  
A: Cukup ubah ekstensi file di `bitmap.Save` dan opsional tentukan `ImageFormat.Jpeg`.

---

**Terakhir Diperbarui:** 2026-07-17  
**Diuji Dengan:** Aspose.Drawing 24.11 for .NET  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Cara Menggambar Teks dengan Aspose.Drawing untuk .NET](/drawing/net/text-and-fonts/draw-text/)
- [Menambahkan Teks pada Gambar di Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [Cara Menggambar Teks dan Font dengan Aspose.Drawing untuk .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}