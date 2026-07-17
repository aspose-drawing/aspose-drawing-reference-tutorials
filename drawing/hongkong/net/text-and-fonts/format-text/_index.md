---
date: 2026-07-17
description: 了解如何透過在 Aspose.Drawing for .NET 中設定文字對齊來防止文字溢出，並將文字加入影像。一步一步的範例指南。
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: 使用 Aspose.Drawing for .NET 設定文字對齊
og_description: 透過在 Aspose.Drawing for .NET 中設定文字對齊防止文字溢出。了解如何在影像上繪製字串、在矩形內置中對齊文字，並取代
  System.Drawing。
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: 防止文字溢出 – 使用 Aspose.Drawing for .NET 設定文字對齊
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: 防止文字溢出 – 使用 Aspose.Drawing for .NET 設定文字對齊
url: /zh-hant/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 防止文字溢位 – 使用 Aspose.Drawing 設定文字對齊

## 介紹

當您在 .NET 中渲染圖形時需要 **防止文字溢位**，Aspose.Drawing 為您提供對文字位置、對齊與換行的精細控制。無論是建立徽章產生器、動態報表或任何基於影像的輸出，掌握文字對齊即可確保文字保持在預定的矩形內且外觀精緻。本指南將逐步說明如何建立 bitmap 畫布、設定 `StringFormat`、繪製帶有置中文字的矩形、處理溢位，最後儲存影像。

## 快速解答
- **「設定文字對齊」是什麼意思？** 它定義文字在繪圖矩形內的水平與垂直位置。  
- **哪個類別控制對齊？** `StringFormat` 讓您設定 `Alignment` 與 `LineAlignment`。  
- **我可以同時繪製字串與矩形嗎？** 可以 — 使用 `Graphics.DrawRectangle` 後接 `Graphics.DrawString`。  
- **如何防止文字溢位？** 調整矩形大小或手動將文字分割成多行。  
- **正式環境需要授權嗎？** 非評估使用需購買商業版 Aspose.Drawing 授權。

## 什麼是 Aspose.Drawing 中的 **設定文字對齊**？

`set text alignment` 會設定文字在 `Rectangle` 或繪圖區域內的水平 (`StringAlignment`) 與垂直 (`LineAlignment`) 位置。透過調整這些屬性，您可以控制文字是左對齊、置中、右對齊，或是上對齊、置中、下對齊，從而在使用 Aspose.Drawing 產生的圖形、徽章與報表中實現精確的版面配置。

## 為什麼使用 Aspose.Drawing 進行文字對齊？

Aspose.Drawing 消除 `System.Drawing.Common` 所受的 GDI+ 限制。它支援 **5 大 .NET 執行環境** – .NET Framework 4.6+、.NET Core 2.0+、.NET 5、.NET 6 與 .NET 7 – 並能在不耗盡記憶體的情況下渲染最高 **4000 × 4000 px**（約 100 MB）的影像。抗鋸齒、高 DPI 縮放以及完整的 Linux 容器相容性，使您能在任何部署情境下產生像素完美的圖形。

## 前置條件

1. **Aspose.Drawing Library** – 前往 [here](https://releases.aspose.com/drawing/net/) 下載。  
2. **Development Environment** – Visual Studio 2022（或任何 C# IDE）。  
3. **Basic .NET knowledge** – 您應該熟悉 C# 專案與 NuGet 套件。

## 匯入命名空間

首先，將所需的命名空間引入作用域。這些命名空間提供圖形、文字渲染與繪圖基元的存取。

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 如何使用 Aspose.Drawing 防止文字溢位？

Bitmap 為代表記憶體中影像的類別，而 `RectangleF` 定義用於繪圖的浮點矩形區域。透過將 `StringFormat` 的 `Trimming` 設為 `StringTrimming.EllipsisCharacter`，多餘的字元會自動以省略號取代，確保文字不會超出矩形邊界。先測量字串可讓您決定是縮小矩形還是將文字分割成多行，從而保證版面整潔不會溢出。

載入 bitmap，定義適當大小的 `RectangleF`，並使用 `Trimming` 設為 `StringTrimming.EllipsisCharacter` 的 `StringFormat` 以自動截斷多餘字元。若需完整控制，可使用 `Graphics.MeasureString` 測量字串，然後在繪製前縮小矩形或將文字分行。此做法可保證不會有字元溢出視覺範圍。

## 步驟 1：建立 Bitmap 與 Graphics 物件  

Bitmap 代表記憶體中的影像，而 Graphics 提供對該 bitmap 的繪圖方法。建立 bitmap 即提供可供繪製的畫布。`Graphics` 物件是繪圖表面，我們透過 `TextRenderingHint` 啟用高品質文字渲染。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## 步驟 2：定義 **StringFormat** 與樣式  

StringFormat 指定文字版面選項，例如對齊、行距與修剪。此處透過設定 `StringFormat` 實例來 **設定文字對齊**。我們同時準備筆刷、畫筆與字型，以便在繪製字串時使用。

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## 步驟 3：建立與格式化文字 – **如何繪製字串** 與 **繪製帶文字的矩形**  

Graphics.DrawString 將文字繪製到畫布上，Graphics.DrawRectangle 則繪製矩形形狀。我們組合文字，定義容納文字的矩形，接著同時繪製矩形邊框與字串本身。

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### 如何處理文字溢位

如果提供的 `text` 超出矩形邊界，您有兩個常見的選項：

1. **調整矩形大小** – 增加 `rectangle.Width` 或 `rectangle.Height`。  
2. **分割文字** – 將字串切成適合的行，然後以調整過的 Y 座標分別呼叫 `DrawString`。

## 如何使用 Aspose.Drawing 在影像上繪製字串？

Graphics.DrawString 會使用字型與格式化選項繪製指定的文字。從 bitmap 建立 `Graphics` 物件，然後以已準備好的 `StringFormat` 呼叫 `DrawString`。此單一呼叫即可在您指定的位置精確繪製文字，並遵守對齊、修剪以及任何已套用的變換矩陣。加入高品質的渲染提示可確保在高 DPI 顯示器上輸出保持清晰。

## 如何在矩形內置中文字？

StringAlignment 決定文字在版面矩形內的水平對齊方式。將 `stringFormat.Alignment = StringAlignment.Center` 與 `stringFormat.LineAlignment = StringAlignment.Center` 設定為置中。如此即可在矩形內水平與垂直置中文字，適用於徽章、按鈕或標籤覆蓋。置中效果在不同影像尺寸與 DPI 設定下皆保持一致，提供平衡的視覺外觀。

## 如何實現垂直文字對齊？

LineAlignment 控制文字在矩形內的垂直位置。使用 `stringFormat.LineAlignment` 並設定為 `StringAlignment.Near`、`Center` 或 `Far`，即可將文字分別置於矩形的上方、中央或下方。若需在旋轉文字同時保留垂直對齊，可結合 `Graphics.TranslateTransform`。調整行對齊可確保多行文字區塊即使在變換後也能精確對齊至預期位置。

## 步驟 4：儲存輸出 – **將文字加入影像**

最後，將 bitmap 寫入磁碟。此步驟示範如何在單一次呼叫中 **將文字加入影像**。

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## 常見問題與解決方案

| Issue | Solution |
|-------|----------|
| **文字顯示模糊** | 確保已設定 `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`。 |
| **文字被裁切** | 增大矩形尺寸或透過測量字串大小 (`Graphics.MeasureString`) 啟用自動換行邏輯。 |
| **找不到字型** | 確認該字型已安裝於主機，或使用 `PrivateFontCollection` 嵌入私有字型。 |
| **顏色異常** | 再次檢查筆刷與畫筆的顏色；請注意 `Color.FromKnownColor` 會使用系統定義的顏色。 |

## 常見問答

**Q1：Aspose.Drawing 是否相容所有 .NET 版本？**  
A1：是的，Aspose.Drawing 設計上相容多種 .NET 版本，確保開發者具備彈性。

**Q2：我可以進一步自訂字型樣式嗎？**  
A2：當然可以！調整 `Font` 物件的參數即可取得想要的字型大小、樣式與字族。

**Q3：如何在定義的矩形內處理文字溢位？**  
A3：您可以透過調整矩形大小或實作自訂邏輯來處理過長文字，以管理文字溢位。

**Q4：Aspose.Drawing 還有其他格式化選項嗎？**  
A4：是的，Aspose.Drawing 提供完整的圖形操作工具，包含文字、形狀等多種格式化選項。

**Q5：在哪裡可以取得 Aspose.Drawing 的其他支援？**  
A5：可前往 Aspose.Drawing 論壇 [here](https://forum.aspose.com/c/drawing/44) 取得社群支援與討論。

**其他問答**

**Q：如何在不使用矩形的情況下繪製字串？**  
A：省略 `DrawRectangle` 呼叫，直接將目標 `PointF` 位置傳給 `Graphics.DrawString`。

**Q：我可以在保持對齊的同時旋轉文字嗎？**  
A：可以 — 在繪製前對 `Graphics` 物件套用 `Matrix` 變換，繪製完畢後再重設。

**Q：是否可以將影像匯出為 JPEG 而非 PNG？**  
A：只要在 `bitmap.Save` 中更改檔案副檔名，並視需要指定 `ImageFormat.Jpeg` 即可。

---

**最後更新：** 2026-07-17  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [如何使用 Aspose.Drawing for .NET 繪製文字](/drawing/net/text-and-fonts/draw-text/)
- [在 Aspose.Drawing 中於影像加入文字](/drawing/net/use-cases/text-on-image/)
- [如何使用 Aspose.Drawing for .NET 繪製文字與字型](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}