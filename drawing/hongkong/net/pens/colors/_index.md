---
date: 2026-09-18
description: 了解如何在 Aspose.Drawing（適用於 .NET）中設定筆的顏色、繪製彩色線條，並使用簡單程式碼範例儲存 PNG 圖片。
keywords:
- set pen color
- save png image
- cross platform drawing
- draw lines with pen
- high quality png
lastmod: 2026-09-18
linktitle: 在 Aspose.Drawing 中使用顏色
og_description: 在 Aspose.Drawing（適用於 .NET）中設定筆的顏色，製作高品質 PNG 圖片。了解跨平台繪圖、使用筆繪製線條，並在數分鐘內儲存
  PNG 圖片。
og_image_alt: Screenshot of code setting pen color and saving a PNG with Aspose.Drawing
og_title: 在 Aspose.Drawing 中設定筆的顏色 – 高品質 PNG 輸出的指南
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored
    lines, and save PNG images with simple code examples.
  headline: How to set pen color in Aspose.Drawing
  type: TechArticle
- description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored
    lines, and save PNG images with simple code examples.
  name: How to set pen color in Aspose.Drawing
  steps:
  - name: '**Aspose.Drawing Library** – download and install from the official site
      **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.'
    text: '**Aspose.Drawing Library** – download and install from the official site
      **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.'
  - name: '**A .NET development environment** – Visual Studio, VS Code, or any IDE
      you prefer.'
    text: '**A .NET development environment** – Visual Studio, VS Code, or any IDE
      you prefer.'
  - name: '**Basic C# knowledge** – familiarity with classes, objects, and namespaces.'
    text: '**Basic C# knowledge** – familiarity with classes, objects, and namespaces.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing integrates smoothly with other .NET libraries, providing
      a versatile environment for graphic manipulation.
    question: Can I use Aspose.Drawing with other .NET libraries?
  - answer: You can get a temporary license **[Aspose temporary license page](https://purchase.aspose.com/temporary-license/)**,
      allowing you to explore the full potential of Aspose.Drawing.
    question: How can I obtain a temporary license for Aspose.Drawing?
  - answer: Yes, Aspose.Drawing supports JPEG, GIF, BMP, TIFF, and more. Refer to
      the documentation for a complete list.
    question: Does Aspose.Drawing support image formats other than PNG?
  - answer: Absolutely! Aspose.Drawing works in both desktop and web applications,
      enabling dynamic graphic generation on servers.
    question: Can I use Aspose.Drawing for web development?
  - answer: Yes, you can explore a free trial **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**,
      letting you evaluate the library before purchasing.
    question: Is there a free trial available for Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- .NET graphics
- pen color
- PNG output
title: 如何在 Aspose.Drawing 中設定筆的顏色
url: /zh-hant/net/pens/colors/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing 中設定筆的顏色

## 介紹

在本教學中，您將學習如何在 .NET 的 Aspose.Drawing 中**設定筆的顏色**、建立圖形畫布、繪製彩色線條，以及**儲存 PNG 圖像**檔案以獲得高品質。無論您是開發桌面工具、報表服務，或是產生圖表的 Web API，控制筆的顏色都是打造專業外觀圖形的關鍵。

## 快速解答
- **繪圖的主要類別是什麼？** `Graphics` 由 `Bitmap` 建立。
- **如何變更筆的顏色？** 使用 `Color.FromKnownColor` 或 `Color.FromArgb`。
- **建議使用哪種格式以獲得無損輸出？** PNG（`.png`）。
- **開發時是否需要授權？** 可取得臨時授權以供評估。
- **可以在 ASP.NET Core 中使用嗎？** 可以，Aspose.Drawing 支援 .NET Core 及 .NET 5+。

## 在 Aspose.Drawing 中「設定筆的顏色」是什麼？

設定筆的顏色是指在任何繪圖操作之前，將 `Color` 值指派給 `Pen` 物件。所選顏色會影響線條、形狀與文字筆畫的色調、透明度與粗細，讓您能精確控制最終影像的視覺效果。

## 為何使用 Aspose.Drawing 進行顏色操作？

Aspose.Drawing 提供**跨平台繪圖**，可在 Windows、Linux 與 macOS 上執行，且不受 System.Drawing.Common 的限制。它支援**高品質 PNG**輸出（最高 32 位 ARGB），並提供豐富的顏色 API，包括 50 多種已知顏色與完整的 ARGB 自訂功能。此函式庫能處理上百頁的影像，同時將記憶體使用量控制在 50 MB 以下，適合伺服器端產生圖形。

## 前置條件

1. **Aspose.Drawing 函式庫** – 從官方網站下載並安裝 **[Aspose.Drawing 下載頁面](https://releases.aspose.com/drawing/net/)**。  
2. **.NET 開發環境** – Visual Studio、VS Code 或您偏好的任何 IDE。  
3. **基本的 C# 知識** – 熟悉類別、物件與命名空間。

## 匯入命名空間

`Aspose.Drawing` 命名空間是核心函式庫，提供所有與繪圖相關的型別，如 `Bitmap`、`Graphics`、`Pen` 與 `Color`，讓開發者能在跨平台環境中建立、操作與呈現影像，而不必依賴 System.Drawing.Common。

```csharp
using System.Drawing;
```

## 步驟 1：建立位圖（畫布）

`Bitmap` 類別代表可在記憶體中的像素緩衝區，可供繪圖使用；它支援多種像素格式，包括保留完整色深與透明度的 32 位 ARGB，這對高品質 PNG 輸出至關重要。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 2：建立 Graphics 物件

`Graphics` 物件作為與 `Bitmap` 相關聯的繪圖表面，提供 `DrawLine`、`DrawRectangle`、`DrawString` 等方法，將形狀、線條與文字繪製到底層影像緩衝區。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 3：使用藍色筆繪製線條（第一條彩色線）

`Pen` 類別定義線條與輪廓的屬性，包括顏色、寬度、虛線樣式與對齊方式，`Graphics` 方法會使用它來在畫布上描繪形狀與路徑。

```csharp
Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawLine(bluePen, 100, 100, 900, 100);
```

## 步驟 4：使用自訂紅色筆繪製線條

此範例示範如何使用自訂 ARGB 值**繪製彩色線條**，讓您完全掌控透明度與精確色階。

```csharp
Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
graphics.DrawLine(redPen, 100, 200, 900, 200);
```

## 步驟 5：將影像儲存為 PNG

最後，我們將**PNG 影像**儲存至指定資料夾。PNG 能保留透明度與色彩忠實度，是網頁圖形與報表的首選格式。

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| **影像顯示空白** | Graphics 未在儲存前刷新 | 呼叫 `graphics.Dispose();` 或將 `Graphics` 包在 `using` 區塊中。 |
| **顏色不正確** | 使用 `FromKnownColor` 時傳入錯誤的列舉值 | 核對列舉值，或使用 `FromArgb` 以取得精確控制。 |
| **檔案路徑錯誤** | 目錄不存在或缺少權限 | 確認目標資料夾已建立，且應用程式具備寫入權限。 |

## 常見問答

**Q: 可以將 Aspose.Drawing 與其他 .NET 函式庫一起使用嗎？**  
A: 可以，Aspose.Drawing 能順暢整合其他 .NET 函式庫，提供多元的圖形操作環境。

**Q: 如何取得 Aspose.Drawing 的臨時授權？**  
A: 您可以前往 **[Aspose 臨時授權頁面](https://purchase.aspose.com/temporary-license/)** 取得臨時授權，讓您探索 Aspose.Drawing 的全部功能。

**Q: Aspose.Drawing 是否支援除 PNG 之外的影像格式？**  
A: 支援，Aspose.Drawing 可處理 JPEG、GIF、BMP、TIFF 等多種格式，完整清單請參考文件說明。

**Q: 可以在 Web 開發中使用 Aspose.Drawing 嗎？**  
A: 當然可以！Aspose.Drawing 可在桌面與 Web 應用程式中使用，讓伺服器端動態產生圖形成為可能。

**Q: Aspose.Drawing 有提供免費試用嗎？**  
A: 有，您可以前往 **[Aspose.Drawing 下載頁面](https://releases.aspose.com/drawing/net/)** 取得免費試用版，先行評估函式庫功能再決定購買。

## 結論

本指南說明了如何**設定筆的顏色**、**繪製彩色線條**、**建立 Graphics 物件**，以及**將結果儲存為高品質 PNG**，全部使用 Aspose.Drawing for .NET。掌握這些基礎後，您即可進一步探索繪製形狀、渲染文字與動態產生圖表等進階情境。若遇到問題，請參考 Aspose.Drawing 的 **[文件說明](https://reference.aspose.com/drawing/net/)** 與 **[支援論壇](https://forum.aspose.com/c/drawing/44)**，那裡有豐富的解答與範例。

---

**最後更新：** 2026-09-18  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [如何在 Aspose.Drawing 中繪製多條線時將位圖儲存為 PNG](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [如何在 Aspose.Drawing .NET 中使用筆合併路徑](/drawing/net/pens/)
- [如何在 Aspose.Drawing 中使用抗鋸齒提升影像品質](/drawing/net/rendering/antialiasing/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}