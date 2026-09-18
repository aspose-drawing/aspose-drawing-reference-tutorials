---
date: 2026-09-18
description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored lines,
  and save PNG images with simple code examples.
images:
- /net/pens/colors/og-image.png
keywords:
- set pen color
- save png image
- cross platform drawing
- draw lines with pen
- high quality png
lastmod: 2026-09-18
linktitle: Working with colors in Aspose.Drawing
og_description: Set pen color in Aspose.Drawing for .NET and create high‑quality PNG
  images. Learn cross‑platform drawing, draw lines with pen, and save PNG images in
  minutes.
og_image_alt: Screenshot of code setting pen color and saving a PNG with Aspose.Drawing
og_title: Set pen color in Aspose.Drawing – guide for high‑quality PNG output
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored
    lines, and save PNG images with simple code examples.
  headline: How to set pen color in Aspose.Drawing
  type: TechArticle
- description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored
    lines, and save PNG images with simple code examples.
  name: How to set pen color in Aspose.Drawing
  steps:
  - name: '**Aspose.Drawing Library** – download and install from the official site
      **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.'
    text: '**Aspose.Drawing Library** – download and install from the official site
      **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.'
  - name: '**A .NET development environment** – Visual Studio, VS Code, or any IDE
      you prefer.'
    text: '**A .NET development environment** – Visual Studio, VS Code, or any IDE
      you prefer.'
  - name: '**Basic C# knowledge** – familiarity with classes, objects, and namespaces.'
    text: '**Basic C# knowledge** – familiarity with classes, objects, and namespaces.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing integrates smoothly with other .NET libraries, providing
      a versatile environment for graphic manipulation.
    question: Can I use Aspose.Drawing with other .NET libraries?
  - answer: You can get a temporary license **[Aspose temporary license page](https://purchase.aspose.com/temporary-license/)**,
      allowing you to explore the full potential of Aspose.Drawing.
    question: How can I obtain a temporary license for Aspose.Drawing?
  - answer: Yes, Aspose.Drawing supports JPEG, GIF, BMP, TIFF, and more. Refer to
      the documentation for a complete list.
    question: Does Aspose.Drawing support image formats other than PNG?
  - answer: Absolutely! Aspose.Drawing works in both desktop and web applications,
      enabling dynamic graphic generation on servers.
    question: Can I use Aspose.Drawing for web development?
  - answer: Yes, you can explore a free trial **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**,
      letting you evaluate the library before purchasing.
    question: Is there a free trial available for Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- .NET graphics
- pen color
- PNG output
title: How to set pen color in Aspose.Drawing
url: /net/pens/colors/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to set pen color in Aspose.Drawing

## Introduction

In this tutorial you’ll learn how to **set pen color** when drawing with Aspose.Drawing for .NET, create a graphics canvas, draw colored lines, and **save PNG image** files with high quality. Whether you’re building a desktop utility, a reporting service, or a web API that generates charts, controlling pen colors is essential for professional‑looking graphics.

## Quick answers
- **What is the primary class for drawing?** `Graphics` created from a `Bitmap`.
- **How do I change a pen’s color?** Use `Color.FromKnownColor` or `Color.FromArgb`.
- **Which format is recommended for lossless output?** PNG (`.png`).
- **Do I need a license for development?** A temporary license is available for evaluation.
- **Can I use this in ASP.NET Core?** Yes, Aspose.Drawing works with .NET Core and .NET 5+.

## What is “set pen color” in Aspose.Drawing?

Setting the pen color means assigning a `Color` value to a `Pen` object before any drawing operation. The chosen color influences the hue, opacity, and thickness of lines, shapes, and text strokes rendered on the canvas, allowing precise visual control over the final image output.

## Why use Aspose.Drawing for color manipulation?

Aspose.Drawing provides **cross‑platform drawing** that runs on Windows, Linux, and macOS without the System.Drawing.Common limitations. It supports **high‑quality PNG** output (up to 32‑bit ARGB) and offers a rich set of color APIs, including 50+ known colors and full ARGB customisation. The library can process multi‑hundred‑page images while keeping memory usage under 50 MB, making it suitable for server‑side generation.

## Prerequisites

Before we dive into the code, ensure you have:

1. **Aspose.Drawing Library** – download and install from the official site **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.  
2. **A .NET development environment** – Visual Studio, VS Code, or any IDE you prefer.  
3. **Basic C# knowledge** – familiarity with classes, objects, and namespaces.

## Import namespaces

The `Aspose.Drawing` namespace is the core library that provides all drawing‑related types such as `Bitmap`, `Graphics`, `Pen`, and `Color`, enabling developers to create, manipulate, and render images across platforms without relying on System.Drawing.Common.

```csharp
using System.Drawing;
```

## Step 1: create a bitmap (the canvas)

The `Bitmap` class represents an in‑memory pixel buffer that can be drawn upon; it supports various pixel formats, including 32‑bit ARGB, which preserves full color depth and transparency essential for high‑quality PNG output.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Step 2: create a graphics object

The `Graphics` object acts as a drawing surface tied to a `Bitmap`, offering methods such as `DrawLine`, `DrawRectangle`, and `DrawString` that render shapes, lines, and text onto the underlying image buffer.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Step 3: draw a line with a blue pen (first colored line)

The `Pen` class defines the attributes of lines and outlines, including color, width, dash style, and alignment, and is used by `Graphics` methods to stroke shapes and paths on the canvas.

```csharp
Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawLine(bluePen, 100, 100, 900, 100);
```

## Step 4: draw a line with a custom red pen

This example shows how to **draw colored lines** with a custom ARGB value, giving you full control over opacity and exact shade.

```csharp
Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
graphics.DrawLine(redPen, 100, 200, 900, 200);
```

## Step 5: save the image as PNG

Finally, we **save PNG image** to the desired folder. PNG preserves transparency and color fidelity, making it the preferred format for web graphics and reports.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
```

## Common issues and solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **Image appears blank** | Graphics not flushed before saving | Call `graphics.Dispose();` or wrap `Graphics` in a `using` block. |
| **Incorrect colors** | Using `FromKnownColor` with wrong enum | Verify the enum value or use `FromArgb` for precise control. |
| **File path errors** | Invalid directory or missing permissions | Ensure the target folder exists and the app has write access. |

## Frequently asked questions

**Q: Can I use Aspose.Drawing with other .NET libraries?**  
A: Yes, Aspose.Drawing integrates smoothly with other .NET libraries, providing a versatile environment for graphic manipulation.

**Q: How can I obtain a temporary license for Aspose.Drawing?**  
A: You can get a temporary license **[Aspose temporary license page](https://purchase.aspose.com/temporary-license/)**, allowing you to explore the full potential of Aspose.Drawing.

**Q: Does Aspose.Drawing support image formats other than PNG?**  
A: Yes, Aspose.Drawing supports JPEG, GIF, BMP, TIFF, and more. Refer to the documentation for a complete list.

**Q: Can I use Aspose.Drawing for web development?**  
A: Absolutely! Aspose.Drawing works in both desktop and web applications, enabling dynamic graphic generation on servers.

**Q: Is there a free trial available for Aspose.Drawing?**  
A: Yes, you can explore a free trial **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**, letting you evaluate the library before purchasing.

## Conclusion

In this guide we covered how to **set pen color**, **draw colored lines**, **create a graphics object**, and **save the result as a high‑quality PNG** using Aspose.Drawing for .NET. These fundamentals open the door to more advanced scenarios such as drawing shapes, rendering text, and generating charts dynamically. If you run into challenges, the Aspose.Drawing **[documentation](https://reference.aspose.com/drawing/net/)** and **[support forum](https://forum.aspose.com/c/drawing/44)** are excellent places to find answers.

---

**Last Updated:** 2026-09-18  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Related Tutorials

- [How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [How to Join Paths with Pen in Aspose.Drawing .NET](/drawing/net/pens/)
- [Improve Image Quality with Antialiasing in Aspose.Drawing](/drawing/net/rendering/antialiasing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}