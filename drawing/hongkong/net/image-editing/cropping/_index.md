---
date: 2026-05-19
description: 一步一步的教學，說明如何使用 Aspose.Drawing（.NET 開發者的 System.Drawing 替代方案）批量裁切圖像為 PNG。
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: 圖像裁切教學 – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing for .NET 批量裁切圖像為 PNG
url: /zh-hant/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing for .NET 批量裁剪圖像為 PNG

如果您需要在 .NET 環境中快速、可靠且大規模地 **裁剪圖像為 PNG**，您來對地方了。在本教學中，我們將逐步說明如何載入圖像、定義裁剪區域，並將結果儲存為 PNG 檔案——全部使用 Aspose.Drawing，這是一個現代的 **System.Drawing 替代方案**，支援跨平台。您還會看到如何將單圖像流程擴展為完整的 **批次裁剪** 流程。

## 快速解答
- **應該使用哪個函式庫？** Aspose.Drawing for .NET（System.Drawing.Common 的完整功能替代方案）  
- **基本裁剪需要多長時間？** 在現代 CPU 上，單張圖像通常在一秒以下完成  
- **可以裁剪為 PNG 嗎？** 是 — 將裁剪後的 bitmap 儲存為 PNG 檔案（見第 6 步）  
- **需要授權嗎？** 免費試用可用於開發；商業授權則需於正式環境使用  
- **是否支援批次處理？** 當然可以 — 將相同步驟包在迴圈中即可處理多個檔案  

## 如何批量裁剪圖像為 PNG？

使用 `new Bitmap(path)` 載入每個來源檔案，為裁剪區域建立相對應的空白 `Bitmap`，使用 `Graphics.DrawImage` 繪製選取的矩形，最後呼叫 `Save("output.png", ImageFormat.Png)`。將這六行程式碼包在遍歷目錄的 `foreach` 迴圈中，即可得到完整的批次裁剪解決方案，能在數秒內處理數十張圖像。

## 為什麼在批次裁剪時使用 Aspose.Drawing？

Aspose.Drawing 支援 **三大作業系統**（Windows、Linux、macOS），且在一般伺服器等級的 CPU 上能在 **0.5 秒以下** 處理 **500 像素以上** 的圖像。其 API 免除原生 GDI+ 相依性，意味著您可以將相同程式碼部署至容器、Azure App Service 或 AWS Lambda，而無需額外的函式庫。此函式庫亦提供 **超過 50 種影像格式** 與 **完整的 Alpha 通道保留**，非常適合大規模的透明 PNG 裁剪。

## 什麼是「裁剪圖像為 PNG」？

`crop image to PNG` 操作會從來源 bitmap 中擷取矩形區域，並將該區域寫入 PNG 檔案。PNG 會保留 Alpha 通道，提供無損壓縮，使得產生的圖像非常適合用於縮圖、圖示、UI 資產，或任何需要高品質與透明度的情境。

## 為什麼 Aspose.Drawing 是 System.Drawing 的替代方案？

Aspose.Drawing 作為 System.Drawing 的即插即用替代方案，提供完整的跨平台相容性，免除原生 GDI+ 函式庫的需求。它支援多種像素格式，提供高效能的影像處理，並包含 Alpha 通道處理與廣泛格式支援等進階功能，適用於簡單編輯與大規模批次處理。

## 前置條件

在開始之前，請確保您已具備：

- 已在 .NET 專案中整合 **Aspose.Drawing 函式庫**。您可以在 [此處](https://releases.aspose.com/drawing/net/) 下載。  
- 包含欲裁剪來源圖像的資料夾。請將程式碼片段中的 `"Your Document Directory"` 替換為您機器上的實際路徑。

## 匯入命名空間

`System.Drawing` 命名空間讓我們可以存取 `Bitmap`、`Graphics` 以及 Aspose.Drawing 所擴充的相關型別。

```csharp
using System.Drawing;
```

## 步驟說明

### 步驟 1：建立 Bitmap 畫布

`Bitmap` 是 Aspose.Drawing 在記憶體中的圖像表示，提供像素層級的存取與格式控制。  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

我們從一個空白畫布開始，其尺寸足以容納裁剪後的結果。請調整寬度與高度以符合您計畫擷取的區域尺寸。

### 步驟 2：建立 Graphics 物件

`Graphics` 是繪圖表面，可讓您在 Bitmap 上繪製形狀、文字或其他圖像。  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` 物件讓我們可以在畫布上繪圖。`InterpolationMode` 控制在縮放或變換過程中像素值的計算方式 — `NearestNeighbor` 在銳利邊緣時表現良好。

### 步驟 3：載入要裁剪的圖像

`Image`（或 `Bitmap`）將來源檔案載入記憶體，準備進行操作。  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

載入來源圖像。請確保路徑指向現有檔案；否則會拋出例外。

### 步驟 4：定義來源與目標矩形

`Rectangle` 物件描述要保留的來源圖像區域以及它在目標畫布上的放置位置。  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` 告訴 API 要保留原始圖像的哪一部分。此處我們選取左上角 50 × 40 像素的區域。將相同的矩形指派給 `destinationRectangle`，即可保持裁剪區域的原始尺寸。

### 步驟 5：執行裁剪操作

`Graphics.DrawImage` 將 `image` 的指定部分複製到我們的空白 `bitmap` 上。  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` 將 `image` 的指定部分複製到我們的空白 `bitmap`。這就是核心的 **crop image to PNG** 操作。

### 步驟 6：儲存裁剪後的圖像（裁剪圖像為 PNG）

`Bitmap.Save` 使用指定的格式將記憶體中的 bitmap 寫入檔案。  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

最後，將畫布寫入磁碟為 PNG 檔案。PNG 會保留任何 Alpha 通道，且提供無損品質——非常適合 UI 資產。

## 如何在迴圈中批量裁剪圖像？

使用 `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` 逐一遍歷每個檔案路徑，在迴圈內重複第 1‑6 步，並將每個結果存入目標資料夾。此模式具線性擴展性，可透過 `Parallel.ForEach` 平行化以獲得更快的吞吐量，能高效且快速地處理圖像。

## 常見陷阱與技巧

- **像素格式不匹配** – 確保來源圖像與畫布 bitmap 使用相容的像素格式，以避免顏色偏移。  
- **GDI 物件的釋放** – 將 `Bitmap` 與 `Graphics` 包在 `using` 陳述式中或手動呼叫 `Dispose()`；否則可能會洩漏未受管理的資源。  
- **座標錯誤** – 矩形座標是從零開始。選取超出來源圖像範圍的矩形會拋出例外。  

## 常見問與答

**Q: 我可以使用 Aspose.Drawing 裁剪任何格式的圖像嗎？**  
A: 可以，Aspose.Drawing 支援多種格式（PNG、JPEG、BMP、GIF、TIFF 等），因此您幾乎可以裁剪任何圖像類型。

**Q: 有提供進階的裁剪選項嗎？**  
A: 當然。您可以結合 `GraphicsPath`、`Matrix` 變換，或使用 `ImageProcessor` 類別來實現更複雜的選取，例如圓形裁剪。

**Q: 我可以對單一圖像執行多次裁剪嗎？**  
A: 可以。第一次裁剪後，您可以將產生的 bitmap 作為新的來源，重複此過程以串接多次裁剪。

**Q: Aspose.Drawing 適合用於批次影像處理嗎？**  
A: 確實如此。其輕量級 API 以及不依賴原生函式庫的特性，使其非常適合在伺服器上處理大量影像集合。

**Q: 我該如何取得 Aspose.Drawing 相關問題的支援？**  
A: 請前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 尋求協助並與社群交流。

---

**最後更新：** 2026-05-19  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [如何使用 Aspose.Drawing for .NET 裁剪圖像為 PNG](/drawing/net/image-editing/cropping/)
- [如何使用 Aspose.Drawing for .NET 縮放圖像](/drawing/net/image-editing/scale/)
- [使用 Aspose.Drawing 將 BMP 轉換為 PNG 及其他格式](/drawing/net/image-editing/load-save/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}