---
date: 2026-07-22
description: 了解如何使用 Aspose.Drawing 將位圖儲存為 PNG 並匯出為 JPEG。逐步指南示範繪製路徑、建立影像以及匯出格式。
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: 在 Aspose.Drawing 中繪製路徑
og_description: 使用 Aspose.Drawing for .NET 將位圖儲存為 PNG 並匯出為 JPEG。遵循本教學以繪製複雜路徑、建立高品質影像，並輸出多種格式。
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: 將位圖儲存為 PNG – 使用 Aspose.Drawing 繪製路徑
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: 將位圖儲存為 PNG – 在 Aspose.Drawing 中使用 GraphicsPath
url: /zh-hant/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Drawing 中繪製路徑

## 如何使用 GraphicsPath – 介紹

**Save bitmap as PNG** 通常是您需要無損圖像以進一步處理或發布時的第一步。 在本教程中，您將學習如何使用 `GraphicsPath` 繪製複雜的向量路徑，將其渲染到位圖上，然後 **save bitmap as PNG** 或甚至 **export image to JPEG**。 無論您是構建報告引擎、自訂圖表庫，或僅需產生動態圖形，Aspose.Drawing 為您提供完整管理、跨平台的 API，取代 System.Drawing.Common。

## 快速解答
- **What can I draw with GraphicsPath?** 線條、矩形、橢圓、曲線以及自訂形狀。  
- **Do I need a license?** 試用版免費；商業授權在正式環境中必須使用。  
- **Which .NET versions are supported?** .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6+。  
- **Is System.Drawing.Common required?** 不需要，Aspose.Drawing 可獨立運作。  
- **Can I save to different formats?** 可以 – PNG、JPEG、BMP、GIF 等。

## GraphicsPath 是什麼？

`GraphicsPath` 是 Aspose.Drawing 的向量容器，可將線條、弧線、曲線等繪圖基元序列儲存為單一物件。透過將這些基元分組，您可以統一套用變換、填充規則和筆觸設定，簡化複雜圖形的建立，並確保在不同輸出格式間保持一致的渲染效果。

## 為何在 Aspose.Drawing 中使用 GraphicsPath？

在 Aspose.Drawing 中使用 GraphicsPath 可提供精確、彈性且高效能的向量繪圖功能。它讓您能構建複雜形狀、套用變換，並高效渲染，同時保持跨平台一致性，支援大規模影像處理。此外，它可與其他 .NET 函式庫無縫整合，使您能在單一應用程式中結合點陣圖與向量工作流程。

- **Precision:** 處理超過 50 種向量基元，具次像素精度，確保在 **save bitmap as PNG** 時輸出在任何解析度下仍保持清晰。  
- **Flexibility:** 將線條、弧線與貝茲曲線結合為單一路徑，然後以單一 `Graphics.DrawPath` 呼叫進行渲染。  
- **Performance:** 優化的渲染管線可處理高達 400 MP 的影像，且無需將整個檔案載入記憶體，使大規模批次作業成為可能。  
- **Cross‑Platform:** 在 Windows、Linux 與 macOS 執行環境上產生相同結果，消除平台特定的錯誤。

## 前置條件

在開始本教程之前，請確保您已具備以下前置條件：

- **Aspose.Drawing Library:** 下載並安裝 Aspose.Drawing 函式庫。您可於 [此處](https://releases.aspose.com/drawing/net/) 取得。  
- **Other Aspose Products:** 探索其他 Aspose 產品 [此處](https://releases.aspose.com/)。  
- **Development Environment:** 設定您的 .NET 開發環境，並安裝必要工具（Visual Studio、.NET SDK 等）。

## 匯入命名空間

Start by importing the required namespaces in your project:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 步驟 1：建立 Bitmap 與 Graphics

Bitmap 代表記憶體中的影像，而 Graphics 提供繪圖方法以在該影像上渲染。首先建立 `Bitmap` 與 `Graphics` 物件以供使用。此 bitmap 將作為 `GraphicsPath` 渲染的畫布，稍後您將 **save bitmap as PNG**：

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 2：定義 Pen 與 GraphicsPath

Pen 定義線條顏色、寬度與樣式；GraphicsPath 將一系列繪圖基元儲存為單一向量物件。接著，定義 `Pen` 以指定繪圖屬性，並建立 `GraphicsPath` 實例。`GraphicsPath` 物件在繪製前保存向量資料：

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## 步驟 3：加入線條與形狀

AddLine、AddRectangle 與 AddEllipse 會將相應的形狀加入 GraphicsPath，以供稍後渲染。將線條、矩形與橢圓加入 `GraphicsPath` 以建立複雜路徑。您亦可加入自訂的貝茲曲線以產生平滑形狀：

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## 步驟 4：繪製路徑

DrawPath 使用指定的 Pen，將 GraphicsPath 中的向量資料渲染至 Graphics 表面。使用指定的 `Pen` 在 `Graphics` 物件上繪製路徑。此操作會將向量資料光柵化至 bitmap 畫布上：

```csharp
graphics.DrawPath(pen, path);
```

## 步驟 5：儲存影像 – 匯出為 PNG 或 JPEG

Bitmap.Save 方法會將影像以選擇的格式（如 PNG 或 JPEG）寫入磁碟。繪製完成後，您可以 **save bitmap as PNG** 以獲得無損品質，或 **export image to JPEG** 以取得較小檔案大小。請依您的後續需求選擇最適合的格式：

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

根據需要重複上述步驟，以建立複雜且具視覺吸引力的路徑。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **路徑未顯示** | 確保 Pen 顏色與背景形成對比，且 bitmap 正確儲存。 |
| **影像尺寸異常** | 驗證 bitmap 的尺寸與像素格式符合需求。 |
| **授權例外** | 使用試用授權進行測試；在部署至正式環境前套用有效授權。 |

## 常見問答

### Q1：我可以將 Aspose.Drawing 與其他 .NET 函式庫一起使用嗎？

A1：可以，Aspose.Drawing 可與其他 .NET 函式庫無縫整合，為您的開發專案提供多樣性。

### Q2：是否提供試用版？

A2：可以，您可於 [此處](https://releases.aspose.com/) 取得免費試用版。

### Q3：我可以在哪裡取得 Aspose.Drawing 的支援？

A3：請前往 Aspose.Drawing [論壇](https://forum.aspose.com/c/drawing/44) 取得協助與社群支援。

### Q4：如何取得臨時授權？

A4：可於 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

### Q5：我可以購買 Aspose.Drawing 嗎？

A5：可以，您可於 [此處](https://purchase.aspose.com/buy) 購買 Aspose.Drawing。

**其他問答**

**Q: 我可以使用 GraphicsPath 繪製自訂貝茲曲線嗎？**  
A: 絕對可以 – 使用 `path.AddBezier(...)` 定義平滑曲線。

**Q: 我該如何在重新使用前清除 GraphicsPath？**  
A: 呼叫 `path.Reset()` 以移除所有圖形並重新開始。

## 結論

恭喜！您已成功學會 **how to use GraphicsPath** 來繪製路徑，並使用 Aspose.Drawing for .NET **save bitmap as PNG** 或 **export image to JPEG**。本教程涵蓋了建立 bitmap、定義 pen、構建 `GraphicsPath`、渲染各種形狀，以及以多種格式匯出最終影像。請嘗試不同的座標、顏色與線寬，以釋放 Aspose.Drawing 的全部創意潛能。

---

**最後更新：** 2026-07-22  
**測試版本：** Aspose.Drawing 24.12 for .NET  
**作者：** Aspose

## 相關教學

- [將 Bitmap 儲存為 PNG 並使用 Aspose.Drawing 繪製閉合曲線](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [儲存 Bitmap C# – 使用 Aspose.Drawing 繪製貝茲樣條](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [如何儲存影像並在 Aspose.Drawing 中繪製基數樣條](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}