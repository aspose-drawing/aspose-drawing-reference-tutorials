---
date: 2025-12-06
description: Pelajari cara menyimpan file gambar PNG sambil menampilkan daftar font
  yang terpasang, menunjukkan keluarga font, membuat grafik dari bitmap, dan menggambar
  teks dengan font menggunakan Aspose.Drawing untuk .NET.
language: id
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Simpan Gambar PNG dan Bekerja dengan Font yang Terpasang di Aspose.Drawing
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan Gambar PNG dan Bekerja dengan Font yang Terpasang di Aspose.Drawing

## Pendahuluan

Jika Anda perlu **menyimpan gambar PNG** yang juga menampilkan informasi tentang font yang terpasang pada mesin, Aspose.Drawing untuk .NET memberikan cara yang bersih dan lintas‑platform untuk melakukannya. Dalam tutorial ini kami akan menelusuri cara menampilkan daftar font yang terpasang, memperlihatkan keluarga font, membuat grafik dari bitmap, dan menggambar teks dengan font — semua sambil akhirnya menyimpan hasilnya sebagai gambar PNG. Pada akhir tutorial Anda akan memiliki potongan kode yang dapat digunakan kembali di proyek .NET mana pun.

## Jawaban Cepat
- **Apa yang dibuat tutorial ini?** Gambar PNG yang menampilkan daftar keluarga font yang terpasang.  
- **Perpustakaan apa yang diperlukan?** Aspose.Drawing untuk .NET (tidak memerlukan System.Drawing.Common).  
- **Apakah saya dapat menggunakan font khusus?** Ya – cukup muat mereka ke dalam `InstalledFontCollection`.  
- **Apakah resolusi output dapat disesuaikan?** Tentu – ubah ukuran bitmap atau format piksel.  
- **Apakah saya memerlukan lisensi untuk menjalankan kode?** Lisensi sementara berfungsi untuk evaluasi; lisensi penuh diperlukan untuk produksi.

## Apa itu “menyimpan gambar PNG” dalam konteks Aspose.Drawing?
Menyimpan gambar PNG berarti merender permukaan gambar Anda (sebuah `Bitmap`) ke file dengan ekstensi `.png`. Aspose.Drawing menangani proses enkoding, jadi Anda hanya perlu memanggil `bitmap.Save(...)` dengan jalur yang diinginkan.

## Mengapa menampilkan daftar font yang terpasang dan memperlihatkan keluarga font?
Mengetahui font apa saja yang tersedia memungkinkan Anda membuat grafik dinamis yang menyesuaikan dengan lingkungan pengguna akhir. Ini sangat berguna untuk menghasilkan laporan, sertifikat, atau konten visual apa pun yang harus mencerminkan identitas merek perusahaan tanpa harus menyertakan file font.

## Prasyarat

- **Perpustakaan Aspose.Drawing** – unduh versi terbaru dari [halaman unduhan Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider, atau editor lain yang kompatibel dengan .NET.  
- **Pengetahuan dasar C#** – Anda sebaiknya nyaman dengan kelas, objek, dan perulangan sederhana.

## Mengimpor Namespace
Untuk bekerja dengan font dan grafik, impor namespace berikut di bagian atas file C# Anda:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Buat bitmap (kanvas)
Pertama, kami membuat bitmap yang akan menampung gambar akhir. Ukuran bitmap dan format piksel menentukan kualitas PNG yang disimpan.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Langkah 2: Buat grafik dari bitmap
Selanjutnya, kami memperoleh objek `Graphics` dari bitmap. Objek ini memungkinkan kami menggambar bentuk, teks, dan gambar ke kanvas.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Langkah 3: Siapkan kuas dan font (menggambar teks dengan font)
Kami memerlukan kuas untuk warna teks dan objek `Font` yang mendefinisikan jenis huruf, ukuran, serta gaya.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Langkah 4: Daftar font yang terpasang dan tampilkan keluarga font
Sekarang kami menampilkan jumlah keluarga font dan beberapa nama pertama langsung pada bitmap. Ini mendemonstrasikan kemampuan **list installed fonts** dan **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Langkah 5: Simpan gambar PNG
Akhirnya, kami menulis bitmap ke disk sebagai file PNG. Inilah operasi inti **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Tip pro:** Gunakan `Path.Combine` untuk membangun jalur file agar terhindar dari masalah pemisah direktori pada sistem operasi yang berbeda.

## Masalah Umum dan Solusinya
| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **Tidak ada font yang ditampilkan** | `InstalledFontCollection` tidak terisi (misalnya, dijalankan pada server tanpa tampilan grafis). | Pasang font yang diperlukan pada server atau sematkan font khusus dalam aplikasi Anda. |
| **File yang disimpan rusak** | Format piksel tidak tepat atau izin menulis tidak cukup. | Pastikan folder tujuan ada dan aplikasi memiliki akses menulis; pertahankan `Format32bppPArgb`. |
| **Teks terlihat buram** | Pengaturan DPI rendah. | Tingkatkan dimensi bitmap atau setel `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya menggunakan font khusus yang tidak terpasang di mesin?**  
J: Ya. Muat file font ke dalam `PrivateFontCollection` dan buat `Font` dari koleksi tersebut.

**T: Bagaimana cara menangani pengecualian terkait font?**  
J: Bungkus pembuatan font dalam blok `try/catch` dan periksa `ArgumentException` untuk keluarga yang tidak ditemukan.

**T: Apakah Aspose.Drawing cocok untuk aplikasi web?**  
J: Tentu. Perpustakaan ini bekerja di ASP.NET Core, Azure Functions, dan lingkungan server‑side lainnya.

**T: Bisakah saya mengubah warna atau gaya teks?**  
J: Ya. Gunakan tipe `Brush` yang berbeda (misalnya `LinearGradientBrush`) dan ubah enum `FontStyle`.

**T: Di mana saya dapat memperoleh lisensi sementara untuk pengujian?**  
J: Unduh lisensi percobaan dari [halaman lisensi sementara Aspose](https://purchase.aspose.com/temporary-license/).

## Kesimpulan

Dengan mengikuti langkah‑langkah ini Anda telah belajar cara **menyimpan gambar PNG** yang secara dinamis **menampilkan daftar font yang terpasang**, **menunjukkan keluarga font**, **membuat grafik dari bitmap**, dan **menggambar teks dengan font** menggunakan Aspose.Drawing untuk .NET. Jangan ragu untuk bereksperimen dengan font lain, warna, dan ukuran bitmap agar sesuai dengan kebutuhan visual proyek Anda.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2025-12-06  
**Diuji Dengan:** Aspose.Drawing 24.11 untuk .NET  
**Penulis:** Aspose