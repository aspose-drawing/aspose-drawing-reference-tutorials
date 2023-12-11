---
title: Drawing Polygons in Aspose.Drawing
linktitle: Drawing Polygons in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 18
url: /net/lines,-curves,-and-shapes/draw-polygon/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.LinesCurvesShapes
{
    class DrawPolygon
    {
        public static void Run()
        {
            //ExStart: DrawPolygon
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);

            Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
            graphics.DrawPolygon(pen, new Point[] { new Point(100, 100), new Point(500, 700), new Point(900, 100) });

            bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPolygon_out.png");
            //ExEnd: DrawPolygon
        }
    }
}

```
