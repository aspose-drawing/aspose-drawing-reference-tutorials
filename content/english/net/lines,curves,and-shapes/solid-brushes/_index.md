---
title: Solid Brushes in Aspose.Drawing
linktitle: Solid Brushes in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 10
url: /net/lines,curves,and-shapes/solid-brushes/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.Brushes
{
    class Solid
    {
        public static void Run()
        {
            //ExStart: Solid
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);

            Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
            graphics.FillEllipse(brush, 100, 100, 800, 600);

            bitmap.Save("Your Document Directory" + @"Brushes\Solid_out.png");
            //ExEnd: Solid
        }
    }
}

```
