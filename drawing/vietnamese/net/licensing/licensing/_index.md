---
date: 2026-02-09
description: Tìm hiểu cách thiết lập giấy phép Aspose.Drawing trong .NET. Thành thạo
  các phương pháp cấp phép để mở khóa đầy đủ tính năng mà không có watermark.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cài đặt giấy phép Aspose.Drawing – Cách cài đặt giấy phép Aspose.Drawing
url: /vi/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt giấy phép Aspose.Drawing

## Giới thiệu

Nếu bạn đang xây dựng các ứng dụng .NET dựa vào đồ họa mạnh mẽ và xử lý ảnh, **việc đặt giấy phép Aspose.Drawing** là bước đầu tiên để loại bỏ các hạn chế của phiên bản dùng thử và truy cập đầy đủ các tính năng. Trong hướng dẫn này, bạn sẽ học ba cách thực tế để đặt giấy phép Aspose.Drawing — tải từ tệp, tải từ luồng, và sử dụng mô hình tính phí theo mức sử dụng — để bạn có thể tích hợp thư viện một cách tự tin.

## Câu trả lời nhanh
- **Cách chính để kích hoạt Aspose.Drawing là gì?** Tải tệp giấy phép bằng cách sử dụng `License.SetLicense("Aspose.Drawing.lic")`.  
- **Tôi có thể áp dụng giấy phép tại thời gian chạy không?** Có, bạn có thể tải giấy phép từ một `Stream` cho các kịch bản động.  
- **Có hỗ trợ giấy phép metered không?** Chắc chắn; sử dụng `Metered.SetMeteredKey(publicKey, privateKey)` để bật thanh toán dựa trên tiêu thụ.  
- **Tôi có cần giấy phép cho bản dựng phát triển không?** Bản dùng thử hoạt động cho việc thử nghiệm, nhưng giấy phép hợp lệ sẽ loại bỏ watermark và mở khóa tất cả các API.  
- **Các phiên bản .NET nào tương thích?** Aspose.Drawing hỗ trợ .NET Framework 4.x, .NET Core 3.1+, và .NET 5/6+.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

- **Thư viện Aspose.Drawing** – tải gói mới nhất từ [here](https://releases.aspose.com/drawing/net/).  
- **Tệp giấy phép** – nhận tệp `.lic` hợp lệ từ [Aspose](https://purchase.aspose.com/buy).  
- **Môi trường phát triển .NET** – Visual Studio, Rider, hoặc bất kỳ IDE nào hỗ trợ .NET Framework/.NET Core.

## Nhập không gian tên

Chúng ta cần các không gian tên .NET tiêu chuẩn cộng với không gian tên Aspose.Drawing để cấp phép. Thêm các câu lệnh `using` sau vào đầu tệp C# của bạn:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Tải giấy phép từ tệp

Tải giấy phép từ tệp là cách tiếp cận đơn giản nhất. Thực hiện ba bước sau:

### Bước 1: Khởi tạo đối tượng License

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Bước 2: Đặt giấy phép từ tệp `.lic`

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Bước 3: Xác nhận thành công

```csharp
Console.WriteLine("License set successfully.");
```

> **Mẹo:** Đặt tệp `.lic` trong cùng thư mục với tệp thực thi của bạn hoặc cung cấp đường dẫn tuyệt đối để tránh lỗi “file not found”.

## Tải giấy phép từ Stream

Khi tệp giấy phép của bạn được nhúng dưới dạng tài nguyên hoặc lấy từ vị trí từ xa, việc tải nó từ một `Stream` sẽ mang lại sự linh hoạt.

### Bước 1: Khởi tạo đối tượng License

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Bước 2: Tải giấy phép bằng `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Bước 3: Xác nhận thành công

```csharp
Console.WriteLine("License set successfully.");
```

> **Cảnh báo:** Hãy nhớ giải phóng `FileStream` (hoặc sử dụng khối `using`) để giải phóng các handle tệp.

## Sử dụng giấy phép Metered

Giấy phép metered lý tưởng cho các kịch bản SaaS hoặc trả‑theo‑sử dụng. Nó theo dõi tiêu thụ và tính phí dựa trên mức sử dụng thực tế.

### Bước 1: Khởi tạo đối tượng Metered

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Bước 2: Đặt khóa công khai và khóa riêng

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Bước 3: Thực hiện xử lý ảnh của bạn

```csharp
// Your image processing logic here
```

### Bước 4: Lấy thông tin tiêu thụ

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Bước 5: Hiển thị chi tiết tiêu thụ

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Cạm bẫy thường gặp:** Nếu bạn quên gọi `SetMeteredKey`, API sẽ quay lại chế độ dùng thử và bạn sẽ thấy watermark trong đầu ra.

## Tại sao cần đặt giấy phép Aspose.Drawing đúng cách?

- **Loại bỏ watermark** xuất hiện trong chế độ dùng thử.  
- **Mở khóa các API cao cấp** như bộ lọc ảnh nâng cao và chuyển đổi PDF.  
- **Đảm bảo tuân thủ** các điều khoản cấp phép của Aspose cho việc phân phối thương mại.  
- **Kích hoạt thanh toán theo mức sử dụng**, cho phép bạn chỉ trả tiền cho những gì bạn dùng.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| Lỗi “Không tìm thấy tệp giấy phép” | Đường dẫn sai hoặc tệp thiếu trong thư mục đầu ra | Sử dụng đường dẫn tuyệt đối hoặc đặt thuộc tính *Copy to Output Directory* của tệp thành *Copy always*. |
| Vẫn xuất hiện watermark sau khi đã đặt giấy phép | Giấy phép chưa được tải trước lần gọi API đầu tiên | Tải giấy phép **trước** bất kỳ thao tác Aspose.Drawing nào. |
| Tiêu thụ theo metered luôn bằng 0 | Khóa chưa được đặt hoặc biến môi trường sai | Xác minh khóa công khai/riêng và đảm bảo kết nối internet tới máy chủ metered của Aspose. |

## Câu hỏi thường gặp

**Q1: Tôi có thể sử dụng Aspose.Drawing mà không có giấy phép không?**  
A1: Có, giấy phép dùng thử hoạt động cho việc phát triển và đánh giá, nhưng nó sẽ thêm watermark và giới hạn một số tính năng.

**Q2: Tôi cần gia hạn giấy phép Aspose.Drawing bao lâu một lần?**  
A2: Giấy phép là vĩnh viễn cho phiên bản đã mua. Việc gia hạn chỉ cần thiết cho hỗ trợ và nâng cấp.

**Q3: Giấy phép metered là gì, và khi nào nên sử dụng?**  
A3: Giấy phép metered tính phí dựa trên mức sử dụng (số thao tác hoặc dữ liệu đã xử lý). Nó phù hợp cho dịch vụ đám mây hoặc mô hình trả‑theo‑sử dụng.

**Q4: Tôi có thể sử dụng Aspose.Drawing trong các dự án thương mại không?**  
A4: Chắc chắn—khi bạn có giấy phép hợp lệ, bạn có thể nhúng Aspose.Drawing vào bất kỳ ứng dụng thương mại nào.

**Q5: Tôi có thể tìm hỗ trợ cộng đồng cho Aspose.Drawing ở đâu?**  
A5: Truy cập [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) để nhận trợ giúp cộng đồng, ví dụ và thảo luận.

## Kết luận

Việc thành thạo cách **đặt giấy phép Aspose.Drawing**—dù từ tệp, luồng, hay qua mô hình metered—giúp bạn khai thác tối đa thư viện đồ họa .NET mạnh mẽ này. Thực hiện các bước trên, chú ý các cạm bẫy thường gặp, và bạn sẽ sẵn sàng xây dựng các giải pháp xử lý ảnh mạnh mẽ mà không gặp rào cản về giấy phép.

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}