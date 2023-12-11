---
title: Drawing Closed Curves in Aspose.Drawing
linktitle: Drawing Closed Curves in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 14
url: /net/lines,curves,and-shapes/draw-closed-curve/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.LinesCurvesShapes
{
    class DrawClosedCurve
    {
        public static void Run()
        {
            //ExStart: DrawClosedCurve
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);

            Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
            graphics.DrawClosedCurve(pen, new Point[] { new Point(100, 700), new Point(350, 600), new Point(500, 500), new Point(650, 600), new Point(900, 700) });

            bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawClosedCurve_out.png");
            //ExEnd: DrawClosedCurve
        }
    }
}

```
