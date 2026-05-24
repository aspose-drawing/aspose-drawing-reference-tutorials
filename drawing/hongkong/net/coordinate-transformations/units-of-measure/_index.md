---
date: 2026-05-24
description: 了解如何在 Aspose.Drawing for .NET 中設定單位、輕鬆轉換圖形單位，並掌握圖形渲染的精確測量。
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Aspose.Drawing 的測量單位
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何在 Aspose.Drawing for .NET 中設定單位 – 測量單位
url: /zh-hant/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing for .NET 中設定單位 – 測量單位

## 介紹

歡迎來到 Aspose.Drawing for .NET 的世界，在這裡精確度與彈性在圖形操作中相得益彰。於本教學中，您將了解 **如何設定單位**，學習在點、毫米與英吋之間 **轉換圖形單位**，並看到實務範例，使您的影像達到像素完美。無論您是建立報告、縮圖或自訂圖表，精通測量單位對於在各種裝置上保持一致的渲染都是必不可少的。

## 快速解答
- **變更單位的主要方法是什麼？** 在 `Graphics` 物件上呼叫 `graphics.PageUnit = PageUnit.Point`（或 `.Millimeter`、`.Inch`）。  
- **哪一個單位等於 1/72 英吋？** 點（Points）。  
- **一英吋等於多少毫米？** 25.4 mm = 1 inch。  
- **使用單位需要額外的函式庫嗎？** 不需要，Aspose.Drawing 核心函式庫已提供所有單位常數。  
- **可以在同一張影像中混合使用不同單位嗎？** 每個 `Graphics` 實例只設定一次單位；所有繪圖均使用該單位以確保一致性。

## 前置條件

在深入本教學之前，請確保已具備以下前置條件：

- Aspose.Drawing for .NET：確保已安裝此函式庫。您可在[此處](https://releases.aspose.com/drawing/net/)下載。  
- 文件目錄：準備一個指定的目錄，用於儲存您建立的文件。  
- 基本 C# 知識：建議具備 C# 基礎概念，以便充分利用本指南。

## 匯入命名空間

在開始之前，讓我們匯入使用 Aspose.Drawing 所需的命名空間：

```csharp
using System.Drawing;
```

現在，讓我們將每個範例分解為多個步驟：

## 如何將單位設定為點（Points）？

`Bitmap` 類別代表記憶體中的圖像，作為繪圖畫布。載入您的 bitmap，建立 `Graphics` 物件，並將頁面單位設定為點（points）——這告訴 Aspose.Drawing 將所有座標解讀為 1/72 英吋的值。使用點可讓您對列印就緒的圖形進行精細控制，並以高精度指定線寬。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步驟 1：建立 Bitmap  
`Bitmap` 類別代表記憶體中的圖像，作為繪圖畫布。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 步驟 2：建立 Graphics 物件  
`Graphics` 提供在 `Bitmap` 上繪製形狀與文字的方法。

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### 步驟 3：將頁面單位設定為點（Points）  
`PageUnit` 為列舉型別，用於指定頁面座標的測量單位。`PageUnit.Point` 將點作為測量單位（1 點 = 1/72 英吋）。此設定會套用於所有後續的繪圖呼叫。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### 步驟 4：以點為單位繪製矩形  
在設定單位後繪製矩形時，您指定的尺寸會被解讀為點，確保尺寸的精確性。

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## 如何將單位設定為毫米（Millimeters）？

`PageUnit` 為列舉型別，用於指定頁面座標的測量單位。切換為毫米在需要公制尺寸時非常有用，例如產生工程圖。Aspose.Drawing 將 1 mm 視為 1/25.4 英吋，使您能將圖形與製造與技術文件中使用的實體測量對齊。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### 步驟 1：將頁面單位設定為毫米  
將 `PageUnit.Millimeter` 指派給 `Graphics` 物件；所有座標現在對應公制系統。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 步驟 2：以毫米為單位繪製矩形  
矩形的寬度與高度現在以毫米表示，便於與實體測量對齊，並確保列印輸出符合實際尺寸。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 如何將單位設定為英吋（Inches）？

`Graphics` 提供在 `Bitmap` 上繪製形狀與文字的方法。英吋是許多美國設計工具的預設單位。將單位設定為英吋可讓您在佈局 UI 元素時使用熟悉的單位，並簡化從螢幕設計轉換至列印（常用英吋）的過程。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### 步驟 1：將頁面單位設定為英吋  
`PageUnit.Inch` 會變更座標系統，使 1 單位等於 1 英吋，提供一種直接的方式為列印導向的版面配置設定尺寸。

CODE_BLOCK_PLACEHOLDER_10_END

### 步驟 2：以英吋為單位繪製矩形  
現在您繪製的任何形狀皆以英吋為測量基礎，這對於列印版面配置以及向習慣使用英制單位的利害關係人傳達尺寸尤為理想。

CODE_BLOCK_PLACEHOLDER_11_END

## 儲存結果

完成範例後，將產生的影像儲存至您的文件目錄。`Bitmap.Save` 方法會以您指定的格式（PNG、JPEG 等）寫入檔案。

CODE_BLOCK_PLACEHOLDER_12_END

現在，您已成功掌握 Aspose.Drawing for .NET 中多樣的測量單位，並使用點、毫米與英吋繪製矩形的視覺表示。

## 為什麼使用 Aspose.Drawing 的單位系統？

Aspose.Drawing 支援 **30+ 種影像格式**，且可在不將整個檔案載入記憶體的情況下處理高達 **5000 × 5000 像素** 的影像，為大規模圖形產生提供高效能。透過明確設定單位，您可消除猜測、減少轉換錯誤，並確保輸出在所有平台上符合精確的實體尺寸。

## 常見問題與解決方案

- **儲存後尺寸異常** – 確認已在任何繪圖呼叫之前設定 `graphics.PageUnit` **before**；之後變更單位不會自動調整已存在的形狀大小。  
- **高 DPI 螢幕顯示模糊** – 提高 bitmap 的解析度（例如 `new Bitmap(width, height, 300)`）以符合目標 DPI。  
- **同一影像混用單位** – 為每種單位建立獨立的 `Graphics` 實例，或在繪圖前自行進行轉換。

## 常見問答

### Q1：我可以在其他 .NET 框架中使用 Aspose.Drawing for .NET 嗎？

A1：是的，Aspose.Drawing 相容於多種 .NET 框架，為您的開發環境提供彈性。

### Q2：是否提供免費試用？

A2：是的，您可在[此處](https://releases.aspose.com/)取得 Aspose.Drawing 的免費試用。

### Q3：如何取得 Aspose.Drawing for .NET 的支援？

A3：請前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 獲取社群支援與討論。

### Q4：我可以為短期專案購買臨時授權嗎？

A4：是的，您可在[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q5：在哪裡可以找到 Aspose.Drawing 的詳細文件？

A5：完整文件可在[此處](https://reference.aspose.com/drawing/net/)取得。

---

**最後更新：** 2026-05-24  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [座標系統轉換 – Aspose.Drawing for .NET 中的頁面轉換](/drawing/net/coordinate-transformations/page-transformation/)
- [矩陣轉換教學：Aspose.Drawing for .NET 中的矩陣轉換](/drawing/net/coordinate-transformations/matrix-transformations/)
- [如何套用轉換：Aspose.Drawing for .NET 中的本地轉換](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}