---
title: Working with Installed Fonts in Aspose.Drawing
linktitle: Working with Installed Fonts in Aspose.Drawing
second_title: Aspose.Zip .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 13
url: /net/text-and-fonts/installed-fonts/
---

## Complete Source Code
```csharp
using System.Drawing;
using System.Drawing.Text;

namespace Aspose.Drawing.Examples.CSharp.TextFonts
{
    class InstalledFonts
    {
        public static void Run()
        {
            //ExStart: InstalledFonts
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);
            graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
            graphics.Clear(Color.FromKnownColor(KnownColor.White));

            Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
            InstalledFontCollection fonts = new InstalledFontCollection();
            Font arial = new Font("Arial", 20, FontStyle.Regular);
            graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

            for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
            {
                graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
            }

            bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
            //ExEnd: InstalledFonts
        }
    }
}

```
