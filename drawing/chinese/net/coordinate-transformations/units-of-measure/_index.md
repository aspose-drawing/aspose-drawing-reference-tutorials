---
date: 2026-05-24
description: 了解如何在 Aspose.Drawing for .NET 中设置单位，轻松转换图形单位，并掌握图形渲染的精确测量。
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Aspose.Drawing 中的计量单位
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何在 Aspose.Drawing for .NET 中设置单位 – 计量单位
url: /zh/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing for .NET 中设置单位 – 度量单位

## 简介

欢迎来到 Aspose.Drawing for .NET 的世界，在这里精确性和灵活性在图形处理上相遇。在本教程中，您将了解 **如何设置单位**，学习在点、毫米和英寸之间 **转换图形单位**，并看到使图像像素完美的真实案例。无论您是构建报告、缩略图还是自定义图表，掌握度量单位对于在各种设备上实现一致渲染都是必不可少的。

## 快速答案
- **更改单位的主要方法是什么？** 调用 `graphics.PageUnit = PageUnit.Point`（或 `.Millimeter`、`.Inch`）在 `Graphics` 对象上。  
- **哪个单位等于 1/72 英寸？** Points.  
- **一英寸等于多少毫米？** 25.4 mm = 1 inch.  
- **使用单位是否需要额外的库？** 否，Aspose.Drawing 核心库提供所有单位常量。  
- **我可以在同一图像中混合使用单位吗？** 对每个 `Graphics` 实例设置一次单位；使用该单位绘制所有内容以保持一致性。

## 先决条件

在我们深入教程之前，请确保您已具备以下先决条件：

- Aspose.Drawing for .NET：确保已安装该库。您可以在 [here](https://releases.aspose.com/drawing/net/) 下载。  
- 文档目录：准备一个用于保存创建的文档的指定目录。  
- 基础 C# 知识：建议具备对 C# 的基本了解，以便充分利用本指南。

## 导入命名空间

在开始之前，让我们导入使用 Aspose.Drawing 所需的命名空间：

```csharp
using System.Drawing;
```

现在，让我们将每个示例拆分为多个步骤：

## 如何将单位设置为点？

`Bitmap` 类表示一个内存中的图像，充当绘图画布。加载您的位图，创建一个 `Graphics` 对象，并将页面单位设置为点——这告诉 Aspose.Drawing 将所有坐标解释为 1/72 英寸的值。使用点可以为打印就绪的图形提供细粒度控制，并让您以高精度指定线宽。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步骤 1：创建 Bitmap  
`Bitmap` 类表示一个内存中的图像，充当绘图画布。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 步骤 2：创建 Graphics 对象  
`Graphics` 提供在 `Bitmap` 上渲染形状和文本的绘图方法。

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### 步骤 3：将页面单位设置为点  
`PageUnit` 是一个枚举，指定页面坐标的度量单位。`PageUnit.Point` 将点定义为度量单位（1 point = 1/72 inch）。此设置适用于所有后续的绘图调用。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### 步骤 4：使用点绘制矩形  
在设置单位后绘制矩形时，您指定的尺寸将被解释为点，从而确保精确的大小。

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## 如何将单位设置为毫米？

`PageUnit` 是一个枚举，指定页面坐标的度量单位。切换到毫米在需要公制尺寸时非常有用，例如生成工程图时。Aspose.Drawing 将 1 mm 视为 1/25.4 inch，允许您将图形与制造和技术文档中使用的物理测量对齐。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### 步骤 1：将页面单位设置为毫米  
将 `PageUnit.Millimeter` 分配给 `Graphics` 对象；所有坐标现在映射到公制系统。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 步骤 2：使用毫米绘制矩形  
矩形的宽度和高度现在以毫米表示，便于与物理测量对齐，并确保打印输出符合实际尺寸。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 如何将单位设置为英寸？

`Graphics` 提供在 `Bitmap` 上渲染形状和文本的绘图方法。英寸是许多美国设计工具的默认单位。将单位设置为英寸可让您在布局 UI 元素时使用熟悉的度量，并简化从屏幕设计到常用英寸的打印的转换。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### 步骤 1：将页面单位设置为英寸  
`PageUnit.Inch` 更改坐标系统，使 1 单位等于 1 inch，提供了一种直接的方式来为面向打印的布局设置元素大小。

CODE_BLOCK_PLACEHOLDER_10_END

### 步骤 2：使用英寸绘制矩形  
现在您绘制的任何形状都使用英寸作为度量基准，这对于打印布局以及向习惯使用英制单位的利益相关者传达尺寸非常理想。

CODE_BLOCK_PLACEHOLDER_11_END

## 保存结果

完成示例后，将生成的图像保存到您的文档目录。`Bitmap.Save` 方法以您指定的格式（PNG、JPEG 等）写入文件。

CODE_BLOCK_PLACEHOLDER_12_END

现在，您已成功掌握 Aspose.Drawing for .NET 中多种度量单位，使用点、毫米和英寸创建矩形的可视化表示。

## 为什么使用 Aspose.Drawing 的单位系统？

Aspose.Drawing 支持 **30+ 图像格式**，并且能够在不将整个文件加载到内存中的情况下处理高达 **5000 × 5000 像素** 的图像，为大规模图形生成提供高性能。通过显式设置单位，您可以消除猜测，减少转换错误，并确保输出在所有平台上匹配精确的物理尺寸。

## 常见问题及解决方案

- **保存后尺寸意外** – 验证您已在任何绘图调用**之前**设置 `graphics.PageUnit`；稍后更改单位不会回溯性地调整已有形状的大小。  
- **高 DPI 屏幕上输出模糊** – 提高位图的分辨率（例如，`new Bitmap(width, height, 300)`）以匹配目标 DPI。  
- **在同一图像中混合使用单位** – 为每种单位创建单独的 `Graphics` 实例，或在绘制前进行手动转换。

## 常见问答

### Q1：我可以在其他 .NET 框架中使用 Aspose.Drawing for .NET 吗？
A1：是的，Aspose.Drawing 与各种 .NET 框架兼容，为您的开发环境提供灵活性。

### Q2：是否提供免费试用？
A2：是的，您可以通过免费试用在 [here](https://releases.aspose.com/) 探索 Aspose.Drawing。

### Q3：如何获取 Aspose.Drawing for .NET 的支持？
A3：访问 [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) 获取社区支持和讨论。

### Q4：我可以为短期项目购买临时许可证吗？
A4：是的，您可以在 [here](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

### Q5：在哪里可以找到 Aspose.Drawing 的详细文档？
A5：完整的文档可在 [here](https://reference.aspose.com/drawing/net/) 获取。

---

**最后更新：** 2026-05-24  
**测试版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
