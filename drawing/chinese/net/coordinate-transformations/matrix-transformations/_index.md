---
date: 2026-08-28
description: 学习此 matrix transformation 教程，适用于 Aspose.Drawing .NET，涵盖如何 draw rotated
  rectangle、apply matrix rotation 和 perform matrix scaling（C#）。
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- matrix rotation c#
- matrix scaling c#
- Aspose.Drawing graphics
lastmod: 2026-08-28
linktitle: Matrix Transformations in Aspose.Drawing
og_description: Matrix transformation 教程，适用于 Aspose.Drawing .NET。学习如何在几分钟内使用 C# draw
  rotated rectangle、apply matrix rotation、translate 和 scale graphics。
og_image_alt: Screenshot of a rotated rectangle created with Aspose.Drawing using
  matrix transformations
og_title: Matrix transformation 教程 – apply rotation, scaling and translation in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  headline: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  type: TechArticle
- description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  name: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  steps:
  - name: set up the canvas
    text: Create a bitmap that will serve as the drawing surface. We also clear it
      with a neutral gray background so the transformed shapes stand out. > **Pro
      tip:** Using `Format32bppPArgb` ensures correct alpha handling when you later
      apply anti‑aliasing.
  - name: define the original rectangle
    text: This rectangle is the base shape we’ll transform. Its coordinates are chosen
      to keep it well within the canvas bounds.
  - name: rotate the rectangle (draw rotated rectangle)
    text: The `Matrix` class is Aspose.Drawing's representation of a 3 × 3 affine
      transformation matrix used for rotation, scaling and translation. We now **apply
      matrix rotation** of 15 degrees around the origin. The helper method `TransformPath`
      (shown later) takes a lambda that receives a `Matrix` instance
  - name: translate the rectangle
    text: Translation moves the shape without altering its size or orientation. Here
      we shift it left‑up by 250 pixels.
  - name: scale the rectangle (matrix scaling C#)
    text: Scaling changes the rectangle’s dimensions. A factor of `0.3f` reduces both
      width and height to 30 % of the original size.
  - name: save the result
    text: Finally, write the transformed image to disk. Adjust the path to point to
      a folder that exists on your machine. > **Note:** The `TransformPath` method
      (used in the steps above) creates a `GraphicsPath` from the rectangle, applies
      the supplied matrix, and draws the transformed shape. It’s a compact w
  type: HowTo
- questions:
  - answer: The documentation is available **[here](https://reference.aspose.com/drawing/net/)**.
    question: Where can I find the Aspose.Drawing documentation?
  - answer: Obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: How do I get a temporary license for Aspose.Drawing?
  - answer: Visit the Aspose.Drawing forum **[here](https://forum.aspose.com/c/drawing/44)**.
    question: Where can I seek support or connect with the community?
  - answer: Yes, download it from **[here](https://releases.aspose.com/drawing/net/)**.
    question: Can I download Aspose.Drawing for .NET?
  - answer: Purchase your license **[here](https://purchase.aspose.com/buy)**.
    question: How can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- matrix transformation
- Aspose.Drawing
- .NET graphics
- C# drawing
- cross‑platform rendering
title: Matrix transformation 教程：matrix transformations in Aspose.Drawing for .NET
url: /zh/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 矩阵变换教程：Aspose.Drawing 在 .NET 中的矩阵变换

## 介绍

在本 **矩阵变换教程** 中，您将了解 Aspose.Drawing 的 `Matrix` 类如何实现旋转、平移和缩放图形对象，并达到像素级的精确度。无论您是在构建图表编辑器、生成自动化报告，还是为服务器端服务添加视觉效果，掌握矩阵变换对于在 Windows、Linux 和 macOS 上生成专业外观的输出都是必不可少的。

## 快速答案
- **本教程涵盖什么内容？** 它展示了如何使用 Aspose.Drawing 的矩阵 API 旋转、平移和缩放矩形。  
- **我需要许可证吗？** 免费试用可用于开发；生产环境需要商业许可证。  
- **支持哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7 及更高版本。  
- **实现需要多长时间？** 完整示例大约需要 10‑15 分钟。  
- **我可以看到输出图像吗？** 可以——教程会保存 PNG，您可以立即打开。

## 什么是矩阵变换教程？

矩阵变换教程解释了如何使用 3 × 3 仿射矩阵来移动、旋转、缩放或剪切图形原语。在 Aspose.Drawing 中，`Matrix` 类封装了这些操作，允许对任何 `GraphicsPath` 或形状进行单个可重用对象的变换。

## 为什么在矩阵变换中使用 Aspose.Drawing？

Aspose.Drawing 支持 **三大操作系统**（Windows、Linux、macOS），并且能够在典型服务器硬件上每次操作在 **200 ms** 以下渲染最高达 **10,000 × 10,000 px** 的图像。该库提供 **100 % GDI+ API 兼容性**，因此您可以在不重写逻辑的情况下迁移现有的 System.Drawing 代码，同时避免在非 Windows 平台上 System.Drawing.Common 的许可限制。

## 先决条件

- 可用的 C# 开发环境（Visual Studio、Rider 或 VS Code）。  
- 已安装 Aspose.Drawing for .NET ——如果尚未下载，请从官方站点 **[此处](https://releases.aspose.com/drawing/net/)** 或 **[此链接](https://releases.aspose.com/drawing/net/)** 下载。  
- 对位图画布、矩形和图形路径有基本了解。

## 导入命名空间

首先，将所需的命名空间引入作用域：

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

这些命名空间为您提供对 `Bitmap`、`Graphics` 和用于变换的 `Matrix` 类的访问。

## 分步指南

下面是一段简明的编号演练。每一步都包含简要说明以及您需要的完整代码（代码块保持原样）。

### 步骤 1：设置画布

创建一个位图作为绘图表面。我们还使用中性灰色背景进行清除，以便变换后的形状更加突出。

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **技巧提示：** 使用 `Format32bppPArgb` 可确保在后续进行抗锯齿时正确处理 alpha。

### 步骤 2：定义原始矩形

此矩形是我们将要变换的基础形状。其坐标选择在画布范围内，以确保完全可见。

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### 步骤 3：旋转矩形（绘制旋转矩形）

`Matrix` 类是 Aspose.Drawing 对 3 × 3 仿射变换矩阵的表示，用于旋转、缩放和位移。我们现在 **应用矩阵旋转**，以原点为中心旋转 15 度。辅助方法 `TransformPath`（后面展示）接受一个 lambda，传入 `Matrix` 实例。

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### 步骤 4：平移矩形

平移在不改变大小或方向的情况下移动形状。这里我们将其向左上移动 250 像素。

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### 步骤 5：缩放矩形（矩阵缩放 C#）

缩放会改变矩形的尺寸。因子 `0.3f` 将宽度和高度均缩小至原始的 30 %。

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### 步骤 6：保存结果

最后，将变换后的图像写入磁盘。请将路径调整为指向您机器上存在的文件夹。

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **注意：** 在上述步骤中使用的 `TransformPath` 方法从矩形创建 `GraphicsPath`，应用提供的矩阵，并绘制变换后的形状。这是一种在每次变换中复用相同绘图逻辑的简洁方式。

## 常见问题与解决方案

| 问题 | 解决方案 |
|-------|----------|
| **图像为空白** | 确保输出目录存在且您拥有写入权限。 |
| **变换看起来偏移中心** | 请记住 `Matrix.Rotate` 围绕原点 (0,0) 旋转。旋转前先将形状平移到所需的枢轴点。 |
| **大图像性能下降** | 仅在需要时使用 `graphics.SmoothingMode = SmoothingMode.AntiAlias;`，并及时释放 `Graphics` 对象。 |

## 常见问题

**问：在哪里可以找到 Aspose.Drawing 文档？**  
答：文档可在 **[此处](https://reference.aspose.com/drawing/net/)** 获取。

**问：如何获取 Aspose.Drawing 的临时许可证？**  
答：可在 **[此处](https://purchase.aspose.com/temporary-license/)** 获取临时许可证。

**问：在哪里可以寻求支持或加入社区？**  
答：请访问 Aspose.Drawing 论坛 **[此处](https://forum.aspose.com/c/drawing/44)**。

**问：我可以下载 Aspose.Drawing for .NET 吗？**  
答：可以，从 **[此处](https://releases.aspose.com/drawing/net/)** 下载。

**问：如何购买 Aspose.Drawing？**  
答：请在 **[此处](https://purchase.aspose.com/buy)** 购买许可证。

## 结论

您已完成使用 Aspose.Drawing for .NET 的完整 **矩阵变换教程**。您已经掌握了如何 **绘制旋转矩形**、**应用矩阵旋转**，以及对任意形状执行 **矩阵缩放 C#**。尝试链式多个变换或使用自定义枢轴点，以实现更具创意的图形效果。

---

**最后更新：** 2026-08-28  
**测试版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相关教程

- [如何使用 Aspose.Drawing API for .NET 绘制矩形 – 坐标系变换（页面变换）](/drawing/net/coordinate-transformations/page-transformation/)
- [如何使用 Aspose.Drawing 保存 PNG – 世界变换](/drawing/net/coordinate-transformations/world-transformation/)
- [分步变换 – 坐标变换](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}