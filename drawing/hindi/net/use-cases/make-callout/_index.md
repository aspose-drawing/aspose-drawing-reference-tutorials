---
title: Aspose.Drawing में कॉलआउट बनाना
linktitle: Aspose.Drawing में कॉलआउट बनाना
second_title: Aspose.Drawing .NET API - System.Drawing.Common का विकल्प
description: .NET के लिए Aspose.Drawing का उपयोग करके अपने दस्तावेज़ चित्रण को बेहतर बनाएं! स्पष्ट और जानकारीपूर्ण दृश्यों के लिए कॉलआउट जोड़ने का चरण-दर-चरण जानें।
weight: 10
url: /hi/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing में कॉलआउट बनाना

## परिचय
.NET के लिए Aspose.Drawing में कॉलआउट बनाने पर हमारी चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है! यदि आप कॉलआउट के साथ अपने दस्तावेज़ चित्रण को बढ़ाना चाह रहे हैं, तो आप सही जगह पर हैं। इस ट्यूटोरियल में, हम Aspose.Drawing लाइब्रेरी का उपयोग करके प्रक्रिया को प्रबंधनीय चरणों में विभाजित करेंगे।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
- C# प्रोग्रामिंग भाषा का बुनियादी ज्ञान।
-  Aspose.Drawing लाइब्रेरी स्थापित की गई। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/drawing/net/).
- एक दस्तावेज़ या छवि जहाँ आप कॉलआउट जोड़ना चाहते हैं।
## नामस्थान आयात करें
सुनिश्चित करें कि आपके प्रोजेक्ट में आवश्यक नामस्थान शामिल हैं:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## चरण 1: छवि लोड करें
 उस छवि को लोड करके प्रारंभ करें जहां आप कॉलआउट जोड़ना चाहते हैं। प्रतिस्थापित करें`"Your Document Directory"` और`"gears.png"` आपकी वास्तविक निर्देशिका और छवि फ़ाइल नाम के साथ।
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // आपका कोड यहाँ
}
```
## चरण 2: ग्राफ़िक्स ऑब्जेक्ट बनाएं
 एक बनाने के`Graphics` ड्राइंग संचालन करने के लिए छवि से ऑब्जेक्ट।
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## चरण 3: कॉलआउट स्थिति परिभाषित करें
कॉलआउट मान और इकाई के साथ प्रत्येक कॉलआउट के लिए प्रारंभ और समाप्ति बिंदु परिभाषित करें।
```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```
## चरण 4: कॉलआउट बनाएं
 लागू करें`DrawCallOut` छवि पर कॉलआउट बनाने की विधि।
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## चरण 5: छवि सहेजें
छवि को कॉलआउट के साथ अपनी इच्छित निर्देशिका में सहेजें।
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## कॉलआउट स्रोत कोड बनाएं
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```
## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.Drawing का उपयोग करके अपनी छवि में सफलतापूर्वक कॉलआउट जोड़ लिया है। अपने कॉलआउट को और अधिक अनुकूलित करने के लिए विभिन्न स्थितियों और मूल्यों के साथ बेझिझक प्रयोग करें।

## पूछे जाने वाले प्रश्न

### क्या मैं अन्य प्रकार के चित्रों के लिए Aspose.Drawing का उपयोग कर सकता हूँ?

हां, Aspose.Drawing विभिन्न प्रकार के चित्रों के लिए ड्राइंग संचालन की एक विस्तृत श्रृंखला का समर्थन करता है।

### क्या Aspose.Drawing विभिन्न छवि प्रारूपों के साथ संगत है?

बिल्कुल! Aspose.Drawing पीएनजी, जेपीईजी, जीआईएफ और अन्य जैसे लोकप्रिय छवि प्रारूपों का समर्थन करता है।

### मुझे और अधिक उदाहरण और दस्तावेज़ कहां मिल सकते हैं?

 व्यापक दस्तावेज़ीकरण का अन्वेषण करें[यहाँ](https://reference.aspose.com/drawing/net/).

### यदि मुझे कोई समस्या आती है तो मुझे सहायता कैसे मिलेगी?

 दौरा करना[Aspose.ड्राइंग फोरम](https://forum.aspose.com/c/drawing/44) सामुदायिक समर्थन के लिए.

### क्या मैं खरीदने से पहले Aspose.Drawing आज़मा सकता हूँ?

 निश्चित रूप से! निःशुल्क परीक्षण के साथ आरंभ करें[यहाँ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
