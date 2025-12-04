---
date: 2025-12-01
description: 學習如何在 .NET 中使用 Aspose.Drawing 執行座標系統轉換並繪製矩形圖形。一步一步的指南，說明如何轉換頁面座標。
language: zh-hant
linktitle: Coordinate System Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: 座標系統轉換 – Aspose.Drawing for .NET 中的頁面轉換
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 坐標系統轉換 – Aspose.Drawing for .NET 中的頁面轉換

## 介紹

歡迎！在本教學中，您將學會 **如何轉換頁面** 座標，並了解 **坐標系統轉換** 的基礎概念。無論您是開發圖形密集型應用程式，或是需要精確控制繪圖單位，本指南都會一步步帶您從設定畫布到繪製矩形圖形元素。完成後，您即可自信地在自己的專案中運用這些技巧。

## 快速回答
- **什麼是坐標系統轉換？** 將頁面層級的單位（如英吋）映射到裝置層級的像素。  
- **為什麼使用 Aspose.Drawing？** 它提供完整受管理的 System.Drawing.Common 替代方案，且支援跨平台。  
- **實作此範例需要多久？** 基本的頁面轉換大約 5‑10 分鐘即可完成。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線則需購買商業授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.6 以上、.NET Core 3.1 以上、.NET 5/6/7。

## 什麼是坐標系統轉換？

**坐標系統轉換** 定義了在渲染圖形時，如何將邏輯頁面單位（如英吋、厘米或點）轉換為裝置像素。透過設定 `Graphics.PageUnit` 屬性，您告訴繪圖引擎如何解讀您提供的座標，從而取得對尺寸與版面配置的精細控制。

## 為什麼在 Aspose.Drawing 中使用坐標系統轉換？

- **裝置無關的設計：** 只寫一次程式碼，Aspose.Drawing 會自動處理任何螢幕或印表機的像素縮放。  
- **精確繪圖：** 適用於技術圖、CAD 風格草圖，或任何需要精確測量的情境。  
- **跨平台可靠性：** 在 Windows、Linux、macOS 上表現一致，且不受 System.Drawing 的 GDI+ 限制。

## 前置條件

在開始之前，請確保您已具備：

- **Aspose.Drawing 套件：** 從官方網站[此處](https://releases.aspose.com/drawing/net/)下載最新版本。  
- **開發環境：** Visual Studio、Rider 或任何相容 .NET 的 IDE。  
- **文件目錄：** 在程式碼中將 `"Your Document Directory"` 替換為您想儲存輸出影像的資料夾路徑。

一切就緒後，讓我們進入逐步教學。

## 匯入命名空間

首先，將所需的命名空間加入專案：

```csharp
using System.Drawing;
```

## 步驟 1：建立 Bitmap

我們先建立一個空白的 bitmap，作為繪圖表面。`Format32bppPArgb` 像素格式提供高品質、預乘 Alpha 支援。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 2：建立 Graphics 物件

`Graphics` 物件提供 bitmap 的繪圖 API，是程式碼與像素緩衝區之間的橋樑。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 3：清除畫布

為畫布設定中性背景，使繪製的圖形更為突出。此處以淡灰色填滿。

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## 步驟 4：設定轉換（如何轉換頁面）

要將頁面座標映射到裝置像素，請設定 `PageUnit` 屬性。本範例使用英吋，您也可以改用 `GraphicsUnit.Millimeter`、`Point` 等。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

## 步驟 5：繪製矩形 – draw rectangle graphics

現在使用細藍筆繪製矩形。因為已切換至英吋單位，矩形的大小與位置以英吋表示，讓程式碼在列印導向的版面配置中更易讀。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

## 步驟 6：儲存影像

最後，將 bitmap 以 PNG 檔案寫入先前指定的資料夾。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

恭喜！您已完成 **坐標系統轉換**，將頁面單位設定為英吋，並在 bitmap 上 **draw rectangle graphics**。

## 常見問題與解決方案

| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| **未產生輸出檔案** | 路徑錯誤或資料夾不存在 | 確認目標目錄已建立，或在儲存前使用 `Directory.CreateDirectory`。 |
| **矩形變形** | `PageUnit` 設定錯誤或 DPI 不匹配 | 確認 `graphics.PageUnit` 與您使用的單位相符，且 bitmap 的 DPI（預設 96 DPI）已正確設定。 |
| **授權例外** | 生產環境未使用有效授權 | 在建立 graphics 物件前套用臨時或永久的 Aspose.Drawing 授權。 |

## 常見問答

**Q: 可以免費使用 Aspose.Drawing 嗎？**  
A: 可以，免費試用版請點[此處](https://releases.aspose.com/)。

**Q: 哪裡可以找到 Aspose.Drawing 的詳細文件？**  
A: 完整 API 參考位於[此處](https://reference.aspose.com/drawing/net/)。

**Q: 如何取得 Aspose.Drawing 的技術支援？**  
A: 前往[Aspose.Drawing 論壇](https://forum.aspose.com/c/diagram/17)取得社群與官方協助。

**Q: 有提供臨時授權嗎？**  
A: 當然，請至[此處](https://purchase.aspose.com/temporary-license/)取得。

**Q: 想購買完整的 Aspose.Drawing 授權，該去哪裡？**  
A: 可在[此處](https://purchase.aspose.com/buy)購買。

## 結論

本指南說明了在 Aspose.Drawing 中執行 **坐標系統轉換** 的全部要點：設定畫布、配置頁面單位、精確繪製矩形圖形，並將結果儲存。運用這些技巧，您可以為報表、CAD 風格圖紙或任何需要測量精度的應用程式，建立可擴充、裝置無關的圖形。

---

**最後更新：** 2025-12-01  
**測試環境：** Aspose.Drawing 24.12 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}