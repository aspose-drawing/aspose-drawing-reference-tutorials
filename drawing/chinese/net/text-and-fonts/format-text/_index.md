---
date: 2026-07-17
description: 了解如何通过在 Aspose.Drawing for .NET 中设置文本对齐来防止文本溢出，并向图像添加文本。一步一步的指南并附有示例。
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: 使用 Aspose.Drawing for .NET 设置文本对齐
og_description: 通过在 Aspose.Drawing for .NET 中设置文本对齐来防止文本溢出。了解如何在图像上绘制字符串、在矩形中居中文本，以及替换
  System.Drawing。
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: 防止文本溢出 – 使用 Aspose.Drawing for .NET 设置文本对齐
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: 防止文本溢出 – 使用 Aspose.Drawing for .NET 设置文本对齐
url: /zh/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 防止文本溢出 – 使用 Aspose.Drawing 设置文本对齐

## 介绍

当您在 .NET 中渲染图形时需要 **防止文本溢出**，Aspose.Drawing 为您提供对文本位置、对齐和换行的细粒度控制。无论您是在构建徽章生成器、动态报告，还是任何基于图像的输出，掌握文本对齐都能确保文本保持在预定矩形内部并呈现出精致的效果。在本指南中，我们将演示如何创建位图画布、配置 `StringFormat`、绘制带居中文本的矩形、处理溢出，最后保存图像。

## 快速答案
- **“设置文本对齐”是什么意思？** 它定义了文本在绘图矩形内的水平和垂直定位方式。  
- **哪个类控制对齐？** `StringFormat` 让您设置 `Alignment` 和 `LineAlignment`。  
- **我可以同时绘制字符串和矩形吗？** 可以——先使用 `Graphics.DrawRectangle`，再调用 `Graphics.DrawString`。  
- **如何防止文本溢出？** 调整矩形大小或手动将文本拆分为多行。  
- **生产环境需要许可证吗？** 商业版 Aspose.Drawing 许可证是非评估使用的必需品。

## 什么是 Aspose.Drawing 中的 **set text alignment**？

`set text alignment` 配置了水平（`StringAlignment`）和垂直（`LineAlignment`）在 `Rectangle` 或绘图区域内的文本放置方式。通过调整这些属性，您可以控制文本是左对齐、居中、右对齐，或是顶部、居中、底部对齐，从而在使用 Aspose.Drawing 生成的徽章、报告等图形中实现精确布局。

## 为什么在文本对齐中使用 Aspose.Drawing？

Aspose.Drawing 消除了 `System.Drawing.Common` 的 GDI+ 限制。它支持 **5 大 .NET 运行时** – .NET Framework 4.6+、.NET Core 2.0+、.NET 5、.NET 6 和 .NET 7 – 并且能够渲染最高 **4000 × 4000 px**（约 100 MB）的图像而不会耗尽内存。抗锯齿、高 DPI 缩放以及完整的 Linux 容器兼容性，使您能够在任何部署场景下生成像素完美的图形。

## 前置条件

1. **Aspose.Drawing 库** – 在此处下载 [here](https://releases.aspose.com/drawing/net/)。  
2. **开发环境** – Visual Studio 2022（或任何 C# IDE）。  
3. **基本 .NET 知识** – 您应熟悉 C# 项目和 NuGet 包的使用。

## 导入命名空间

首先，将所需的命名空间引入作用域。这些命名空间为您提供图形、文本渲染和绘图基元的访问权限。

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 如何使用 Aspose.Drawing 防止文本溢出？

`Bitmap` 是表示内存中图像的类，而 `RectangleF` 定义了用于绘制的浮点矩形区域。通过使用 `StringFormat` 并将 `Trimming` 设置为 `StringTrimming.EllipsisCharacter`，多余字符会自动替换为省略号，确保文本永不超出矩形边界。先测量字符串可以让您决定是缩小矩形还是将文本拆分为多行，从而保证布局整洁且不溢出。

加载位图，定义合适大小的 `RectangleF`，并使用 `StringFormat`（`Trimming` 为 `StringTrimming.EllipsisCharacter`）自动截断多余字符。若需完全控制，可使用 `Graphics.MeasureString` 测量字符串后再缩小矩形或拆分文本后再绘制。此方法确保没有字符会超出可视范围。

## 步骤 1：创建 Bitmap 和 Graphics 对象  

`Bitmap` 表示内存中的图像，而 `Graphics` 为该位图提供绘图方法。创建位图即得到一个可以绘制的画布。`Graphics` 对象是绘图表面，我们通过 `TextRenderingHint` 启用高质量文本渲染。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## 步骤 2：定义 **StringFormat** 和样式  

`StringFormat` 指定文本布局选项，如对齐、行间距和修剪。这里我们通过配置 `StringFormat` 实例 **设置文本对齐**。同时我们准备画刷、画笔和将在绘制字符串时使用的字体。

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## 步骤 3：创建并格式化文本 – **how to draw string** 和 **draw rectangle with text**

`Graphics.DrawString` 将文本渲染到画布上，`Graphics.DrawRectangle` 绘制矩形形状。我们组合文本，定义包含文本的矩形，然后绘制矩形边框和字符串本身。

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### 如何处理文本溢出

如果提供的 `text` 超出矩形边界，您有两种常见选项：

1. **调整矩形大小** – 增加 `rectangle.Width` 或 `rectangle.Height`。  
2. **拆分文本** – 将字符串拆分为适合的行，然后对每行调用 `DrawString` 并调整 Y 坐标。

## 如何使用 Aspose.Drawing 在图像上绘制字符串？

`Graphics.DrawString` 使用指定的字体和格式选项绘制文本。先从位图实例化 `Graphics` 对象，然后使用准备好的 `StringFormat` 调用 `DrawString`。此单次调用即可在您期望的位置精确渲染文本，遵循对齐、修剪以及任何已应用的变换矩阵。添加高质量渲染提示可确保在高 DPI 显示器上输出保持清晰。

## 如何在矩形中居中文本？

`StringAlignment` 决定文本在布局矩形内的水平对齐方式。设置 `stringFormat.Alignment = StringAlignment.Center` 并 `stringFormat.LineAlignment = StringAlignment.Center` 即可实现水平和垂直居中。这在徽章、按钮或标签覆盖等场景中非常理想，且在不同图像尺寸和 DPI 设置下均能保持平衡的视觉效果。

## 如何实现垂直文本对齐？

`LineAlignment` 控制文本在矩形内部的垂直位置。使用 `stringFormat.LineAlignment` 并取值 `StringAlignment.Near`、`Center` 或 `Far`，即可将文本定位在矩形的顶部、居中或底部。如需在旋转文本时保持垂直对齐，可结合 `Graphics.TranslateTransform` 使用。调整行对齐可确保多行文本块在经过变换后仍准确对齐。

## 步骤 4：保存输出 – **add text to image**

最后，将位图写入磁盘。此步骤演示了在单次调用中 **add text to image** 的完整过程。

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## 常见问题与解决方案

| 问题 | 解决方案 |
|-------|----------|
| **文本模糊** | 确保 `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` 已设置。 |
| **文本被截断** | 增大矩形尺寸或通过测量字符串大小 (`Graphics.MeasureString`) 启用自动换行逻辑。 |
| **未找到字体** | 确认该字体已安装在主机机器上，或使用 `PrivateFontCollection` 嵌入私有字体。 |
| **颜色异常** | 再次检查画笔和笔的颜色；记住 `Color.FromKnownColor` 使用系统预定义颜色。 |

## 常见问答

**Q1：Aspose.Drawing 是否兼容所有 .NET 版本？**  
A1：是的，Aspose.Drawing 设计为兼容广泛的 .NET 版本，为开发者提供灵活性。

**Q2：我可以进一步自定义字体样式吗？**  
A2：当然！调整 `Font` 对象的参数即可实现所需的字体大小、样式和族。

**Q3：如何在定义的矩形内处理文本溢出？**  
A3：您可以通过调整矩形大小或实现自定义逻辑来处理过长文本。

**Q4：Aspose.Drawing 还有其他格式化选项吗？**  
A4：有，Aspose.Drawing 提供了一整套图形操作工具，包括文本、形状等多种格式化选项。

**Q5：在哪里可以找到 Aspose.Drawing 的其他支持？**  
A5：访问 Aspose.Drawing 论坛 [here](https://forum.aspose.com/c/drawing/44) 获取社区支持和讨论。

### 附加问答

**问：如何在没有矩形的情况下绘制字符串？**  
答：省略 `DrawRectangle` 调用，直接将期望的 `PointF` 位置传递给 `Graphics.DrawString`。

**问：在保持对齐的情况下，我可以旋转文本吗？**  
答：可以——在绘制前对 `Graphics` 对象应用 `Matrix` 变换，绘制后再重置即可。

**问：是否可以将图像导出为 JPEG 而不是 PNG？**  
答：只需在 `bitmap.Save` 中更改文件扩展名为 `.jpeg`，并可选地指定 `ImageFormat.Jpeg`。

****最后更新:** 2026-07-17  
**已测试于:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [如何使用 Aspose.Drawing for .NET 绘制文本](/drawing/net/text-and-fonts/draw-text/)
- [在 Aspose.Drawing 中向图像添加文本](/drawing/net/use-cases/text-on-image/)
- [如何使用 Aspose.Drawing for .NET 绘制文本和字体](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}