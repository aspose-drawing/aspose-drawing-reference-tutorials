---
title: Units of Measure in Aspose.Drawing for .NET
linktitle: Units of Measure in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Explore the versatility of Aspose.Drawing for .NET in this in-depth tutorial, mastering units of measure for precision graphics.
type: docs
weight: 14
url: /net/coordinate-transformations/units-of-measure/
---
## Introduction

Welcome to the world of Aspose.Drawing for .NET, where precision and flexibility meet in graphic manipulation. In this tutorial, we'll delve into the intricacies of units of measure within Aspose.Drawing, providing you with a step-by-step guide to harness the power of this remarkable library.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites in place:

- Aspose.Drawing for .NET: Ensure that you have the library installed. You can download it [here](https://releases.aspose.com/drawing/net/).

- Document Directory: Have a designated directory where you want to save your created documents.

- Basic C# Knowledge: A fundamental understanding of C# is recommended to make the most out of this guide.

## Import Namespaces

Before we start, let's import the necessary namespaces to use Aspose.Drawing effectively:

```csharp
using System.Drawing;
```

Now, let's break down each example into multiple steps:

## Points as Units of Measure

1. Create a Bitmap: Initialize a bitmap with a specified width and height.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Create Graphics: Generate a Graphics object from the bitmap to draw on it.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Set Page Unit to Points: Define points as the unit of measure (1 point = 1/72 inch).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Draw Rectangle: Draw a rectangle using points as the unit.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Millimeters as Units of Measure

1. Set Page Unit to Millimeters: Change the unit of measure to millimeters (1 mm = 1/25.4 inch).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Draw Rectangle in Millimeters: Draw another rectangle using millimeters as the unit.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Inches as Units of Measure

1. Set Page Unit to Inches: Switch the unit of measure to inches.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Draw Rectangle in Inches: Draw a rectangle using inches as the unit.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Save the Result

After completing the examples, save the resulting image to your document directory:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Now, you've successfully navigated the diverse units of measure in Aspose.Drawing for .NET, creating a visual representation of rectangles using points, millimeters, and inches.

## Conclusion

In this tutorial, we've explored how Aspose.Drawing for .NET handles different units of measure. By manipulating points, millimeters, and inches, you can achieve precision and adaptability in your graphic creations. Experiment with these concepts to unlock the full potential of Aspose.Drawing.

## FAQ's

### Q1: Can I use Aspose.Drawing for .NET with other .NET frameworks?

A1: Yes, Aspose.Drawing is compatible with various .NET frameworks, providing flexibility in your development environment.

### Q2: Is there a free trial available?

A2: Yes, you can explore Aspose.Drawing with a free trial [here](https://releases.aspose.com/).

### Q3: How do I get support for Aspose.Drawing for .NET?

A3: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17) for community support and discussions.

### Q4: Can I purchase a temporary license for short-term projects?

A4: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I find detailed documentation for Aspose.Drawing?

A5: The comprehensive documentation is available [here](https://reference.aspose.com/drawing/net/).
