---
date: 2026-01-27
description: 學習如何使用 Aspose.Drawing for .NET 旋轉橢圓形並將圖形轉換為 PNG。逐步指南與程式碼範例。
linktitle: Local Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何旋轉橢圓：Aspose.Drawing for .NET 中的本地變換
url: /zh-hant/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何旋轉橢圓：Aspose.Drawing for .NET 的本地變換

## 簡介

如果您需要在 .NET 應用程式中 **旋轉橢圓**，Aspose.Drawing 提供簡單且可靠的方式。於本教學中，您將學會使用變換矩陣 **旋轉橢圓**、呈現結果，並最終 **將圖形轉換為 PNG** 以供儲存或後續處理。完成後，您將擁有可重複使用的模式，適用於任何本地變換情境。

## 快速回答
- **什麼是本地變換？** 它是一種基於矩陣的操作（旋轉、縮放、平移、斜切），應用於特定的繪圖元素而不影響整個畫布。  
- **哪個函式庫在 .NET 中支援它？** Aspose.Drawing for .NET 提供完整功能的 API，適用於所有支援的 .NET 版本。  
- **我可以將結果儲存為 PNG 嗎？** 可以——只需使用「.png」檔名呼叫 `Bitmap.Save`，Aspose.Drawing 會處理轉換。  
- **開發需要授權嗎？** 免費試用版可用於測試；正式使用需購買商業授權。  
- **實作需要多長時間？** 基本範例大約需要 10‑15 分鐘。

## 如何使用 Aspose.Drawing 旋轉橢圓
旋轉橢圓本質上是 **使用矩陣旋轉形狀**。您建立一個 `Matrix`，設定旋轉角度，指定橢圓的中心點，然後將該矩陣套用到 `GraphicsPath`。這樣可讓旋轉僅限於橢圓，而畫布的其他部分保持不變。

## 在圖形程式設計中，什麼是「套用變換」？
套用變換是指使用 **Matrix** 來修改繪圖物件的座標系統。矩陣定義了點的旋轉、縮放或移動方式，讓您以最少的程式碼即可產生複雜的視覺效果。

## 為什麼使用 Aspose.Drawing **將圖形轉換為 PNG**？
- **跨平台**：支援 .NET Framework、.NET Core 以及 .NET 5/6+。  
- **無 GDI+ 依賴**：避免在非 Windows 平台上使用 `System.Drawing.Common` 的問題。  
- **高品質渲染**：具備抗鋸齒與像素精準的 PNG 輸出。  
- **豐富的 API**：完整支援路徑、筆、畫刷以及變換矩陣。

## 先決條件

在開始之前，請確保您已具備以下項目：

1. **Aspose.Drawing for .NET** – 從 [download link](https://releases.aspose.com/drawing/net/) 下載並安裝。  
2. 您機器上的資料夾，用於儲存輸出影像（例如 `C:\MyImages\`）。  
3. 具備 C# 與 .NET 專案設定的基本知識。  

## 匯入命名空間

首先，將所需的命名空間加入您的 C# 檔案：

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

這些命名空間讓您能使用 `Bitmap`、`Graphics`、`GraphicsPath` 與 `Matrix` 類別，以完成變換工作流程。

## 逐步指南

### 步驟 1：建立 Bitmap

我們從空白畫布開始。Bitmap 的尺寸與像素格式被選擇為高品質、32 位元且支援 Alpha 透明度的影像。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **專業提示：** 使用 `Format32bppPArgb` 可確保影像保留預乘 Alpha，這對 PNG 輸出非常理想。

### 步驟 2：建立 Graphics 物件

`Graphics` 物件提供在 Bitmap 上繪圖的方法。我們將背景清除為中性灰，以突顯變換後的形狀。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### 步驟 3：建立 GraphicsPath

`GraphicsPath` 讓您定義複雜形狀。此處我們加入一個位於 (300, 300)，寬 400 高 200 的橢圓。

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### 步驟 4：套用本地變換（使用矩陣旋轉形狀）

現在回答核心問題：**如何旋轉橢圓**。我們建立一個 `Matrix`，以橢圓中心 (500, 400) 為旋轉點，旋轉 45°，然後將矩陣套用到路徑上。

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **為什麼要以點旋轉？** 以形狀中心為旋轉點可避免它繞原點旋轉，呈現自然外觀。

### 步驟 5：繪製變換後的路徑

在套用變換後，我們使用寬度為 2 的藍色筆繪製路徑。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### 步驟 6：儲存變換後的影像（將圖形轉換為 PNG）

最後，我們將 Bitmap 持久化為 PNG 檔案。路徑結合您選擇的目錄與一個用於變換範例的子資料夾。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **注意：** 這行程式碼同時示範了如何 **將 Bitmap 儲存為 PNG**。`.png` 副檔名會自動觸發 Aspose.Drawing 的 PNG 編碼器，滿足 **將圖形轉換為 PNG** 的需求。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| **空白輸出影像** | 未清除圖形或筆色與背景相同 | 呼叫 `graphics.Clear` 並使用對比色，確保筆色可見。 |
| **旋轉失真** | 使用 `Rotate` 而非 `RotateAt` | 使用 `RotateAt` 並指定形狀的中心點。 |
| **檔案未儲存** | 目錄路徑無效或缺少寫入權限 | 確認目錄存在且應用程式具有寫入權限。 |
| **PNG 看起來模糊** | Bitmap 的 DPI 設定過低 | 使用較高解析度建立 Bitmap，或設定 `graphics.SmoothingMode = SmoothingMode.AntiAlias`。 |

## 常見問答

**問：** 我可以串接多個變換（例如先縮放再旋轉）嗎？  
**答：** 可以。建立單一 `Matrix`，依需求依序呼叫 `Scale`、`RotateAt`、`Translate` 等方法，最後以 `path.Transform(matrix);` 套用。

**問：** Aspose.Drawing 適合高效能渲染嗎？  
**答：** 絕對適合。此函式庫在速度與品質上皆經過最佳化，且避免了非 Windows 平台上 GDI+ 的限制。

**問：** 支援哪些其他變換類型？  
**答：** 除了旋轉，您還可以使用相同的 `Matrix` 類別執行平移、縮放與斜切。

**問：** 如何處理變換過程中的例外？  
**答：** 將繪圖程式碼包在 `try‑catch` 區塊中，檢查 `System.Drawing.Drawing2D` 例外。請參考官方的 [Aspose.Drawing 文件](https://reference.aspose.com/drawing/net/) 取得詳細的錯誤處理說明。

**問：** 我可以在購買前試用 Aspose.Drawing 嗎？  
**答：** 可以，透過 [free trial](https://releases.aspose.com/) 連結提供完整功能的免費試用版。

## 結論

透過本指南，您現在已掌握使用 Aspose.Drawing for .NET **旋轉橢圓** 以及 **將圖形轉換為 PNG** 以進行永久儲存的方法。同樣的模式亦可重複用於縮放、平移或斜切任何形狀，讓您在應用程式中打造豐富、互動的視覺元件。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-27  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose