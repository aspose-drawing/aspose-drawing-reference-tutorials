---
date: 2026-02-25
description: 学习如何使用 Aspose.Drawing for .NET 绘制文本并创建动态文本图像。本分步指南展示了如何向位图添加文本、在图像上绘制字符串以及将位图保存为
  PNG。
linktitle: How to Draw Text with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing for .NET 绘制文本
url: /zh/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing for .NET 绘制文本

## Introduction

在本分步指南中，您将学习 **如何在图像上绘制文本**，使用 Aspose.Drawing for .NET。无论您需要创建 *动态文本图像*、向现有位图添加文本，还是使用自定义字体生成图形，本教程将逐步讲解所有细节，让您在几分钟内开始绘制文本。

## Quick Answers
- **使用的库是什么？** Aspose.Drawing for .NET  
- **主要任务？** 在图像上绘制文本（创建带文本的图像）  
- **关键方法？** `Graphics.DrawString`（在图像上绘制字符串）  
- **输出格式？** PNG（将位图保存为 PNG）  
- **前置条件？** .NET 开发环境和 Aspose.Drawing 库  

## What is drawing text with Aspose.Drawing?
Aspose.Drawing 提供了一个完全托管的 API，镜像经典的 GDI+ 模型，同时增加了跨平台支持。它让您在不依赖 System.Drawing.Common 的情况下渲染高质量的文本、形状和图像。

## Why use Aspose.Drawing to add text to images?
- **跨平台可靠性** – 在 Windows、Linux 和 macOS 上均可工作。  
- **高级渲染** – 抗锯齿和子像素文本平滑，输出清晰。  
- **无外部依赖** – 库已打包所有创建带文本图像所需的内容。

## Prerequisites

在开始之前，请确保您已拥有：

- **Aspose.Drawing for .NET** – 从 [Aspose.Drawing 文档](https://reference.aspose.com/drawing/net/) 下载。  
- **.NET IDE**，如 Visual Studio 或 VS Code。  

## Import Namespaces

首先导入所需的命名空间：

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step 1: Create Bitmap and Graphics Objects

步骤 1：创建 Bitmap 和 Graphics 对象

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

这里我们创建一个用于保存最终图像的 `Bitmap`，以及一个用于在其上绘图的 `Graphics` 对象。抗锯齿提示确保文本平滑。

## Step 2: Set Up Brush, Pen, and Font

步骤 2：设置 Brush、Pen 和 Font

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** 定义文本颜色。  
- **Pen** 用于随后绘制文本周围的矩形（可选）。  
- **Font** 指定用于 *在图像上绘制字符串* 操作的字体、大小和样式。

## Step 3: Define Text and Rectangle

步骤 3：定义文本和矩形

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` 决定文本放置的位置。根据布局调整坐标和尺寸。

## Step 4: Draw Rectangle and Text

步骤 4：绘制矩形和文本

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

首先使用蓝色矩形勾勒出区域，然后通过调用 `DrawString` **向位图添加文本**。这就是在图像上 *绘制文本* 的核心。

## Step 5: Save the Result

步骤 5：保存结果

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

图像以 PNG 文件保存，满足 *将位图保存为 PNG* 的要求。将占位路径替换为实际想要存放文件的文件夹。

## Common Use Cases

常见使用场景

- **生成带有个性化姓名的证书**。  
- **为网页相册创建带水印的缩略图**。  
- **构建包含标签或注释的动态图表**。  

## Troubleshooting & Tips

故障排除与技巧

- **找不到字体？** 确认该字体已安装在主机上，或使用私有字体集合。  
- **文本被截断？** 增大矩形尺寸或减小字体大小。  
- **性能问题？** 尽可能复用同一个 `Graphics` 对象进行多次绘制。

## FAQ's

### Q1: 我可以在 Aspose.Drawing for .NET 中使用自定义字体吗？

A1: 可以，在代码中创建 `Font` 对象时可以指定自定义字体。

### Q2: 如何添加粗体或斜体等文本效果？

A2: 调整 `Font` 对象的 `FontStyle` 属性。例如，使用 `FontStyle.Bold` 实现粗体。

### Q3: Aspose.Drawing 与 .NET Core 兼容吗？

A3: 是的，Aspose.Drawing 支持 .NET Core，可用于跨平台应用。

### Q4: 我可以在已有图像上绘制文本吗？

A4: 当然！使用 `Bitmap.FromFile()` 加载已有图像，然后继续文本绘制步骤。

### Q5: 是否有 Aspose.Drawing 支持的社区论坛？

A5: 有，您可以在 [Aspose.Drawing 论坛](https://forum.aspose.com/c/drawing/44) 获取支持并讨论问题。

## Frequently Asked Questions

**问：如何将输出格式改为 JPEG？**  
答：在 `Save` 方法中将 `.png` 扩展名改为 `.jpg`，并可选地指定 `ImageCodecInfo` 以设置 JPEG 质量。

**问：可以绘制多行文本吗？**  
答：可以，在字符串中加入换行符 (`\n`) 或使用带 `FormatFlags.LineLimit` 的 `StringFormat`。

**问：有没有办法在绘制前测量文本大小？**  
答：使用 `Graphics.MeasureString` 获取渲染文本的精确尺寸。

**问：Aspose.Drawing 支持 Unicode 字符吗？**  
答：完全支持。提供包含所需字形的字体，库即可正确渲染。

**问：测试使用的 Aspose.Drawing 版本是什么？**  
答：示例在 Aspose.Drawing 24.11 for .NET 上进行测试。

---

**最后更新：** 2026-02-25  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}