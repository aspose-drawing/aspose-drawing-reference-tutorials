---
date: 2025-11-30
description: Tìm hiểu cách áp dụng chuyển đổi hệ tọa độ, vẽ bitmap hình chữ nhật và
  chuyển đổi các trang bằng Aspose.Drawing cho .NET.
language: vi
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Biến đổi Hệ tọa độ (Biến đổi Trang) trong Aspose.Drawing cho .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Biến Đổi Hệ Tọa Độ (Biến Đổi Trang) trong Aspose.Drawing cho .NET

## Giới thiệu

Chào mừng! Trong hướng dẫn này bạn sẽ khám phá **cách thực hiện biến đổi hệ tọa độ** trên một trang bằng Aspose.Drawing cho .NET. Dù bạn cần **vẽ hình chữ nhật bitmap**, thay đổi tỷ lệ bản vẽ, hay chỉ đơn giản là ánh xạ đơn vị trang sang đơn vị thiết bị, các bước dưới đây sẽ hướng dẫn bạn toàn bộ quy trình—rõ ràng, ngắn gọn và sẵn sàng sao chép‑dán vào dự án của bạn.

## Câu trả lời nhanh
- **Lớp chính để vẽ là gì?** `Graphics` từ Aspose.Drawing.
- **Làm sao để đặt đơn vị trang?** Sử dụng `graphics.PageUnit = GraphicsUnit.Inch;`.
- **Tôi có thể vẽ một hình chữ nhật trên trang đã biến đổi không?** Có—tạo một `Pen` và gọi `DrawRectangle`.
- **Kết quả được lưu ở đâu?** Vào thư mục bạn chỉ định trong `bitmap.Save`.
- **Có cần giấy phép cho môi trường sản xuất không?** Cần một giấy phép Aspose.Drawing hợp lệ cho việc sử dụng thương mại.

## Biến đổi hệ tọa độ là gì?

Một **biến đổi hệ tọa độ** thay đổi cách các tọa độ trang logic (như inch hoặc milimet) được ánh xạ tới các tọa độ thiết bị thực (pixel). Bằng cách điều chỉnh biến đổi, bạn kiểm soát việc phóng to, quay và dịch chuyển của tất cả các thao tác vẽ, giúp dễ dàng thiết kế đồ họa không phụ thuộc vào độ phân giải.

## Tại sao nên dùng Aspose.Drawing cho biến đổi trang?

- **Tương thích đầy đủ với .NET** – hoạt động với .NET Framework, .NET Core và .NET 5/6.
- **API đồ họa phong phú** – cung cấp cùng chức năng như System.Drawing.Common mà không bị giới hạn nền tảng.
- **Xử lý đơn vị đơn giản** – chuyển đổi giữa inch, milimet, point, v.v. chỉ bằng một thuộc tính.
- **Kết quả chất lượng cao** – tạo PNG, JPEG, BMP và các định dạng khác với kiểm soát chính xác.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

- **Thư viện Aspose.Drawing** – tải phiên bản mới nhất từ trang chính thức [ở đây](https://releases.aspose.com/drawing/net/).
- **Môi trường phát triển** – Visual Studio (bất kỳ phiên bản nào) hoặc IDE .NET khác.
- **Quyền ghi** – một thư mục trên máy của bạn nơi ảnh đã biến đổi sẽ được lưu (thay `"Your Document Directory"` trong mã bằng đường dẫn thực tế).

Bây giờ chúng ta đã sẵn sàng, hãy đi qua từng bước.

## Nhập không gian tên

Đầu tiên, đưa không gian tên cần thiết vào phạm vi:

```csharp
using System.Drawing;
```

> *Tại sao điều này quan trọng*: `System.Drawing` chứa các cấu trúc `Bitmap`, `Graphics`, `Pen` và màu sắc mà chúng ta sẽ sử dụng xuyên suốt hướng dẫn.

## Bước 1: Tạo một Bitmap

Tạo một canvas trống sẽ chứa bản vẽ đã biến đổi. Chúng ta chỉ định kích thước **1000 × 800 pixel** và định dạng pixel hỗ trợ độ trong suốt alpha.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> Bitmap này đóng vai trò là bề mặt vẽ. Định dạng pixel được chọn (`Format32bppPArgb`) đảm bảo việc render chất lượng cao với alpha đã được tiền nhân.

## Bước 2: Tạo đối tượng Graphics

Đối tượng `Graphics` cung cấp các phương thức vẽ (đường, hình, văn bản). Chúng ta lấy nó từ bitmap vừa tạo.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> Đối tượng `Graphics` là trung tâm của mọi thao tác render; nó sẽ tuân theo các cài đặt biến đổi mà chúng ta sẽ áp dụng tiếp theo.

## Bước 3: Xóa sạch Canvas

Trước khi vẽ bất kỳ thứ gì, xóa canvas về màu nền trung tính (xám trong ví dụ này). Bước này cũng minh họa cách lấp đầy toàn bộ bitmap bằng một màu đồng nhất.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Bước 4: Đặt biến đổi (Áp dụng biến đổi trang)

Ở đây chúng ta **áp dụng biến đổi trang** bằng cách đặt `PageUnit` thành inch. Điều này nói với engine đồ họa rằng tất cả các tọa độ tiếp theo sẽ được hiểu là inch thay vì pixel.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *Mẹo*: Thay đổi `PageUnit` là cách đơn giản để **biến đổi tọa độ trang** mà không cần tính toán giá trị pixel thủ công.

## Bước 5: Vẽ một hình chữ nhật (Draw rectangle bitmap)

Bây giờ chúng ta vẽ một hình chữ nhật có kích thước **1 inch × 1 inch** tại vị trí (1, 1) inch. Độ rộng `Pen` được đặt là `0.1f` inch, tạo ra một đường mỏng nhưng dễ nhìn.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> Điều này minh họa **draw rectangle bitmap** sau khi đã áp dụng biến đổi—lưu ý rằng kích thước hình chữ nhật được định nghĩa bằng inch, không phải pixel.

## Bước 6: Lưu ảnh

Cuối cùng, lưu bitmap đã biến đổi ra đĩa. Thay `"Your Document Directory"` bằng đường dẫn thư mục thực tế trên máy của bạn.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> Tệp đầu ra (`PageTransformation_out.png`) sẽ chứa hình chữ nhật được vẽ bằng biến đổi hệ tọa độ mà chúng ta đã thiết lập trước đó.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|-----------|
| **Hình ảnh xuất hiện trống** | Canvas chưa được xóa hoặc vẽ ngoài vùng hiển thị. | Kiểm tra `graphics.PageUnit` và giá trị tọa độ; đảm bảo hình chữ nhật nằm trong giới hạn bitmap. |
| **Tỷ lệ không đúng** | Sử dụng `GraphicsUnit` sai. | Đảm bảo `graphics.PageUnit` khớp với đơn vị bạn muốn (ví dụ `GraphicsUnit.Inch`). |
| **Lỗi đường dẫn tệp** | Thư mục không tồn tại hoặc ký tự không hợp lệ. | Tạo thư mục đích trước hoặc dùng `Path.Combine` để xây dựng đường dẫn một cách an toàn. |

## Câu hỏi thường gặp

**H: Tôi có thể dùng Aspose.Drawing miễn phí không?**  
Đ: Aspose.Drawing cung cấp bản dùng thử miễn phí mà bạn có thể truy cập [tại đây](https://releases.aspose.com/).

**H: Tôi có thể tìm tài liệu chi tiết cho Aspose.Drawing ở đâu?**  
Đ: Tài liệu có sẵn [tại đây](https://reference.aspose.com/drawing/net/).

**H: Làm sao tôi có thể nhận hỗ trợ cho Aspose.Drawing?**  
Đ: Để được hỗ trợ, hãy truy cập [Diễn đàn Aspose.Drawing](https://forum.aspose.com/c/diagram/17).

**H: Có giấy phép tạm thời cho Aspose.Drawing không?**  
Đ: Có, bạn có thể lấy giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

**H: Tôi có thể mua Aspose.Drawing ở đâu?**  
Đ: Bạn có thể mua Aspose.Drawing [tại đây](https://purchase.aspose.com/buy).

## Kết luận

Bạn đã học cách **áp dụng biến đổi hệ tọa độ**, **vẽ rectangle bitmap**, và **lưu kết quả** bằng Aspose.Drawing cho .NET. Những khối xây dựng này cho phép bạn tạo đồ họa không phụ thuộc vào độ phân giải, hoàn hảo cho báo cáo, thành phần UI, hoặc bất kỳ trường hợp nào mà kích thước chính xác là quan trọng. Hãy thử nghiệm với các giá trị `GraphicsUnit` khác (như `Millimeter` hoặc `Point`) để xem chúng ảnh hưởng như thế nào tới bản vẽ của bạn.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2025-11-30  
**Đã kiểm tra với:** Aspose.Drawing 24.11 cho .NET  
**Tác giả:** Aspose