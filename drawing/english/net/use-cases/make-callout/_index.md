---
title: Making Callouts in Aspose.Drawing
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Enhance your document illustrations using Aspose.Drawing for .NET! Learn step-by-step how to add callouts for clearer and informative visuals.
weight: 10
url: /net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Making Callouts in Aspose.Drawing

## Introduction
Welcome to our step-by-step guide on making callouts in Aspose.Drawing for .NET! If you're looking to enhance your document illustrations with callouts, you're in the right place. In this tutorial, we'll break down the process into manageable steps using the Aspose.Drawing library.
## Prerequisites
Before diving into the tutorial, make sure you have the following prerequisites:
- Basic knowledge of C# programming language.
- Aspose.Drawing library installed. You can download it [here](https://releases.aspose.com/drawing/net/).
- A document or image where you want to add callouts.
## Import Namespaces
Ensure you have the necessary namespaces included in your project:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Step 1: Load the Image
Start by loading the image where you want to add callouts. Replace `"Your Document Directory"` and `"gears.png"` with your actual directory and image filename.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```
## Step 2: Create Graphics Object
Create a `Graphics` object from the image to perform drawing operations.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Step 3: Define Callout Positions
Define the start and end points for each callout along with the callout value and unit.
```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```
## Step 4: Draw Callouts
Implement the `DrawCallOut` method to draw callouts on the image.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Step 5: Save the Image
Save the image with callouts to your desired directory.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Draw Callout Source Code
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```
## Conclusion

Congratulations! You've successfully added callouts to your image using Aspose.Drawing for .NET. Feel free to experiment with different positions and values to customize your callouts further.

## FAQs

### Can I use Aspose.Drawing for other types of illustrations?

Yes, Aspose.Drawing supports a wide range of drawing operations for various types of illustrations.

### Is Aspose.Drawing compatible with different image formats?

Absolutely! Aspose.Drawing supports popular image formats like PNG, JPEG, GIF, and more.

### Where can I find more examples and documentation?

Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).

### How do I get support if I encounter issues?

Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/diagram/17) for community support.

### Can I try Aspose.Drawing before purchasing?

Certainly! Get started with a free trial [here](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
