---
date: 2026-02-19
description: 学习如何在 Aspose.Drawing 中使用画笔绘制路径并连接路径，然后使用简洁的 C# 代码将图像保存为 PNG。
linktitle: Joining Paths with Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用笔在 Aspose.Drawing 中绘制路径并连接路径
url: /zh/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing 中使用画笔绘制路径并连接路径

## Introduction

欢迎来到 **Aspose.Drawing for .NET** 的世界！在本教程中，您将学习 **如何绘制路径** 对象，使用不同的线段连接样式将它们连接起来，最后 **将图像保存为 PNG**。无论您是在构建报告工具、设计编辑器，还是仅需要清晰的矢量图形，掌握使用画笔绘制路径都能让您对视觉输出进行细粒度控制。

## Quick Answers
- **“draw path” 是什么意思？** 它创建基于矢量的线条或形状定义，`Graphics` 对象可以对其进行渲染。  
- **有哪些线段连接方式可用？** `Bevel`、`Miter`、`Round` 和 `BevelClipped`。  
- **我可以将结果导出为 PNG 吗？** 可以——使用带有 `.png` 扩展名的 `Bitmap.Save`。  
- **我需要许可证吗？** 试用版可用于评估；生产环境需要商业许可证。  
- **支持哪些 .NET 版本？** .NET Framework 4.6+、.NET Core 3.1+ 和 .NET 6+。

## What is “how to draw path” in Aspose.Drawing?

在 Aspose.Drawing 中，绘制路径是指构建一个包含一系列线条、曲线或形状的 `GraphicsPath`。路径构建完成后，使用 `Pen` 在 `Graphics` 表面上绘制它。这种方式比逐个绘制线条更灵活，因为可以对整个形状应用变换、裁剪和不同的连接样式。

## Why use Aspose.Drawing for joining paths?

- **完整的 .NET 兼容性** – 在 Windows、Linux 和 macOS 上均可运行。  
- **丰富的线段连接选项** – 通过单一属性即可创建斜角、圆角或斜接角。  
- **高质量光栅输出** – 直接保存为 PNG、JPEG、BMP 等，无需额外转换步骤。  
- **无 GDI+ 限制** – 适用于 `System.Drawing.Common` 可能受限的服务器端渲染场景。

## Prerequisites

在深入代码之前，请确保您已具备以下条件：

1. **Aspose.Drawing Library** – 下载地址 **[here](https://releases.aspose.com/drawing/net/)**。  
2. **.NET Development Environment** – Visual Studio、VS Code 或任何支持 C# 的 IDE。

现在一切就绪，让我们逐步演示。

## Import Namespaces

在文件顶部添加所需的命名空间，以便编译器能够找到图形类：

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Step 1: Create a Bitmap and Graphics Object

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

我们从一个空白画布（`Bitmap`）开始，尺寸为 1000 × 800 像素，并获取一个用于渲染绘图指令的 `Graphics` 对象。

## Step 2: Define the DrawPath Method

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

- **Pen** – 设置颜色和粗细（30 像素）。  
- **GraphicsPath** – 定义两条相连的线，形成一个 “L” 形。  
- **LineJoin** – 控制两条线之间拐角的渲染方式（`Bevel`、`Round` 等）。

您可以使用任意 `LineJoin` 值调用此方法，以观察视觉差异。

## Step 3: Join Paths with Bevel LineJoin

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

使用 `LineJoin.Bevel` 会在两条线相交处创建一个平坦的拐角。

## Step 4: Join Paths with Round LineJoin

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

`LineJoin.Round` 产生平滑的圆形拐角——适合更精致的外观。

## Step 5: Save the Result as PNG

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

`Save` 调用会将位图以 PNG 格式写入文件。根据您的环境调整路径。

## Common Issues and Solutions

| 问题 | 原因 | 解决方案 |
|-------|----------------|-----|
| **图像为空白** | 未清除 `Graphics` 对象或位图尺寸过小。 | 在绘制前调用 `graphics.Clear(Color.White);`，或增大位图尺寸。 |
| **拐角出现锯齿** | 使用低分辨率位图且笔刷太粗。 | 增加位图 DPI（`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`）或减小笔刷宽度。 |
| **文件未找到错误** | 保存路径无效。 | 使用 `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`。 |

## Frequently Asked Questions

### Q1: 我可以免费使用 Aspose.Drawing 吗？

A1: Aspose.Drawing 是商业产品，但您可以通过 **[free trial](https://releases.aspose.com/)** 体验其功能。

### Q2: 在哪里可以找到 Aspose.Drawing 文档？

A2: 请参阅 **[documentation](https://reference.aspose.com/drawing/net/)** 获取全面指南。

### Q3: 如何获取 Aspose.Drawing 的支持？

A3: 访问 **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)** 获取社区帮助和官方支持。

### Q4: Aspose.Drawing 是否提供临时许可证？

A4: 是的，您可以获取 **[temporary license](https://purchase.aspose.com/temporary-license/)** 用于短期使用。

### Q5: 在哪里购买 Aspose.Drawing？

A5: 在 **[here](https://purchase.aspose.com/buy)** 购买 Aspose.Drawing。

## Conclusion

本指南介绍了 **如何绘制路径** 对象，应用不同的 `LineJoin` 样式，并使用 Aspose.Drawing for .NET 将最终图形保存为 PNG 文件。掌握这些步骤后，您可以直接在服务器端代码中创建复杂的矢量图形、自定义图标或动态图表。

**最后更新：** 2026-02-19  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}