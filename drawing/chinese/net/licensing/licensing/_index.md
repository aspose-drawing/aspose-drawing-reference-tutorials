---
date: 2026-02-09
description: 学习如何在 .NET 中设置 Aspose.Drawing 许可证。掌握授权方法，解锁全部功能，去除水印。
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 设置 Aspose.Drawing 许可证 – 如何设置 Aspose.Drawing 许可证
url: /zh/net/licensing/licensing/
weight: 10
---

 etc. Keep code block placeholders unchanged.

Let's produce translation.

We must keep the shortcodes at top and bottom as is.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 设置 Aspose.Drawing 许可证

## 介绍

如果您正在构建依赖强大图形和图像处理功能的 .NET 应用程序，**设置 Aspose.Drawing 许可证** 是消除评估限制并获取完整功能集的第一步。在本教程中，您将学习三种实用的设置 Aspose.Drawing 许可证的方法——从文件加载、从流加载以及使用计量使用模型——从而自信地集成该库。

## 快速答案
- **激活 Aspose.Drawing 的主要方式是什么？** 使用 `License.SetLicense("Aspose.Drawing.lic")` 加载许可证文件。  
- **可以在运行时应用许可证吗？** 可以，您可以从 `Stream` 加载许可证，以应对动态场景。  
- **是否支持计量许可证？** 当然；使用 `Metered.SetMeteredKey(publicKey, privateKey)` 启用基于消耗的计费。  
- **开发构建是否需要许可证？** 试用版可用于测试，但有效许可证会去除水印并解锁所有 API。  
- **哪些 .NET 版本兼容？** Aspose.Drawing 支持 .NET Framework 4.x、.NET Core 3.1+ 以及 .NET 5/6+。

## 前置条件

在开始之前，请确保您拥有：

- **Aspose.Drawing 库** – 从 [here](https://releases.aspose.com/drawing/net/) 下载最新包。  
- **许可证文件** – 从 [Aspose](https://purchase.aspose.com/buy) 获取有效的 `.lic` 文件。  
- **.NET 开发环境** – Visual Studio、Rider 或任何面向 .NET Framework/.NET Core 的 IDE。

## 导入命名空间

我们需要标准的 .NET 命名空间以及 Aspose.Drawing 命名空间来进行授权。在 C# 文件顶部添加以下 `using` 语句：

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## 从文件加载许可证

从文件加载许可证是最直接的方法。按照以下三个步骤操作：

### 步骤 1：初始化 License 对象

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### 步骤 2：从 `.lic` 文件设置许可证

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### 步骤 3：确认成功

```csharp
Console.WriteLine("License set successfully.");
```

> **专业提示：** 将 `.lic` 文件放在可执行文件所在的同一文件夹，或提供绝对路径，以避免 “file not found” 错误。

## 从流加载许可证

当您的许可证文件作为资源嵌入或从远程位置获取时，从 `Stream` 加载可以提供灵活性。

### 步骤 1：初始化 License 对象

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### 步骤 2：使用 `FileStream` 加载许可证

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### 步骤 3：确认成功

```csharp
Console.WriteLine("License set successfully.");
```

> **警告：** 记得释放 `FileStream`（或使用 `using` 块）以释放文件句柄。

## 使用计量许可证

计量授权非常适合 SaaS 或按使用付费的场景。它会跟踪消耗并根据实际使用计费。

### 步骤 1：初始化 Metered 对象

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### 步骤 2：设置公钥和私钥

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### 步骤 3：执行图像处理

```csharp
// Your image processing logic here
```

### 步骤 4：获取消耗信息

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### 步骤 5：显示消耗详情

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **常见陷阱：** 如果忘记调用 `SetMeteredKey`，API 将回退到试用模式，输出中会出现水印。

## 为什么要正确设置 Aspose.Drawing 许可证？

- **去除试用模式下的水印**。  
- **解锁高级 API**，如高级图像滤镜和 PDF 转换。  
- **确保遵守 Aspose 的授权条款**，用于商业分发。  
- **启用计量计费**，只为实际使用付费。

## 常见问题及解决方案

| 问题 | 原因 | 解决办法 |
|------|------|----------|
| “License file not found” 错误 | 路径错误或输出文件夹缺少文件 | 使用绝对路径或将文件的 *Copy to Output Directory* 属性设为 *Copy always*。 |
| 设置许可证后仍出现水印 | 在首次 API 调用前未加载许可证 | 在任何 Aspose.Drawing 操作 **之前** 加载许可证。 |
| 计量消耗始终为零 | 未设置密钥或环境变量错误 | 核实公钥/私钥并确保能够访问 Aspose 的计量服务器。 |

## 常见问答

**Q1：可以在没有许可证的情况下使用 Aspose.Drawing 吗？**  
A1：可以，试用许可证可用于开发和评估，但会添加水印并限制部分功能。

**Q2：我需要多久更新一次 Aspose.Drawing 许可证？**  
A2：许可证对购买的版本是永久有效的。仅在需要支持和升级时才需续订。

**Q3：什么是计量授权，何时应该使用？**  
A3：计量授权根据使用量（操作次数或处理的数据）计费。它非常适合云服务或按使用付费的模型。

**Q4：可以在商业项目中使用 Aspose.Drawing 吗？**  
A4：完全可以——拥有有效许可证后，您可以在任何商业应用中嵌入 Aspose.Drawing。

**Q5：在哪里可以找到 Aspose.Drawing 的社区支持？**  
A5：访问 [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) 获取社区帮助、示例和讨论。

## 结论

掌握如何 **设置 Aspose.Drawing 许可证**——无论是从文件、流还是通过计量使用——都能让您充分利用这款强大的 .NET 图形库。按照上述步骤操作，注意常见陷阱，即可构建稳健的图像处理解决方案，毫无授权障碍。

---

**最后更新：** 2026-02-09  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}