---
date: 2025-12-01
description: 學習如何使用 Aspose.Drawing 的直接資料存取來讀取像素與寫入像素資料，以在 .NET 中高效地進行圖像像素操作。
language: zh-hant
linktitle: How to Read Pixels with Direct Data Access in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Direct Data Access for Image Pixel Manipulation
title: 如何在 Aspose.Drawing 中使用直接資料存取讀取像素
url: /net/image-editing/direct-data-access/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing 的直接資料存取讀取像素

## 簡介

在本教學中，您將學會 **如何讀取像素**，以及使用 Aspose.Drawing 的 **直接資料存取** 功能將像素資料寫回。直接資料存取讓您能低階控制像素緩衝區，使圖像像素操作快速且節省記憶體——非常適合自訂濾鏡、圖像分析，或在 .NET 應用程式中大量像素轉換等情境。

## 快速回答
- **主要的讀取像素方法是什麼？** 在 `Bitmap` 實例上使用 `ReadArgb32Pixels`。  
- **哪種像素格式最適合直接存取？** `PixelFormat.Format32bppPArgb` 提供帶預乘 Alpha 的 32 位元 ARGB 值。  
- **使用 Aspose.Drawing 是否需要授權？** 提供免費試用版；正式環境需購買授權。  
- **此程式碼能在 .NET 6+ 上執行嗎？** 能，Aspose.Drawing 支援 .NET 5、.NET 6 以及更新版本。  
- **此操作是否為執行緒安全？** 在不同的 bitmap 實例上讀寫是安全的；若在多執行緒共享同一 bitmap，需自行同步。

## 什麼是 Aspose.Drawing 的直接資料存取？

直接資料存取讓您在不使用逐像素 getter/setter 方法的情況下，直接操作 bitmap 的底層像素緩衝區。一次讀取整個 ARGB32 陣列，即可在單一操作中處理數千個像素，之後再一次寫回修改後的陣列。

## 為什麼在圖像像素操作中使用直接資料存取？

- **效能：** 大量讀寫可減少 interop 呼叫，提升大圖像處理速度。  
- **彈性：** 您會取得原始整數值 (`0xAARRGGBB`)，可使用任何 .NET 邏輯進行操作。  
- **簡易性：** 只需一次方法呼叫讀取、一次寫入——除非您自行實作演算法，否則不必寫巢狀迴圈。

## 先決條件

- **Aspose.Drawing 程式庫：** 從官方網站下載並參考最新的 Aspose.Drawing for .NET。  
- **開發環境：** 任何 .NET IDE（Visual Studio、Rider、VS Code）並安裝 Aspose.Drawing NuGet 套件。  

您可以在[此處](https://releases.aspose.com/drawing/net/)下載程式庫。

## 匯入命名空間

首先，將所需的命名空間匯入作用域，以便使用 bitmap 類別。

```csharp
using System.Drawing;
```

## 逐步指南

### 步驟 1：載入來源圖像  

我們先載入要分析的圖像。請將佔位路徑替換為實際的圖像檔案位置。

```csharp
Bitmap sourceBitmap = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

### 步驟 2：建立目標 Bitmap  

建立一個與來源尺寸相同、且使用適合直接存取的 32 位元像素格式的新 bitmap。

```csharp
Bitmap targetBitmap = new Bitmap(sourceBitmap.Width, sourceBitmap.Height, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步驟 3：讀取像素資料  

將來源 bitmap 的整個 ARGB32 像素緩衝區讀入整數陣列。這就是 **如何讀取像素** 的步驟。

```csharp
int[] pixels = new int[sourceBitmap.Width * sourceBitmap.Height];
sourceBitmap.ReadArgb32Pixels(pixels);
```

### 步驟 4：寫入像素資料  

在完成任意可選的操作（例如套用濾鏡）後，將像素陣列寫回目標 bitmap。此步驟示範 **如何有效寫入像素**。

```csharp
targetBitmap.WriteArgb32Pixels(pixels);
```

### 步驟 5：儲存結果  

將修改後的 bitmap 持久化至磁碟。視需要調整輸出路徑。

```csharp
targetBitmap.Save("Your Document Directory" + @"Images\DirectDataAccess_out.png");
```

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **`ArgumentException` 於 `ReadArgb32Pixels`** | 確認來源 bitmap 使用 32 位元像素格式；若不是，先使用 `sourceBitmap.Clone(..., PixelFormat.Format32bppPArgb)` 轉換。 |
| **寫入後顏色不正確** | 檢查是否意外修改了 alpha 通道；若不需要透明度，請保持 `0xFF`（不透明）值。 |
| **處理超大圖像時效能下降** | 將像素陣列分塊處理，或使用 `Parallel.For` 利用多核心。 |

## 常見問答

**Q: Aspose.Drawing 能在其他 .NET 框架上使用嗎？**  
A: 可以，Aspose.Drawing 支援 .NET Framework、.NET Core，以及 .NET 5/6+。

**Q: 有提供 Aspose.Drawing 的免費試用嗎？**  
A: 當然，有試用版可在[此處](https://releases.aspose.com/)下載。

**Q: 如何取得 Aspose.Drawing 的技術支援？**  
A: 前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 取得社群與官方支援。

**Q: 哪裡可以找到 Aspose.Drawing 的文件？**  
A: 完整 API 參考位於 [Aspose.Drawing 文件站點](https://reference.aspose.com/drawing/net/)。

**Q: 如何購買 Aspose.Drawing 授權？**  
A: 可直接在 Aspose 商店[此處](https://purchase.aspose.com/buy)購買。

**Q: 可以在多執行緒環境下操作像素資料嗎？**  
A: 可以，只要每個執行緒使用各自的 bitmap 實例，或對共享資源加上同步機制。

## 結論

您現在已學會 **如何從 bitmap 讀取像素**、操作 ARGB32 陣列，並使用 Aspose.Drawing 的直接資料存取 **寫回像素資料**。此技術為在 .NET 應用程式中實作自訂濾鏡、像素層級分析與大量轉換等高效能圖像處理任務開啟了大門。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-01  
**測試環境：** Aspose.Drawing 24.12 for .NET  
**作者：** Aspose  

---