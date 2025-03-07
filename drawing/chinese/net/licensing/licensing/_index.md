---
title: Aspose.Drawing 中的许可
linktitle: Aspose.Drawing 中的许可
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 释放 .NET 中 Aspose.Drawing 的全部潜力。无缝集成的主许可。立即下载并提升您的图形和图像处理能力。
weight: 10
url: /zh/net/licensing/licensing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing 中的许可

## 介绍

在 .NET 开发领域，Aspose.Drawing 作为图形和图像处理的强大工具脱颖而出。要释放 Aspose.Drawing 的全部潜力，了解许可至关重要。本教程将指导您完成各种许可方法，确保您将 Aspose.Drawing 无缝集成到您的 .NET 项目中。

## 先决条件

在深入了解 Aspose.Drawing 许可之前，请确保您满足以下先决条件：

-  Aspose.Drawing Library：从以下位置下载该库[这里](https://releases.aspose.com/drawing/net/).
- 许可证文件：从以下位置获取有效的许可证文件[阿斯普斯](https://purchase.aspose.com/buy).
- .NET 环境：确保您有一个有效的 .NET 开发环境。

## 导入命名空间

在继续之前，必须将必要的命名空间导入到您的项目中：

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## 从文件加载许可证

让我们从基础开始。从文件加载许可证是一种常见做法。按着这些次序：

### 第1步：初始化许可证对象

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### 第 2 步：从文件设置许可证

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### 第3步：显示成功消息

```csharp
Console.WriteLine("License set successfully.");
```

## 从流加载许可证

从流加载许可证提供了灵活性。您可以这样做：

### 第1步：初始化许可证对象

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### 步骤 2：从 FileStream 加载许可证

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### 第3步：显示成功消息

```csharp
Console.WriteLine("License set successfully.");
```

## 使用计量许可证

计量许可提供了基于消费的模型。设置方法如下：

### 步骤一：初始化被测对象

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### 第 2 步：设置计量公钥和私钥

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### 步骤3：执行处理

```csharp
//您的图像处理逻辑在这里
```

### 第四步：获取消费信息

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### 第5步：显示信息

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

## 结论

掌握 Aspose.Drawing 中的许可对于释放这个强大的 .NET 库的全部潜力至关重要。无论是从文件、流加载还是使用计量许可加载，这些步骤都可确保无缝集成到您的项目中。

## 常见问题解答

### Q1：我可以在没有许可证的情况下使用Aspose.Drawing吗？

A1：虽然您可以在没有许可证的情况下使用它，但有效的许可证可以解锁附加功能并删除水印。

### 问题 2：我需要多久更新一次 Aspose.Drawing 许可证？

A2：许可证通常是永久性的，允许您无限期地使用您购买的版本。但是，更新和支持可能需要续订。

### 问题 3：什么是计量许可？何时应该使用它？

A3：计量许可基于使用情况。适合需要按操作次数或处理数据量付费的场景。

### Q4：我可以在商业项目中使用Aspose.Drawing吗？

A4：是的，只要有适当的许可，您就可以在商业和非商业项目中使用 Aspose.Drawing。

### Q5：在哪里可以找到 Aspose.Drawing 的社区支持？

 A5：访问[Aspose.绘图论坛](https://forum.aspose.com/c/diagram/17)以获得社区支持和讨论。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
