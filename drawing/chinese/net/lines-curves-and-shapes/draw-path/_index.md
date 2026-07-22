---
date: 2026-07-22
description: 了解如何使用 Aspose.Drawing 将位图保存为 PNG 并导出为 JPEG。一步步指南展示了绘制路径、创建图像以及导出格式。
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: 在 Aspose.Drawing 中绘制路径
og_description: 使用 Aspose.Drawing for .NET 将位图保存为 PNG 并导出为 JPEG。按照本教程绘制复杂路径、创建高质量图像并输出多种格式。
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: 将位图保存为 PNG – 使用 Aspose.Drawing 绘制路径
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: 将位图保存为 PNG – 在 Aspose.Drawing 中使用 GraphicsPath
url: /zh/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Drawing 中绘制路径

## 如何使用 GraphicsPath – 介绍

**Save bitmap as PNG** 通常是当您需要无损图像进行后续处理或发布时的第一步。在本教程中，您将学习如何使用 `GraphicsPath` 绘制复杂的矢量路径，将其渲染到位图上，然后 **save bitmap as PNG** 或甚至 **export image to JPEG**。无论您是构建报表引擎、定制图表库，还是仅仅需要生成动态图形，Aspose.Drawing 为您提供了一个完全托管的跨平台 API，取代了 System.Drawing.Common。

## 快速回答

- **What can I draw with GraphicsPath?** 线条、矩形、椭圆、曲线和自定义形状。  
- **Do I need a license?** 试用版免费；生产环境需要商业许可证。  
- **Which .NET versions are supported?** 支持 .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6+。  
- **Is System.Drawing.Common required?** 不需要，Aspose.Drawing 可独立工作。  
- **Can I save to different formats?** 可以 – PNG、JPEG、BMP、GIF 等。

## 什么是 GraphicsPath？

`GraphicsPath` 是 Aspose.Drawing 的矢量容器，用于将一系列绘图基元（如直线、弧线和曲线）存储为单个对象。通过对这些基元进行分组，您可以统一应用变换、填充规则和笔触设置，从而简化复杂图形的创建，并确保在不同输出格式之间保持一致的渲染。

## 为什么在 Aspose.Drawing 中使用 GraphicsPath？

在 Aspose.Drawing 中使用 GraphicsPath 可为您提供精确、灵活且高性能的矢量绘制能力。它让您能够构建复杂形状、应用变换并高效渲染，同时保持跨平台的一致性并支持大规模图像处理。此外，它还能与其他 .NET 库无缝集成，使您能够在单个应用程序中结合光栅和矢量工作流。

- **Precision:** 处理 50 多种矢量基元，具备亚像素精度，确保在 **save bitmap as PNG** 时输出在任何分辨率下都保持清晰。  
- **Flexibility:** 将直线、弧线和贝塞尔曲线组合成一个路径，然后使用单个 `Graphics.DrawPath` 调用进行渲染。  
- **Performance:** 优化的渲染管线可处理高达 400 MP 的图像，而无需将整个文件加载到内存中，使大规模批处理作业成为可能。  
- **Cross‑Platform:** 在 Windows、Linux 和 macOS 运行时上得到相同的结果，消除平台特定的错误。

## 前置条件

在开始本教程之前，请确保您具备以下前置条件：

- **Aspose.Drawing Library:** 下载并安装 Aspose.Drawing 库。您可以在 [此处](https://releases.aspose.com/drawing/net/) 找到该库。  
- **Other Aspose Products:** 探索其他 Aspose 产品，链接 [此处](https://releases.aspose.com/)。  
- **Development Environment:** 设置您的 .NET 开发环境并安装必要的工具（Visual Studio、.NET SDK 等）。

## 导入命名空间

Start by importing the required namespaces in your project:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 步骤 1：创建 Bitmap 和 Graphics

Bitmap 表示内存中的图像，而 Graphics 提供在该图像上渲染的绘图方法。首先创建一个 `Bitmap` 和一个 `Graphics` 对象以供使用。该位图将作为渲染 `GraphicsPath` 的画布，随后您将 **save bitmap as PNG**：

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步骤 2：定义 Pen 和 GraphicsPath

Pen 定义线条的颜色、宽度和样式；GraphicsPath 将一组绘图基元存储为单个矢量对象。接下来，定义一个 `Pen` 来指定绘图属性，并实例化一个 `GraphicsPath`。`GraphicsPath` 对象在绘制之前保存矢量数据：

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## 步骤 3：添加线条和形状

AddLine、AddRectangle 和 AddEllipse 将相应的形状添加到 GraphicsPath，以便后续渲染。向 `GraphicsPath` 添加线条、矩形和椭圆以创建复杂路径。您还可以添加自定义贝塞尔曲线以获得平滑形状：

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## 步骤 4：绘制路径

DrawPath 使用指定的 Pen 将 GraphicsPath 中的矢量数据渲染到 Graphics 表面上。使用指定的 `Pen` 将路径绘制到 `Graphics` 对象上。此操作将矢量数据光栅化到位图画布上：

```csharp
graphics.DrawPath(pen, path);
```

## 步骤 5：保存图像 – 导出为 PNG 或 JPEG

Bitmap.Save 方法将图像以所选格式（如 PNG 或 JPEG）写入磁盘。绘制完成后，您可以 **save bitmap as PNG** 以获得无损质量，或 **export image to JPEG** 以获得更小的文件大小。请选择最适合您后续场景的格式：

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

根据需要重复这些步骤，以创建复杂且视觉上吸引人的路径。

## 常见问题及解决方案

| 问题 | 解决方案 |
|-------|----------|
| **路径不可见** | 确保 Pen 颜色与背景形成对比，并且位图已正确保存。 |
| **意外的图像尺寸** | 验证位图的尺寸和像素格式是否符合您的要求。 |
| **许可证异常** | 在测试时使用试用许可证；在投入生产前应用有效许可证。 |

## 常见问答

### Q1：我可以将 Aspose.Drawing 与其他 .NET 库一起使用吗？

A1：是的，Aspose.Drawing 可无缝集成其他 .NET 库，为您的开发项目提供多样性。

### Q2：是否提供试用版？

A2：是的，您可以在 [此处](https://releases.aspose.com/) 获取免费试用。

### Q3：在哪里可以找到 Aspose.Drawing 的支持？

A3：访问 Aspose.Drawing [论坛](https://forum.aspose.com/c/drawing/44) 获取帮助和社区支持。

### Q4：如何获取临时许可证？

A4：在 [此处](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

### Q5：我可以购买 Aspose.Drawing 吗？

A5：是的，您可以在 [此处](https://purchase.aspose.com/buy) 购买 Aspose.Drawing。

**附加问答**

**Q: 我可以使用 GraphicsPath 绘制自定义贝塞尔曲线吗？**  
A: 当然可以 – 使用 `path.AddBezier(...)` 定义平滑曲线。

**Q: 在重新使用之前，我如何清除 GraphicsPath？**  
A: 调用 `path.Reset()` 可移除所有图形并重新开始。

## 结论

恭喜！您已成功学习了 **how to use GraphicsPath**（如何使用 GraphicsPath）来绘制路径，并使用 Aspose.Drawing for .NET 将其 **save bitmap as PNG** 或 **export image to JPEG**。本教程涵盖了创建位图、定义笔、构建 `GraphicsPath`、渲染各种形状以及以多种格式导出最终图像。尝试不同的坐标、颜色和线宽，以释放 Aspose.Drawing 的全部创意潜力。

---

**最后更新：** 2026-07-22  
**测试环境：** Aspose.Drawing 24.12 for .NET  
**作者：** Aspose

## 相关教程

- [保存位图为 PNG 并使用 Aspose.Drawing 绘制闭合曲线](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [保存位图 C# – 使用 Aspose.Drawing 绘制贝塞尔样条](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [如何保存图像并在 Aspose.Drawing 中绘制基数样条](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}