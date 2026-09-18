---
date: 2026-09-18
description: 了解如何在 Aspose.Drawing 中绘制 path 并使用 pens 连接路径，然后使用简易的 C# 代码将图像保存为 PNG。
keywords:
- save image as png
- server side image rendering
- raster image from vector
- export graphics to png
- alternative to system drawing
lastmod: 2026-09-18
linktitle: 在 Aspose.Drawing 中使用 pens 连接 paths
og_description: 使用 Aspose.Drawing 将图像保存为 PNG。了解如何绘制 paths、应用 line‑join 样式，并从服务器上的
  vector data 导出高质量的 raster graphics。
og_image_alt: Developer guide showing how to draw and join paths with pens, then save
  the result as a PNG file using Aspose.Drawing
og_title: 如何绘制 path、使用 pens 连接路径并将图像保存为 PNG
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to draw path and join paths with pens in Aspose.Drawing,
    then save the image as PNG using simple C# code.
  headline: How to draw path, join paths with pens and save image as PNG
  type: TechArticle
- questions:
  - answer: Aspose.Drawing is a commercial product, but you can explore its capabilities
      with a **[free trial](https://releases.aspose.com/)**.
    question: Can I use Aspose.Drawing for free?
  - answer: Refer to the **[documentation](https://reference.aspose.com/drawing/net/)**
      for comprehensive guidance.
    question: Where can I find Aspose.Drawing documentation?
  - answer: Visit the **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)**
      for community help and official assistance.
    question: How can I get support for Aspose.Drawing?
  - answer: Yes, you can obtain a **[temporary license](https://purchase.aspose.com/temporary-license/)**
      for short‑term usage.
    question: Are temporary licenses available for Aspose.Drawing?
  - answer: Purchase Aspose.Drawing **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.
    question: Where can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- C# graphics
- save PNG
- vector to raster
- server side rendering
title: 如何绘制 path、使用 pens 连接路径并将图像保存为 PNG
url: /zh/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何绘制路径、使用笔连接路径并将图像保存为 PNG

## 介绍

在本教程中，您将学习如何使用 Aspose.Drawing for .NET **draw path** 对象，使用不同的 line‑join 样式将它们连接，并 **save image as PNG**。无论您是在构建报表引擎、设计编辑器，还是需要为 Web 服务进行服务器端图像渲染，掌握使用笔绘制路径都能让您对矢量到光栅的转换进行精确控制。

## 快速回答
- **“draw path” 是什么意思？** 它创建基于矢量的线条或形状定义，`Graphics` 对象可以对其进行渲染。  
- **可用的线连接方式有哪些？** `Bevel`, `Miter`, `Round`, 和 `BevelClipped`。  
- **我可以将结果导出为 PNG 吗？** 是的——使用 `Bitmap.Save` 并指定 `.png` 扩展名。  
- **我需要许可证吗？** 试用版可用于评估；生产环境需要商业许可证。  
- **支持哪些 .NET 版本？** .NET Framework 4.6+、.NET Core 3.1+ 和 .NET 6+。

## Aspose.Drawing 中的 “draw path” 是什么？

**Draw path** 指构建一个包含一系列线条、曲线或形状的 `GraphicsPath`。  
`GraphicsPath` 是 Aspose.Drawing 用于矢量几何的容器；您随后可以使用 `Pen` 对其进行描边或使用画刷填充。此方法允许您对整个形状应用变换、裁剪以及一致的 line‑join 样式，而无需单独绘制每个段落。

## 为什么在服务器端图像渲染中使用 Aspose.Drawing？

Aspose.Drawing 提供了一个强大的服务器端渲染引擎，可在任何操作系统上运行且不依赖 GDI+，因此非常适合云服务、容器化应用以及需要跨平台兼容性和无头运行的高性能 Web API，确保可扩展的性能。

- **完整的 .NET 兼容性** – 支持 .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6/7。  
- **丰富的 line‑join 选项** – `Bevel`, `Miter`, `Round`, `BevelClipped`。  
- **高质量光栅输出** – 可直接从矢量数据导出到 **10+ 光栅格式**（PNG、JPEG、BMP、GIF、TIFF 等）。  
- **无 GDI+ 限制** – 适用于云服务、容器和无头环境。

## 前置条件

在深入代码之前，请确保您已拥有：

1. **Aspose.Drawing 库** – 从 **[Aspose.Drawing 下载页面](https://releases.aspose.com/drawing/net/)** 下载。  
2. **.NET 开发环境** – Visual Studio、VS Code 或任何支持 C# 的 IDE。

现在一切就绪，让我们逐步演示。

## 导入命名空间

`System.Drawing` 和 `System.Drawing.Drawing2D` 命名空间包含 Aspose.Drawing 使用的核心图形类型。

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 步骤 1：创建位图和图形对象

`Bitmap` 是 Aspose.Drawing 的内存中光栅画布。它表示一个光栅图像，您可以使用 `Graphics` 表面在其上绘制。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

我们从一个大小为 1000 × 800 像素的空白画布（`Bitmap`）开始，并获取一个将渲染绘图指令的 `Graphics` 对象。

## 步骤 2：定义 drawPath 方法

`Pen` 是 Aspose.Drawing 用于描绘矢量轮廓的工具；它定义颜色、粗细和 line‑join 样式。  
`LineJoin` 控制两个线段在拐角处的连接方式。  
`GraphicsPath` 是保存我们将要连接的线段系列的矢量容器。

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

此辅助方法封装了绘图逻辑：

- **Pen** – 设置颜色和粗细（30 px）。  
- **GraphicsPath** – 定义两条相连的线，形成 “L” 形。  
- **LineJoin** – 控制两条线之间拐角的渲染方式（`Bevel`、`Round` 等）。

您可以使用任意 `LineJoin` 值调用此方法，以查看视觉差异。

## 步骤 3：使用 bevel 线连接方式连接路径

`LineJoin.Bevel` 在两条线相交处创建一个平坦的拐角，适用于需要清晰、无重叠连接的情况。

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

## 步骤 4：使用 round 线连接方式连接路径

`LineJoin.Round` 产生平滑的圆角——非常适合更精致的外观。

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

## 步骤 5：将结果保存为 PNG

`Save` 调用将位图以 PNG 格式写入文件，完成 **save image as PNG** 工作流。请根据您的环境调整路径。

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

## 常见问题及解决方案

| 问题 | 产生原因 | 解决方案 |
|-------|----------------|-----|
| **图像为空白** | `Graphics` 对象未清除或位图尺寸过小。 | 在绘制前调用 `graphics.Clear(Color.White);`，或增大位图尺寸。 |
| **拐角出现锯齿** | 使用低分辨率位图且笔粗细过大。 | 增加位图 DPI (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) 或减小笔宽。 |
| **文件未找到错误** | 保存路径无效。 | 使用 `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`。 |

## 常见问答

**Q: 我可以免费使用 Aspose.Drawing 吗？**  
A: Aspose.Drawing 是商业产品，但您可以通过 **[免费试用](https://releases.aspose.com/)** 来探索其功能。

**Q: 在哪里可以找到 Aspose.Drawing 文档？**  
A: 请参考 **[文档](https://reference.aspose.com/drawing/net/)** 获取全面指导。

**Q: 如何获取 Aspose.Drawing 的支持？**  
A: 访问 **[Aspose.Drawing 论坛](https://forum.aspose.com/c/drawing/44)** 获取社区帮助和官方支持。

**Q: Aspose.Drawing 是否提供临时许可证？**  
A: 是的，您可以获取 **[临时许可证](https://purchase.aspose.com/temporary-license/)** 用于短期使用。

**Q: 在哪里可以购买 Aspose.Drawing？**  
A: 请前往 **[Aspose.Drawing 购买页面](https://purchase.aspose.com/buy)** 进行购买。

## 结论

在本指南中，我们介绍了如何使用 Aspose.Drawing for .NET **draw path** 对象，应用不同的 `LineJoin` 样式，并 **save image as PNG**。掌握这些步骤后，您可以直接从服务器端代码生成复杂的矢量图形、定制图标或动态图表，提供可靠的 **export graphics to PNG** 解决方案，适用于任何平台。

---

**最后更新：** 2026-09-18  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相关教程

- [如何使用 Aspose.Drawing 绘制弧线并保存为 PNG 图像](/drawing/net/lines-curves-and-shapes/draw-arc/)
- [如何在使用 Aspose.Drawing 绘制多条线时将位图保存为 PNG](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [如何使用 Aspose.Drawing API for .NET 将位图保存为 PNG](/drawing/net/image-editing/display/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}