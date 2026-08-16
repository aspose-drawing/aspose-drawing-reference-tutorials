---
date: 2026-08-16
description: 了解如何使用 Aspose.Drawing for .NET 填充區域、產生動態影像，並透過逐步程式碼從多邊形建立區域。
keywords:
- how to fill region
- server side image generation
- create dynamic images
- fill shape gradient
- region filling graphics
lastmod: 2026-08-16
linktitle: 如何在 Aspose.Drawing 中填充區域
og_description: 了解如何使用 Aspose.Drawing for .NET 填充區域。本指南涵蓋伺服器端影像產生、建立動態影像，以及使用漸層填充區域。
og_image_alt: Screenshot of a filled polygon region created with Aspose.Drawing in
  .NET
og_title: 如何在 Aspose.Drawing 中填充區域 – 伺服器端影像產生
schemas:
- author: Aspose
  dateModified: '2026-08-16'
  description: Learn how to fill region using Aspose.Drawing for .NET, generate dynamic
    images, and create a region from polygon with step‑by‑step code.
  headline: How to Fill Region in Aspose.Drawing
  type: TechArticle
- description: Learn how to fill region using Aspose.Drawing for .NET, generate dynamic
    images, and create a region from polygon with step‑by‑step code.
  name: How to Fill Region in Aspose.Drawing
  steps:
  - name: Create a bitmap and graphics object
    text: '`Graphics` is Aspose.Drawing’s primary drawing surface that provides methods
      for rendering shapes, text, and images onto a bitmap. We first allocate a bitmap
      that will act as our canvas and obtain a `Graphics` object to draw on it. >
      **Pro tip:** Using `Format32bppPArgb` gives you premultiplied alph'
  - name: Define a graphics path and create a region
    text: '`GraphicsPath` represents a series of connected lines and curves that can
      describe any shape. Here we add a polygon that forms a diamond‑like shape, then
      wrap it in a `Region` object. > This is the **region from polygon** you were
      looking for. The `Region` object now represents the interior of that '
  - name: Exclude an inner region
    text: '`Region.Exclude` removes the pixels of a supplied shape from the current
      region, effectively creating a “hole.” We create a rectangle and exclude it
      from the main region.'
  - name: Choose a brush and fill the region
    text: '`Brush` is the abstract base for all fill styles. In this example we use
      a solid blue brush, but you could swap in a `LinearGradientBrush` or `TextureBrush`
      to generate richer visuals.'
  - name: Save the resulting image
    text: '`Bitmap.Save` writes the image to disk in the format you specify. Adjust
      the path to point to a folder that exists on your machine.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing can be used for both personal and commercial projects.
      For licensing details, visit the [Aspose.Drawing purchase page](https://purchase.aspose.com/buy).
    question: Can I use Aspose.Drawing for commercial projects?
  - answer: Yes, you can access a free trial [Aspose.Drawing free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      to get assistance from the community and experts.
    question: How can I get support for Aspose.Drawing?
  - answer: Absolutely. Aspose.Drawing enables you to dynamically create and manipulate
      images in your .NET applications.
    question: Can I generate dynamic images using Aspose.Drawing?
  - answer: Yes, temporary licenses can be obtained [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- fill region
- Aspose.Drawing
- .NET graphics
- server‑side image generation
- dynamic image creation
title: 如何在 Aspose.Drawing 中填充區域
url: /zh-hant/net/lines-curves-and-shapes/fill-region/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing 中填充區域

創建視覺上吸引人的圖形通常涉及 **如何填充區域**，使用顏色、圖案或漸層。Aspose.Drawing for .NET 為您提供乾淨且高效能的 API 來處理此任務，無論您是在構建報表引擎、設計工具，或即時產生動態影像。在本教學中，您將一步步看到 **如何填充區域**，從設定 bitmap 到儲存最終圖片。

## 快速解答
- **哪個函式庫處理區域填充？** Aspose.Drawing for .NET  
- **主要方法？** `Graphics.FillRegion` with a `Brush` and a `Region`  
- **我可以產生動態影像嗎？** Yes – the same API lets you create images at runtime  
- **生產環境需要授權嗎？** A commercial license is required; a free trial is available  
- **支援的 .NET 版本？** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+

## 在圖形程式設計中什麼是「填充區域」？
填充區域指的是使用畫筆將屬於已定義形狀（多邊形、橢圓或自訂路徑）的每個像素上色。畫筆可以是純色、漸層或紋理，讓您完整掌控該區域的視覺外觀。`Graphics.FillRegion` 是在 Aspose.Drawing 中執行此操作的核心方法。

## 為何使用 Aspose.Drawing 進行區域填充？
Aspose.Drawing 可處理 **超過 30 種影像格式**，且能在不將整個檔案載入記憶體的情況下渲染多百頁的圖形，於一般伺服器硬體上提供高達 GDI+ 兩倍的效能。此函式庫在 .NET Framework、.NET Core 與 .NET 5/6 上表現一致，消除平台特有的怪癖，並免除在無頭伺服器上對原生 GDI+ 的相依需求。

## 前置條件

在開始之前，請確保您已具備：

1. **Aspose.Drawing Library** – 下載並從官方網站安裝最新版本。您可以在此找到函式庫及其文件 [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/)。  
2. **Development environment** – Visual Studio (any edition) or your preferred .NET IDE.  
3. **A .NET project** targeting .NET Framework 4.6+ or .NET Core 3.1+.

## 匯入命名空間

首先匯入包含我們將使用的圖形類別的命名空間。

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

現在讓我們逐步走過完整範例，將其拆解為易於跟隨的步驟。

## 步驟指南

### 步驟 1：建立 bitmap 與 graphics 物件
`Graphics` 是 Aspose.Drawing 的主要繪圖表面，提供在 bitmap 上繪製形狀、文字與影像的方法。我們首先分配一個作為畫布的 bitmap，並取得 `Graphics` 物件以在其上繪圖。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

> **專業提示：** 使用 `Format32bppPArgb` 可取得預乘 Alpha，當您之後套用半透明畫筆時，能產生更平滑的混合效果。

### 步驟 2：定義 graphics path 並建立 region
`GraphicsPath` 代表一系列相連的直線與曲線，可描述任何形狀。此處我們加入一個形成菱形的多邊形，然後將其包裹於 `Region` 物件中。

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

> 這就是您尋找的 **由多邊形產生的區域**。`Region` 物件現在代表該多邊形的內部。

### 步驟 3：排除內部區域
`Region.Exclude` 會從目前的區域中移除提供之形狀的像素，實際上會產生一個「洞」。我們建立一個矩形並將其從主要區域中排除。

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

### 步驟 4：選擇畫筆並填充區域
`Brush` 是所有填充樣式的抽象基底。在此範例中我們使用實心藍色畫筆，但您也可以換成 `LinearGradientBrush` 或 `TextureBrush` 以產生更豐富的視覺效果。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

### 步驟 5：儲存產生的影像
`Bitmap.Save` 會將影像以您指定的格式寫入磁碟。請調整路徑指向您機器上已存在的資料夾。

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

## 常見問題與解決方案
| 問題 | 原因 | 解決方式 |
|-------|-------|-----|
| **影像顯示空白** | Bitmap 未儲存至可寫入的資料夾或 `Graphics` 未刷新。 | 確保目錄存在，且在繪圖後呼叫 `graphics.Dispose()`。 |
| **區域未排除內部形狀** | 在區域完全定義之前使用 `Exclude`。 | 在建立外部區域後 **呼叫** `region.Exclude(innerPath);`，如範例所示。 |
| **大型影像效能延遲** | 使用 `PixelFormat.Format32bppArgb`（非預乘）。 | 切換至 `Format32bppPArgb` 以加快 Alpha 混合。 |

## 常見問答

**Q: 我可以在商業專案中使用 Aspose.Drawing 嗎？**  
A: 可以，Aspose.Drawing 可用於個人與商業專案。授權細節請參閱 [Aspose.Drawing purchase page](https://purchase.aspose.com/buy)。

**Q: 有免費試用版嗎？**  
A: 有，您可以存取免費試用版 [Aspose.Drawing free trial page](https://releases.aspose.com/)。

**Q: 如何取得 Aspose.Drawing 的支援？**  
A: 前往 [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) 以獲得社群與專家的協助。

**Q: 我可以使用 Aspose.Drawing 產生動態影像嗎？**  
A: 當然可以。Aspose.Drawing 讓您在 .NET 應用程式中動態建立與操作影像。

**Q: 是否提供臨時授權？**  
A: 有，臨時授權可於 [temporary license page](https://purchase.aspose.com/temporary-license/) 取得。

## 結論

使用 Aspose.Drawing 填充區域是一項簡單卻強大的技術，讓您能 **產生動態影像**、建立自訂形狀，並以程式方式產出精緻的圖形。請嘗試不同的畫筆、漸層與複雜路徑，以發揮函式庫的全部潛能。

---

**Last Updated:** 2026-08-16  
**Tested with:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [在 Aspose.Drawing 中設定裁剪區域 – .NET 指南](/drawing/net/rendering/clipping/)
- [如何使用 Aspose.Drawing for .NET 繪製弧線與其他形狀](/drawing/net/lines-curves-and-shapes/)
- [如何使用 Aspose.Drawing API for .NET 繪製矩形 – 座標系統轉換（頁面轉換）](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}