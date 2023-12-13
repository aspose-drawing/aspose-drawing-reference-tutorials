---
title: Adding Text on Images in Aspose.Drawing
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Explore the seamless integration of text into images with Aspose.Drawing for .NET. Follow our step-by-step guide for effortless image manipulation. Download now!
type: docs
weight: 12
url: /net/use-cases/text-on-image/
---
## Introduction
In the dynamic world of .NET development, Aspose.Drawing stands out as a powerful tool for manipulating images with ease. Adding text to images is a common requirement, whether it's for watermarking, annotations, or creating personalized graphics. In this tutorial, we will explore how to leverage Aspose.Drawing to seamlessly integrate text into your images using C#.
## Prerequisites
Before diving into the tutorial, ensure you have the following in place:
1. Aspose.Drawing Library: Download and install the Aspose.Drawing library from the [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/).
2. Development Environment: Have a working .NET development environment, including Visual Studio or any other compatible IDE.
Now, let's get started with the step-by-step guide.
## Import Namespaces
Begin by importing the necessary namespaces into your C# project:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## Step 1: Load the Image
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Here, we load the image from the specified file path and initialize the graphics object for further processing.
## Step 2: Set Text Properties
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Define the text properties such as color, font, and padding. Adjust these parameters according to your preferences.
## Step 3: Measure Text Size
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Calculate the required size for the text by measuring each word individually. This ensures proper placement and avoids text overlap.
## Step 4: Draw Text on Image
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Now, position the text on the image based on the calculated size and draw it using the specified font and color.
## Step 5: Save the Image
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Save the modified image to your desired directory.
This step-by-step guide demonstrates a straightforward process of adding text to images using Aspose.Drawing for .NET. Experiment with different fonts, colors, and text content to achieve the desired visual effect.
## Conclusion
Aspose.Drawing simplifies image manipulation tasks in .NET, providing developers with a robust toolkit. Adding text to images is just one example of its capabilities, showcasing the library's versatility in handling graphical elements.
### Frequently Asked Questions
### Is Aspose.Drawing compatible with all image formats?
Aspose.Drawing supports a wide range of image formats, including popular ones like JPEG, PNG, and GIF. Refer to the [documentation](https://reference.aspose.com/drawing/net/) for a complete list.
### Can I use Aspose.Drawing for commercial projects?
Yes, Aspose.Drawing is suitable for both personal and commercial projects. For licensing details, visit the [purchase page](https://purchase.aspose.com/buy).
### Are temporary licenses available for testing purposes?
Yes, you can obtain a temporary license for testing by visiting [Temporary License](https://purchase.aspose.com/temporary-license/).
### Where can I find community support for Aspose.Drawing?
Engage with the community and get support on the [Aspose.Drawing forum](https://forum.aspose.com/c/diagram/17).
### How do I get started with Aspose.Drawing?
Begin by downloading the library from [here](https://releases.aspose.com/drawing/net/) and explore the comprehensive [documentation](https://reference.aspose.com/drawing/net/).
#