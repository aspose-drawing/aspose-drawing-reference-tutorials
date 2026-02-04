---
title: "Create Bitmap with Aspose.Drawing – Units of Measure"
linktitle: Units of Measure in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: "Learn how to create bitmap Aspose.Drawing for .NET, draw rectangle with points, and master units of measure for precise graphics."
weight: 14
url: /net/coordinate-transformations/units-of-measure/
date: 2026-02-04
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create Bitmap with Aspose.Drawing – Units of Measure

## Introduction

In this tutorial you’ll **create bitmap Aspose.Drawing** for .NET and explore how different units of measure affect your drawings. We’ll walk through drawing rectangles using points, millimeters, and inches, so you can pick the right unit for any graphic‑intensive scenario. By the end you’ll be comfortable switching between units and producing pixel‑perfect images.

## Quick Answers
- **What is the primary purpose of this guide?** To show how to create a bitmap with Aspose.Drawing and draw shapes using various units of measure.  
- **Which units are demonstrated?** Points, millimeters, and inches.  
- **Do I need a license to run the examples?** A free trial works for evaluation; a commercial license is required for production.  
- **What .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Where can I download Aspose.Drawing?** From the official download page linked below.

## What is “create bitmap Aspose.Drawing”?
Creating a bitmap with Aspose.Drawing means instantiating a `Bitmap` object that you can draw on using the Aspose.Drawing graphics API. Unlike System.Drawing, Aspose.Drawing works consistently across all .NET platforms.

## Why use different units of measure?
Choosing the right unit (points, millimeters, inches) lets you align graphics with real‑world measurements, making it easier to integrate drawings into printed media, PDFs, or UI layouts where physical dimensions matter.

## Prerequisites

- **Aspose.Drawing for .NET** – download it [here](https://releases.aspose.com/drawing/net/).  
- **Document Directory** – a folder on your machine where the generated image will be saved.  
- **Basic C# Knowledge** – familiarity with classes, objects, and method calls.

## Import Namespaces

First, import the essential namespace so you can work with the drawing objects:

```csharp
using System.Drawing;
```

## Create Bitmap with Aspose.Drawing – Understanding Units of Measure

### Step 1: Create a Bitmap

We start by creating a 1000 × 800 pixel bitmap that will serve as our canvas.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Step 2: Create a Graphics Object

The `Graphics` object gives us drawing capabilities on the bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Draw Rectangle with Points

Points are a traditional printing unit (1 point = 1/72 inch). Setting the page unit to points lets you work with familiar typographic measurements.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

Now draw a rectangle using points. The pen width is set to 36 points (½ inch) for clear visibility.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

**Pro tip:** The coordinates `(72,72)` correspond to a 1‑inch offset from the top‑left corner because 72 points = 1 inch.

## Draw Rectangle in Millimeters

Millimeters are ideal for engineering drawings or when you need metric precision.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

The following rectangle uses a 6.35 mm pen (equivalent to 0.25 mm) and a 25.4 mm (1 inch) side length.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Draw Rectangle in Inches

Inches are common in U.S. printing and UI design. Switching to inches makes it easy to align with screen DPI settings.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

Here we draw a blue rectangle with a thin 0.125 inch pen.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Save the Result

After drawing all shapes, persist the bitmap to the file system. Adjust the path to match your document directory.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

When you open the saved PNG, you’ll see three rectangles—each rendered using a different unit of measure.

## Common Issues & Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Image appears blank** | Graphics object not flushed before saving. | Call `graphics.Dispose();` before `bitmap.Save()`. |
| **Incorrect dimensions** | Wrong `PageUnit` value. | Verify you set `graphics.PageUnit` to the intended `GraphicsUnit`. |
| **File path errors** | Missing folder or invalid characters. | Ensure the target directory exists and use `Path.Combine`. |

## FAQ's

### Q1: Can I use Aspose.Drawing for .NET with other .NET frameworks?

A1: Yes, Aspose.Drawing is compatible with various .NET frameworks, providing flexibility in your development environment.

### Q2: Is there a free trial available?

A2: Yes, you can explore Aspose.Drawing with a free trial [here](https://releases.aspose.com/).

### Q3: How do I get support for Aspose.Drawing for .NET?

A3: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) for community support and discussions.

### Q4: Can I purchase a temporary license for short‑term projects?

A4: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I find detailed documentation for Aspose.Drawing?

A5: The comprehensive documentation is available [here](https://reference.aspose.com/drawing/net/).

## Frequently Asked Questions

**Q: Does Aspose.Drawing support high‑DPI rendering?**  
A: Absolutely. The library respects the bitmap’s DPI settings, allowing crisp output on high‑resolution displays.

**Q: Can I combine multiple units in a single drawing?**  
A: You can switch `Graphics.PageUnit` at any point, but keep track of the current unit to avoid mismatched dimensions.

**Q: Is anti‑aliasing enabled by default?**  
A: Yes, Aspose.Drawing applies anti‑aliasing to shapes and text unless you explicitly disable it via `graphics.SmoothingMode`.

**Q: How do I release resources after drawing?**  
A: Call `graphics.Dispose();` and `bitmap.Dispose();` when you’re finished to free unmanaged memory.

**Q: Can I export the bitmap to formats other than PNG?**  
A: The `Bitmap.Save` method supports JPEG, BMP, GIF, and TIFF—just change the file extension.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2026-02-04  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

---