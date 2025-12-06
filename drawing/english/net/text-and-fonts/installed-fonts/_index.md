---
title: "Save PNG Image and Work with Installed Fonts in Aspose.Drawing"
linktitle: "Save PNG Image and Work with Installed Fonts in Aspose.Drawing"
second_title: "Aspose.Drawing .NET API - Alternative to System.Drawing.Common"
description: "Learn how to save PNG image files while listing installed fonts, showing font families, creating graphics from bitmap, and drawing text with fonts using Aspose.Drawing for .NET."
weight: 13
url: /net/text-and-fonts/installed-fonts/
date: 2025-12-06
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save PNG Image and Work with Installed Fonts in Aspose.Drawing

## Introduction

If you need to **save PNG image** files that also display information about the fonts installed on a machine, Aspose.Drawing for .NET gives you a clean, cross‑platform way to do it. In this tutorial we’ll walk through listing installed fonts, showing font families, creating graphics from a bitmap, and drawing text with fonts—all while finally saving the result as a PNG image. By the end you’ll have a reusable snippet you can drop into any .NET project.

## Quick Answers
- **What does this tutorial create?** A PNG image that lists installed font families.  
- **Which library is required?** Aspose.Drawing for .NET (no System.Drawing.Common needed).  
- **Can I use custom fonts?** Yes – just load them into an `InstalledFontCollection`.  
- **Is the output resolution adjustable?** Absolutely – change the bitmap size or pixel format.  
- **Do I need a license to run the code?** A temporary license works for evaluation; a full license is required for production.

## What is “save PNG image” in the context of Aspose.Drawing?
Saving a PNG image means rendering your drawing surface (a `Bitmap`) to a file with the `.png` extension. Aspose.Drawing handles the encoding for you, so you only need to call `bitmap.Save(...)` with the desired path.

## Why list installed fonts and show font families?
Knowing which fonts are available lets you create dynamic graphics that adapt to the end‑user’s environment. It’s especially handy for generating reports, certificates, or any visual content that must match corporate branding without shipping font files.

## Prerequisites

- **Aspose.Drawing Library** – download the latest version from the [Aspose Drawing download page](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider, or any .NET‑compatible editor.  
- **Basic C# knowledge** – you should be comfortable with classes, objects, and simple loops.

## Import Namespaces
To work with fonts and graphics, import these namespaces at the top of your C# file:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step‑by‑Step Guide

### Step 1: Create a bitmap (the canvas)
First, we create a bitmap that will hold the final image. The bitmap size and pixel format determine the quality of the saved PNG.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Step 2: Create graphics from bitmap
Next, we obtain a `Graphics` object from the bitmap. This object lets us draw shapes, text, and images onto the canvas.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Step 3: Set up brush and font (draw text with fonts)
We need a brush for the text colour and a `Font` object that defines the typeface, size, and style.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Step 4: List installed fonts and show font families
Now we display the number of font families and the first few names directly on the bitmap. This demonstrates the **list installed fonts** and **show font families** capabilities.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Step 5: Save PNG image
Finally, we write the bitmap to disk as a PNG file. This is the core **save png image** operation.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tip:** Use `Path.Combine` for building file paths to avoid issues with directory separators on different operating systems.

## Common Issues and Solutions
| Issue | Cause | Fix |
|-------|-------|-----|
| **No fonts displayed** | `InstalledFontCollection` not populated (e.g., running on a headless server without fonts). | Install the required fonts on the server or embed custom fonts in your application. |
| **Saved file is corrupted** | Incorrect pixel format or missing write permissions. | Ensure the target folder exists and the app has write access; keep `Format32bppPArgb`. |
| **Text looks blurry** | Low DPI settings. | Increase bitmap dimensions or set `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Frequently Asked Questions

**Q: Can I use custom fonts that are not installed on the machine?**  
A: Yes. Load the font file into a `PrivateFontCollection` and create a `Font` from that collection.

**Q: How do I handle font‑related exceptions?**  
A: Wrap font creation in a `try/catch` block and inspect `ArgumentException` for missing families.

**Q: Is Aspose.Drawing suitable for web applications?**  
A: Absolutely. The library works in ASP.NET Core, Azure Functions, and other server‑side environments.

**Q: Can I change the text colour or style?**  
A: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify the `FontStyle` enum.

**Q: Where can I get a temporary license for testing?**  
A: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).

## Conclusion

By following these steps you’ve learned how to **save PNG image** files that dynamically **list installed fonts**, **show font families**, **create graphics from bitmap**, and **draw text with fonts** using Aspose.Drawing for .NET. Feel free to experiment with other fonts, colors, and bitmap sizes to match your project’s visual requirements.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose