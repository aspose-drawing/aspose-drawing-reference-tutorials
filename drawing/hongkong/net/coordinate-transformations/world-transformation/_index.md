---
date: 2026-06-23
description: 了解如何使用 Aspose.Drawing 儲存 PNG、套用世界變換，並將圖形轉換為 PNG。內容包括 C# 的平移變換範例以及多種圖形變換。
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: Aspose.Drawing 中的世界變換
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing 儲存 PNG – 世界變換
url: /zh-hant/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing 儲存 PNG – 世界變換

## 將 Bitmap 儲存為 PNG – 介紹

**如何使用 Aspose.Drawing 儲存 PNG** 是在需要即時產生高品質、透明影像時的常見需求。在本教學中，您將學會 **將 bitmap 儲存為 PNG**、套用平移、旋轉與縮放等世界變換，最後將圖形轉換為 PNG——全部使用乾淨且易於維護的 C# 程式碼。無論您是在建構報表引擎、圖表元件，或是自訂 UI 渲染器，掌握這些步驟即可產生在任何裝置上都表現優秀的動態影像。

## 快速解答
- **什麼是「世界變換」？** 它將您的繪圖邏輯（世界）座標映射到頁面（裝置）座標。  
- **我可以將結果匯出為 PNG 嗎？** 可以 – 繪圖完成後，只需呼叫 `bitmap.Save(...)` 並使用 `.png` 副檔名。  
- **我需要 Aspose.Drawing 的授權嗎？** 免費試用可用於開發；商業授權則需於正式環境使用。  
- **這與 .NET 6/7 相容嗎？** 完全相容 – Aspose.Drawing 支援 .NET Framework 4.5+ 以及 .NET Core/5/6/7。  
- **我可以串接多少個變換？** 您可以依序套用 **多個圖形變換**（平移、旋轉、縮放等）。

## 什麼是 Aspose.Drawing 中的世界變換？

世界變換會改變繪圖指令使用的座標系統。預設情況下，(0,0) 位於 bitmap 的左上角。透過 `TranslateTransform`、`RotateTransform` 或 `ScaleTransform`，您可以重新定位原點、旋轉形狀或調整大小，而不必改變原始幾何形狀。

## 如何使用 Aspose.Drawing 儲存 PNG？

載入 `Bitmap` 物件，在其 `Graphics` 實例上設定所需的世界變換，繪製形狀，最後呼叫 `bitmap.Save("output.png", ImageFormat.Png)`。這行儲存指令會寫入無損的 PNG 檔案，保留透明度與色彩忠實度，非常適合作為網頁資產與 UI 疊加層。

## 為什麼使用圖形平移範例？

圖形平移範例讓您一次性移動繪圖原點，而不必為每個點重新計算。此做法可減少程式碼複雜度、提升可讀性，並讓圖形引擎有效處理矩陣運算，於大型畫布上可提升最高 30 % 的渲染效能。

## 圖形平移範例

**圖形平移範例** 示範了移動原點如何簡化定位。您只需一次性平移座標系統，即可如同新原點位於畫布中心般繪圖，無需逐點重新計算。

## 先決條件

在開始之前，請確保您已具備：

- **Aspose.Drawing 程式庫** 已整合至您的 .NET 專案 – 從官方 [Aspose.Drawing 釋出頁面](https://releases.aspose.com/drawing/net/) 下載。  
- 一個 **文件目錄** 用於儲存輸出圖像。  
- 具備 **C#** 語法的基本認識，以及 Visual Studio 或您偏好的 IDE。  

現在，讓我們深入程式碼吧！

## 匯入命名空間

`Bitmap`、`Graphics` 以及 Aspose 繪圖工具位於以下命名空間。  
**定義：** `System.Drawing` 提供核心 GDI+ 類型，而 `Aspose.Drawing` 則以跨平台功能擴充它們。

## 逐步指南

### 步驟 1：建立 Bitmap

我們先建立一個空白畫布，用來容納繪圖。

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` 會建立一個每像素 32 位元、具預乘 Alpha 的 bitmap，這是 PNG 輸出的最佳格式，因為它能在不需額外轉換的情況下保留透明度。

- **為什麼使用 32bppPArgb？** 此像素格式支援 Alpha 透明度與高品質色彩渲染，完美適用於 PNG 輸出。  
- **專業提示：** 調整寬度/高度以符合目標影像尺寸。

### 步驟 2：設定世界變換（圖形平移範例）

`TranslateTransform` 會將座標系統的原點移動到新位置。  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` 將 (0,0) 點平移至畫布中心。此呼叫之後，任何使用 (0,0) 座標繪製的形狀都會出現在影像的正中央。

- 這會將 (0,0) 點移至 (500, 400) – 即 1000 × 800 畫布的中心。  
- 您可以串接其他變換：`RotateTransform` 會旋轉座標系統，`ScaleTransform` 會縮放座標系統，從而實現 **多個圖形變換**。

### 步驟 3：使用變換後的座標繪製矩形

`DrawRectangle` 會使用指定的筆與座標繪製矩形。

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` 會在畫布中心繪製矩形，因為其左上角相對於變換後的原點已偏移半寬與半高。

- 矩形的左上角起始於變換後的原點（影像中心）。  
- 您可以自由嘗試其他形狀——橢圓、直線或自訂路徑。

### 步驟 4：儲存結果 – 將圖形轉換為 PNG

`Save` 會將 bitmap 依指定的影像格式寫入檔案。  
`ImageFormat` 用於指定儲存影像的檔案格式，例如 PNG。

`bitmap.Save(outputPath, ImageFormat.Png)` 會寫入無損的 PNG 檔案，可直接在網頁或 UI 元件中使用。

- PNG 會保留先前設定的精確顏色與透明度。  
- 請將 `"Your Document Directory"` 替換為您機器上的實際路徑。

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方法 |
|-------|----------------|-----|
| **檔案未找到錯誤**（儲存時） | 目標資料夾不存在。 | 在呼叫 `Save` 前以程式方式建立資料夾（`Directory.CreateDirectory`）。 |
| **空白影像**（變換後） | `TranslateTransform` 在繪圖之後呼叫。 | 確保變換在任何繪圖指令之前 **設定**。 |
| **顏色失真** | 使用不相容的像素格式。 | PNG 輸出請使用 `Format32bppPArgb`。 |

## 常見問答

**Q: 我可以套用超過一個變換嗎？**  
A: 可以 – 您可以串接 `TranslateTransform`、`RotateTransform` 與 `ScaleTransform`，在單一圖形管線中實現複雜效果。

**Q: Aspose.Drawing 可免費用於商業專案嗎？**  
A: 提供免費試用供評估使用，但正式環境必須購買商業授權。

**Q: 這能在 .NET Core 與 .NET 5/6/7 上運作嗎？**  
A: 完全相容。Aspose.Drawing 支援所有現代 .NET 執行環境，包括 .NET Core、.NET 5、.NET 6 與 .NET 7。

**Q: 我可以在哪裡找到完整的 API 參考文件？**  
A: 完整文件可於 [此處](https://reference.aspose.com/drawing/net/) 取得。

**Q: 若找不到輸出檔案該如何排除故障？**  
A: 核對路徑字串、確認寫入權限，並在呼叫 `Save` 前確保目錄已存在。

## 結論

您現在已掌握 **如何使用 Aspose.Drawing 儲存 PNG**、套用 **世界變換**，以及執行 **圖形平移範例**，未來可再加入旋轉或縮放等變換。透過這些基礎建構塊，您能產生動態影像、建立自訂圖表，或為任何 .NET 應用程式即時產生圖形。

---

**最後更新：** 2026-06-23  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  
**相關資源：** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## 相關教學

- [矩陣變換教學：Aspose.Drawing 在 .NET 中的矩陣變換](/drawing/net/coordinate-transformations/matrix-transformations/)
- [如何使用 Aspose.Drawing 全域變換旋轉圖像](/drawing/net/coordinate-transformations/global-transformation/)
- [座標系統變換 – Aspose.Drawing 在 .NET 中的頁面變換](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}