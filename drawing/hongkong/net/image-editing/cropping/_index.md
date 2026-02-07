---
date: 2026-02-07
description: 逐步教學：使用 Aspose.Drawing（.NET 開發者的 System.Drawing 替代方案）將圖像裁剪為 PNG，並包含批量裁剪及必備技巧。
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing for .NET 將圖片裁剪為 PNG
url: /zh-hant/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing for .NET 裁剪圖像為 PNG

如果您需要在 .NET 環境中快速且可靠地 **crop image to PNG**，您來對地方了。在本教學中，我們將一步步說明如何載入圖像、定義裁剪區域，並將結果儲存為 PNG 檔案——全部使用 Aspose.Drawing，這是一個現代的 **alternative to System.Drawing**，支援跨平台運作。

## Quick Answers
- **What library should I use?** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **How long does the basic crop take?** Usually under a second for a single image on a modern CPU  
- **Can I crop to PNG?** Yes – save the cropped bitmap as a PNG file (see Step 6)  
- **Do I need a license?** A free trial works for development; a commercial license is required for production  
- **Is batch processing possible?** Absolutely – wrap the same steps in a loop to process multiple files  

## 什麼是「crop image to PNG」？

裁剪圖像是指從原始位圖中擷取一個矩形區域。將該區域儲存為 PNG 時，可保留透明度並提供無損壓縮——非常適合縮圖、圖示或任何 UI 資產。

## 為什麼 Aspose.Drawing 是 System.Drawing 的替代方案？

- **跨平台支援** – 可在 Windows、Linux 與 macOS 上執行，無需原生 GDI+ 相依。  
- **豐富的像素格式處理** – 支援 32 位元、24 位元、索引色等多種格式。  
- **效能導向的 API** – 適合單張圖像編輯與大規模批次作業。

## 前置條件

在開始之前，請確保您已：

- **Aspose.Drawing 套件** 已整合至您的 .NET 專案。您可以在此處下載 [here](https://releases.aspose.com/drawing/net/)。  
- 有一個資料夾存放要裁剪的來源圖像。請將程式碼片段中的 `"Your Document Directory"` 替換為您機器上的實際路徑。

## 匯入命名空間

```csharp
using System.Drawing;
```

`System.Drawing` 命名空間讓我們可以使用 `Bitmap`、`Graphics` 以及 Aspose.Drawing 所擴充的相關型別。

## Step‑by‑Step Guide

### Step 1: 建立 Bitmap 畫布

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

我們先建立一個空白畫布，尺寸足以容納裁剪後的結果。請依照您要擷取的區域大小調整寬度與高度。

### Step 2: 建立 Graphics 物件

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` 物件讓我們可以在畫布上繪圖。`InterpolationMode` 控制在縮放或變形時像素值的計算方式——`NearestNeighbor` 在銳利邊緣時表現良好。

### Step 3: 載入要裁剪的圖像

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

載入來源圖像。請確保路徑指向已存在的檔案，否則會拋出例外。

### Step 4: 定義來源與目標矩形

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` 告訴 API 要保留原圖的哪一部分。此處我們選取左上角 50 × 40 像素的區域。將相同的矩形指定給 `destinationRectangle`，即可保持裁剪區域的原始大小。

### Step 5: 執行裁剪操作

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` 會將 `image` 中定義的部分複製到我們的空白 `bitmap` 上。這就是核心的 **crop image to PNG** 操作。

### Step 6: 儲存裁剪後的圖像（Crop Image to PNG）

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

最後，將畫布寫入磁碟並以 PNG 格式儲存。PNG 會保留任何 alpha 通道，且提供無損品質——非常適合 UI 資產。

## 如何在批次情境下裁剪圖像

當您需要處理數十或數百張圖片時，只要將整段程式碼放入 `foreach` 迴圈，遍歷檔案路徑集合即可。相同的 `Graphics.DrawImage` 邏輯適用於 **batch image cropping**，讓此教學的延伸變得簡單。

## 常見問題與技巧

- **像素格式不匹配** – 請確保來源圖像與畫布 bitmap 使用相容的像素格式，以免出現顏色偏移。  
- **釋放 GDI 物件** – 請將 `Bitmap` 與 `Graphics` 包在 `using` 陳述式中，或手動呼叫 `Dispose()`；否則可能會洩漏非受控資源。  
- **座標錯誤** – 矩形座標採零基礎。若選取的矩形超出來源圖像範圍，將拋出例外。

## Frequently Asked Questions

**Q: Can I crop images of any format using Aspose.Drawing?**  
A: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP, GIF, TIFF, etc.), so you can crop virtually any image type.

**Q: Are there advanced cropping options available?**  
A: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations, or use the `ImageProcessor` class for more complex selections like circular crops.

**Q: Can I apply multiple crop operations to a single image?**  
A: Yes. After the first crop, you can reuse the resulting bitmap as the new source and repeat the process to chain multiple crops.

**Q: Is Aspose.Drawing suitable for batch image processing?**  
A: Indeed. Its lightweight API and lack of native dependencies make it perfect for processing large image collections on servers.

**Q: How can I get support for Aspose.Drawing‑related queries?**  
A: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) to seek assistance and connect with the community.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}