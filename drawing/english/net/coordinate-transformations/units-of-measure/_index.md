---
title: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
linktitle: Units of Measure in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics units easily, and master precise measurements for graphics rendering.
weight: 14
url: /net/coordinate-transformations/units-of-measure/
date: 2026-05-24
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
schemas:
- type: TechArticle
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  dateModified: '2026-05-24'
  author: Aspose
- type: HowTo
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
- type: FAQPage
  questions:
  - question: What is the primary way to change units?
    answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
  - question: Which unit equals 1/72 inch?
    answer: Points.
  - question: How many millimeters are in an inch?
    answer: 25.4 mm = 1 inch.
  - question: Do I need extra libraries to use units?
    answer: No, the Aspose.Drawing core library provides all unit constants.
  - question: Can I mix units in one image?
    answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Set Unit in Aspose.Drawing for .NET – Units of Measure

## Introduction

Welcome to the world of Aspose.Drawing for .NET, where precision and flexibility meet in graphic manipulation. In this tutorial you’ll discover **how to set unit** for your drawings, learn to **convert graphics units** between points, millimeters, and inches, and see real‑world examples that make your images pixel‑perfect. Whether you’re building reports, thumbnails, or custom charts, mastering units of measure is essential for consistent rendering across devices.

## Quick Answers
- **What is the primary way to change units?** Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`) on the `Graphics` object.  
- **Which unit equals 1/72 inch?** Points.  
- **How many millimeters are in an inch?** 25.4 mm = 1 inch.  
- **Do I need extra libraries to use units?** No, the Aspose.Drawing core library provides all unit constants.  
- **Can I mix units in one image?** Set the unit once per `Graphics` instance; draw everything using that unit for consistency.

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

## How to set unit to Points?

The `Bitmap` class represents an in‑memory image that serves as a drawing canvas. Load your bitmap, create a `Graphics` object, and set the page unit to points — this tells Aspose.Drawing to interpret all coordinates as 1/72 inch values. Using points gives you fine‑grained control for print‑ready graphics and lets you specify line widths with high precision.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Step 1: Create a Bitmap  
The `Bitmap` class represents an in‑memory image that serves as a drawing canvas.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Step 2: Create a Graphics Object  
`Graphics` provides drawing methods for rendering shapes and text onto a `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Step 3: Set Page Unit to Points  
`PageUnit` is an enumeration that specifies the unit of measure for page coordinates. `PageUnit.Point` defines points as the unit of measure (1 point = 1/72 inch). This setting applies to all subsequent drawing calls.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Step 4: Draw a Rectangle in Points  
When you draw a rectangle after setting the unit, the dimensions you specify are interpreted as points, ensuring precise sizing.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## How to set unit to Millimeters?

`PageUnit` is an enumeration that specifies the unit of measure for page coordinates. Switching to millimeters is helpful when you need metric dimensions, for example when generating engineering diagrams. Aspose.Drawing treats 1 mm as 1/25.4 inch, allowing you to align graphics with physical measurements used in manufacturing and technical documentation.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Step 1: Set Page Unit to Millimeters  
Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now map to the metric system.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Step 2: Draw a Rectangle in Millimeters  
The rectangle’s width and height are now expressed in millimeters, making it easy to align with physical measurements and ensuring that printed output matches real‑world sizes.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## How to set unit to Inches?

`Graphics` provides drawing methods for rendering shapes and text onto a `Bitmap`. Inches are the default unit for many U.S.‑based design tools. Setting the unit to inches lets you think in familiar terms when laying out UI elements, and it simplifies the transition from screen design to print where inches are commonly used.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Step 1: Set Page Unit to Inches  
`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch, providing a straightforward way to size elements for print‑oriented layouts.

CODE_BLOCK_PLACEHOLDER_10_END

### Step 2: Draw a Rectangle in Inches  
Now any shape you draw uses inches as its measurement base, which is ideal for print layouts and for communicating dimensions to stakeholders accustomed to imperial units.

CODE_BLOCK_PLACEHOLDER_11_END

## Save the Result

After completing the examples, save the resulting image to your document directory. The `Bitmap.Save` method writes the file in the format you specify (PNG, JPEG, etc.).

CODE_BLOCK_PLACEHOLDER_12_END

Now, you've successfully navigated the diverse units of measure in Aspose.Drawing for .NET, creating a visual representation of rectangles using points, millimeters, and inches.

## Why use Aspose.Drawing’s unit system?

Aspose.Drawing supports **30+ image formats** and can process images up to **5000 × 5000 pixels** without loading the entire file into memory, delivering high performance for large‑scale graphics generation. By explicitly setting the unit, you eliminate guesswork, reduce conversion errors, and ensure that your output matches exact physical dimensions across all platforms.

## Common Issues and Solutions

- **Unexpected size after saving** – Verify that you set `graphics.PageUnit` **before** any drawing calls; changing the unit later does not retroactively resize existing shapes.  
- **Blurry output on high‑DPI screens** – Increase the bitmap’s resolution (e.g., `new Bitmap(width, height, 300)`) to match the target DPI.  
- **Mixed units in one image** – Create separate `Graphics` instances for each unit or perform manual conversion before drawing.

## Frequently Asked Questions

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

---

**Last Updated:** 2026-05-24  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
