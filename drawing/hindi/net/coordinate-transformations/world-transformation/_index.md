---
date: 2026-06-23
description: Aspose.Drawing का उपयोग करके PNG कैसे सहेजें, वर्ल्ड ट्रांसफ़ॉर्मेशन
  लागू करें, और ग्राफ़िक्स को PNG में बदलें, यह सीखें। इसमें translate transform C#
  उदाहरण और कई ग्राफ़िक्स ट्रांसफ़ॉर्मेशन शामिल हैं।
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: Aspose.Drawing में वर्ल्ड ट्रांसफ़ॉर्मेशन
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing के साथ PNG कैसे सहेजें – वर्ल्ड ट्रांसफ़ॉर्मेशन
url: /hi/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG को Aspose.Drawing के साथ कैसे सहेजें – विश्व रूपांतरण

## PNG के रूप में बिटमैप सहेजें – परिचय

**How to save PNG** using Aspose.Drawing एक सामान्य आवश्यकता है जब आपको उच्च‑गुणवत्ता, पारदर्शी छवियों को तुरंत उत्पन्न करने की जरूरत होती है। इस ट्यूटोरियल में आप सीखेंगे कि **save bitmap as PNG** कैसे किया जाता है, translate, rotate, और scale जैसे विश्व रूपांतरण लागू करें, और अंत में ग्राफ़िक्स को PNG में बदलें—सभी साफ़, रखरखाव योग्य C# कोड के साथ। चाहे आप रिपोर्टिंग इंजन, चार्टिंग कंपोनेंट, या कस्टम UI रेंडरर बना रहे हों, इन चरणों में महारत हासिल करने से आप गतिशील छवियाँ बना सकते हैं जो किसी भी डिवाइस पर शानदार दिखें।

## त्वरित उत्तर
- **What does “world transformation” mean?** यह आपके ड्रॉइंग के तार्किक (world) निर्देशांक को पेज (डिवाइस) निर्देशांक में मैप करता है।  
- **Can I export the result as PNG?** हाँ – ड्रॉइंग के बाद आप बस `bitmap.Save(...)` को `.png` एक्सटेंशन के साथ कॉल करें।  
- **Do I need a license for Aspose.Drawing?** विकास के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक वाणिज्यिक लाइसेंस आवश्यक है।  
- **Is this compatible with .NET 6/7?** बिल्कुल – Aspose.Drawing .NET Framework 4.5+ और .NET Core/5/6/7 को सपोर्ट करता है।  
- **How many transformations can I chain?** आप क्रम में **multiple graphics transformations** लागू कर सकते हैं (translate, rotate, scale, आदि)।

## Aspose.Drawing में विश्व रूपांतरण क्या है?
एक विश्व रूपांतरण आपके ड्रॉइंग कमांड्स द्वारा उपयोग किए जाने वाले निर्देशांक प्रणाली को बदलता है। डिफ़ॉल्ट रूप से, (0,0) बिटमैप के ऊपर‑बाएँ कोने पर होता है। `TranslateTransform`, `RotateTransform`, या `ScaleTransform` के साथ, आप उस मूल बिंदु को पुनःस्थापित कर सकते हैं, आकारों को घुमा सकते हैं, या उन्हें मूल ज्यामिति को बदले बिना आकार बदल सकते हैं।

## Aspose.Drawing का उपयोग करके PNG कैसे सहेजें?
एक `Bitmap` ऑब्जेक्ट लोड करें, उसके `Graphics` इंस्टेंस पर इच्छित विश्व रूपांतरण सेट करें, अपने आकार बनाएं, और अंत में `bitmap.Save("output.png", ImageFormat.Png)` कॉल करें। यह एक‑लाइन सहेजने का कॉल एक लॉसलेस PNG फ़ाइल लिखता है जो पारदर्शिता और रंग की सटीकता को बनाए रखता है, जिससे यह वेब एसेट्स और UI ओवरलेज़ के लिए आदर्श बनता है।

## ग्राफ़िक्स ट्रांसलेट उदाहरण का उपयोग क्यों करें?
एक ग्राफ़िक्स ट्रांसलेट उदाहरण आपको ड्रॉइंग मूल बिंदु को एक बार स्थानांतरित करने देता है, बजाय हर बिंदु को पुनः गणना करने के। यह तरीका कोड की जटिलता को कम करता है, पठनीयता बढ़ाता है, और ग्राफ़िक्स इंजन को मैट्रिक्स गणना कुशलता से संभालने देता है, जिससे बड़े कैनवास पर रेंडरिंग प्रदर्शन में 30 % तक वृद्धि हो सकती है।

## ग्राफ़िक्स ट्रांसलेट उदाहरण
एक **graphics translate example** दर्शाता है कि मूल बिंदु को स्थानांतरित करने से पोजिशनिंग कैसे सरल हो जाती है। हर बिंदु को पुनः गणना करने के बजाय, आप एक बार निर्देशांक प्रणाली को शिफ्ट करते हैं और ऐसे ड्रॉ करते हैं जैसे नया मूल बिंदु कैनवास के केंद्र में हो।

## पूर्वापेक्षाएँ
Before we begin, ensure you have:

- **Aspose.Drawing library** को अपने .NET प्रोजेक्ट में एकीकृत करें – इसे आधिकारिक [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/) से डाउनलोड करें।  
- एक **document directory** जहाँ आउटपुट इमेज सहेजी जाएगी।  
- **C#** सिंटैक्स और Visual Studio या अपने पसंदीदा IDE की बुनियादी जानकारी।  

अब, चलिए कोड में डुबकी लगाते हैं!

## नेमस्पेस इम्पोर्ट करें
`Bitmap`, `Graphics`, और Aspose ड्रॉइंग यूटिलिटीज़ इन नेमस्पेस में स्थित हैं।  
**Definition:** `System.Drawing` कोर GDI+ टाइप्स प्रदान करता है, जबकि `Aspose.Drawing` उन्हें क्रॉस‑प्लेटफ़ॉर्म क्षमताओं के साथ विस्तारित करता है।

## चरण‑दर‑चरण मार्गदर्शिका

### चरण 1: एक Bitmap बनाएं
हम एक खाली कैनवास बनाकर शुरू करते हैं जो हमारे ड्रॉइंग को रखेगा।

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` 32‑बिट प्रति पिक्सेल बिटमैप बनाता है जिसमें प्री‑मल्टिप्लाइड अल्फा होता है, जो PNG आउटपुट के लिए इष्टतम फॉर्मेट है क्योंकि यह अतिरिक्त रूपांतरण चरणों के बिना पारदर्शिता को बनाए रखता है।

- **Why 32bppPArgb?** यह पिक्सेल फॉर्मेट अल्फा पारदर्शिता और उच्च‑गुणवत्ता रंग रेंडरिंग को सपोर्ट करता है, PNG आउटपुट के लिए बिल्कुल उपयुक्त है।  
- **Pro tip:** लक्ष्य इमेज आकार से मेल खाने के लिए चौड़ाई/ऊँचाई समायोजित करें।

### चरण 2: विश्व रूपांतरण सेट करें (Graphics Translate Example)
`TranslateTransform` निर्देशांक प्रणाली की मूल बिंदु को नई जगह पर ले जाता है।  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` (0,0) बिंदु को कैनवास के केंद्र पर शिफ्ट करता है। इस कॉल के बाद, आप जो भी आकार (0,0) निर्देशांक से ड्रॉ करेंगे वह इमेज के मध्य में दिखाई देगा।

- यह (0,0) बिंदु को (500, 400) पर ले जाता है – 1000 × 800 कैनवास का मध्य।  
- आप अतिरिक्त रूपांतरण जोड़ सकते हैं: `RotateTransform` निर्देशांक प्रणाली को घुमाता है, और `ScaleTransform` इसे स्केल करता है, जिससे **multiple graphics transformations** सक्षम होते हैं।

### चरण 3: परिवर्तित निर्देशांक का उपयोग करके आयत ड्रॉ करें
`DrawRectangle` निर्दिष्ट पेन और निर्देशांक का उपयोग करके एक आयत ड्रॉ करता है।

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` कैनवास के केंद्र में आयत ड्रॉ करता है क्योंकि इसका ऊपर‑बायाँ कोना परिवर्तित मूल बिंदु से उसकी चौड़ाई और ऊँचाई के आधे भाग से ऑफ़सेट है।

- आयत का ऊपर‑बायाँ कोना परिवर्तित मूल बिंदु (इमेज के केंद्र) से शुरू होता है।  
- अन्य आकारों—एलिप्स, लाइन्स, या कस्टम पाथ्स—के साथ प्रयोग करने में संकोच न करें।

### चरण 4: परिणाम सहेजें – ग्राफ़िक्स को PNG में बदलें
`Save` बिटमैप को निर्दिष्ट इमेज फॉर्मेट में फ़ाइल में लिखता है।  
`ImageFormat` इमेज को सहेजने के लिए फ़ाइल फॉर्मेट निर्दिष्ट करता है, जैसे PNG।

`bitmap.Save(outputPath, ImageFormat.Png)` एक लॉसलेस PNG फ़ाइल लिखता है जिसे सीधे वेब पेज या UI कंपोनेंट्स में उपयोग किया जा सकता है।

- PNG पहले सेट किए गए सटीक रंग और पारदर्शिता को बनाए रखता है।  
- `"Your Document Directory"` को अपने मशीन पर वास्तविक पाथ से बदलें।

## सामान्य समस्याएँ और समाधान
| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **File not found error** when saving | लक्ष्य फ़ोल्डर मौजूद नहीं है। | `Save` कॉल करने से पहले प्रोग्रामेटिक रूप से फ़ोल्डर बनाएं (`Directory.CreateDirectory`)। |
| **Blank image** after transformation | `TranslateTransform` ड्रॉइंग के बाद कॉल किया गया। | सुनिश्चित करें कि रूपांतरण **ड्रॉइंग कमांड्स** से पहले सेट किया गया है। |
| **Distorted colors** | असंगत पिक्सेल फॉर्मेट का उपयोग। | PNG आउटपुट के लिए `Format32bppPArgb` ही उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न
**Q: Can I apply more than one transformation?**  
A: हाँ – आप `TranslateTransform`, `RotateTransform`, और `ScaleTransform` को चेन करके एक ही ग्राफ़िक्स पाइपलाइन में जटिल प्रभाव प्राप्त कर सकते हैं।

**Q: Is Aspose.Drawing free for commercial projects?**  
A: मूल्यांकन के लिए एक मुफ्त ट्रायल उपलब्ध है, लेकिन उत्पादन उपयोग के लिए वाणिज्यिक लाइसेंस आवश्यक है।

**Q: Does this work with .NET Core and .NET 5/6/7?**  
A: बिल्कुल। Aspose.Drawing सभी आधुनिक .NET रनटाइम्स को सपोर्ट करता है, जिसमें .NET Core, .NET 5, .NET 6, और .NET 7 शामिल हैं।

**Q: Where can I find the full API reference?**  
A: पूरी दस्तावेज़ीकरण [here](https://reference.aspose.com/drawing/net/) पर उपलब्ध है।

**Q: How do I troubleshoot a missing output file?**  
A: पाथ स्ट्रिंग की जाँच करें, लिखने की अनुमति सुनिश्चित करें, और `Save` कॉल करने से पहले यह पुष्टि करें कि डायरेक्टरी मौजूद है।

## निष्कर्ष
आपने अब **how to save PNG** को Aspose.Drawing के साथ सीख लिया है, एक **world transformation** लागू किया है, और एक **graphics translate example** किया है जिसे घुमा‍व या स्केल के साथ विस्तारित किया जा सकता है। इन बिल्डिंग ब्लॉक्स में महारत हासिल करके आप गतिशील छवियां बना सकते हैं, कस्टम चार्ट बना सकते हैं, या किसी भी .NET एप्लिकेशन के लिए ऑन‑द‑फ्लाई ग्राफ़िक्स बना सकते हैं।

---

**अंतिम अपडेट:** 2026-06-23  
**परीक्षित संस्करण:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose  
**संबंधित संसाधन:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## संबंधित ट्यूटोरियल

- [मैट्रिक्स रूपांतरण ट्यूटोरियल: Aspose.Drawing के लिए .NET में मैट्रिक्स रूपांतरण](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Aspose.Drawing ग्लोबल ट्रांसफ़ॉर्मेशन के साथ इमेज कैसे घुमाएँ](/drawing/net/coordinate-transformations/global-transformation/)
- [कोऑर्डिनेट सिस्टम ट्रांसफ़ॉर्मेशन – Aspose.Drawing के लिए .NET में पेज ट्रांसफ़ॉर्मेशन](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}