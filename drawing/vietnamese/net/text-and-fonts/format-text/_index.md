---
date: 2026-07-17
description: Tìm hiểu cách ngăn chặn tràn văn bản bằng cách đặt căn chỉnh văn bản
  trong Aspose.Drawing cho .NET và thêm văn bản vào hình ảnh. Hướng dẫn chi tiết từng
  bước kèm ví dụ.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Đặt căn chỉnh văn bản với Aspose.Drawing cho .NET
og_description: Ngăn chặn tràn văn bản bằng cách đặt căn chỉnh văn bản trong Aspose.Drawing
  cho .NET. Tìm hiểu cách vẽ chuỗi trên hình ảnh, căn giữa văn bản trong hình chữ
  nhật và thay thế System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Ngăn chặn tràn văn bản – Đặt căn chỉnh văn bản với Aspose.Drawing cho .NET
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
title: Ngăn chặn tràn văn bản – Đặt căn chỉnh văn bản với Aspose.Drawing cho .NET
url: /vi/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ngăn Tràn Văn Bản – Đặt Căn Văn Bản với Aspose.Drawing

## Giới thiệu

Khi bạn cần **ngăn tràn văn bản** khi render đồ họa trong .NET, Aspose.Drawing cung cấp cho bạn khả năng kiểm soát chi tiết vị trí, căn chỉnh và ngắt dòng của văn bản. Dù bạn đang xây dựng một trình tạo huy hiệu, một báo cáo động, hay bất kỳ đầu ra dựa trên hình ảnh nào, việc nắm vững căn chỉnh văn bản sẽ đảm bảo văn bản của bạn nằm trong hình chữ nhật mong muốn và trông chuyên nghiệp. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách tạo canvas bitmap, cấu hình `StringFormat`, vẽ một hình chữ nhật với văn bản căn giữa, xử lý tràn văn bản, và cuối cùng lưu hình ảnh.

## Câu trả lời nhanh
- **What does “set text alignment” mean?** Nó xác định cách văn bản được đặt vị trí theo chiều ngang và chiều dọc trong một hình chữ nhật vẽ.  
- **Which class controls alignment?** `StringFormat` cho phép bạn đặt `Alignment` và `LineAlignment`.  
- **Can I draw a string and a rectangle together?** Có—sử dụng `Graphics.DrawRectangle` rồi `Graphics.DrawString`.  
- **How do I prevent text overflow?** Điều chỉnh kích thước hình chữ nhật hoặc chia văn bản thành nhiều dòng thủ công.  
- **Do I need a license for production?** Cần có giấy phép thương mại Aspose.Drawing cho việc sử dụng không phải thử nghiệm.

## **set text alignment** là gì trong Aspose.Drawing?

`set text alignment` cấu hình vị trí ngang (`StringAlignment`) và dọc (`LineAlignment`) của văn bản trong một `Rectangle` hoặc vùng vẽ. Bằng cách điều chỉnh các thuộc tính này, bạn kiểm soát việc văn bản hiển thị căn trái, căn giữa, căn phải, căn trên, căn giữa dọc, hoặc căn dưới, cho phép bố cục chính xác trong đồ họa, huy hiệu và báo cáo được tạo bằng Aspose.Drawing.

## Tại sao nên sử dụng Aspose.Drawing cho căn chỉnh văn bản?

Aspose.Drawing loại bỏ các hạn chế của GDI+ gây ra cho `System.Drawing.Common`. Nó hỗ trợ **5 môi trường .NET chính** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 và .NET 7 – và có thể render hình ảnh lên đến **4000 × 4000 px** (≈ 100 MB) mà không tiêu tốn bộ nhớ. Khả năng khử răng cưa, thu phóng DPI cao và tương thích đầy đủ với container Linux cho phép bạn tạo đồ họa pixel‑perfect trong bất kỳ kịch bản triển khai nào.

## Yêu cầu trước

1. **Aspose.Drawing Library** – tải xuống tại [here](https://releases.aspose.com/drawing/net/).  
2. **Development Environment** – Visual Studio 2022 (hoặc bất kỳ IDE C# nào).  
3. **Basic .NET knowledge** – bạn nên quen thuộc với các dự án C# và gói NuGet.

## Nhập không gian tên

Để bắt đầu, đưa các không gian tên cần thiết vào phạm vi. Chúng cho phép bạn truy cập vào đồ họa, render văn bản và các primitive vẽ.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Cách ngăn tràn văn bản với Aspose.Drawing?

Bitmap là một lớp đại diện cho hình ảnh được lưu trong bộ nhớ, trong khi `RectangleF` định nghĩa một vùng hình chữ nhật dạng số thực để vẽ. Bằng cách sử dụng `StringFormat` với `Trimming` được đặt thành `StringTrimming.EllipsisCharacter`, các ký tự thừa sẽ tự động được thay bằng dấu ba chấm, đảm bảo văn bản không bao giờ vượt quá giới hạn của hình chữ nhật. Đo kích thước chuỗi trước sẽ cho phép bạn quyết định thu nhỏ hình chữ nhật hoặc chia văn bản thành nhiều dòng, đảm bảo bố cục sạch sẽ mà không bị tràn.

Tải bitmap của bạn, định nghĩa một `RectangleF` có kích thước phù hợp, và sử dụng `StringFormat` với `Trimming` được đặt thành `StringTrimming.EllipsisCharacter` để tự động cắt bỏ các ký tự thừa. Để có kiểm soát đầy đủ, đo chuỗi bằng `Graphics.MeasureString` và thu nhỏ hình chữ nhật hoặc chia văn bản thành các dòng trước khi vẽ. Cách tiếp cận này đảm bảo không có ký tự nào tràn ra ngoài giới hạn hiển thị.

## Bước 1: Tạo đối tượng Bitmap và Graphics  

Bitmap đại diện cho một hình ảnh trong bộ nhớ, trong khi Graphics cung cấp các phương thức vẽ cho bitmap đó. Tạo một bitmap cung cấp một canvas để bạn có thể vẽ lên. Đối tượng `Graphics` là bề mặt vẽ, và chúng ta bật chế độ render văn bản chất lượng cao bằng `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Bước 2: Định nghĩa **StringFormat** và Kiểu dáng  

`StringFormat` chỉ định các tùy chọn bố cục văn bản như căn chỉnh, khoảng cách dòng và cắt bớt. Ở đây chúng tôi **set text alignment** bằng cách cấu hình một thể hiện `StringFormat`. Chúng tôi cũng chuẩn bị các brush, pen và font sẽ được sử dụng khi vẽ chuỗi.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Bước 3: Tạo và Định dạng Văn bản – **how to draw string** và **draw rectangle with text**

`Graphics.DrawString` render văn bản lên canvas, và `Graphics.DrawRectangle` vẽ một hình chữ nhật. Chúng tôi tạo nội dung văn bản, định nghĩa hình chữ nhật sẽ chứa nó, và sau đó vẽ cả viền hình chữ nhật và chuỗi văn bản.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Cách xử lý tràn văn bản

Nếu `text` được cung cấp vượt quá giới hạn của hình chữ nhật, bạn có hai tùy chọn phổ biến:

1. **Resize the rectangle** – tăng `rectangle.Width` hoặc `rectangle.Height`.  
2. **Split the text** – chia chuỗi thành các dòng phù hợp, sau đó gọi `DrawString` cho mỗi dòng với tọa độ Y đã điều chỉnh.

## Cách vẽ chuỗi lên hình ảnh bằng Aspose.Drawing?

`Graphics.DrawString` vẽ văn bản được chỉ định bằng một font và các tùy chọn định dạng. Tạo một đối tượng `Graphics` từ bitmap của bạn, sau đó gọi `DrawString` với `StringFormat` đã chuẩn bị. Lệnh duy nhất này render văn bản chính xác ở vị trí bạn muốn, tôn trọng căn chỉnh, cắt bớt và bất kỳ ma trận biến đổi nào bạn đã áp dụng. Thêm gợi ý render chất lượng cao đảm bảo đầu ra vẫn sắc nét trên màn hình DPI cao.

## Cách căn giữa văn bản trong hình chữ nhật?

`StringAlignment` xác định căn chỉnh ngang của văn bản trong một hình chữ nhật bố cục. Đặt `stringFormat.Alignment = StringAlignment.Center` và `stringFormat.LineAlignment = StringAlignment.Center`. Điều này căn giữa văn bản cả theo chiều ngang và chiều dọc bên trong hình chữ nhật, rất phù hợp cho huy hiệu, nút hoặc lớp phủ nhãn. Vị trí căn giữa hoạt động nhất quán trên các kích thước hình ảnh và cài đặt DPI khác nhau, mang lại vẻ ngoài cân đối.

## Cách đạt được căn chỉnh dọc cho văn bản?

`LineAlignment` kiểm soát vị trí dọc của văn bản bên trong hình chữ nhật. Sử dụng `stringFormat.LineAlignment` với các giá trị `StringAlignment.Near`, `Center` hoặc `Far` để đặt văn bản ở trên, giữa hoặc dưới của hình chữ nhật. Kết hợp với `Graphics.TranslateTransform` nếu bạn cần quay văn bản trong khi vẫn giữ căn chỉnh dọc. Điều chỉnh line alignment đảm bảo các khối đa dòng căn chỉnh chính xác như mong muốn, ngay cả sau khi biến đổi.

## Bước 4: Lưu Kết quả – **add text to image**

Cuối cùng, ghi bitmap ra đĩa. Bước này minh họa **add text to image** trong một lệnh duy nhất.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Các vấn đề thường gặp và giải pháp

| Issue | Solution |
|-------|----------|
| **Text appears blurry** | Đảm bảo đặt `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`. |
| **Text is clipped** | Tăng kích thước hình chữ nhật hoặc bật logic ngắt từ bằng cách đo kích thước chuỗi (`Graphics.MeasureString`). |
| **Font not found** | Kiểm tra phông chữ đã được cài đặt trên máy chủ hoặc nhúng phông chữ riêng bằng `PrivateFontCollection`. |
| **Unexpected colors** | Kiểm tra lại màu brush và pen; nhớ rằng `Color.FromKnownColor` sử dụng màu định nghĩa bởi hệ thống. |

## Câu hỏi thường gặp

**Q1: Aspose.Drawing có tương thích với mọi phiên bản .NET không?**  
A1: Có, Aspose.Drawing được thiết kế để tương thích với nhiều phiên bản .NET, đảm bảo tính linh hoạt cho nhà phát triển.

**Q2: Tôi có thể tùy chỉnh kiểu phông chữ hơn nữa không?**  
A2: Chắc chắn! Điều chỉnh các tham số của đối tượng `Font` để đạt kích thước, kiểu và họ phông chữ mong muốn.

**Q3: Làm thế nào để xử lý tràn văn bản trong hình chữ nhật đã định nghĩa?**  
A3: Bạn có thể quản lý tràn văn bản bằng cách điều chỉnh kích thước hình chữ nhật hoặc triển khai logic tùy chỉnh để xử lý văn bản dài.

**Q4: Có các tùy chọn định dạng khác có sẵn trong Aspose.Drawing không?**  
A4: Có, Aspose.Drawing cung cấp một bộ công cụ toàn diện cho việc thao tác đồ họa, bao gồm nhiều tùy chọn định dạng cho văn bản, hình dạng và hơn thế nữa.

**Q5: Tôi có thể tìm hỗ trợ bổ sung cho Aspose.Drawing ở đâu?**  
A5: Khám phá diễn đàn Aspose.Drawing [here](https://forum.aspose.com/c/drawing/44) để nhận hỗ trợ cộng đồng và thảo luận.

**Additional Q&A**

**Q: Làm sao để vẽ chuỗi mà không có hình chữ nhật bao quanh?**  
A: Bỏ qua lệnh `DrawRectangle` và truyền vị trí `PointF` mong muốn vào `Graphics.DrawString`.

**Q: Tôi có thể quay văn bản trong khi vẫn giữ căn chỉnh không?**  
A: Có—áp dụng biến đổi `Matrix` cho đối tượng `Graphics` trước khi vẽ, sau đó đặt lại sau khi hoàn thành.

**Q: Có thể xuất hình ảnh dưới dạng JPEG thay vì PNG không?**  
A: Chỉ cần thay đổi phần mở rộng tệp trong `bitmap.Save` và tùy chọn chỉ định `ImageFormat.Jpeg`.

---

**Cập nhật lần cuối:** 2026-07-17  
**Kiểm tra với:** Aspose.Drawing 24.11 for .NET  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Cách Vẽ Văn Bản với Aspose.Drawing cho .NET](/drawing/net/text-and-fonts/draw-text/)
- [Thêm Văn Bản lên Hình Ảnh trong Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [Cách Vẽ Văn Bản và Phông Chữ với Aspose.Drawing cho .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}