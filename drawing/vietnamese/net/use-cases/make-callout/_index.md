---
title: Tạo chú thích trong Aspose.draw
linktitle: Tạo chú thích trong Aspose.draw
second_title: Aspose.draw .NET API - Thay thế cho System.draw.common
description: Nâng cao hình ảnh minh họa tài liệu của bạn bằng Aspose.draw cho .NET! Tìm hiểu từng bước cách thêm chú thích để có hình ảnh rõ ràng và giàu thông tin hơn.
weight: 10
url: /vi/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo chú thích trong Aspose.draw

## Giới thiệu
Chào mừng bạn đến với hướng dẫn từng bước của chúng tôi về cách tạo chú thích trong Aspose.draw cho .NET! Nếu bạn đang tìm cách cải thiện hình minh họa tài liệu của mình bằng chú thích thì bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ chia quy trình thành các bước có thể quản lý được bằng thư viện Aspose.draw.
## Điều kiện tiên quyết
Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:
- Kiến thức cơ bản về ngôn ngữ lập trình C#.
-  Đã cài đặt thư viện Aspose.draw. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/drawing/net/).
- Tài liệu hoặc hình ảnh mà bạn muốn thêm chú thích.
## Nhập không gian tên
Đảm bảo bạn có các không gian tên cần thiết trong dự án của mình:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Bước 1: Tải hình ảnh
 Bắt đầu bằng cách tải hình ảnh nơi bạn muốn thêm chú thích. Thay thế`"Your Document Directory"` Và`"gears.png"` với thư mục thực tế và tên tệp hình ảnh của bạn.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Mã của bạn ở đây
}
```
## Bước 2: Tạo đối tượng đồ họa
 Tạo một`Graphics` đối tượng khỏi ảnh để thực hiện các thao tác vẽ.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Bước 3: Xác định vị trí chú thích
Xác định điểm bắt đầu và điểm kết thúc cho mỗi chú thích cùng với giá trị và đơn vị chú thích.
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
## Bước 4: Vẽ chú thích
 Thực hiện các`DrawCallOut` phương pháp vẽ chú thích trên hình ảnh.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Bước 5: Lưu hình ảnh
Lưu hình ảnh có chú thích vào thư mục bạn muốn.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Vẽ mã nguồn chú thích
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
## Phần kết luận

Chúc mừng! Bạn đã thêm thành công chú thích vào hình ảnh của mình bằng Aspose.draw cho .NET. Hãy thoải mái thử nghiệm các vị trí và giá trị khác nhau để tùy chỉnh thêm chú thích của bạn.

## Câu hỏi thường gặp

### Tôi có thể sử dụng Aspose.draw cho các loại hình minh họa khác không?

Có, Aspose.draw hỗ trợ nhiều thao tác vẽ cho nhiều loại hình minh họa khác nhau.

### Aspose.draw có tương thích với các định dạng hình ảnh khác nhau không?

Tuyệt đối! Aspose.draw hỗ trợ các định dạng hình ảnh phổ biến như PNG, JPEG, GIF, v.v.

### Tôi có thể tìm thêm ví dụ và tài liệu ở đâu?

 Khám phá tài liệu toàn diện[đây](https://reference.aspose.com/drawing/net/).

### Làm cách nào để nhận được hỗ trợ nếu tôi gặp sự cố?

 Tham quan[diễn đàn Aspose.draw](https://forum.aspose.com/c/drawing/44) để hỗ trợ cộng đồng.

### Tôi có thể dùng thử Aspose.draw trước khi mua không?

 Chắc chắn! Bắt đầu dùng thử miễn phí[đây](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
