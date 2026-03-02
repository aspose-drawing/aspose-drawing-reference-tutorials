---
date: 2026-03-02
description: 使用 Aspose.Drawing for .NET 提升文件插圖！一步一步學習如何加入說明框，打造更清晰且具資訊性的視覺效果。
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing for .NET 添加註解框
url: /zh-hant/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Drawing 中製作標註

## 簡介
如果你想了解 **如何在 Aspose.Drawing for .NET 中加入標註**，你來對地方了。在本教學中，我們將一步步說明完整流程——從載入圖片到繪製精美的標註——讓你的圖示更清晰、更具資訊性。

## 快速解答
- **需要什麼函式庫？** Aspose.Drawing for .NET（可從官方網站下載）。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **實作需要多久？** 基本標註通常在 10 分鐘內完成。  
- **可以自訂顏色與字型嗎？** 可以——所有設定皆透過標準 GDI+ 物件（Pen、Font、Brush）控制。

## 如何在 Aspose.Drawing 中加入標註
以下提供簡潔的逐步指南，說明 **如何在圖片上加入標註**。歡迎直接複製程式碼、調整位置，或依品牌需求自訂樣式。

## 先決條件
在開始之前，請確保你已具備：

- 基本的 C# 程式語言知識。  
- 已安裝 Aspose.Drawing 函式庫。你可以在此下載 [here](https://releases.aspose.com/drawing/net/)。  
- 一個想要加入標註的文件或圖片。

## 匯入命名空間
確保在專案中加入必要的命名空間：

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## 步驟 1：載入圖片
先載入要加入標註的圖片。將 `"Your Document Directory"` 與 `"gears.png"` 替換為實際的目錄與檔名。

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## 步驟 2：建立 Graphics 物件
從圖片建立 `Graphics` 物件，以便執行繪圖操作。

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## 步驟 3：定義標註位置
為每個標註定義起點與終點座標，並設定標註的數值與單位。

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

## 步驟 4：繪製標註
實作 `DrawCallOut` 方法，在圖片上繪製標註。

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## 步驟 5：儲存圖片
將加入標註的圖片儲存至指定目錄。

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## 繪製標註的原始程式碼
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

## 常見問題與技巧
- **座標設定錯誤** – 請確認起點與終點在圖片範圍內，否則標註可能被裁切。  
- **文字重疊** – 如標籤與其他圖形衝突，可調整 `spaceSize` 或字型大小。  
- **效能** – 處理極大圖片時，建議在使用完畢後釋放 `Pen`、`Font`、`Brush` 物件，以節省資源。

## 結論
恭喜！你現在已掌握 **如何在 Aspose.Drawing for .NET 中加入標註**。歡迎自行嘗試不同的位置、顏色與字型，打造符合視覺風格的圖示。

## 常見問答

### 我可以將 Aspose.Drawing 用於其他類型的插圖嗎？
可以，Aspose.Drawing 支援多種繪圖操作，適用於各類插圖。

### Aspose.Drawing 是否相容於不同的圖像格式？
當然！Aspose.Drawing 支援常見的圖像格式，如 PNG、JPEG、GIF 等。

### 在哪裡可以找到更多範例與文件說明？
請前往完整文件說明 [here](https://reference.aspose.com/drawing/net/)。

### 如果遇到問題，我該如何取得支援？
可前往 [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) 取得社群支援。

### 我可以在購買前先試用 Aspose.Drawing 嗎？
可以！立即前往 [here](https://releases.aspose.com/) 下載免費試用版。

**其他問答**

**Q: 可以變更標註線條樣式（虛線、點線）嗎？**  
A: 可以——在繪製線條前，只需設定 `Pen.DashStyle` 屬性即可。

**Q: 能否為標註標籤加入背景顏色？**  
A: 完全可以。先建立帶有目標顏色的 `SolidBrush`，在呼叫 `DrawString` 前先填滿文字背後的矩形。

**Q: 如何確保標註在高 DPI 顯示器上保持相同外觀？**  
A: 如範例所示，設定 `graphics.PageUnit = GraphicsUnit.Pixel`，並使用向量基礎的測量方式，以維持一致的縮放比例。

---

**最後更新：** 2026-03-02  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}