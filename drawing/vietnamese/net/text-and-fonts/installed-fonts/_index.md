---
date: 2025-12-06
description: Tìm hiểu cách lưu tệp hình ảnh PNG đồng thời liệt kê các phông chữ đã
  cài đặt, hiển thị họ phông chữ, tạo đồ họa từ bitmap và vẽ văn bản bằng phông chữ
  sử dụng Aspose.Drawing cho .NET.
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Lưu hình ảnh PNG và làm việc với các phông chữ đã cài đặt trong Aspose.Drawing
url: /vi/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu ảnh PNG và làm việc với các phông chữ đã cài đặt trong Aspose.Drawing

## Giới thiệu

Nếu bạn cần **lưu tệp ảnh PNG** đồng thời hiển thị thông tin về các phông chữ đã cài đặt trên máy, Aspose.Drawing cho .NET cung cấp cho bạn một cách sạch sẽ, đa nền tảng để thực hiện. Trong hướng dẫn này, chúng ta sẽ đi qua việc liệt kê các phông chữ đã cài đặt, hiển thị các họ phông chữ, tạo đồ họa từ bitmap và vẽ văn bản bằng phông chữ — tất cả đều cuối cùng được lưu dưới dạng ảnh PNG. Khi kết thúc, bạn sẽ có một đoạn mã có thể tái sử dụng trong bất kỳ dự án .NET nào.

## Trả lời nhanh
- **Hướng dẫn này tạo gì?** Một ảnh PNG liệt kê các họ phông chữ đã cài đặt.  
- **Thư viện nào cần thiết?** Aspose.Drawing cho .NET (không cần System.Drawing.Common).  
- **Có thể dùng phông chữ tùy chỉnh không?** Có – chỉ cần tải chúng vào một `InstalledFontCollection`.  
- **Độ phân giải đầu ra có thể điều chỉnh không?** Chắc chắn – thay đổi kích thước bitmap hoặc định dạng pixel.  
- **Có cần giấy phép để chạy mã không?** Giấy phép tạm thời hoạt động cho việc đánh giá; giấy phép đầy đủ cần thiết cho môi trường sản xuất.

## “Lưu ảnh PNG” trong ngữ cảnh Aspose.Drawing là gì?
Lưu ảnh PNG có nghĩa là render bề mặt vẽ của bạn (một `Bitmap`) thành tệp có phần mở rộng `.png`. Aspose.Drawing xử lý việc mã hoá cho bạn, vì vậy bạn chỉ cần gọi `bitmap.Save(...)` với đường dẫn mong muốn.

## Tại sao phải liệt kê các phông chữ đã cài đặt và hiển thị các họ phông chữ?
Biết được những phông chữ nào có sẵn cho phép bạn tạo đồ họa động thích ứng với môi trường của người dùng cuối. Điều này đặc biệt hữu ích khi tạo báo cáo, chứng chỉ, hoặc bất kỳ nội dung hình ảnh nào cần phù hợp với thương hiệu công ty mà không cần phân phối các tệp phông chữ.

## Yêu cầu trước

- **Thư viện Aspose.Drawing** – tải phiên bản mới nhất từ [trang tải Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider, hoặc bất kỳ trình soạn thảo nào hỗ trợ .NET.  
- **Kiến thức C# cơ bản** – bạn nên quen thuộc với lớp, đối tượng và các vòng lặp đơn giản.

## Nhập không gian tên
Để làm việc với phông chữ và đồ họa, nhập các không gian tên sau ở đầu tệp C# của bạn:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Hướng dẫn từng bước

### Bước 1: Tạo bitmap (bảng vẽ)
Đầu tiên, chúng ta tạo một bitmap sẽ chứa ảnh cuối cùng. Kích thước bitmap và định dạng pixel quyết định chất lượng của PNG được lưu.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Bước 2: Tạo graphics từ bitmap
Tiếp theo, chúng ta lấy một đối tượng `Graphics` từ bitmap. Đối tượng này cho phép chúng ta vẽ hình, văn bản và ảnh lên bảng vẽ.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Bước 3: Thiết lập brush và font (vẽ văn bản với phông chữ)
Chúng ta cần một brush cho màu văn bản và một đối tượng `Font` xác định kiểu chữ, kích thước và kiểu dáng.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Bước 4: Liệt kê các phông chữ đã cài đặt và hiển thị các họ phông chữ
Bây giờ chúng ta hiển thị số lượng các họ phông chữ và một vài tên đầu tiên trực tiếp trên bitmap. Điều này minh họa khả năng **liệt kê các phông chữ đã cài đặt** và **hiển thị các họ phông chữ**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Bước 5: Lưu ảnh PNG
Cuối cùng, chúng ta ghi bitmap ra đĩa dưới dạng tệp PNG. Đây là thao tác cốt lõi **lưu ảnh png**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Mẹo chuyên nghiệp:** Sử dụng `Path.Combine` để xây dựng đường dẫn tệp nhằm tránh các vấn đề về ký tự phân tách thư mục trên các hệ điều hành khác nhau.

## Các vấn đề thường gặp và giải pháp
| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **Không hiển thị phông chữ** | `InstalledFontCollection` không được nạp (ví dụ: chạy trên máy chủ không có giao diện đồ họa). | Cài đặt các phông chữ cần thiết trên máy chủ hoặc nhúng phông chữ tùy chỉnh vào ứng dụng của bạn. |
| **Tệp đã lưu bị hỏng** | Định dạng pixel không đúng hoặc thiếu quyền ghi. | Đảm bảo thư mục đích tồn tại và ứng dụng có quyền ghi; giữ `Format32bppPArgb`. |
| **Văn bản bị mờ** | Cài đặt DPI thấp. | Tăng kích thước bitmap hoặc đặt `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Câu hỏi thường gặp

**H: Tôi có thể sử dụng phông chữ tùy chỉnh không có trên máy không?**  
Đ: Có. Tải tệp phông chữ vào một `PrivateFontCollection` và tạo `Font` từ bộ sưu tập đó.

**H: Làm sao xử lý các ngoại lệ liên quan đến phông chữ?**  
Đ: Bao quanh việc tạo phông chữ bằng khối `try/catch` và kiểm tra `ArgumentException` để biết thiếu họ phông chữ.

**H: Aspose.Drawing có phù hợp cho ứng dụng web không?**  
Đ: Hoàn toàn. Thư viện hoạt động trong ASP.NET Core, Azure Functions và các môi trường phía máy chủ khác.

**H: Tôi có thể thay đổi màu hoặc kiểu chữ không?**  
Đ: Có. Sử dụng các loại `Brush` khác nhau (ví dụ: `LinearGradientBrush`) và thay đổi enum `FontStyle`.

**H: Tôi có thể lấy giấy phép tạm thời để thử nghiệm ở đâu?**  
Đ: Tải giấy phép dùng thử từ [trang giấy phép tạm thời của Aspose](https://purchase.aspose.com/temporary-license/).

## Kết luận

Bằng cách thực hiện các bước trên, bạn đã học được cách **lưu tệp ảnh PNG** mà động **liệt kê các phông chữ đã cài đặt**, **hiển thị các họ phông chữ**, **tạo đồ họa từ bitmap**, và **vẽ văn bản với phông chữ** bằng Aspose.Drawing cho .NET. Hãy tự do thử nghiệm với các phông chữ, màu sắc và kích thước bitmap khác nhau để đáp ứng yêu cầu hình ảnh của dự án.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2025-12-06  
**Đã kiểm tra với:** Aspose.Drawing 24.11 cho .NET  
**Tác giả:** Aspose