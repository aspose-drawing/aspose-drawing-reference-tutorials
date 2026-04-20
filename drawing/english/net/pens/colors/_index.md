---
title: How to set pen color in Aspose.Drawing for .NET
linktitle: Working with Colors in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored lines, and save PNG images with simple code examples.
weight: 10
url: /net/pens/colors/
date: 2026-02-22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to set pen color in Aspose.Drawing

## Introduction

Welcome to our step‑by‑step guide on how to **set pen color** when drawing with Aspose.Drawing for .NET. In this tutorial you’ll learn to create a graphics object, draw colored lines, and **save image PNG** files—all with clear, real‑world code examples. Whether you’re building a desktop utility or a web service that generates charts, mastering pen colors is essential for producing professional‑looking graphics.

## Quick Answers
- **What is the primary class for drawing?** `Graphics` created from a `Bitmap`.
- **How do I change a pen’s color?** Use `Color.FromKnownColor` or `Color.FromArgb`.
- **Which format is recommended for lossless output?** PNG (`.png`).
- **Do I need a license for development?** A temporary license is available for evaluation.
- **Can I use this in ASP.NET Core?** Yes, Aspose.Drawing works with .NET Core and .NET 5+.

## What is “set pen color” in Aspose.Drawing?

Setting the pen color means assigning a `Color` value to a `Pen` object before drawing. The color determines how lines, shapes, or text appear on the canvas. Aspose.Drawing mirrors the familiar System.Drawing API, so you can use `Color.FromKnownColor`, `Color.FromArgb`, or predefined `Color` properties.

## Why use Aspose.Drawing for color manipulation?

* **Cross‑platform support** – works on Windows, Linux, and macOS without the System.Drawing.Common limitations.  
* **Full .NET compatibility** – integrates seamlessly with .NET 6, .NET Core, and .NET Framework projects.  
* **Rich color APIs** – easy creation of custom ARGB colors, known colors, and gradient brushes.  
* **High‑quality PNG output** – perfect for web graphics, reports, and thumbnails.

## Prerequisites

Before we dive into the code, ensure you have:

1. **Aspose.Drawing Library** – download and install from the official site **[here](https://releases.aspose.com/drawing/net/)**.  
2. **A .NET development environment** – Visual Studio, VS Code, or any IDE you prefer.  
3. **Basic C# knowledge** – familiarity with classes, objects, and namespaces.

## Import Namespaces

In your C# file, import the namespace that gives you access to Aspose.Drawing’s drawing primitives.

```csharp
using System.Drawing;
```

## Step 1: Create a Bitmap (the canvas)

A `Bitmap` represents the pixel buffer we’ll draw onto. Here we create a 1000 × 800 canvas with a 32‑bit ARGB pixel format.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Step 2: Create a Graphics object

The `Graphics` object is the drawing surface that lets you render shapes, text, and images onto the bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Step 3: Draw a line with a blue pen (first colored line)

We **set pen color** to blue using `Color.FromKnownColor`. The pen width is set to 2 pixels.

```csharp
Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawLine(bluePen, 100, 100, 900, 100);
```

## Step 4: Draw a line with a custom red pen

This example shows how to **draw colored lines** with a custom ARGB value, giving you full control over opacity and exact shade.

```csharp
Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
graphics.DrawLine(redPen, 100, 200, 900, 200);
```

## Step 5: Save the image as PNG

Finally, we **save image PNG** to the desired folder. Adjust the path to match your project’s output directory.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
```

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **Image appears blank** | Graphics not flushed before saving | Call `graphics.Dispose();` or wrap `Graphics` in a `using` block. |
| **Incorrect colors** | Using `FromKnownColor` with wrong enum | Verify the enum value or use `FromArgb` for precise control. |
| **File path errors** | Invalid directory or missing permissions | Ensure the target folder exists and the app has write access. |

## Frequently Asked Questions

**Q: Can I use Aspose.Drawing with other .NET libraries?**  
A: Yes, Aspose.Drawing seamlessly integrates with other .NET libraries, providing a versatile environment for graphic manipulation.

**Q: How can I obtain a temporary license for Aspose.Drawing?**  
A: You can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**, allowing you to explore the full potential of Aspose.Drawing.

**Q: Does Aspose.Drawing support image formats other than PNG?**  
A: Yes, Aspose.Drawing supports various image formats, including JPEG, GIF, BMP, and more. Refer to the documentation for a complete list.

**Q: Can I use Aspose.Drawing for web development?**  
A: Absolutely! Aspose.Drawing is versatile and can be used in both desktop and web applications, adding dynamic graphic features to your websites.

**Q: Is there a free trial available for Aspose.Drawing?**  
A: Yes, you can explore a free trial **[here](https://releases.aspose.com/drawing/net/)**, allowing you to experience the capabilities of Aspose.Drawing before making a purchase.

## Conclusion

In this tutorial we covered how to **set pen color**, **draw colored lines**, **create a graphics object**, and **save the result as a PNG** using Aspose.Drawing for .NET. These fundamentals open the door to more advanced scenarios such as drawing shapes, rendering text, and generating charts dynamically. If you run into challenges, the Aspose.Drawing **[documentation](https://reference.aspose.com/drawing/net/)** and **[support forum](https://forum.aspose.com/c/drawing/44)** are excellent places to find answers.

---

**Last Updated:** 2026-02-22  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}