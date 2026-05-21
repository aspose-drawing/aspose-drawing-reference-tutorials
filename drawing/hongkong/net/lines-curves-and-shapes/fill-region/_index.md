---
date: 2026-02-17
description: 學習如何使用 Aspose.Drawing for .NET 填充區域、產生動態圖像，並透過逐步程式碼從多邊形建立區域。
linktitle: How to Fill Region in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何在 Aspose.Drawing for .NET 中填充區域
url: /zh-hant/net/lines-curves-and-shapes/fill-region/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing 中填充區域

創建美觀的圖形通常涉及如何使用顏色、圖案或漸變填充區域。 Aspose.Drawing for .NET 提供了一個簡潔、高效能的 API 來處理這項任務，無論您是建立報表引擎、設計工具，還是動態產生映像。在本教程中，您將逐步了解如何填滿區域，從設定點陣圖到儲存最終影像。

## 快速解答

- **哪個庫處理區域填充？ ** Aspose.Drawing for .NET
- **主要方法？ ** 使用 `Graphics.FillRegion` 和 `Brush` 以及 `Region`
- **我可以產生動態影像嗎？ ** 可以—同一個 API 允許您在執行時建立影像
- **我需要用於生產環境的許可證嗎？ ** 需要商業許可證；提供免費試用
- **支援的 .NET 版本？ ** .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6+

## 什麼是圖形程式設計中的「填滿區域」？

填充區域是指使用畫筆繪製屬於已定義形狀（多邊形、橢圓、自訂路徑）的每個像素。畫筆可以是純色、漸層色，甚至是紋理，讓您可以完全控制區域的視覺效果。

## 為什麼要使用 Aspose.Drawing 來填滿區域？

- **行為一致性**，適用於 .NET Framework、.NET Core 和 .NET 5/6 – 無平台差異。
- **效能最佳化**的渲染管線，非常適合伺服器端影像生成。
- **豐富的 API**，支援複雜路徑、排除內部形狀和進階畫筆。 - **無外部依賴** – 無需在伺服器上安裝 GDI+，從而簡化了部署。

## 準備工作

在開始之前，請確保您已具備以下條件：

1. **Aspose.Drawing 庫** – 從官方網站下載並安裝最新版本。您可以在[此處](https://reference.aspose.com/drawing/net/)找到該程式庫及其文件。
2. **開發環境** – Visual Studio（任何版本）或您首選的 .NET IDE。
3. ** .NET Framework 4.6+ 或 .NET Core 3.1+ 導向的 .NET 專案**。

## 匯入命名空間

首先導入包含我們將要使用的圖形類別的命名空間。

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

現在讓我們一步一步完成這個完整的範例，並將其分解成易於理解的步驟。

## 逐步指南

### 步驟 1：建立 Bitmap 與 Graphics 物件

首先，我們分配一個位圖作為畫布，並取得一個 `Graphics` 物件來在其上繪製圖形。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

> **專業提示：** 使用 `Format32bppPArgb` 可以預先乘以 alpha 值，這樣在之後套用半透明畫筆時可以獲得更平滑的混合效果。

### 步驟 2：定義 GraphicsPath 並建立 Region

`GraphicsPath` 允許我們描述複雜的形狀。這裡我們加上一個多邊形，形成類似菱形的形狀。

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

> 這就是您要找的**從多邊形中提取區域**。 `Region` 物件現在表示該多邊形的內部區域。

### 步驟 3：排除內部區域

通常，您需要在形狀內部建立一個“孔”。我們建立一個矩形並將其從主區域中排除。

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

### 步驟 4：選擇筆刷並填充區域

選擇您喜歡的任何畫筆。在本例中，我們使用純藍色畫筆，但您可以替換為 `LinearGradientBrush` 或 `TextureBrush` 來產生具有更豐富視覺效果的動態影像。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

### 步驟 5：儲存產生的影像

最後，將位圖寫入磁碟。調整路徑，使其指向電腦上存在的資料夾。

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

## 常見問題與解決方案
| 問題 | 原因 | 解決方法 |
|-------|-------|-----|
| **影像顯示空白** | 點陣圖未儲存到可寫資料夾或 `Graphics` 目錄未刷新。 | 請確保目錄存在，並在繪製完成後呼叫 `graphics.Dispose()`。 |
| **Region 未排除內部形狀** | 在區域完全定義之前使用 `Exclude`。 | 如圖所示，在外部區域建立之後呼叫 `region.Exclude(innerPath);`。 |
| **大型影像效能延遲** | 使用 `PixelFormat.Format32bppArgb`（非預乘）。 | 切換到 `Format32bppPArgb` 可加快 alpha 混合速度。 |

## 常見問答

**問：我可以在商業專案中使用 Aspose.Drawing 嗎？ ** 答：是的，Aspose.Drawing 可用於個人和商業項目。有關許可詳細信息，請訪問[此處](https://purchase.aspose.com/buy)。

**問：是否提供免費實驗？ **
答：是的，您可以[此處](https://releases.aspose.com/) 存取免費試用版。

**問：如何獲得 Aspose.Drawing 的支援？ **
答：請造訪 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 以獲得社群和專家的協助。

**問：我可以使用Aspose.Drawing 產生動態影像嗎？ **
答：當然。 Aspose.Drawing 可讓您在 .NET 應用程式中動態建立和操作影像。

**問：是否提供臨時授權？ **
答：是的，您可以[在此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。


## 結論

使用 Aspose.Drawing 填充區域是一種簡單而強大的技術，它能夠**生成動態圖像**、創建自訂形狀以及以編程方式生成精美的圖形。嘗試使用不同的畫筆、漸層和複雜路徑，以充分發揮該庫的潛力。

---

**上次更新：** 2026-02-17
**測試版本：** Aspose.Drawing 24.11 for .NET
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}