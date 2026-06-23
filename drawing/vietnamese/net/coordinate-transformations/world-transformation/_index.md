---
date: 2026-06-23
description: Tìm hiểu cách lưu PNG bằng Aspose.Drawing, áp dụng các biến đổi world,
  và chuyển đổi đồ họa sang PNG. Bao gồm các ví dụ C# về translate transform và nhiều
  biến đổi đồ họa.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: World Transformation trong Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cách lưu PNG với Aspose.Drawing – World Transformation
url: /vi/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Lưu PNG với Aspose.Drawing – Biến Đổi Thế Giới

## Lưu Bitmap dưới dạng PNG – Giới thiệu

**Cách lưu PNG** bằng Aspose.Drawing là một yêu cầu phổ biến khi bạn cần các hình ảnh trong suốt, chất lượng cao được tạo ra ngay lập tức. Trong hướng dẫn này, bạn sẽ học cách **lưu bitmap dưới dạng PNG**, áp dụng các biến đổi thế giới như dịch chuyển, quay và thu phóng, và cuối cùng chuyển đồ họa thành PNG — tất cả đều bằng mã C# sạch sẽ, dễ bảo trì. Dù bạn đang xây dựng một công cụ báo cáo, một thành phần biểu đồ, hay một trình render UI tùy chỉnh, việc nắm vững các bước này sẽ giúp bạn tạo ra các hình ảnh động đẹp mắt trên mọi thiết bị.

## Câu trả lời nhanh
- **“Biến đổi thế giới” có nghĩa là gì?** Nó ánh xạ các tọa độ logic (thế giới) của bản vẽ sang tọa độ trang (thiết bị).  
- **Tôi có thể xuất kết quả dưới dạng PNG không?** Có – sau khi vẽ, bạn chỉ cần gọi `bitmap.Save(...)` với phần mở rộng `.png`.  
- **Tôi có cần giấy phép cho Aspose.Drawing không?** Bản dùng thử miễn phí đủ cho việc phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Điều này có tương thích với .NET 6/7 không?** Hoàn toàn – Aspose.Drawing hỗ trợ .NET Framework 4.5+ và .NET Core/5/6/7.  
- **Tôi có thể xâu chuỗi bao nhiêu biến đổi?** Bạn có thể áp dụng **nhiều biến đổi đồ họa** liên tiếp (dịch, quay, thu phóng, v.v.).

## Biến đổi thế giới là gì trong Aspose.Drawing?

Biến đổi thế giới thay đổi hệ tọa độ mà các lệnh vẽ của bạn sử dụng. Mặc định, (0,0) là góc trên‑trái của bitmap. Với `TranslateTransform`, `RotateTransform` hoặc `ScaleTransform`, bạn có thể di chuyển gốc tọa độ, quay các hình, hoặc thay đổi kích thước chúng mà không làm thay đổi hình học gốc.

## Cách Lưu PNG bằng Aspose.Drawing?

Tải một đối tượng `Bitmap`, đặt các biến đổi thế giới mong muốn lên thể hiện `Graphics` của nó, vẽ các hình, và cuối cùng gọi `bitmap.Save("output.png", ImageFormat.Png)`. Lệnh lưu một dòng này sẽ ghi một file PNG không mất dữ liệu, giữ nguyên độ trong suốt và độ chính xác màu, rất thích hợp cho tài nguyên web và lớp phủ UI.

## Tại sao nên sử dụng ví dụ dịch đồ họa?

Một ví dụ dịch đồ họa cho phép bạn di chuyển gốc vẽ một lần thay vì tính lại mọi điểm. Cách tiếp cận này giảm độ phức tạp của mã, cải thiện khả năng đọc, và cho phép engine đồ họa xử lý phép toán ma trận một cách hiệu quả, có thể tăng tốc độ render lên tới 30 % trên các canvas lớn.

## Ví dụ Dịch Đồ Họa

Một **ví dụ dịch đồ họa** cho thấy việc di chuyển gốc làm đơn giản hoá việc định vị. Thay vì tính lại mọi điểm, bạn chỉ cần dịch hệ tọa độ một lần và vẽ như thể gốc mới là trung tâm canvas.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

- **Thư viện Aspose.Drawing** được tích hợp vào dự án .NET của bạn – tải về từ trang [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/).  
- Một **thư mục tài liệu** nơi hình ảnh đầu ra sẽ được lưu.  
- Kiến thức cơ bản về cú pháp **C#** và Visual Studio hoặc IDE ưa thích của bạn.  

Bây giờ, chúng ta cùng khám phá mã nhé!

## Nhập không gian tên

Các lớp `Bitmap`, `Graphics` và các tiện ích vẽ của Aspose nằm trong các không gian tên này.  
**Định nghĩa:** `System.Drawing` cung cấp các kiểu GDI+ cốt lõi, trong khi `Aspose.Drawing` mở rộng chúng với khả năng đa nền tảng.

## Hướng dẫn từng bước

### Bước 1: Tạo một Bitmap

Chúng ta bắt đầu bằng việc tạo một canvas trống để chứa bản vẽ.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` tạo một bitmap 32‑bit mỗi pixel với alpha đã được nhân trước, là định dạng tối ưu cho đầu ra PNG vì nó giữ nguyên độ trong suốt mà không cần bước chuyển đổi thêm.

- **Tại sao lại dùng 32bppPArgb?** Định dạng pixel này hỗ trợ độ trong suốt alpha và màu sắc chất lượng cao, hoàn hảo cho đầu ra PNG.  
- **Mẹo:** Điều chỉnh chiều rộng/chiều cao để phù hợp với kích thước ảnh mục tiêu.

### Bước 2: Đặt Biến đổi Thế giới (Ví dụ Dịch Đồ Họa)

`TranslateTransform` di chuyển gốc của hệ tọa độ đến vị trí mới.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` dịch điểm (0,0) tới trung tâm canvas. Sau lệnh này, bất kỳ hình nào bạn vẽ bằng tọa độ (0,0) sẽ xuất hiện ở giữa ảnh.

- Điều này di chuyển điểm (0,0) tới (500, 400) – trung tâm của canvas 1000 × 800.  
- Bạn có thể xâu chuỗi các biến đổi khác: `RotateTransform` quay hệ tọa độ, và `ScaleTransform` thu phóng nó, cho phép **nhiều biến đổi đồ họa**.

### Bước 3: Vẽ một Hình Chữ Nhật bằng các tọa độ đã biến đổi

`DrawRectangle` vẽ một hình chữ nhật bằng bút và các tọa độ đã cho.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` vẽ một hình chữ nhật nằm ở trung tâm canvas vì góc trên‑trái của nó được dịch ra nửa chiều rộng và chiều cao từ gốc đã biến đổi.

- Góc trên‑trái của hình chữ nhật bắt đầu tại gốc đã dịch (giữa ảnh).  
- Bạn có thể thử nghiệm với các hình khác — ellipses, lines, hoặc custom paths.

### Bước 4: Lưu Kết quả – Chuyển Đồ Họa sang PNG

`Save` ghi bitmap ra file ở định dạng ảnh đã chỉ định.  
`ImageFormat` xác định định dạng file cho việc lưu ảnh, chẳng hạn PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` ghi một file PNG không mất dữ liệu, có thể dùng trực tiếp trong trang web hoặc thành phần UI.

- PNG giữ nguyên màu sắc và độ trong suốt chúng ta đã thiết lập trước đó.  
- Thay `"Your Document Directory"` bằng đường dẫn thực tế trên máy của bạn.

## Vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|----------|
| **Lỗi không tìm thấy file** khi lưu | Thư mục đích không tồn tại. | Tạo thư mục bằng mã (`Directory.CreateDirectory`) trước khi gọi `Save`. |
| **Hình ảnh trống** sau khi biến đổi | `TranslateTransform` được gọi sau khi vẽ. | Đảm bảo đặt biến đổi **trước** bất kỳ lệnh vẽ nào. |
| **Màu sắc bị biến dạng** | Sử dụng định dạng pixel không tương thích. | Giữ nguyên `Format32bppPArgb` cho đầu ra PNG. |

## Câu hỏi thường gặp

**H: Tôi có thể áp dụng hơn một biến đổi không?**  
Đ: Có – bạn có thể xâu chuỗi `TranslateTransform`, `RotateTransform` và `ScaleTransform` để đạt hiệu ứng phức tạp trong một pipeline đồ họa duy nhất.

**H: Aspose.Drawing có miễn phí cho dự án thương mại không?**  
Đ: Bản dùng thử miễn phí chỉ dành cho đánh giá; giấy phép thương mại là bắt buộc cho môi trường sản xuất.

**H: Điều này có hoạt động với .NET Core và .NET 5/6/7 không?**  
Đ: Hoàn toàn. Aspose.Drawing hỗ trợ tất cả các runtime .NET hiện đại, bao gồm .NET Core, .NET 5, .NET 6 và .NET 7.

**H: Tôi có thể tìm tài liệu API đầy đủ ở đâu?**  
Đ: Tài liệu đầy đủ có sẵn [tại đây](https://reference.aspose.com/drawing/net/).

**H: Làm sao khắc phục khi file đầu ra không xuất hiện?**  
Đ: Kiểm tra chuỗi đường dẫn, đảm bảo có quyền ghi, và xác nhận thư mục tồn tại trước khi gọi `Save`.

## Kết luận

Bạn đã học **cách lưu PNG** với Aspose.Drawing, áp dụng **biến đổi thế giới**, và thực hiện một **ví dụ dịch đồ họa** có thể mở rộng bằng quay hoặc thu phóng. Khi nắm vững các khối xây dựng này, bạn có thể tạo ra các hình ảnh động, biểu đồ tùy chỉnh, hoặc đồ họa tức thời cho bất kỳ ứng dụng .NET nào.

---

**Cập nhật lần cuối:** 2026-06-23  
**Kiểm tra với:** Aspose.Drawing 24.11 for .NET  
**Tác giả:** Aspose  
**Tài nguyên liên quan:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Tải bản dùng thử miễn phí](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Hướng dẫn liên quan

- [Matrix Transformation Tutorial: Matrix Transformations in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [How to Rotate Image with Aspose.Drawing Global Transformation](/drawing/net/coordinate-transformations/global-transformation/)
- [Coordinate System Transformation – Page Transformation in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}