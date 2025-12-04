---
title: Đơn vị đo lường trong Aspose.draw cho .NET
linktitle: Đơn vị đo lường trong Aspose.draw
second_title: Aspose.draw .NET API - Thay thế cho System.draw.common
description: Khám phá tính linh hoạt của Aspose.draw cho .NET trong hướng dẫn chuyên sâu này, nắm vững các đơn vị đo lường cho đồ họa chính xác.
weight: 14
url: /vi/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đơn vị đo lường trong Aspose.draw cho .NET

## Giới thiệu

Chào mừng bạn đến với thế giới của Aspose.draw cho .NET, nơi đáp ứng được độ chính xác và tính linh hoạt trong thao tác đồ họa. Trong hướng dẫn này, chúng ta sẽ đi sâu vào sự phức tạp của các đơn vị đo lường trong Aspose. Draw, cung cấp cho bạn hướng dẫn từng bước để khai thác sức mạnh của thư viện đáng chú ý này.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.draw for .NET: Đảm bảo rằng bạn đã cài đặt thư viện. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/drawing/net/).

- Thư mục Tài liệu: Có một thư mục được chỉ định nơi bạn muốn lưu các tài liệu đã tạo của mình.

- Kiến thức cơ bản về C#: Bạn nên hiểu biết cơ bản về C# để tận dụng tối đa hướng dẫn này.

## Nhập không gian tên

Trước khi bắt đầu, hãy nhập các không gian tên cần thiết để sử dụng Aspose. Draw một cách hiệu quả:

```csharp
using System.Drawing;
```

Bây giờ, hãy chia từng ví dụ thành nhiều bước:

## Điểm là đơn vị đo lường

1. Tạo Bitmap: Khởi tạo bitmap với chiều rộng và chiều cao được chỉ định.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Tạo đồ họa: Tạo đối tượng Đồ họa từ bitmap để vẽ trên đó.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Set Page Unit to Points: Xác định điểm làm đơn vị đo (1 điểm = 1/72 inch).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Vẽ hình chữ nhật: Vẽ hình chữ nhật sử dụng các điểm làm đơn vị.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Milimet là đơn vị đo lường

1. Đặt Đơn vị Trang thành Milimet: Thay đổi đơn vị đo thành milimét (1 mm = 1/25,4 inch).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Vẽ hình chữ nhật tính bằng milimét: Vẽ một hình chữ nhật khác sử dụng milimét làm đơn vị.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Inch là đơn vị đo lường

1. Đặt đơn vị trang thành inch: Chuyển đơn vị đo sang inch.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Vẽ hình chữ nhật theo inch: Vẽ hình chữ nhật sử dụng inch làm đơn vị.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Lưu kết quả

Sau khi hoàn thành các ví dụ, hãy lưu hình ảnh thu được vào thư mục tài liệu của bạn:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Giờ đây, bạn đã điều hướng thành công các đơn vị đo lường đa dạng trong Aspose.draw cho .NET, tạo biểu diễn trực quan của hình chữ nhật bằng cách sử dụng các điểm, milimét và inch.

## Phần kết luận

Trong hướng dẫn này, chúng ta đã khám phá cách Aspose.draw cho .NET xử lý các đơn vị đo khác nhau. Bằng cách thao tác các điểm, milimét và inch, bạn có thể đạt được độ chính xác và khả năng thích ứng trong các sáng tạo đồ họa của mình. Hãy thử nghiệm những khái niệm này để phát huy toàn bộ tiềm năng của Aspose.draw.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.draw cho .NET với các khung .NET khác không?

Câu trả lời 1: Có, Aspose.draw tương thích với nhiều khung .NET khác nhau, mang lại sự linh hoạt trong môi trường phát triển của bạn.

### Q2: Có bản dùng thử miễn phí không?

 Câu trả lời 2: Có, bạn có thể khám phá Aspose. Draw bằng bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 3: Làm cách nào để nhận được hỗ trợ cho Aspose.draw cho .NET?

 A3: Tham quan[Diễn đàn Aspose.draw](https://forum.aspose.com/c/drawing/44) để được cộng đồng hỗ trợ và thảo luận.

### Câu hỏi 4: Tôi có thể mua giấy phép tạm thời cho các dự án ngắn hạn không?

 A4: Có, bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 5: Tôi có thể tìm tài liệu chi tiết về Aspose.drawing ở đâu?

 A5: Tài liệu toàn diện có sẵn[đây](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
