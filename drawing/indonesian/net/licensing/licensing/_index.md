---
date: 2026-05-29
description: Pelajari cara mengatur lisensi Aspose.Drawing di .NET dan menghapus watermark
  Aspose. Kuasai metode lisensi untuk membuka semua fitur tanpa watermark.
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
linktitle: Lisensi di Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  headline: Remove Aspose Watermark – Set Aspose.Drawing License
  type: TechArticle
- description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  name: Remove Aspose Watermark – Set Aspose.Drawing License
  steps:
  - name: Confirm Success
    text: '> **Pro tip:** Place the `.lic` file in the same folder as your executable
      or provide an absolute path to avoid “file not found” errors.'
  - name: Confirm Success
    text: '> **Warning:** Remember to dispose the `FileStream` (or use a `using` block)
      to free file handles.'
  - name: Display the Consumption Details
    text: '> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will
      fall back to trial mode and you’ll see watermarks in the output.'
  type: HowTo
- questions:
  - answer: Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.
    question: What is the primary way to activate Aspose.Drawing?
  - answer: Yes, you can load the license from a `Stream` for dynamic scenarios.
    question: Can I apply a license at runtime?
  - answer: Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable
      consumption‑based billing.
    question: Is a metered license supported?
  - answer: A trial works for testing, but a valid license removes watermarks and
      unlocks all APIs.
    question: Do I need a license for development builds?
  - answer: Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.
    question: Which .NET versions are compatible?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hapus Watermark Aspose – Atur Lisensi Aspose.Drawing
url: /id/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Lisensi Aspose.Drawing

## Pendahuluan

Jika Anda membangun aplikasi .NET yang mengandalkan grafik dan manipulasi gambar yang kuat, **menetapkan lisensi Aspose.Drawing** adalah langkah pertama untuk menghilangkan watermark Aspose dan mengakses seluruh set fitur. Dalam tutorial ini Anda akan mempelajari tiga cara praktis untuk menetapkan lisensi Aspose.Drawing—memuat dari file, memuat dari stream, dan menggunakan model penggunaan bermeter—sehingga Anda dapat mengintegrasikan perpustakaan dengan percaya diri dan menjaga output tetap bersih.

## Jawaban Cepat
- **Apa cara utama untuk mengaktifkan Aspose.Drawing?** Muat file lisensi menggunakan `License.SetLicense("Aspose.Drawing.lic")`.  
- **Bisakah saya menerapkan lisensi saat runtime?** Ya, Anda dapat memuat lisensi dari sebuah `Stream` untuk skenario dinamis.  
- **Apakah lisensi bermeter didukung?** Tentu saja; gunakan `Metered.SetMeteredKey(publicKey, privateKey)` untuk mengaktifkan penagihan berbasis konsumsi.  
- **Apakah saya memerlukan lisensi untuk build pengembangan?** Versi trial dapat digunakan untuk pengujian, tetapi lisensi yang valid menghilangkan watermark dan membuka semua API.  
- **Versi .NET mana yang kompatibel?** Aspose.Drawing mendukung .NET Framework 4.x, .NET Core 3.1+, dan .NET 5/6+.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Aspose.Drawing Library** – unduh paket terbaru dari [here](https://releases.aspose.com/drawing/net/).  
- **License File** – dapatkan file `.lic` yang valid dari [Aspose](https://purchase.aspose.com/buy).  
- **.NET Development Environment** – Visual Studio, Rider, atau IDE apa pun yang menargetkan .NET Framework/.NET Core.

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

## Cara Memuat Lisensi dari File?

Kelas `License` mewakili komponen lisensi Aspose.Drawing yang, ketika diinstansiasi, memungkinkan Anda menerapkan lisensi ke perpustakaan. Memuat lisensi dari file adalah pendekatan paling sederhana; Anda cukup menunjuk metode `SetLicense` ke file `.lic` dan perpustakaan akan menghapus semua watermark trial selama sisa sesi aplikasi. Metode ini berfungsi di lingkungan desktop maupun server dan tidak memerlukan konfigurasi tambahan selain memastikan file dapat diakses pada runtime.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## Cara Memuat Lisensi dari Stream?

Ketika file lisensi disematkan sebagai sumber daya atau diambil melalui jaringan, memuatnya dari sebuah `Stream` memberi Anda fleksibilitas sambil tetap menjamin watermark dihapus. Dengan melewatkan instance `Stream` ke metode `SetLicense`, Anda menjaga lisensi tetap di luar folder deployment, yang dapat meningkatkan keamanan dan menyederhanakan distribusi dalam skenario container atau cloud. Prosesnya identik dengan pemuatan berbasis file, kecuali Anda mengelola siklus hidup stream sendiri.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## Cara Mengaktifkan Lisensi Metered?

Kelas `Metered` menangani aktivasi penggunaan bermeter untuk Aspose.Drawing, memungkinkan penagihan berbasis konsumsi. Lisensi bermeter memungkinkan Anda membayar hanya untuk operasi yang benar‑benar Anda lakukan, yang ideal untuk SaaS atau skenario bayar‑per‑pakai. Setelah Anda menyediakan kunci publik dan privat, setiap panggilan pemrosesan gambar dilacak dan ditagih secara otomatis, dan perpustakaan beroperasi dalam mode fitur penuh tanpa watermark selama sesi.

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## Mengapa Mengatur Lisensi Aspose.Drawing dengan Benar?

Mengatur lisensi dengan benar memastikan perpustakaan berjalan dalam mode fitur penuh, menghapus watermark trial, dan mematuhi ketentuan lisensi Aspose. Lisensi yang diterapkan dengan tepat juga mengaktifkan API premium, meningkatkan kinerja dengan menonaktifkan pemeriksaan evaluasi, serta memungkinkan penagihan bermeter jika diinginkan. Jika lisensi tidak dimuat sebelum pemanggilan API pertama, perpustakaan akan kembali ke mode trial, menghasilkan watermark pada semua gambar yang dihasilkan.

- **Menghapus watermark** yang muncul dalam mode trial.  
- **Membuka kunci API premium** seperti filter gambar lanjutan dan konversi PDF.  
- **Menjamin kepatuhan** dengan ketentuan lisensi Aspose untuk distribusi komersial.  
- **Mengaktifkan penagihan berbasis meter**, memungkinkan Anda membayar hanya untuk apa yang Anda gunakan.  

Aspose.Drawing mendukung **lebih dari 30 format gambar** (termasuk PNG, JPEG, BMP, TIFF, dan WebP) dan dapat memproses **dokumen PDF ratusan halaman tanpa memuat seluruh file ke memori**, memberikan konversi berperforma tinggi pada perangkat keras yang sederhana.

## Memuat Lisensi dari File

Memuat lisensi dari file adalah pendekatan paling sederhana. Ikuti tiga langkah berikut:

### Langkah 1: Inisialisasi Objek Lisensi

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Langkah 2: Atur Lisensi dari File `.lic`

```csharp
Console.WriteLine("License set successfully.");
```

### Langkah 3: Konfirmasi Keberhasilan

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro tip:** Letakkan file `.lic` di folder yang sama dengan executable Anda atau berikan path absolut untuk menghindari kesalahan “file not found”.

## Memuat Lisensi dari Stream

Ketika file lisensi Anda disematkan sebagai sumber daya atau diambil dari lokasi remote, memuatnya dari sebuah `Stream` memberi Anda fleksibilitas.

### Langkah 1: Inisialisasi Objek Lisensi

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Langkah 2: Muat Lisensi Menggunakan `FileStream`

```csharp
Console.WriteLine("License set successfully.");
```

### Langkah 3: Konfirmasi Keberhasilan

```csharp
Console.WriteLine("License set successfully.");
```

> **Warning:** Ingatlah untuk membuang `FileStream` (atau gunakan blok `using`) guna membebaskan handle file.

## Menggunakan Lisensi Metered

Lisensi bermeter ideal untuk SaaS atau skenario bayar‑per‑pakai. Ini melacak konsumsi dan menagih Anda berdasarkan penggunaan aktual.

### Langkah 1: Inisialisasi Objek Metered

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Langkah 2: Atur Kunci Publik dan Privat

```csharp
// Your image processing logic here
```

### Langkah 3: Lakukan Pemrosesan Gambar Anda

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Langkah 4: Ambil Informasi Konsumsi

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### Langkah 5: Tampilkan Detail Konsumsi

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Common pitfall:** Jika Anda lupa memanggil `SetMeteredKey`, API akan kembali ke mode trial dan Anda akan melihat watermark pada output.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| “License file not found” error | Path salah atau file tidak ada di folder output | Gunakan path absolut atau atur properti *Copy to Output Directory* file menjadi *Copy always*. |
| Watermark still appears after setting license | Lisensi tidak dimuat sebelum pemanggilan API pertama | Muat lisensi **sebelum** operasi Aspose.Drawing apa pun. |
| Metered consumption always zero | Kunci tidak diatur atau variabel lingkungan salah | Verifikasi kunci publik/privat dan pastikan konektivitas internet ke server metered Aspose. |

## Pertanyaan yang Sering Diajukan

**Q1: Apakah saya dapat menggunakan Aspose.Drawing tanpa lisensi?**  
A1: Ya, lisensi trial dapat digunakan untuk pengembangan dan evaluasi, tetapi akan menambahkan watermark dan membatasi beberapa fitur.

**Q2: Seberapa sering saya perlu memperpanjang lisensi Aspose.Drawing saya?**  
A2: Lisensi bersifat perpetual untuk versi yang dibeli. Perpanjangan hanya diperlukan untuk dukungan dan pembaruan.

**Q3: Apa itu lisensi metered, dan kapan saya harus menggunakannya?**  
A3: Lisensi metered mengenakan biaya berdasarkan penggunaan (operasi atau data yang diproses). Ini sempurna untuk layanan cloud atau model bayar‑per‑pakai.

**Q4: Apakah saya dapat menggunakan Aspose.Drawing dalam proyek komersial?**  
A4: Tentu saja—setelah Anda memiliki lisensi yang valid, Anda dapat menyematkan Aspose.Drawing dalam aplikasi komersial apa pun.

**Q5: Di mana saya dapat menemukan dukungan komunitas untuk Aspose.Drawing?**  
A5: Kunjungi [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) untuk bantuan komunitas, contoh, dan diskusi.

## Kesimpulan

Menguasai cara **menetapkan lisensi Aspose.Drawing**—baik dari file, stream, atau melalui penggunaan bermeter—memastikan Anda mendapatkan manfaat maksimal dari perpustakaan grafis .NET yang kuat ini sekaligus **menghilangkan watermark Aspose** sepenuhnya. Ikuti langkah‑langkah di atas, perhatikan jebakan umum, dan Anda siap membangun solusi pemrosesan gambar yang handal tanpa hambatan lisensi.

---

**Last Updated:** 2026-05-29  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
