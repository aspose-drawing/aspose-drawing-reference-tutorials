---
title: Global Transformation in Aspose.Drawing
linktitle: Global Transformation in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 10
url: /net/coordinate-transformations/global-transformation/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.CoordinateSystemsTransformations
{
    class GlobalTransformation
    {
        public static void Run()
        {
            //ExStart: GlobalTransformation
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);
            graphics.Clear(Color.FromKnownColor(KnownColor.Gray));

            // Set a transformation that applies to every drawn item:
            graphics.RotateTransform(15);

            Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
            graphics.DrawEllipse(pen, 300, 300, 400, 200);

            bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\GlobalTransformation_out.png");
            //ExEnd: GlobalTransformation
        }
    }
}

```
