---
date: 2026-02-09
description: 學習如何在 .NET 中設定 Aspose.Drawing 授權。掌握授權方法，解鎖完整功能，無浮水印。
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 設定 Aspose.Drawing 授權 – 如何設定 Aspose.Drawing 授權
url: /zh-hant/net/licensing/licensing/
weight: 10
---

**Tested With:** Aspose.Drawing 24.11 for .NET" -> "**測試環境：** Aspose.Drawing 24.11 for .NET"

"**Author:** Aspose" -> "**作者：** Aspose"

Then closing shortcodes.

Also include the backtop button shortcode after.

Make sure to keep all shortcodes exactly.

Now produce final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定 Aspose.Drawing 授權

## 介紹

如果您正在開發依賴強大圖形與影像處理功能的 .NET 應用程式，**設定 Aspose.Drawing 授權** 是移除評估限制並取得完整功能的第一步。在本教學中，您將學習設定 Aspose.Drawing 授權的三種實用方式——從檔案載入、從串流載入，以及使用計量使用模式——讓您能自信地整合此函式庫。

## 快速解答
- **什麼是啟用 Aspose.Drawing 的主要方式？** 使用 `License.SetLicense("Aspose.Drawing.lic")` 載入授權檔案。  
- **我可以在執行時套用授權嗎？** 可以，您可以從 `Stream` 載入授權以因應動態情境。  
- **是否支援計量授權？** 當然支援；使用 `Metered.SetMeteredKey(publicKey, privateKey)` 以啟用依使用量計費。  
- **開發版需要授權嗎？** 試用版可用於測試，但有效授權會移除浮水印並解鎖所有 API。  
- **相容的 .NET 版本有哪些？** Aspose.Drawing 支援 .NET Framework 4.x、.NET Core 3.1 以上，以及 .NET 5/6 以上。

## 前置條件

在開始之前，請確保您已擁有：

- **Aspose.Drawing 函式庫** – 從 [here](https://releases.aspose.com/drawing/net/) 下載最新套件。  
- **授權檔案** – 從 [Aspose](https://purchase.aspose.com/buy) 取得有效的 `.lic` 檔案。  
- **.NET 開發環境** – Visual Studio、Rider，或任何以 .NET Framework/.NET Core 為目標的 IDE。

## 匯入命名空間

我們需要標準的 .NET 命名空間以及 Aspose.Drawing 命名空間來設定授權。請在 C# 檔案的頂部加入以下 `using` 陳述式：

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## 從檔案載入授權

從檔案載入授權是最直接的方式。請依照以下三個步驟操作：

### 步驟 1：初始化 License 物件

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### 步驟 2：從 `.lic` 檔案設定授權

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### 步驟 3：確認成功

```csharp
Console.WriteLine("License set successfully.");
```

> **小技巧：** 將 `.lic` 檔案放置於可執行檔相同資料夾，或提供絕對路徑，以避免出現「找不到檔案」錯誤。

## 從串流載入授權

當授權檔案以資源嵌入或從遠端取得時，從 `Stream` 載入可提供彈性。

### 步驟 1：初始化 License 物件

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### 步驟 2：使用 `FileStream` 載入授權

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### 步驟 3：確認成功

```csharp
Console.WriteLine("License set successfully.");
```

> **警告：** 記得釋放 `FileStream`（或使用 `using` 區塊）以釋放檔案句柄。

## 使用計量授權

計量授權非常適合 SaaS 或按使用付費的情境。它會追蹤消耗量並依實際使用量計費。

### 步驟 1：初始化 Metered 物件

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### 步驟 2：設定公私鑰

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### 步驟 3：執行影像處理

```csharp
// Your image processing logic here
```

### 步驟 4：取得消耗資訊

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### 步驟 5：顯示消耗細節

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **常見陷阱：** 若忘記呼叫 `SetMeteredKey`，API 會回退至試用模式，輸出會出現浮水印。

## 為何要正確設定 Aspose.Drawing 授權？

- **移除** 試用模式下出現的浮水印。  
- **解鎖高級 API**，如進階影像濾鏡與 PDF 轉換。  
- **確保符合** Aspose 授權條款，以供商業發佈。  
- **啟用計量計費**，讓您只為實際使用付費。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| “找不到授權檔案”錯誤 | 路徑錯誤或輸出資料夾缺少檔案 | 使用絕對路徑，或將檔案的 *Copy to Output Directory* 屬性設為 *Copy always*。 |
| 設定授權後仍出現浮水印 | 在首次 API 呼叫前未載入授權 | 在任何 Aspose.Drawing 操作之前 **先** 載入授權。 |
| 計量消耗始終為零 | 金鑰未設定或環境變數錯誤 | 核對公私鑰，並確保能連線至 Aspose 的計量伺服器。 |

## 常見問答

**Q1：我可以在沒有授權的情況下使用 Aspose.Drawing 嗎？**  
A1：可以，試用授權可用於開發與評估，但會加上浮水印且限制部分功能。

**Q2：我需要多久更新一次 Aspose.Drawing 授權？**  
A2：授權對於已購買的版本是永久性的。僅在需要支援與升級時才需續約。

**Q3：什麼是計量授權，何時該使用？**  
A3：計量授權依使用量（操作次數或處理資料量）收費。非常適合雲端服務或按使用付費模式。

**Q4：我可以在商業專案中使用 Aspose.Drawing 嗎？**  
A4：絕對可以——只要擁有有效授權，即可在任何商業應用程式中嵌入 Aspose.Drawing。

**Q5：在哪裡可以找到 Aspose.Drawing 的社群支援？**  
A5：請前往 [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) 取得社群協助、範例與討論。

## 結論

精通如何 **設定 Aspose.Drawing 授權**——無論是從檔案、串流或透過計量使用——都能確保您充分發揮此功能強大的 .NET 圖形函式庫。依照上述步驟操作，留意常見陷阱，即可順利打造穩健的影像處理解決方案，免除授權障礙。

---

**最後更新：** 2026-02-09  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}