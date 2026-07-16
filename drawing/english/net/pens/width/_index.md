---
title: How to Change Thickness of Pens in Aspose.Drawing
linktitle: Setting Width of Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Learn how to change thickness of pens, save drawing as PNG, and create bitmap graphics using Aspose.Drawing for .NET in this step‑by‑step guide.
weight: 12
url: /net/pens/width/
date: 2026-02-19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Change Thickness of Pens in Aspose.Drawing

## Introduction

Welcome to this step‑by‑step guide on **how to change thickness** of pens using Aspose.Drawing for .NET. Whether you’re building a reporting tool, a design application, or simply need to draw sharper lines, controlling pen thickness is essential for visual impact. In this tutorial we’ll also show you how to **save drawing as PNG** and **create bitmap graphics** that can be reused across your projects.

## Quick Answers
- **What is the primary class for drawing?** `Graphics` from Aspose.Drawing.
- **How do I change pen thickness?** Set the second parameter of the `Pen` constructor (e.g., `new Pen(Color.Blue, 5)`).
- **Can I export the result as PNG?** Yes – use `bitmap.Save("Path\\Width_out.png")`.
- **Do I need a license for commercial use?** A commercial license is required; a free trial is available.
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.

## What is “how to change thickness” in drawing code?

Changing the thickness (or width) of a pen determines how bold a line appears on the canvas. A thicker pen draws a heavier line, which can be used to highlight sections, create borders, or simply improve readability of graphics.

## Why use Aspose.Drawing for this task?

Aspose.Drawing offers a pure .NET API that works without the limitations of `System.Drawing.Common` on non‑Windows platforms. It provides high‑performance rendering, extensive pixel‑format support, and seamless integration with other Aspose products.

## Prerequisites

Before you start, make sure you have:

1. **Aspose.Drawing Library** – download it from the [website](https://releases.aspose.com/drawing/net/).
2. **Development Environment** – Visual Studio, Rider, or any IDE that supports .NET development.

## Import Namespaces

Add the required namespace at the top of your C# file so you can access the drawing classes:

```csharp
using System.Drawing;
```

## Step 1: Create Bitmap and Graphics Objects

First, we’ll **create bitmap graphics** that serve as the drawing surface. A bitmap gives you a pixel‑perfect canvas that you can later export as PNG.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Step 2: Set Pen Thickness in a Loop

Now we’ll demonstrate **how to change thickness** by creating several pens with increasing widths and drawing horizontal lines. This visual example makes it easy to see the effect of each thickness level.

```csharp
for (int i = 1; i < 8; ++i)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), i);
    graphics.DrawLine(pen, 100, i * 100, 900, i * 100);
}
```

The loop draws seven lines, each with a different pen thickness from 1 to 7 pixels.

## Step 3: Save the Output Image

After drawing, you’ll want to **save drawing as PNG** so it can be used in web pages, reports, or further processing.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Width_out.png");
```

Replace `"Your Document Directory"` with the actual folder path where you’d like the PNG file to be stored.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **File path invalid** | Use `Path.Combine` to build the path safely, e.g., `Path.Combine(Environment.CurrentDirectory, "Pens", "Width_out.png")`. |
| **Pen appears too thin on high‑DPI displays** | Increase the thickness value or set `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |
| **Image looks blurry** | Ensure you use a high‑resolution bitmap (e.g., 300 DPI) by setting the appropriate `PixelFormat`. |

## Frequently Asked Questions

### Q1: Can I use Aspose.Drawing for commercial projects?

A1: Yes, Aspose.Drawing is suitable for both personal and commercial projects. Visit the [purchase page](https://purchase.aspose.com/buy) for licensing details.

### Q2: How can I get a temporary license for testing purposes?

A2: Obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/) to explore the full potential of Aspose.Drawing during the trial period.

### Q3: Where can I find additional support or ask questions?

A3: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) to seek assistance, share experiences, and connect with the community.

### Q4: Is there a free trial available?

A4: Yes, you can access the free trial version of Aspose.Drawing [here](https://releases.aspose.com/).

### Q5: What documentation resources are available?

A5: Refer to the [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/) for in‑depth information and examples.

### Q6: Can I change the pen color dynamically?

A6: Absolutely. Pass any `Color` object to the `Pen` constructor, e.g., `new Pen(Color.Red, 3)`. You can also use `Color.FromArgb` for custom colors.

### Q7: How do I draw anti‑aliased lines for smoother edges?

A7: Set `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;` before drawing your lines.

## Conclusion

You’ve now mastered **how to change thickness** of pens, learned to **create bitmap graphics**, and discovered how to **save drawing as PNG** using Aspose.Drawing for .NET. These techniques let you produce professional‑grade visuals that enhance the look and feel of any application.

---

**Last Updated:** 2026-02-19  
**Tested With:** Aspose.Drawing 24.10 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}