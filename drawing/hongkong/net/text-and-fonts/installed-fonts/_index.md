---
date: 2025-12-06
description: 學習如何在列出已安裝字型、顯示字型系列、從點陣圖建立圖形以及使用 Aspose.Drawing for .NET 繪製文字時，儲存 PNG
  圖像檔案。
language: zh-hant
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 在 Aspose.Drawing 中儲存 PNG 圖像並使用已安裝字型
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 儲存 PNG 圖像並在 Aspose.Drawing 中使用已安裝字型

## 簡介

如果您需要 **save PNG image** 檔案，同時顯示機器上已安裝字型的資訊，Aspose.Drawing for .NET 為您提供一個乾淨、跨平台的解決方案。在本教學中，我們將逐步說明列出已安裝字型、顯示字型族、從位圖建立圖形，以及使用字型繪製文字——最終將結果儲存為 PNG 圖像。完成後，您將擁有一段可重複使用的程式碼片段，能直接嵌入任何 .NET 專案。

## 快速答覆
- **本教學會產生什麼？** 列出已安裝字型族的 PNG 圖像。  
- **需要哪個函式庫？** Aspose.Drawing for .NET（不需要 System.Drawing.Common）。  
- **可以使用自訂字型嗎？** 可以——只需將它們載入 `InstalledFontCollection`。  
- **輸出解析度可調整嗎？** 當然可以——變更位圖尺寸或像素格式即可。  
- **執行程式碼需要授權嗎？** 評估時可使用臨時授權；正式環境需購買完整授權。

## 在 Aspose.Drawing 中「save PNG image」是什麼意思？

儲存 PNG 圖像即是將您的繪圖表面（`Bitmap`）渲染為副檔名為 `.png` 的檔案。Aspose.Drawing 會為您處理編碼，只需呼叫 `bitmap.Save(...)` 並指定路徑即可。

## 為什麼要列出已安裝字型並顯示字型族？

了解可用的字型可讓您建立能因應最終使用者環境而變化的動態圖形。這對於產生報告、證書或任何必須符合企業品牌而不需隨附字型檔案的視覺內容特別有用。

## 先決條件

- **Aspose.Drawing 函式庫** – 從 [Aspose Drawing 下載頁面](https://releases.aspose.com/drawing/net/) 取得最新版本。  
- **IDE** – Visual Studio、Rider 或任何相容 .NET 的編輯器。  
- **基本 C# 知識** – 您應該熟悉類別、物件與簡單迴圈。

## 匯入命名空間

若要使用字型與圖形，請在 C# 檔案的頂部匯入以下命名空間：

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 步驟說明

### 步驟 1：建立位圖（畫布）

首先，我們建立一個位圖來容納最終圖像。位圖的尺寸與像素格式決定儲存 PNG 的品質。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步驟 2：從位圖建立 Graphics 物件

接著，我們從位圖取得 `Graphics` 物件。此物件可讓我們在畫布上繪製形狀、文字與影像。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### 步驟 3：設定筆刷與字型（使用字型繪製文字）

我們需要一支筆刷來設定文字顏色，並建立 `Font` 物件以定義字型、大小與樣式。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### 步驟 4：列出已安裝字型並顯示字型族

現在，我們直接在位圖上顯示字型族的數量與前幾個名稱。此範例示範 **list installed fonts** 與 **show font families** 功能。

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### 步驟 5：儲存 PNG 圖像

最後，我們將位圖寫入磁碟，儲存為 PNG 檔案。這就是核心的 **save png image** 操作。

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **專業提示：** 使用 `Path.Combine` 組合檔案路徑，可避免不同作業系統的目錄分隔符問題。

## 常見問題與解決方案
| Issue | Cause | Fix |
|-------|-------|-----|
| **未顯示字型** | `InstalledFontCollection` 未被填充（例如在無字型的無頭伺服器上執行）。 | 在伺服器上安裝所需字型，或在應用程式中嵌入自訂字型。 |
| **儲存的檔案損毀** | 像素格式不正確或缺少寫入權限。 | 確保目標資料夾存在且應用程式具有寫入權限；保留 `Format32bppPArgb`。 |
| **文字模糊** | DPI 設定過低。 | 增大位圖尺寸或設定 `graphics.SmoothingMode = SmoothingMode.AntiAlias`。 |

## 常見問與答

**問：我可以使用未安裝在機器上的自訂字型嗎？**  
**答：** 可以。將字型檔載入 `PrivateFontCollection`，再從該集合建立 `Font`。

**問：如何處理與字型相關的例外？**  
**答：** 在 `try/catch` 區塊中包裹字型建立，並檢查 `ArgumentException` 以判斷缺少的字型族。

**問：Aspose.Drawing 適合用於 Web 應用程式嗎？**  
**答：** 當然適合。此函式庫可在 ASP.NET Core、Azure Functions 以及其他伺服器端環境中使用。

**問：我可以變更文字顏色或樣式嗎？**  
**答：** 可以。使用不同的 `Brush` 類型（例如 `LinearGradientBrush`），並修改 `FontStyle` 列舉。

**問：在哪裡可以取得測試用的臨時授權？**  
**答：** 從 [Aspose 臨時授權頁面](https://purchase.aspose.com/temporary-license/) 下載試用授權。

## 結論

透過上述步驟，您已學會如何使用 Aspose.Drawing for .NET **save PNG image** 檔案，動態 **list installed fonts**、**show font families**、**create graphics from bitmap**，以及 **draw text with fonts**。歡迎自行嘗試其他字型、顏色與位圖尺寸，以符合專案的視覺需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-06  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose