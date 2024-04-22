---
title: 在 Aspose.Drawing 中進行標註
linktitle: 在 Aspose.Drawing 中進行標註
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 使用 Aspose.Drawing for .NET 增強您的文件插圖！逐步了解如何添加標註以獲得更清晰、資訊豐富的視覺效果。
type: docs
weight: 10
url: /zh-hant/net/use-cases/make-callout/
---
## 介紹
歡迎來到我們關於在 Aspose.Drawing for .NET 中進行標註的逐步指南！如果您希望透過標註來增強文件插圖，那麼您來對地方了。在本教程中，我們將使用 Aspose.Drawing 函式庫將流程分解為可管理的步驟。
## 先決條件
在深入學習本教程之前，請確保您符合以下先決條件：
- C# 程式語言的基礎知識。
-  Aspose.Drawing 庫已安裝。你可以下載它[這裡](https://releases.aspose.com/drawing/net/).
- 若要新增標註的文件或影像。
## 導入命名空間
確保您的專案中包含必要的命名空間：
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## 第 1 步：載入圖像
首先載入要新增標註的圖像。代替`"Your Document Directory"`和`"gears.png"`與您的實際目錄和圖像檔案名稱。
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    //你的程式碼在這裡
}
```
## 第2步：建立圖形對象
創建一個`Graphics`從影像中提取物件來執行繪圖操作。
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## 第 3 步：定義標註位置
定義每個標註的起點和終點以及標註值和單位。
```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```
## 第四步：繪製標註
實施`DrawCallOut`方法在影像上繪製標註。
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## 第 5 步：儲存影像
將帶有標註的圖像儲存到所需的目錄。
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## 繪製標註原始碼
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```
## 結論

恭喜！您已使用 Aspose.Drawing for .NET 成功地為圖片新增標註。請隨意嘗試不同的位置和值，以進一步自訂您的標註。

## 常見問題解答

### 我可以將 Aspose.Drawing 用於其他類型的插圖嗎？

是的，Aspose.Drawing 支援各種類型插圖的廣泛繪圖操作。

### Aspose.Drawing 是否相容於不同的影像格式？

絕對地！ Aspose.Drawing 支援流行的圖片格式，如 PNG、JPEG、GIF 等。

### 在哪裡可以找到更多範例和文件？

探索全面的文檔[這裡](https://reference.aspose.com/drawing/net/).

### 如果遇到問題，我該如何獲得支援？

參觀[Aspose.Drawing 論壇](https://forum.aspose.com/c/diagram/17)以獲得社區支持。

### 購買前我可以試用 Aspose.Drawing 嗎？

當然！開始免費試用[這裡](https://releases.aspose.com/).