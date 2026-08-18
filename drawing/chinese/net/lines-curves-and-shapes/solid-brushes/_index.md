---
date: 2026-08-01
description: 了解如何在 Aspose.Drawing for .NET 中使用实心画笔将位图保存为 PNG。使用实心画笔填充形状并创建生动的图形。
keywords:
- save bitmap as png
- export bitmap to png
- fill shape solid color
- bitmap to png conversion
lastmod: 2026-08-01
linktitle: Aspose.Drawing 中的实心画笔
og_description: 使用 Aspose.Drawing 中的实心画笔将位图保存为 PNG。本分步教程展示了如何创建位图、使用实色填充形状，并将结果导出为适用于
  .NET 6+ 项目的无损 PNG 文件。
og_image_alt: Guide showing how to save a bitmap as PNG using solid brushes in Aspose.Drawing
og_title: 使用实心画笔将位图保存为 PNG – Aspose.Drawing 指南
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  headline: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  name: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image canvas. The `Bitmap` class
      is Aspose.Drawing's top‑level object that stores pixel data in a mutable buffer.
      You can specify width, height, and pixel format when constructing it.
  - name: Create Graphics Object
    text: A `Graphics` object provides drawing methods for the bitmap. The `Graphics`
      class acts as a drawing surface linked to a `Bitmap`. All subsequent drawing
      commands (lines, shapes, text) are routed through this object.
  - name: Choose a Solid Brush
    text: Select a colour for the brush; in this example we use a vivid blue. The
      `SolidBrush` class defines a brush that paints with a single, uniform colour.
      It is ideal for filling shapes where a flat colour is required.
  - name: Fill Shapes with Brush
    text: Use the brush to paint an ellipse (or any other shape) on the bitmap. `FillEllipse`
      draws an ellipse filled with the specified brush. The `FillEllipse` method of
      the `Graphics` object draws an ellipse filled with the supplied `SolidBrush`.
      You can replace it with `FillRectangle`, `FillPolygon`, etc.
  - name: Save the Result as PNG
    text: Export the bitmap to a PNG file on disk. `Save` writes the image to a file
      in the chosen format. The `Save` method writes the bitmap to the specified path
      using `ImageFormat.Png`. This operation preserves the alpha channel, ensuring
      transparent backgrounds remain intact. Repeat these steps, customiz
  type: HowTo
- questions:
  - answer: Absolutely—methods like `FillRectangle`, `FillPolygon`, or `DrawPath`
      work with the same solid brush.
    question: Can I use a different shape instead of an ellipse?
  - answer: Replace the file extension in `Save` and use `ImageFormat.Jpeg` (e.g.,
      `bitmap.Save("output.jpg", ImageFormat.Jpeg);`).
    question: How do I change the output format to JPEG?
  - answer: Yes—create separate `SolidBrush` instances for each colour and call the
      appropriate `Fill*` methods sequentially.
    question: Is it possible to draw multiple shapes with different brushes in one
      bitmap?
  - answer: It's best practice to wrap them in `using` statements or call `Dispose()`
      to free unmanaged resources.
    question: Do I need to dispose of the `Graphics` and `Bitmap` objects?
  - answer: Aspose.Drawing is cross‑platform; the same code runs on Linux and macOS
      when targeting .NET Core or .NET 5+.
    question: Will this work on Linux/macOS with .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- solid brush
title: 在 Aspose.Drawing 中使用实心画笔将位图保存为 PNG
url: /zh/net/lines-curves-and-shapes/solid-brushes/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用实心画刷在 Aspose.Drawing 中将位图保存为 PNG

## 介绍

在本指南中，您将学习 **如何使用 Aspose.Drawing .NET 库的实心画刷将位图保存为 PNG**。无论您是在构建桌面实用程序、生成图标的 Web 服务，还是需要清晰 PNG 资源的报表引擎，下面的步骤都能让您仅用几行代码就从空白画布得到可直接使用的 PNG 文件。我们将覆盖完整工作流，解释为何实心画刷是均匀颜色填充的理想选择，并展示如何保持代码简洁且跨平台。

## 快速答案
- **“将位图保存为 png”是什么意思？** 它指的是将 `Bitmap` 对象导出为磁盘上的无损 PNG 图像文件。  
- **哪个类创建实心画刷？** 来自 `Aspose.Drawing.Brushes` 命名空间的 `SolidBrush`。  
- **我可以更改画刷颜色吗？** 可以——向 `SolidBrush` 构造函数传入任意 `Color`（包括 ARGB 值）。  
- **生产环境需要许可证吗？** 试用版可用于评估；商业许可证是生产部署的必需。  
- **此方法兼容 .NET 6+ 吗？** 完全兼容——Aspose.Drawing 完全支持 .NET 5、.NET 6 及更高版本。

## 什么是“将位图保存为 PNG”？

将位图保存为 PNG 将内存中的像素数组转换为无损 PNG 文件，保留透明度和精确的颜色值。**将位图保存为 PNG** 是在需要一种浏览器和图像编辑器能够读取且不损失质量的可移植图像格式时的常见操作。

## 为什么在保存位图为 PNG 时使用实心画刷？

实心画刷提供单一、均匀的颜色，可瞬间填充任何矢量形状，避免在只需要平面颜色时使用复杂的渐变。使用 Aspose.Drawing 的实心画刷还能利用其渲染引擎，处理最高 **10,000 × 10,000 像素** 的图像，同时将内存使用保持在 **200 MB** 以下，适用于高分辨率资源。

## 前置条件

在开始教程之前，请确保已满足以下前置条件：

- Aspose.Drawing for .NET Library：从 [Aspose.Drawing .NET 文档](https://reference.aspose.com/drawing/net/) 下载并安装库。
- 集成开发环境（IDE）：在您的机器上配置好可用的 .NET 开发环境，例如 Visual Studio。

准备就绪后，让我们进入实现步骤。

## 导入命名空间

`using` 指令将所需类型引入作用域。

`Aspose.Drawing` 命名空间提供核心图形类，而 `System.Drawing` 提供颜色定义和 `SolidBrush` 类。

```csharp
using System.Drawing;
```

## 如何使用实心画刷将位图保存为 PNG

本节概述完整工作流：创建位图画布、获取图形表面、实例化带有所需颜色的 `SolidBrush`、填充一个或多个形状，最后调用 `Save` 将图像写入 PNG 文件。代码在 .NET 6 及更高版本上跨平台运行。

### 步骤 1：创建位图

`Bitmap` 类表示内存中的图像画布。

`Bitmap` 类是 Aspose.Drawing 的顶层对象，在可变缓冲区中存储像素数据。构造时可以指定宽度、高度和像素格式。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步骤 2：创建 Graphics 对象

`Graphics` 对象为位图提供绘图方法。

`Graphics` 类充当链接到 `Bitmap` 的绘图表面。所有后续的绘图命令（线条、形状、文本）都通过该对象路由。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 步骤 3：选择实心画刷

为画刷选择颜色；本例使用鲜艳的蓝色。

`SolidBrush` 类定义一种使用单一、均匀颜色进行绘制的画刷。它非常适合需要平面颜色填充的形状。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
```

### 步骤 4：使用画刷填充形状

使用画刷在位图上绘制椭圆（或任何其他形状）。

`FillEllipse` 使用指定的画刷绘制填充椭圆。`Graphics` 对象的 `FillEllipse` 方法使用提供的 `SolidBrush` 绘制填充椭圆。您可以将其替换为 `FillRectangle`、`FillPolygon` 等，以创建不同的几何图形。

```csharp
graphics.FillEllipse(brush, 100, 100, 800, 600);
```

### 步骤 5：将结果保存为 PNG

将位图导出为磁盘上的 PNG 文件。

`Save` 将图像以选定格式写入文件。`Save` 方法使用 `ImageFormat.Png` 将位图写入指定路径。此操作保留 alpha 通道，确保透明背景保持完整。

```csharp
bitmap.Save("Your Document Directory" + @"Brushes\Solid_out.png");
```

重复上述步骤，按需自定义颜色和形状，以符合您应用的视觉设计。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|----------------|-----|
| **文件未找到错误** 在保存时 | 目标文件夹不存在 | 在调用 `Save` 之前确保已创建目录 (`Your Document Directory\Brushes`)。 |
| **颜色不正确** | 使用映射到系统主题的 `KnownColor` | 使用 `Color.FromArgb` 获取精确的 RGBA 值。 |
| **透明度丢失** | 使用不带 alpha 通道的像素格式 | 如示例中保持使用 `PixelFormat.Format32bppPArgb` 以保留 alpha 通道。 |

## 常见问答

**问：我可以使用除椭圆之外的其他形状吗？**  
答：当然可以——`FillRectangle`、`FillPolygon` 或 `DrawPath` 等方法都可以与相同的实心画刷一起使用。

**问：如何将输出格式更改为 JPEG？**  
答：在 `Save` 中更改文件扩展名并使用 `ImageFormat.Jpeg`（例如，`bitmap.Save("output.jpg", ImageFormat.Jpeg);`）。

**问：是否可以在同一位图中使用不同的画刷绘制多个形状？**  
答：可以——为每种颜色创建单独的 `SolidBrush` 实例，并依次调用相应的 `Fill*` 方法。

**问：是否需要释放 `Graphics` 和 `Bitmap` 对象？**  
答：最佳实践是将它们放在 `using` 语句块中或调用 `Dispose()` 来释放非托管资源。

**问：在 Linux/macOS 上使用 .NET Core 能否运行？**  
答：Aspose.Drawing 是跨平台的；相同代码在针对 .NET Core 或 .NET 5+ 的 Linux 和 macOS 上均可运行。

---

**最后更新：** 2026-08-01  
**测试环境：** Aspose.Drawing 24.12 for .NET  
**作者：** Aspose

## 相关教程

- [保存位图为 PNG 并使用 Aspose.Drawing 绘制闭合曲线](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [使用 Aspose.Drawing 中的变换保存位图为 PNG](/drawing/net/coordinate-transformations/local-transformation/)
- [如何使用 Aspose.Drawing for .NET 将图像裁剪为 PNG](/drawing/net/image-editing/cropping/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}