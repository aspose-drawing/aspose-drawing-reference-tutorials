---
title: Điền các vùng trong Aspose.draw
linktitle: Điền các vùng trong Aspose.draw
second_title: Aspose.draw .NET API - Thay thế cho System.draw.common
description: Tìm hiểu cách điền các vùng trong Aspose.draw cho .NET bằng hướng dẫn từng bước này. Nâng cao kỹ năng thiết kế đồ họa của bạn một cách dễ dàng.
weight: 20
url: /vi/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Điền các vùng trong Aspose.draw

## Giới thiệu

Việc tạo đồ họa hấp dẫn trực quan thường liên quan đến việc lấp đầy các vùng bằng màu sắc, hoa văn hoặc độ chuyển màu. Aspose.draw for .NET cung cấp các công cụ mạnh mẽ để đạt được điều này một cách hiệu quả. Trong hướng dẫn này, chúng ta sẽ đi sâu vào quá trình lấp đầy các vùng bằng Aspose.draw, một thư viện đa năng giúp đơn giản hóa các thao tác đồ họa trong các ứng dụng .NET.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

1.  Thư viện Aspose.draw: Tải xuống và cài đặt thư viện Aspose.draw. Bạn có thể tìm thấy thư viện và tài liệu của nó[đây](https://reference.aspose.com/drawing/net/).

2. Môi trường phát triển: Thiết lập môi trường phát triển .NET, chẳng hạn như Visual Studio, để tích hợp Aspose.draw vào các dự án của bạn.

## Nhập không gian tên

Bắt đầu bằng cách nhập các không gian tên cần thiết vào dự án của bạn. Các không gian tên này cung cấp quyền truy cập vào các lớp và phương thức cần thiết để làm việc với Aspose.drawing.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


Bây giờ, hãy chia mã ví dụ thành nhiều bước để hiểu rõ ràng và toàn diện.

## Bước 1: Tạo đối tượng Bitmap và đồ họa

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Trong bước này, chúng ta khởi tạo một bitmap mới và một đối tượng đồ họa để vẽ trên đó.

## Bước 2: Xác định GraphicsPath và Tạo Vùng

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

Xác định đường dẫn đồ họa bằng cách chỉ định một đa giác với một tập hợp các điểm. Tạo một vùng bằng đường dẫn này.

## Bước 3: Loại trừ khu vực bên trong

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

Tạo một đường dẫn đồ họa khác biểu thị một hình chữ nhật bên trong và loại trừ nó khỏi vùng chính.

## Bước 4: Chọn Brush và tô màu vùng

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

Chọn một cọ vẽ (trong trường hợp này là màu xanh lam đồng nhất) và tô màu vùng được xác định trước đó bằng cọ đã chọn.

## Bước 5: Lưu hình ảnh kết quả

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

Lưu hình ảnh cuối cùng vào thư mục bạn muốn.

## Phần kết luận

Điền các vùng trong Aspose.draw cho .NET là một quá trình đơn giản, cung cấp cho bạn sự linh hoạt để tạo đồ họa phức tạp và hấp dẫn về mặt hình ảnh. Hãy thử nghiệm với nhiều hình dạng, màu sắc và hoa văn khác nhau để phát huy khả năng sáng tạo của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.draw cho các dự án thương mại không?

 Trả lời 1: Có, Aspose.draw có thể được sử dụng cho cả dự án cá nhân và thương mại. Để biết chi tiết cấp phép, hãy truy cập[đây](https://purchase.aspose.com/buy).

### Q2: Có bản dùng thử miễn phí không?

 Câu trả lời 2: Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu 3: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.drawing?

 A3: Tham quan[diễn đàn Aspose.draw](https://forum.aspose.com/c/diagram/17) để nhận được sự hỗ trợ từ cộng đồng và các chuyên gia.

### Câu hỏi 4: Tôi có thể tạo hình ảnh động bằng Aspose.drawing không?

A4: Chắc chắn rồi. Aspose. Draw cho phép bạn tạo và thao tác hình ảnh một cách linh hoạt trong các ứng dụng .NET của mình.

### Câu hỏi 5: Có giấy phép tạm thời không?

 Câu trả lời 5: Có, có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
