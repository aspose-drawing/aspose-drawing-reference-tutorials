---
date: 2026-05-24
description: Tìm hiểu cách đặt đơn vị trong Aspose.Drawing cho .NET, chuyển đổi đơn
  vị đồ họa một cách dễ dàng, và nắm vững các phép đo chính xác cho việc render đồ
  họa.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Đơn vị đo lường trong Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cách Đặt Đơn Vị trong Aspose.Drawing cho .NET – Đơn vị đo lường
url: /vi/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Đặt Đơn Vị trong Aspose.Drawing cho .NET – Đơn Vị Đo Lường

## Giới thiệu

Chào mừng đến với thế giới Aspose.Drawing cho .NET, nơi độ chính xác và tính linh hoạt gặp nhau trong việc thao tác đồ họa. Trong hướng dẫn này, bạn sẽ khám phá **cách đặt đơn vị** cho các bản vẽ của mình, học cách **chuyển đổi đơn vị đồ họa** giữa points, millimeters và inches, và xem các ví dụ thực tế giúp hình ảnh của bạn trở nên pixel‑perfect. Dù bạn đang xây dựng báo cáo, hình thu nhỏ, hay biểu đồ tùy chỉnh, việc nắm vững các đơn vị đo lường là cần thiết để đảm bảo việc render nhất quán trên mọi thiết bị.

## Câu Trả Lời Nhanh
- **Cách chính để thay đổi đơn vị là gì?** Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`) on the `Graphics` object.  
- **Đơn vị nào bằng 1/72 inch?** Points.  
- **Có bao nhiêu milimet trong một inch?** 25.4 mm = 1 inch.  
- **Tôi có cần thư viện bổ sung để sử dụng các đơn vị không?** No, the Aspose.Drawing core library provides all unit constants.  
- **Tôi có thể trộn các đơn vị trong một hình ảnh không?** Set the unit once per `Graphics` instance; draw everything using that unit for consistency.

## Yêu Cầu Trước

Trước khi chúng ta bắt đầu hướng dẫn, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

- Aspose.Drawing for .NET: Đảm bảo rằng bạn đã cài đặt thư viện. Bạn có thể tải xuống [tại đây](https://releases.aspose.com/drawing/net/).
- Thư Mục Tài Liệu: Có một thư mục được chỉ định nơi bạn muốn lưu các tài liệu đã tạo.
- Kiến Thức Cơ Bản về C#: Hiểu biết cơ bản về C# được khuyến nghị để tận dụng tối đa hướng dẫn này.

## Nhập Không Gian Tên

Trước khi bắt đầu, hãy nhập các không gian tên cần thiết để sử dụng Aspose.Drawing một cách hiệu quả:

```csharp
using System.Drawing;
```

Bây giờ, chúng ta sẽ phân tích từng ví dụ thành nhiều bước:

## Cách đặt đơn vị thành Points?

`Bitmap` là lớp đại diện cho một hình ảnh trong bộ nhớ dùng làm canvas vẽ. Tải bitmap của bạn, tạo một đối tượng `Graphics`, và đặt đơn vị trang thành points — điều này cho Aspose.Drawing hiểu tất cả các tọa độ là giá trị 1/72 inch. Sử dụng points cung cấp cho bạn kiểm soát chi tiết cho đồ họa sẵn sàng in và cho phép bạn chỉ định độ rộng đường nét với độ chính xác cao.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Bước 1: Tạo Bitmap  
`Bitmap` là lớp đại diện cho một hình ảnh trong bộ nhớ dùng làm canvas vẽ.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Bước 2: Tạo Đối Tượng Graphics  
`Graphics` cung cấp các phương pháp vẽ để hiển thị hình dạng và văn bản lên một `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Bước 3: Đặt Page Unit thành Points  
`PageUnit` là một enumeration xác định đơn vị đo lường cho tọa độ trang. `PageUnit.Point` định nghĩa points là đơn vị đo (1 point = 1/72 inch). Cài đặt này áp dụng cho tất cả các lời gọi vẽ tiếp theo.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Bước 4: Vẽ Hình Chữ Nhật bằng Points  
Khi bạn vẽ một hình chữ nhật sau khi đã đặt đơn vị, các kích thước bạn chỉ định sẽ được hiểu là points, đảm bảo kích thước chính xác.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Cách đặt đơn vị thành Millimeters?

`PageUnit` là một enumeration xác định đơn vị đo lường cho tọa độ trang. Chuyển sang millimeters hữu ích khi bạn cần kích thước mét, ví dụ khi tạo sơ đồ kỹ thuật. Aspose.Drawing coi 1 mm là 1/25.4 inch, cho phép bạn căn chỉnh đồ họa với các đo lường vật lý được sử dụng trong sản xuất và tài liệu kỹ thuật.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Bước 1: Đặt Page Unit thành Millimeters  
Gán `PageUnit.Millimeter` cho đối tượng `Graphics`; tất cả các tọa độ bây giờ sẽ tương ứng với hệ mét.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Bước 2: Vẽ Hình Chữ Nhật bằng Millimeters  
Chiều rộng và chiều cao của hình chữ nhật hiện được biểu thị bằng millimeters, giúp dễ dàng căn chỉnh với các đo lường vật lý và đảm bảo đầu ra in khớp với kích thước thực tế.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Cách đặt đơn vị thành Inches?

`Graphics` cung cấp các phương pháp vẽ để hiển thị hình dạng và văn bản lên một `Bitmap`. Inches là đơn vị mặc định cho nhiều công cụ thiết kế của Mỹ. Đặt đơn vị thành inches cho phép bạn suy nghĩ bằng các khái niệm quen thuộc khi bố trí các yếu tố UI, và nó đơn giản hoá việc chuyển từ thiết kế màn hình sang in, nơi inches thường được sử dụng.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Bước 1: Đặt Page Unit thành Inches  
`PageUnit.Inch` thay đổi hệ tọa độ sao cho 1 đơn vị bằng 1 inch, cung cấp cách đơn giản để định kích thước các yếu tố cho bố cục hướng in.

CODE_BLOCK_PLACEHOLDER_10_END

### Bước 2: Vẽ Hình Chữ Nhật bằng Inches  
Bây giờ bất kỳ hình nào bạn vẽ đều sử dụng inches làm cơ sở đo lường, điều này lý tưởng cho bố cục in và cho việc truyền đạt kích thước tới các bên liên quan quen thuộc với đơn vị imperial.

CODE_BLOCK_PLACEHOLDER_11_END

## Lưu Kết Quả

Sau khi hoàn thành các ví dụ, lưu hình ảnh kết quả vào thư mục tài liệu của bạn. Phương thức `Bitmap.Save` ghi file ở định dạng bạn chỉ định (PNG, JPEG, v.v.).

CODE_BLOCK_PLACEHOLDER_12_END

Bây giờ, bạn đã thành công trong việc sử dụng các đơn vị đo lường đa dạng trong Aspose.Drawing cho .NET, tạo ra hình ảnh trực quan của các hình chữ nhật bằng points, millimeters và inches.

## Tại sao nên sử dụng hệ thống đơn vị của Aspose.Drawing?

Aspose.Drawing hỗ trợ **hơn 30 định dạng ảnh** và có thể xử lý ảnh lên tới **5000 × 5000 pixel** mà không cần tải toàn bộ file vào bộ nhớ, mang lại hiệu suất cao cho việc tạo đồ họa quy mô lớn. Bằng cách đặt đơn vị một cách rõ ràng, bạn loại bỏ việc đoán mò, giảm lỗi chuyển đổi và đảm bảo đầu ra của bạn khớp với các kích thước vật lý chính xác trên mọi nền tảng.

## Các Vấn Đề Thường Gặp và Giải Pháp

- **Kích thước không mong muốn sau khi lưu** – Kiểm tra rằng bạn đã đặt `graphics.PageUnit` **trước** bất kỳ lời gọi vẽ nào; việc thay đổi đơn vị sau này sẽ không tự động thay đổi kích thước các hình đã vẽ.  
- **Đầu ra mờ trên màn hình DPI cao** – Tăng độ phân giải của bitmap (ví dụ, `new Bitmap(width, height, 300)`) để phù hợp với DPI mục tiêu.  
- **Đơn vị hỗn hợp trong một hình ảnh** – Tạo các instance `Graphics` riêng cho mỗi đơn vị hoặc thực hiện chuyển đổi thủ công trước khi vẽ.

## Câu Hỏi Thường Gặp

### Q1: Tôi có thể sử dụng Aspose.Drawing cho .NET với các framework .NET khác không?
A1: Có, Aspose.Drawing tương thích với nhiều framework .NET, cung cấp tính linh hoạt trong môi trường phát triển của bạn.

### Q2: Có bản dùng thử miễn phí không?
A2: Có, bạn có thể khám phá Aspose.Drawing với bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q3: Làm thế nào để tôi nhận được hỗ trợ cho Aspose.Drawing cho .NET?
A3: Truy cập [Diễn đàn Aspose.Drawing](https://forum.aspose.com/c/drawing/44) để được cộng đồng hỗ trợ và thảo luận.

### Q4: Tôi có thể mua giấy phép tạm thời cho các dự án ngắn hạn không?
A4: Có, bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### Q5: Tôi có thể tìm tài liệu chi tiết cho Aspose.Drawing ở đâu?
A5: Tài liệu đầy đủ có sẵn [tại đây](https://reference.aspose.com/drawing/net/).

---

**Cập Nhật Cuối Cùng:** 2026-05-24  
**Được Kiểm Tra Với:** Aspose.Drawing 24.11 for .NET  
**Tác Giả:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
