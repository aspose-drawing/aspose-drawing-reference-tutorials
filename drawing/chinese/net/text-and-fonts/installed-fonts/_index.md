---
date: 2026-02-25
description: 学习如何使用 C# 创建位图图形并保存 PNG 图像，同时列出已安装的字体、使用字体绘制文本，并使用 Aspose.Drawing for
  .NET 调整位图分辨率。
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 使用 C# 创建位图图形 – 在 Aspose.Drawing 中保存 PNG 图像并使用已安装的字体
url: /zh/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 保存 PNG 图像并在 Aspose.Drawing 中使用已安装的字体

## Introduction

如果您需要 **保存 PNG 图像** 文件，同时 **创建位图图形 C#**，Aspose.Drawing for .NET 为您提供了一种干净、跨平台的方式来实现。在本教程中，我们将演示列出已安装的字体、显示字体族、从位图创建图形以及使用字体绘制文本——最终将结果保存为 PNG 图像。完成后，您将拥有一个可在任何 .NET 项目中使用的可重用代码片段。

## Quick Answers
- **本教程创建了什么？** 一个列出已安装字体族的 PNG 图像。  
- **需要哪个库？** Aspose.Drawing for .NET（不需要 System.Drawing.Common）。  
- **我可以使用自定义字体吗？** 可以——只需将它们加载到 `InstalledFontCollection`。  
- **输出分辨率可调吗？** 当然——更改位图大小或像素格式即可 **adjust bitmap resolution C#** 样式。  
- **运行代码是否需要许可证？** 临时许可证可用于评估；生产环境需要完整许可证。

## What is “save PNG image” in the context of Aspose.Drawing?
在 Aspose.Drawing 中，“保存 PNG 图像”意味着将您的绘图表面（`Bitmap`）渲染为扩展名为 `.png` 的文件。Aspose.Drawing 会为您处理编码，只需调用 `bitmap.Save(...)` 并提供所需路径即可。

## Why list installed fonts and show font families?
了解系统中有哪些字体可用，可让您创建能够适应终端用户环境的动态图形。这在生成报告、证书或任何必须符合企业品牌而不需要随应用程序一起分发字体文件的视觉内容时尤为实用。

## How to create bitmap graphics C# with Aspose.Drawing?
下面提供了一个实用的、逐步的演练，展示如何 **create bitmap graphics C#**、使用字体绘制文本，并在需要时调整位图分辨率。

## Prerequisites

- **Aspose.Drawing Library** – 从 [Aspose Drawing 下载页面](https://releases.aspose.com/drawing/net/) 下载最新版本。  
- **IDE** – Visual Studio、Rider 或任何兼容 .NET 的编辑器。  
- **Basic C# knowledge** – 您应熟悉类、对象以及简单循环。

## Import Namespaces
要使用字体和图形，请在 C# 文件顶部导入以下命名空间：

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step‑by‑Step Guide

### Step 1: Create a bitmap (the canvas)
首先，创建一个位图来容纳最终图像。位图的大小和像素格式决定了保存的 PNG 的质量，并让您能够 **adjust bitmap resolution C#**。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Step 2: Create graphics from bitmap
接下来，从位图获取一个 `Graphics` 对象。该对象允许我们在画布上绘制形状、文本和图像。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Step 3: Set up brush and font (draw text with fonts)
我们需要一个画刷来设置文本颜色，以及一个 `Font` 对象来定义字体、大小和样式。这正是 **draw text with fonts** 的所在。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Step 4: List installed fonts and show font families
现在，我们将在位图上直接显示字体族的数量以及前几个名称，以演示 **list installed fonts** 和 **show font families** 的功能。

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Step 5: Save PNG image
最后，将位图写入磁盘并保存为 PNG 文件。这就是核心的 **save png image** 操作。

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tip:** 使用 `Path.Combine` 构建文件路径，可避免不同操作系统之间目录分隔符的问题。

## Common Issues and Solutions
| Issue | Cause | Fix |
|-------|-------|-----|
| **未显示字体** | `InstalledFontCollection` 未填充（例如在没有字体的无头服务器上运行）。 | 在服务器上安装所需字体，或在应用程序中嵌入自定义字体。 |
| **保存的文件损坏** | 像素格式不正确或缺少写入权限。 | 确保目标文件夹存在且应用具有写入权限；保持使用 `Format32bppPArgb`。 |
| **文本模糊** | DPI 设置过低。 | 增大位图尺寸或设置 `graphics.SmoothingMode = SmoothingMode.AntiAlias`。 |

## Frequently Asked Questions

**Q: 我可以使用机器上未安装的自定义字体吗？**  
A: 可以。将字体文件加载到 `PrivateFontCollection`，然后从该集合创建 `Font`。

**Q: 如何处理与字体相关的异常？**  
A: 将字体创建代码放在 `try/catch` 块中，捕获 `ArgumentException` 并检查缺失的字体族。

**Q: Aspose.Drawing 适合用于 Web 应用吗？**  
A: 绝对适合。该库可在 ASP.NET Core、Azure Functions 以及其他服务器端环境中使用。

**Q: 我可以更改文本颜色或样式吗？**  
A: 可以。使用不同的 `Brush` 类型（例如 `LinearGradientBrush`）并修改 `FontStyle` 枚举。

**Q: 哪里可以获取用于测试的临时许可证？**  
A: 从 [Aspose 临时许可证页面](https://purchase.aspose.com/temporary-license/) 下载试用许可证。

## Conclusion

通过遵循上述步骤，您已经学会了如何使用 Aspose.Drawing for .NET **save PNG image**，并动态 **list installed fonts**、**show font families**、**create graphics from bitmap**、以及 **draw text with fonts**。您现在能够 **create bitmap graphics C#**、调整位图分辨率，并在需要时加入自定义字体。欢迎尝试其他字体、颜色和位图尺寸，以满足项目的视觉需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2026-02-25  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose