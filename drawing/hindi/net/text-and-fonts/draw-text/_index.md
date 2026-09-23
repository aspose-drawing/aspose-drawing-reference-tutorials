---
date: 2026-09-23
description: Aspose.Drawing for .NET का उपयोग करके छवि पर टेक्स्ट कैसे ड्रॉ किया जाए,
  सीखें। टेक्स्ट के साथ छवि बनाएं, टेक्स्ट को bitmap में जोड़ें, और bitmap को कस्टम
  fonts के साथ PNG के रूप में सहेजें।
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Aspose.Drawing के साथ टेक्स्ट कैसे ड्रॉ करें
og_description: Aspose.Drawing for .NET का उपयोग करके छवि पर टेक्स्ट कैसे ड्रॉ किया
  जाए, जानें। यह ट्यूटोरियल दिखाता है कि टेक्स्ट के साथ छवि कैसे बनाएं, टेक्स्ट को
  bitmap में कैसे जोड़ें, और bitmap को कस्टम fonts के साथ PNG के रूप में कैसे सहेजें।
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Aspose.Drawing for .NET के साथ छवि पर टेक्स्ट ड्रॉ करें – Quick guide
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Aspose.Drawing for .NET के साथ छवि पर टेक्स्ट कैसे ड्रॉ करें
url: /hi/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET के साथ छवि पर टेक्स्ट कैसे ड्रॉ करें

## परिचय

इस चरण‑दर‑चरण गाइड में आप Aspose.Drawing for .NET का उपयोग करके **छवि पर टेक्स्ट कैसे ड्रॉ करें** सीखेंगे। चाहे आपको *डायनामिक टेक्स्ट इमेज* बनाना हो, मौजूदा बिटमैप में टेक्स्ट जोड़ना हो, या कस्टम फ़ॉन्ट्स के साथ ग्राफ़िक जनरेट करना हो, यह ट्यूटोरियल हर विवरण के साथ आपका मार्गदर्शन करता है ताकि आप मिनटों में टेक्स्ट ड्रॉ करना शुरू कर सकें। लाइब्रेरी 30 से अधिक GDI+ मेथड्स का समर्थन करती है, Windows, Linux, और macOS पर चलती है, और **शून्य बाहरी निर्भरताएँ** रखती है, जिससे यह सर्वर‑साइड इमेज जेनरेशन के लिए एक विश्वसनीय विकल्प बनती है।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी उपयोग की गई है?** Aspose.Drawing for .NET  
- **मुख्य कार्य?** छवि पर टेक्स्ट ड्रॉ करें (टेक्स्ट के साथ इमेज बनाएं)  
- **मुख्य मेथड?** `Graphics.DrawString` (इमेज पर स्ट्रिंग ड्रॉ करें)  
- **आउटपुट फ़ॉर्मेट?** PNG (बिटमैप को PNG के रूप में सहेजें)  
- **पूर्वापेक्षाएँ?** .NET विकास पर्यावरण और Aspose.Drawing लाइब्रेरी  

## Aspose.Drawing के साथ टेक्स्ट ड्रॉ करना क्या है?

Aspose.Drawing के साथ टेक्स्ट ड्रॉ करना का मतलब है लाइब्रेरी के GDI+‑संगत API का उपयोग करके यूनिकोड स्ट्रिंग्स को रास्टर कैनवास पर रेंडर करना। `Graphics.DrawString` मेथड टेक्स्ट को बिटमैप में लिखता है, जिससे आप फ़ॉन्ट, रंग, संरेखण और एंटी‑एलियासिंग को नियंत्रित कर सकते हैं। यह तरीका System.Drawing.Common इंस्टॉल किए बिना उच्च‑गुणवत्ता वाली छवियां जनरेट करने की सुविधा देता है।

## छवियों में टेक्स्ट जोड़ने के लिए Aspose.Drawing क्यों उपयोग करें?

Aspose.Drawing एक विश्वसनीय, क्रॉस‑प्लेटफ़ॉर्म तरीका प्रदान करता है जिससे आप मूल GDI+ लाइब्रेरीज़ की आवश्यकता के बिना छवियों पर टेक्स्ट रेंडर कर सकते हैं, और किसी भी ऑपरेटिंग सिस्टम पर निरंतर गुणवत्ता और प्रदर्शन प्रदान करता है। यह उन्नत एंटी‑एलियासिंग, यूनिकोड कैरेक्टर्स, और कस्टम फ़ॉन्ट्स का समर्थन करता है, और .NET एप्लिकेशन के साथ सहजता से एकीकृत होता है, जिससे यह सर्वर‑साइड इमेज जेनरेशन और डेस्कटॉप टूल्स दोनों के लिए आदर्श बनता है।

- **क्रॉस‑प्लेटफ़ॉर्म विश्वसनीयता** – Windows, Linux, और macOS पर काम करता है।  
- **उन्नत रेंडरिंग** – स्पष्ट आउटपुट के लिए एंटी‑एलियासिंग और सब‑पिक्सेल टेक्स्ट स्मूदिंग।  
- **कोई बाहरी निर्भरताएँ नहीं** – लाइब्रेरी वह सब कुछ बंडल करती है जो आपको *टेक्स्ट के साथ इमेज बनाने* के लिए चाहिए।

## आवश्यकताएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

- **Aspose.Drawing for .NET** – इसे [Aspose.Drawing दस्तावेज़ीकरण](https://reference.aspose.com/drawing/net/) से डाउनलोड करें।  
- **एक .NET IDE** जैसे Visual Studio या VS Code।  

## नेमस्पेस इम्पोर्ट करें

आवश्यक नेमस्पेस इम्पोर्ट करके शुरू करें:

ये नेमस्पेस कोर GDI+ टाइप्स जैसे `Bitmap`, `Graphics`, और टेक्स्ट रेंडरिंग यूटिलिटीज़ प्रदान करते हैं।  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## चरण 1: बिटमैप और ग्राफ़िक्स ऑब्जेक्ट बनाएं

`Bitmap` Aspose.Drawing का रास्टर इमेज कंटेनर है जो पिक्सेल डेटा रखता है, और `Graphics` ड्रॉइंग मेथड्स प्रदान करता है जिससे आप आकार और टेक्स्ट उस पर रेंडर कर सकते हैं।  

`Bitmap` मेमोरी में एक इमेज का प्रतिनिधित्व करता है, जबकि `Graphics` ड्रॉइंग मेथड्स प्रदान करता है जिससे आप उस बिटमैप पर रेंडर कर सकते हैं।  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

यहां हम एक `Bitmap` बनाते हैं जो अंतिम चित्र रखेगा और एक `Graphics` ऑब्जेक्ट जो हमें उस पर ड्रॉ करने की अनुमति देता है। एंटी‑एलियासिंग संकेत सुनिश्चित करता है कि टेक्स्ट स्मूद दिखे।

## चरण 2: ब्रश, पेन और फ़ॉन्ट सेट करें

`Brush` भरने का रंग निर्धारित करता है, `Pen` आकारों की रूपरेखा बनाता है, और `Font` टेक्स्ट रेंडरिंग के लिए टाइपफ़ेस, आकार, और शैली निर्दिष्ट करता है।  

`Brush` आकारों को रंग से भरता है, `Pen` आकारों की रूपरेखा बनाता है, और `Font` टेक्स्ट रेंडरिंग के लिए टाइपफ़ेस और आकार निर्धारित करता है।  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** टेक्स्ट का रंग निर्धारित करता है।  
- **Pen** बाद में टेक्स्ट के चारों ओर आयत ड्रॉ करने के लिए उपयोग किया जाता है (वैकल्पिक)।  
- **Font** *draw string on image* ऑपरेशन के लिए टाइपफ़ेस, आकार, और शैली निर्दिष्ट करता है।

## चरण 3: टेक्स्ट और आयत निर्धारित करें

`Rectangle` वह बाउंडिंग बॉक्स निर्धारित करता है जहाँ टेक्स्ट रखा जाएगा, X/Y निर्देशांक और चौड़ाई/ऊँचाई निर्दिष्ट करता है।  

`Rectangle` एक आयताकार क्षेत्र की स्थिति और आकार निर्दिष्ट करता है, जिसका उपयोग यहाँ ड्रॉ किए गए टेक्स्ट को सीमित करने के लिए किया गया है।  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` निर्धारित करता है कि टेक्स्ट कहाँ रखा जाएगा। अपने लेआउट के अनुसार निर्देशांक और आकार समायोजित करें।

## चरण 4: आयत और टेक्स्ट ड्रॉ करें

`Graphics.DrawString` प्रदान किए गए फ़ॉन्ट और ब्रश का उपयोग करके निर्दिष्ट आयत के भीतर टेक्स्ट रेंडर करता है।  

`Graphics.DrawString` दिए गए फ़ॉन्ट और ब्रश का उपयोग करके निर्दिष्ट आयत के भीतर टेक्स्ट की स्ट्रिंग रेंडर करता है।  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

पहले हम क्षेत्र को एक नीली आयत से रूपरेखा देते हैं, फिर `DrawString` को कॉल करके **बिटमैप में टेक्स्ट जोड़ते** हैं। यह छवि पर *टेक्स्ट ड्रॉ करने* का मुख्य भाग है।

## चरण 5: परिणाम सहेजें

छवि को PNG फ़ाइल के रूप में सहेजा जाता है, जिससे *save bitmap as PNG* आवश्यकता पूरी होती है। प्लेसहोल्डर पाथ को उस वास्तविक फ़ोल्डर से बदलें जहाँ आप फ़ाइल संग्रहीत करना चाहते हैं।  

`bitmap.Save` चुने हुए फ़ॉर्मेट (जैसे PNG) में इमेज को फ़ाइल में लिखता है।  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## सामान्य उपयोग के मामले

- **व्यक्तिगत नामों के साथ प्रमाणपत्र जनरेट करना**।  
- **वेब गैलरी के लिए वाटरमार्केड थंबनेल बनाना**।  
- **लेबल या एनोटेशन सहित डायनामिक चार्ट बनाना**।  

## समस्या निवारण और टिप्स

- **फ़ॉन्ट नहीं मिला?** सुनिश्चित करें कि फ़ॉन्ट होस्ट मशीन पर इंस्टॉल है या प्राइवेट फ़ॉन्ट कलेक्शन उपयोग करें।  
- **टेक्स्ट कट गया?** आयत का आकार बढ़ाएँ या फ़ॉन्ट आकार घटाएँ।  
- **परफ़ॉर्मेंस संबंधी चिंताएँ?** संभव हो तो कई ड्रॉ ऑपरेशन्स के लिए वही `Graphics` ऑब्जेक्ट पुनः उपयोग करें।  

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: आउटपुट फ़ॉर्मेट को JPEG में कैसे बदलें?**  
उत्तर: `Save` मेथड में `.png` एक्सटेंशन को `.jpg` से बदलें और वैकल्पिक रूप से JPEG गुणवत्ता के लिए `ImageCodecInfo` निर्दिष्ट करें।

**प्रश्न: क्या मैं मल्टी‑लाइन टेक्स्ट ड्रॉ कर सकता हूँ?**  
उत्तर: हाँ, स्ट्रिंग में लाइन‑ब्रेक कैरेक्टर्स (`\n`) शामिल करें या `StringFormat` के साथ `FormatFlags.LineLimit` का उपयोग करें।

**प्रश्न: ड्रॉ करने से पहले टेक्स्ट का आकार मापने का कोई तरीका है?**  
उत्तर: रेंडर किए गए टेक्स्ट के सटीक आयाम प्राप्त करने के लिए `Graphics.MeasureString` का उपयोग करें।

**प्रश्न: क्या Aspose.Drawing यूनिकोड कैरेक्टर्स को सपोर्ट करता है?**  
उत्तर: बिल्कुल। आवश्यक ग्लिफ़्स वाले फ़ॉन्ट को प्रदान करें और लाइब्रेरी उन्हें सही ढंग से रेंडर करेगी।

**प्रश्न: परीक्षण के लिए कौन सा Aspose.Drawing संस्करण उपयोग किया गया?**  
उत्तर: उदाहरणों का परीक्षण Aspose.Drawing 24.11 for .NET के साथ किया गया था।

---

**अंतिम अपडेट:** 2026-09-23  
**परीक्षण किया गया:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [बिटमैप ग्राफ़िक्स C# बनाएं – PNG इमेज सहेजें और Aspose.Drawing में इंस्टॉल्ड फ़ॉन्ट्स के साथ काम करें](/drawing/net/text-and-fonts/installed-fonts/)
- [Aspose.Drawing API for .NET का उपयोग करके बिटमैप को PNG के रूप में कैसे सहेजें](/drawing/net/image-editing/display/)
- [छवि पर टेक्स्ट](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}