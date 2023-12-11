---
title: Displaying Images in Aspose.Drawing
linktitle: Displaying Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 12
url: /net/image-editing/display/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.Images
{
    class Display
    {
        public static void Run()
        {
            //ExStart: Display
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);

            // Load an image:
            Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");

            // Draw the image:
            graphics.DrawImage(image, 0, 0);

            bitmap.Save("Your Document Directory" + @"Images\Display_out.png");
            //ExEnd: Display
        }
    }
}

```
