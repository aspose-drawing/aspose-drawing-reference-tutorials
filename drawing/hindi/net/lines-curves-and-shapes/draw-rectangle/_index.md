---
date: 2026-08-01
description: Aspose.Drawing का उपयोग करके C# में bitmap image कैसे बनाएं और bitmap
  पर rectangle कैसे बनाएं, सीखें। .NET डेवलपर्स के लिए चरण-दर-चरण गाइड।
keywords:
- create bitmap image c#
- draw rectangle on bitmap
- replace system.drawing
lastmod: 2026-08-01
linktitle: Aspose.Drawing में Rectangles बनाना
og_description: Aspose.Drawing का उपयोग करके C# में bitmap image बनाएं और bitmap पर
  rectangle ड्रॉ करें। यह ट्यूटोरियल दिखाता है कि .NET में rectangle ग्राफिक्स को
  कैसे जनरेट, स्टाइल और सेव करें।
og_image_alt: Guide to drawing rectangles on a bitmap with Aspose.Drawing for .NET
og_title: Create Bitmap Image C# – Aspose.Drawing के साथ Rectangle बनाएं
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to create bitmap image C# and draw rectangle on bitmap using
    Aspose.Drawing. Step‑by‑step guide for .NET developers.
  headline: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)`
      before or after drawing the outline.
    question: Can I fill the rectangle with a solid color?
  - answer: Loop through a collection of `Rectangle` structs and call `DrawRectangle`
      for each iteration.
    question: How do I draw multiple rectangles?
  - answer: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform
      after.
    question: Is there a way to rotate the rectangle?
  - answer: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat`
      parameter.
    question: What image formats are supported for saving?
  - answer: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and
      later versions.
    question: Does Aspose.Drawing work on .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- create bitmap image
- Aspose.Drawing
- .NET graphics
- draw rectangle
title: Create Bitmap Image C# – Aspose.Drawing के साथ .NET में Rectangle बनाएं
url: /hi/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Drawing के साथ आयत कैसे बनाएं

## परिचय

इस ट्यूटोरियल में आप **आयत कैसे बनाएं** सीखेंगे और साथ ही Aspose.Drawing का उपयोग करके **C# में बिटमैप इमेज बनाना** भी सीखेंगे। चाहे आपको एक साधारण UI तत्व चाहिए या रिपोर्ट के लिए हाई‑रेज़ोल्यूशन ग्राफिक, हम बिटमैप बनाना, ग्राफ़िक्स ऑब्जेक्ट कॉन्फ़िगर करना, आयत ड्रॉ करना और अंतिम इमेज सहेजना दिखाएंगे। यह तरीका Windows, Linux, और macOS पर काम करता है, और पुराने `System.Drawing.Common` API को पूरी तरह से क्रॉस‑प्लेटफ़ॉर्म समाधान से बदलता है।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी आवश्यक है?** Aspose.Drawing for .NET  
- **कौन सा मेथड आकृति बनाता है?** `Graphics.DrawRectangle`  
- **क्या मुझे लाइसेंस चाहिए?** ट्रायल मुफ्त है; उत्पादन के लिए व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं आयत का आकार बदल सकता हूँ?** हाँ – चौड़ाई, ऊँचाई और स्थिति पैरामीटर को समायोजित करें।  
- **क्या कोड .NET 6+ के साथ संगत है?** बिल्कुल, Aspose.Drawing आधुनिक .NET संस्करणों का समर्थन करता है।

## Aspose.Drawing के संदर्भ में “आयत कैसे बनाएं” क्या है?

Aspose.Drawing के साथ आयत बनाना `Graphics` क्लास का उपयोग करके बिटमैप कैनवास पर आयताकार रूपरेखा या भरी हुई आकृति रेंडर करता है। यह आकार, रंग, लाइन मोटाई और इमेज फॉर्मेट पर पूर्ण नियंत्रण देता है, जिससे ऑन‑द‑फ़्लाई ग्राफ़िक्स बनाना आसान हो जाता है। क्योंकि Aspose.Drawing एक शुद्ध‑मैनेज्ड इंजन पर चलता है, यह `System.Drawing.Common` की मूल GDI+ सीमाओं से बचता है।

## आयत निर्माण के लिए Aspose.Drawing क्यों उपयोग करें?

Aspose.Drawing आपको **बिटमैप पर आयत ड्रॉ** करने की अनुमति देता है बिना किसी प्लेटफ़ॉर्म‑विशिष्ट DLL के, और यह **30+ आउटपुट फ़ॉर्मेट** (PNG, JPEG, BMP, GIF, और TIFF सहित) का समर्थन करता है। यह **10,000 × 10,000 पिक्सेल** तक की छवियों को प्रोसेस कर सकता है जबकि मेमोरी उपयोग **100 MB** से कम रखता है, जो लेगेसी System.Drawing कार्यान्वयन से 2‑3× अधिक कुशल है।

## पूर्वापेक्षाएँ

कोड में जाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- **Aspose.Drawing लाइब्रेरी** – इसे आधिकारिक साइट से [यहाँ](https://releases.aspose.com/drawing/net/) डाउनलोड करें।  
- **डेवलपमेंट एनवायरनमेंट** – Visual Studio 2022 या कोई भी .NET‑संगत IDE।  
- **बुनियादी .NET ज्ञान** – C# सिंटैक्स और प्रोजेक्ट स्ट्रक्चर की परिचितता।

## नेमस्पेस इम्पोर्ट करें

`using` निर्देश आवश्यक क्लासेज़ को स्कोप में लाते हैं। ये किसी भी ड्रॉइंग ऑपरेशन के लिए आवश्यक हैं।

```csharp
using System.Drawing;
```

## चरण 1: बिटमैप इमेज बनाएं

`Bitmap` एक इन‑मेमोरी रास्टर इमेज को दर्शाता है जिस पर आप ड्रॉ कर सकते हैं। इसे बनाते समय कैनवास का आकार और पिक्सेल फॉर्मेट निर्धारित होता है।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## चरण 2: ग्राफ़िक्स ऑब्जेक्ट बनाएं

`Graphics` वह इंजन है जो बिटमैप सतह पर सभी ड्रॉइंग कमांड्स को निष्पादित करता है। एक बार मिलने के बाद आप आकृतियाँ, टेक्स्ट और इमेज रेंडर कर सकते हैं।

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## चरण 3: आयत के लिए पेन परिभाषित करें

`Pen` आयत की रूपरेखा का रंग और मोटाई निर्धारित करता है। यह डैश स्टाइल और लाइन जॉइन भी नियंत्रित करता है।

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## चरण 4: बिटमैप पर आयत ड्रॉ करें

`Graphics.DrawRectangle` पहले परिभाषित पेन का उपयोग करके आयत ड्रॉ करता है। आप X, Y निर्देशांक के साथ चौड़ाई और ऊँचाई प्रदान करके आकृति को ठीक उसी जगह रख सकते हैं जहाँ आपको चाहिए।

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## चरण 5: ड्रॉ की गई इमेज सहेजें

`Bitmap.Save` मेथड चुने हुए फॉर्मेट (जैसे PNG, JPEG) में इमेज को डिस्क पर लिखता है। यह चरण **ड्रॉ की गई इमेज सहेजें** क्षमता को दर्शाता है और बिटमैप को पुन: उपयोग के लिए अंतिम रूप देता है।

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

बधाई हो! आपने Aspose.Drawing for .NET का उपयोग करके **आयत कैसे बनाएं** सफलतापूर्वक पूरा कर लिया है और प्रक्रिया में **C# में बिटमैप इमेज बनाना** भी सीख लिया है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|-------|----------|
| खाली इमेज आउटपुट | Bitmap डिस्पोज़ नहीं हुआ या graphics फ्लश नहीं हुआ | `graphics.Dispose();` को सहेजने से पहले कॉल करें, या `using` ब्लॉक का उपयोग करें। |
| किनारे धुंधले | डिफ़ॉल्ट स्मूदिंग मोड | `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;` सेट करें। |
| फ़ाइल पाथ त्रुटियाँ | अमान्य डायरेक्टरी | सुनिश्चित करें कि लक्ष्य फ़ोल्डर मौजूद है या सुरक्षित पाथ बनाने के लिए `Path.Combine` का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q:** क्या मैं आयत को ठोस रंग से भर सकता हूँ?  
**A:** हाँ, एक `SolidBrush` बनाएं और `graphics.FillRectangle(brush, …)` को रूपरेखा ड्रॉ करने से पहले या बाद में कॉल करें।

**Q:** मैं कई आयतें कैसे बनाऊँ?  
**A:** `Rectangle` स्ट्रक्ट्स के संग्रह पर लूप चलाएँ और प्रत्येक इटरेशन में `DrawRectangle` कॉल करें।

**Q:** क्या आयत को घुमाने का कोई तरीका है?  
**A:** ड्रॉ करने से पहले `graphics.RotateTransform(angle)` उपयोग करें, फिर ट्रांसफ़ॉर्म को रीसेट करें।

**Q:** सहेजने के लिए कौन‑से इमेज फ़ॉर्मेट समर्थित हैं?  
**A:** PNG, JPEG, BMP, GIF, और TIFF सभी उपयुक्त `ImageFormat` पैरामीटर के माध्यम से समर्थित हैं।

**Q:** क्या Aspose.Drawing .NET Core पर काम करता है?  
**A:** हाँ, लाइब्रेरी .NET Core, .NET 5, .NET 6 और बाद के संस्करणों के साथ पूरी तरह संगत है।

---

**अंतिम अपडेट:** 2026-08-01  
**परीक्षित संस्करण:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose  

---

## संबंधित ट्यूटोरियल

- [How to Draw Ellipse with Aspose.Drawing for .NET](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [Draw multiple lines with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [How to create bitmap aspose.drawing – Draw Polygons in .NET](/drawing/net/lines-curves-and-shapes/draw-polygon/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}