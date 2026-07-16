---
title: Set Text Alignment with Aspose.Drawing for .NET
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Learn how to set text alignment in Aspose.Drawing for .NET and add text to images. Step‑by‑step guide with examples.
weight: 11
url: /net/text-and-fonts/format-text/
date: 2026-02-25
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Text Alignment in Aspose.Drawing

## Introduction

When it comes to **set text alignment** and formatting text in your .NET applications, Aspose.Drawing is the go‑to library for developers who need precision, performance, and a rich API surface. Whether you’re building a reporting engine, a dynamic badge generator, or any graphic‑intensive solution, being able to control how text lines up inside shapes makes your output look polished and professional. In this tutorial we’ll walk through the entire process—from creating a bitmap canvas to drawing a rectangle with text, handling overflow, and finally saving the image.

## Quick Answers
- **What does “set text alignment” mean?** It defines how text is positioned horizontally and vertically within a drawing rectangle.  
- **Which class controls alignment?** `StringFormat` lets you set `Alignment` and `LineAlignment`.  
- **Can I draw a string and a rectangle together?** Yes—use `Graphics.DrawRectangle` followed by `Graphics.DrawString`.  
- **How do I prevent text overflow?** Adjust the rectangle size or split the text into multiple lines manually.  
- **Do I need a license for production?** A commercial Aspose.Drawing license is required for non‑evaluation use.

## What is **set text alignment** in Aspose.Drawing?

`set text alignment` refers to the configuration of horizontal (`StringAlignment`) and vertical (`LineAlignment`) positioning of text inside a `Rectangle` or any drawing region. By tweaking these settings you control whether the text appears left‑aligned, centered, right‑aligned, top‑aligned, middle‑aligned, or bottom‑aligned.

## Why use Aspose.Drawing for text alignment?

- **Full .NET compatibility** – works with .NET Framework, .NET Core, and .NET 5/6+.  
- **Pixel‑perfect rendering** – anti‑aliasing and high‑DPI support out of the box.  
- **No GDI+ limitations** – unlike `System.Drawing.Common`, Aspose.Drawing runs on Linux containers without native dependencies.  
- **Rich styling** – combine fonts, brushes, pens, and custom `StringFormat` objects for sophisticated layouts.

## Prerequisites

1. **Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).  
2. **Development Environment** – Visual Studio 2022 (or any C# IDE).  
3. **Basic .NET knowledge** – you should be comfortable with C# projects and NuGet packages.

## Import Namespaces

To start, bring the required namespaces into scope. These give you access to graphics, text rendering, and drawing primitives.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step 1: Create Bitmap and Graphics Objects  

Creating a bitmap provides a canvas you can draw on. The `Graphics` object is the drawing surface, and we enable high‑quality text rendering with `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Step 2: Define **StringFormat** and Styling  

Here we **set text alignment** by configuring a `StringFormat` instance. We also prepare brushes, pens, and a font that will be used when drawing the string.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Step 3: Create and Format Text – **how to draw string** and **draw rectangle with text**

We compose the text, define the rectangle that will contain it, and then draw both the rectangle border and the string itself.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### How to handle text overflow

If the supplied `text` exceeds the rectangle’s bounds, you have two common options:

1. **Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.  
2. **Split the text** – break the string into lines that fit, then call `DrawString` for each line with adjusted Y‑coordinates.

## Step 4: Save the Output – **add text to image**

Finally, write the bitmap to disk. This step demonstrates **add text to image** in a single call.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Text appears blurry** | Ensure `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` is set. |
| **Text is clipped** | Increase the rectangle size or enable word‑wrap logic by measuring string size (`Graphics.MeasureString`). |
| **Font not found** | Verify the font is installed on the host machine or embed a private font using `PrivateFontCollection`. |
| **Unexpected colors** | Double‑check brush and pen colors; remember that `Color.FromKnownColor` uses system‑defined colors. |

## Frequently Asked Questions

### Q1: Is Aspose.Drawing compatible with all .NET versions?

A1: Yes, Aspose.Drawing is designed to be compatible with a wide range of .NET versions, ensuring flexibility for developers.

### Q2: Can I customize the font style further?

A2: Absolutely! Adjust the `Font` object parameters to achieve the desired font size, style, and family.

### Q3: How can I handle text overflow within the defined rectangle?

A3: You can manage text overflow by adjusting the size of the rectangle or implementing custom logic to handle lengthy text.

### Q4: Are there other formatting options available in Aspose.Drawing?

A4: Yes, Aspose.Drawing provides a comprehensive set of tools for graphic manipulation, including various formatting options for text, shapes, and more.

### Q5: Where can I find additional support for Aspose.Drawing?

A5: Explore the Aspose.Drawing forum [here](https://forum.aspose.com/c/drawing/44) for community support and discussions.

**Additional Q&A**

**Q: How do I draw a string without a surrounding rectangle?**  
A: Omit the `DrawRectangle` call and pass the desired `PointF` location to `Graphics.DrawString`.

**Q: Can I rotate the text while keeping alignment?**  
A: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing, then reset it afterwards.

**Q: Is it possible to export the image as JPEG instead of PNG?**  
A: Simply change the file extension in `bitmap.Save` and optionally specify `ImageFormat.Jpeg`.

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}