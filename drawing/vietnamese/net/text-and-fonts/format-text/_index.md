---
date: 2026-02-25
description: Tìm hiểu cách thiết lập căn chỉnh văn bản trong Aspose.Drawing cho .NET
  và thêm văn bản vào hình ảnh. Hướng dẫn từng bước kèm ví dụ.
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Thiết lập căn chỉnh văn bản với Aspose.Drawing cho .NET
url: /vi/net/text-and-fonts/format-text/
weight: 11
---

 formatting.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Căn Văn Bản trong Aspose.Drawing

## Giới thiệu

Khi nói đến **set text alignment** và định dạng văn bản trong các ứng dụng .NET của bạn, Aspose.Drawing là thư viện được các nhà phát triển lựa chọn để có độ chính xác, hiệu năng và một API phong phú. Dù bạn đang xây dựng một engine báo cáo, một trình tạo huy hiệu động, hay bất kỳ giải pháp đồ họa nào, việc kiểm soát cách văn bản căn chỉnh bên trong các hình dạng sẽ giúp kết quả của bạn trông chuyên nghiệp và tinh tế. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình — từ tạo canvas bitmap, vẽ hình chữ nhật có văn bản, xử lý tràn văn bản, cho tới lưu ảnh.

## Câu trả lời nhanh
- **“set text alignment” có nghĩa là gì?** Nó xác định cách văn bản được đặt vị trí theo chiều ngang và chiều dọc bên trong một hình chữ nhật vẽ.  
- **Lớp nào điều khiển căn chỉnh?** `StringFormat` cho phép bạn đặt `Alignment` và `LineAlignment`.  
- **Tôi có thể vẽ một chuỗi và một hình chữ nhật cùng lúc không?** Có — sử dụng `Graphics.DrawRectangle` rồi tiếp theo là `Graphics.DrawString`.  
- **Làm sao ngăn văn bản tràn ra ngoài?** Điều chỉnh kích thước hình chữ nhật hoặc chia văn bản thành nhiều dòng một cách thủ công.  
- **Có cần giấy phép cho môi trường production không?** Cần có giấy phép thương mại Aspose.Drawing cho việc sử dụng không phải thử nghiệm.

## **set text alignment** là gì trong Aspose.Drawing?

`set text alignment` đề cập đến việc cấu hình vị trí ngang (`StringAlignment`) và dọc (`LineAlignment`) của văn bản bên trong một `Rectangle` hoặc bất kỳ vùng vẽ nào. Bằng cách điều chỉnh các thiết lập này, bạn kiểm soát việc văn bản hiển thị căn trái, căn giữa, căn phải, căn trên, căn giữa dọc, hoặc căn dưới.

## Tại sao nên sử dụng Aspose.Drawing cho việc căn văn bản?

- **Tương thích đầy đủ với .NET** – hoạt động với .NET Framework, .NET Core và .NET 5/6+.  
- **Kết xuất pixel‑perfect** – hỗ trợ anti‑aliasing và DPI cao ngay từ đầu.  
- **Không có giới hạn GDI+** – khác với `System.Drawing.Common`, Aspose.Drawing chạy trên container Linux mà không cần phụ thuộc gốc.  
- **Styling phong phú** – kết hợp phông chữ, brush, pen và các đối tượng `StringFormat` tùy chỉnh để tạo bố cục tinh vi.

## Yêu cầu trước

1. **Thư viện Aspose.Drawing** – tải về [tại đây](https://releases.aspose.com/drawing/net/).  
2. **Môi trường phát triển** – Visual Studio 2022 (hoặc bất kỳ IDE C# nào).  
3. **Kiến thức .NET cơ bản** – bạn nên quen thuộc với dự án C# và các gói NuGet.

## Nhập các Namespace

Để bắt đầu, đưa các namespace cần thiết vào phạm vi. Chúng cung cấp quyền truy cập vào đồ họa, render văn bản và các primitive vẽ.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Bước 1: Tạo đối tượng Bitmap và Graphics  

Tạo một bitmap cung cấp canvas để bạn có thể vẽ lên. Đối tượng `Graphics` là bề mặt vẽ, và chúng ta bật render văn bản chất lượng cao bằng `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Bước 2: Định nghĩa **StringFormat** và Kiểu dáng  

Ở đây chúng ta **set text alignment** bằng cách cấu hình một thể hiện `StringFormat`. Đồng thời chuẩn bị các brush, pen và font sẽ được dùng khi vẽ chuỗi.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Bước 3: Tạo và Định dạng Văn bản – **how to draw string** và **draw rectangle with text**

Chúng ta tạo nội dung văn bản, định nghĩa hình chữ nhật chứa nó, rồi vẽ cả viền hình chữ nhật và chuỗi văn bản.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Cách xử lý tràn văn bản

Nếu `text` cung cấp vượt quá giới hạn của hình chữ nhật, bạn có hai lựa chọn phổ biến:

1. **Resize the rectangle** – tăng `rectangle.Width` hoặc `rectangle.Height`.  
2. **Split the text** – chia chuỗi thành các dòng phù hợp, sau đó gọi `DrawString` cho mỗi dòng với tọa độ Y đã điều chỉnh.

## Bước 4: Lưu Kết quả – **add text to image**

Cuối cùng, ghi bitmap ra đĩa. Bước này minh họa **add text to image** trong một lời gọi duy nhất.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Văn bản bị mờ** | Đảm bảo rằng `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` được thiết lập. |
| **Văn bản bị cắt** | Tăng kích thước hình chữ nhật hoặc bật logic ngắt từ bằng cách đo kích thước chuỗi (`Graphics.MeasureString`). |
| **Phông chữ không tìm thấy** | Kiểm tra xem phông chữ đã được cài đặt trên máy chủ hay chưa hoặc nhúng phông chữ riêng bằng `PrivateFontCollection`. |
| **Màu không mong muốn** | Kiểm tra lại màu của brush và pen; nhớ rằng `Color.FromKnownColor` sử dụng các màu được hệ thống định nghĩa. |

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Drawing có tương thích với tất cả các phiên bản .NET không?

**Trả lời:** Có, Aspose.Drawing được thiết kế để tương thích với một loạt các phiên bản .NET, đảm bảo tính linh hoạt cho các nhà phát triển.

### Câu hỏi 2: Tôi có thể tùy chỉnh kiểu phông chữ thêm không?

**Trả lời:** Chắc chắn! Điều chỉnh các tham số của đối tượng `Font` để đạt được kích thước, kiểu và họ phông chữ mong muốn.

### Câu hỏi 3: Làm thế nào để xử lý tràn văn bản trong hình chữ nhật đã định nghĩa?

**Trả lời:** Bạn có thể quản lý tràn văn bản bằng cách điều chỉnh kích thước của hình chữ nhật hoặc triển khai logic tùy chỉnh để xử lý văn bản dài.

### Câu hỏi 4: Có các tùy chọn định dạng khác có sẵn trong Aspose.Drawing không?

**Trả lời:** Có, Aspose.Drawing cung cấp một bộ công cụ toàn diện cho việc xử lý đồ họa, bao gồm nhiều tùy chọn định dạng cho văn bản, hình dạng và hơn thế nữa.

### Câu hỏi 5: Tôi có thể tìm hỗ trợ bổ sung cho Aspose.Drawing ở đâu?

**Trả lời:** Khám phá diễn đàn Aspose.Drawing [tại đây](https://forum.aspose.com/c/drawing/44) để nhận hỗ trợ cộng đồng và thảo luận.

**Additional Q&A**

**Q: Làm thế nào để vẽ một chuỗi mà không có hình chữ nhật bao quanh?**  
**A:** Bỏ qua lời gọi `DrawRectangle` và truyền vị trí `PointF` mong muốn vào `Graphics.DrawString`.

**Q: Tôi có thể xoay văn bản trong khi vẫn giữ căn chỉnh không?**  
**A:** Có — áp dụng biến đổi `Matrix` cho đối tượng `Graphics` trước khi vẽ, sau đó đặt lại lại sau khi hoàn thành.

**Q: Có thể xuất ảnh dưới dạng JPEG thay vì PNG không?**  
**A:** Chỉ cần thay đổi phần mở rộng tệp trong `bitmap.Save` và tùy chọn chỉ định `ImageFormat.Jpeg`.

---

**Cập nhật lần cuối:** 2026-02-25  
**Kiểm tra với:** Aspose.Drawing 24.11 for .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}