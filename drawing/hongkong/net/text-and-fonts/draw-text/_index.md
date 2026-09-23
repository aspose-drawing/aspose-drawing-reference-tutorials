---
date: 2026-09-23
description: 了解如何使用 Aspose.Drawing for .NET 在圖像上繪製文字。生成帶文字的圖像、將文字添加到位圖，並使用自訂字型將位圖儲存為
  PNG。
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: 使用 Aspose.Drawing 繪製文字的方法
og_description: 了解如何使用 Aspose.Drawing for .NET 在圖像上繪製文字。本教學示範如何生成帶文字的圖像、將文字添加到位圖，並使用自訂字型將位圖儲存為
  PNG。
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: 使用 Aspose.Drawing for .NET 在圖像上繪製文字 – 快速指南
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: 使用 Aspose.Drawing for .NET 在圖像上繪製文字的方法
url: /zh-hant/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing for .NET 在圖像上繪製文字

## 簡介

在本步驟指南中，您將學習如何使用 Aspose.Drawing for .NET **在圖像上繪製文字**。無論您需要建立 *動態文字圖像*、在現有位圖上加入文字，或是使用自訂字型產生圖形，本教學都會逐步說明所有細節，讓您在幾分鐘內開始繪製文字。此函式庫支援超過 30 種 GDI+ 方法，能在 Windows、Linux 與 macOS 上執行，且 **無任何外部相依性**，是伺服器端圖像產生的可靠選擇。

## 快速答案

- **使用的函式庫是什麼？** Aspose.Drawing for .NET  
- **主要任務？** Draw text on an image (create image with text)  
- **關鍵方法？** `Graphics.DrawString` (draw string on image)  
- **輸出格式？** PNG (save bitmap as PNG)  
- **先決條件？** .NET development environment and Aspose.Drawing library  

## 什麼是使用 Aspose.Drawing 繪製文字？

使用 Aspose.Drawing 繪製文字即是利用該函式庫相容 GDI+ 的 API，將 Unicode 字串渲染到點陣畫布上。`Graphics.DrawString` 方法會將文字寫入位圖，讓您能控制字型、顏色、對齊方式與抗鋸齒。此方式可在不安裝 System.Drawing.Common 的情況下產生高品質圖像。

## 為什麼使用 Aspose.Drawing 為圖像加入文字？

Aspose.Drawing 提供可靠且跨平台的方式在圖像上渲染文字，無需原生 GDI+ 函式庫，即可在任何作業系統上提供一致的品質與效能。它支援進階抗鋸齒、Unicode 字元與自訂字型，且能無縫整合至 .NET 應用程式，讓它同時適用於伺服器端圖像產生與桌面工具。

- **跨平台可靠性** – 可在 Windows、Linux 與 macOS 上運作。  
- **進階渲染** – 抗鋸齒與次像素文字平滑，提供清晰的輸出。  
- **無外部相依性** – 函式庫已捆綁所有建立 *create image with text* 所需的元件。

## 先決條件

在開始之前，請確保您已擁有：

- **Aspose.Drawing for .NET** – 從 [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/) 下載。  
- **.NET IDE** 如 Visual Studio 或 VS Code。

## 匯入命名空間

首先匯入所需的命名空間：

這些命名空間提供核心 GDI+ 類型，例如 `Bitmap`、`Graphics` 與文字渲染工具。  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 步驟 1：建立 bitmap 與 graphics 物件

`Bitmap` 是 Aspose.Drawing 用於儲存像素資料的點陣圖容器，而 `Graphics` 提供繪圖方法以在其上繪製形狀與文字。

`Bitmap` 代表記憶體中的圖像，`Graphics` 則提供在該 bitmap 上繪製的功能。  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

在此我們建立一個 `Bitmap` 用於保存最終圖片，並建立一個 `Graphics` 物件以便在其上繪圖。抗鋸齒提示可確保文字平滑。

## 步驟 2：設定 brush、pen 與 font

`Brush` 定義填充顏色，`Pen` 用於描繪形狀的輪廓，`Font` 指定字型、大小與樣式以渲染文字。

`Brush` 為形狀填色，`Pen` 為形狀描邊，`Font` 定義文字的字型與大小。  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** 定義文字顏色。  
- **Pen** 稍後用於在文字周圍繪製矩形（可選）。  
- **Font** 指定字型、大小與樣式，以執行 *draw string on image* 操作。

## 步驟 3：定義文字與矩形

`Rectangle` 定義文字放置的邊界框，指定 X/Y 座標以及寬度/高度。

`Rectangle` 指定矩形區域的位置與尺寸，此處用於限制繪製的文字範圍。  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` 決定文字的放置位置。請依需求調整座標與尺寸以符合版面配置。

## 步驟 4：繪製矩形與文字

`Graphics.DrawString` 使用指定的字型與筆刷，將文字繪製在給定的矩形內。

`Graphics.DrawString` 使用提供的字型與筆刷，將文字字串繪製於指定的矩形內。  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

首先以藍色矩形勾勒出區域，接著呼叫 `DrawString` **將文字加入 bitmap**。這就是在圖像上 *drawing text* 的核心步驟。

## 步驟 5：儲存結果

圖像會儲存為 PNG 檔案，滿足 *save bitmap as PNG* 的需求。請將佔位路徑替換為實際想要存放檔案的資料夾。

`bitmap.Save` 會將圖像寫入指定格式的檔案，例如 PNG。  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## 常見使用情境

- **產生具個人化姓名的證書**。  
- **為網站相簿建立帶有浮水印的縮圖**。  
- **建構包含標籤或註解的動態圖表**。

## 故障排除與技巧

- **找不到字型？** 請確認該字型已安裝在主機上，或使用私有字型集合。  
- **文字被截斷？** 增大矩形尺寸或縮小字型大小。  
- **效能問題？** 如有可能，重複使用相同的 `Graphics` 物件進行多次繪製。  

## 常見問題

**Q: 如何將輸出格式改為 JPEG？**  
A: 在 `Save` 方法中將 `.png` 副檔名改為 `.jpg`，並可選擇指定 `ImageCodecInfo` 以設定 JPEG 品質。

**Q: 可以繪製多行文字嗎？**  
A: 可以，在字串中加入換行字元 (`\n`) 或使用帶有 `FormatFlags.LineLimit` 的 `StringFormat`。

**Q: 有沒有方法在繪製前測量文字大小？**  
A: 使用 `Graphics.MeasureString` 可取得渲染文字的精確尺寸。

**Q: Aspose.Drawing 是否支援 Unicode 字元？**  
A: 當然支援。提供包含所需字形的字型，函式庫即可正確渲染。

**Q: 測試時使用的 Aspose.Drawing 版本為何？**  
A: 範例已在 Aspose.Drawing 24.11 for .NET 上測試。

---

**最後更新：** 2026-09-23  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [建立 Bitmap 圖形 C# – 儲存 PNG 圖像並使用已安裝的字型於 Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [如何使用 Aspose.Drawing API for .NET 將 bitmap 儲存為 PNG](/drawing/net/image-editing/display/)
- [圖像上的文字](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}