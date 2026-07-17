---
date: 2026-03-02
description: 使用 Aspose.Drawing for .NET 增强文档插图！一步一步学习如何添加标注，以获得更清晰、更具信息性的视觉效果。
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing for .NET 添加标注
url: /zh/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Drawing 中制作标注

## 介绍
如果你想了解 **如何在 Aspose.Drawing for .NET 中为图像或图表添加标注**，你来对地方了。在本教程中，我们将完整演示从加载图像到绘制精美标注的整个过程，让你的插图更加清晰、信息更丰富。

## 快速答疑
- **需要哪个库？** Aspose.Drawing for .NET（可从官方网站下载）。  
- **支持哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **是否需要许可证？** 开发阶段可使用免费试用版；生产环境需购买商业许可证。  
- **实现需要多长时间？** 基本标注通常在 10 分钟以内完成。  
- **可以自定义颜色和字体吗？** 可以——所有样式均由标准 GDI+ 对象（Pen、Font、Brush）驱动。

## 在 Aspose.Drawing 中添加标注的步骤
下面是一份简明的 **逐步指南**，展示 **如何在图像中添加标注**。复制代码、尝试不同位置、根据品牌需求调整样式即可。

## 前置条件
在开始之前，请确保你已经具备：

- 基本的 C# 编程知识。  
- 已安装 Aspose.Drawing 库。可在此处下载 [here](https://releases.aspose.com/drawing/net/)。  
- 一份需要添加标注的文档或图像。

## 引入命名空间
确保在项目中引用了必要的命名空间：

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## 步骤 1：加载图像
首先加载需要添加标注的图像。将 `"Your Document Directory"` 和 `"gears.png"` 替换为实际的目录和文件名。

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## 步骤 2：创建 Graphics 对象
从图像创建一个 `Graphics` 对象，以便执行绘图操作。

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## 步骤 3：定义标注位置
为每个标注定义起点、终点以及标注的数值和单位。

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
实现 `DrawCallOut` 方法，在图像上绘制标注。

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## 步骤 5：保存图像
将带有标注的图像保存到指定目录。

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## 标注绘制源码
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
- **锚点坐标不正确** – 确保起点和终点位于图像范围内，否则标注可能被裁剪。  
- **文字重叠** – 如标签与其他图形冲突，可调整 `spaceSize` 或字体大小。  
- **性能** – 对于超大图像，使用完 `Pen`、`Font`、`Brush` 后请及时 `Dispose`，以释放资源。

## 结论
恭喜！你已经掌握 **如何在 Aspose.Drawing for .NET 中为图像添加标注**。可以尝试不同的位置、颜色和字体，以匹配你的视觉风格。

## 常见问答

### 我可以在其他类型的插图中使用 Aspose.Drawing 吗？
可以，Aspose.Drawing 支持多种绘图操作，适用于各种插图类型。

### Aspose.Drawing 是否兼容不同的图像格式？
完全兼容！Aspose.Drawing 支持 PNG、JPEG、GIF 等常见图像格式。

### 在哪里可以找到更多示例和文档？
请在此处查看完整文档 [here](https://reference.aspose.com/drawing/net/)。

### 如果遇到问题，如何获取支持？
访问 [Aspose.Drawing 论坛](https://forum.aspose.com/c/drawing/44) 获取社区帮助。

### 我可以在购买前试用 Aspose.Drawing 吗？
当然！点击此处获取免费试用版 [here](https://releases.aspose.com/)。

**附加问答**

**问：我可以更改标注线的样式（虚线、点线）吗？**  
答：可以——在绘制线条前设置 `Pen.DashStyle` 属性即可。

**问：是否可以为标注标签添加背景颜色？**  
答：可以。创建带有所需颜色的 `SolidBrush`，在调用 `DrawString` 前先绘制一个矩形作为背景。

**问：如何确保标注在高 DPI 显示器上保持一致？**  
答：如示例所示，将 `graphics.PageUnit = GraphicsUnit.Pixel`，并使用基于矢量的度量保持缩放一致。

---

**最后更新：** 2026-03-02  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}