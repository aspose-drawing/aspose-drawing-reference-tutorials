---
title: Menambahkan Teks pada Gambar di Aspose.Drawing
linktitle: Menambahkan Teks pada Gambar di Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternatif untuk System.Drawing.Common
description: Jelajahi integrasi teks ke dalam gambar dengan Aspose.Drawing for .NET. Ikuti panduan langkah demi langkah kami untuk manipulasi gambar yang mudah. Unduh sekarang!
type: docs
weight: 12
url: /id/net/use-cases/text-on-image/
---
## Perkenalan
Dalam dunia pengembangan .NET yang dinamis, Aspose.Drawing menonjol sebagai alat yang ampuh untuk memanipulasi gambar dengan mudah. Menambahkan teks ke gambar adalah persyaratan umum, baik untuk memberi tanda air, anotasi, atau membuat grafik yang dipersonalisasi. Dalam tutorial ini, kita akan mempelajari cara memanfaatkan Aspose.Drawing untuk mengintegrasikan teks ke dalam gambar Anda dengan mulus menggunakan C#.
## Prasyarat
Sebelum masuk ke tutorial, pastikan Anda memiliki hal berikut:
1.  Aspose.Drawing Library: Unduh dan instal perpustakaan Aspose.Drawing dari[Aspose.Drawing untuk dokumentasi .NET](https://reference.aspose.com/drawing/net/).
2. Lingkungan Pengembangan: Memiliki lingkungan pengembangan .NET yang berfungsi, termasuk Visual Studio atau IDE lain yang kompatibel.
Sekarang, mari kita mulai dengan panduan langkah demi langkah.
## Impor Namespace
Mulailah dengan mengimpor namespace yang diperlukan ke proyek C# Anda:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## Langkah 1: Muat Gambar
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Di sini, kami memuat gambar dari jalur file yang ditentukan dan menginisialisasi objek grafik untuk diproses lebih lanjut.
## Langkah 2: Atur Properti Teks
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Tentukan properti teks seperti warna, font, dan padding. Sesuaikan parameter ini sesuai dengan preferensi Anda.
## Langkah 3: Ukur Ukuran Teks
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Hitung ukuran teks yang diperlukan dengan mengukur setiap kata satu per satu. Hal ini memastikan penempatan yang tepat dan menghindari teks yang tumpang tindih.
## Langkah 4: Gambar Teks pada Gambar
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Sekarang, posisikan teks pada gambar berdasarkan ukuran yang dihitung dan gambarlah menggunakan font dan warna yang ditentukan.
## Langkah 5: Simpan Gambar
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Simpan gambar yang dimodifikasi ke direktori yang Anda inginkan.
Panduan langkah demi langkah ini menunjukkan proses mudah menambahkan teks ke gambar menggunakan Aspose.Drawing untuk .NET. Bereksperimenlah dengan berbagai font, warna, dan konten teks untuk mencapai efek visual yang diinginkan.
## Kesimpulan
Aspose.Drawing menyederhanakan tugas manipulasi gambar di .NET, menyediakan perangkat yang tangguh bagi pengembang. Menambahkan teks ke gambar hanyalah salah satu contoh kemampuannya, yang menunjukkan keserbagunaan perpustakaan dalam menangani elemen grafis.
## Pertanyaan yang Sering Diajukan
### Apakah Aspose.Drawing kompatibel dengan semua format gambar?
 Aspose.Drawing mendukung berbagai format gambar, termasuk format populer seperti JPEG, PNG, dan GIF. Mengacu kepada[dokumentasi](https://reference.aspose.com/drawing/net/) untuk daftar lengkap.
### Bisakah saya menggunakan Aspose.Drawing untuk proyek komersial?
Ya, Aspose.Drawing cocok untuk proyek pribadi dan komersial. Untuk rincian perizinan, kunjungi[halaman pembelian](https://purchase.aspose.com/buy).
### Apakah lisensi sementara tersedia untuk tujuan pengujian?
 Ya, Anda bisa mendapatkan lisensi sementara untuk pengujian dengan mengunjungi[Lisensi Sementara](https://purchase.aspose.com/temporary-license/).
### Di mana saya dapat menemukan dukungan komunitas untuk Aspose.Drawing?
 Terlibat dengan komunitas dan dapatkan dukungan di[Aspose.Forum menggambar](https://forum.aspose.com/c/diagram/17).
### Bagaimana cara memulai Aspose.Drawing?
 Mulailah dengan mengunduh perpustakaan dari[Di Sini](https://releases.aspose.com/drawing/net/) dan jelajahi secara komprehensif[dokumentasi](https://reference.aspose.com/drawing/net/).