---
title: 在 Aspose.Drawing 中載入並儲存圖片
linktitle: 在 Aspose.Drawing 中載入並儲存圖片
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 使用 Aspose.Drawing 在 .NET 中掌握映像載入和儲存。輕鬆探索 BMP、GIF、JPG、PNG、TIFF 格式。
type: docs
weight: 13
url: /zh-hant/net/image-editing/load-save/
---
## 介紹

歡迎來到我們關於使用 Aspose.Drawing for .NET 掌握圖片載入和儲存的逐步指南！如果您希望提高輕鬆處理各種圖像格式的技能，那麼您來對地方了。 Aspose.Drawing for .NET 是一個功能強大的函式庫，可以簡化影像處理過程，在本教學過程中，我們將深入探討以不同格式載入和儲存影像。

## 先決條件

在我們開始這個學習之旅之前，請確保您具備以下先決條件：

-  Aspose.Drawing for .NET：確保您已安裝程式庫。你可以下載它[這裡](https://releases.aspose.com/drawing/net/).

- .NET 環境：本教學假設您具有 .NET 開發的應用知識。

現在我們已經準備好了，讓我們探索基本的命名空間並深入研究逐步指南。

## 導入命名空間

在您的 .NET 專案中，首先匯入必要的命名空間：

```csharp
using System.Drawing;
```

這些命名空間提供影像操作所需的基本類別和方法。

## 第 1 步：載入圖像

讓我們從加載圖像開始。此範例載入各種格式的圖像，例如 BMP、GIF、JPG、PNG 和 TIFF。

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## 步驟2：實作LoadAndSave方法

現在，分解`LoadAndSave`方法分為多個步驟：

### 步驟2.1：載入圖片

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### 步驟2.2：儲存影像

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    //儲存影像
    loadedImage.Save(outputPath);
}
```

對您想要支援的每種圖像格式重複這些步驟。

## 結論

恭喜！您已經掌握了使用 Aspose.Drawing for .NET 載入和儲存影像的藝術。對於使用多種影像格式的開發人員來說，這項技能非常寶貴。實驗、探索並將這些知識整合到您的專案中。

## 常見問題解答

### Q1：Aspose.Drawing 是否相容於所有影像格式？

A1：Aspose.Drawing 支援多種格式，包括 BMP、GIF、JPG、PNG 和 TIFF。

### Q2：在哪裡可以找到Aspose.Drawing的詳細文件？

A2：查看官方文檔[這裡](https://reference.aspose.com/drawing/net/).

### Q3：如何取得 Aspose.Drawing 的臨時授權？

 A3：參觀[這裡](https://purchase.aspose.com/temporary-license/)了解臨時許可證詳細資訊。

### Q4：如果我在實施過程中遇到問題或有疑問怎麼辦？

 A4：向 Aspose.Drawing 社群尋求協助，網址為[Aspose論壇](https://forum.aspose.com/c/diagram/17).

### Q5：哪裡可以購買Aspose.Drawing庫？

 A5：可以買[這裡](https://purchase.aspose.com/buy).