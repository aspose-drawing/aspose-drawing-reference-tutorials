---
date: 2026-09-23
description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
  image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
images:
- /net/text-and-fonts/draw-text/og-image.png
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: How to Draw Text with Aspose.Drawing
og_description: Learn how to draw text on image using Aspose.Drawing for .NET. This
  tutorial shows you how to generate image with text, add text to bitmap, and save
  bitmap as PNG with custom fonts.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Draw text on image with Aspose.Drawing for .NET – Quick guide
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: How to draw text on image with Aspose.Drawing for .NET
url: /net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to draw text on image with Aspose.Drawing for .NET

## Introduction

In this step‑by‑step guide you’ll learn **how to draw text on image** using Aspose.Drawing for .NET. Whether you need to create a *dynamic text image*, add text to an existing bitmap, or generate a graphic with custom fonts, this tutorial walks you through every detail so you can start drawing text in minutes. The library supports over 30 GDI+ methods, runs on Windows, Linux, and macOS, and has **zero external dependencies**, making it a reliable choice for server‑side image generation.

## Quick answers
- **What library is used?** Aspose.Drawing for .NET  
- **Primary task?** Draw text on an image (create image with text)  
- **Key method?** `Graphics.DrawString` (draw string on image)  
- **Output format?** PNG (save bitmap as PNG)  
- **Prerequisites?** .NET development environment and Aspose.Drawing library  

## What is drawing text with Aspose.Drawing?

Draw text with Aspose.Drawing means using the library’s GDI+‑compatible API to render Unicode strings onto a raster canvas. The `Graphics.DrawString` method writes the text into a bitmap, allowing you to control font, color, alignment, and anti‑aliasing. This approach lets you generate high‑quality images without installing System.Drawing.Common.

## Why use Aspose.Drawing to add text to images?

Aspose.Drawing offers a reliable, cross‑platform way to render text on images without needing native GDI+ libraries, delivering consistent quality and performance on any operating system. It supports advanced anti‑aliasing, Unicode characters, and custom fonts, and integrates seamlessly with .NET applications, making it ideal for server‑side image generation and desktop tools alike.

- **Cross‑platform reliability** – works on Windows, Linux, and macOS.  
- **Advanced rendering** – anti‑aliasing and sub‑pixel text smoothing for crisp output.  
- **No external dependencies** – the library bundles everything you need to *create image with text*.

## Prerequisites

Before diving in, make sure you have:

- **Aspose.Drawing for .NET** – download it from the [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/).  
- **A .NET IDE** such as Visual Studio or VS Code.  

## Import namespaces

Begin by importing the required namespaces:

These namespaces provide the core GDI+ types such as `Bitmap`, `Graphics`, and text rendering utilities.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step 1: create bitmap and graphics objects

`Bitmap` is Aspose.Drawing's raster image container for pixel data, and `Graphics` supplies drawing methods to render shapes and text onto it.  

`Bitmap` represents an image in memory, while `Graphics` provides drawing methods to render onto that bitmap.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Here we create a `Bitmap` that will hold the final picture and a `Graphics` object that lets us draw on it. The anti‑aliasing hint ensures the text looks smooth.

## Step 2: set up brush, pen, and font

`Brush` defines the fill color, `Pen` outlines shapes, and `Font` specifies typeface, size, and style for rendering text.  

`Brush` fills shapes with color, `Pen` outlines shapes, and `Font` defines the typeface and size for text rendering.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** defines the text color.  
- **Pen** is used later to draw a rectangle around the text (optional).  
- **Font** specifies the typeface, size, and style for the *draw string on image* operation.

## Step 3: define text and rectangle

`Rectangle` defines the bounding box where text will be placed, specifying X/Y coordinates and width/height.  

`Rectangle` specifies the position and size of a rectangular area, used here to bound the drawn text.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

The `Rectangle` determines where the text will be placed. Adjust the coordinates and size to suit your layout.

## Step 4: draw rectangle and text

`Graphics.DrawString` renders the specified text inside the given rectangle using the provided font and brush.  

`Graphics.DrawString` renders a string of text inside a specified rectangle using the given font and brush.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

First we outline the area with a blue rectangle, then we **add text to bitmap** by calling `DrawString`. This is the core of *drawing text* on the image.

## Step 5: save the result

The image is saved as a PNG file, fulfilling the *save bitmap as PNG* requirement. Replace the placeholder path with the actual folder where you want the file stored.  

`bitmap.Save` writes the image to a file in the chosen format, such as PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Common use cases

- **Generating certificates** with personalized names.  
- **Creating watermarked thumbnails** for web galleries.  
- **Building dynamic charts** that include labels or annotations.  

## Troubleshooting & tips

- **Font not found?** Ensure the font is installed on the host machine or use a private font collection.  
- **Text clipped?** Increase the rectangle size or reduce the font size.  
- **Performance concerns?** Reuse the same `Graphics` object for multiple draw operations when possible.  

## Frequently asked questions

**Q: How do I change the output format to JPEG?**  
A: Replace the `.png` extension with `.jpg` in the `Save` method and optionally specify an `ImageCodecInfo` for JPEG quality.

**Q: Can I draw multi‑line text?**  
A: Yes, include line‑break characters (`\n`) in the string or use `StringFormat` with `FormatFlags.LineLimit`.

**Q: Is there a way to measure text size before drawing?**  
A: Use `Graphics.MeasureString` to get the exact dimensions of the rendered text.

**Q: Does Aspose.Drawing support Unicode characters?**  
A: Absolutely. Provide a font that contains the required glyphs and the library will render them correctly.

**Q: What version of Aspose.Drawing was used for testing?**  
A: The examples were tested with Aspose.Drawing 24.11 for .NET.

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Related Tutorials

- [Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts in Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [How to save a bitmap as PNG using the Aspose.Drawing API for .NET](/drawing/net/image-editing/display/)
- [Text On Image](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}