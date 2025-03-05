---
title: 在 Aspose.Drawing 中的图像上添加文本
linktitle: 在 Aspose.Drawing 中的图像上添加文本
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 探索使用 Aspose.Drawing for .NET 将文本无缝集成到图像中。按照我们的分步指南轻松进行图像处理。现在下载！
type: docs
weight: 12
url: /zh/net/use-cases/text-on-image/
---
## 介绍
在 .NET 开发的动态世界中，Aspose.Drawing 作为轻松操作图像的强大工具脱颖而出。无论是用于水印、注释还是创建个性化图形，向图像添加文本都是常见要求。在本教程中，我们将探索如何利用 C# 利用 Aspose.Drawing 将文本无缝集成到图像中。
## 先决条件
在深入学习本教程之前，请确保您已具备以下条件：
1.  Aspose.Drawing 库：从以下位置下载并安装 Aspose.Drawing 库：[Aspose.Drawing for .NET 文档](https://reference.aspose.com/drawing/net/).
2. 开发环境：拥有有效的 .NET 开发环境，包括 Visual Studio 或任何其他兼容的 IDE。
现在，让我们开始使用分步指南。
## 导入命名空间
首先将必要的命名空间导入到您的 C# 项目中：
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## 第 1 步：加载图像
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
在这里，我们从指定的文件路径加载图像并初始化图形对象以进行进一步处理。
## 第 2 步：设置文本属性
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
定义文本属性，例如颜色、字体和填充。根据您的喜好调整这些参数。
## 第 3 步：测量文字大小
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
通过单独测量每个单词来计算文本所需的大小。这可确保正确放置并避免文本重叠。
## 第四步：在图像上绘制文本
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
现在，根据计算出的尺寸将文本放置在图像上，并使用指定的字体和颜色进行绘制。
## 第 5 步：保存图像
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
将修改后的图像保存到所需的目录。
本分步指南演示了使用 Aspose.Drawing for .NET 将文本添加到图像的简单过程。尝试不同的字体、颜色和文本内容以达到所需的视觉效果。
## 结论
Aspose.Drawing 简化了 .NET 中的图像操作任务，为开发人员提供了强大的工具包。向图像添加文本只是其功能的示例之一，展示了该库在处理图形元素方面的多功能性。
## 经常问的问题
### Aspose.Drawing 与所有图像格式兼容吗？
Aspose.Drawing 支持多种图像格式，包括 JPEG、PNG 和 GIF 等流行格式。请参阅[文档](https://reference.aspose.com/drawing/net/)以获得完整列表。
### 我可以将 Aspose.Drawing 用于商业项目吗？
是的，Aspose.Drawing 适用于个人和商业项目。有关许可详细信息，请访问[购买页面](https://purchase.aspose.com/buy).
### 临时许可证是否可用于测试目的？
是的，您可以通过访问获得临时测试许可证[临时牌照](https://purchase.aspose.com/temporary-license/).
### 在哪里可以找到 Aspose.Drawing 的社区支持？
参与社区并获得支持[Aspose.Drawing 论坛](https://forum.aspose.com/c/diagram/17).
### 我如何开始使用 Aspose.Drawing？
首先从下载库[这里](https://releases.aspose.com/drawing/net/)并探索全面的[文档](https://reference.aspose.com/drawing/net/).