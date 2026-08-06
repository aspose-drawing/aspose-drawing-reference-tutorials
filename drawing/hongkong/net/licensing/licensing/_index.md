---
date: 2026-05-29
description: 了解如何在 .NET 中設定 Aspose.Drawing 授權並移除 Aspose 水印。掌握授權方法，解鎖完整功能，無水印。
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
linktitle: Aspose.Drawing 授權
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  headline: Remove Aspose Watermark – Set Aspose.Drawing License
  type: TechArticle
- description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  name: Remove Aspose Watermark – Set Aspose.Drawing License
  steps:
  - name: Confirm Success
    text: '> **Pro tip:** Place the `.lic` file in the same folder as your executable
      or provide an absolute path to avoid “file not found” errors.'
  - name: Confirm Success
    text: '> **Warning:** Remember to dispose the `FileStream` (or use a `using` block)
      to free file handles.'
  - name: Display the Consumption Details
    text: '> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will
      fall back to trial mode and you’ll see watermarks in the output.'
  type: HowTo
- questions:
  - answer: Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.
    question: What is the primary way to activate Aspose.Drawing?
  - answer: Yes, you can load the license from a `Stream` for dynamic scenarios.
    question: Can I apply a license at runtime?
  - answer: Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable
      consumption‑based billing.
    question: Is a metered license supported?
  - answer: A trial works for testing, but a valid license removes watermarks and
      unlocks all APIs.
    question: Do I need a license for development builds?
  - answer: Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.
    question: Which .NET versions are compatible?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 移除 Aspose 水印 – 設定 Aspose.Drawing 授權
url: /zh-hant/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定 Aspose.Drawing 授權

## 介紹

如果您正在開發依賴強大圖形與影像處理功能的 .NET 應用程式，**設定 Aspose.Drawing 授權** 是移除 Aspose 水印並取得完整功能的第一步。在本教學中，您將學會三種實用的授權設定方式——從檔案載入、從串流載入，以及使用計量使用模式——讓您能自信地整合此函式庫，並保持輸出結果乾淨。

## 快速回答
- **啟用 Aspose.Drawing 的主要方式是什麼？** 使用 `License.SetLicense("Aspose.Drawing.lic")` 載入授權檔案。  
- **可以在執行時套用授權嗎？** 可以，您可以從 `Stream` 載入授權以因應動態情境。  
- **是否支援計量授權？** 當然；使用 `Metered.SetMeteredKey(publicKey, privateKey)` 即可啟用依使用量計費。  
- **開發版需要授權嗎？** 試用版可用於測試，但有效授權會移除水印並解鎖所有 API。  
- **相容的 .NET 版本有哪些？** Aspose.Drawing 支援 .NET Framework 4.x、.NET Core 3.1+ 以及 .NET 5/6+。

## 前置條件

開始之前，請確保您已具備：

- **Aspose.Drawing 函式庫** – 從 [here](https://releases.aspose.com/drawing/net/) 下載最新套件。  
- **授權檔案** – 從 [Aspose](https://purchase.aspose.com/buy) 取得有效的 `.lic` 檔案。  
- **.NET 開發環境** – Visual Studio、Rider 或任何支援 .NET Framework/.NET Core 的 IDE。

## 匯入命名空間

我們需要標準的 .NET 命名空間以及 Aspose.Drawing 的命名空間來處理授權。請在 C# 檔案的最上方加入以下 `using` 陳述式：

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## 如何從檔案載入授權？

`License` 類別代表 Aspose.Drawing 的授權元件，實例化後即可將授權套用至函式庫。從檔案載入授權是最直接的做法；只要將 `SetLicense` 方法指向 `.lic` 檔案，函式庫就會在整個應用程式執行期間移除所有試用水印。此方法同時適用於桌面與伺服器環境，且不需要額外設定，只要確保執行時能存取該檔案即可。

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## 如何從串流載入授權？

當授權檔案以資源形式嵌入或透過網路取得時，從 `Stream` 載入可提供彈性，同時保證水印被移除。將 `Stream` 實例傳遞給 `SetLicense` 方法，可將授權檔案置於部署目錄之外，提升安全性並簡化容器或雲端情境的發佈流程。此流程與檔案載入相同，唯一差別在於您自行管理串流的生命週期。

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## 如何啟用計量授權？

`Metered` 類別負責 Aspose.Drawing 的計量使用啟用，支援依使用量計費。計量授權讓您只為實際執行的操作付費，特別適合 SaaS 或按次付費的情境。提供公鑰與私鑰後，所有影像處理呼叫皆會自動被追蹤與計費，函式庫在整個工作階段內以完整功能模式運作且不會出現水印。

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## 為何要正確設定 Aspose.Drawing 授權？

正確設定授權可確保函式庫以完整功能模式執行、移除試用水印，並遵守 Aspose 的授權條款。正確套用授權還能啟用高階 API、透過停用評估檢查提升效能，並在需要時使用計量計費。若在首次呼叫 API 前未載入授權，函式庫將回退至試用模式，導致所有產生的影像帶有水印。

- **移除試用模式下的水印**。  
- **解鎖高階 API**，如進階影像濾鏡與 PDF 轉換。  
- **確保符合 Aspose 授權條款**，適用於商業發佈。  
- **啟用計量計費**，只為實際使用付費。  

Aspose.Drawing 支援 **30 多種影像格式**（包括 PNG、JPEG、BMP、TIFF 與 WebP），且能在不將整個檔案載入記憶體的情況下處理 **上百頁的 PDF 文件**，在一般硬體上提供高效能轉換。

## 從檔案載入授權

從檔案載入授權是最直接的方式。請依照以下三個步驟操作：

### 步驟 1：初始化 License 物件

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### 步驟 2：從 `.lic` 檔案設定授權

```csharp
Console.WriteLine("License set successfully.");
```

### 步驟 3：確認成功

```csharp
Console.WriteLine("License set successfully.");
```

> **專業提示：** 將 `.lic` 檔案放在可執行檔同一資料夾，或使用絕對路徑，以避免「找不到檔案」錯誤。

## 從串流載入授權

當授權檔案以資源形式嵌入或從遠端取得時，從 `Stream` 載入可提供彈性。

### 步驟 1：初始化 License 物件

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### 步驟 2：使用 `FileStream` 載入授權

```csharp
Console.WriteLine("License set successfully.");
```

### 步驟 3：確認成功

```csharp
Console.WriteLine("License set successfully.");
```

> **警告：** 記得釋放 `FileStream`（或使用 `using` 區塊）以關閉檔案句柄。

## 使用計量授權

計量授權非常適合 SaaS 或按次付費的情境。它會追蹤使用量並依實際使用情形計費。

### 步驟 1：初始化 Metered 物件

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### 步驟 2：設定公私鑰

```csharp
// Your image processing logic here
```

### 步驟 3：執行影像處理

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### 步驟 4：取得消耗資訊

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### 步驟 5：顯示消耗細節

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **常見陷阱：** 若忘記呼叫 `SetMeteredKey`，API 會回退至試用模式，輸出結果會出現水印。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| 「找不到授權檔案」錯誤 | 路徑錯誤或輸出資料夾缺少檔案 | 使用絕對路徑或將檔案的 *Copy to Output Directory* 屬性設為 *Copy always*。 |
| 設定授權後仍出現水印 | 在首次 API 呼叫前未載入授權 | **在** 任何 Aspose.Drawing 操作之前先載入授權。 |
| 計量消耗始終為 0 | 未設定金鑰或環境變數錯誤 | 核對公私鑰，並確保能連線至 Aspose 的計量伺服器。 |

## 常見問答

**Q1：可以在沒有授權的情況下使用 Aspose.Drawing 嗎？**  
A1：可以，試用授權可用於開發與評估，但會加上水印且限制部分功能。

**Q2：需要多久更新一次 Aspose.Drawing 授權？**  
A2：授權為永久授權，僅在需要支援與升級時才需續約。

**Q3：什麼是計量授權，何時該使用？**  
A3：計量授權依使用量（操作次數或處理資料量）收費，適合雲端服務或按次付費模式。

**Q4：可以在商業專案中使用 Aspose.Drawing 嗎？**  
A4：絕對可以——取得有效授權後，您可在任何商業應用程式中嵌入 Aspose.Drawing。

**Q5：在哪裡可以取得 Aspose.Drawing 的社群支援？**  
A5：請前往 [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) 取得社群協助、範例與討論。

## 結論

熟練 **設定 Aspose.Drawing 授權** 的各種方式——無論是從檔案、從串流，或透過計量使用——都能讓您充分發揮此強大 .NET 圖形函式庫的效能，同時 **徹底移除 Aspose 水印**。依照上述步驟操作，留意常見陷阱，即可順利建構無授權障礙的影像處理解決方案。

---

**最後更新：** 2026-05-29  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
