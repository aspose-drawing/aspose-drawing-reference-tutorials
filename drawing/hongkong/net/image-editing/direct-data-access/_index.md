---
date: 2026-07-22
description: 了解如何使用 Aspose.Drawing 的直接資料存取高效讀取像素，以在 .NET 中實現高效能影像處理。
keywords:
- how to read pixels
- high performance image processing
- bulk image watermarking
lastmod: 2026-07-22
linktitle: 如何在 Aspose.Drawing 中使用直接資料存取讀取像素
og_description: 如何使用 Aspose.Drawing 的直接資料存取快速讀取像素。本指南展示了適用於 .NET 開發人員的高效能影像處理技術。
og_image_alt: 'Developer guide: Direct pixel access with Aspose.Drawing in .NET'
og_title: 如何讀取像素 – 使用 Aspose.Drawing 的高效能影像處理
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to read pixels efficiently using Aspose.Drawing's direct
    data access for high performance image processing in .NET.
  headline: How to Read Pixels with Direct Data Access in Aspose.Drawing
  type: TechArticle
- description: Learn how to read pixels efficiently using Aspose.Drawing's direct
    data access for high performance image processing in .NET.
  name: How to Read Pixels with Direct Data Access in Aspose.Drawing
  steps:
  - name: Load the Source Image
    text: We start by loading the image you want to analyze. Replace the placeholder
      path with the actual location of your image file.
  - name: Create a Target Bitmap
    text: Create a new bitmap that matches the source dimensions and uses a 32‑bit
      pixel format suitable for direct access.
  - name: Read Pixel Data
    text: Read the entire ARGB32 pixel buffer from the source bitmap into an integer
      array. This is the **how to read pixels** step.
  - name: Write Pixel Data
    text: After any optional manipulation (e.g., applying a filter), write the pixel
      array back to the target bitmap. This demonstrates **how to write pixels** efficiently.
  - name: Save the Result
    text: Persist the modified bitmap to disk. Adjust the output path as needed.
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing works with .NET Framework, .NET Core, and .NET 5/6+.
    question: Can I use Aspose.Drawing for .NET with other .NET frameworks?
  - answer: Absolutely—download a trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official support.
    question: How can I get support for Aspose.Drawing?
  - answer: The full API reference is available at the [Aspose.Drawing documentation
      site](https://reference.aspose.com/drawing/net/).
    question: Where can I find the documentation for Aspose.Drawing?
  - answer: You can buy a license directly from the Aspose store [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Direct Data Access for Image Pixel Manipulation
tags:
- image processing
- Aspose.Drawing
- pixel manipulation
- .NET image editing
title: 如何在 Aspose.Drawing 中使用直接資料存取讀取像素
url: /zh-hant/net/image-editing/direct-data-access/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Drawing 直接資料存取讀取像素

## 介紹

在本教學中，您將學會 **如何讀取像素**，以及使用 Aspose.Drawing 的 **直接資料存取** 功能將像素資料寫回。利用 **高效能影像處理** 的直接資料存取，您可以對像素緩衝區進行低階控制，使影像操作快速且節省記憶體——非常適合自訂濾鏡、影像分析或在 .NET 應用程式中進行大量像素轉換。

## 快速解答
- **主要的讀取像素方法是什麼？** 使用 `ReadArgb32Pixels` 於 `Bitmap` 實例上。  
- **哪種像素格式最適合直接存取？** `PixelFormat.Format32bppPArgb` 提供具預乘 Alpha 的 32 位元 ARGB 值。  
- **使用 Aspose.Drawing 是否需要授權？** 提供免費試用版；正式環境需購買授權。  
- **此程式碼能在 .NET 6+ 上執行嗎？** 能，Aspose.Drawing 支援 .NET 5、.NET 6 以及更新版本。  
- **此操作是否為執行緒安全？** 在不同的 bitmap 實例上讀寫是安全的；避免在未同步的情況下共享同一 bitmap。

`ReadArgb32Pixels` 會將 bitmap 的整個 ARGB32 像素緩衝區讀取到整數陣列中。  
`PixelFormat.Format32bppPArgb` 是具預乘 Alpha 的 32 位元像素格式。  
`Bitmap` 代表由像素資料定義的影像。

## Aspose.Drawing 中的直接資料存取是什麼？

直接資料存取讓您一次性取得或取代 bitmap 的整個像素緩衝區，省去逐像素 getter/setter 方法的開銷。此方式會讀取一個 ARGB32 整數陣列（`0xAARRGGBB`），您可以使用任何 .NET 邏輯對其進行操作，然後再一次寫回修改後的陣列。

## 為什麼在高效能影像處理中使用直接資料存取？

將整張影像載入受管理的整數陣列，使用向量化或平行程式碼處理成千上萬的像素，最後只需兩個 API 呼叫寫回結果。這可將互操作轉換減少高達 90 %，且在處理 10,000 × 10,000 像素的影像時不需額外的暫存緩衝區，真正實現高效能影像處理。

## 常見使用案例

- 建立自訂影像濾鏡（棕褐色、邊緣偵測、**套用棕褐色濾鏡**）  
- 為電腦視覺任務執行像素層級的統計分析  
- 轉換影像色彩空間或執行大量色彩校正  
- 產生縮圖或 **大量影像加浮水印** 以處理海量影像批次  

## 前置條件

- **Aspose.Drawing Library：** 從官方網站下載並參考最新的 Aspose.Drawing for .NET。  
- **開發環境：** 任意 .NET IDE（Visual Studio、Rider、VS Code），並安裝 Aspose.Drawing NuGet 套件。  

您可以在此處下載程式庫 [here](https://releases.aspose.com/drawing/net/)。

## 匯入命名空間

首先，將所需的命名空間匯入作用域，以便使用 bitmap 類別。

```csharp
using System.Drawing;
```

## 步驟指南

### 步驟 1：載入來源影像  

我們先載入您想要分析的影像。將佔位路徑替換為實際的影像檔案位置。

```csharp
Bitmap sourceBitmap = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

### 步驟 2：建立目標 Bitmap  

建立一個與來源尺寸相同、且使用適合直接存取的 32 位元像素格式的新 bitmap。

```csharp
Bitmap targetBitmap = new Bitmap(sourceBitmap.Width, sourceBitmap.Height, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步驟 3：讀取像素資料  

將來源 bitmap 的整個 ARGB32 像素緩衝區讀取到整數陣列中。這就是 **如何讀取像素** 的步驟。

```csharp
int[] pixels = new int[sourceBitmap.Width * sourceBitmap.Height];
sourceBitmap.ReadArgb32Pixels(pixels);
```

### 步驟 4：寫入像素資料  

在完成任何可選的操作（例如套用濾鏡）後，將像素陣列寫回目標 bitmap。此步驟示範 **如何高效寫入像素**。

```csharp
targetBitmap.WriteArgb32Pixels(pixels);
```

### 步驟 5：儲存結果  

將修改後的 bitmap 持久化至磁碟。視需要調整輸出路徑。

```csharp
targetBitmap.Save("Your Document Directory" + @"Images\DirectDataAccess_out.png");
```

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **`ArgumentException` 在 `ReadArgb32Pixels` 上** | 確認來源 bitmap 使用 32 位元像素格式；若不是，先使用 `sourceBitmap.Clone(..., PixelFormat.Format32bppPArgb)` 轉換。 |
| **寫入後顏色不正確** | 確認未意外修改 Alpha 通道；若不需要透明度，請保留 `0xFF`（不透明）值。 |
| **處理非常大影像時效能延遲** | 將像素陣列分塊處理，或使用 `Parallel.For` 以利用多核心。`Parallel.For` 會在多個執行緒間平行執行迴圈。 |

## 常見問答

**Q: 可以在 .NET 以外的其他 .NET 框架中使用 Aspose.Drawing 嗎？**  
A: 可以，Aspose.Drawing 支援 .NET Framework、.NET Core，以及 .NET 5/6+。

**Q: Aspose.Drawing 有提供免費試用版嗎？**  
A: 當然有——可在此下載試用版 [here](https://releases.aspose.com/)。

**Q: 如何取得 Aspose.Drawing 的支援？**  
A: 前往 [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) 取得社群協助與官方支援。

**Q: 哪裡可以找到 Aspose.Drawing 的文件？**  
A: 完整的 API 參考位於 [Aspose.Drawing documentation site](https://reference.aspose.com/drawing/net/)。

**Q: 如何購買 Aspose.Drawing 的授權？**  
A: 您可直接在 Aspose 商店購買授權 [here](https://purchase.aspose.com/buy)。

**Q: 可以在多執行緒環境中操作像素資料嗎？**  
A: 可以，只要每個執行緒使用各自的 bitmap 實例，或對共享資源進行同步。

## 結論

您現在已學會 **如何從 bitmap 讀取像素**、操作 ARGB32 陣列，並使用 Aspose.Drawing 的直接資料存取 **寫回像素資料**。此方法為在 .NET 應用程式中實作自訂濾鏡、像素層級分析與大量轉換提供 **高效能影像處理** 的能力。

---

**最後更新：** 2026-07-22  
**測試環境：** Aspose.Drawing latest for .NET  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [如何在不失真的情況下縮放影像 – 使用 Aspose.Drawing 進行影像編輯](/drawing/net/image-editing/)
- [如何使用 Aspose.Drawing 為 .NET 縮放影像](/drawing/net/image-editing/scale/)
- [如何使用 Aspose.Drawing 為 .NET 裁切影像為 PNG](/drawing/net/image-editing/cropping/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}