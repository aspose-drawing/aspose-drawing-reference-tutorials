---
date: 2026-09-23
description: Aspose.Drawing का उपयोग करके C# में PNG इमेज सहेजना, स्थापित फ़ॉन्ट्स
  की सूची बनाना, कस्टम फ़ॉन्ट्स के साथ टेक्स्ट ड्रॉ करना, और हाई‑क्वालिटी ग्राफिक्स
  के लिए bitmap resolution को समायोजित करना सीखें।
keywords:
- save png image c#
- installed fonts aspnet
- aspose.drawing bitmap graphics
- c# font collection
- png export .net
lastmod: 2026-09-23
linktitle: Aspose.Drawing और स्थापित फ़ॉन्ट्स के साथ C# में PNG इमेज सहेजें
og_description: Aspose.Drawing का उपयोग करके C# में PNG इमेज सहेजें। यह गाइड स्थापित
  फ़ॉन्ट्स की सूची, टेक्स्ट ड्रॉ करना, और प्रोफ़ेशनल ग्राफिक्स के लिए bitmap resolution
  को नियंत्रित करना दिखाता है।
og_image_alt: Developer guide showing C# code that creates a bitmap, lists system
  fonts, and saves a PNG file with Aspose.Drawing
og_title: Aspose.Drawing और स्थापित फ़ॉन्ट्स के साथ C# में PNG इमेज सहेजें
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  headline: Save PNG image in C# with Aspose.Drawing and installed fonts
  type: TechArticle
- description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  name: Save PNG image in C# with Aspose.Drawing and installed fonts
  steps:
  - name: Create a bitmap (the canvas)
    text: '`Bitmap` is the raster image object that holds pixel data for the canvas.'
  - name: Create graphics from bitmap
    text: '`Graphics` is the object that supplies drawing functions such as drawing
      shapes and text onto a bitmap.'
  - name: Set up brush and font (draw text with fonts)
    text: '`Brush` defines how shapes and text are filled with colour, while `Font`
      specifies the typeface, size, and style for text rendering.'
  - name: List installed fonts and show font families
    text: '`InstalledFontCollection` provides access to all font families installed
      on the host system.'
  - name: Save PNG image
    text: '`bitmap.Save` writes the bitmap to a file in the chosen image format, such
      as PNG. > **Pro tip:** Use `Path.Combine` for building file paths to avoid issues
      with directory separators on different operating systems.'
  type: HowTo
- questions:
  - answer: Yes. Load the font file into a `PrivateFontCollection` and create a `Font`
      from that collection, then draw it the same way as system fonts.
    question: Can I use custom fonts that are not installed on the machine?
  - answer: Wrap font creation in a `try/catch` block and inspect `ArgumentException`
      for missing families; provide a fallback font such as `Arial`.
    question: How do I handle font‑related exceptions?
  - answer: Absolutely. The library works in ASP.NET Core, Azure Functions, and other
      server‑side .NET environments without needing GDI+.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify
      the `FontStyle` enum to apply bold, italic, or underline.
    question: Can I change the text colour or style?
  - answer: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – bitmap graphics and font handling
tags:
- save png
- aspose.drawing
- c# graphics
- installed fonts
- bitmap
title: Aspose.Drawing और स्थापित फ़ॉन्ट्स के साथ C# में PNG इमेज सहेजें
url: /hi/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# में Aspose.Drawing और स्थापित फ़ॉन्ट्स के साथ PNG छवि सहेजें

## परिचय

यदि आपको **C# में PNG छवि सहेजनी** है और साथ ही **बिटमैप ग्राफ़िक्स बनाना** है, तो Aspose.Drawing for .NET आपको एक साफ़, क्रॉस‑प्लेटफ़ॉर्म तरीका प्रदान करता है। इस ट्यूटोरियल में हम स्थापित फ़ॉन्ट्स की सूची, फ़ॉन्ट फ़ैमिली दिखाने, बिटमैप से ग्राफ़िक्स बनाने, और फ़ॉन्ट्स के साथ टेक्स्ट ड्रॉ करने की प्रक्रिया को चरण‑दर‑चरण देखेंगे—और अंत में परिणाम को PNG छवि के रूप में सहेजेंगे। अंत तक आपके पास एक पुन: उपयोग योग्य स्निपेट होगा जिसे आप किसी भी .NET प्रोजेक्ट में डाल सकते हैं, चाहे वह Windows, Linux, या macOS पर चले।

## त्वरित उत्तर
- **इस ट्यूटोरियल का परिणाम क्या है?** होस्ट मशीन पर स्थापित फ़ॉन्ट फ़ैमिली की सूची वाली PNG छवि।  
- **कौनसी लाइब्रेरी आवश्यक है?** Aspose.Drawing for .NET (कोई System.Drawing.Common निर्भरता नहीं)।  
- **क्या मैं कस्टम फ़ॉन्ट्स उपयोग कर सकता हूँ?** हाँ – उन्हें `InstalledFontCollection` या `PrivateFontCollection` में लोड करें।  
- **क्या आउटपुट रेज़ोल्यूशन समायोज्य है?** बिल्कुल – रेज़ोल्यूशन नियंत्रित करने के लिए बिटमैप आकार या पिक्सेल फ़ॉर्मेट बदलें।  
- **क्या कोड चलाने के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।

## Aspose.Drawing के संदर्भ में “PNG छवि सहेजें” क्या है?

`Bitmap` Aspose.Drawing का रास्टर इमेज कंटेनर है जो पिक्सेल डेटा संग्रहीत करता है।  

PNG छवि सहेजना का अर्थ है आपके ड्रॉइंग सतह—एक `Bitmap`—को `.png` एक्सटेंशन वाली फ़ाइल में रेंडर करना। Aspose.Drawing लॉसलेस PNG संपीड़न करता है और **10 000 × 10 000 पिक्सेल** तक की छवियों को मेमोरी समाप्त किए बिना संभाल सकता है, जिससे यह हाई‑रेज़ोल्यूशन ग्राफ़िक्स के लिए उपयुक्त बनता है। परिणामी फ़ाइल को वेब पेज, रिपोर्ट, या आगे की इमेज‑प्रोसेसिंग पाइपलाइन में उपयोग किया जा सकता है।

## स्थापित फ़ॉन्ट्स की सूची बनाना और फ़ॉन्ट फ़ैमिली दिखाना क्यों आवश्यक है?

स्थापित फ़ॉन्ट्स की सूची बनाकर आपका एप्लिकेशन अंतिम‑उपयोगकर्ता के वातावरण के अनुसार अनुकूल हो सकता है, यह सुनिश्चित करता है कि उत्पन्न ग्राफ़िक्स कॉर्पोरेट ब्रांडिंग या उपयोगकर्ता प्राथमिकताओं से मेल खाते हों बिना अतिरिक्त फ़ॉन्ट फ़ाइलें शिप किए। `InstalledFontCollection` ऑपरेटिंग सिस्टम पर स्थापित फ़ॉन्ट्स को एन्हांस करता है। यह स्वचालित रिपोर्ट जेनरेशन, प्रमाणपत्र, या किसी भी दृश्य सामग्री के लिए विशेष रूप से उपयोगी है जिसे सिस्टम की टाइपोग्राफी का सम्मान करना आवश्यक है।

## Aspose.Drawing के साथ C# में बिटमैप ग्राफ़िक्स कैसे बनाएं?

`Bitmap` एक इमेज कैनवास को दर्शाता है; `Graphics` उस कैनवास के लिए ड्रॉइंग मेथड्स प्रदान करता है; `Font` टेक्स्ट रेंडरिंग के लिए टाइपफ़ेस का विवरण देता है। आप कुछ ही लाइनों में पूर्ण PNG बना सकते हैं: एक `Bitmap` बनाएं, एक `Graphics` ऑब्जेक्ट प्राप्त करें, स्थापित संग्रह से `Font` का उपयोग करके टेक्स्ट ड्रॉ करें, और अंत में `bitmap.Save` कॉल करें। नीचे दिया गया चरण‑दर‑चरण गाइड प्रत्येक भाग को विस्तारित करता है और व्यावहारिक टिप्स जोड़ता है।

## पूर्वापेक्षाएँ

- **Aspose.Drawing लाइब्रेरी** – नवीनतम संस्करण [Aspose Drawing download page](https://releases.aspose.com/drawing/net/) से डाउनलोड करें।  
- **IDE** – Visual Studio, Rider, या कोई भी .NET‑संगत एडिटर।  
- **बेसिक C# ज्ञान** – आपको क्लासेज़, ऑब्जेक्ट्स, और साधारण लूप्स में सहज होना चाहिए।  
- **.NET रनटाइम** – पूर्ण क्रॉस‑प्लेटफ़ॉर्म समर्थन के लिए .NET 6+ या .NET Core 3.1+ की सिफारिश की जाती है।

## नेमस्पेस इम्पोर्ट करें

Add the following `using` statements at the top of your C# file so the compiler can locate the graphics and font types:

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Text;
using System.IO;
```

## चरण‑दर‑चरण गाइड

### चरण 1: बिटमैप बनाएं (कैनवास)

`Bitmap` वह रास्टर इमेज ऑब्जेक्ट है जो कैनवास के लिए पिक्सेल डेटा रखता है।  

```csharp
using System.Drawing;
using System.Drawing.Text;
```

### चरण 2: बिटमैप से ग्राफ़िक्स बनाएं

`Graphics` वह ऑब्जेक्ट है जो बिटमैप पर आकार और टेक्स्ट जैसी ड्रॉइंग फ़ंक्शन प्रदान करता है।  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### चरण 3: ब्रश और फ़ॉन्ट सेट करें (फ़ॉन्ट्स के साथ टेक्स्ट ड्रॉ करें)

`Brush` यह निर्धारित करता है कि आकार और टेक्स्ट को किस रंग से भरा जाए, जबकि `Font` टेक्स्ट रेंडरिंग के लिए टाइपफ़ेस, आकार, और शैली निर्दिष्ट करता है।  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### चरण 4: स्थापित फ़ॉन्ट्स की सूची बनाएं और फ़ॉन्ट फ़ैमिली दिखाएं

`InstalledFontCollection` होस्ट सिस्टम पर स्थापित सभी फ़ॉन्ट फ़ैमिली तक पहुंच प्रदान करता है।  

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### चरण 5: PNG छवि सहेजें

`bitmap.Save` चयनित इमेज फ़ॉर्मेट (जैसे PNG) में बिटमैट को फ़ाइल में लिखता है।  

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

> **प्रो टिप:** विभिन्न ऑपरेटिंग सिस्टम पर डायरेक्टरी सेपरेटर समस्याओं से बचने के लिए फ़ाइल पाथ बनाने में `Path.Combine` का उपयोग करें।

## सामान्य समस्याएँ और समाधान
| समस्या | कारण | समाधान |
|-------|-------|-----|
| **फ़ॉन्ट्स नहीं दिख रहे हैं** | `InstalledFontCollection` नहीं भरा गया (उदाहरण के लिए, बिना फ़ॉन्ट्स के हेडलेस सर्वर पर चल रहा है)। | सर्वर पर आवश्यक फ़ॉन्ट्स इंस्टॉल करें या अपने एप्लिकेशन में कस्टम फ़ॉन्ट्स एम्बेड करें। |
| **सहेजी गई फ़ाइल भ्रष्ट है** | गलत पिक्सेल फ़ॉर्मेट या लिखने की अनुमति नहीं है। | सुनिश्चित करें कि लक्ष्य फ़ोल्डर मौजूद है और एप्लिकेशन को लिखने की अनुमति है; `PixelFormat.Format32bppPArgb` रखें। |
| **टेक्स्ट धुंधला दिख रहा है** | कम DPI सेटिंग या छोटा बिटमैप आकार। | बिटमैप आकार बढ़ाएँ या `graphics.SmoothingMode = SmoothingMode.AntiAlias` सेट करें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं मशीन पर इंस्टॉल नहीं किए गए कस्टम फ़ॉन्ट्स उपयोग कर सकता हूँ?**  
**उत्तर:** हाँ। फ़ॉन्ट फ़ाइल को `PrivateFontCollection` में लोड करें और उस संग्रह से `Font` बनाएं, फिर इसे सिस्टम फ़ॉन्ट्स की तरह ड्रॉ करें।

**प्रश्न: फ़ॉन्ट‑संबंधी अपवादों को कैसे संभालूँ?**  
**उत्तर:** फ़ॉन्ट निर्माण को `try/catch` ब्लॉक में रखें और गायब फ़ॉन्ट फ़ैमिली के लिए `ArgumentException` जांचें; फ़ॉलबैक फ़ॉन्ट जैसे `Arial` प्रदान करें।

**प्रश्न: क्या Aspose.Drawing वेब एप्लिकेशन्स के लिए उपयुक्त है?**  
**उत्तर:** बिल्कुल। लाइब्रेरी ASP.NET Core, Azure Functions, और अन्य सर्वर‑साइड .NET वातावरण में बिना GDI+ की आवश्यकता के काम करती है।

**प्रश्न: क्या मैं टेक्स्ट का रंग या शैली बदल सकता हूँ?**  
**उत्तर:** हाँ। विभिन्न `Brush` प्रकार (जैसे `LinearGradientBrush`) का उपयोग करें और `FontStyle` एन्नम को बदलकर बोल्ड, इटैलिक, या अंडरलाइन लागू करें।

**प्रश्न: परीक्षण के लिए अस्थायी लाइसेंस कहाँ प्राप्त कर सकता हूँ?**  
**उत्तर:** [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/) से ट्रायल लाइसेंस डाउनलोड करें।

## निष्कर्ष

इन चरणों का पालन करके आपने **C# में PNG छवि सहेजना** सीखा, जो गतिशील रूप से **स्थापित फ़ॉन्ट्स की सूची**, **फ़ॉन्ट फ़ैमिली दिखाना**, **बिटमैप से ग्राफ़िक्स बनाना**, और **फ़ॉन्ट्स के साथ टेक्स्ट ड्रॉ करना** Aspose.Drawing for .NET का उपयोग करके करता है। अब आप **C# में बिटमैप ग्राफ़िक्स बनाना**, बिटमैप रेज़ोल्यूशन समायोजित करना, और आवश्यकतानुसार कस्टम फ़ॉन्ट्स को शामिल करना जानते हैं। विभिन्न रंगों, फ़ॉन्ट आकारों, और बिटमैप आयामों के साथ प्रयोग करें ताकि आपके प्रोजेक्ट की दृश्य आवश्यकताओं को पूरा किया जा सके, और अधिक समृद्ध ग्राफ़िक्स के लिए shape drawing और image manipulation जैसी अन्य Aspose.Drawing सुविधाओं का अन्वेषण करें।

---

**अंतिम अपडेट:** 2026-09-23  
**परीक्षित संस्करण:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

## संबंधित ट्यूटोरियल

- [Aspose.Drawing for .NET के साथ टेक्स्ट कैसे ड्रॉ करें](/drawing/net/text-and-fonts/draw-text/)
- [Aspose.Drawing में एंटीएलियासिंग के साथ इमेज क्वालिटी सुधारें](/drawing/net/rendering/antialiasing/)
- [Aspose.Drawing के साथ PNG कैसे सहेजें – वर्ल्ड ट्रांसफ़ॉर्मेशन](/drawing/net/coordinate-transformations/world-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}