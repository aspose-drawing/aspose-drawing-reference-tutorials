---
date: 2026-02-27
description: Học cách tạo hình ảnh thiệp sinh nhật bằng Aspose.Drawing cho .NET. Hướng
  dẫn này cho bạn biết cách vẽ chuỗi ký tự lên hình ảnh, chồng lớp văn bản lên ảnh
  và thêm chú thích vào ảnh một cách nhanh chóng.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cách tạo hình ảnh thiệp sinh nhật với Aspose.Drawing
url: /vi/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Tạo Hình Ảnh Thiệp Sinh Nhật với Aspose.Drawing

## Giới thiệu
Trong thế giới .NET năng động, Aspose.Drawing nổi bật như một công cụ mạnh mẽ để thao tác hình ảnh một cách dễ dàng. Cho dù bạn cần **create birthday card image**, thêm watermark, hoặc chỉ đơn giản là overlay text on picture, hướng dẫn này sẽ dẫn bạn qua các bước chính xác để draw string on image bằng C#. Khi kết thúc hướng dẫn, bạn sẽ có một thiệp sinh nhật cá nhân hoá sẵn sàng chia sẻ.

## Câu trả lời nhanh
- **Thư viện nào nên dùng?** Aspose.Drawing for .NET  
- **Có thể thêm caption vào ảnh không?** Có – use `Graphics.DrawString` with custom fonts.  
- **Cần giấy phép cho môi trường production không?** Có, a commercial license is needed.  
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Thời gian triển khai mất bao lâu?** Thường dưới 10 phút cho một thiệp đơn giản.

## Thiệp Sinh Nhật là gì?
Một hình ảnh thiệp sinh nhật là một bức ảnh cá nhân hoá kết hợp ảnh nền với văn bản tùy chỉnh—như lời chúc, tên người nhận, hoặc thông điệp chúc mừng. Sử dụng Aspose.Drawing, bạn có thể tạo các thiệp này một cách lập trình mà không cần công cụ thiết kế đồ họa thủ công.

## Tại sao nên dùng Aspose.Drawing để Overlay Text on Picture?
- **Hỗ trợ đa nền tảng:** Hoạt động trên Windows, Linux và macOS.  
- **Rich drawing API:** Full control over fonts, colors, and layout.  
- **Không có phụ thuộc bên ngoài:** Thay thế `System.Drawing.Common` bằng một thư viện được quản lý hoàn toàn.  
- **Hiệu năng cao:** Tối ưu cho xử lý hàng loạt hình ảnh.

## Yêu cầu trước
Trước khi bắt đầu hướng dẫn, hãy chắc chắn bạn đã chuẩn bị các yếu tố sau:

1. Aspose.Drawing Library: Tải xuống và cài đặt thư viện Aspose.Drawing từ [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/).  
2. Development Environment: Môi trường phát triển .NET hoạt động, chẳng hạn Visual Studio hoặc Visual Studio Code, với .NET 6 SDK hoặc phiên bản mới hơn đã được cài đặt.

Bây giờ, chúng ta sẽ đi qua hướng dẫn từng bước để thêm văn bản vào hình ảnh và lưu lại như một thiệp sinh nhật.

## Nhập các Namespace
Bắt đầu bằng cách nhập các namespace cần thiết vào dự án C# của bạn:

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## Bước 1: Tải ảnh
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Ở đây, chúng ta tải ảnh từ đường dẫn tệp đã chỉ định và khởi tạo đối tượng graphics để xử lý tiếp theo.

## Bước 2: Đặt thuộc tính văn bản
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Xác định các thuộc tính văn bản như màu, phông chữ và padding. Điều chỉnh các tham số này theo sở thích thiết kế của bạn.

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
Tính kích thước cần thiết cho văn bản bằng cách đo từng từ một cách riêng lẻ. Điều này đảm bảo vị trí chính xác và tránh chồng lấn văn bản.

## Bước 4: Vẽ văn bản lên ảnh
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Bây giờ, đặt vị trí văn bản trên ảnh dựa trên kích thước đã tính và vẽ nó bằng phông chữ và màu đã chỉ định.

## Bước 5: Lưu ảnh
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Lưu ảnh đã chỉnh sửa vào thư mục mong muốn. Tệp kết quả là một hình ảnh thiệp sinh nhật sẵn sàng gửi.

## Các trường hợp sử dụng phổ biến & Mẹo
- **Thêm caption vào ảnh:** Thay thế `text` bằng bất kỳ caption nào bạn cần, chẳng hạn “Celebrating 30 Years!”.  
- **Draw text on bitmap:** Cách tiếp cận này cũng hoạt động cho các đối tượng `Bitmap` được tạo từ đầu.  
- **Overlay multiple lines:** Lặp qua một mảng các chuỗi và điều chỉnh tọa độ Y của `Rectangle` cho mỗi dòng.  
- **Pro tip:** Sử dụng `Graphics.SmoothingMode = SmoothingMode.AntiAlias` để render văn bản mượt hơn.

## Kết luận
Aspose.Drawing đơn giản hoá các nhiệm vụ thao tác hình ảnh trong .NET, cung cấp cho nhà phát triển một bộ công cụ mạnh mẽ. Thêm văn bản vào hình ảnh—cho dù để **create birthday card image**, **draw string on image**, hoặc **add caption to photo**—chỉ là một ví dụ về tính đa năng của nó trong việc xử lý các yếu tố đồ họa.

## Câu hỏi thường gặp
### Aspose.Drawing có tương thích với tất cả các định dạng ảnh không?
Aspose.Drawing hỗ trợ nhiều định dạng ảnh, bao gồm các định dạng phổ biến như JPEG, PNG và GIF. Tham khảo [documentation](https://reference.aspose.com/drawing/net/) để xem danh sách đầy đủ.

### Tôi có thể sử dụng Aspose.Drawing cho dự án thương mại không?
Có, Aspose.Drawing phù hợp cho cả dự án cá nhân và thương mại. Để biết chi tiết giấy phép, hãy truy cập [purchase page](https://purchase.aspose.com/buy).

### Có giấy phép tạm thời cho mục đích thử nghiệm không?
Có, bạn có thể nhận giấy phép tạm thời để thử nghiệm bằng cách truy cập [Temporary License](https://purchase.aspose.com/temporary-license/).

### Tôi có thể tìm hỗ trợ cộng đồng cho Aspose.Drawing ở đâu?
Tham gia cộng đồng và nhận hỗ trợ tại [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).

### Làm sao để bắt đầu với Aspose.Drawing?
Bắt đầu bằng cách tải thư viện từ [here](https://releases.aspose.com/drawing/net/) và khám phá [documentation](https://reference.aspose.com/drawing/net/) đầy đủ.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-02-27  
**Kiểm tra với:** Aspose.Drawing 24.11 for .NET  
**Tác giả:** Aspose