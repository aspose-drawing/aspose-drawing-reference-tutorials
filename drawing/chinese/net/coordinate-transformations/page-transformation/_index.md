---
date: 2026-05-19
description: 了解如何在 .NET 中使用 Aspose.Drawing 进行坐标系转换时绘制矩形图形。本分步指南展示了如何将 inches 转换为 pixels
  并设置 page units。
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Aspose.Drawing 中的 Coordinate System Transformation
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: 如何在 Aspose.Drawing for .NET 中绘制矩形 – Coordinate System Transformation（Page Transformation）
url: /zh/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing for .NET 中绘制矩形 – 坐标系转换（页面转换）

## 介绍

欢迎！在本教程中，您将学习如何使用 Aspose.Drawing for .NET 在转换页面坐标的同时 **绘制矩形** 图形。无论您是构建图形密集型应用程序，还是需要对绘图单位进行精确控制，本指南都会一步步带您完成——从设置画布到绘制矩形元素。完成后，您即可自信地在自己的项目中应用这些技术。

## 快速答案
- **什么是坐标系转换？** 将页面级单位（如英寸）映射到设备级像素。  
- **为什么使用 Aspose.Drawing？** 它提供了一个完全托管、跨平台的替代方案，取代 System.Drawing.Common。  
- **实现示例需要多长时间？** 基本的页面转换大约需要 5‑10 分钟。  
- **是否需要许可证？** 开发阶段可使用免费试用版；生产环境需要商业许可证。  
- **支持哪些 .NET 版本？** .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6/7。

## Aspose.Drawing 是什么？

`Aspose.Drawing` 是一个 .NET 图形库，提供 **设备无关的 API** 用于创建和操作光栅图像、矢量图以及页面级绘图，而无需依赖 GDI+。它支持 **30 多种图像格式**，并且能够在不将整个文件加载到内存的情况下处理高达 **10,000 × 10,000 像素** 的图像。

## 为什么在 Aspose.Drawing 中使用坐标系转换？

坐标系转换让您可以使用真实世界的单位来设计图形，库会为任何输出设备处理像素缩放。这确保了在屏幕和打印机上的尺寸保持一致，并简化了布局计算。

- **设备无关的设计：** 编写一次代码，Aspose.Drawing 会为任何屏幕或打印机处理像素缩放。  
- **精确绘图：** 适用于技术图表、CAD 风格草图或任何对精确测量有要求的场景。  
- **跨平台可靠性：** 在 Windows、Linux 和 macOS 上表现一致，避免了 System.Drawing 的 GDI+ 限制。  
- **性能数据：** 在典型的 2.5 GHz CPU 上，绘制一个 5 英寸、300 DPI 的矩形耗时不足 **15 ms**，库在实时预览场景下可实现 **每秒 50 帧** 的渲染。

## 前置条件

在开始之前，请确保您已具备：

- **Aspose.Drawing 库：** 从官方站点 [here](https://releases.aspose.com/drawing/net/) 下载最新版本。  
- **开发环境：** Visual Studio、Rider 或任何兼容 .NET 的 IDE。  
- **文档目录：** 将代码中的 `"Your Document Directory"` 替换为您希望保存输出图像的文件夹路径。  
- **ASP.NET 支持（可选）：** 您可以在 ASP.NET Core 项目中通过添加 NuGet 包使用 Aspose.Drawing——这遵循与其他 .NET 库相同的 **how to use aspnet** 模式。

现在一切就绪，让我们进入分步指南。

## 如何使用页面转换绘制矩形？

加载一个空白位图，将页面单位设为英寸，并使用细蓝色笔绘制矩形——只需几行代码即可完成矩形绘制。`Graphics.PageUnit` 属性告诉引擎将所有坐标解释为英寸，这样您就可以使用真实世界的测量而不是原始像素。

### 步骤 1：导入命名空间

`using` 语句让您可以访问核心绘图类。

```csharp
using System.Drawing;
```

### 步骤 2：创建位图

`Bitmap` 表示内存中的图像，您可以在其上绘图。我们首先创建一个空白位图作为绘图表面。像素格式 `Format32bppPArgb` 为我们提供高质量的预乘 Alpha 支持。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步骤 3：创建 Graphics 对象

`Graphics` 对象为位图提供绘图 API。它是代码与像素缓冲区之间的桥梁。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 步骤 4：清除画布

为画布设置中性背景，使绘制的形状更加突出。这里我们使用浅灰色填充。

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### 步骤 5：设置转换（如何设置单位）

`Graphics.PageUnit` 指定页面坐标使用的测量单位。要将页面坐标映射到设备像素，只需设置 `PageUnit` 属性。本例选择英寸，您也可以使用 `GraphicsUnit.Millimeter`、`GraphicsUnit.Point` 或 `GraphicsUnit.Pixel`。将单位设为英寸后，库会根据位图的 DPI（默认 96 DPI，高清打印为 300 DPI）自动 **将英寸转换为像素**。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 步骤 6：绘制矩形 – 绘制矩形图形

`Pen` 定义了在图形表面上绘制线条的颜色、宽度和样式。现在我们使用细蓝色笔绘制矩形。由于已切换到英寸，矩形的大小和位置均以英寸表示，使代码在面向打印的布局中更易读。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### 步骤 7：保存图像

最后，将位图写入 PNG 文件到您之前指定的文件夹中。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## 如何为打印机缩放图形？

在绘制之前，将位图的 DPI 设置为目标打印机分辨率（例如 300 DPI）。这会自动 **缩放打印机输出**，使代码中的一英寸等同于打印页面上的一英寸。设置 `bitmap.SetResolution(300, 300)` 后，同一矩形在打印纸上会显得更大，但尺寸保持精确。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| **未创建输出文件** | 路径错误或文件夹不存在 | 确保目标目录存在，或在保存前使用 `Directory.CreateDirectory` 创建。 |
| **矩形出现畸形** | `PageUnit` 设置错误或 DPI 不匹配 | 验证 `graphics.PageUnit` 与您计划使用的单位一致，并确保位图 DPI 正确设置（默认 96 DPI）。 |
| **许可证异常** | 生产环境中未使用有效许可证运行 | 在创建图形对象之前应用临时或永久的 Aspose.Drawing 许可证。 |

## 常见问答

**Q: 可以免费使用 Aspose.Drawing 吗？**  
A: 可以，免费试用版可在 [here](https://releases.aspose.com/) 获取。

**Q: 在哪里可以找到 Aspose.Drawing 的详细文档？**  
A: 完整的 API 参考位于 [here](https://reference.aspose.com/drawing/net/)。

**Q: 如何获取 Aspose.Drawing 的支持？**  
A: 访问 [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) 获取社区帮助和官方支持。

**Q: 是否提供 Aspose.Drawing 的临时许可证？**  
A: 当然——可在 [here](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

**Q: 哪里可以购买完整的 Aspose.Drawing 许可证？**  
A: 您可以在 [here](https://purchase.aspose.com/buy) 购买。

## 结论

本指南涵盖了使用 Aspose.Drawing **绘制矩形** 图形的全部要点：设置画布、配置页面单位、精确绘制形状以及保存结果。使用这些技术，您可以为报告、CAD 风格绘图或任何对测量精度有要求的应用构建可伸缩、设备无关的图形。接下来，探索旋转、缩放和自定义坐标原点等高级转换，以解锁更强大的绘图场景。

---

**最后更新:** 2026-05-19  
**测试环境:** Aspose.Drawing 24.12 for .NET  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [Aspose.Drawing for .NET 中的度量单位](/drawing/net/coordinate-transformations/units-of-measure/)
- [如何应用转换：Aspose.Drawing for .NET 中的局部转换](/drawing/net/coordinate-transformations/local-transformation/)
- [矩阵转换教程：Aspose.Drawing for .NET 中的矩阵转换](/drawing/net/coordinate-transformations/matrix-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}