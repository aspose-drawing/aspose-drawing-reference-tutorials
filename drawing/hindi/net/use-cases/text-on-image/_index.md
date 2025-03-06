---
title: Aspose.Drawing में छवियों पर टेक्स्ट जोड़ना
linktitle: Aspose.Drawing में छवियों पर टेक्स्ट जोड़ना
second_title: Aspose.Drawing .NET API - System.Drawing.Common का विकल्प
description: .NET के लिए Aspose.Drawing के साथ छवियों में पाठ के निर्बाध एकीकरण का अन्वेषण करें। सहज छवि हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें। अब डाउनलोड करो!
weight: 12
url: /hi/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing में छवियों पर टेक्स्ट जोड़ना

## परिचय
.NET विकास की गतिशील दुनिया में, Aspose.Drawing आसानी से छवियों में हेरफेर करने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। छवियों में टेक्स्ट जोड़ना एक सामान्य आवश्यकता है, चाहे वह वॉटरमार्किंग, एनोटेशन, या वैयक्तिकृत ग्राफिक्स बनाने के लिए हो। इस ट्यूटोरियल में, हम यह पता लगाएंगे कि C# का उपयोग करके अपनी छवियों में टेक्स्ट को सहजता से एकीकृत करने के लिए Aspose.Drawing का लाभ कैसे उठाया जाए।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित स्थान हैं:
1.  Aspose.Drawing लाइब्रेरी: Aspose.Drawing लाइब्रेरी को डाउनलोड और इंस्टॉल करें[.NET दस्तावेज़ीकरण के लिए Aspose.Drawing](https://reference.aspose.com/drawing/net/).
2. विकास वातावरण: विजुअल स्टूडियो या किसी अन्य संगत आईडीई सहित एक कार्यशील .NET विकास वातावरण रखें।
अब, आइए चरण-दर-चरण मार्गदर्शिका के साथ शुरुआत करें।
## नामस्थान आयात करें
अपने C# प्रोजेक्ट में आवश्यक नामस्थान आयात करके प्रारंभ करें:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## चरण 1: छवि लोड करें
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
यहां, हम छवि को निर्दिष्ट फ़ाइल पथ से लोड करते हैं और आगे की प्रक्रिया के लिए ग्राफिक्स ऑब्जेक्ट को प्रारंभ करते हैं।
## चरण 2: टेक्स्ट गुण सेट करें
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
रंग, फ़ॉन्ट और पैडिंग जैसे टेक्स्ट गुणों को परिभाषित करें। इन मापदंडों को अपनी प्राथमिकताओं के अनुसार समायोजित करें।
## चरण 3: टेक्स्ट का आकार मापें
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
प्रत्येक शब्द को व्यक्तिगत रूप से मापकर पाठ के लिए आवश्यक आकार की गणना करें। यह उचित प्लेसमेंट सुनिश्चित करता है और टेक्स्ट ओवरलैप से बचाता है।
## चरण 4: छवि पर टेक्स्ट बनाएं
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
अब, गणना किए गए आकार के आधार पर टेक्स्ट को छवि पर रखें और निर्दिष्ट फ़ॉन्ट और रंग का उपयोग करके इसे बनाएं।
## चरण 5: छवि सहेजें
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
संशोधित छवि को अपनी इच्छित निर्देशिका में सहेजें।
यह चरण-दर-चरण मार्गदर्शिका .NET के लिए Aspose.Drawing का उपयोग करके छवियों में टेक्स्ट जोड़ने की एक सीधी प्रक्रिया को प्रदर्शित करती है। वांछित दृश्य प्रभाव प्राप्त करने के लिए विभिन्न फ़ॉन्ट, रंग और पाठ्य सामग्री के साथ प्रयोग करें।
## निष्कर्ष
Aspose.Drawing .NET में छवि हेरफेर कार्यों को सरल बनाता है, डेवलपर्स को एक मजबूत टूलकिट प्रदान करता है। छवियों में पाठ जोड़ना इसकी क्षमताओं का सिर्फ एक उदाहरण है, जो ग्राफिकल तत्वों को संभालने में लाइब्रेरी की बहुमुखी प्रतिभा को प्रदर्शित करता है।
## अक्सर पूछे जाने वाले प्रश्नों
### क्या Aspose.Drawing सभी छवि प्रारूपों के साथ संगत है?
 Aspose.Drawing छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है, जिसमें JPEG, PNG और GIF जैसे लोकप्रिय प्रारूप शामिल हैं। को देखें[प्रलेखन](https://reference.aspose.com/drawing/net/) पूरी सूची के लिए.
### क्या मैं व्यावसायिक परियोजनाओं के लिए Aspose.Drawing का उपयोग कर सकता हूँ?
हां, Aspose.Drawing व्यक्तिगत और व्यावसायिक दोनों परियोजनाओं के लिए उपयुक्त है। लाइसेंसिंग विवरण के लिए, पर जाएँ[खरीद पृष्ठ](https://purchase.aspose.com/buy).
### क्या अस्थायी लाइसेंस परीक्षण उद्देश्यों के लिए उपलब्ध हैं?
 हां, आप यहां जाकर परीक्षण के लिए अस्थायी लाइसेंस प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/).
### मुझे Aspose.Drawing के लिए सामुदायिक समर्थन कहां मिल सकता है?
 समुदाय के साथ जुड़ें और समर्थन प्राप्त करें[Aspose.ड्राइंग फोरम](https://forum.aspose.com/c/diagram/17).
### मैं Aspose.Drawing के साथ कैसे शुरुआत करूं?
 से लाइब्रेरी डाउनलोड करके शुरुआत करें[यहाँ](https://releases.aspose.com/drawing/net/) और व्यापक का अन्वेषण करें[प्रलेखन](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
