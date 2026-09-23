---
date: 2026-09-23
description: 了解如何使用 Aspose.Drawing for .NET 在图像上绘制文本。生成带文本的图像，将文本添加到 bitmap，并使用 custom
  fonts 将 bitmap 保存为 PNG。
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: 如何使用 Aspose.Drawing 绘制文本
og_description: 了解如何使用 Aspose.Drawing for .NET 在图像上绘制文本。本教程展示了如何生成带文本的图像、将文本添加到 bitmap，以及使用
  custom fonts 将 bitmap 保存为 PNG。
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: 使用 Aspose.Drawing for .NET 在图像上绘制文本 – 快速指南
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: 如何使用 Aspose.Drawing for .NET 在图像上绘制文本
url: /zh/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Drawing for .NET 在图像上绘制文本

## 介绍

在本分步指南中，您将学习使用 Aspose.Drawing for .NET **在图像上绘制文本**。无论您需要创建 *动态文本图像*、向现有位图添加文本，还是生成带有自定义字体的图形，本教程都会详细讲解，让您在几分钟内开始绘制文本。该库支持超过 30 种 GDI+ 方法，可在 Windows、Linux 和 macOS 上运行，并且 **零外部依赖**，是服务器端图像生成的可靠选择。

## 快速答案
- **使用的库是什么？** Aspose.Drawing for .NET  
- **主要任务？** 在图像上绘制文本（创建带文本的图像）  
- **关键方法？** `Graphics.DrawString`（在图像上绘制字符串）  
- **输出格式？** PNG（将位图保存为 PNG）  
- **先决条件？** .NET 开发环境和 Aspose.Drawing 库  

## 什么是使用 Aspose.Drawing 绘制文本？

使用 Aspose.Drawing 绘制文本是指利用该库兼容 GDI+ 的 API 将 Unicode 字符串渲染到光栅画布上。`Graphics.DrawString` 方法将文本写入位图，您可以控制字体、颜色、对齐方式和抗锯齿。此方法使您无需安装 System.Drawing.Common 即可生成高质量图像。

## 为什么使用 Aspose.Drawing 向图像添加文本？

Aspose.Drawing 提供了一种可靠的跨平台方式，在无需本机 GDI+ 库的情况下在图像上渲染文本，能够在任何操作系统上提供一致的质量和性能。它支持高级抗锯齿、Unicode 字符和自定义字体，并能无缝集成到 .NET 应用程序中，因而非常适合服务器端图像生成和桌面工具。

- **跨平台可靠性** – 在 Windows、Linux 和 macOS 上均可工作。  
- **高级渲染** – 抗锯齿和子像素文字平滑，输出清晰。  
- **无外部依赖** – 该库捆绑了创建带文本图像所需的全部内容。

## 先决条件

在开始之前，请确保您已拥有：

- **Aspose.Drawing for .NET** – 从 [Aspose.Drawing 文档](https://reference.aspose.com/drawing/net/) 下载。  
- **.NET IDE**，例如 Visual Studio 或 VS Code。  

## 导入命名空间

首先导入所需的命名空间：

这些命名空间提供了核心 GDI+ 类型，例如 `Bitmap`、`Graphics` 和文本渲染实用程序。  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 步骤 1：创建 bitmap 和 graphics 对象

`Bitmap` 是 Aspose.Drawing 用于像素数据的光栅图像容器，`Graphics` 提供绘图方法以在其上渲染形状和文本。

`Bitmap` 表示内存中的图像，而 `Graphics` 提供在该 bitmap 上进行渲染的绘图方法。  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

这里我们创建一个用于保存最终图片的 `Bitmap`，以及一个允许我们在其上绘图的 `Graphics` 对象。抗锯齿提示确保文本平滑。

## 步骤 2：设置 brush、pen 和 font

`Brush` 定义填充颜色，`Pen` 勾勒形状，`Font` 指定用于渲染文本的字体、大小和样式。

`Brush` 用颜色填充形状，`Pen` 勾勒形状，`Font` 定义文本渲染的字体和大小。  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** 定义文本颜色。  
- **Pen** 稍后用于在文本周围绘制矩形（可选）。  
- **Font** 为 *在图像上绘制字符串* 操作指定字体、大小和样式。

## 步骤 3：定义文本和矩形

`Rectangle` 定义放置文本的边界框，指定 X/Y 坐标以及宽度/高度。

`Rectangle` 指定矩形区域的位置和大小，此处用于限定绘制的文本。  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` 决定文本放置的位置。根据布局需要调整坐标和尺寸。

## 步骤 4：绘制矩形和文本

`Graphics.DrawString` 使用提供的字体和画刷在指定矩形内渲染文本。

`Graphics.DrawString` 使用给定的字体和画刷在指定矩形内渲染一段文本。  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

首先我们用蓝色矩形勾勒出区域，然后通过调用 `DrawString` **向 bitmap 添加文本**。这就是在图像上 *绘制文本* 的核心。

## 步骤 5：保存结果

图像将保存为 PNG 文件，满足 *将 bitmap 保存为 PNG* 的要求。请将占位路径替换为实际想要存放文件的文件夹。

`bitmap.Save` 将图像写入指定格式的文件，例如 PNG。  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## 常见用例

- **生成带有个性化姓名的证书**。  
- **为网页图库创建带水印的缩略图**。  
- **构建包含标签或注释的动态图表**。  

## 故障排除与技巧

- **未找到字体？** 确保该字体已安装在主机上，或使用私有字体集合。  
- **文本被截断？** 增大矩形尺寸或减小字体大小。  
- **性能问题？** 尽可能复用同一个 `Graphics` 对象进行多次绘制操作。  

## 常见问题

**问：如何将输出格式更改为 JPEG？**  
答：在 `Save` 方法中将 `.png` 扩展名替换为 `.jpg`，并可选地指定 `ImageCodecInfo` 以设置 JPEG 质量。

**问：我可以绘制多行文本吗？**  
答：可以，在字符串中包含换行符 (`\n`) 或使用带有 `FormatFlags.LineLimit` 的 `StringFormat`。

**问：有没有办法在绘制前测量文本大小？**  
答：使用 `Graphics.MeasureString` 获取渲染文本的精确尺寸。

**问：Aspose.Drawing 支持 Unicode 字符吗？**  
答：当然。提供包含所需字形的字体，库即可正确渲染。

**问：测试使用的 Aspose.Drawing 版本是什么？**  
答：示例使用 Aspose.Drawing 24.11 for .NET 进行测试。

---

**最后更新：** 2026-09-23  
**测试版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相关教程

- [创建位图图形 C# – 保存 PNG 图像并使用 Aspose.Drawing 中已安装的字体](/drawing/net/text-and-fonts/installed-fonts/)
- [如何使用 Aspose.Drawing API for .NET 将位图保存为 PNG](/drawing/net/image-editing/display/)
- [图像上的文字](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}