---
date: 2026-09-23
description: Tìm hiểu cách vẽ văn bản lên hình ảnh bằng Aspose.Drawing cho .NET. Tạo
  hình ảnh có văn bản, thêm văn bản vào bitmap và lưu bitmap dưới dạng PNG với phông
  chữ tùy chỉnh.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Cách vẽ văn bản với Aspose.Drawing
og_description: Tìm hiểu cách vẽ văn bản lên hình ảnh bằng Aspose.Drawing cho .NET.
  Bài hướng dẫn này chỉ cho bạn cách tạo hình ảnh có văn bản, thêm văn bản vào bitmap
  và lưu bitmap dưới dạng PNG với phông chữ tùy chỉnh.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Vẽ văn bản lên hình ảnh bằng Aspose.Drawing cho .NET – Hướng dẫn nhanh
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Cách vẽ văn bản lên hình ảnh bằng Aspose.Drawing cho .NET
url: /vi/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách vẽ văn bản lên hình ảnh với Aspose.Drawing cho .NET

## Giới thiệu

Trong hướng dẫn từng bước này, bạn sẽ học **cách vẽ văn bản lên hình ảnh** bằng Aspose.Drawing cho .NET. Cho dù bạn cần tạo một *hình ảnh văn bản động*, thêm văn bản vào bitmap hiện có, hoặc tạo đồ họa với phông chữ tùy chỉnh, bài hướng dẫn này sẽ dẫn bạn qua mọi chi tiết để bạn có thể bắt đầu vẽ văn bản trong vài phút. Thư viện hỗ trợ hơn 30 phương thức GDI+, chạy trên Windows, Linux và macOS, và có **không phụ thuộc bên ngoài**, làm cho nó trở thành lựa chọn đáng tin cậy cho việc tạo hình ảnh phía máy chủ.

## Câu trả lời nhanh
- **Thư viện nào được sử dụng?** Aspose.Drawing cho .NET  
- **Nhiệm vụ chính?** Vẽ văn bản lên hình ảnh (tạo hình ảnh với văn bản)  
- **Phương thức chính?** `Graphics.DrawString` (vẽ chuỗi lên hình ảnh)  
- **Định dạng đầu ra?** PNG (lưu bitmap dưới dạng PNG)  
- **Điều kiện tiên quyết?** Môi trường phát triển .NET và thư viện Aspose.Drawing  

## Vẽ văn bản với Aspose.Drawing là gì?

Vẽ văn bản với Aspose.Drawing có nghĩa là sử dụng API tương thích GDI+ của thư viện để hiển thị các chuỗi Unicode lên một canvas raster. Phương thức `Graphics.DrawString` ghi văn bản vào bitmap, cho phép bạn kiểm soát phông chữ, màu sắc, căn chỉnh và khử răng cưa. Cách tiếp cận này cho phép bạn tạo ra các hình ảnh chất lượng cao mà không cần cài đặt System.Drawing.Common.

## Tại sao nên sử dụng Aspose.Drawing để thêm văn bản vào hình ảnh?

Aspose.Drawing cung cấp một cách đáng tin cậy, đa nền tảng để hiển thị văn bản trên hình ảnh mà không cần các thư viện GDI+ gốc, mang lại chất lượng và hiệu năng nhất quán trên mọi hệ điều hành. Nó hỗ trợ khử răng cưa nâng cao, ký tự Unicode và phông chữ tùy chỉnh, và tích hợp liền mạch với các ứng dụng .NET, khiến nó trở nên lý tưởng cho việc tạo hình ảnh phía máy chủ và các công cụ desktop.

- **Độ tin cậy đa nền tảng** – hoạt động trên Windows, Linux và macOS.  
- **Kết xuất nâng cao** – khử răng cưa và làm mịn văn bản sub‑pixel cho đầu ra sắc nét.  
- **Không phụ thuộc bên ngoài** – thư viện gói mọi thứ bạn cần để *tạo hình ảnh với văn bản*.

## Điều kiện tiên quyết

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

- **Aspose.Drawing cho .NET** – tải xuống từ [tài liệu Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **IDE .NET** như Visual Studio hoặc VS Code.  

## Nhập không gian tên

Bắt đầu bằng cách nhập các không gian tên cần thiết:

Các không gian tên này cung cấp các kiểu GDI+ cốt lõi như `Bitmap`, `Graphics`, và các tiện ích render văn bản.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Bước 1: tạo đối tượng bitmap và graphics

`Bitmap` là container ảnh raster của Aspose.Drawing cho dữ liệu pixel, và `Graphics` cung cấp các phương thức vẽ để render hình dạng và văn bản lên nó.  

`Bitmap` đại diện cho một hình ảnh trong bộ nhớ, trong khi `Graphics` cung cấp các phương thức vẽ để render lên bitmap đó.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Ở đây chúng ta tạo một `Bitmap` sẽ chứa hình ảnh cuối cùng và một đối tượng `Graphics` cho phép chúng ta vẽ lên nó. Gợi ý khử răng cưa đảm bảo văn bản trông mượt mà.

## Bước 2: thiết lập brush, pen và font

`Brush` định nghĩa màu nền, `Pen` tạo viền cho các hình dạng, và `Font` chỉ định phông chữ, kích thước và kiểu cho việc render văn bản.  

`Brush` lấp đầy các hình dạng bằng màu, `Pen` tạo viền cho các hình dạng, và `Font` xác định phông chữ và kích thước cho việc render văn bản.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** định nghĩa màu văn bản.  
- **Pen** được dùng sau này để vẽ một hình chữ nhật quanh văn bản (tùy chọn).  
- **Font** xác định phông chữ, kích thước và kiểu cho thao tác *vẽ chuỗi trên hình ảnh*.

## Bước 3: xác định văn bản và hình chữ nhật

`Rectangle` định nghĩa hộp bao quanh nơi văn bản sẽ được đặt, chỉ định tọa độ X/Y và chiều rộng/chiều cao.  

`Rectangle` chỉ định vị trí và kích thước của một khu vực hình chữ nhật, được sử dụng ở đây để giới hạn văn bản đã vẽ.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` xác định nơi văn bản sẽ được đặt. Điều chỉnh tọa độ và kích thước cho phù hợp với bố cục của bạn.

## Bước 4: vẽ hình chữ nhật và văn bản

`Graphics.DrawString` render văn bản đã chỉ định bên trong hình chữ nhật cho trước bằng phông chữ và brush đã cung cấp.  

`Graphics.DrawString` render một chuỗi văn bản bên trong một hình chữ nhật xác định bằng phông chữ và brush đã cho.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Đầu tiên chúng ta vẽ viền khu vực bằng một hình chữ nhật màu xanh, sau đó chúng ta **thêm văn bản vào bitmap** bằng cách gọi `DrawString`. Đây là phần cốt lõi của *vẽ văn bản* trên hình ảnh.

## Bước 5: lưu kết quả

Hình ảnh được lưu dưới dạng tệp PNG, đáp ứng yêu cầu *lưu bitmap dưới dạng PNG*. Thay thế đường dẫn placeholder bằng thư mục thực tế nơi bạn muốn lưu tệp.  

`bitmap.Save` ghi hình ảnh vào tệp ở định dạng đã chọn, chẳng hạn PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Các trường hợp sử dụng phổ biến

- **Tạo chứng chỉ** với tên cá nhân hoá.  
- **Tạo ảnh thu nhỏ có dấu watermark** cho các bộ sưu tập web.  
- **Xây dựng biểu đồ động** có nhãn hoặc chú thích.  

## Khắc phục sự cố & mẹo

- **Không tìm thấy phông chữ?** Đảm bảo phông chữ đã được cài đặt trên máy chủ hoặc sử dụng bộ sưu tập phông chữ riêng.  
- **Văn bản bị cắt?** Tăng kích thước hình chữ nhật hoặc giảm kích thước phông chữ.  
- **Lo ngại về hiệu năng?** Tái sử dụng cùng một đối tượng `Graphics` cho nhiều thao tác vẽ khi có thể.  

## Câu hỏi thường gặp

**H: Làm thế nào để thay đổi định dạng đầu ra thành JPEG?**  
Trả lời: Thay thế phần mở rộng `.png` bằng `.jpg` trong phương thức `Save` và tùy chọn chỉ định một `ImageCodecInfo` cho chất lượng JPEG.

**H: Tôi có thể vẽ văn bản đa dòng không?**  
Trả lời: Có, bao gồm các ký tự ngắt dòng (`\n`) trong chuỗi hoặc sử dụng `StringFormat` với `FormatFlags.LineLimit`.

**H: Có cách nào đo kích thước văn bản trước khi vẽ không?**  
Trả lời: Sử dụng `Graphics.MeasureString` để lấy kích thước chính xác của văn bản đã render.

**H: Aspose.Drawing có hỗ trợ ký tự Unicode không?**  
Trả lời: Chắc chắn. Cung cấp một phông chữ chứa các glyph cần thiết và thư viện sẽ render chúng đúng cách.

**H: Phiên bản Aspose.Drawing nào đã được sử dụng để kiểm thử?**  
Trả lời: Các ví dụ đã được kiểm thử với Aspose.Drawing 24.11 cho .NET.

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Hướng dẫn liên quan

- [Tạo Đồ họa Bitmap C# – Lưu ảnh PNG và làm việc với phông chữ đã cài đặt trong Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Cách lưu bitmap dưới dạng PNG bằng API Aspose.Drawing cho .NET](/drawing/net/image-editing/display/)
- [Văn bản trên hình ảnh](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}