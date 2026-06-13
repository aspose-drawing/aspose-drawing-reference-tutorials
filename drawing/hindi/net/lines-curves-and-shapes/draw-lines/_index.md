---
date: 2026-06-13
description: Aspose.Drawing का उपयोग करके .NET अनुप्रयोगों में बिटमैप को PNG के रूप
  में सहेजना और कई लाइनों को ड्रॉ करना सीखें। यह चरण-दर-चरण गाइड .NET लाइन ड्रॉइंग,
  लाइन ड्रॉ बिटमैप तकनीकों, और सर्वोत्तम प्रथाओं को कवर करता है।
keywords:
- save bitmap as png
- draw multiple lines
- how to draw lines
linktitle: Aspose.Drawing के साथ कई लाइनों को ड्रॉ करें
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  headline: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  name: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  steps:
  - name: Create a Bitmap (draw line bitmap)
    text: The `Bitmap` class represents an in‑memory raster image that you can draw
      onto. Start by creating a new bitmap with the desired width and height. This
      will be the canvas on which you draw your lines.
  - name: Get Graphics Object
    text: The `Graphics` object provides drawing methods such as lines, shapes, and
      text for a bitmap. Obtain a `Graphics` object from the created bitmap. This
      object provides methods for drawing on the bitmap.
  - name: Define a Pen
    text: A `Pen` defines the color, width, and style of lines drawn by the `Graphics`
      object. Create a `Pen` object that defines the attributes of the line you want
      to draw. In this case, we've chosen a blue color with a thickness of 2 pixels.
  - name: Draw Lines
    text: Use the `DrawLine` method to draw lines on the bitmap. The coordinates `(x1,
      y1)` to `(x2, y2)` represent the starting and ending points of each line. By
      calling the method twice, we effectively **draw multiple lines** that form a
      simple “V” shape.
  - name: Save the Image
    text: The `Bitmap.Save` method writes the in‑memory image to a file in the format
      you specify—PNG being the most common loss‑less option. Specify the directory
      where you want to save the output image. Make sure to replace `"Your Document
      Directory"` with the actual path.
  type: HowTo
- questions:
  - answer: Yes, simply modify the `Color` parameter when creating the `Pen` object.
    question: Can I change the color of the lines?
  - answer: Aspose.Drawing supports rectangles, ellipses, curves, polygons, and more.
      Check the official documentation for a complete list.
    question: What other shapes can I draw with Aspose.Drawing?
  - answer: Absolutely. It works in ASP.NET Core, MVC, and other web frameworks, allowing
      server‑side image generation without additional dependencies.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Wrap your drawing code in a `try‑catch` block and consult the Aspose.Drawing
      forum (https://forum.aspose.com/c/drawing/44) for community support.
    question: How should I handle errors while using Aspose.Drawing?
  - answer: Yes, you can use Aspose.Drawing for commercial projects. Visit the [purchase
      page](https://purchase.aspose.com/buy) for licensing details.
    question: Can I use Aspose.Drawing for a commercial project?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing के साथ कई लाइनों को ड्रॉ करते हुए बिटमैप को PNG के रूप में कैसे
  सहेजें
url: /hi/net/lines-curves-and-shapes/draw-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# बिटमैप को PNG के रूप में सहेजें जबकि Aspose.Drawing के साथ कई रेखाएँ बनाएं

## परिचय

इस ट्यूटोरियल में आप सीखेंगे **बिटमैप को PNG के रूप में सहेजना** और Aspose.Drawing for .NET का उपयोग करके कई रेखाएँ बनाना। चाहे आप एक साधारण चार्ट, एक कस्टम UI कंट्रोल बना रहे हों, या सर्वर पर ग्राफिक्स जेनरेट कर रहे हों, स्पष्ट, एंटी‑एलियास्ड रेखाएँ रेंडर करने और उन्हें PNG फ़ाइलों के रूप में सहेजने की क्षमता एक मुख्य कौशल है। हम पूरे कार्यप्रवाह को चरण‑दर‑चरण दिखाएंगे—कैनवास तैयार करने से लेकर अंतिम इमेज को एक्सपोर्ट करने तक—ताकि आप तुरंत विज़ुअल कंपोनेंट बनाना शुरू कर सकें।

## त्वरित उत्तर
- **मैं क्या बना सकता हूँ?** कोई भी सीधी रेखा, पॉलीलाइन, या बिटमैप पर कोई भी आकार।  
- **कौन सी लाइब्रेरी?** Aspose.Drawing for .NET (कोई System.Drawing.Common आवश्यक नहीं)।  
- **कितनी रेखाएँ?** जितनी चाहें बनाएं – वही `Graphics.DrawLine` कॉल दोहराई जा सकती है।  
- **पूर्वापेक्षाएँ?** .NET विकास वातावरण और Aspose.Drawing लाइब्रेरी।  
- **आउटपुट फ़ॉर्मेट?** PNG, JPEG, BMP, या Aspose.Drawing द्वारा समर्थित कोई भी फ़ॉर्मेट।

## कई रेखाएँ बनाना क्या है?

एकाधिक रेखाएँ बनाना का अर्थ है एक ही इमेज कैनवास पर दो या अधिक सीधी रेखा खंडों को रेंडर करना। Aspose.Drawing में आप यह एक ही `Graphics` ऑब्जेक्ट को पुन: उपयोग करके और प्रत्येक कॉर्डिनेट जोड़ी के लिए `DrawLine` को कॉल करके प्राप्त करते हैं, जो रास्टर और वेक्टर दोनों आउटपुट के लिए तेज़, मेमोरी‑कुशल रेंडरिंग प्रदान करता है।

## .NET लाइन ड्रॉइंग के लिए Aspose.Drawing क्यों उपयोग करें?

Aspose.Drawing एक आधुनिक, क्रॉस‑प्लेटफ़ॉर्म API प्रदान करता है जो **30 से अधिक आउटपुट फ़ॉर्मेट** का समर्थन करता है और **10,000 × 10,000 पिक्सेल** तक की इमेज को पूरी फ़ाइल को मेमोरी में लोड किए बिना प्रोसेस कर सकता है। यह बिल्ट‑इन एंटी‑एलियासिंग, सटीक पिक्सेल नियंत्रण, और पूर्ण .NET Core/5+ संगतता प्रदान करता है, जिससे `System.Drawing.Common` की पुरानी निर्भरताएँ समाप्त हो जाती हैं।

## पूर्वापेक्षाएँ

ट्यूटोरियल में डुबकी लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- Aspose.Drawing लाइब्रेरी: Aspose.Drawing लाइब्रेरी को [यहाँ](https://releases.aspose.com/drawing/net/) से डाउनलोड और इंस्टॉल करें।
- विकास वातावरण: सुनिश्चित करें कि आपके मशीन पर .NET विकास वातावरण सेट अप है।
- डॉक्यूमेंट डायरेक्टरी: अपने सिस्टम पर एक डायरेक्टरी बनाएं जहाँ आप आउटपुट इमेज सहेजना चाहते हैं।

## नेमस्पेस आयात करें

अपने .NET एप्लिकेशन में, Aspose.Drawing के साथ काम करने के लिए आपको आवश्यक नेमस्पेस आयात करने होंगे। अपने कोड की शुरुआत में निम्नलिखित नेमस्पेस जोड़ें:

```csharp
using System.Drawing;
```

अब, हम उदाहरण को कई चरणों में विभाजित करेंगे ताकि Aspose.Drawing का उपयोग करके रेखाएँ बनाने की प्रक्रिया में आपका मार्गदर्शन कर सकें।

## Aspose.Drawing में कई रेखाएँ कैसे बनाएं

एक बिटमैप लोड करें, `Graphics` ऑब्जेक्ट प्राप्त करें, एक `Pen` कॉन्फ़िगर करें, प्रत्येक सेगमेंट के लिए `DrawLine` कॉल करें, और अंत में कैनवास को PNG के रूप में सहेजें—इन पाँच संक्षिप्त चरणों में जो दोहराए या अधिक जटिल ड्रॉइंग के लिए विस्तारित किए जा सकते हैं। प्रत्येक चरण को कोड स्निपेट्स के साथ दर्शाया गया है जो आवश्यक API कॉल्स और वैकल्पिक सेटिंग्स जैसे एंटी‑एलियासिंग को दिखाते हैं।

### चरण 1: एक बिटमैप बनाएं (रेखा बिटमैप)

`Bitmap` क्लास एक इन‑मेमोरी रास्टर इमेज का प्रतिनिधित्व करती है जिस पर आप ड्रॉ कर सकते हैं।  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, PixelFormat.Format32bppPArgb);
```

पहले वांछित चौड़ाई और ऊँचाई के साथ एक नया बिटमैप बनाएं। यह वह कैनवास होगा जिस पर आप अपनी रेखाएँ बनाएँगे।

### चरण 2: Graphics ऑब्जेक्ट प्राप्त करें

`Graphics` ऑब्जेक्ट बिटमैप के लिए रेखाएँ, आकार, और टेक्स्ट जैसी ड्रॉइंग मेथड्स प्रदान करता है।  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

बनाए गए बिटमैप से एक `Graphics` ऑब्जेक्ट प्राप्त करें। यह ऑब्जेक्ट बिटमैप पर ड्रॉ करने के मेथड्स प्रदान करता है।

### चरण 3: एक Pen परिभाषित करें

`Pen` `Graphics` ऑब्जेक्ट द्वारा ड्रॉ की गई रेखाओं का रंग, चौड़ाई, और शैली निर्धारित करता है।  
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

एक `Pen` ऑब्जेक्ट बनाएं जो आप जो रेखा ड्रॉ करना चाहते हैं उसकी विशेषताएँ निर्धारित करता है। इस मामले में, हमने 2 पिक्सेल की मोटाई के साथ नीला रंग चुना है।

### चरण 4: रेखाएँ बनाएं

`DrawLine` मेथड का उपयोग करके बिटमैप पर रेखाएँ बनाएं। निर्देशांक `(x1, y1)` से `(x2, y2)` प्रत्येक रेखा के प्रारंभ और अंत बिंदु दर्शाते हैं। मेथड को दो बार कॉल करके, हम प्रभावी रूप से **कई रेखाएँ बनाते** हैं जो एक साधारण “V” आकार बनाती हैं।  
```csharp
graphics.DrawLine(pen, 10, 700, 500, 10);
graphics.DrawLine(pen, 500, 10, 990, 700);
```

### चरण 5: इमेज सहेजें

`Bitmap.Save` मेथड इन‑मेमोरी इमेज को उस फ़ॉर्मेट में फ़ाइल में लिखता है जिसे आप निर्दिष्ट करते हैं—PNG सबसे सामान्य लॉस‑लेस विकल्प है।  
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawLines_out.png");
```

उस डायरेक्टरी को निर्दिष्ट करें जहाँ आप आउटपुट इमेज सहेजना चाहते हैं। सुनिश्चित करें कि `"Your Document Directory"` को वास्तविक पाथ से बदलें।

## बिटमैप को PNG के रूप में कैसे सहेजें

बिटमैप को PNG के रूप में सहेजना एक एकल‑लाइन ऑपरेशन है: उस `Bitmap` इंस्टेंस पर `bitmap.Save("output.png", ImageFormat.Png)` कॉल करें जिस पर आपने पहले ही ड्रॉ किया है। `ImageFormat` क्लास इमेज को सहेजने के फ़ॉर्मेट को निर्दिष्ट करती है, जैसे PNG, JPEG, या BMP। Aspose.Drawing स्वचालित रूप से कम्प्रेशन को संभालता है और ट्रांसपैरेंसी को बनाए रखता है, जिससे PNG वेब और UI एसेट्स के लिए आदर्श बनता है।

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| **इमेज खाली दिखती है** | Graphics ऑब्जेक्ट बिटमैप से जुड़ा नहीं है या पिक्सेल फ़ॉर्मेट गलत है। | सुनिश्चित करें कि `Graphics.FromImage(bitmap)` उपयोग किया गया है और बिटमैप समर्थित पिक्सेल फ़ॉर्मेट के साथ बनाया गया है। |
| **रेखाएँ खुरदरी हैं** | एंटी‑एलियासिंग निष्क्रिय है। | ड्रॉ करने से पहले `graphics.SmoothingMode = SmoothingMode.AntiAlias;` सेट करें (इसके लिए `using System.Drawing.Drawing2D;` आवश्यक है)। |
| **सेव पर पाथ नहीं मिला** | अमान्य डायरेक्टरी स्ट्रिंग। | `Path.Combine` का उपयोग करके पाथ बनाएं और सुनिश्चित करें कि फ़ोल्डर मौजूद है। |

`SmoothingMode` एन्यूमरेशन रेखाओं की रेंडरिंग क्वालिटी को नियंत्रित करता है, जहाँ `AntiAlias` स्मूथ किनारे प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं रेखाओं का रंग बदल सकता हूँ?**  
A: हाँ, बस `Pen` ऑब्जेक्ट बनाते समय `Color` पैरामीटर को बदल दें।

**Q: Aspose.Drawing के साथ मैं और कौन से आकार बना सकता हूँ?**  
A: Aspose.Drawing आयत, दीर्घवृत्त, कर्व, बहुभुज, और अधिक को सपोर्ट करता है। पूरी सूची के लिए आधिकारिक दस्तावेज़ देखें।

**Q: क्या Aspose.Drawing वेब एप्लिकेशन के लिए उपयुक्त है?**  
A: बिल्कुल। यह ASP.NET Core, MVC, और अन्य वेब फ्रेमवर्क में काम करता है, जिससे सर्वर‑साइड इमेज जेनरेशन बिना अतिरिक्त निर्भरताओं के संभव है।

**Q: Aspose.Drawing का उपयोग करते समय त्रुटियों को कैसे संभालें?**  
A: अपने ड्रॉइंग कोड को `try‑catch` ब्लॉक में रखें और समुदाय समर्थन के लिए Aspose.Drawing फ़ोरम (https://forum.aspose.com/c/drawing/44) देखें।

**Q: क्या मैं Aspose.Drawing को व्यावसायिक प्रोजेक्ट में उपयोग कर सकता हूँ?**  
A: हाँ, आप Aspose.Drawing को व्यावसायिक प्रोजेक्ट में उपयोग कर सकते हैं। लाइसेंसिंग विवरण के लिए [purchase page](https://purchase.aspose.com/buy) देखें।

## निष्कर्ष

इस गाइड में हमने Aspose.Drawing for .NET के साथ **बिटमैप को PNG के रूप में सहेजते हुए कई रेखाएँ बनाना** के लिए आवश्यक सभी चीज़ें कवर कीं: बिटमैप बनाना, ग्राफ़िक्स कॉन्टेक्स्ट प्राप्त करना, पेन कॉन्फ़िगर करना, रेखाएँ रेंडर करना, और परिणाम को सहेजना। इस आधार के साथ आप डायनामिक चार्ट, कस्टम UI एलिमेंट्स, या सर्वर‑साइड ग्राफ़िक्स जेनरेशन तक विस्तार कर सकते हैं—कोई भी परिदृश्य जो उच्च‑गुणवत्ता, स्केलेबल लाइन रेंडरिंग की मांग करता है।

---

**अंतिम अपडेट:** 2026-06-13  
**परीक्षण किया गया:** Aspose.Drawing 24.12 for .NET  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Aspose.Drawing के साथ बिटमैप को PNG के रूप में सहेजें और बंद वक्र बनाएं](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [C# में बिटमैप सहेजें – Aspose.Drawing के साथ बीज़ियर स्प्लाइन बनाएं](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Aspose.Drawing में सॉलिड ब्रश के साथ बिटमैप को PNG के रूप में सहेजें](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}