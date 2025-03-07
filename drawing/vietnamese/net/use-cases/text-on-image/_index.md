---
title: Thêm văn bản trên hình ảnh trong Aspose.draw
linktitle: Thêm văn bản trên hình ảnh trong Aspose.draw
second_title: Aspose.draw .NET API - Thay thế cho System.draw.common
description: Khám phá khả năng tích hợp liền mạch văn bản vào hình ảnh với Aspose.draw cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để thao tác hình ảnh dễ dàng. Tải ngay!
weight: 12
url: /vi/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm văn bản trên hình ảnh trong Aspose.draw

## Giới thiệu
Trong thế giới năng động của sự phát triển .NET, Aspose. Draw nổi bật như một công cụ mạnh mẽ để thao tác hình ảnh một cách dễ dàng. Thêm văn bản vào hình ảnh là một yêu cầu phổ biến, cho dù đó là để tạo hình mờ, chú thích hay tạo đồ họa được cá nhân hóa. Trong hướng dẫn này, chúng ta sẽ khám phá cách tận dụng Aspose.draw để tích hợp liền mạch văn bản vào hình ảnh của bạn bằng C#.
## Điều kiện tiên quyết
Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có những điều sau:
1.  Thư viện Aspose.draw: Tải xuống và cài đặt thư viện Aspose.draw từ[Aspose.draw cho tài liệu .NET](https://reference.aspose.com/drawing/net/).
2. Môi trường phát triển: Có môi trường phát triển .NET đang hoạt động, bao gồm Visual Studio hoặc bất kỳ IDE tương thích nào khác.
Bây giờ, hãy bắt đầu với hướng dẫn từng bước.
## Nhập không gian tên
Bắt đầu bằng cách nhập các không gian tên cần thiết vào dự án C# của bạn:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## Bước 1: Tải hình ảnh
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Ở đây, chúng tôi tải hình ảnh từ đường dẫn tệp đã chỉ định và khởi tạo đối tượng đồ họa để xử lý thêm.
## Bước 2: Đặt thuộc tính văn bản
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Xác định các thuộc tính của văn bản như màu sắc, phông chữ và phần đệm. Điều chỉnh các thông số này theo sở thích của bạn.
## Bước 3: Đo kích thước văn bản
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Tính toán kích thước cần thiết cho văn bản bằng cách đo từng từ riêng lẻ. Điều này đảm bảo vị trí thích hợp và tránh chồng chéo văn bản.
## Bước 4: Vẽ văn bản trên hình ảnh
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Bây giờ, định vị văn bản trên hình ảnh dựa trên kích thước được tính toán và vẽ nó bằng phông chữ và màu sắc được chỉ định.
## Bước 5: Lưu hình ảnh
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Lưu hình ảnh đã sửa đổi vào thư mục bạn muốn.
Hướng dẫn từng bước này trình bày quy trình đơn giản để thêm văn bản vào hình ảnh bằng Aspose.draw cho .NET. Thử nghiệm với các phông chữ, màu sắc và nội dung văn bản khác nhau để đạt được hiệu ứng hình ảnh mong muốn.
## Phần kết luận
Aspose.draw đơn giản hóa các tác vụ xử lý hình ảnh trong .NET, cung cấp cho các nhà phát triển một bộ công cụ mạnh mẽ. Thêm văn bản vào hình ảnh chỉ là một ví dụ về khả năng của nó, thể hiện tính linh hoạt của thư viện trong việc xử lý các phần tử đồ họa.
## Các câu hỏi thường gặp
### Aspose.draw có tương thích với tất cả các định dạng hình ảnh không?
 Aspose.draw hỗ trợ nhiều định dạng hình ảnh, bao gồm các định dạng phổ biến như JPEG, PNG và GIF. Tham khảo đến[tài liệu](https://reference.aspose.com/drawing/net/) để có danh sách đầy đủ.
### Tôi có thể sử dụng Aspose.draw cho các dự án thương mại không?
Có, Aspose.draw phù hợp cho cả dự án cá nhân và thương mại. Để biết chi tiết cấp phép, hãy truy cập[trang mua hàng](https://purchase.aspose.com/buy).
### Giấy phép tạm thời có sẵn cho mục đích thử nghiệm không?
 Có, bạn có thể xin giấy phép tạm thời để thử nghiệm bằng cách truy cập[Giấy phép tạm thời](https://purchase.aspose.com/temporary-license/).
### Tôi có thể tìm sự hỗ trợ của cộng đồng cho Aspose.draw ở đâu?
 Tương tác với cộng đồng và nhận được sự hỗ trợ về[diễn đàn Aspose.draw](https://forum.aspose.com/c/diagram/17).
### Làm cách nào để bắt đầu với Aspose.draw?
 Bắt đầu bằng cách tải xuống thư viện từ[đây](https://releases.aspose.com/drawing/net/) và khám phá toàn diện[tài liệu](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
