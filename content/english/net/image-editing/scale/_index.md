---
title: Scaling Images in Aspose.Drawing
linktitle: Scaling Images in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 14
url: /net/image-editing/scale/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.Images
{
    class Scale
    {
        public static void Run()
        {
            //ExStart: Scale
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);
            graphics.InterpolationMode = System.Drawing.Drawing2D.InterpolationMode.NearestNeighbor;

            Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");

            // Scale the image 5x:
            Rectangle expansionRectangle = new Rectangle(0, 0, image.Width * 5, image.Height * 5);
            graphics.DrawImage(image, expansionRectangle);

            bitmap.Save("Your Document Directory" + @"Images\Scale_out.png");
            //ExEnd: Scale
        }
    }
}

```
