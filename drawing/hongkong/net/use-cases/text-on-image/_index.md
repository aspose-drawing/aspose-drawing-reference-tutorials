---
date: 2026-02-27
description: 學習如何使用 Aspose.Drawing for .NET 建立生日卡片圖像。本指南將示範如何在圖像上繪製字串、在圖片上覆蓋文字，以及快速為相片加入說明文字。
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing 建立生日卡圖片
url: /zh-hant/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing 建立生日卡片圖像

## 介紹
在充滿活力的 .NET 開發世界中，Aspose.Drawing 脫穎而出，成為一個強大的影像操作工具。無論您需要 **create birthday card image**、加入浮水印，或僅僅在圖片上覆蓋文字，本教學將逐步說明如何使用 C# **draw string on image**。完成本指南後，您將擁有一張可分享的個人化生日卡片。

## 快速解答
- **我應該使用哪個函式庫？** Aspose.Drawing for .NET  
- **我可以在相片上加入說明文字嗎？** Yes – use `Graphics.DrawString` with custom fonts.  
- **生產環境需要授權嗎？** Yes, a commercial license is needed.  
- **支援哪些 .NET 版本？** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **實作需要多長時間？** Typically under 10 minutes for a simple card.

## 什麼是生日卡片圖像？
生日卡片圖像是一種個人化的圖片，將背景相片與自訂文字（例如問候語、收件人姓名或慶祝訊息）結合。使用 Aspose.Drawing，您可以透過程式自動產生這些卡片，無需手動的圖形設計工具。

## 為什麼使用 Aspose.Drawing 在圖片上覆蓋文字？
- **跨平台支援：** Works on Windows, Linux, and macOS.  
- **豐富的繪圖 API：** Full control over fonts, colors, and layout.  
- **無外部相依性：** Replaces `System.Drawing.Common` with a fully managed library.  
- **高效能：** Optimized for bulk image processing.

## 前置條件
在深入教學之前，請確保您已具備以下條件：

1. Aspose.Drawing 函式庫：從 [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/) 下載並安裝 Aspose.Drawing 函式庫。  
2. 開發環境：具備可運作的 .NET 開發環境，例如 Visual Studio 或 Visual Studio Code，並已安裝 .NET 6 SDK 或更新版本。

現在，讓我們一步一步說明如何在影像上加入文字並儲存為生日卡片。

## 匯入命名空間
首先，在您的 C# 專案中匯入必要的命名空間：

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## 步驟 1：載入影像
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
在此，我們從指定的檔案路徑載入影像，並初始化 graphics 物件以供後續處理。

## 步驟 2：設定文字屬性
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
定義文字屬性，例如顏色、字型與間距。依照您的設計需求調整這些參數。

## 步驟 3：測量文字大小
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
透過逐字測量每個單詞來計算文字所需的大小。此方式可確保正確放置，避免文字重疊。

## 步驟 4：在影像上繪製文字
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
現在，根據先前計算的大小定位文字於影像上，並使用指定的字型與顏色繪製。

## 步驟 5：儲存影像
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
將修改後的影像儲存至您指定的目錄。產生的檔案即為可直接寄送的生日卡片圖像。

## 常見使用情境與技巧
- **在相片上加入說明文字：** Replace `text` with any caption you need, such as “Celebrating 30 Years!”.  
- **在 bitmap 上繪製文字：** The same approach works for `Bitmap` objects created from scratch.  
- **覆蓋多行文字：** Loop through an array of strings and adjust the `Rectangle` Y‑coordinate for each line.  
- **專業提示：** Use `Graphics.SmoothingMode = SmoothingMode.AntiAlias` for even smoother text rendering.

## 結論
Aspose.Drawing 簡化了 .NET 中的影像操作工作，為開發人員提供了強大的工具組。將文字加入影像——無論是 **create birthday card image**、**draw string on image**，或 **add caption to photo**——都是其在圖形元素處理上多功能性的其中一個範例。

## 常見問題
### Aspose.Drawing 是否相容所有影像格式？
Aspose.Drawing 支援多種影像格式，包括常見的 JPEG、PNG、GIF 等。請參考 [documentation](https://reference.aspose.com/drawing/net/) 取得完整清單。

### 我可以在商業專案中使用 Aspose.Drawing 嗎？
是的，Aspose.Drawing 適用於個人與商業專案。欲了解授權細節，請前往 [purchase page](https://purchase.aspose.com/buy)。

### 是否提供測試用的臨時授權？
是的，您可透過前往 [Temporary License](https://purchase.aspose.com/temporary-license/) 取得測試用的臨時授權。

### 我可以在哪裡取得 Aspose.Drawing 的社群支援？
可在 [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) 與社群互動並取得支援。

### 如何開始使用 Aspose.Drawing？
首先從 [here](https://releases.aspose.com/drawing/net/) 下載函式庫，並參考完整的 [documentation](https://reference.aspose.com/drawing/net/) 進行探索。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-02-27  
**測試版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose