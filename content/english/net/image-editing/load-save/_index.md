---
title: Loading and Saving Images in Aspose.Drawing
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 13
url: /net/image-editing/load-save/
---

## Complete Source Code
```csharp
using System.Drawing;

namespace Aspose.Drawing.Examples.CSharp.GraphicsFileFormats
{
    class LoadSave
    {
        public static void Run()
        {
            LoadAndSave("bmp");
            LoadAndSave("gif");
            LoadAndSave("jpg");
            LoadAndSave("png");
            LoadAndSave("tiff");
        }

        private static void LoadAndSave(string graphicsFileFormats)
        {
            new Bitmap("Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats).Save("Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats);
        }
    }
}

```
