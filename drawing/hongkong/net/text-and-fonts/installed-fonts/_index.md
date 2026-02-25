---
date: 2026-02-25
description: 學習如何使用 C# 建立點陣圖圖形並儲存 PNG 圖像，同時列出已安裝的字型、以字型繪製文字，以及使用 Aspose.Drawing for
  .NET 調整點陣圖解析度。
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 使用 C# 建立位圖圖形 – 在 Aspose.Drawing 中儲存 PNG 圖像並使用已安裝字型
url: /zh-hant/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 儲存 PNG 圖像並在 Aspose.Drawing 中使用已安裝字型

## Introduction

如果您需要 **save PNG image** 檔案，同時 **create bitmap graphics C#**，Aspose.Drawing for .NET 為您提供一個簡潔、跨平台的解決方案。在本教學中，我們將逐步說明如何列出已安裝的字型、顯示字型系列、從位圖建立圖形，以及使用字型繪製文字——最後將結果儲存為 PNG 圖像。完成後，您將擁有一段可重複使用的程式碼片段，能直接嵌入任何 .NET 專案。

## Quick Answers
- **這個教學會產生什麼？** 列出已安裝字型系列的 PNG 圖像。  
- **需要哪個函式庫？** Aspose.Drawing for .NET（不需要 System.Drawing.Common）。  
- **我可以使用自訂字型嗎？** 可以——只需將它們載入 `InstalledFontCollection`。  
- **輸出解析度可以調整嗎？** 當然可以——變更位圖尺寸或像素格式，即可 **adjust bitmap resolution C#**。  
- **執行程式碼需要授權嗎？** 評估期間可使用臨時授權；正式環境需購買完整授權。

## What is “save PNG image” in the context of Aspose.Drawing?
在 Aspose.Drawing 中，「save PNG image」指的是將您的繪圖表面（`Bitmap`）渲染為副檔名為 `.png` 的檔案。Aspose.Drawing 會為您處理編碼，只需呼叫 `bitmap.Save(...)` 並指定目標路徑即可。

## Why list installed fonts and show font families?
了解系統中有哪些字型，可讓您建立能依使用者環境自動調整的動態圖形。這在產生報告、證書或任何必須符合企業品牌且不想隨程式一起分發字型檔的視覺內容時，特別實用。

## How to create bitmap graphics C# with Aspose.Drawing?
以下是一個實用的逐步說明，完整展示如何 **create bitmap graphics C#**、使用字型繪製文字，以及在需要時調整位圖解析度。

## Prerequisites

- **Aspose.Drawing 函式庫** – 從 [Aspose Drawing 下載頁面](https://releases.aspose.com/drawing/net/) 下載最新版本。  
- **IDE** – Visual Studio、Rider 或任何相容 .NET 的編輯器。  
- **基本 C# 知識** – 您應該熟悉類別、物件與簡單迴圈。

## Import Namespaces
要使用字型與圖形，請在 C# 檔案的最上方匯入以下命名空間：

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step‑by‑Step Guide

### Step 1: Create a bitmap (the canvas)
首先，我們建立一個用來容納最終圖像的位圖。位圖的尺寸與像素格式決定了儲存 PNG 的品質，並讓您可以 **adjust bitmap resolution C#**。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Step 2: Create graphics from bitmap
接著，我們從位圖取得 `Graphics` 物件。此物件可讓我們在畫布上繪製形狀、文字與圖像。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Step 3: Set up brush and font (draw text with fonts)
我們需要一個畫刷來設定文字顏色，並建立一個定義字型、大小與樣式的 `Font` 物件。這就是執行 **draw text with fonts** 的地方。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Step 4: List installed fonts and show font families
現在，我們直接在位圖上顯示字型系列的數量以及前幾個名稱。此範例展示了 **list installed fonts** 與 **show font families** 的功能。

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Step 5: Save PNG image
最後，我們將位圖寫入磁碟，儲存為 PNG 檔案。這就是核心的 **save png image** 操作。

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tip:** 使用 `Path.Combine` 來組合檔案路徑，可避免不同作業系統的目錄分隔符問題。

## Common Issues and Solutions
| Issue | Cause | Fix |
|-------|-------|-----|
| **未顯示字型** | `InstalledFontCollection` 未填充（例如在沒有字型的無頭伺服器上執行）。 | 在伺服器上安裝所需字型，或將自訂字型嵌入應用程式中。 |
| **儲存的檔案損毀** | 像素格式不正確或缺少寫入權限。 | 確認目標資料夾存在且應用程式具有寫入權限；保留 `Format32bppPArgb`。 |
| **文字模糊** | DPI 設定過低。 | 增加位圖尺寸或設定 `graphics.SmoothingMode = SmoothingMode.AntiAlias`。 |

## Frequently Asked Questions

**Q: 我可以使用未安裝在機器上的自訂字型嗎？**  
A: 可以。將字型檔載入 `PrivateFontCollection`，再從該集合建立 `Font`。

**Q: 我要如何處理與字型相關的例外狀況？**  
A: 在 `try/catch` 區塊中包住字型建立程式，並檢查 `ArgumentException` 以判斷缺少的字型系列。

**Q: Aspose.Drawing 適用於 Web 應用程式嗎？**  
A: 完全適用。此函式庫可在 ASP.NET Core、Azure Functions 以及其他伺服器端環境中使用。

**Q: 我可以變更文字顏色或樣式嗎？**  
A: 可以。使用不同的 `Brush` 類型（例如 `LinearGradientBrush`）並修改 `FontStyle` 列舉。

**Q: 我可以從哪裡取得測試用的臨時授權？**  
A: 從 [Aspose 臨時授權頁面](https://purchase.aspose.com/temporary-license/) 下載試用授權。

## Conclusion

透過上述步驟，您已學會如何使用 Aspose.Drawing for .NET **save PNG image** 檔案，並動態 **list installed fonts**、**show font families**、**create graphics from bitmap** 以及 **draw text with fonts**。現在您也了解如何 **create bitmap graphics C#**、調整位圖解析度，並在需要時加入自訂字型。歡迎自行嘗試其他字型、顏色與位圖尺寸，以符合專案的視覺需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-02-25  
**測試版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose