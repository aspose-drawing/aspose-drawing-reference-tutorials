---
title: World Transformation in Aspose.Drawing
linktitle: World Transformation in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 15
url: /net/coordinate-transformations/world-transformation/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.CoordinateSystemsTransformations
{
    class WorldTransformation
    {
        public static void Run()
        {
            //ExStart: WorldTransformation
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);
            graphics.Clear(Color.FromKnownColor(KnownColor.Gray));

            // Set the transformation that maps world coordinates to page coordinates:
            graphics.TranslateTransform(500, 400);

            Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
            graphics.DrawRectangle(pen, 0, 0, 300, 200);

            bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
            //ExEnd: WorldTransformation
        }
    }
}

```
