---
date: 2026-02-25
description: 學習如何使用 Aspose.Drawing for .NET 繪製文字並建立動態文字圖像。本分步指南會示範如何將文字加入位圖、在圖像上繪製字串，以及將位圖儲存為
  PNG。
linktitle: How to Draw Text with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 使用 Aspose.Drawing for .NET 繪製文字
url: /zh-hant/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspise.Drawing for .NET 繪製文字

## 簡介

在本分步指南中，您將學習 **如何在圖像上繪製文字**，使用 Aspose.Drawing for .NET。無論您需要建立 *動態文字圖像*、在現有位圖上加入文字，或是使用自訂字型產生圖形，本教學都會逐步說明所有細節，讓您在數分鐘內即可開始繪製文字。

## 快速解答
- **使用的函式庫？** Aspose.Drawing for .NET  
- **主要任務？** 在圖像上繪製文字（create image with text）  
- **關鍵方法？** `Graphics.DrawString`（draw string on image）  
- **輸出格式？** PNG（save bitmap as PNG）  
- **先決條件？** .NET 開發環境與 Aspose.Drawing 函式庫  

## 什麼是使用 Aspose.Drawing 繪製文字？

Aspose.Drawing 提供完整受管理的 API，與傳統 GDI+ 模型相同，同時加入跨平台支援。它讓您在不依賴 System.Drawing.Common 的情況下，渲染高品質的文字、形狀與圖像。

## 為什麼使用 Aspose.Drawing 為圖像加入文字？

- **跨平台可靠性** – 可在 Windows、Linux 與 macOS 上運作。  
- **進階渲染** – 具備抗鋸齒與次像素文字平滑，確保輸出清晰。  
- **無外部相依性** – 函式庫已封裝所有建立 *create image with text* 所需的元件。

## 先決條件

在開始之前，請確保您已具備：

- **Aspose.Drawing for .NET** – 從 [Aspose.Drawing 文件](https://reference.aspose.com/drawing/net/) 下載。  
- **.NET IDE**，如 Visual Studio 或 VS Code。

## 匯入命名空間

首先匯入所需的命名空間：

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 步驟 1：建立 Bitmap 與 Graphics 物件

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

此處我們建立一個將保存最終圖片的 `Bitmap`，以及一個允許我們在其上繪圖的 `Graphics` 物件。抗鋸齒提示可確保文字平滑。

## 步驟 2：設定 Brush、Pen 與 Font

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** 定義文字顏色。  
- **Pen** 稍後用於在文字周圍繪製矩形（可選）。  
- **Font** 指定字型、大小與樣式，用於 *draw string on image* 操作。

## 步驟 3：定義文字與矩形

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` 決定文字的放置位置。請依需求調整座標與尺寸以符合版面配置。

## 步驟 4：繪製矩形與文字

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

首先以藍色矩形勾勒區域，接著透過呼叫 `DrawString` **將文字加入位圖**。這就是在圖像上 *drawing text* 的核心步驟。

## 步驟 5：儲存結果

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

圖像會以 PNG 檔案儲存，滿足 *save bitmap as PNG* 的需求。請將佔位路徑替換為實際欲存放檔案的資料夾路徑。

## 常見使用情境

- **產生具個人化姓名的證書**。  
- **為網站相簿建立帶有浮水印的縮圖**。  
- **建構包含標籤或註解的動態圖表**。

## 故障排除與技巧

- **找不到字型？** 確認該字型已安裝於主機，或使用私有字型集合。  
- **文字被裁切？** 增大矩形尺寸或縮小字型大小。  
- **效能顧慮？** 如有可能，重複使用同一個 `Graphics` 物件進行多次繪圖操作。

## 常見問題

### Q1：我可以在 Aspose.Drawing for .NET 中使用自訂字型嗎？

A1：可以，您可以在程式碼中建立 `Font` 物件時指定自訂字型。

### Q2：如何為文字加入粗體或斜體等效果？

A2：調整 `Font` 物件的 `FontStyle` 屬性。例如，使用 `FontStyle.Bold` 取得粗體文字。

### Q3：Aspose.Drawing 是否相容於 .NET Core？

A3：是的，Aspose.Drawing 支援 .NET Core，讓您可在跨平台應用程式中使用。

### Q4：我可以在現有圖像上繪製文字嗎？

A4：當然可以！使用 `Bitmap.FromFile()` 載入現有圖像，然後繼續執行文字繪製步驟。

### Q5：是否有 Aspose.Drawing 的社群論壇可供支援？

A5：有，您可在 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 獲得支援與討論問題。

## 常見問答

**Q：如何將輸出格式改為 JPEG？**  
A：在 `Save` 方法中將 `.png` 副檔名改為 `.jpg`，並可選擇指定 `ImageCodecInfo` 以設定 JPEG 品質。

**Q：我可以繪製多行文字嗎？**  
A：可以，在字串中加入換行字元 (`\n`) 或使用帶有 `FormatFlags.LineLimit` 的 `StringFormat`。

**Q：有沒有方法在繪製前測量文字大小？**  
A：使用 `Graphics.MeasureString` 可取得渲染文字的精確尺寸。

**Q：Aspose.Drawing 是否支援 Unicode 字元？**  
A：當然支援。提供包含所需字形的字型，函式庫即可正確渲染。

**Q：測試時使用的 Aspose.Drawing 版本為何？**  
A：範例已使用 Aspose.Drawing 24.11 for .NET 進行測試。

---

**最後更新：** 2026-02-25  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}