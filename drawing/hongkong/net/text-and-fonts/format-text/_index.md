---
date: 2026-02-25
description: 學習如何在 Aspose.Drawing for .NET 中設定文字對齊方式，並將文字加入圖片。一步一步的教學，附有範例。
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 使用 Aspose.Drawing for .NET 設定文字對齊
url: /zh-hant/net/text-and-fonts/format-text/
weight: 11
---

 sure to preserve all markdown formatting.

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Drawing 中設定文字對齊

## 簡介

當在 .NET 應用程式中需要 **set text alignment** 與文字格式化時，Aspose.Drawing 是開發人員追求精準、效能與豐富 API 的首選函式庫。無論是建立報表引擎、動態徽章產生器，或任何圖形密集的解決方案，能夠控制文字在形狀內的對齊方式，都能讓輸出看起來更精緻、專業。本教學將完整說明從建立 bitmap 畫布、繪製帶文字的矩形、處理文字溢位，到最後儲存影像的全過程。

## 快速解答
- **What does “set text alignment” mean?** 它定義文字在繪圖矩形內的水平與垂直定位方式。  
- **Which class controls alignment?** `StringFormat` 讓您設定 `Alignment` 與 `LineAlignment`。  
- **Can I draw a string and a rectangle together?** 可以——先使用 `Graphics.DrawRectangle`，再呼叫 `Graphics.DrawString`。  
- **How do I prevent text overflow?** 調整矩形尺寸或手動將文字分割成多行。  
- **Do I need a license for production?** 商業用途需購買 Aspose.Drawing 授權。

## 什麼是 Aspose.Drawing 中的 **set text alignment**？

`set text alignment` 指的是在 `Rectangle` 或任何繪圖區域內，設定文字的水平 (`StringAlignment`) 與垂直 (`LineAlignment`) 位置。透過調整這些設定，您可以決定文字是左對齊、置中、右對齊，或是上對齊、置中、下對齊。

## 為什麼在文字對齊上使用 Aspose.Drawing？

- **完整 .NET 相容性** – 支援 .NET Framework、.NET Core 與 .NET 5/6+。  
- **像素完美渲染** – 內建抗鋸齒與高 DPI 支援。  
- **無 GDI+ 限制** – 與 `System.Drawing.Common` 不同，Aspose.Drawing 可在 Linux 容器中執行，無需本機相依性。  
- **豐富樣式** – 結合字型、筆刷、畫筆與自訂 `StringFormat` 物件，實現複雜版面配置。

## 前置條件

1. **Aspose.Drawing Library** – 前往[此處](https://releases.aspose.com/drawing/net/)下載。  
2. **開發環境** – Visual Studio 2022（或任何 C# IDE）。  
3. **基本 .NET 知識** – 需要熟悉 C# 專案與 NuGet 套件。

## 匯入命名空間

開始之前，先將必要的命名空間匯入，以取得圖形、文字渲染與繪圖基元的存取權。

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 步驟 1：建立 Bitmap 與 Graphics 物件  

建立 bitmap 為您提供可繪製的畫布。`Graphics` 物件則是繪圖表面，我們會使用 `TextRenderingHint` 來啟用高品質文字渲染。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## 步驟 2：定義 **StringFormat** 與樣式  

此處透過設定 `StringFormat` 實例來 **set text alignment**。同時也會準備筆刷、畫筆與字型，供繪製文字時使用。

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## 步驟 3：建立與格式化文字 – **how to draw string** 與 **draw rectangle with text**

我們組合文字內容，定義容納文字的矩形，然後同時繪製矩形邊框與文字本身。

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### 如何處理文字溢位

若提供的 `text` 超出矩形範圍，您有兩個常見的處理方式：

1. **調整矩形大小** – 增加 `rectangle.Width` 或 `rectangle.Height`。  
2. **分割文字** – 將字串切成符合寬度的多行，然後針對每一行呼叫 `DrawString`，並調整 Y 座標。

## 步驟 4：儲存輸出 – **add text to image**

最後，將 bitmap 寫入磁碟。本步驟示範如何在單一次呼叫中完成 **add text to image**。

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **文字顯示模糊** | 確保已設定 `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`。 |
| **文字被裁切** | 增大矩形尺寸或使用 `Graphics.MeasureString` 來實作自動換行邏輯。 |
| **找不到字型** | 確認目標機器已安裝該字型，或使用 `PrivateFontCollection` 內嵌私有字型。 |
| **顏色不如預期** | 再次檢查筆刷與畫筆的顏色設定；`Color.FromKnownColor` 會使用系統預設顏色。 |

## 常見問答

### Q1：Aspose.Drawing 是否相容於所有 .NET 版本？

A1：是的，Aspose.Drawing 設計上相容於多種 .NET 版本，為開發者提供彈性。

### Q2：我可以進一步自訂字型樣式嗎？

A2：當然可以！調整 `Font` 物件的大小、樣式與字族，即可達成所需的字型外觀。

### Q3：如何在已定義的矩形內處理文字溢位？

A3：您可以透過調整矩形尺寸或自行實作文字換行邏輯，以確保文字完整顯示。

### Q4：Aspose.Drawing 還提供其他格式化選項嗎？

A4：提供完整的圖形操作工具集，包含文字、形狀等多種格式化功能。

### Q5：在哪裡可以取得 Aspose.Drawing 的其他支援資源？

A5：請前往 Aspose.Drawing 論壇[此處](https://forum.aspose.com/c/drawing/44)取得社群支援與討論。

**Additional Q&A**

**Q: How do I draw a string without a surrounding rectangle?**  
A: 省略 `DrawRectangle` 呼叫，直接將目標 `PointF` 位置傳給 `Graphics.DrawString`。

**Q: Can I rotate the text while keeping alignment?**  
A: 可以——在繪製前對 `Graphics` 物件套用 `Matrix` 變換，繪製完畢後再重設。

**Q: Is it possible to export the image as JPEG instead of PNG?**  
A: 只要在 `bitmap.Save` 時更改檔案副檔名，並視需要指定 `ImageFormat.Jpeg` 即可。

---

**最後更新：** 2026-02-25  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}