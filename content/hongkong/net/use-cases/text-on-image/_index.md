---
title: 在 Aspose.Drawing 中的圖像上新增文本
linktitle: 在 Aspose.Drawing 中的圖像上新增文本
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 探索使用 Aspose.Drawing for .NET 將文字無縫整合到圖像中。按照我們的逐步指南輕鬆進行影像處理。現在下載！
type: docs
weight: 12
url: /zh-hant/net/use-cases/text-on-image/
---
## 介紹
在 .NET 開發的動態世界中，Aspose.Drawing 作為輕鬆操作影像的強大工具脫穎而出。無論是用於浮水印、註釋還是創建個人化圖形，向圖像添加文字都是常見要求。在本教程中，我們將探索如何利用 C# 利用 Aspose.Drawing 將文字無縫整合到圖像中。
## 先決條件
在深入學習本教學之前，請確保您已具備以下條件：
1.  Aspose.Drawing 函式庫：從下列位置下載並安裝 Aspose.Drawing 函式庫：[Aspose.Drawing for .NET 文檔](https://reference.aspose.com/drawing/net/).
2. 開發環境：擁有有效的 .NET 開發環境，包括 Visual Studio 或任何其他相容的 IDE。
現在，讓我們開始使用逐步指南。
## 導入命名空間
首先將必要的命名空間匯入到您的 C# 專案中：
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## 第 1 步：載入圖像
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
在這裡，我們從指定的檔案路徑載入圖像並初始化圖形物件以進行進一步處理。
## 第 2 步：設定文字屬性
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
定義文字屬性，例如顏色、字體和填滿。根據您的喜好調整這些參數。
## 第 3 步：測量文字大小
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
透過單獨測量每個單字來計算文字所需的大小。這可確保正確放置並避免文字重疊。
## 第四步：在圖像上繪製文本
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
現在，根據計算的尺寸將文字放置在圖像上，並使用指定的字體和顏色進行繪製。
## 第 5 步：儲存影像
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
將修改後的影像儲存到所需的目錄。
本逐步指南示範了使用 Aspose.Drawing for .NET 將文字新增至圖像的簡單流程。嘗試不同的字體、顏色和文字內容以達到所需的視覺效果。
## 結論
Aspose.Drawing 簡化了 .NET 中的映像操作任務，為開發人員提供了強大的工具包。向圖像添加文字只是其功能的範例之一，展示了該庫在處理圖形元素方面的多功能性。
## 經常問的問題
### Aspose.Drawing 與所有影像格式相容嗎？
Aspose.Drawing 支援多種圖片格式，包括 JPEG、PNG 和 GIF 等流行格式。請參閱[文件](https://reference.aspose.com/drawing/net/)以獲得完整清單。
### 我可以將 Aspose.Drawing 用於商業項目嗎？
是的，Aspose.Drawing 適用於個人和商業項目。有關許可詳細信息，請訪問[購買頁面](https://purchase.aspose.com/buy).
### 臨時許可證是否可用於測試目的？
是的，您可以透過造訪獲得臨時測試許可證[臨時執照](https://purchase.aspose.com/temporary-license/).
### 在哪裡可以找到 Aspose.Drawing 的社群支援？
參與社區並獲得支持[Aspose.Drawing 論壇](https://forum.aspose.com/c/diagram/17).
### 我該如何開始使用 Aspose.Drawing？
首先從下載庫[這裡](https://releases.aspose.com/drawing/net/)並探索全面的[文件](https://reference.aspose.com/drawing/net/).