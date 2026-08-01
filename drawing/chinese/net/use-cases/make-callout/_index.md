---
date: 2026-08-01
description: 了解如何使用 Aspose.Drawing for .NET 为图像添加标注——一步一步的指南，包含代码占位符、技巧和常见问题解答。
keywords:
- how to add callouts
- Aspose.Drawing callout tutorial
- .NET image annotation
lastmod: 2026-08-01
linktitle: 在 Aspose.Drawing 中创建标注
og_description: 了解如何在 Aspose.Drawing for .NET 中添加标注。本教程涵盖前置条件、一步一步的实现、技巧以及面向开发者的常见问题解答。
og_image_alt: Screenshot showing callout annotation on an image using Aspose.Drawing
og_title: 如何使用 Aspose.Drawing for .NET 添加标注 – 快速指南
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to add callouts to images using Aspose.Drawing for .NET –
    step‑by‑step guide with code placeholders, tips, and FAQs.
  headline: How to Add Callouts with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of drawing operations for diagrams,
      charts, and custom graphics beyond simple callouts.
    question: Can I use Aspose.Drawing for other types of illustrations?
  - answer: Absolutely! Aspose.Drawing handles PNG, JPEG, GIF, BMP, TIFF, and many
      more formats.
    question: Is Aspose.Drawing compatible with different image formats?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find more examples and documentation?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      for community assistance and official support.
    question: How do I get support if I encounter issues?
  - answer: Certainly! Get started with a free trial [here](https://releases.aspose.com/).
    question: Can I try Aspose.Drawing before purchasing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- callout
- Aspose.Drawing
- .NET graphics
- image annotation
title: 如何使用 Aspose.Drawing for .NET 添加标注
url: /zh/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing for .NET 添加标注

## 介绍
如果您正在寻找使用 Aspose.Drawing for .NET 在图像或图表中 **添加标注** 的方法，您来对地方了。在本教程中，我们将逐步演示——从加载位图、创建 `Graphics` 画布、定义标注几何形状，到渲染样式化的标注——让您的视觉内容更加清晰和富有信息。

## 快速答案
- **我需要哪个库？** Aspose.Drawing for .NET（可从官方网站下载）。  
- **支持哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **我需要许可证吗？** 免费试用可用于开发；生产环境需要商业许可证。  
- **实现需要多长时间？** 对于基本标注，通常在 10 分钟以内。  
- **我可以自定义颜色和字体吗？** 可以——所有操作均由标准 GDI+ 对象（Pen、Font、Brush）驱动。

## 什么是标注？
标注是一种图形注释，将线条（或箭头）与文本标签相结合，用于突出图像的特定部分。它常用于技术图表、截图和演示文稿，以吸引对特定元素的注意、解释功能或提供测量信息，使视觉传达更清晰、更有效。

## 为什么在标注中使用 Aspose.Drawing？
Aspose.Drawing 专为高性能图像处理而构建，支持广泛的格式，使其非常适合在大型或复杂图形中添加标注。其内存高效的架构能够处理高达 **500 MB** 的文件而无需将整个位图加载到 RAM 中，并且提供对绘图基元、颜色和文本渲染的细粒度控制，确保标注清晰、专业。

## 前置条件
在开始之前，请确保您具备以下条件：

- 基本的 C# 编程语言知识。  
- 已安装 Aspose.Drawing 库。您可以在[此处](https://releases.aspose.com/drawing/net/)下载。  
- 一个您想要添加标注的文档或图像。

## 导入命名空间
以下命名空间为您提供核心绘图类的访问权限：

`System.Drawing` 提供 GDI+ 类型，如 `Bitmap`、`Graphics`、`Pen`、`Font` 和 `Brush`。在开始编码前请导入它们。

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## 如何在 Aspose.Drawing 中添加标注
加载源图像，创建 `Graphics` 画布，定义起始/结束点，并调用一个帮助方法来绘制线条、箭头和标签——全部通过几行简洁的代码实现。此方法适用于 PNG、JPEG、BMP 和 GIF 文件，并允许您完全自定义颜色、字体和线条样式。

## 步骤 1：加载图像
`Image` 表示光栅图像，并提供加载、保存和操作位图数据的方法。首先加载您想要添加标注的图像。将 `"Your Document Directory"` 和 `"gears.png"` 替换为实际的目录和图像文件名。

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## 步骤 2：创建 Graphics 对象
`Graphics` 提供在位图上渲染形状、文本和图像的绘图表面方法。使用图像创建的 `Graphics` 对象可执行绘图操作。

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## 步骤 3：定义标注位置
`PointF` 使用浮点坐标定义二维空间中的点。为每个标注指定起始（锚点）和结束（标签）点。这些坐标必须位于图像边界内，否则标注会被裁剪。

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## 步骤 4：绘制标注
实现 `DrawCallOut` 方法以渲染线条、可选的箭头以及文本标签。该方法使用 `Pen` 绘制线条，`Font` 绘制标签，`SolidBrush` 用于填充颜色。

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## 步骤 5：保存图像
将带注释的位图持久化到磁盘。您可以选择任何受支持的格式，如 PNG 或 JPEG。

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## 标注源代码
将所有步骤串联起来的完整源代码位于下面的占位符中。请在标示处插入您自己的实现细节。

```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## 常见问题与技巧
- **锚点坐标不正确** – 确保起始和结束点位于图像边界内；否则标注可能被裁剪。  
- **文本重叠** – 如果标签与其他图形冲突，请调整 `spaceSize` 或字体大小。  
- **性能** – 对于非常大的图像，使用后请考虑释放 `Pen`、`Font` 和 `Brush` 对象以释放资源。

## 结论
现在，您已经拥有使用 Aspose.Drawing for .NET 为任何图像 **添加标注** 的完整、可投入生产的模式。欢迎尝试不同的颜色、线条样式和字体系列，以匹配您的品牌。

## 常见问题

**Q: 我可以将 Aspose.Drawing 用于其他类型的插图吗？**  
A: 可以，Aspose.Drawing 支持广泛的绘图操作，可用于图表、图形以及超出简单标注的自定义图形。

**Q: Aspose.Drawing 是否兼容不同的图像格式？**  
A: 绝对兼容！Aspose.Drawing 支持 PNG、JPEG、GIF、BMP、TIFF 等多种格式。

**Q: 我在哪里可以找到更多示例和文档？**  
A: 请在[此处](https://reference.aspose.com/drawing/net/)查看完整文档。

**Q: 如果遇到问题，我该如何获取支持？**  
A: 访问 [Aspose.Drawing 论坛](https://forum.aspose.com/c/drawing/44) 获取社区帮助和官方支持。

**Q: 我可以在购买前试用 Aspose.Drawing 吗？**  
A: 当然！请在[此处](https://releases.aspose.com/)获取免费试用。

---

**最后更新：** 2026-08-01  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [如何使用 Aspose.Drawing for .NET 绘制弧线和其他形状](/drawing/net/lines-curves-and-shapes/)
- [矩阵变换教程：Aspose.Drawing for .NET 中的矩阵变换](/drawing/net/coordinate-transformations/matrix-transformations/)
- [如何在 Aspose.Drawing .NET 中使用 Pen 合并路径](/drawing/net/pens/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}