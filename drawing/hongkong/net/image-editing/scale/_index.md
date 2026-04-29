---
date: 2026-02-07
description: 學習如何使用 Aspose.Drawing for .NET 進行圖像縮放。本指南逐步說明如何在 C# 中使用最近鄰插值法調整位圖大小，並儲存縮放後的圖像檔案。
linktitle: Scaling Images in Aspose.Drawing
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

歡迎閱讀本完整指南，了解如何使用 Aspose.Drawing for .NET **縮放圖像**！在軟體開發的動態環境中，操作與縮放圖像是常見需求。Aspose.Drawing 簡化了此過程，提供強大的工具與功能，讓您在 .NET 應用程式中處理圖像。

## 快速回答
- **應該使用哪個函式庫？** Aspose.Drawing for .NET  
- **哪種插值方法能得到最銳利的結果？** NearestNeighbor interpolation  
- **我可以在 C# 中更改圖像大小嗎？** Yes – use the Bitmap and Graphics classes  
- **如何儲存縮放後的圖像？** Call `bitmap.Save(...)` with the desired path  
- **是否需要授權？** A temporary license is available for evaluation  

## 什麼是 Aspose.Drawing 中的圖像縮放？

圖像縮放是將位圖調整為更大或更小尺寸的過程，同時保持視覺品質。Aspose.Drawing 提供直觀的 API 讓 C# 開發人員可以控制每一步——從建立畫布到使用矩形繪製圖像，以變更圖像大小。

## 為什麼使用 Aspose.Drawing 進行縮放？

- **高效能渲染** – 為大型圖像優化。  
- **豐富的插值選項** – 包括用於像素完美縮放的 nearest neighbor。  
- **完整的 .NET 支援** – 可在 .NET Framework、.NET Core 以及 .NET 5/6+ 上運作。  
- **無外部相依性** – 單一 NuGet 套件即可取代 System.Drawing.Common。

## 先決條件

在開始本教學之前，請確保您已具備以下先決條件：

1. Aspose.Drawing for .NET：確保已在專案中安裝 Aspose.Drawing 函式庫。您可以在[此處](https://releases.aspose.com/drawing/net/)下載。  
2. 開發環境：設定 .NET 開發環境，例如 Visual Studio。  
3. 基本的 C# 知識：熟悉 C# 程式語言是實作範例的必要條件。

## 匯入命名空間

在您的 C# 專案中，首先匯入必要的命名空間。此步驟對於順暢使用 Aspose.Drawing 功能至關重要。

```csharp
using System.Drawing;
```

## 步驟 1：建立 Bitmap（畫布）

首先建立一個作為圖像畫布的 `Bitmap` 物件。依需求指定寬度、高度與像素格式。這是經典的 *resize bitmap C#* 方法。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 2：建立 Graphics 物件

接著，從先前建立的 `Bitmap` 產生 `Graphics` 物件。此物件提供圖像操作所需的繪圖功能，包含之後可使用的 **drawimage with rectangle**。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 3：設定插值模式

為提升縮放圖像的品質，請設定插值模式。在本範例中，我們使用 **NearestNeighbor interpolation** 模式，適合需要清晰、像素藝術風格放大的情況。

```csharp
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

## 步驟 4：載入圖像

將欲縮放的圖像載入 `Bitmap` 物件。將 `"Your Document Directory" + @"Images\aspose_logo.png"` 替換為您的圖像路徑。

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

## 步驟 5：縮放圖像

定義一個代表圖像擴展的矩形。在本例中，圖像在寬度與高度上皆放大 5 倍。此示範 **drawimage with rectangle** 技術。

```csharp
Rectangle expansionRectangle = new Rectangle(0, 0, image.Width * 5, image.Height * 5);
graphics.DrawImage(image, expansionRectangle);
```

## 步驟 6：儲存縮放後的圖像

將縮放後的圖像儲存至指定位置。依專案結構調整檔案路徑。此步驟示範如何以 PNG 等常見格式 **save scaled image**。

```csharp
bitmap.Save("Your Document Directory" + @"Images\Scale_out.png");
```

恭喜！您已成功學會使用 Aspose.Drawing for .NET **縮放圖像**。

## 結論

在本教學中，我們探討了使用 Aspose.Drawing 進行圖像縮放的流程。此函式庫讓開發人員能在 .NET 應用程式中高效處理圖像操作。透過逐步指南，您已獲得關於圖像縮放實作的寶貴見解，包括更改圖像大小 C#、調整 bitmap 大小 C#、使用 nearest neighbor 插值、以矩形繪製圖像，以及儲存縮放後的圖像。

歡迎進一步實驗，探索 Aspose.Drawing 提供的其他功能，以提升您的圖像處理能力。

## 常見問題

### Q1：我可以在 Web 與桌面應用程式中使用 Aspose.Drawing for .NET 嗎？

A1：是的，Aspose.Drawing 多功能且可在各種 .NET 應用程式中使用，包括 Web 與桌面。

### Q2：Aspose.Drawing 是否提供暫時授權？

A2：是的，您可於[此處](https://purchase.aspose.com/temporary-license/)取得暫時授權，以供測試與評估使用。

### Q3：我可以在哪裡取得 Aspose.Drawing 的其他支援？

A3：如有任何問題或需要協助，請前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44)。

### Q4：Aspose.Drawing 支援的圖像格式是否有任何限制？

A4：Aspose.Drawing 支援多種圖像格式，包括 JPEG、PNG、GIF、BMP 等。詳情請參考[文件說明](https://reference.aspose.com/drawing/net/)。

### Q5：我可以為圖像縮放套用自訂的插值模式嗎？

A5：是的，Aspose.Drawing 提供彈性，讓您可在多種插值模式中選擇以進行圖像縮放。

## 常見問答

**Q：nearest neighbor 插值與 bilinear 有何不同？**  
A：nearest neighbor 直接複製最近的像素值，保留硬邊緣；而 bilinear 會計算加權平均，以獲得較平滑的結果。

**Q：我可以在不保留長寬比的情況下縮放圖像嗎？**  
A：可以——在矩形中指定不同的寬度與高度，即可依需求拉伸或壓縮圖像。

**Q：能否在迴圈中一次縮放多張圖像？**  
A：完全可以。將 bitmap 建立、繪製與儲存的邏輯包在 `foreach` 迴圈中，遍歷來源檔案即可。

---

**最後更新：** 2026-02-07  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}