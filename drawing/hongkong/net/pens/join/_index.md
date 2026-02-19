---
date: 2026-02-19
description: 學習如何在 Aspose.Drawing 中使用筆繪製路徑並連接路徑，然後使用簡單的 C# 程式碼將圖像儲存為 PNG。
linktitle: Joining Paths with Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何在 Aspose.Drawing 中使用筆繪製路徑並連接路徑
url: /zh-hant/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing 中使用筆繪製路徑並合併路徑

## 簡介

歡迎來到 **Aspose.Drawing for .NET** 的世界！在本教學中，您將學會 **如何繪製路徑** 物件、使用不同的 line‑join 樣式將它們合併，最後 **將影像儲存為 PNG**。無論您是在建構報表工具、設計編輯器，或只是需要清晰的向量圖形，掌握使用筆繪製路徑的技巧，都能讓您對視覺輸出擁有精細的控制。

## 快速答案
- **「draw path」是什麼意思？** 它會建立向量基礎的線條或形狀定義，供 `Graphics` 物件渲染。  
- **有哪些線條連接方式可用？** `Bevel`、`Miter`、`Round` 與 `BevelClipped`。  
- **我可以將結果匯出為 PNG 嗎？** 可以——使用 `Bitmap.Save` 並指定 `.png` 副檔名。  
- **需要授權嗎？** 試用版可用於評估；正式環境需購買商業授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.6 以上、 .NET Core 3.1 以上，以及 .NET 6 以上。

## 什麼是 Aspose.Drawing 中的「draw path」？

繪製路徑指的是建立一個 `GraphicsPath`，其中包含一系列線條、曲線或形狀。路徑建好之後，您使用 `Pen` 在 `Graphics` 表面上繪製。相較於逐條繪製線條，這種方式更具彈性，因為您可以對整個形狀套用變換、裁剪以及不同的連接樣式。

## 為什麼使用 Aspose.Drawing 來合併路徑？

- **完整的 .NET 相容性** – 可在 Windows、Linux 與 macOS 上執行。  
- **豐富的線條連接選項** – 只需設定一個屬性即可產生斜角、圓角或斜接角。  
- **高品質點陣輸出** – 可直接儲存為 PNG、JPEG、BMP 等格式，無需額外轉換。  
- **無 GDI+ 限制** – 適用於 `System.Drawing.Common` 受限的伺服器端渲染情境。

## 先決條件

在開始編寫程式碼之前，請確保您已具備以下項目：

1. **Aspose.Drawing 程式庫** – 前往 **[此處](https://releases.aspose.com/drawing/net/)** 下載。  
2. **.NET 開發環境** – Visual Studio、VS Code，或任何支援 C# 的 IDE。

現在一切就緒，讓我們一步步操作。

## 匯入命名空間

在檔案頂部加入必要的命名空間，讓編譯器知道圖形類別的所在位置：

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 步驟 1：建立 Bitmap 與 Graphics 物件

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

我們先建立一個 1000 × 800 像素的空白畫布 (`Bitmap`)，再取得一個 `Graphics` 物件，用來執行繪圖指令。

## 步驟 2：定義 DrawPath 方法

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

此輔助方法封裝了繪圖邏輯：

- **Pen** – 設定顏色與粗細（30 像素）。  
- **GraphicsPath** – 定義兩條相連的線段，形成「L」形狀。  
- **LineJoin** – 控制兩條線之間角落的呈現方式（`Bevel`、`Round` 等）。

您可以傳入任意 `LineJoin` 值來觀察視覺差異。

## 步驟 3：使用 Bevel LineJoin 合併路徑

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

使用 `LineJoin.Bevel` 會在兩條線相交處產生平坦的角落。

## 步驟 4：使用 Round LineJoin 合併路徑

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

`LineJoin.Round` 會產生平滑的圓角——非常適合想要更精緻外觀的情況。

## 步驟 5：將結果儲存為 PNG

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

`Save` 呼叫會將 bitmap 以 PNG 格式寫入檔案。請依您的環境調整儲存路徑。

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方式 |
|------|----------|----------|
| **圖像顯示為空白** | `Graphics` 物件未清除或 Bitmap 大小過小。 | 在繪製前呼叫 `graphics.Clear(Color.White);`，或增大 Bitmap 尺寸。 |
| **角落呈鋸齒狀** | 使用低解析度的 Bitmap 搭配粗筆。 | 提升 Bitmap DPI（`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`）或減小筆寬。 |
| **找不到檔案錯誤** | 儲存路徑無效。 | 使用 `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`。 |

## 常見問答

### Q1：我可以免費使用 Aspose.Drawing 嗎？

A1：Aspose.Drawing 為商業產品，但您可透過 **[免費試用](https://releases.aspose.com/)** 來體驗其功能。

### Q2：在哪裡可以找到 Aspose.Drawing 文件？

A2：請參閱 **[文件說明](https://reference.aspose.com/drawing/net/)** 以獲得完整指引。

### Q3：如何取得 Aspose.Drawing 的支援？

A3：前往 **[Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44)** 取得社群協助與官方支援。

### Q4：Aspose.Drawing 是否提供臨時授權？

A4：是的，您可取得 **[臨時授權](https://purchase.aspose.com/temporary-license/)** 以供短期使用。

### Q5：在哪裡可以購買 Aspose.Drawing？

A5：請於 **[此處](https://purchase.aspose.com/buy)** 購買 Aspose.Drawing。

## 結論

在本指南中，我們說明了 **如何繪製路徑** 物件、套用不同的 `LineJoin` 樣式，並使用 Aspose.Drawing for .NET 將最終圖形儲存為 PNG 檔案。掌握這些步驟後，您即可在伺服器端程式碼中直接產生精緻的向量圖形、客製圖示或動態圖表。

---

**最後更新：** 2026-02-19  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}