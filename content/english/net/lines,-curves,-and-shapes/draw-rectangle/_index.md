---
title: Drawing Rectangles in Aspose.Drawing
linktitle: Drawing Rectangles in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 19
url: /net/lines,-curves,-and-shapes/draw-rectangle/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.LinesCurvesShapes
{
    class DrawRectangle
    {
        public static void Run()
        {
            //ExStart: DrawRectangle
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);

            Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
            graphics.DrawRectangle(pen, 10, 10, 900, 700);

            bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
            //ExEnd: DrawRectangle
        }
    }
}

```
