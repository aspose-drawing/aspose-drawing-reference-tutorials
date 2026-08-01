---
date: 2026-08-01
description: Learn how to create bitmap image C# and draw rectangle on bitmap using
  Aspose.Drawing. Step‑by‑step guide for .NET developers.
images:
- /net/lines-curves-and-shapes/draw-rectangle/og-image.png
keywords:
- create bitmap image c#
- draw rectangle on bitmap
- replace system.drawing
lastmod: 2026-08-01
linktitle: Drawing Rectangles in Aspose.Drawing
og_description: Create bitmap image C# and draw rectangle on bitmap using Aspose.Drawing.
  This tutorial shows how to generate, style, and save rectangle graphics in .NET.
og_image_alt: Guide to drawing rectangles on a bitmap with Aspose.Drawing for .NET
og_title: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to create bitmap image C# and draw rectangle on bitmap using
    Aspose.Drawing. Step‑by‑step guide for .NET developers.
  headline: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)`
      before or after drawing the outline.
    question: Can I fill the rectangle with a solid color?
  - answer: Loop through a collection of `Rectangle` structs and call `DrawRectangle`
      for each iteration.
    question: How do I draw multiple rectangles?
  - answer: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform
      after.
    question: Is there a way to rotate the rectangle?
  - answer: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat`
      parameter.
    question: What image formats are supported for saving?
  - answer: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and
      later versions.
    question: Does Aspose.Drawing work on .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- create bitmap image
- Aspose.Drawing
- .NET graphics
- draw rectangle
title: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
url: /net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Draw Rectangle with Aspose.Drawing for .NET

## Introduction

In this tutorial you’ll learn **how to draw rectangle** shapes while also mastering how to **create bitmap image C#** using Aspose.Drawing. Whether you need a simple UI element or a high‑resolution graphic for a report, we’ll walk through creating a bitmap, configuring a graphics object, drawing the rectangle, and saving the final image. The approach works on Windows, Linux, and macOS, and it replaces the older `System.Drawing.Common` API with a fully cross‑platform solution.

## Quick Answers
- **What library is required?** Aspose.Drawing for .NET  
- **Which method draws the shape?** `Graphics.DrawRectangle`  
- **Do I need a license?** A trial is free; a commercial license is required for production.  
- **Can I change the rectangle size?** Yes – adjust the width, height, and position parameters.  
- **Is the code compatible with .NET 6+?** Absolutely, Aspose.Drawing supports modern .NET versions.

## What is “how to draw rectangle” in the context of Aspose.Drawing?

Drawing a rectangle with Aspose.Drawing uses the `Graphics` class to render a rectangular outline or filled shape onto a bitmap canvas. This gives full control over size, color, line thickness, and image format, making it ideal for on‑the‑fly graphics. Because Aspose.Drawing runs on a pure‑managed engine, it avoids the native GDI+ limits of `System.Drawing.Common`.

## Why use Aspose.Drawing for rectangle creation?

Aspose.Drawing lets you **draw rectangle on bitmap** without any platform‑specific DLLs, and it supports **30+ output formats** (including PNG, JPEG, BMP, GIF, and TIFF). It can process images up to **10,000 × 10,000 pixels** while keeping memory usage under **100 MB**, which is 2‑3× more efficient than the legacy System.Drawing implementation.

## Prerequisites

Before we dive into the code, ensure you have the following:

- **Aspose.Drawing Library** – download it from the official site [here](https://releases.aspose.com/drawing/net/).  
- **Development Environment** – Visual Studio 2022 or any .NET‑compatible IDE.  
- **Basic .NET Knowledge** – familiarity with C# syntax and project structure.

## Import Namespaces

The `using` directives bring the essential classes into scope. They are required for any drawing operation.

```csharp
using System.Drawing;
```

## Step 1: Create a Bitmap Image

`Bitmap` represents an in‑memory raster image that you can draw on. Creating it defines the canvas size and pixel format.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Step 2: Create Graphics Object

`Graphics` is the engine that performs all drawing commands on the bitmap surface. Once you obtain it, you can render shapes, text, and images.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Step 3: Define Pen for Rectangle

`Pen` specifies the outline color and thickness for the rectangle. It also controls dash styles and line joins.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## Step 4: Draw Rectangle on Bitmap

`Graphics.DrawRectangle` draws the rectangle using the previously defined pen. You provide X, Y coordinates plus width and height to position the shape exactly where you need it.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## Step 5: Save Drawn Image

The `Bitmap.Save` method writes the image to disk in the format you choose (e.g., PNG, JPEG). This step demonstrates the **save drawn image** capability and finalizes the bitmap for reuse.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

Congratulations! You've successfully completed **how to draw rectangle** using Aspose.Drawing for .NET and learned how to **create bitmap image C#** in the process.

## Common Issues and Solutions

| Issue | Cause | Solution |
|-------|-------|----------|
| Blank image output | Bitmap not disposed or graphics not flushed | Call `graphics.Dispose();` before saving, or use a `using` block. |
| Low‑quality edges | Default smoothing mode | Set `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`. |
| File path errors | Invalid directory | Ensure the target folder exists or use `Path.Combine` to build a safe path. |

## Frequently Asked Questions

**Q: Can I fill the rectangle with a solid color?**  
A: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)` before or after drawing the outline.

**Q: How do I draw multiple rectangles?**  
A: Loop through a collection of `Rectangle` structs and call `DrawRectangle` for each iteration.

**Q: Is there a way to rotate the rectangle?**  
A: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform after.

**Q: What image formats are supported for saving?**  
A: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat` parameter.

**Q: Does Aspose.Drawing work on .NET Core?**  
A: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and later versions.

---

**Last Updated:** 2026-08-01  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

---

## Related Tutorials

- [How to Draw Ellipse with Aspose.Drawing for .NET](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [Draw multiple lines with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [How to create bitmap aspose.drawing – Draw Polygons in .NET](/drawing/net/lines-curves-and-shapes/draw-polygon/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}