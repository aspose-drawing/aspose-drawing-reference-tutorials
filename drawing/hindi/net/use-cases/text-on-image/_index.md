---
date: 2026-09-03
description: Aspose.Drawing for .NET का उपयोग करके छवियों पर टेक्स्ट ओवरले बनाना सीखें।
  यह चरण-दर-चरण गाइड आपको दिखाता है कि छवि में टेक्स्ट कैसे जोड़ें, छवि पर टेक्स्ट
  कैसे ड्रॉ करें, और स्ट्रिंग का आकार प्रभावी ढंग से कैसे मापें।
keywords:
- create text overlay
- add text to image
- draw text on image
- measure string size
- calculate text dimensions
lastmod: 2026-09-03
linktitle: Aspose.Drawing में छवियों पर टेक्स्ट जोड़ना
og_description: Aspose.Drawing for .NET का उपयोग करके छवियों पर टेक्स्ट ओवरले बनाना
  सीखें। यह गाइड छवि में टेक्स्ट जोड़ना, छवि पर टेक्स्ट ड्रॉ करना, और कुछ आसान चरणों
  में स्ट्रिंग का आकार मापना शामिल करता है।
og_image_alt: Tutorial showing how to create text overlay on images using Aspose.Drawing
  in .NET
og_title: Aspose.Drawing के साथ छवियों पर टेक्स्ट ओवरले कैसे बनाएं
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create text overlay on images using Aspose.Drawing for
    .NET. This step‑by‑step guide shows you how to add text to image, draw text on
    image, and measure string size efficiently.
  headline: How to create text overlay on images with Aspose.Drawing
  type: TechArticle
- description: Learn how to create text overlay on images using Aspose.Drawing for
    .NET. This step‑by‑step guide shows you how to add text to image, draw text on
    image, and measure string size efficiently.
  name: How to create text overlay on images with Aspose.Drawing
  steps:
  - name: import namespaces
    text: 'Begin by importing the necessary namespaces into your C# project:'
  - name: load the image
    text: Here, we load the image from the specified file path and initialize the
      graphics object for further processing.
  - name: set text properties
    text: Define the text properties such as color, font, and padding. Adjust these
      parameters according to your preferences.
  - name: measure text size
    text: Calculate the required size for the text by measuring each word individually.
      This ensures proper placement and avoids text overlap.
  - name: draw text on image
    text: Now, position the text on the image based on the calculated size and draw
      it using the specified font and color.
  - name: save the image
    text: Save the modified image to your desired directory. This step‑by‑step guide
      demonstrates a straightforward process of adding text to images using Aspose.Drawing
      for .NET. Experiment with different fonts, colors, and text content to achieve
      the desired visual effect.
  type: HowTo
- questions:
  - answer: Measure the string width with `Graphics.MeasureString`, subtract it from
      the image width, divide by two, and use that X coordinate when calling `DrawString`.
    question: How do I center text horizontally on the image?
  - answer: Yes—use `StringFormat` with `FormatFlags.LineLimit` and pass a string
      containing `\n` to `DrawString`.
    question: Can I add multi‑line text with line breaks?
  - answer: Absolutely. Set the brush color using `Color.FromArgb(alpha, r, g, b)`
      where `alpha` controls opacity.
    question: Does Aspose.Drawing support transparent text?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- image processing
- Aspose.Drawing
- .NET graphics
title: Aspose.Drawing के साथ छवियों पर टेक्स्ट ओवरले कैसे बनाएं
url: /hi/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing के साथ छवियों पर टेक्स्ट ओवरले कैसे बनाएं

## परिचय
Aspose.Drawing एक .NET API है जो System.Drawing.Common पर निर्भर हुए बिना उन्नत इमेज‑प्रोसेसिंग क्षमताएँ प्रदान करता है। .NET विकास की गतिशील दुनिया में, छवियों पर टेक्स्ट ओवरले बनाना एक सामान्य आवश्यकता है—चाहे आप फ़ोटो पर वॉटरमार्क लगा रहे हों, कैप्शन जोड़ रहे हों, या कस्टम ग्राफ़िक्स बना रहे हों। यह ट्यूटोरियल आपको C# और Aspose.Drawing का उपयोग करके छवियों पर टेक्स्ट जोड़ने की पूरी प्रक्रिया से परिचित कराता है, ताकि आप मिनटों में समाधान लागू कर सकें।

## त्वरित उत्तर
- **ड्रॉइंग के लिए प्राथमिक क्लास क्या है?** Aspose.Drawing का `Graphics` सभी ड्रॉइंग ऑपरेशन्स को संभालता है।  
- **क्या विकास के लिए मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **कौन से इमेज फॉर्मेट्स समर्थित हैं?** 30 से अधिक फॉर्मेट्स, जिसमें JPEG, PNG, BMP, और GIF शामिल हैं।  
- **क्या मैं ड्रॉ करने से पहले टेक्स्ट आकार माप सकता हूँ?** हाँ—सटीक आयामों की गणना के लिए `Graphics.MeasureString` का उपयोग करें।  
- **क्या API .NET 6 के साथ संगत है?** बिल्कुल, Aspose.Drawing .NET Framework 4.5+ और .NET 5/6+ को लक्षित करता है।

## टेक्स्ट ओवरले बनाना क्या है?
टेक्स्ट ओवरले बनाना मौजूदा बिटमैप इमेज के ऊपर टेक्स्ट सामग्री को रेंडर करने की प्रक्रिया को दर्शाता है, जिससे एक एकल संयुक्त दृश्य संपत्ति बनती है जिसे सहेजा या प्रदर्शित किया जा सकता है। व्यवहार में, टेक्स्ट पिक्सेल डेटा का हिस्सा बन जाता है, जिससे परिणामी इमेज को जहाँ भी मानक इमेज स्वीकार किए जाते हैं, जैसे वेब पेज, रिपोर्ट, या प्रिंटेड सामग्री, उपयोग किया जा सकता है। ओवरले में स्टाइलिंग, पोजिशनिंग, और ट्रांसपेरेंसी शामिल हो सकती है ताकि वांछित दृश्य प्रभाव प्राप्त हो सके।

## इस कार्य के लिए Aspose.Drawing का उपयोग क्यों करें?
Aspose.Drawing 30 से अधिक इमेज फॉर्मेट्स को सपोर्ट करता है और पूरी इमेज को मेमोरी में लोड किए बिना 500 MB से बड़ी फाइलों को प्रोसेस कर सकता है, जिससे बड़े बैचों पर System.Drawing की तुलना में रेंडरिंग 2× तक तेज़ हो जाती है। इसका API पूरी तरह से मैनेज्ड है, जिससे नेटिव‑कोड निर्भरताएँ समाप्त होती हैं और Windows, Linux, और macOS पर डिप्लॉयमेंट सरल हो जाता है।

## पूर्वापेक्षाएँ
1. **Aspose.Drawing लाइब्रेरी** – [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/) से डाउनलोड और इंस्टॉल करें।  
2. **डेवलपमेंट एनवायरनमेंट** – Visual Studio 2022, Rider, या कोई भी IDE जो .NET 6+ को सपोर्ट करता हो।  
3. **एक सैंपल इमेज** – कोई भी JPEG/PNG फ़ाइल जिसे आप एनोटेट करना चाहते हैं।

अब, आइए कार्यान्वयन को चरण-दर-चरण देखें।

## एक छवि पर टेक्स्ट ओवरले कैसे बनाएं?
आप स्रोत बिटमैप को `Graphics` ऑब्जेक्ट में लोड करके शुरू करेंगे, फिर फ़ॉन्ट, ब्रश, और पैडिंग को परिभाषित करेंगे। टेक्स्ट आयामों को मापने के बाद क्लिपिंग से बचने के लिए, आप आयत को स्थित करेंगे और स्ट्रिंग को रेंडर करेंगे। अंत में, आप संशोधित इमेज को डिस्क पर सहेजेंगे। नीचे दिया गया संक्षिप्त विवरण उन सभी चरणों की पूरी श्रृंखला दिखाता है जिन्हें आप विस्तृत चरणों में पालन करेंगे।

### चरण 1: नेमस्पेस आयात करें
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

### चरण 2: छवि लोड करें
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Here, we load the image from the specified file path and initialize the graphics object for further processing.

### चरण 3: टेक्स्ट गुण सेट करें
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Define the text properties such as color, font, and padding. Adjust these parameters according to your preferences.

### चरण 4: टेक्स्ट आकार मापें
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
Calculate the required size for the text by measuring each word individually. This ensures proper placement and avoids text overlap.

### चरण 5: छवि पर टेक्स्ट ड्रॉ करें
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Now, position the text on the image based on the calculated size and draw it using the specified font and color.

### चरण 6: छवि सहेजें
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Save the modified image to your desired directory.

This step‑by‑step guide demonstrates a straightforward process of adding text to images using Aspose.Drawing for .NET. Experiment with different fonts, colors, and text content to achieve the desired visual effect.

## सामान्य समस्याएँ और समाधान
- **टेक्स्ट धुंधला दिखता है** – सुनिश्चित करें कि इमेज रेज़ोल्यूशन (DPI) फ़ॉन्ट साइज से मेल खाता हो; `Graphics.SmoothingMode = SmoothingMode.AntiAlias` का उपयोग करें।  
- **अप्रत्याशित क्लिपिंग** – जांचें कि मापी गई स्ट्रिंग की चौड़ाई इमेज की सीमा से अधिक न हो; आवश्यकतानुसार पैडिंग जोड़ें या फ़ॉन्ट साइज घटाएँ।  
- **लाइसेंस नहीं मिला** – लाइसेंस फ़ाइल को एक्सीक्यूटेबल डायरेक्टरी में रखें या प्रोग्रामेटिकली `new License().SetLicense("Aspose.Drawing.lic")` के साथ सेट करें।

## अक्सर पूछे जाने वाले प्रश्न
### क्या Aspose.Drawing सभी इमेज फॉर्मेट्स के साथ संगत है?
Aspose.Drawing इमेज फॉर्मेट्स की एक विस्तृत श्रृंखला को सपोर्ट करता है, जिसमें JPEG, PNG, और GIF जैसे लोकप्रिय फॉर्मेट्स शामिल हैं। पूरी सूची के लिए [documentation](https://reference.aspose.com/drawing/net/) देखें।

### क्या मैं Aspose.Drawing को वाणिज्यिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?
हाँ, Aspose.Drawing व्यक्तिगत और वाणिज्यिक दोनों प्रोजेक्ट्स के लिए उपयुक्त है। लाइसेंसिंग विवरण के लिए [purchase page](https://purchase.aspose.com/buy) देखें।

### क्या परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस उपलब्ध हैं?
हाँ, आप परीक्षण के लिए अस्थायी लाइसेंस प्राप्त कर सकते हैं, इसके लिए [Temporary License](https://purchase.aspose.com/temporary-license/) पर जाएँ।

### मैं Aspose.Drawing के लिए समुदाय समर्थन कहाँ पा सकता हूँ?
समुदाय के साथ जुड़ें और समर्थन प्राप्त करें [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) पर।

### मैं Aspose.Drawing के साथ कैसे शुरू करूँ?
लाइब्रेरी को [Aspose.Drawing download page](https://releases.aspose.com/drawing/net/) से डाउनलोड करके शुरू करें और व्यापक [documentation](https://reference.aspose.com/drawing/net/) देखें।

**अतिरिक्त प्रश्न और उत्तर**

**प्र: मैं छवि पर टेक्स्ट को क्षैतिज रूप से कैसे केंद्रित करूँ?**  
**उ: `Graphics.MeasureString` से स्ट्रिंग की चौड़ाई मापें, इसे इमेज की चौड़ाई से घटाएँ, दो से भाग दें, और `DrawString` कॉल करते समय उस X निर्देशांक का उपयोग करें।**

**प्र: क्या मैं लाइन ब्रेक के साथ मल्टी‑लाइन टेक्स्ट जोड़ सकता हूँ?**  
**उ: हाँ—`StringFormat` को `FormatFlags.LineLimit` के साथ उपयोग करें और `DrawString` को `\n` वाला स्ट्रिंग पास करें।**

**प्र: क्या Aspose.Drawing पारदर्शी टेक्स्ट को सपोर्ट करता है?**  
**उ: बिल्कुल। ब्रश का रंग `Color.FromArgb(alpha, r, g, b)` से सेट करें जहाँ `alpha` अपारदर्शिता को नियंत्रित करता है।**

## निष्कर्ष
Aspose.Drawing .NET में इमेज मैनिपुलेशन कार्यों को सरल बनाता है, एक मजबूत टूलकिट प्रदान करता है जो **30 से अधिक इमेज फॉर्मेट्स** को प्रोसेस कर सकता है और **500 MB से बड़ी फाइलों** को पूरी मेमोरी लोड किए बिना संभाल सकता है। टेक्स्ट ओवरले जोड़ना इसकी बहुमुखी प्रतिभा का एक उदाहरण है, जिससे आप कुशलता से वॉटरमार्क, कैप्शन, और कस्टम ग्राफ़िक्स बना सकते हैं।

---

**अंतिम अपडेट:** 2026-09-03  
**परीक्षण किया गया:** Aspose.Drawing 24.12 for .NET  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल्स

- [Aspose.Drawing for .NET के साथ टेक्स्ट और फ़ॉन्ट कैसे ड्रॉ करें](/drawing/net/text-and-fonts/)
- [Aspose.Drawing for .NET के साथ टेक्स्ट कैसे ड्रॉ करें](/drawing/net/text-and-fonts/draw-text/)
- [Aspose.Drawing API for .NET का उपयोग करके आयत ड्रॉ करें – कोऑर्डिनेट सिस्टम ट्रांसफ़ॉर्मेशन (पेज ट्रांसफ़ॉर्मेशन)](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}