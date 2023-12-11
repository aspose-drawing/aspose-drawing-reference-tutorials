---
title: Direct Data Access in Aspose.Drawing
linktitle: Direct Data Access in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 11
url: /net/image-editing/direct-data-access/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.Images
{
    class DirectDataAccess
    {
        public static void Run()
        {
            //ExStart: DirectDataAccess
            Bitmap sourceBitmap = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
            Bitmap targetBitmap = new Bitmap(sourceBitmap.Width, sourceBitmap.Height, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);

            // Directly copy pixel data from the source to the target bitmap:
            int[] pixels = new int[sourceBitmap.Width * sourceBitmap.Height];
            sourceBitmap.ReadArgb32Pixels(pixels);
            targetBitmap.WriteArgb32Pixels(pixels);

            targetBitmap.Save("Your Document Directory" + @"Images\DirectDataAccess_out.png");
            //ExEnd: DirectDataAccess
        }
    }
}

```
