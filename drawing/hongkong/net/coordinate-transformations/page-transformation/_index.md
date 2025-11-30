---
date: 2025-11-30
description: 學習如何使用 Aspose.Drawing for .NET 應用座標系統轉換、繪製矩形位圖以及轉換頁面。
language: zh-hant
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET 中的坐標系統轉換（頁面轉換）
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET 中的座標系統轉換（頁面轉換）

## 簡介

歡迎！在本教學中，您將學會 **如何在頁面上執行座標系統轉換**，使用 Aspose.Drawing for .NET。無論您需要 **draw rectangle bitmap** 物件、縮放圖形，或只是將頁面單位映射到裝置單位，以下步驟將清晰、簡潔地指引您完成整個流程，且可直接複製貼上至您的專案。

## 快速答覆
- **繪圖的主要類別是什麼？** `Graphics` 來自 Aspose.Drawing。
- **如何設定頁面單位？** 使用 `graphics.PageUnit = GraphicsUnit.Inch;`。
- **我可以在已轉換的頁面上繪製矩形嗎？** 可以——建立 `Pen` 後呼叫 `DrawRectangle`。
- **輸出檔案儲存在哪裡？** 儲存於您在 `bitmap.Save` 中指定的資料夾。
- **商業使用是否需要授權？** 商業使用需具有效的 Aspose.Drawing 授權。

## 什麼是座標系統轉換？

**座標系統轉換** 會改變邏輯頁面座標（如英吋或毫米）映射到實體裝置座標（像素）的方式。透過調整轉換，您可以控制所有繪圖操作的縮放、旋轉與平移，讓設計的圖形具備解析度無關性。

## 為什麼要使用 Aspose.Drawing 進行頁面轉換？

- **完整 .NET 相容性** – 支援 .NET Framework、.NET Core 以及 .NET 5/6。
- **豐富的圖形 API** – 提供與 System.Drawing.Common 相同的功能，且無平台限制。
- **簡易的單位處理** – 只需一個屬性即可在英吋、毫米、點等單位間切換。
- **高品質輸出** – 可產生 PNG、JPEG、BMP 等格式，並具精確控制。

## 先決條件

在開始之前，請確保您已具備：

- **Aspose.Drawing 程式庫** – 從官方網站[此處](https://releases.aspose.com/drawing/net/)下載最新版本。
- **開發環境** – Visual Studio（任何版本）或其他 .NET IDE。
- **寫入權限** – 您機器上有可寫入的資料夾，用於儲存轉換後的影像（請將程式碼中的 `"Your Document Directory"` 替換為實際路徑）。

現在我們已就緒，讓我們逐步說明每個步驟。

## 匯入命名空間

首先，將所需的命名空間引入範圍：

```csharp
using System.Drawing;
```

> *為什麼這很重要*：`System.Drawing` 包含我們在整個教學中會使用的 `Bitmap`、`Graphics`、`Pen` 與顏色結構。

## 步驟 1：建立 Bitmap

建立一個空白畫布，以容納轉換後的繪圖。我們指定 **1000 × 800 像素** 的大小，並使用支援 Alpha 透明度的像素格式。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> 此 Bitmap 作為繪圖表面。選用的像素格式（`Format32bppPArgb`）可確保具有預乘 Alpha 的高品質渲染。

## 步驟 2：建立 Graphics 物件

`Graphics` 物件提供繪圖方法（線條、形狀、文字）。我們從剛才建立的 Bitmap 取得它。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> `Graphics` 物件是所有渲染操作的核心；它會遵循我們接下來設定的轉換設定。

## 步驟 3：清除畫布

在繪製任何內容之前，先將畫布清除為中性背景色（本例為灰色）。此步驟同時示範如何以單一顏色填滿整個 Bitmap。

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## 步驟 4：設定轉換（套用頁面轉換）

在此 **套用頁面轉換**，將 `PageUnit` 設為英吋。這告訴圖形引擎將所有後續座標解讀為英吋，而非像素。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *提示*：變更 `PageUnit` 是一種簡單的 **how to transform page** 方式，無需手動計算像素值。

## 步驟 5：繪製矩形（Draw rectangle bitmap）

現在繪製一個尺寸為 **1 英吋 × 1 英吋**、位置在 (1, 1) 英吋的矩形。`Pen` 寬度設定為 `0.1f` 英吋，線條細而可見。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> 這示範了在套用轉換後 **draw rectangle bitmap** 的效果——注意矩形尺寸是以英吋定義，而非像素。

## 步驟 6：儲存影像

最後，將轉換後的 Bitmap 持久化至磁碟。請將 `"Your Document Directory"` 替換為您機器上的實際資料夾路徑。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> 輸出檔案 (`PageTransformation_out.png`) 會包含使用先前設定的座標系統轉換所繪製的矩形。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| **影像顯示空白** | 畫布未清除或繪圖超出可見範圍。 | 核對 `graphics.PageUnit` 與座標值；確保矩形位於 Bitmap 範圍內。 |
| **縮放不正確** | 使用了錯誤的 `GraphicsUnit`。 | 再次確認 `graphics.PageUnit` 與您預期的單位相符（例如 `GraphicsUnit.Inch`）。 |
| **檔案路徑錯誤** | 目錄不存在或包含無效字元。 | 事先建立目標資料夾，或使用 `Path.Combine` 安全組合路徑。 |

## 常見問答

**Q: 我可以免費使用 Aspose.Drawing 嗎？**  
A: Aspose.Drawing 提供可於[此處](https://releases.aspose.com/)取得的免費試用版。

**Q: 哪裡可以找到 Aspose.Drawing 的詳細文件？**  
A: 文件可於[此處](https://reference.aspose.com/drawing/net/)取得。

**Q: 如何取得 Aspose.Drawing 的支援？**  
A: 請前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/diagram/17)取得支援。

**Q: Aspose.Drawing 是否提供臨時授權？**  
A: 是的，您可於[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

**Q: 哪裡可以購買 Aspose.Drawing？**  
A: 您可於[此處](https://purchase.aspose.com/buy)購買 Aspose.Drawing。

## 結論

您現在已學會 **套用座標系統轉換**、**draw rectangle bitmap** 物件，並 **儲存結果**，使用 Aspose.Drawing for .NET。這些基礎讓您能建立解析度無關的圖形，適用於報表、UI 元素或任何需要精確尺寸的情境。可嘗試其他 `GraphicsUnit` 值（如 `Millimeter` 或 `Point`），觀察它們對繪圖的影響。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-11-30  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose