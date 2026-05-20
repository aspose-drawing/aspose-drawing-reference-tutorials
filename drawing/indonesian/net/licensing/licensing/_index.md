---
date: 2026-02-09
description: Pelajari cara mengatur lisensi Aspose.Drawing di .NET. Kuasai metode
  lisensi untuk membuka semua fitur tanpa watermark.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Atur Lisensi Aspose.Drawing – Cara Mengatur Lisensi Aspose.Drawing
url: /id/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tetapkan Lisensi Aspose.Drawing

## Perkenalan

Jika Anda membangun aplikasi .NET yang mengandalkan manipulasi grafik dan gambar yang kuat, **menetapkan lisensi Aspose.Drawingapkan** adalah langkah pertama untuk menghilangkan batasan evaluasi dan mengakses seluruh set fitur. Dalam tutorial ini Anda akan mempelajari tiga cara praktis untuk mengatur lisensi Aspose. Menggambar—memuat dari file, memuat dari stream, dan menggunakan model penggunaan bermeter—sehingga Anda dapat mengintegrasikan perpustakaan dengan percaya diri.

## Jawaban Cepat
- **Apa cara utama untuk mengaktifkan Aspose.Drawing?** Muat file lisensi menggunakan `License.SetLicense("Aspose.Drawing.lic")`.
- **Apakah saya dapat menerapkan lisensi saat runtime?** Ya, Anda dapat mengunduh lisensi dari `Stream` untuk skenario dinamis.
- **Apakah lisensi bermeter didukung?** Tentu saja; gunakan `Metered.SetMeteredKey(publicKey, privateKey)` untuk mengaktifkan pengumpulan berbasis konsumsi.
- **Apakah saya memerlukan lisensi untuk membangun pengembangan?** Versi percobaan dapat digunakan untuk pengujian, tetapi lisensi yang valid menghilangkan watermark dan membuka semua API.
- **Versi .NET mana yang kompatibel?** Aspose.Drawing mendukung .NET Framework 4.x, .NET Core 3.1+, dan .NET 5/6+.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Aspose.Drawing Library** – unduh paket terbaru dari [di sini](https://releases.aspose.com/drawing/net/).
- **File Lisensi** – dapatkan file `.lic` yang valid dari [Aspose](https://purchase.aspose.com/buy).
- **.NET Development Environment** – Visual Studio, Rider, atau IDE apa pun yang menargetkan .NETFramework/.NETCore.

## Impor Namespace

Kita memerlukan namespace .NET standar serta namespace Aspose.Drawing untuk lisensi. Tambahkan pernyataan `using` berikut di bagian atas file C# Anda:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Memuat Lisensi dari File

Memuat lisensi dari file adalah pendekatan paling sederhana. Ikuti tiga langkah berikut:

### Langkah 1: Inisialisasi Objek Lisensi

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Langkah 2: Atur Lisensi dari File `.lic`

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Langkah 3: Konfirmasi Sukses

```csharp
Console.WriteLine("License set successfully.");
```

> **Tips pro:** letakkan file `.lic` di folder yang sama dengan executable Anda atau berikan path absolut untuk menghindari error “file not found”.

## Memuat Lisensi dari Aliran

Ketika file lisensi Anda tersemat sebagai sumber daya atau diambil dari lokasi jarak jauh, memuatnya dari `Stream` memberi Anda momen.

### Langkah 1: Inisialisasi Objek Lisensi

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Langkah 2: Muat Lisensi Menggunakan `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Langkah 3: Konfirmasi Sukses

```csharp
Console.WriteLine("License set successfully.");
```

> **Peringatan:** Ingatlah untuk melepaskan `FileStream` (atau gunakan blok `using`) agar pegangan file dibebaskan.

## Menggunakan Lisensi Terukur

Lisensi bermeter ideal untuk skenario SaaS atau bayar per penggunaan. Ia melacak konsumsi dan menagih Anda berdasarkan penggunaan aktual.

### Langkah 1: Inisialisasi Objek Berukuran

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Langkah 2: Tetapkan Kunci Publik dan Pribadi

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Langkah 3: Lakukan Pemrosesan Gambar Anda

```csharp
// Your image processing logic here
```

### Langkah 4: Ambil Informasi Konsumsi

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Langkah 5: Tampilkan Detail Konsumsi

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Perangkap umum:** Jika Anda lupa memanggil `SetMeteredKey`, API akan kembali ke mode percobaan dan Anda akan melihat watermark pada output.

## Mengapa Mengatur Lisensi Aspose.Drawing dengan Benar?

- **Menghilangkan watermark** yang muncul dalam mode percobaan.
- **Membuka API premium** seperti filter gambar lanjutan dan konversi PDF.
- **Menjamin pemenuhan** dengan ketentuan lisensi Aspose untuk distribusi komersial.
- **Mengaktifkan pengumpulan bermeter**, memungkinkan Anda membayar hanya untuk apa yang Anda gunakan.

## Masalah Umum dan Solusinya

| Edisi | Penyebab | Perbaiki |
|-------|-------|-----|
| Kesalahan “File lisensi tidak ditemukan” | Path salah atau file tidak ada di folder output | Gunakan path absolut atau atur properti file *Copy to Output Directory* menjadi *Copy Always*. |
| Watermark masih muncul setelah pembukaan lisensi | Lisensi tidak dimuat sebelum memanggil API pertama | Muat lisensi **sebelum** operasi Aspose.Drawing apa pun. |
| Konsumsi terukur selalu nol | Kunci tidak diet atau variabel lingkungan salah | Verifikasi kunci publik/privat dan pastikan koneksi internet ke server terukur Aspose. |

## Pertanyaan yang Sering Diajukan

**Q1: ​​Bisakah saya menggunakan Aspose.Drawing tanpa lisensi?**
A1: Ya, lisensi percobaan dapat digunakan untuk pengembangan dan evaluasi, tetapi akan menambahkan watermark dan membatasi beberapa fitur.

**Q2: Seberapa sering saya perlu memperbarui lisensi Aspose.Drawing saya?**
A2: Lisensi bersifat abadi untuk versi yang dibeli. Pembaruan hanya diperlukan untuk dukungan dan peningkatan.

**Q3: Apa itu lisensi terukur, dan kapan saya harus menggunakannya?**
A3: Lisensi bermeter menagih berdasarkan penggunaan (operasi atau data yang diproses). Ini sempurna untuk layanan cloud atau model bayar per penggunaan.

**Q4: Dapatkah saya menggunakan Aspose.Drawing dalam proyek komersial?**
A4: Tentu saja—setelah Anda memiliki lisensi yang valid, Anda dapat menyematkan Aspose.Drawing dalam aplikasi komersial apa pun.

**Q5: Di mana saya dapat menemukan dukungan komunitas untuk Aspose.Drawing?**
A5: Kunjungi [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) untuk bantuan komunitas, contoh, dan diskusi.

## Kesimpulan

Menguasai cara **menetapkan lisensi Aspose.Drawing**—baik dari file, stream, atau melalui penggunaan bermeter—memastikan Anda mendapatkan manfaat maksimal dari perpustakaan grafis .NET yang kuat ini. Ikuti langkah‑langkah di atas, perhatikan jebakan umum, dan Anda siap membangun solusi pemrosesan gambar yang handal tanpa hambatan lisensi.

---

**Terakhir Diperbarui:** 2026-02-09
**Diuji Dengan:** Aspose.Drawing 24.11 untuk .NET
**Pengarang:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}