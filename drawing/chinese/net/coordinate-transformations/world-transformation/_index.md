---
date: 2025-11-29
description: 学习如何使用 Aspose.Drawing 创建位图、应用世界变换并将图形转换为 PNG。针对 .NET 开发者的分步指南。
language: zh
linktitle: World Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 使用 Aspose.Drawing 创建位图 – 世界变换指南
url: /net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Drawing 创建位图 – 世界变换

## 介绍

欢迎！在本教程中，您将 **使用 Aspose.Drawing 创建位图**，并探索世界变换，让您轻松平移、旋转或缩放图形。无论您需要 **graphics translate 示例**，想要 **将图形转换为 PNG**，还是计划 **多个图形变换**，本指南都会以清晰、对话式的方式一步步带您完成。

## 快速答案
- **“世界变换”是什么意思？** 它将绘图的逻辑（世界）坐标映射到页面（设备）坐标。  
- **我可以将结果导出为 PNG 吗？** 可以——绘制完成后，只需使用 `.png` 扩展名调用 `bitmap.Save(...)` 即可。  
- **使用 Aspose.Drawing 是否需要许可证？** 免费试用可用于开发；生产环境需要商业许可证。  
- **这与 .NET 6/7 兼容吗？** 完全兼容——Aspose.Drawing 支持 .NET Framework 4.5+ 以及 .NET Core/5/6/7。  
- **可以链式使用多少个变换？** 您可以按顺序应用 **多个图形变换**（平移、旋转、缩放等）。

## 什么是 Aspose.Drawing 中的世界变换？

世界变换会改变绘图命令使用的坐标系。默认情况下，(0,0) 位于位图的左上角。通过 `TranslateTransform`、`RotateTransform` 或 `ScaleTransform`，您可以重新定位原点、旋转形状或在不改变原始几何形状的情况下调整大小。

## 为什么要使用 Graphics Translate 示例？

- **简化定位** – 移动物体时无需重新计算每个点。  
- **保持代码整洁** – 一个变换调用即可替代大量手动坐标调整。  
- **提升性能** – 图形引擎在内部处理数学运算。  

## 前置条件

在开始之前，请确保您已具备：

- 已在 .NET 项目中集成 **Aspose.Drawing 库**（可从官方 [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/) 下载）。  
- 一个 **文档目录**，用于保存输出图像。  
- 对 **C#** 语法和 Visual Studio 或您偏好的 IDE 有基本了解。  

现在，让我们进入代码吧！

## 导入命名空间

首先，引入所需的命名空间：

```csharp
using System.Drawing;
using Aspose.Drawing;
```

这些命名空间为您提供 `Bitmap`、`Graphics` 以及 Aspose 绘图工具的访问权限。

## 步骤指南

### 步骤 1：创建位图

我们先创建一个空白画布，用于承载绘图。

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

- **为什么使用 32bppPArgb？** 该像素格式支持 alpha 透明度和高质量颜色渲染，非常适合 PNG 输出。  
- **小技巧：** 根据目标图像尺寸调整宽度/高度。

### 步骤 2：设置世界变换（Graphics Translate 示例）

这里我们将原点平移到位图中心，使绘图命令相对于该点进行。

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

- 这会将 (0,0) 点移动到 (500, 400) —— 即 1000 × 800 画布的中心。  
- 您可以链式添加其他变换（例如 `RotateTransform`、`ScaleTransform`），实现 **多个图形变换**。

### 步骤 3：使用变换后的坐标绘制矩形

现在绘制的任何形状都将相对于新的原点定位。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

- 矩形的左上角位于变换后的原点（图像中心）。  
- 您可以尝试绘制其他形状——椭圆、直线或自定义路径。

### 步骤 4：保存结果 – 将图形转换为 PNG

最后，将位图持久化为 PNG 文件。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

- PNG 能保留我们之前设置的精确颜色和透明度。  
- 将 `"Your Document Directory"` 替换为您机器上的实际路径。

## 常见问题及解决方案

| 问题 | 产生原因 | 解决办法 |
|------|----------|----------|
| **保存时文件未找到错误** | 目标文件夹不存在。 | 在调用 `Save` 前使用 `Directory.CreateDirectory` 程序化创建文件夹。 |
| **变换后出现空白图像** | `TranslateTransform` 在绘制之后调用。 | 确保在任何绘图命令 **之前** 设置变换。 |
| **颜色失真** | 使用了不兼容的像素格式。 | 对于 PNG 输出，请坚持使用 `Format32bppPArgb`。 |

## 常见问答

**问：可以应用多个变换吗？**  
答：可以——您可以链式使用 `TranslateTransform`、`RotateTransform` 和 `ScaleTransform` 来实现复杂效果。

**问：Aspose.Drawing 对商业项目免费吗？**  
答：提供免费试用供评估使用，但生产环境必须购买商业许可证。

**问：这在 .NET Core 和 .NET 5/6/7 上可用吗？**  
答：完全可用。Aspose.Drawing 支持所有现代 .NET 运行时。

**问：在哪里可以找到完整的 API 参考？**  
答：完整文档可在 [here](https://reference.aspose.com/drawing/net/) 查看。

**问：如何排查输出文件缺失的问题？**  
答：检查路径字符串，确保拥有写入权限，并在调用 `Save` 前确认目录已存在。

## 结论

您已经学会了使用 Aspose.Drawing 创建位图**、应用 **世界变换**，以及 **将图形转换为 PNG**。掌握这些基础后，您可以构建更丰富的图形、生成动态图像，并在任何 .NET 应用中集成高级视觉效果。

---

**最后更新：** 2025-11-29  
**测试环境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  
**相关资源：** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}