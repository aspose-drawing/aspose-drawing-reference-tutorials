---
date: 2025-12-04
description: 掌握使用 Aspose.Drawing 在 .NET 中的图像加载、批量图像转换和格式更改。学习将 BMP 转换为 PNG 等操作。
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 使用 Aspose.Drawing 将 BMP 转换为 PNG 及其他格式
url: /zh/net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Drawing 将 BMP 转换为 PNG 及其他格式

## 介绍

欢迎阅读我们的分步指南，了解如何使用 Aspose.Drawing for .NET **将 BMP 转换为 PNG**（以及许多其他图像格式）。无论您是需要为单个文件 **更改图像格式**，还是在数十张图片上执行 **批量图像转换**，本教程都将向您展示如何以简洁、易维护的代码加载、转换并保存图像。

## 快速答案
- **Aspose.Drawing 能将 BMP 转换为 PNG 吗？** 是的 – 只需加载 BMP 并使用 `.png` 扩展名调用 `Save`。  
- **是否支持批量转换？** 当然可以；遍历文件并复用同一个 `LoadAndSave` 方法即可。  
- **生产环境是否需要许可证？** 生产使用需要许可证；评估期间可使用临时许可证。  
- **.NET 哪些版本兼容？** 支持 .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。  
- **在哪里可以下载该库？** 请从官方下载页面获取最新的 Aspose.Drawing 包。

## 什么是使用 Aspose.Drawing 的 C# 图像格式转换？

Aspose.Drawing 是一个高性能、完全托管的 .NET 库，取代了旧的 `System.Drawing.Common`。它为 **load image ASP.NET** 场景提供完整控制，支持超过 100 种图像格式，并消除了平台特定的限制。

## 为什么在批量图像转换中使用 Aspose.Drawing？

- **跨平台可靠性** – 无需 GDI+ 依赖。  
- **丰富的格式支持** – BMP、GIF、JPG、PNG、TIFF 等众多格式。  
- **一致的 API** – 相同代码在 Windows、Linux、macOS 上均可运行。  
- **性能** – 为大规模图像处理流水线进行优化。

## 前置条件

在开始之前，请确保您拥有：

- **Aspose.Drawing for .NET** – 在此处下载 [here](https://releases.aspose.com/drawing/net/)。  
- 一个可用的 **.NET 开发环境**（Visual Studio、VS Code 或 Rider）。  

现在准备就绪，让我们导入所需的命名空间并开始编写代码。

## 导入命名空间

在您的 .NET 项目中，首先导入必要的命名空间：

```csharp
using System.Drawing;
```

这些类提供了加载和保存图像的核心功能。

## 步骤 1：加载图像

第一步是加载图像文件。下面的示例演示了加载包括 BMP 在内的多种格式的图像，随后我们将把它们转换为 PNG。

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## 如何使用 Aspose.Drawing 将 BMP 转换为 PNG

`LoadAndSave` 方法同时负责加载源文件并以所需的输出格式保存。通过传入 `"bmp"` 作为参数，方法将在您更改 `outputPath` 的扩展名时自动生成 PNG 文件。

### 步骤 2.1：加载图像

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### 步骤 2.2：保存图像（更改图像格式）

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

对每种需要处理的图像格式重复调用 `LoadAndSave`。只需调整 `outputPath` 的扩展名，即可 **将 BMP 转换为 PNG**、**更改图像格式** 为 GIF、JPG 等，全部使用同一方法。

## 常见陷阱与技巧

- **文件路径分隔符** – 使用 `Path.Combine` 以确保跨平台安全，而不是手动拼接字符串。  
- **释放 Bitmap** – 将 `Bitmap` 包裹在 `using` 块中，以及时释放本机资源。  
- **质量设置** – 保存 JPEG 时，可指定 `EncoderParameters` 对象来控制压缩质量。  
- **批量处理** – 将图像文件放入文件夹，使用 `Directory.GetFiles` 进行遍历，实现大规模自动转换。

## 常见问题

### 问题 1：Aspose.Drawing 是否兼容所有图像格式？

A1: Aspose.Drawing 支持广泛的格式，包括 BMP、GIF、JPG、PNG 和 TIFF 等。

### 问题 2：在哪里可以找到 Aspose.Drawing 的详细文档？

A2: 请查看官方文档 [here](https://reference.aspose.com/drawing/net/)。

### 问题 3：如何获取 Aspose.Drawing 的临时许可证？

A3: 前往 [here](https://purchase.aspose.com/temporary-license/) 获取临时许可证详情。

### 问题 4：如果在实现过程中遇到问题或有疑问怎么办？

A4: 可在 Aspose.Drawing 社区的 [Aspose Forum](https://forum.aspose.com/c/drawing/44) 寻求帮助。

### 问题 5：在哪里可以购买 Aspose.Drawing 库？

A5: 您可以在此处购买 [here](https://purchase.aspose.com/buy)。

**Additional Q&A**

**Q: 我可以在 ASP.NET Web 应用程序中使用这段代码吗？**  
A: 可以 – 相同的 `LoadAndSave` 逻辑在 ASP.NET、MVC 或 Razor Pages 中均可使用，只需确保文件路径对 Web 进程可访问。

**Q: 是否可以并行处理图像以加快批量转换速度？**  
A: 完全可以。将 `LoadAndSave` 调用包装在 `Parallel.ForEach` 循环中，但需注意线程安全地释放 `Bitmap` 对象。

## 结论

您已经学习了如何使用 Aspose.Drawing for .NET **将 BMP 转换为 PNG**、执行 **批量图像转换**，以及 **更改图像格式**。将这些模式应用于自动化图像流水线、生成缩略图或为 Web 交付准备资源。尝试不同的格式，将代码集成到您的服务中，享受全托管绘图库带来的可靠性。

---

**最后更新：** 2025-12-04  
**测试环境：** Aspose.Drawing 24.12 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}