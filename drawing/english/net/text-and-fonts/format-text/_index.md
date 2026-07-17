---
date: 2026-07-17
description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
  for .NET and add text to images. Step‑by‑step guide with examples.
images:
- /net/text-and-fonts/format-text/og-image.png
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Set Text Alignment with Aspose.Drawing for .NET
og_description: Prevent text overflow by setting text alignment in Aspose.Drawing
  for .NET. Learn to draw string on image, center text in rectangle, and replace System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
url: /net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Prevent Text Overflow – Set Text Alignment with Aspose.Drawing

## Introduction

When you need to **prevent text overflow** while rendering graphics in .NET, Aspose.Drawing gives you fine‑grained control over text placement, alignment, and wrapping. Whether you’re building a badge generator, a dynamic report, or any image‑based output, mastering text alignment ensures that your text stays inside the intended rectangle and looks polished. In this guide we’ll walk through creating a bitmap canvas, configuring `StringFormat`, drawing a rectangle with centered text, handling overflow, and finally saving the image.

## Quick Answers
- **What does “set text alignment” mean?** It defines how text is positioned horizontally and vertically within a drawing rectangle.  
- **Which class controls alignment?** `StringFormat` lets you set `Alignment` and `LineAlignment`.  
- **Can I draw a string and a rectangle together?** Yes—use `Graphics.DrawRectangle` followed by `Graphics.DrawString`.  
- **How do I prevent text overflow?** Adjust the rectangle size or split the text into multiple lines manually.  
- **Do I need a license for production?** A commercial Aspose.Drawing license is required for non‑evaluation use.

## What is **set text alignment** in Aspose.Drawing?

`set text alignment` configures horizontal (`StringAlignment`) and vertical (`LineAlignment`) placement of text within a `Rectangle` or drawing region. By adjusting these properties you control whether text appears left‑aligned, centered, right‑aligned, top‑aligned, middle‑aligned, or bottom‑aligned, enabling precise layout in graphics, badges, and reports generated with Aspose.Drawing.

## Why use Aspose.Drawing for text alignment?

Aspose.Drawing eliminates the GDI+ limitations that plague `System.Drawing.Common`. It supports **5 major .NET runtimes** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6, and .NET 7 – and can render images up to **4000 × 4000 px** (≈ 100 MB) without exhausting memory. Anti‑aliasing, high‑DPI scaling, and full Linux container compatibility let you generate pixel‑perfect graphics in any deployment scenario.

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

## How to prevent text overflow with Aspose.Drawing?

Bitmap is a class representing an image stored in memory, while `RectangleF` defines a floating‑point rectangle area for drawing. By using a `StringFormat` with `Trimming` set to `StringTrimming.EllipsisCharacter`, excess characters are automatically replaced with an ellipsis, ensuring the text never exceeds the rectangle bounds. Measuring the string first lets you decide whether to shrink the rectangle or split the text into multiple lines, guaranteeing a clean layout without spill‑over.

Load your bitmap, define a suitably sized `RectangleF`, and use a `StringFormat` with `Trimming` set to `StringTrimming.EllipsisCharacter` to automatically cut off excess characters. For full control, measure the string with `Graphics.MeasureString` and shrink the rectangle or split the text into lines before drawing. This approach guarantees that no characters spill outside the visual bounds.

## Step 1: Create Bitmap and Graphics Objects  

Bitmap represents an in‑memory image, while Graphics provides drawing methods for that bitmap. Creating a bitmap provides a canvas you can draw on. The `Graphics` object is the drawing surface, and we enable high‑quality text rendering with `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Step 2: Define **StringFormat** and Styling  

StringFormat specifies text layout options such as alignment, line spacing, and trimming. Here we **set text alignment** by configuring a `StringFormat` instance. We also prepare brushes, pens, and a font that will be used when drawing the string.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Step 3: Create and Format Text – **how to draw string** and **draw rectangle with text**

Graphics.DrawString renders text onto the canvas, and Graphics.DrawRectangle draws a rectangle shape. We compose the text, define the rectangle that will contain it, and then draw both the rectangle border and the string itself.

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

## How to draw string on image using Aspose.Drawing?

Graphics.DrawString draws the specified text using a font and formatting options. Instantiate a `Graphics` object from your bitmap, then call `DrawString` with the prepared `StringFormat`. This single call renders the text exactly where you want it, respecting alignment, trimming, and any transformation matrix you have applied. Adding a high‑quality rendering hint ensures the output remains crisp on high‑DPI displays.

## How to center text in rectangle?

StringAlignment determines horizontal alignment of text within a layout rectangle. Set `stringFormat.Alignment = StringAlignment.Center` and `stringFormat.LineAlignment = StringAlignment.Center`. This centers the text horizontally and vertically inside the rectangle, making it ideal for badges, buttons, or label overlays. The centered placement works consistently across different image sizes and DPI settings, providing a balanced visual appearance.

## How to achieve vertical text alignment?

LineAlignment controls vertical placement of text inside the rectangle. Use `stringFormat.LineAlignment` with values `StringAlignment.Near`, `Center`, or `Far` to position text at the top, middle, or bottom of the rectangle. Combine this with `Graphics.TranslateTransform` if you need to rotate the text while preserving vertical alignment. Adjusting the line alignment ensures that multi‑line blocks line up exactly where you expect them to, even after transformations.

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

**Q1: Is Aspose.Drawing compatible with all .NET versions?**  
A1: Yes, Aspose.Drawing is designed to be compatible with a wide range of .NET versions, ensuring flexibility for developers.

**Q2: Can I customize the font style further?**  
A2: Absolutely! Adjust the `Font` object parameters to achieve the desired font size, style, and family.

**Q3: How can I handle text overflow within the defined rectangle?**  
A3: You can manage text overflow by adjusting the size of the rectangle or implementing custom logic to handle lengthy text.

**Q4: Are there other formatting options available in Aspose.Drawing?**  
A4: Yes, Aspose.Drawing provides a comprehensive set of tools for graphic manipulation, including various formatting options for text, shapes, and more.

**Q5: Where can I find additional support for Aspose.Drawing?**  
A5: Explore the Aspose.Drawing forum [here](https://forum.aspose.com/c/drawing/44) for community support and discussions.

**Additional Q&A**

**Q: How do I draw a string without a surrounding rectangle?**  
A: Omit the `DrawRectangle` call and pass the desired `PointF` location to `Graphics.DrawString`.

**Q: Can I rotate the text while keeping alignment?**  
A: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing, then reset it afterwards.

**Q: Is it possible to export the image as JPEG instead of PNG?**  
A: Simply change the file extension in `bitmap.Save` and optionally specify `ImageFormat.Jpeg`.

---

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [How to Draw Text with Aspose.Drawing for .NET](/drawing/net/text-and-fonts/draw-text/)
- [Adding Text on Images in Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [How to Draw Text and Fonts with Aspose.Drawing for .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}