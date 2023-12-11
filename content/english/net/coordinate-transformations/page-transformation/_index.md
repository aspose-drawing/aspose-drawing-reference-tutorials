---
title: Page Transformation in Aspose.Drawing
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 13
url: /net/coordinate-transformations/page-transformation/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.CoordinateSystemsTransformations
{
    class PageTransformation
    {
        public static void Run()
        {
            //ExStart: PageTransformation
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);
            graphics.Clear(Color.FromKnownColor(KnownColor.Gray));

            // Set the transformation that maps page coordinates to device coordinates:
            graphics.PageUnit = GraphicsUnit.Inch;

            Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
            graphics.DrawRectangle(pen, 1, 1, 1, 1);

            bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
            //ExEnd: PageTransformation
        }
    }
}

```
