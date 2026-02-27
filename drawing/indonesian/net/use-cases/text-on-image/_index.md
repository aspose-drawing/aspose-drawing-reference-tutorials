---
date: 2026-02-27
description: Pelajari cara membuat gambar kartu ulang tahun menggunakan Aspose.Drawing
  untuk .NET. Panduan ini menunjukkan cara menggambar teks pada gambar, menambahkan
  teks di atas foto, dan menambahkan keterangan pada foto dengan cepat.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cara Membuat Gambar Kartu Ulang Tahun dengan Aspose.Drawing
url: /id/net/use-cases/text-on-image/
weight: 12
---

 lists.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Membuat Gambar Kartu Ulang Tahun dengan Aspose.Drawing

## Pendahuluan
Di dunia .NET yang dinamis, Aspose.Drawing menonjol sebagai alat yang kuat untuk memanipulasi gambar dengan mudah. Baik Anda perlu **membuat gambar kartu ulang tahun**, menambahkan watermark, atau sekadar menimpa teks pada foto, tutorial ini akan memandu Anda melalui langkah‑langkah tepat untuk menggambar string pada gambar menggunakan C#. Pada akhir panduan ini Anda akan memiliki kartu ulang tahun yang dipersonalisasi siap dibagikan.

## Jawaban Cepat
- **Pustaka apa yang harus saya gunakan?** Aspose.Drawing untuk .NET  
- **Bisakah saya menambahkan keterangan pada foto?** Ya – gunakan `Graphics.DrawString` dengan font khusus.  
- **Apakah lisensi diperlukan untuk produksi?** Ya, lisensi komersial diperlukan.  
- **Versi .NET mana yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk kartu sederhana.

## Apa Itu Gambar Kartu Ulang Tahun?
Gambar kartu ulang tahun adalah foto yang dipersonalisasi yang menggabungkan latar belakang dengan teks khusus—seperti ucapan, nama penerima, atau pesan perayaan. Dengan Aspose.Drawing, Anda dapat menghasilkan kartu ini secara programatis tanpa harus menggunakan alat desain grafis manual.

## Mengapa Menggunakan Aspose.Drawing untuk Menimpa Teks pada Foto?
- **Dukungan lintas‑platform:** Berfungsi di Windows, Linux, dan macOS.  
- **API menggambar yang kaya:** Kontrol penuh atas font, warna, dan tata letak.  
- **Tanpa dependensi eksternal:** Menggantikan `System.Drawing.Common` dengan pustaka yang sepenuhnya dikelola.  
- **Kinerja tinggi:** Dioptimalkan untuk pemrosesan gambar dalam jumlah besar.

## Prasyarat
Sebelum masuk ke tutorial, pastikan hal‑hal berikut sudah tersedia:

1. **Pustaka Aspose.Drawing:** Unduh dan instal pustaka Aspose.Drawing dari [dokumentasi Aspose.Drawing untuk .NET](https://reference.aspose.com/drawing/net/).  
2. **Lingkungan Pengembangan:** Lingkungan pengembangan .NET yang berfungsi, seperti Visual Studio atau Visual Studio Code, dengan .NET 6 SDK atau yang lebih baru terpasang.

Sekarang, mari ikuti panduan langkah‑demi‑langkah untuk menambahkan teks ke gambar dan menyimpannya sebagai kartu ulang tahun.

## Impor Namespace
Mulailah dengan mengimpor namespace yang diperlukan ke dalam proyek C# Anda:

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
Di sini, kami memuat gambar dari jalur file yang ditentukan dan menginisialisasi objek graphics untuk pemrosesan selanjutnya.

## Langkah 2: Atur Properti Teks
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Tentukan properti teks seperti warna, font, dan padding. Sesuaikan parameter ini sesuai preferensi desain Anda.

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
Hitung ukuran yang diperlukan untuk teks dengan mengukur setiap kata secara terpisah. Ini memastikan penempatan yang tepat dan menghindari tumpang tindih teks.

## Langkah 4: Gambar Teks pada Gambar
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Sekarang, posisikan teks pada gambar berdasarkan ukuran yang telah dihitung dan gambar menggunakan font serta warna yang ditentukan.

## Langkah 5: Simpan Gambar
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Simpan gambar yang telah dimodifikasi ke direktori yang Anda inginkan. File hasilnya adalah gambar kartu ulang tahun yang siap dikirim.

## Kasus Penggunaan Umum & Tips
- **Tambahkan keterangan pada foto:** Ganti `text` dengan keterangan apa pun yang Anda butuhkan, misalnya “Merayakan 30 Tahun!”.  
- **Gambar teks pada bitmap:** Pendekatan yang sama berlaku untuk objek `Bitmap` yang dibuat dari awal.  
- **Tumpang tindih beberapa baris:** Loop melalui array string dan sesuaikan koordinat Y `Rectangle` untuk setiap baris.  
- **Tip profesional:** Gunakan `Graphics.SmoothingMode = SmoothingMode.AntiAlias` untuk rendering teks yang lebih halus.

## Kesimpulan
Aspose.Drawing menyederhanakan tugas manipulasi gambar di .NET, memberikan pengembang toolkit yang kuat. Menambahkan teks ke gambar—baik untuk **membuat gambar kartu ulang tahun**, **menggambar string pada gambar**, atau **menambahkan keterangan pada foto**—hanya satu contoh dari fleksibilitasnya dalam menangani elemen grafis.

## Pertanyaan yang Sering Diajukan
### Apakah Aspose.Drawing kompatibel dengan semua format gambar?
Aspose.Drawing mendukung berbagai format gambar, termasuk yang populer seperti JPEG, PNG, dan GIF. Lihat [dokumentasi](https://reference.aspose.com/drawing/net/) untuk daftar lengkap.

### Bisakah saya menggunakan Aspose.Drawing untuk proyek komersial?
Ya, Aspose.Drawing cocok untuk proyek pribadi maupun komersial. Untuk detail lisensi, kunjungi [halaman pembelian](https://purchase.aspose.com/buy).

### Apakah lisensi sementara tersedia untuk tujuan pengujian?
Ya, Anda dapat memperoleh lisensi sementara untuk pengujian dengan mengunjungi [Lisensi Sementara](https://purchase.aspose.com/temporary-license/).

### Di mana saya dapat menemukan dukungan komunitas untuk Aspose.Drawing?
Berinteraksilah dengan komunitas dan dapatkan dukungan di [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

### Bagaimana cara memulai dengan Aspose.Drawing?
Mulailah dengan mengunduh pustaka dari [sini](https://releases.aspose.com/drawing/net/) dan jelajahi [dokumentasi lengkapnya](https://reference.aspose.com/drawing/net/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-02-27  
**Diuji Dengan:** Aspose.Drawing 24.11 untuk .NET  
**Penulis:** Aspose  

---