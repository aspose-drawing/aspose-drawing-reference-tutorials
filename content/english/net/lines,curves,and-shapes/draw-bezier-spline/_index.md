---
title: Drawing Bezier Splines in Aspose.Drawing
linktitle: Drawing Bezier Splines in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 12
url: /net/lines,curves,and-shapes/draw-bezier-spline/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.LinesCurvesShapes
{
    class DrawBezierSpline
    {
        public static void Run()
        {
            //ExStart: DrawBezierSpline
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);

            Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
            PointF p1 = new PointF(0, 0);   // start point
            PointF c1 = new PointF(0, 800);   // first control point
            PointF c2 = new PointF(1000, 0);  // second control point
            PointF p2 = new PointF(1000, 800);  // end point
            graphics.DrawBezier(pen, p1, c1, c2, p2);

            bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawBezierSpline_out.png");
            //ExEnd: DrawBezierSpline
        }
    }
}

```
