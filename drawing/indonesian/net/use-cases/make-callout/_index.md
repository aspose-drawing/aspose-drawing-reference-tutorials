---
date: 2026-03-02
description: Tingkatkan ilustrasi dokumen Anda menggunakan Aspose.Drawing untuk .NET!
  Pelajari langkah demi langkah cara menambahkan callout untuk visual yang lebih jelas
  dan informatif.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cara Menambahkan Callouts dengan Aspose.Drawing untuk .NET
url: /id/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Membuat Callout di Aspose.Drawing

## Pendahuluan
Jika Anda bertanya‑tanya **cara menambahkan callout** ke gambar atau diagram Anda menggunakan Aspose.Drawing untuk .NET, Anda berada di tempat yang tepat. Pada tutorial ini kami akan membahas seluruh proses—dari memuat gambar hingga menggambar callout dengan gaya yang indah—sehingga ilustrasi Anda menjadi lebih jelas dan informatif.

## Jawaban Cepat
- **Apa perpustakaan yang saya butuhkan?** Aspose.Drawing untuk .NET (dapat diunduh dari situs resmi).  
- **Versi .NET mana yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis cukup untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk callout dasar.  
- **Bisakah saya menyesuaikan warna dan font?** Ya—semua dikendalikan oleh objek standar GDI+ (Pen, Font, Brush).

## Cara Menambahkan Callout di Aspose.Drawing
Berikut adalah panduan singkat langkah‑demi‑langkah yang menunjukkan secara tepat **cara menambahkan callout** ke sebuah gambar. Silakan salin kode, bereksperimen dengan posisi, dan sesuaikan gaya agar cocok dengan merek Anda.

## Prasyarat
Sebelum memulai, pastikan Anda memiliki:

- Pengetahuan dasar tentang bahasa pemrograman C#.  
- Perpustakaan Aspose.Drawing terpasang. Anda dapat mengunduhnya [di sini](https://releases.aspose.com/drawing/net/).  
- Dokumen atau gambar tempat Anda ingin menambahkan callout.

## Impor Namespace
Pastikan namespace yang diperlukan sudah disertakan dalam proyek Anda:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Langkah 1: Muat Gambar
Mulailah dengan memuat gambar tempat Anda ingin menambahkan callout. Ganti `"Your Document Directory"` dan `"gears.png"` dengan direktori dan nama file gambar Anda yang sebenarnya.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Langkah 2: Buat Objek Graphics
Buat objek `Graphics` dari gambar untuk melakukan operasi menggambar.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Langkah 3: Tentukan Posisi Callout
Tentukan titik awal dan akhir untuk setiap callout beserta nilai dan satuan callout.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## Langkah 4: Gambar Callout
Implementasikan metode `DrawCallOut` untuk menggambar callout pada gambar.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Langkah 5: Simpan Gambar
Simpan gambar dengan callout ke direktori yang Anda inginkan.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Kode Sumber Draw Callout
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## Masalah Umum & Tips
- **Koordinat jangkar tidak tepat** – pastikan titik awal dan akhir berada dalam batas gambar; jika tidak, callout dapat terpotong.  
- **Teks saling tumpang** – sesuaikan `spaceSize` atau ukuran font jika label bertabrakan dengan grafik lain.  
- **Kinerja** – untuk gambar berukuran sangat besar, pertimbangkan untuk membuang objek `Pen`, `Font`, dan `Brush` setelah selesai digunakan guna membebaskan sumber daya.

## Kesimpulan
Selamat! Anda kini tahu **cara menambahkan callout** ke sebuah gambar menggunakan Aspose.Drawing untuk .NET. Silakan bereksperimen dengan posisi, warna, dan font yang berbeda agar sesuai dengan gaya visual Anda.

## FAQ

### Bisakah saya menggunakan Aspose.Drawing untuk jenis ilustrasi lain?
Ya, Aspose.Drawing mendukung berbagai operasi menggambar untuk berbagai jenis ilustrasi.

### Apakah Aspose.Drawing kompatibel dengan format gambar yang berbeda?
Tentu saja! Aspose.Drawing mendukung format gambar populer seperti PNG, JPEG, GIF, dan lainnya.

### Di mana saya dapat menemukan contoh dan dokumentasi lebih lanjut?
Jelajahi dokumentasi lengkap [di sini](https://reference.aspose.com/drawing/net/).

### Bagaimana cara mendapatkan dukungan jika saya mengalami masalah?
Kunjungi [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) untuk dukungan komunitas.

### Bisakah saya mencoba Aspose.Drawing sebelum membeli?
Tentu! Mulailah dengan percobaan gratis [di sini](https://releases.aspose.com/).

**Additional Q&A**

**Q: Bisakah saya mengubah gaya garis callout (dash, dot)?**  
A: Ya—cukup konfigurasikan properti `Pen.DashStyle` sebelum menggambar garis.

**Q: Apakah memungkinkan menambahkan warna latar belakang pada label callout?**  
A: Tentu. Buat `SolidBrush` dengan warna yang diinginkan dan isi persegi panjang di belakang teks sebelum memanggil `DrawString`.

**Q: Bagaimana cara memastikan callout terlihat sama pada tampilan high‑DPI?**  
A: Atur `graphics.PageUnit = GraphicsUnit.Pixel` (seperti yang ditunjukkan) dan gunakan ukuran berbasis vektor untuk menjaga konsistensi skala.

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}