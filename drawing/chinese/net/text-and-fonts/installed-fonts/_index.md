---
date: 2025-12-06
description: 学习如何在列出已安装字体、显示字体系列、从位图创建图形以及使用 Aspose.Drawing for .NET 绘制带字体的文本时保存 PNG
  图像文件。
language: zh
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 在 Aspose.Drawing 中保存 PNG 图像并使用已安装的字体
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 保存 PNG 图像并在 Aspose.Drawing 中使用已安装的字体

## 介绍

如果您需要 **save PNG image** 文件，并且还想显示机器上已安装字体的信息，Aspose.Drawing for .NET 为您提供了一种简洁、跨平台的实现方式。在本教程中，我们将逐步演示列出已安装字体、显示字体族、从位图创建图形以及使用字体绘制文本——最终将结果保存为 PNG 图像。完成后，您将拥有一个可在任何 .NET 项目中直接使用的可复用代码片段。

## 快速答案
- **本教程创建什么？** 列出已安装字体族的 PNG 图像。  
- **需要哪个库？** Aspose.Drawing for .NET（不需要 System.Drawing.Common）。  
- **可以使用自定义字体吗？** 可以——只需将其加载到 `InstalledFontCollection` 中。  
- **输出分辨率可调吗？** 完全可以——更改位图大小或像素格式。  
- **运行代码是否需要许可证？** 临时许可证可用于评估；生产环境需要正式许可证。

## 在 Aspose.Drawing 中，“save PNG image” 是什么？

保存 PNG 图像是指将绘图表面（即 `Bitmap`）渲染为扩展名为 `.png` 的文件。Aspose.Drawing 为您处理编码，因此您只需使用目标路径调用 `bitmap.Save(...)` 即可。

## 为什么要列出已安装的字体并显示字体族？

了解可用的字体可以让您创建能够适应最终用户环境的动态图形。这在生成报告、证书或任何必须符合企业品牌而无需随应用程序一起分发字体文件的视觉内容时尤为便利。

## 先决条件

- **Aspose.Drawing Library** – 从 [Aspose Drawing download page](https://releases.aspose.com/drawing/net/) 下载最新版本。  
- **IDE** – Visual Studio、Rider 或任何 .NET 兼容的编辑器。  
- **基本的 C# 知识** – 您应熟悉类、对象以及简单的循环。

## 导入命名空间
要使用字体和图形功能，请在 C# 文件顶部导入以下命名空间：

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 分步指南

### 步骤 1：创建位图（画布）

首先，我们创建一个用于保存最终图像的位图。位图的尺寸和像素格式决定了保存的 PNG 的质量。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步骤 2：从位图创建 Graphics 对象

接下来，我们从位图获取一个 `Graphics` 对象。该对象允许我们在画布上绘制形状、文本和图像。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### 步骤 3：设置画刷和字体（使用字体绘制文本）

我们需要一个用于文本颜色的画刷，以及一个定义字体、大小和样式的 `Font` 对象。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### 步骤 4：列出已安装的字体并显示字体族

现在我们将在位图上直接显示字体族的数量以及前几个名称。这演示了 **list installed fonts** 和 **show font families** 功能。

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### 步骤 5：保存 PNG 图像

最后，我们将位图写入磁盘保存为 PNG 文件。这就是核心的 **save png image** 操作。

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **专业提示：** 使用 `Path.Combine` 构建文件路径，可避免不同操作系统目录分隔符带来的问题。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| **未显示字体** | `InstalledFontCollection` 未填充（例如在没有字体的无头服务器上运行）。 | 在服务器上安装所需字体，或在应用程序中嵌入自定义字体。 |
| **保存的文件损坏** | 像素格式不正确或缺少写入权限。 | 确保目标文件夹存在且应用具有写入权限；保持使用 `Format32bppPArgb`。 |
| **文字模糊** | DPI 设置过低。 | 增大位图尺寸或设置 `graphics.SmoothingMode = SmoothingMode.AntiAlias`。 |

## 常见问答

**问：我可以使用机器上未安装的自定义字体吗？**  
答：可以。将字体文件加载到 `PrivateFontCollection` 中，然后从该集合创建 `Font`。

**问：如何处理与字体相关的异常？**  
答：在 `try/catch` 块中包装字体创建，并检查 `ArgumentException` 以判断缺少的字体族。

**问：Aspose.Drawing 适用于 Web 应用程序吗？**  
答：完全适用。该库可在 ASP.NET Core、Azure Functions 以及其他服务器端环境中使用。

**问：我可以更改文本颜色或样式吗？**  
答：可以。使用不同的 `Brush` 类型（例如 `LinearGradientBrush`），并修改 `FontStyle` 枚举。

**问：在哪里可以获取用于测试的临时许可证？**  
答：从 [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/) 下载试用许可证。

## 结论

通过上述步骤，您已经学习了如何使用 Aspose.Drawing for .NET **save PNG image** 文件，并动态 **list installed fonts**、**show font families**、**create graphics from bitmap**、以及 **draw text with fonts**。欢迎尝试其他字体、颜色和位图尺寸，以满足项目的视觉需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2025-12-06  
**测试版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose