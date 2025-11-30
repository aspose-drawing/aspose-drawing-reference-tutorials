---
date: 2025-11-30
description: 学习如何使用 Aspose.Drawing for .NET 应用坐标系变换、绘制矩形位图以及转换页面。
language: zh
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET 中的坐标系转换（页面转换）
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET 中的坐标系转换（页面转换）

## 介绍

欢迎！在本教程中，您将学习 **如何在 Aspose.Drawing for .NET 中对页面执行坐标系转换**。无论您是需要 **绘制矩形位图** 对象、缩放绘图，还是仅仅将页面单位映射到设备单位，下面的步骤都将为您提供清晰、简洁且可直接复制粘贴到项目中的完整指南。

## 快速回答
- **绘图的主要类是什么？** Aspose.Drawing 中的 `Graphics`。
- **如何设置页面单位？** 使用 `graphics.PageUnit = GraphicsUnit.Inch;`。
- **可以在转换后的页面上绘制矩形吗？** 可以——创建 `Pen` 并调用 `DrawRectangle`。
- **输出保存在哪里？** 保存到您在 `bitmap.Save` 中指定的文件夹。
- **生产环境需要许可证吗？** 商业使用必须拥有有效的 Aspose.Drawing 许可证。

## 什么是坐标系转换？

**坐标系转换** 改变逻辑页面坐标（如英寸或毫米）映射到物理设备坐标（像素）的方式。通过调整转换，您可以控制所有绘图操作的缩放、旋转和平移，从而更容易设计分辨率无关的图形。

## 为什么使用 Aspose.Drawing 进行页面转换？

- **完整的 .NET 兼容性** – 支持 .NET Framework、.NET Core 以及 .NET 5/6。
- **丰富的图形 API** – 提供与 System.Drawing.Common 相同的功能且无平台限制。
- **简易的单位处理** – 只需一个属性即可在英寸、毫米、点等单位之间切换。
- **高质量输出** – 生成 PNG、JPEG、BMP 等格式，并可精确控制。

## 前置条件

在开始之前，请确保您已经具备：

- **Aspose.Drawing 库** – 从官方站点[此处](https://releases.aspose.com/drawing/net/)下载最新版本。
- **开发环境** – Visual Studio（任意版本）或其他 .NET IDE。
- **写入权限** – 您机器上的一个文件夹，用于保存转换后的图像（请在代码中将 `"Your Document Directory"` 替换为实际路径）。

准备就绪后，让我们逐步操作。

## 导入命名空间

首先，将所需的命名空间引入作用域：

```csharp
using System.Drawing;
```

> *为什么重要*：`System.Drawing` 包含我们在整个教程中使用的 `Bitmap`、`Graphics`、`Pen` 和颜色结构。

## 步骤 1：创建位图

创建一个空白画布，用于承载转换后的绘图。我们指定 **1000 × 800 像素** 的尺寸以及支持 alpha 透明度的像素格式。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> 该位图充当绘图表面。所选像素格式 (`Format32bppPArgb`) 可确保使用预乘 alpha 的高质量渲染。

## 步骤 2：创建 Graphics 对象

`Graphics` 对象提供绘图方法（线条、形状、文本）。我们从刚创建的位图中获取它。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> `Graphics` 对象是所有渲染操作的核心；它会遵循我们随后设置的转换设置。

## 步骤 3：清除画布

在绘制任何内容之前，将画布清除为中性背景色（本例中为灰色）。此步骤还演示了如何用纯色填充整个位图。

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## 步骤 4：设置转换（应用页面转换）

在这里我们 **通过将 `PageUnit` 设置为英寸** 来 **应用页面转换**。这告诉图形引擎将所有后续坐标解释为英寸而不是像素。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *提示*：更改 `PageUnit` 是一种简便的 **如何转换页面** 坐标的方法，无需手动计算像素值。

## 步骤 5：绘制矩形（Draw rectangle bitmap）

现在绘制一个 **1 英寸 × 1 英寸** 的矩形，位置为 (1, 1) 英寸。`Pen` 宽度设为 `0.1f` 英寸，线条细但可见。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> 这演示了在应用转换后 **draw rectangle bitmap** 的效果——请注意矩形尺寸是以英寸而非像素定义的。

## 步骤 6：保存图像

最后，将转换后的位图持久化到磁盘。将 `"Your Document Directory"` 替换为您机器上的实际文件夹路径。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> 输出文件 (`PageTransformation_out.png`) 将包含使用我们之前设置的坐标系转换绘制的矩形。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| **图像为空白** | 画布未清除或绘制超出可见区域。 | 检查 `graphics.PageUnit` 与坐标值；确保矩形位于位图范围内。 |
| **缩放不正确** | 使用了错误的 `GraphicsUnit`。 | 再次确认 `graphics.PageUnit` 与您期望的单位（如 `GraphicsUnit.Inch`）一致。 |
| **文件路径错误** | 目标目录不存在或包含非法字符。 | 预先创建目标文件夹，或使用 `Path.Combine` 安全构建路径。 |

## 常见问答

**问：Aspose.Drawing 可以免费使用吗？**  
答：Aspose.Drawing 提供可在[此处](https://releases.aspose.com/)获取的免费试用版。

**问：在哪里可以找到 Aspose.Drawing 的详细文档？**  
答：文档可在[此处](https://reference.aspose.com/drawing/net/)查看。

**问：如何获取 Aspose.Drawing 的技术支持？**  
答：请访问 [Aspose.Drawing 论坛](https://forum.aspose.com/c/diagram/17)。

**问：是否有临时许可证可供使用？**  
答：可以，在[此处](https://purchase.aspose.com/temporary-license/)获取临时许可证。

**问：在哪里可以购买 Aspose.Drawing？**  
答：请前往[此处](https://purchase.aspose.com/buy)购买。

## 结论

您已经学习了如何 **应用坐标系转换**、**绘制矩形位图** 对象，并使用 Aspose.Drawing for .NET **保存结果**。这些基础块让您能够创建分辨率无关的图形，适用于报告、UI 元素或任何需要精确尺寸的场景。尝试使用其他 `GraphicsUnit` 值（如 `Millimeter` 或 `Point`），观察它们对绘图的影响。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2025-11-30  
**测试版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose