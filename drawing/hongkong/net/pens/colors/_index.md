---
date: 2026-02-22
description: 學習如何在 Aspose.Drawing for .NET 中設定筆的顏色、繪製彩色線條，並使用簡單的程式碼範例儲存 PNG 圖像。
linktitle: Working with Colors in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何在 Aspose.Drawing for .NET 中設定筆的顏色
url: /zh-hant/net/pens/colors/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing 中設定筆刷顏色

## 介紹

歡迎閱讀本步驟教學，了解在 Aspose.Drawing for .NET 繪圖時如何 **設定筆刷顏色**。本教學將教您建立 graphics 物件、繪製彩色線條，並 **儲存 PNG 影像** 檔案——全部以清晰、實務的程式碼範例示範。無論您是開發桌面工具或產生圖表的 Web 服務，掌握筆刷顏色都是製作專業圖形的關鍵。

## 快速回答
- **繪圖的主要類別是什麼？** `Graphics` 由 `Bitmap` 建立。  
- **如何變更筆刷的顏色？** 使用 `Color.FromKnownColor` 或 `Color.FromArgb`。  
- **建議使用哪種格式作為無損輸出？** PNG（`.png`）。  
- **開發是否需要授權？** 可取得臨時授權以供評估。  
- **可以在 ASP.NET Core 中使用嗎？** 可以，Aspose.Drawing 支援 .NET Core 及 .NET 5 以上。

## 什麼是 Aspose.Drawing 中的「設定筆刷顏色」？

設定筆刷顏色即在繪圖前將 `Color` 值指派給 `Pen` 物件。顏色決定線條、形狀或文字在畫布上的呈現方式。Aspose.Drawing 與熟悉的 System.Drawing API 保持一致，您可以使用 `Color.FromKnownColor`、`Color.FromArgb` 或預定義的 `Color` 屬性。

## 為什麼使用 Aspose.Drawing 進行顏色操作？

* **跨平台支援** – 在 Windows、Linux 與 macOS 上皆可使用，無 System.Drawing.Common 的限制。  
* **完整 .NET 相容性** – 可無縫整合至 .NET 6、.NET Core 與 .NET Framework 專案。  
* **豐富的顏色 API** – 輕鬆建立自訂 ARGB 顏色、已知顏色與漸層筆刷。  
* **高品質 PNG 輸出** – 非常適合 Web 圖形、報表與縮圖。

## 前置條件

在開始撰寫程式碼前，請確保您已具備：

1. **Aspose.Drawing Library** – 從官方網站 **[此處](https://releases.aspose.com/drawing/net/)** 下載並安裝。  
2. **.NET 開發環境** – Visual Studio、VS Code 或您慣用的任何 IDE。  
3. **基本的 C# 知識** – 熟悉類別、物件與命名空間。

## 匯入命名空間

在 C# 檔案中匯入提供 Aspose.Drawing 繪圖基元的命名空間。

```csharp
using System.Drawing;
```

## 步驟 1：建立 Bitmap（畫布）

`Bitmap` 代表我們將要繪製的像素緩衝區。此處建立一個 1000 × 800、32 位元 ARGB 格式的畫布。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 2：建立 Graphics 物件

`Graphics` 物件是繪圖表面，讓您能在 bitmap 上繪製形狀、文字與影像。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 3：使用藍色筆刷繪製第一條線

我們使用 `Color.FromKnownColor` **設定筆刷顏色** 為藍色，筆寬設定為 2 像素。

```csharp
Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawLine(bluePen, 100, 100, 900, 100);
```

## 步驟 4：使用自訂紅色筆刷繪製線條

此範例示範如何使用自訂 ARGB 值 **繪製彩色線條**，讓您完整掌控透明度與色調。

```csharp
Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
graphics.DrawLine(redPen, 100, 200, 900, 200);
```

## 步驟 5：將影像儲存為 PNG

最後，我們將 **儲存 PNG 影像** 至指定資料夾。請依您的專案輸出目錄調整路徑。

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|-------|--------|-----|
| **圖像顯示為空白** | 在儲存前未刷新 Graphics | 呼叫 `graphics.Dispose();` 或將 `Graphics` 包在 `using` 區塊中。 |
| **顏色不正確** | 使用錯誤的 enum 呼叫 `FromKnownColor` | 確認 enum 值，或使用 `FromArgb` 以取得精確控制。 |
| **檔案路徑錯誤** | 目錄無效或缺少權限 | 確保目標資料夾存在且應用程式具有寫入權限。 |

## 常見問答

**Q: 我可以將 Aspose.Drawing 與其他 .NET 函式庫一起使用嗎？**  
A: 可以，Aspose.Drawing 可無縫整合其他 .NET 函式庫，提供多功能的圖形操作環境。

**Q: 如何取得 Aspose.Drawing 的臨時授權？**  
A: 您可在 **[此處](https://purchase.aspose.com/temporary-license/)** 取得臨時授權，讓您探索 Aspose.Drawing 的全部功能。

**Q: Aspose.Drawing 是否支援 PNG 以外的影像格式？**  
A: 是的，Aspose.Drawing 支援多種影像格式，包括 JPEG、GIF、BMP 等。請參閱文件取得完整清單。

**Q: 我可以在網頁開發中使用 Aspose.Drawing 嗎？**  
A: 當然可以！Aspose.Drawing 多功能且可用於桌面與網頁應用程式，為您的網站加入動態圖形功能。

**Q: 是否提供 Aspose.Drawing 的免費試用？**  
A: 是的，您可在 **[此處](https://releases.aspose.com/drawing/net/)** 取得免費試用，先體驗 Aspose.Drawing 的功能再決定是否購買。

## 結論

在本教學中，我們說明了如何 **設定筆刷顏色**、**繪製彩色線條**、**建立 graphics 物件**，以及 **將結果儲存為 PNG**，全部使用 Aspose.Drawing for .NET。這些基礎為更進階的情境鋪路，例如繪製形狀、渲染文字與動態產生圖表。如遇到問題，請參考 Aspose.Drawing 的 **[文件](https://reference.aspose.com/drawing/net/)** 與 **[支援論壇](https://forum.aspose.com/c/drawing/44)**，那裡有豐富的解答。

---

**最後更新：** 2026-02-22  
**測試版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}