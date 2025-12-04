---
title: Aspose.Drawing for .NET 中的测量单位
linktitle: Aspose.Drawing 中的测量单位
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 在这个深入的教程中探索 Aspose.Drawing for .NET 的多功能性，掌握精确图形的测量单位。
weight: 14
url: /zh/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET 中的测量单位

## 介绍

欢迎来到 Aspose.Drawing for .NET 的世界，在这里，图形操作的精确性和灵活性得到了满足。在本教程中，我们将深入研究 Aspose.Drawing 中测量单位的复杂性，为您提供逐步指南，以利用这个非凡库的强大功能。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.Drawing for .NET：确保您已安装该库。你可以下载它[这里](https://releases.aspose.com/drawing/net/).

- 文档目录：有一个指定的目录来保存您创建的文档。

- 基本 C# 知识：建议对 C# 有基本了解，以便充分利用本指南。

## 导入命名空间

在开始之前，让我们导入必要的命名空间以有效地使用 Aspose.Drawing：

```csharp
using System.Drawing;
```

现在，让我们将每个示例分解为多个步骤：

## 点作为测量单位

1. 创建位图：初始化具有指定宽度和高度的位图。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. 创建图形：从位图生成一个 Graphics 对象以在其上绘制。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. 将页面单位设置为点：将点定义为测量单位（1 点 = 1/72 英寸）。

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. 绘制矩形：以点为单位绘制矩形。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## 毫米作为测量单位

1. 将页面单位设置为毫米：将测量单位更改为毫米（1 毫米 = 1/25.4 英寸）。

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. 以毫米为单位绘制矩形：以毫米为单位绘制另一个矩形。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## 英寸作为测量单位

1. 将页面单位设置为英寸：将测量单位切换为英寸。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. 以英寸为单位绘制矩形：以英寸为单位绘制矩形。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 保存结果

完成示例后，将生成的图像保存到文档目录中：

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

现在，您已经成功地在 Aspose.Drawing for .NET 中导航了不同的测量单位，使用点、毫米和英寸创建了矩形的可视化表示。

## 结论

在本教程中，我们探讨了 Aspose.Drawing for .NET 如何处理不同的测量单位。通过操纵点、毫米和英寸，您可以在图形创作中实现精度和适应性。尝试这些概念来释放 Aspose.Drawing 的全部潜力。

## 常见问题解答

### Q1：我可以将 Aspose.Drawing for .NET 与其他 .NET 框架一起使用吗？

A1：是的，Aspose.Drawing 与各种 .NET 框架兼容，为您的开发环境提供灵活性。

### Q2: 有免费试用吗？

 A2：是的，您可以通过免费试用来探索 Aspose.Drawing[这里](https://releases.aspose.com/).

### 问题 3：如何获得 Aspose.Drawing for .NET 支持？

 A3：访问[Aspose.绘图论坛](https://forum.aspose.com/c/drawing/44)以获得社区支持和讨论。

### Q4：我可以为短期项目购买临时许可证吗？

 A4：是的，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5：哪里可以找到Aspose.Drawing的详细文档？

 A5：提供全面的文档[这里](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
