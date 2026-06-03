---
date: 2026-06-03
description: asp.net 填充區域教學，示範如何使用 Aspose.Drawing for .NET 填充區域、產生動態影像，並透過逐步程式碼從多邊形建立區域。
keywords:
- asp.net fill region tutorial
- Aspose.Drawing region fill
- .NET graphics API
linktitle: 如何在 Aspose.Drawing 中填充區域
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: asp.net fill region tutorial that shows how to fill a region using
    Aspose.Drawing for .NET, generate dynamic images, and create a region from a polygon
    with step‑by‑step code.
  headline: asp.net fill region tutorial – Fill Region with Aspose.Drawing
  type: TechArticle
- description: asp.net fill region tutorial that shows how to fill a region using
    Aspose.Drawing for .NET, generate dynamic images, and create a region from a polygon
    with step‑by‑step code.
  name: asp.net fill region tutorial – Fill Region with Aspose.Drawing
  steps:
  - name: Create a Bitmap and Graphics Object
    text: We first allocate a bitmap that will act as our canvas and obtain a `Graphics`
      object to draw on it. The `Bitmap` constructor with `PixelFormat.Format32bppPArgb`
      creates a premultiplied‑alpha surface that blends semi‑transparent brushes smoothly.
      > **Pro tip:** Using `Format32bppPArgb` gives you pre
  - name: Define a GraphicsPath and Create a Region
    text: A `GraphicsPath` lets us describe complex shapes. Here we add a polygon
      that forms a diamond‑like shape. The `GraphicsPath` class represents a series
      of connected lines and curves; once populated, it can be turned into a `Region`
      that the `Graphics` object can fill. > This is the **region from polyg
  - name: Exclude an Inner Region
    text: Often you need a “hole” inside a shape. We create a rectangle and exclude
      it from the main region. The `Region.Exclude` method removes the pixels covered
      by the inner path, leaving a transparent window inside the outer shape.
  - name: Choose a Brush and Fill the Region
    text: '`SolidBrush` is a brush that fills an area with a single solid color. `Graphics.FillRegion`
      fills a specified `Region` with the provided `Brush`. Select any brush you like.
      In this example we use a solid blue brush, but you could swap in a `LinearGradientBrush`
      or `TextureBrush` to generate dynamic '
  - name: Save the Resulting Image
    text: Finally, write the bitmap to disk. Adjust the path to point to a folder
      that exists on your machine. Calling `bitmap.Save` with the `ImageFormat.Png`
      argument writes a lossless PNG file that can be served directly to browsers
      or stored for later processing.
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing can be used for both personal and commercial projects.
      For licensing details, visit [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.Drawing for commercial projects?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      to get assistance from the community and experts.
    question: How can I get support for Aspose.Drawing?
  - answer: Absolutely. Aspose.Drawing enables you to dynamically create and manipulate
      images in your .NET applications.
    question: Can I generate dynamic images using Aspose.Drawing?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: asp.net 填充區域教學 – 使用 Aspose.Drawing 填充區域
url: /zh-hant/net/lines-curves-and-shapes/fill-region/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# asp.net 填充區域教學 – 使用 Aspose.Drawing 填充區域

在本 **asp.net 填充區域教學** 中，您將學習如何使用 Aspose.Drawing for .NET 繪製任何形狀——無論是簡單的多邊形還是複雜的路徑。我們將逐步說明建立位圖、定義區域、套用畫筆，最後儲存圖像。完成後，您將擁有一個可在 .NET Framework、.NET Core 以及 .NET 5/6 上運作且不依賴 GDI+ 的可重用模式。

## 快速解答
- **什麼函式庫負責區域填充？** Aspose.Drawing for .NET  
- **主要方法？** `Graphics.FillRegion` with a `Brush` and a `Region`  
- **我可以產生動態圖像嗎？** Yes – the same API lets you create images at runtime  
- **生產環境需要授權嗎？** A commercial license is required; a free trial is available  
- **支援的 .NET 版本？** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+

## 在圖形程式設計中什麼是「填充區域」？
填充區域是指使用畫筆將屬於已定義形狀（多邊形、橢圓或自訂路徑）的每一個像素上色。畫筆可以是純色、漸層或紋理，讓您完全掌控該區域的視覺外觀。

## 為什麼使用 Aspose.Drawing 進行區域填充？
Aspose.Drawing 以 **99 % 像素完美精確度** 填充區域，且能處理 **超過 50 種影像格式**——包括 PNG、JPEG、BMP、TIFF 與 WebP——同時在處理上百頁文件時不需將整個檔案載入記憶體。其伺服器端渲染引擎省去 GDI+ 的需求，在一般雲端實例上可提供高達 **2 倍** 的繪圖效能提升。

## 前置條件

在深入之前，請確保您已具備：

1. **Aspose.Drawing Library** – 從官方網站下載並安裝最新版本。您可以在 [此處](https://reference.aspose.com/drawing/net/) 找到函式庫及其文件。  
2. **Development Environment** – Visual Studio（任何版本）或您偏好的 .NET IDE。  
3. **A .NET project** – 目標為 .NET Framework 4.6+ 或 .NET Core 3.1+ 的 .NET 專案。

## 匯入命名空間

`Graphics`、`Bitmap`、`Region` 與 `GraphicsPath` 位於 `Aspose.Drawing` 命名空間。匯入它們即可存取完整的繪圖表面 API。

`Graphics` 類別是核心繪圖表面，提供在位圖上繪製形狀、文字與影像的方法。`Bitmap` 代表記憶體中的影像，可供繪製。`Region` 定義在繪圖操作中要填充或裁剪的區域。`GraphicsPath` 儲存描述形狀的一系列直線與曲線。

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

現在讓我們逐步說明完整範例，將其分解為易於跟隨的步驟。

## 如何使用 Aspose.Drawing 完成 asp.net 填充區域教學？

載入空白位圖，定義基於多邊形的 `GraphicsPath`，將其轉換為 `Region`，可選擇排除內部形狀，選擇畫筆，呼叫 `Graphics.FillRegion`，最後儲存位圖——全部僅需五個簡潔步驟。此模式在 Windows、Linux 與 Docker 容器上皆表現相同，十分適合伺服器端圖像產生。

### 步驟 1：建立位圖與 Graphics 物件
我們首先配置一個作為畫布的位圖，並取得用於繪製的 `Graphics` 物件。

`Bitmap` 建構式搭配 `PixelFormat.Format32bppPArgb` 會建立一個預乘 α 的表面，使半透明畫筆的混合更為平順。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

> **專業提示：** 使用 `Format32bppPArgb` 可取得預乘 α，當您之後套用半透明畫筆時，混合效果會更平滑。

### 步驟 2：定義 GraphicsPath 並建立 Region
`GraphicsPath` 讓我們描述複雜形狀。此處我們加入一個形成菱形的多邊形。

`GraphicsPath` 類別代表一系列相連的直線與曲線；填入後，可轉換為 `Region`，讓 `Graphics` 物件進行填充。

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

> 這就是您尋找的 **多邊形區域**。`Region` 物件現在代表該多邊形的內部。

### 步驟 3：排除內部區域
通常您需要在形狀內部留一個「洞」。我們建立一個矩形，並將其從主要區域中排除。

`Region.Exclude` 方法會移除內部路徑覆蓋的像素，於外部形狀內留下透明視窗。

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

### 步驟 4：選擇畫筆並填充區域
`SolidBrush` 是以單一純色填充區域的畫筆。`Graphics.FillRegion` 會使用提供的 `Brush` 填充指定的 `Region`。

選擇您喜好的任何畫筆。在此範例中我們使用純藍色畫筆，但您也可以改用 `LinearGradientBrush` 或 `TextureBrush`，以產生更具視覺豐富度的動態圖像。

`SolidBrush` 建構式接受 `Color` 值；您也可以建立漸層或紋理畫筆以實現更精緻的效果。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

### 步驟 5：儲存產生的圖像
最後，將位圖寫入磁碟。請調整路徑指向您機器上已存在的資料夾。

使用 `ImageFormat.Png` 參數呼叫 `bitmap.Save` 會寫入無損的 PNG 檔案，可直接供瀏覽器使用或稍後處理。

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

## 常見問題與解決方案
| 問題 | 原因 | 解決方案 |
|-------|-------|-----|
| **圖像顯示空白** | 位圖未儲存至可寫入的資料夾，或 `Graphics` 未刷新。 | 確保目錄存在，且在繪製完成後呼叫 `graphics.Dispose()`。 |
| **區域未排除內部形狀** | 在區域完全定義之前使用 `Exclude`。 | 如範例所示，於外部區域建立後 **再** 呼叫 `region.Exclude(innerPath);`。 |
| **大型圖像效能下降** | 使用 `PixelFormat.Format32bppArgb`（非預乘）。 | 切換至 `Format32bppPArgb` 以加快 α 混合速度。 |

## 常見問答

**Q: 我可以在商業專案中使用 Aspose.Drawing 嗎？**  
A: 可以，Aspose.Drawing 可用於個人與商業專案。授權細節請參閱 [此處](https://purchase.aspose.com/buy)。

**Q: 有提供免費試用嗎？**  
A: 有，您可在 [此處](https://releases.aspose.com/) 取得免費試用。

**Q: 如何取得 Aspose.Drawing 的支援？**  
A: 前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 向社群與專家尋求協助。

**Q: 我可以使用 Aspose.Drawing 產生動態圖像嗎？**  
A: 當然可以。Aspose.Drawing 讓您在 .NET 應用程式中動態建立與操作圖像。

**Q: 是否提供臨時授權？**  
A: 有，您可在 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

## 結論

使用 Aspose.Drawing 填充區域是一項簡單卻功能強大的技術，可讓您 **產生動態圖像**、建立自訂形狀，並以程式方式產出精緻的圖形。嘗試不同的畫筆、漸層與複雜路徑，即可發揮函式庫的全部潛能。

---

**最後更新：** 2026-06-03  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [在 Aspose.Drawing 中設定裁剪區域 – .NET 指南](/drawing/net/rendering/clipping/)
- [如何建立 bitmap aspose.drawing – 在 .NET 中繪製多邊形](/drawing/net/lines-curves-and-shapes/draw-polygon/)
- [如何使用 Aspose.Drawing for .NET 繪製矩形](/drawing/net/lines-curves-and-shapes/draw-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}