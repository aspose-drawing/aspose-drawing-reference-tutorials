---
date: 2026-10-13
description: 了解如何使用 Aspose.Drawing API 批次裁剪圖像為 PNG，這是 .NET 開發人員的跨平台替代方案，取代 System.Drawing。
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: 圖像裁剪教學 – Aspose.Drawing
og_description: 了解如何使用 Aspose.Drawing 快速批次裁剪圖像為 PNG，這是 .NET 開發人員的跨平台替代方案，取代 System.Drawing。遵循一步一步的說明，能有效處理多個檔案。
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: 使用 Aspose.Drawing for .NET 批次裁剪圖像為 PNG 的方法
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
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
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: 使用 Aspose.Drawing for .NET 批次裁剪圖像為 PNG 的方法
url: /zh-hant/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Drawing for .NET 批次裁剪圖像為 PNG

如果您需要在 .NET 環境中快速、可靠且大規模地 **裁剪圖像為 PNG**，此處正是您要找的地方。在本教學中，我們將逐步說明如何載入圖像、定義裁剪區域，並將結果儲存為 PNG 檔案——全部使用 Aspose.Drawing，這是一個現代的 **System.Drawing 替代方案**，支援跨平台。您也會看到如何將單一圖像的流程擴展為完整的 **批次裁剪** 管線。

## 快速解答
- **應該使用哪個函式庫？** Aspose.Drawing for .NET（完整功能的 System.Drawing.Common 替代方案）  
- **基本裁剪需要多長時間？** 通常在現代 CPU 上單張圖像不到一秒  
- **可以裁剪為 PNG 嗎？** 可以——將裁剪後的位圖儲存為 PNG 檔（見第 6 步）  
- **需要授權嗎？** 免費試用可用於開發；正式環境需購買商業授權  
- **可以批次處理嗎？** 完全可以——將相同步驟包在迴圈中，即可在數秒內處理多個檔案  

## 如何批次裁剪圖像為 PNG？

使用 `new Bitmap(path)` 載入每個來源檔案，為裁剪區域建立相同尺寸的空白 `Bitmap`，使用 `Graphics.DrawImage` 繪製選取的矩形，最後呼叫 `Save("output.png", ImageFormat.Png)`。將這六行程式碼放入遍歷目錄的 `foreach` 迴圈，即可得到完整的批次裁剪解決方案，能在數秒內處理數十張圖像。

## 為什麼在批次裁剪時使用 Aspose.Drawing？

Aspose.Drawing 可在 **Windows、Linux 與 macOS** 上執行，在一般伺服器等級 CPU 上能於 0.5 秒內處理 **500 像素以上的圖像**，且支援 **超過 50 種圖像格式**，完整保留 Alpha 通道。由於它不依賴本機 GDI+，您可以將相同程式碼部署至容器、Azure App Service 或 AWS Lambda，無需額外函式庫，非常適合大規模圖像流水線。

## 什麼是「裁剪圖像為 PNG」？

`crop image to PNG` 操作會從來源位圖中擷取矩形區域，並將該區域寫入 PNG 檔案。PNG 會保留任何 Alpha 通道，提供無損壓縮，使得產出的圖像非常適合縮圖、圖示、使用者介面資源，或任何需要高品質與透明度的情境。

## 為什麼 Aspose.Drawing 是 System.Drawing 的替代方案？

Aspose.Drawing 可作為 System.Drawing 的即插即用替代方案，提供完整的跨平台相容性，免除本機 GDI+ 函式庫的需求。它支援多種像素格式，提供高效能的圖像處理，且包含 Alpha 通道處理與廣泛格式支援等進階功能，適用於簡單編輯與大規模批次處理。

## 前置條件

在開始之前，請確保您已具備以下條件：

- 已在 .NET 專案中整合 **Aspose.Drawing 函式庫**。您可從 [Aspose.Drawing 下載頁面](https://releases.aspose.com/drawing/net/) 取得。  
- 包含欲裁剪來源圖像的資料夾。請將程式碼片段中的 `"Your Document Directory"` 替換為您機器上的實際路徑。

## 匯入命名空間

`System.Drawing` 命名空間讓我們可以使用 `Bitmap`、`Graphics` 以及 Aspose.Drawing 所擴充的相關型別。

```csharp
using System.Drawing;
```

## 步驟說明

### 步驟 1：建立 Bitmap 畫布

`Bitmap` 是 Aspose.Drawing 在記憶體中的圖像表示，提供像素層級的存取與格式控制。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

我們先建立一個空白畫布，其尺寸足以容納裁剪後的結果。請依您要擷取的區域調整寬度與高度。

### 步驟 2：建立 Graphics 物件

`Graphics` 是繪圖表面，可讓您在 Bitmap 上繪製形狀、文字或其他圖像。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` 物件讓我們能在畫布上繪圖。`InterpolationMode` 控制在縮放或變換時像素值的計算方式——`NearestNeighbor` 在銳利邊緣時表現良好。

### 步驟 3：載入要裁剪的圖像

`Image`（或 `Bitmap`）會將來源檔案載入記憶體，準備進行操作。

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

載入來源圖像。請確保路徑指向已存在的檔案，否則會拋出例外。

### 步驟 4：定義來源與目標矩形

`Rectangle` 物件描述要保留的來源圖像區域以及它在目標畫布上的放置位置。

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` 告訴 API 要保留原始圖像的哪一部分。此處選取左上角 50 × 40 像素的區域。將相同的矩形指派給 `destinationRectangle`，即可保持裁剪區域的原始大小。

### 步驟 5：執行裁剪操作

`Graphics.DrawImage` 會將 `image` 中定義的部分複製到我們的空白 `bitmap`。

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

這就是核心的 **裁剪圖像為 PNG** 操作。此方法會遵循來源矩形，只將選取的像素寫入目標位圖。

### 步驟 6：儲存裁剪後的圖像（裁剪圖像為 PNG）

`Bitmap.Save` 會使用指定的格式將記憶體中的位圖寫入檔案。

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

最後，將畫布寫入磁碟為 PNG 檔。PNG 會保留 Alpha 通道並提供無損品質——非常適合 UI 資源。

## 如何在迴圈中批次裁剪圖像？

使用 `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` 迭代每個檔案路徑，在迴圈內重複第 1‑6 步，並將每個結果儲存至目標資料夾。此模式具線性擴展性，可透過 `Parallel.ForEach` 平行化以獲得更快的吞吐量，能有效且快速地處理圖像。

## 常見陷阱與技巧

- **像素格式不匹配** – 確保來源圖像與畫布位圖使用相容的像素格式，以免顏色偏移。  
- **GDI 物件的釋放** – 將 `Bitmap` 與 `Graphics` 包在 `using` 陳述式中或手動呼叫 `Dispose()`；否則可能會洩漏非受控資源。  
- **座標錯誤** – 矩形座標採零基礎。若選取的矩形超出來源圖像範圍，將拋出例外。  

## 常見問題

**Q: 我可以使用 Aspose.Drawing 裁剪任何格式的圖像嗎？**  
A: 可以，Aspose.Drawing 支援多種格式（PNG、JPEG、BMP、GIF、TIFF 等），因此幾乎可以裁剪任何圖像類型。

**Q: 有進階的裁剪選項嗎？**  
A: 當然可以。您可以結合 `GraphicsPath`、`Matrix` 變換，或使用 `ImageProcessor` 類別，實現如圓形裁剪等更複雜的選取。

**Q: 我可以對同一張圖像執行多次裁剪嗎？**  
A: 可以。第一次裁剪後，您可以將產生的位圖作為新來源，重複此流程以串接多次裁剪。

**Q: Aspose.Drawing 適合批次圖像處理嗎？**  
A: 確實如此。其輕量級 API 以及不依賴本機函式庫的特性，使其非常適合在伺服器上處理大量圖像集合。

**Q: 如何取得 Aspose.Drawing 相關問題的支援？**  
A: 前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 尋求協助並與社群交流。

---

**最後更新：** 2026-10-13  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [載入、將 BMP 轉換為 PNG 及其他格式 (使用 Aspose.Drawing)](/drawing/net/image-editing/load-save/)
- [如何為 .NET 授權 Aspose.Drawing – 授權 aspose.drawing 方法](/drawing/net/licensing/)
- [如何繪製矩形 – 座標系統轉換（頁面轉換）使用 Aspose.Drawing API for .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}