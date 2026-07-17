---
date: 2026-03-02
description: Nâng cao các minh họa tài liệu của bạn bằng Aspose.Drawing cho .NET!
  Học từng bước cách thêm chú thích để có hình ảnh rõ ràng và thông tin hơn.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cách Thêm Callouts với Aspose.Drawing cho .NET
url: /vi/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo Callouts trong Aspose.Drawing

## Giới thiệu
Nếu bạn đang tự hỏi **cách thêm callouts** vào hình ảnh hoặc sơ đồ của mình bằng Aspose.Drawing cho .NET, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ đi qua toàn bộ quy trình — từ tải ảnh đến vẽ các callout được thiết kế đẹp mắt — để bạn có thể làm cho minh họa của mình rõ ràng và thông tin hơn.

## Trả lời nhanh
- **Thư viện tôi cần là gì?** Aspose.Drawing cho .NET (có thể tải về từ trang chính thức).  
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Thời gian triển khai mất bao lâu?** Thông thường dưới 10 phút cho một callout cơ bản.  
- **Có thể tùy chỉnh màu sắc và phông chữ không?** Có — mọi thứ được điều khiển bằng các đối tượng GDI+ tiêu chuẩn (Pen, Font, Brush).

## Cách Thêm Callouts trong Aspose.Drawing
Dưới đây là hướng dẫn ngắn gọn, từng bước, cho thấy **cách thêm callouts** vào một hình ảnh. Bạn có thể sao chép mã, thử nghiệm với các vị trí, và điều chỉnh kiểu dáng để phù hợp với thương hiệu của mình.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

- Kiến thức cơ bản về ngôn ngữ lập trình C#.  
- Thư viện Aspose.Drawing đã được cài đặt. Bạn có thể tải về [tại đây](https://releases.aspose.com/drawing/net/).  
- Một tài liệu hoặc hình ảnh mà bạn muốn thêm callouts.

## Nhập các Namespace
Đảm bảo bạn đã bao gồm các namespace cần thiết trong dự án:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Bước 1: Tải Ảnh
Bắt đầu bằng việc tải ảnh mà bạn muốn thêm callouts. Thay `"Your Document Directory"` và `"gears.png"` bằng thư mục và tên tệp thực tế của bạn.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Bước 2: Tạo Đối Tượng Graphics
Tạo một đối tượng `Graphics` từ ảnh để thực hiện các thao tác vẽ.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Bước 3: Xác Định Vị Trí Callout
Xác định các điểm bắt đầu và kết thúc cho mỗi callout cùng với giá trị và đơn vị của callout.

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

## Bước 4: Vẽ Callouts
Triển khai phương thức `DrawCallOut` để vẽ các callout lên ảnh.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Bước 5: Lưu Ảnh
Lưu ảnh đã có callouts vào thư mục mong muốn.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Mã Nguồn Vẽ Callout
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

## Các Vấn Đề Thường Gặp & Mẹo
- **Tọa độ neo không đúng** – hãy chắc chắn rằng các điểm bắt đầu và kết thúc nằm trong giới hạn của ảnh; nếu không callout có thể bị cắt.  
- **Văn bản chồng lên nhau** – điều chỉnh `spaceSize` hoặc kích thước phông chữ nếu nhãn va chạm với các đồ họa khác.  
- **Hiệu năng** – đối với các ảnh rất lớn, hãy xem xét việc giải phóng các đối tượng `Pen`, `Font`, và `Brush` sau khi sử dụng để giải phóng tài nguyên.

## Kết luận
Chúc mừng! Bây giờ bạn đã biết **cách thêm callouts** vào một ảnh bằng Aspose.Drawing cho .NET. Hãy tự do thử nghiệm với các vị trí, màu sắc và phông chữ khác nhau để phù hợp với phong cách trực quan của bạn.

## Câu Hỏi Thường Gặp

### Tôi có thể dùng Aspose.Drawing cho các loại minh họa khác không?
Có, Aspose.Drawing hỗ trợ một loạt các thao tác vẽ cho nhiều loại minh họa khác nhau.

### Aspose.Drawing có tương thích với các định dạng ảnh khác nhau không?
Chắc chắn! Aspose.Drawing hỗ trợ các định dạng ảnh phổ biến như PNG, JPEG, GIF và nhiều hơn nữa.

### Tôi có thể tìm thêm ví dụ và tài liệu ở đâu?
Khám phá tài liệu đầy đủ [tại đây](https://reference.aspose.com/drawing/net/).

### Làm sao tôi có thể nhận hỗ trợ nếu gặp vấn đề?
Truy cập diễn đàn [Aspose.Drawing](https://forum.aspose.com/c/drawing/44) để nhận hỗ trợ từ cộng đồng.

### Tôi có thể dùng thử Aspose.Drawing trước khi mua không?
Chắc chắn! Bắt đầu với bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

**Câu Hỏi & Trả Lời Bổ Sung**

**H: Tôi có thể thay đổi kiểu đường callout (gạch đứt, chấm) không?**  
Đ: Có — chỉ cần cấu hình thuộc tính `Pen.DashStyle` trước khi vẽ đường.

**H: Có thể thêm màu nền cho nhãn callout không?**  
Đ: Hoàn toàn có thể. Tạo một `SolidBrush` với màu mong muốn và tô một hình chữ nhật phía sau văn bản trước khi gọi `DrawString`.

**H: Làm sao để đảm bảo callout hiển thị giống nhau trên màn hình DPI cao?**  
Đ: Đặt `graphics.PageUnit = GraphicsUnit.Pixel` (như trong ví dụ) và sử dụng các đo lường dựa trên vector để duy trì tỷ lệ phóng đại nhất quán.

---

**Cập nhật lần cuối:** 2026-03-02  
**Đã kiểm tra với:** Aspose.Drawing 24.11 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}