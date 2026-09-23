---
date: 2026-09-23
description: 了解如何在 C# 中使用 Aspose.Drawing 儲存 PNG 圖像、列出已安裝字型、以自訂字型繪製文字，並調整點陣圖解析度以獲得高品質圖形。
keywords:
- save png image c#
- installed fonts aspnet
- aspose.drawing bitmap graphics
- c# font collection
- png export .net
lastmod: 2026-09-23
linktitle: 在 C# 中使用 Aspose.Drawing 及已安裝字型儲存 PNG 圖像
og_description: 在 C# 中使用 Aspose.Drawing 儲存 PNG 圖像。本指南說明如何列出已安裝字型、繪製文字，以及控制點陣圖解析度以製作專業圖形。
og_image_alt: Developer guide showing C# code that creates a bitmap, lists system
  fonts, and saves a PNG file with Aspose.Drawing
og_title: 在 C# 中使用 Aspose.Drawing 及已安裝字型儲存 PNG 圖像
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  headline: Save PNG image in C# with Aspose.Drawing and installed fonts
  type: TechArticle
- description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  name: Save PNG image in C# with Aspose.Drawing and installed fonts
  steps:
  - name: Create a bitmap (the canvas)
    text: '`Bitmap` is the raster image object that holds pixel data for the canvas.'
  - name: Create graphics from bitmap
    text: '`Graphics` is the object that supplies drawing functions such as drawing
      shapes and text onto a bitmap.'
  - name: Set up brush and font (draw text with fonts)
    text: '`Brush` defines how shapes and text are filled with colour, while `Font`
      specifies the typeface, size, and style for text rendering.'
  - name: List installed fonts and show font families
    text: '`InstalledFontCollection` provides access to all font families installed
      on the host system.'
  - name: Save PNG image
    text: '`bitmap.Save` writes the bitmap to a file in the chosen image format, such
      as PNG. > **Pro tip:** Use `Path.Combine` for building file paths to avoid issues
      with directory separators on different operating systems.'
  type: HowTo
- questions:
  - answer: Yes. Load the font file into a `PrivateFontCollection` and create a `Font`
      from that collection, then draw it the same way as system fonts.
    question: Can I use custom fonts that are not installed on the machine?
  - answer: Wrap font creation in a `try/catch` block and inspect `ArgumentException`
      for missing families; provide a fallback font such as `Arial`.
    question: How do I handle font‑related exceptions?
  - answer: Absolutely. The library works in ASP.NET Core, Azure Functions, and other
      server‑side .NET environments without needing GDI+.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify
      the `FontStyle` enum to apply bold, italic, or underline.
    question: Can I change the text colour or style?
  - answer: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – bitmap graphics and font handling
tags:
- save png
- aspose.drawing
- c# graphics
- installed fonts
- bitmap
title: 在 C# 中使用 Aspose.Drawing 及已安裝字型儲存 PNG 圖像
url: /zh-hant/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中使用 Aspose.Drawing 與已安裝字型儲存 PNG 圖像

## 簡介

如果您需要在 C# 中 **儲存 PNG 圖像** 同時 **建立點陣圖圖形**，Aspose.Drawing for .NET 為您提供一個簡潔、跨平台的解決方案。本教學將逐步說明列出已安裝字型、顯示字型族、從點陣圖建立圖形，以及使用字型繪製文字——最終將結果儲存為 PNG 圖像。完成後，您將擁有一段可重複使用的程式碼片段，可直接嵌入任何 .NET 專案，無論是運行於 Windows、Linux 或 macOS。

## 快速回答
- **此教學會產生什麼？** 列出主機上已安裝字型族的 PNG 圖像。  
- **需要哪個函式庫？** Aspose.Drawing for .NET（不需要 System.Drawing.Common 相依性）。  
- **我可以使用自訂字型嗎？** 可以——將字型載入 `InstalledFontCollection` 或 `PrivateFontCollection`。  
- **輸出解析度可以調整嗎？** 當然可以——變更點陣圖尺寸或像素格式即可控制解析度。  
- **執行程式碼需要授權嗎？** 評估時可使用臨時授權；正式環境則需完整授權。

## 在 Aspose.Drawing 中「儲存 PNG 圖像」是什麼意思？

`Bitmap` 是 Aspose.Drawing 的點陣圖影像容器，用於儲存像素資料。  
儲存 PNG 圖像即是將您的繪圖表面——`Bitmap`——輸出為副檔名為 `.png` 的檔案。Aspose.Drawing 會執行無損 PNG 壓縮，且可處理高達 **10 000 × 10 000 像素** 的影像而不會耗盡記憶體，非常適合高解析度圖形。產生的檔案可用於網頁、報表或後續的影像處理流程。

## 為何要列出已安裝字型並顯示字型族？

列出已安裝的字型可讓應用程式依據最終使用者的環境自動調整，確保產生的圖形符合企業品牌或使用者偏好，且不必額外隨程式一起攜帶字型檔案。`InstalledFontCollection` 會列舉作業系統中已安裝的字型。此功能在自動化報表產生、證書製作，或任何必須遵循系統排版的視覺內容中特別有用。

## 如何在 C# 中使用 Aspose.Drawing 建立點陣圖圖形？

`Bitmap` 代表影像畫布；`Graphics` 為該畫布提供繪圖方法；`Font` 描述文字渲染所使用的字型。只需幾行程式碼即可產生完整的 PNG：建立 `Bitmap`、取得 `Graphics` 物件、使用已安裝集合中的 `Font` 繪製文字，最後呼叫 `bitmap.Save`。以下逐步指南將說明每個部分並提供實用技巧。

## 先決條件

- **Aspose.Drawing 函式庫** – 從 [Aspose Drawing 下載頁面](https://releases.aspose.com/drawing/net/) 下載最新版本。  
- **IDE** – Visual Studio、Rider 或任何相容 .NET 的編輯器。  
- **基本 C# 知識** – 您應該熟悉類別、物件與簡單迴圈。  
- **.NET 執行環境** – 建議使用 .NET 6+ 或 .NET Core 3.1+ 以獲得完整跨平台支援。

## 匯入命名空間

在 C# 檔案的頂部加入以下 `using` 陳述式，讓編譯器能找到圖形與字型相關類型：

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Text;
using System.IO;
```

## 逐步指南

### 步驟 1：建立點陣圖（畫布）

`Bitmap` 是用於保存畫布像素資料的點陣圖物件。  

```csharp
using System.Drawing;
using System.Drawing.Text;
```

### 步驟 2：從點陣圖建立 Graphics 物件

`Graphics` 提供在點陣圖上繪製形狀與文字等功能的物件。  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步驟 3：設定筆刷與字型（使用字型繪製文字）

`Brush` 定義形狀與文字的填色方式，而 `Font` 指定文字渲染的字型、大小與樣式。  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### 步驟 4：列出已安裝字型並顯示字型族

`InstalledFontCollection` 可存取主機系統上所有已安裝的字型族。  

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### 步驟 5：儲存 PNG 圖像

`bitmap.Save` 將點陣圖寫入指定的影像格式檔案，例如 PNG。  

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

> **專業提示：** 使用 `Path.Combine` 組合檔案路徑，可避免不同作業系統的目錄分隔符問題。

## 常見問題與解決方案
| Issue | Cause | Fix |
|-------|-------|-----|
| **未顯示字型** | `InstalledFontCollection` 未被填充（例如在無字型的無頭伺服器上執行）。 | 在伺服器上安裝所需字型，或在應用程式中嵌入自訂字型。 |
| **儲存的檔案損毀** | 像素格式不正確或缺少寫入權限。 | 確保目標資料夾存在且應用程式具有寫入權限；保留 `PixelFormat.Format32bppPArgb`。 |
| **文字模糊** | DPI 設定過低或點陣圖尺寸過小。 | 增大點陣圖尺寸或設定 `graphics.SmoothingMode = SmoothingMode.AntiAlias`。 |

## 常見問答

**Q: 我可以使用未安裝在機器上的自訂字型嗎？**  
A: 可以。將字型檔載入 `PrivateFontCollection`，再從該集合建立 `Font`，並以與系統字型相同的方式繪製。

**Q: 如何處理與字型相關的例外情況？**  
A: 將字型建立包在 `try/catch` 區塊中，檢查 `ArgumentException` 以判斷缺少的字型族；提供備用字型，例如 `Arial`。

**Q: Aspose.Drawing 適合用於 Web 應用程式嗎？**  
A: 完全適合。此函式庫可在 ASP.NET Core、Azure Functions 以及其他伺服器端 .NET 環境中使用，且不需要 GDI+。

**Q: 我可以變更文字顏色或樣式嗎？**  
A: 可以。使用不同的 `Brush` 類型（例如 `LinearGradientBrush`），並修改 `FontStyle` 列舉以套用粗體、斜體或底線。

**Q: 我可以從哪裡取得測試用的臨時授權？**  
A: 從 [Aspose 臨時授權頁面](https://purchase.aspose.com/temporary-license/) 下載試用授權。

## 結論

透過上述步驟，您已學會如何使用 Aspose.Drawing for .NET 在 C# 中 **儲存 PNG 圖像**，並且能動態 **列出已安裝的字型**、**顯示字型族**、**從點陣圖建立圖形**，以及 **使用字型繪製文字**。現在您知道如何 **在 C# 中建立點陣圖圖形**、調整點陣圖解析度，並在需要時加入自訂字型。請嘗試不同的顏色、字型大小與點陣圖尺寸，以符合專案的視覺需求，並探索 Aspose.Drawing 的其他功能，如形狀繪製與影像處理，以打造更豐富的圖形。

---

**最後更新：** 2026-09-23  
**測試版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

## 相關教學

- [如何使用 Aspose.Drawing for .NET 繪製文字](/drawing/net/text-and-fonts/draw-text/)
- [使用抗鋸齒提升影像品質於 Aspose.Drawing](/drawing/net/rendering/antialiasing/)
- [如何使用 Aspose.Drawing 儲存 PNG – 世界座標變換](/drawing/net/coordinate-transformations/world-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}