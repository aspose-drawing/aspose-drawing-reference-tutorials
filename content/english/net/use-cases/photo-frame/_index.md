---
title: Creating Photo Frames in Aspose.Drawing
linktitle: Creating Photo Frames in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 11
url: /net/use-cases/photo-frame/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Drawing.Text;
using System.Drawing;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Aspose.Drawing.Examples.CSharp.UseCases
{
    internal class PhotoFrame
    {
        public static void Run()
        {
            // Create photo frame
            using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "cat.jpg")))
            {
                var graphics = Graphics.FromImage(image);

                graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
                graphics.PageUnit = GraphicsUnit.Pixel;

                var pen = new Pen(Color.Magenta, 1);

                int gap = 2;

                graphics.DrawRectangle(pen, 0, 0, image.Width - 1, image.Height - 1);
                graphics.DrawRectangle(pen, gap, gap, image.Width - gap - 1, image.Height - gap - 1);

                image.Save(Path.Combine("Your Document Directory", "UseCases", "cat_with_honor_out.jpg"));
            }
        }
    }
}

```
