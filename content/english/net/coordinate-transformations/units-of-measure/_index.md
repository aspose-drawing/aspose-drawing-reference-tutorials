---
title: Units of Measure in Aspose.Drawing
linktitle: Units of Measure in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 14
url: /net/coordinate-transformations/units-of-measure/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.CoordinateSystemsTransformations
{
    class UnitsOfMeasure
    {
        public static void Run()
        {
            //ExStart: UnitsOfMeasure
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);
            graphics.Clear(Color.FromKnownColor(KnownColor.Gray));

            // 1 point is 1/72 inch.
            graphics.PageUnit = GraphicsUnit.Point;
            graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);

            // 1 mm is 1/25.4 inch.
            graphics.PageUnit = GraphicsUnit.Millimeter;
            graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);

            graphics.PageUnit = GraphicsUnit.Inch;
            graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);

            bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
            //ExEnd: UnitsOfMeasure
        }
    }
}

```
