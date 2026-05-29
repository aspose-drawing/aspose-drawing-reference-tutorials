---
date: 2026-05-29
description: 了解如何在 .NET 中使用 Aspose.Drawing 保存 PNG 并绘制 Cardinal Splines。将曲线保存为 PNG，创建平滑图形，并轻松生成位图文件。
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: 在 Aspose.Drawing 中绘制 Cardinal Splines
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 使用 Aspose.Drawing 保存 PNG 并绘制 Cardinal Splines 的教程
url: /zh/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何保存 PNG 并使用 Aspose.Drawing 绘制基数样条

## 介绍

在本教程中，您将了解 **如何保存 PNG** 文件，同时使用 Aspose.Drawing for .NET 绘制平滑的基数样条。无论您是在构建图表组件、图表编辑器，还是仅仅需要将自定义曲线导出为 PNG，下面的步骤将指导您创建位图画布、使用笔绘制样条，并将结果持久化到磁盘。您还将看到为什么 Aspose.Drawing 是 System.Drawing.Common 的可靠跨平台替代方案。

## 快速答案
- **主要方法的作用是什么？** `Graphics.DrawCurve` 将一系列点插值为平滑的基数样条。  
- **使用哪种格式保存图像？** 通过 `Bitmap.Save` 保存为 PNG。  
- **保存图像是否需要许可证？** 开发阶段使用试用版即可；生产环境需要商业许可证。  
- **可以更改曲线张力吗？** 可以，`DrawCurve` 的重载允许您指定张力。  
- **Aspose.Drawing 是否兼容 .NET 6+？** 完全兼容——它支持 .NET Framework 和 .NET Core/5/6。

## 在 Aspose.Drawing 中，“如何保存 PNG” 是什么意思？
保存 PNG 指的是将您在内存中绘制的位图转换为磁盘上的实际 PNG 文件。此过程使用无损压缩写入像素数据，保留精确的颜色以及任何 alpha 通道信息。Aspose.Drawing 的 `Bitmap.Save` 方法会自动处理 PNG 编码，您无需自行管理格式细节。

## 为什么使用 Aspose.Drawing 绘制基数样条？
基数样条能够生成平滑、流畅的曲线，紧密跟随一组控制点，非常适合数据可视化、UI 图形和自定义形状。Aspose.Drawing 支持 **30+ 图像格式**，并且可以在不将整个文件加载到内存的情况下渲染数百页图形，提供速度与灵活性的双重优势。

## 先决条件

在开始之前，请确保您具备以下条件：

- 已安装 Visual Studio（任何近期版本）。  
- Aspose.Drawing for .NET 库。您可以在[此处](https://releases.aspose.com/drawing/net/)下载。  
- 基本的 C# 编程知识。

## 导入命名空间

在您的 C# 文件中，首先导入必要的命名空间：

`Aspose.Drawing` 命名空间包含所有核心类型，如 `Bitmap`、`Graphics` 和 `Pen`。  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## 步骤 1：创建位图（画布）

首先，创建一个位图作为绘图的画布。该位图将在 **保存图像** 之前渲染样条。

位图表示具有定义像素格式和尺寸的内存图像。  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步骤 2：创建 Graphics 对象

接下来，从位图获取一个 `Graphics` 对象。该对象提供绘图表面。

Graphics 为在位图上渲染形状、文本和图像提供绘图表面。  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步骤 3：定义 Pen 并绘制曲线

定义一个具有所需颜色和宽度的 `Pen`，然后使用 `DrawCurve` 绘制基数样条。这演示了 **使用笔绘制曲线** 的技术，并作为 **基数样条示例**。

Pen 封装了用于绘制线条和曲线的颜色、宽度和线型。  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## 步骤 4：保存图像（将曲线保存为 PNG）

最后，将位图持久化为 PNG 文件。这是本教程中 **如何保存 PNG** 的核心步骤。

`Bitmap.Save` 将图像以指定格式（如 PNG）写入文件。  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **专业提示：** 使用 `Path.Combine` 在跨平台时安全地构建文件路径。

恭喜！您已成功绘制基数样条并使用 Aspose.Drawing for .NET 将结果保存为 PNG 图像。欢迎尝试不同的点数组、笔颜色或线宽，以自定义您的曲线。

## 常见使用场景

- **数据可视化** – 需要精确控制点的平滑折线图。  
- **自定义 UI 组件** – 绘制旋钮、滑块或装饰性边框。  
- **可导出图形** – 为报告或网页内容即时生成 PNG 资源。

## 故障排除与技巧

- **图像显示为空白？** 确保位图的像素格式支持 alpha（`Format32bppPArgb`），并在需要时调用 `graphics.Clear(Color.Transparent)`。  
- **曲线形状异常？** 使用 `DrawCurve(pen, points, tension)` 重载来调整张力参数。  
- **文件访问错误？** 验证目标目录是否存在，并确保您的应用程序具有写入权限。

## 常见问题

**Q1: 我可以在商业项目中使用 Aspose.Drawing 吗？**  
A1: 可以，Aspose.Drawing 适用于个人和商业项目。请在[购买页面](https://purchase.aspose.com/buy)查看许可详情。

**Q2: 如何获取用于测试的临时许可证？**  
A2: 可在[此处](https://purchase.aspose.com/temporary-license/)获取用于测试的临时许可证。

**Q3: 在哪里可以找到更多支持？**  
A3: 访问[Aspose.Drawing 论坛](https://forum.aspose.com/c/drawing/44)获取社区支持和讨论。

**Q4: 是否提供免费试用？**  
A4: 是的，在购买前可通过[免费试用](https://releases.aspose.com/)版本探索功能。

**Q5: 如何访问文档？**  
A5: 请参考完整的[文档](https://reference.aspose.com/drawing/net/)获取详细信息和示例。

---

**最后更新：** 2026-05-29  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [保存位图为 PNG 并使用 Aspose.Drawing 绘制闭合曲线](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [保存位图 C# – 使用 Aspose.Drawing 绘制贝塞尔样条](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [使用实心画刷在 Aspose.Drawing 中将位图保存为 PNG](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}