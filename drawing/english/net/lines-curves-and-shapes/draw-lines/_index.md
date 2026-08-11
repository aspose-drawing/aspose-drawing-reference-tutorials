---
title: "How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing"
linktitle: Draw multiple lines with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line bitmap techniques, and best practices.
weight: 16
url: /net/lines-curves-and-shapes/draw-lines/
date: 2026-06-13
keywords:
- save bitmap as png
- draw multiple lines
- how to draw lines
schemas:
- type: TechArticle
  headline: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  dateModified: '2026-06-13'
  author: Aspose
- type: HowTo
  name: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  steps:
  - name: Create a Bitmap (draw line bitmap)
    text: The `Bitmap` class represents an in‑memory raster image that you can draw
      onto. Start by creating a new bitmap with the desired width and height. This
      will be the canvas on which you draw your lines.
  - name: Get Graphics Object
    text: The `Graphics` object provides drawing methods such as lines, shapes, and
      text for a bitmap. Obtain a `Graphics` object from the created bitmap. This
      object provides methods for drawing on the bitmap.
  - name: Define a Pen
    text: A `Pen` defines the color, width, and style of lines drawn by the `Graphics`
      object. Create a `Pen` object that defines the attributes of the line you want
      to draw. In this case, we've chosen a blue color with a thickness of 2 pixels.
  - name: Draw Lines
    text: Use the `DrawLine` method to draw lines on the bitmap. The coordinates `(x1,
      y1)` to `(x2, y2)` represent the starting and ending points of each line. By
      calling the method twice, we effectively **draw multiple lines** that form a
      simple “V” shape.
  - name: Save the Image
    text: The `Bitmap.Save` method writes the in‑memory image to a file in the format
      you specify—PNG being the most common loss‑less option. Specify the directory
      where you want to save the output image. Make sure to replace `"Your Document
      Directory"` with the actual path.
- type: FAQPage
  questions:
  - question: Can I change the color of the lines?
    answer: Yes, simply modify the `Color` parameter when creating the `Pen` object.
  - question: What other shapes can I draw with Aspose.Drawing?
    answer: Aspose.Drawing supports rectangles, ellipses, curves, polygons, and more.
      Check the official documentation for a complete list.
  - question: Is Aspose.Drawing suitable for web applications?
    answer: Absolutely. It works in ASP.NET Core, MVC, and other web frameworks, allowing
      server‑side image generation without additional dependencies.
  - question: How should I handle errors while using Aspose.Drawing?
    answer: Wrap your drawing code in a `try‑catch` block and consult the Aspose.Drawing
      forum (https://forum.aspose.com/c/drawing/44) for community support.
  - question: Can I use Aspose.Drawing for a commercial project?
    answer: Yes, you can use Aspose.Drawing for commercial projects. Visit the [purchase
      page](https://purchase.aspose.com/buy) for licensing details.
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save bitmap as PNG while drawing multiple lines with Aspose.Drawing

## Introduction

In this tutorial you’ll learn **how to save bitmap as PNG** and draw multiple lines using Aspose.Drawing for .NET. Whether you’re creating a simple chart, a custom UI control, or generating graphics on a server, the ability to render crisp, anti‑aliased lines and then persist them as PNG files is a core skill. We’ll walk through the entire workflow—from preparing the canvas to exporting the final image—so you can start building visual components right away.

## Quick Answers
- **What can I draw?** Any straight line, polyline, or shape on a bitmap.  
- **Which library?** Aspose.Drawing for .NET (no System.Drawing.Common required).  
- **How many lines?** Draw as many as you need – the same `Graphics.DrawLine` call can be repeated.  
- **Prerequisites?** .NET development environment and the Aspose.Drawing library.  
- **Output format?** PNG, JPEG, BMP, or any format supported by Aspose.Drawing.

## What is drawing multiple lines?

Drawing multiple lines means rendering two or more straight line segments on the same image canvas. In Aspose.Drawing you achieve this by reusing a single `Graphics` object and invoking `DrawLine` for each coordinate pair, which delivers fast, memory‑efficient rendering for both raster and vector outputs.

## Why use Aspose.Drawing for .net line drawing?

Aspose.Drawing provides a modern, cross‑platform API that supports **over 30 output formats** and can process images up to **10,000 × 10,000 pixels** without loading the entire file into memory. It offers built‑in anti‑aliasing, precise pixel control, and full .NET Core/5+ compatibility, eliminating the legacy dependencies of `System.Drawing.Common`.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Aspose.Drawing Library: Download and install the Aspose.Drawing library from [here](https://releases.aspose.com/drawing/net/).
- Development Environment: Ensure that you have a .NET development environment set up on your machine.
- Document Directory: Create a directory on your system where you want to save the output images.

## Import Namespaces

In your .NET application, you need to import the necessary namespaces to work with Aspose.Drawing. Add the following namespaces at the beginning of your code:

```csharp
using System.Drawing;
```

Now, let's break down the example into multiple steps to guide you through the process of drawing lines using Aspose.Drawing.

## How to draw multiple lines in Aspose.Drawing

Load a bitmap, obtain a `Graphics` object, configure a `Pen`, call `DrawLine` for each segment, and finally save the canvas as PNG – all in five concise steps that can be repeated or extended for more complex drawings. Each step is illustrated with code snippets that demonstrate the required API calls and optional settings such as anti‑aliasing.

### Step 1: Create a Bitmap (draw line bitmap)

The `Bitmap` class represents an in‑memory raster image that you can draw onto.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, PixelFormat.Format32bppPArgb);
```

Start by creating a new bitmap with the desired width and height. This will be the canvas on which you draw your lines.

### Step 2: Get Graphics Object

The `Graphics` object provides drawing methods such as lines, shapes, and text for a bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

Obtain a `Graphics` object from the created bitmap. This object provides methods for drawing on the bitmap.

### Step 3: Define a Pen

A `Pen` defines the color, width, and style of lines drawn by the `Graphics` object.  
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

Create a `Pen` object that defines the attributes of the line you want to draw. In this case, we've chosen a blue color with a thickness of 2 pixels.

### Step 4: Draw Lines

Use the `DrawLine` method to draw lines on the bitmap. The coordinates `(x1, y1)` to `(x2, y2)` represent the starting and ending points of each line. By calling the method twice, we effectively **draw multiple lines** that form a simple “V” shape.  
```csharp
graphics.DrawLine(pen, 10, 700, 500, 10);
graphics.DrawLine(pen, 500, 10, 990, 700);
```

### Step 5: Save the Image

The `Bitmap.Save` method writes the in‑memory image to a file in the format you specify—PNG being the most common loss‑less option.  
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawLines_out.png");
```

Specify the directory where you want to save the output image. Make sure to replace `"Your Document Directory"` with the actual path.

## How to save bitmap as PNG

Saving a bitmap as PNG is a single‑line operation: call `bitmap.Save("output.png", ImageFormat.Png)` on the `Bitmap` instance you have already drawn on. The `ImageFormat` class specifies the file format for saving images, such as PNG, JPEG, or BMP. Aspose.Drawing automatically handles compression and preserves transparency, making PNG ideal for web and UI assets.

## Common Issues and Solutions

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **Image appears blank** | Graphics object not linked to bitmap or wrong pixel format. | Ensure `Graphics.FromImage(bitmap)` is used and the bitmap is created with a supported pixel format. |
| **Lines are jagged** | Anti‑aliasing disabled. | Set `graphics.SmoothingMode = SmoothingMode.AntiAlias;` before drawing (requires `using System.Drawing.Drawing2D;`). |
| **Path not found on Save** | Invalid directory string. | Use `Path.Combine` to build the path and verify the folder exists. |

The `SmoothingMode` enumeration controls the rendering quality of lines, with `AntiAlias` providing smoother edges.

## Frequently Asked Questions

**Q: Can I change the color of the lines?**  
A: Yes, simply modify the `Color` parameter when creating the `Pen` object.

**Q: What other shapes can I draw with Aspose.Drawing?**  
A: Aspose.Drawing supports rectangles, ellipses, curves, polygons, and more. Check the official documentation for a complete list.

**Q: Is Aspose.Drawing suitable for web applications?**  
A: Absolutely. It works in ASP.NET Core, MVC, and other web frameworks, allowing server‑side image generation without additional dependencies.

**Q: How should I handle errors while using Aspose.Drawing?**  
A: Wrap your drawing code in a `try‑catch` block and consult the Aspose.Drawing forum (https://forum.aspose.com/c/drawing/44) for community support.

**Q: Can I use Aspose.Drawing for a commercial project?**  
A: Yes, you can use Aspose.Drawing for commercial projects. Visit the [purchase page](https://purchase.aspose.com/buy) for licensing details.

## Conclusion

In this guide we covered everything you need to **save bitmap as PNG while drawing multiple lines** with Aspose.Drawing for .NET: creating a bitmap, obtaining a graphics context, configuring a pen, rendering lines, and persisting the result. With this foundation you can expand to dynamic charts, custom UI elements, or server‑side graphics generation—any scenario that demands high‑quality, scalable line rendering.

---

**Last Updated:** 2026-06-13  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [Save Bitmap as PNG & Draw Closed Curves with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Save Bitmap C# – Draw Bezier Splines with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Save Bitmap as PNG with Solid Brushes in Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}