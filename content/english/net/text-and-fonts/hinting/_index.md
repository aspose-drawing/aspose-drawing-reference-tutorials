---
title: Hinting in Aspose.Drawing
linktitle: Hinting in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: 
type: docs
weight: 12
url: /net/text-and-fonts/hinting/
---

## Complete Source Code
```csharp
using System.Drawing;
using System.Drawing.Text;

namespace Aspose.Drawing.Examples.CSharp.TextFonts
{
    class Hinting
    {
        public static void Run()
        {
            //ExStart: Hinting
            Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);
            graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
            graphics.Clear(Color.FromKnownColor(KnownColor.White));

            DrawText(graphics, "Arial", 100);
            DrawText(graphics, "Times New Roman", 200);
            DrawText(graphics, "Verdana", 300);

            bitmap.Save("Your Document Directory" + @"TextFonts\Hinting_out.png");
            //ExEnd: Hinting
        }

        //ExStart: HintingDrawText
        private static void DrawText(Graphics graphics, string familyName, int y)
        {
            Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
            Font font = new Font(familyName, 10, FontStyle.Regular);
            string text = "The quick brown fox jumps over the lazy dog. 0123456789 ~!@#$%^&*()_+-={}[];':\"<>?/,.\\№`";
            graphics.DrawString(text, font, brush, 100, y);
        }
        //ExEnd: HintingDrawText
    }
}

```
