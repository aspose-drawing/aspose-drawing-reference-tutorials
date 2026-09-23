---
date: 2026-09-23
description: 了解如何使用 Aspose.Drawing 在 C# 中保存 PNG 图像、列出已安装的字体、使用自定义字体绘制文本，以及调整位图分辨率以实现高质量图形。
keywords:
- save png image c#
- installed fonts aspnet
- aspose.drawing bitmap graphics
- c# font collection
- png export .net
lastmod: 2026-09-23
linktitle: 使用 Aspose.Drawing 和已安装字体在 C# 中保存 PNG 图像
og_description: 使用 Aspose.Drawing 在 C# 中保存 PNG 图像。本指南展示了如何列出已安装的字体、绘制文本以及控制位图分辨率，以实现专业图形。
og_image_alt: Developer guide showing C# code that creates a bitmap, lists system
  fonts, and saves a PNG file with Aspose.Drawing
og_title: 使用 Aspose.Drawing 和已安装字体在 C# 中保存 PNG 图像
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  headline: Save PNG image in C# with Aspose.Drawing and installed fonts
  type: TechArticle
- description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  name: Save PNG image in C# with Aspose.Drawing and installed fonts
  steps:
  - name: Create a bitmap (the canvas)
    text: '`Bitmap` is the raster image object that holds pixel data for the canvas.'
  - name: Create graphics from bitmap
    text: '`Graphics` is the object that supplies drawing functions such as drawing
      shapes and text onto a bitmap.'
  - name: Set up brush and font (draw text with fonts)
    text: '`Brush` defines how shapes and text are filled with colour, while `Font`
      specifies the typeface, size, and style for text rendering.'
  - name: List installed fonts and show font families
    text: '`InstalledFontCollection` provides access to all font families installed
      on the host system.'
  - name: Save PNG image
    text: '`bitmap.Save` writes the bitmap to a file in the chosen image format, such
      as PNG. > **Pro tip:** Use `Path.Combine` for building file paths to avoid issues
      with directory separators on different operating systems.'
  type: HowTo
- questions:
  - answer: Yes. Load the font file into a `PrivateFontCollection` and create a `Font`
      from that collection, then draw it the same way as system fonts.
    question: Can I use custom fonts that are not installed on the machine?
  - answer: Wrap font creation in a `try/catch` block and inspect `ArgumentException`
      for missing families; provide a fallback font such as `Arial`.
    question: How do I handle font‑related exceptions?
  - answer: Absolutely. The library works in ASP.NET Core, Azure Functions, and other
      server‑side .NET environments without needing GDI+.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify
      the `FontStyle` enum to apply bold, italic, or underline.
    question: Can I change the text colour or style?
  - answer: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – bitmap graphics and font handling
tags:
- save png
- aspose.drawing
- c# graphics
- installed fonts
- bitmap
title: 使用 Aspose.Drawing 和已安装字体在 C# 中保存 PNG 图像
url: /zh/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中使用 Aspose.Drawing 和已安装字体保存 PNG 图像

## 介绍

如果您需要在 C# 中 **保存 PNG 图像** 并且 **创建位图图形**，Aspose.Drawing for .NET 为您提供了一种简洁、跨平台的方式来实现。在本教程中，我们将逐步演示列出已安装的字体、显示字体族、从位图创建图形以及使用字体绘制文本——最终将结果保存为 PNG 图像。完成后，您将拥有一个可在任何 .NET 项目中使用的可复用代码片段，无论它运行在 Windows、Linux 还是 macOS 上。

## 快速答案
- **本教程创建了什么？** 列出主机上已安装字体族的 PNG 图像。  
- **需要哪个库？** Aspose.Drawing for .NET（不依赖 System.Drawing.Common）。  
- **我可以使用自定义字体吗？** 可以——将其加载到 `InstalledFontCollection` 或 `PrivateFontCollection` 中。  
- **输出分辨率可调吗？** 当然——通过更改位图尺寸或像素格式来控制分辨率。  
- **运行代码是否需要许可证？** 临时许可证可用于评估；生产环境需要正式许可证。

## 在 Aspose.Drawing 中，“保存 PNG 图像” 是什么？

`Bitmap` 是 Aspose.Drawing 的光栅图像容器，用于存储像素数据。  
保存 PNG 图像意味着将您的绘图表面——一个 `Bitmap`——渲染为扩展名为 `.png` 的文件。Aspose.Drawing 执行无损 PNG 压缩，且能够处理高达 **10 000 × 10 000 像素** 的图像而不会耗尽内存，适用于高分辨率图形。生成的文件可用于网页、报告或后续的图像处理流水线。

## 为什么列出已安装的字体并显示字体族？

列出已安装的字体让您的应用能够适配终端用户的环境，确保生成的图形符合企业品牌或用户偏好，而无需额外分发字体文件。`InstalledFontCollection` 枚举操作系统中已安装的字体。这在自动化报告生成、证书制作或任何必须遵循系统排版的视觉内容中尤为有用。

## 如何使用 Aspose.Drawing 在 C# 中创建位图图形？

`Bitmap` 表示图像画布；`Graphics` 为该画布提供绘图方法；`Font` 描述用于文本渲染的字体。您只需几行代码即可生成完整的 PNG：创建 `Bitmap`，获取 `Graphics` 对象，使用已安装集合中的 `Font` 绘制文本，最后调用 `bitmap.Save`。下面的分步指南会展开每个部分并提供实用技巧。

## 先决条件

- **Aspose.Drawing 库** – 从 [Aspose Drawing 下载页面](https://releases.aspose.com/drawing/net/) 下载最新版本。  
- **IDE** – Visual Studio、Rider 或任何 .NET 兼容的编辑器。  
- **基本的 C# 知识** – 您应熟悉类、对象和简单循环。  
- **.NET 运行时** – 推荐使用 .NET 6+ 或 .NET Core 3.1+ 以获得完整的跨平台支持。

## 导入命名空间

在 C# 文件顶部添加以下 `using` 语句，以便编译器能够定位图形和字体类型：

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Text;
using System.IO;
```

## 分步指南

### 步骤 1：创建位图（画布）

`Bitmap` 是用于保存画布像素数据的光栅图像对象。  

```csharp
using System.Drawing;
using System.Drawing.Text;
```

### 步骤 2：从位图创建图形

`Graphics` 是提供绘图功能的对象，可在位图上绘制形状和文本。  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步骤 3：设置画刷和字体（使用字体绘制文本）

`Brush` 定义形状和文本的填充颜色，而 `Font` 指定文本渲染时使用的字体、大小和样式。  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### 步骤 4：列出已安装的字体并显示字体族

`InstalledFontCollection` 提供对主机系统上所有已安装字体族的访问。  

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### 步骤 5：保存 PNG 图像

`bitmap.Save` 将位图写入指定图像格式的文件，例如 PNG。  

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

> **技巧提示：** 使用 `Path.Combine` 构建文件路径，以避免不同操作系统的目录分隔符问题。

## 常见问题及解决方案

| 问题 | 原因 | 解决方法 |
|------|------|----------|
| **未显示字体** | `InstalledFontCollection` 未填充（例如，在没有字体的无头服务器上运行）。 | 在服务器上安装所需字体，或在应用程序中嵌入自定义字体。 |
| **保存的文件损坏** | 像素格式不正确或缺少写入权限。 | 确保目标文件夹存在且应用具有写入权限；保持 `PixelFormat.Format32bppPArgb`。 |
| **文本模糊** | DPI 设置过低或位图尺寸太小。 | 增大位图尺寸或设置 `graphics.SmoothingMode = SmoothingMode.AntiAlias`。 |

## 常见问题

**问：我可以使用机器上未安装的自定义字体吗？**  
答：可以。将字体文件加载到 `PrivateFontCollection` 中，然后从该集合创建 `Font`，并像系统字体一样绘制。

**问：如何处理与字体相关的异常？**  
答：在创建字体时使用 `try/catch` 包裹，并检查 `ArgumentException` 以捕获缺失的字体族；提供如 `Arial` 的后备字体。

**问：Aspose.Drawing 适用于 Web 应用程序吗？**  
答：完全适用。该库可在 ASP.NET Core、Azure Functions 等服务器端 .NET 环境中使用，无需 GDI+。

**问：我可以更改文本颜色或样式吗？**  
答：可以。使用不同的 `Brush` 类型（例如 `LinearGradientBrush`）并修改 `FontStyle` 枚举以实现粗体、斜体或下划线等样式。

**问：在哪里可以获取用于测试的临时许可证？**  
答：从 [Aspose 临时许可证页面](https://purchase.aspose.com/temporary-license/) 下载试用许可证。

## 结论

通过本教程，您已经学会了如何使用 Aspose.Drawing for .NET **在 C# 中保存 PNG 图像**，并动态 **列出已安装的字体**、**显示字体族**、**从位图创建图形**以及 **使用字体绘制文本**。您现在了解了 **创建位图图形 C#**、调整位图分辨率以及在需要时嵌入自定义字体的技巧。请尝试不同的颜色、字体大小和位图尺寸，以满足项目的视觉需求，并探索 Aspose.Drawing 的其他功能，如形状绘制和图像处理，以实现更丰富的图形效果。

---

**最后更新：** 2026-09-23  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

## 相关教程

- [如何使用 Aspose.Drawing for .NET 绘制文本](/drawing/net/text-and-fonts/draw-text/)
- [使用 Antialiasing 提升 Aspose.Drawing 图像质量](/drawing/net/rendering/antialiasing/)
- [如何使用 Aspose.Drawing 保存 PNG – 世界变换](/drawing/net/coordinate-transformations/world-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}