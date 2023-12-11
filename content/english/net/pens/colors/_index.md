---
title: Working with Colors in Aspose.Drawing
linktitle: Working with Colors in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 10
url: /net/pens/colors/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.Pens
{
    class Colors
    {
        public static void Run()
        {
            //ExStart: Colors
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);

            Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
            graphics.DrawLine(bluePen, 100, 100, 900, 100);

            Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
            graphics.DrawLine(redPen, 100, 200, 900, 200);

            bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
            //ExEnd: Colors
        }
    }
}

```
