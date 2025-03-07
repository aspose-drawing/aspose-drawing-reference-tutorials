---
title: Membuat Callout di Aspose.Drawing
linktitle: Membuat Callout di Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternatif untuk System.Drawing.Common
description: Sempurnakan ilustrasi dokumen Anda menggunakan Aspose.Drawing untuk .NET! Pelajari langkah demi langkah cara menambahkan info untuk visual yang lebih jelas dan informatif.
weight: 10
url: /id/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Membuat Callout di Aspose.Drawing

## Perkenalan
Selamat datang di panduan langkah demi langkah kami dalam membuat info di Aspose.Drawing untuk .NET! Jika Anda ingin menyempurnakan ilustrasi dokumen Anda dengan info, Anda berada di tempat yang tepat. Dalam tutorial ini, kami akan memecah proses menjadi langkah-langkah yang dapat dikelola menggunakan pustaka Aspose.Drawing.
## Prasyarat
Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
- Pengetahuan dasar bahasa pemrograman C#.
-  Perpustakaan Aspose.Drawing diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/drawing/net/).
- Dokumen atau gambar yang ingin Anda tambahkan infonya.
## Impor Namespace
Pastikan Anda memiliki namespace yang diperlukan dalam proyek Anda:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Langkah 1: Muat Gambar
 Mulailah dengan memuat gambar di mana Anda ingin menambahkan info. Mengganti`"Your Document Directory"` Dan`"gears.png"` dengan direktori aktual dan nama file gambar Anda.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Kode Anda di sini
}
```
## Langkah 2: Buat Objek Grafik
 Membuat`Graphics` objek dari gambar untuk melakukan operasi menggambar.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Langkah 3: Tentukan Posisi Info
Tentukan titik awal dan akhir untuk setiap pemanggilan beserta nilai dan unit pemanggilan.
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
## Langkah 4: Gambar Info
 Menerapkan`DrawCallOut` metode untuk menggambar info pada gambar.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Langkah 5: Simpan Gambar
Simpan gambar dengan info ke direktori yang Anda inginkan.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Gambar Kode Sumber Info
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
## Kesimpulan

Selamat! Anda telah berhasil menambahkan info ke gambar Anda menggunakan Aspose.Drawing untuk .NET. Jangan ragu untuk bereksperimen dengan berbagai posisi dan nilai untuk menyesuaikan info Anda lebih lanjut.

## FAQ

### Bisakah saya menggunakan Aspose.Drawing untuk jenis ilustrasi lainnya?

Ya, Aspose.Drawing mendukung berbagai operasi menggambar untuk berbagai jenis ilustrasi.

### Apakah Aspose.Drawing kompatibel dengan format gambar yang berbeda?

Sangat! Aspose.Drawing mendukung format gambar populer seperti PNG, JPEG, GIF, dan lainnya.

### Di mana saya dapat menemukan lebih banyak contoh dan dokumentasi?

 Jelajahi dokumentasi komprehensif[Di Sini](https://reference.aspose.com/drawing/net/).

### Bagaimana cara mendapatkan dukungan jika saya mengalami masalah?

 Mengunjungi[Aspose.Forum menggambar](https://forum.aspose.com/c/diagram/17) untuk dukungan masyarakat.

### Bisakah saya mencoba Aspose.Drawing sebelum membeli?

 Tentu! Mulailah dengan uji coba gratis[Di Sini](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
