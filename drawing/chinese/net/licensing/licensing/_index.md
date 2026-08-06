---
date: 2026-05-29
description: 了解如何在 .NET 中设置 Aspose.Drawing 许可证并移除 Aspose 水印。掌握授权方法，以解锁全部功能并去除水印。
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
linktitle: Aspose.Drawing 授权
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
title: 移除 Aspose 水印 – 设置 Aspose.Drawing 许可证
url: /zh/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 设置 Aspose.Drawing 许可证

## 介绍

如果您正在构建依赖强大图形和图像处理功能的 .NET 应用程序，**设置 Aspose.Drawing 许可证**是去除 Aspose 水印并访问完整功能集的第一步。在本教程中，您将学习三种实用的设置 Aspose.Drawing 许可证的方法——从文件加载、从流加载以及使用计量使用模型——从而能够自信地集成该库并保持输出的整洁。

## 快速答案
- **激活 Aspose.Drawing 的主要方式是什么？** 使用 `License.SetLicense("Aspose.Drawing.lic")` 加载许可证文件。  
- **我可以在运行时应用许可证吗？** 可以，您可以从 `Stream` 加载许可证以适应动态场景。  
- **是否支持计量许可证？** 当然；使用 `Metered.SetMeteredKey(publicKey, privateKey)` 启用基于消耗的计费。  
- **开发构建是否需要许可证？** 试用版可用于测试，但有效许可证会去除水印并解锁所有 API。  
- **兼容哪些 .NET 版本？** Aspose.Drawing 支持 .NET Framework 4.x、.NET Core 3.1+ 和 .NET 5/6+。

## 先决条件

在开始之前，请确保您拥有：

- **Aspose.Drawing 库** – 从 [here](https://releases.aspose.com/drawing/net/) 下载最新包。  
- **许可证文件** – 从 [Aspose](https://purchase.aspose.com/buy) 获取有效的 `.lic` 文件。  
- **.NET 开发环境** – Visual Studio、Rider 或任何面向 .NET Framework/.NET Core 的 IDE。

## 导入命名空间

我们需要标准的 .NET 命名空间以及用于授权的 Aspose.Drawing 命名空间。在 C# 文件顶部添加以下 `using` 语句：

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## 如何从文件加载许可证？

`License` 类代表 Aspose.Drawing 授权组件，实例化后可将许可证应用于库。从文件加载许可证是最直接的方法；只需将 `SetLicense` 方法指向 `.lic` 文件，库即可在整个应用会话期间移除所有试用水印。此方法适用于桌面和服务器环境，无需额外配置，只需确保运行时文件可访问。

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## 如何从流加载许可证？

当许可证文件作为资源嵌入或通过网络获取时，从 `Stream` 加载可提供灵活性，同时仍能保证去除水印。将 `Stream` 实例传递给 `SetLicense` 方法，可将许可证置于部署文件夹之外，这有助于提升安全性并简化容器化或云场景的分发。过程与基于文件的加载相同，只是需自行管理流的生命周期。

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## 如何激活计量许可证？

`Metered` 类处理 Aspose.Drawing 的计量使用激活，实现基于消耗的计费。计量授权让您仅为实际执行的操作付费，非常适合 SaaS 或按使用付费的场景。提供公钥和私钥后，所有图像处理调用都会被自动跟踪计费，库在会话期间以完整功能模式运行且无水印。

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## 为什么正确设置 Aspose.Drawing 许可证？

正确设置许可证可确保库以完整功能模式运行，去除试用水印，并符合 Aspose 的授权条款。恰当的许可证还可启用高级 API、通过关闭评估检查提升性能，并在需要时使用计量计费。如果在首次 API 调用前未加载许可证，库将回退到试用模式，导致所有生成的图像出现水印。

- **去除** 试用模式下出现的水印。  
- **解锁高级 API**，如高级图像过滤器和 PDF 转换。  
- **确保合规**，符合 Aspose 的商业分发许可条款。  
- **启用计量计费**，仅为实际使用付费。  

Aspose.Drawing 支持 **30 多种图像格式**（包括 PNG、JPEG、BMP、TIFF 和 WebP），并且能够在不将整个文件加载到内存的情况下处理 **多百页 PDF 文档**，在普通硬件上实现高性能转换。

## 从文件加载许可证

从文件加载许可证是最直接的方法。请遵循以下三个步骤：

### 步骤 1：初始化许可证对象

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### 步骤 2：从 `.lic` 文件设置许可证

```csharp
Console.WriteLine("License set successfully.");
```

### 步骤 3：确认成功

```csharp
Console.WriteLine("License set successfully.");
```

> **专业提示：** 将 `.lic` 文件放在可执行文件相同的文件夹中，或提供绝对路径，以避免 “file not found” 错误。

## 从流加载许可证

当您的许可证文件作为资源嵌入或从远程位置获取时，使用 `Stream` 加载可提供灵活性。

### 步骤 1：初始化许可证对象

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### 步骤 2：使用 `FileStream` 加载许可证

```csharp
Console.WriteLine("License set successfully.");
```

### 步骤 3：确认成功

```csharp
Console.WriteLine("License set successfully.");
```

> **警告：** 请记得释放 `FileStream`（或使用 `using` 块）以释放文件句柄。

## 使用计量许可证

计量授权非常适合 SaaS 或按使用付费的场景。它会跟踪消耗并根据实际使用计费。

### 步骤 1：初始化计量对象

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### 步骤 2：设置公钥和私钥

```csharp
// Your image processing logic here
```

### 步骤 3：执行图像处理

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### 步骤 4：检索消耗信息

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### 步骤 5：显示消耗详情

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **常见陷阱：** 如果忘记调用 `SetMeteredKey`，API 将回退到试用模式，输出中会出现水印。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| “未找到许可证文件”错误 | 路径错误或输出文件夹中缺少文件 | 使用绝对路径或将文件的 *Copy to Output Directory* 属性设置为 *Copy always*。 |
| 设置许可证后仍出现水印 | 在首次 API 调用前未加载许可证 | 在任何 Aspose.Drawing 操作之前 **加载** 许可证。 |
| 计量消耗始终为零 | 密钥未设置或环境变量错误 | 验证公钥/私钥并确保能够连接 Aspose 的计量服务器。 |

## 常见问题

**Q1：我可以在没有许可证的情况下使用 Aspose.Drawing 吗？**  
A1：可以，试用许可证可用于开发和评估，但会添加水印并限制某些功能。

**Q2：我需要多久续订一次 Aspose.Drawing 许可证？**  
A2：许可证对购买的版本是永久有效的。仅在需要支持和升级时才需续订。

**Q3：什么是计量许可证，何时使用？**  
A3：计量许可证根据使用量（操作或处理的数据）收费。非常适合云服务或按使用付费的模式。

**Q4：我可以在商业项目中使用 Aspose.Drawing 吗？**  
A4：当然——只要拥有有效许可证，就可以在任何商业应用中嵌入 Aspose.Drawing。

**Q5：在哪里可以找到 Aspose.Drawing 的社区支持？**  
A5：访问 [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) 获取社区帮助、示例和讨论。

## 结论

掌握 **设置 Aspose.Drawing 许可证** 的方法——无论是从文件、从流还是通过计量使用——都能确保您充分利用这款强大的 .NET 图形库，同时 **彻底去除 Aspose 水印**。按照上述步骤操作，留意常见陷阱，即可构建稳健的图像处理解决方案，摆脱授权障碍。

---

**Last Updated:** 2026-05-29  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
