---
title: 在 Aspose.Drawing 中进行标注
linktitle: 在 Aspose.Drawing 中进行标注
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 使用 Aspose.Drawing for .NET 增强您的文档插图！逐步了解如何添加标注以获得更清晰、信息丰富的视觉效果。
weight: 10
url: /zh/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Drawing 中进行标注

## 介绍
欢迎来到我们关于在 Aspose.Drawing for .NET 中进行标注的分步指南！如果您希望通过标注来增强文档插图，那么您来对地方了。在本教程中，我们将使用 Aspose.Drawing 库将该过程分解为可管理的步骤。
## 先决条件
在深入学习本教程之前，请确保您满足以下先决条件：
- C# 编程语言的基础知识。
-  Aspose.Drawing 库已安装。你可以下载它[这里](https://releases.aspose.com/drawing/net/).
- 要添加标注的文档或图像。
## 导入命名空间
确保您的项目中包含必要的命名空间：
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## 第 1 步：加载图像
首先加载要添加标注的图像。代替`"Your Document Directory"`和`"gears.png"`与您的实际目录和图像文件名。
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    //你的代码在这里
}
```
## 第2步：创建图形对象
创建一个`Graphics`从图像中提取对象来执行绘图操作。
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## 第 3 步：定义标注位置
定义每个标注的起点和终点以及标注值和单位。
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
## 第四步：绘制标注
实施`DrawCallOut`方法在图像上绘制标注。
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## 第 5 步：保存图像
将带有标注的图像保存到所需的目录。
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## 绘制标注源代码
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
## 结论

恭喜！您已使用 Aspose.Drawing for .NET 成功向图像添加标注。请随意尝试不同的位置和值，以进一步自定义您的标注。

## 常见问题解答

### 我可以将 Aspose.Drawing 用于其他类型的插图吗？

是的，Aspose.Drawing 支持各种类型插图的广泛绘图操作。

### Aspose.Drawing 是否兼容不同的图像格式？

绝对地！ Aspose.Drawing 支持流行的图像格式，如 PNG、JPEG、GIF 等。

### 在哪里可以找到更多示例和文档？

探索全面的文档[这里](https://reference.aspose.com/drawing/net/).

### 如果遇到问题，我如何获得支持？

参观[Aspose.Drawing 论坛](https://forum.aspose.com/c/drawing/44)以获得社区支持。

### 我可以在购买前试用 Aspose.Drawing 吗？

当然！开始免费试用[这里](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
