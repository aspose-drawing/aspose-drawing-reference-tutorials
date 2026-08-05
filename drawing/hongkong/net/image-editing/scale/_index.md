---
date: 2026-05-24
description: 了解如何使用 Aspose.Drawing for .NET 縮放圖像。本指南逐步說明如何使用最近鄰插值法在 C# 中調整位圖尺寸，並儲存縮放後的圖像檔案。
keywords:
- how to scale images
- nearest neighbor scaling
- change image size
- high performance scaling
- resize bitmap c#
linktitle: 在 Aspose.Drawing 中縮放圖像
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to scale images with Aspose.Drawing for .NET. This guide
    shows step‑by‑step how to resize bitmap C# using nearest neighbor interpolation
    and save scaled image files.
  headline: How to Scale Images with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to scale images with Aspose.Drawing for .NET. This guide
    shows step‑by‑step how to resize bitmap C# using nearest neighbor interpolation
    and save scaled image files.
  name: How to Scale Images with Aspose.Drawing for .NET
  steps:
  - name: 'Aspose.Drawing for .NET - Ensure that you have the Aspose.Drawing library
      installed in your project. You can download it [here](https://releases.aspose.com/drawing/net/).'
    text: 'Aspose.Drawing for .NET - Ensure that you have the Aspose.Drawing library
      installed in your project. You can download it [here](https://releases.aspose.com/drawing/net/).'
  - name: 'Development Environment - Set up a .NET development environment, such as
      Visual Studio.'
    text: 'Development Environment - Set up a .NET development environment, such as
      Visual Studio.'
  - name: 'Basic Understanding of C# - Familiarity with the C# programming language
      is essential for implementing the examples.'
    text: 'Basic Understanding of C# - Familiarity with the C# programming language
      is essential for implementing the examples.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing is fully compatible with ASP.NET, ASP.NET Core, WPF,
      WinForms, and console applications.
    question: Can I use Aspose.Drawing for .NET in both web and desktop applications?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for testing and evaluation purposes.
    question: Is a temporary license available for Aspose.Drawing?
  - answer: For any queries or assistance, visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).
    question: Where can I find additional support for Aspose.Drawing?
  - answer: Aspose.Drawing supports a wide range of formats, including JPEG, PNG,
      GIF, BMP, TIFF, WebP, and SVG. See the full list in the [documentation](https://reference.aspose.com/drawing/net/).
    question: Are there any limitations on the image formats supported by Aspose.Drawing?
  - answer: Yes, Aspose.Drawing provides `NearestNeighbor`, `Bilinear`, `Bicubic`,
      and `HighQualityBicubic` modes, allowing you to balance speed and quality.
    question: Can I apply custom interpolation modes for image scaling?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing for .NET 縮放圖像
url: /zh-hant/net/image-editing/scale/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing for .NET 縮放圖像

## 簡介

在本完整教學中，您將學習如何使用 Aspose.Drawing for .NET 高效地 **縮放圖像**。無論您是建立產生縮圖的 Web 服務，或是放大像素藝術素材的桌面工具，圖像縮放都是核心需求。我們將逐步說明每個步驟——從建立畫布、套用最近鄰插值，到最終儲存結果——讓您在數分鐘內實作高效能的縮放。

## 快速解答
- **應該使用哪個函式庫？** Aspose.Drawing for .NET  
- **哪種插值能提供最銳利的結果？** NearestNeighbor interpolation  
- **我可以在 C# 中變更圖像大小嗎？** 是 – 使用 `Bitmap` 和 `Graphics` 類別  
- **如何儲存縮放後的圖像？** 呼叫 `bitmap.Save(...)` 並指定路徑  
- **是否需要授權？** 可取得臨時授權以供評估  

## 什麼是 Aspose.Drawing 中的圖像縮放？

圖像縮放是將位圖調整為更大或更小尺寸的過程，同時保持視覺品質。Aspose.Drawing 提供直觀的 API，讓 C# 開發人員能掌控每一步——從建立畫布到在目標矩形內繪製來源圖像。

## 為什麼使用 Aspose.Drawing 進行縮放？

Aspose.Drawing 為高負載工作提供 **高效能縮放**：支援 **30 多種圖像格式**（包括 PNG、JPEG、BMP、TIFF 和 WebP），且可在不將整張圖像載入記憶體的情況下處理高達 **500 MB** 的檔案。此函式庫亦提供 **四種插值模式**，其中 **NearestNeighbor** 可提供像素完美的結果，特別適用於圖示和遊戲美術。由於它是單一的 NuGet 套件，**沒有外部原生相依性**，因此可順利部署至 Linux 容器或 Azure Functions。

## 先決條件

在開始本教學之前，請確保您具備以下先決條件：

1. Aspose.Drawing for .NET：確保已在專案中安裝 Aspose.Drawing 函式庫。您可於 [此處](https://releases.aspose.com/drawing/net/) 下載。  
2. 開發環境：建立 .NET 開發環境，例如 Visual Studio。  
3. C# 基礎知識：熟悉 C# 程式語言對於實作範例至關重要。  

## 匯入命名空間

在您的 C# 專案中，首先匯入必要的命名空間。此步驟對於順利存取 Aspose.Drawing 功能至關重要。

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Drawing2D;
```

## 步驟 1：建立 Bitmap（畫布）

`Bitmap` 類別代表可在記憶體中操作的圖像，您可以在其上繪圖或進行處理。  
首先建立一個 `Bitmap` 物件，作為圖像的畫布。依需求指定寬度、高度與像素格式。這是傳統的 *resize bitmap C#* 方法。

```csharp
using System.Drawing;
```

## 步驟 2：建立 Graphics 物件

`Graphics` 類別提供在 bitmap 上繪製形狀、文字與圖像的方法。  
接著，從先前建立的 `Bitmap` 產生 `Graphics` 物件。此物件提供影像操作所需的繪圖功能，包含之後可使用的 **drawimage with rectangle**。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 3：設定插值模式

`InterpolationMode` 決定圖像縮放時像素值的計算方式。  
為提升縮放圖像的品質，請設定插值模式。在此範例中，我們使用 **NearestNeighbor** 模式，適合需要清晰像素藝術風格放大的情況。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 4：載入圖像

`Image.FromFile` 方法將現有圖像檔案載入記憶體，成為 `Bitmap`。  
將您想要縮放的圖像載入為 `Bitmap` 物件。將 `"Your Document Directory" + @"Images\aspose_logo.png"` 替換為您的圖像路徑。

```csharp
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

## 步驟 5：縮放圖像

`Rectangle` 定義來源圖像將被繪製的目標區域。  
定義一個表示圖像擴展的矩形。在此範例中，圖像在寬度與高度上皆放大 5 倍，示範 **drawimage with rectangle** 技術。

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

## 步驟 6：儲存縮放後的圖像

`Bitmap.Save` 將記憶體中的 bitmap 依檔案副檔名推斷的格式寫入檔案。  
將縮放後的圖像儲存至指定位置。依專案結構調整檔案路徑。此步驟示範如何在常見格式（如 PNG）中 **save scaled image**。

```csharp
Rectangle expansionRectangle = new Rectangle(0, 0, image.Width * 5, image.Height * 5);
graphics.DrawImage(image, expansionRectangle);
```

恭喜！您已成功學會使用 Aspose.Drawing for .NET **縮放圖像**。

## 常見問題與解決方案

- **圖像縮放後變得模糊** – 確保使用 `InterpolationMode.NearestNeighbor` 以獲得像素完美的結果；若要平滑縮放照片，可改用 `Bilinear` 或 `HighQualityBicubic`。  
- **大型檔案導致記憶體不足例外** – Aspose.Drawing 以分塊方式處理圖像；若需處理超過 500 MB 的檔案，請提升 `MemoryLimit` 屬性。  
- **比例失真** – 寬高使用相同的縮放係數，或依原始長寬比計算矩形，以避免變形。

## 常見問答

**Q: 我可以在 Web 與桌面應用程式中同時使用 Aspose.Drawing for .NET 嗎？**  
A: 可以，Aspose.Drawing 完全相容於 ASP.NET、ASP.NET Core、WPF、WinForms 以及主控台應用程式。

**Q: 是否提供 Aspose.Drawing 的臨時授權？**  
A: 可以，您可於 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權，以供測試與評估使用。

**Q: 哪裡可以取得 Aspose.Drawing 的其他支援？**  
A: 如有任何問題或需要協助，請前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44)。

**Q: Aspose.Drawing 支援的圖像格式是否有任何限制？**  
A: Aspose.Drawing 支援多種格式，包括 JPEG、PNG、GIF、BMP、TIFF、WebP 與 SVG。完整清單請參閱 [文件說明](https://reference.aspose.com/drawing/net/)。

**Q: 我可以為圖像縮放套用自訂插值模式嗎？**  
A: 可以，Aspose.Drawing 提供 `NearestNeighbor`、`Bilinear`、`Bicubic` 與 `HighQualityBicubic` 模式，讓您在速度與品質之間取得平衡。

## 結論

在本教學中，我們探討了使用 Aspose.Drawing **縮放圖像** 的完整工作流程。您現在已了解如何建立 bitmap 畫布、設定 graphics 物件、選擇最佳插值模式、載入來源圖像、將其繪製至縮放矩形，最後儲存結果。透過 Aspose.Drawing 的 **高效能縮放** 與 **30 多種格式支援**，您可以構建在任何 .NET 平台上高效執行的強大影像處理管線。

歡迎嘗試不同的插值模式、在迴圈中批次處理多個檔案，或將縮放與 Aspose.Drawing 其他功能（如浮水印或色彩空間轉換）結合使用。

---

**最後更新：** 2026-05-24  
**測試版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Scale_out.png");
```

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [如何使用 Aspose.Drawing for .NET 繪製影像 bitmap](/drawing/net/image-editing/display/)
- [如何使用 Aspose.Drawing for .NET 裁切圖像為 PNG](/drawing/net/image-editing/cropping/)
- [如何使用 Aspose.Drawing 全域變換旋轉圖像](/drawing/net/coordinate-transformations/global-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}