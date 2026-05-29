---
date: 2026-05-29
description: Aspose.Drawing का उपयोग करके .NET एप्लिकेशन्स में आर्क ड्रॉ करना और इमेज
  PNG सहेजना सीखें। यह चरण‑दर‑चरण इमेज ड्रॉइंग ट्यूटोरियल दिखाता है कि C# में bitmap
  कैसे बनाएं, line color सेट करें, आर्क ड्रॉ करें, और परिणाम को PNG फ़ाइल के रूप में
  सहेजें।
keywords:
- save image png
- how to draw arc
- set line color
- cross platform drawing
- replace system drawing
linktitle: Aspose.Drawing में आर्क ड्रॉ करना
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to draw arc and save image PNG in .NET applications using
    Aspose.Drawing. This step‑by‑step image drawing tutorial shows you how to create
    a bitmap in C#, set line color, draw the arc, and save the result as a PNG file.
  headline: How to Draw Arc and Save Image PNG with Aspose.Drawing
  type: TechArticle
- description: Learn how to draw arc and save image PNG in .NET applications using
    Aspose.Drawing. This step‑by‑step image drawing tutorial shows you how to create
    a bitmap in C#, set line color, draw the arc, and save the result as a PNG file.
  name: How to Draw Arc and Save Image PNG with Aspose.Drawing
  steps:
  - name: Create a bitmap C# object
    text: 'We first create a `Bitmap` that will serve as the canvas for our drawing.
      *Explanation*: The bitmap size (1000 × 800) gives us plenty of room, and the
      pixel format ensures high‑quality alpha blending.'
  - name: Set up a pen and set pen color
    text: Now we define a `Pen` that determines the line’s appearance. Here we **set
      pen color** to blue and choose a width of 2 pixels. You can replace `KnownColor.Blue`
      with any other known color or a custom `Color.FromArgb` value.
  - name: Draw the arc on bitmap
    text: 'With the graphics surface and pen ready, we can **draw arc on bitmap**.
      The parameters are: - `pen` – the styling we defined. - `0, 0` – the top‑left
      corner of the bounding rectangle. - `700, 700` – width and height of the rectangle
      (creates a perfect circle). - `0` – start angle in degrees. - `180`'
  - name: Save the bitmap PNG
    text: Load the bitmap into memory and call `Save` with a `.png` extension to **save
      image PNG** to disk. Adjust the path to match your project’s output folder.
      The saved file (`DrawArc_out.png`) contains the generated arc image, ready for
      use in UI, reports, or further processing.
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing fully supports .NET 6, .NET 7, and .NET 8 runtimes.
    question: Does this work with .NET 6 and later?
  - answer: The size is limited only by the available memory; for very large images
      consider streaming or tiling techniques.
    question: How large can the bitmap be?
  - answer: Absolutely—just call `graphics.DrawArc` multiple times with different
      coordinates or angles.
    question: Can I draw multiple arcs on the same bitmap?
  - answer: You can enable it by setting `graphics.SmoothingMode = SmoothingMode.AntiAlias;`
      before drawing.
    question: Is anti‑aliasing applied automatically?
  - answer: Call `graphics.Dispose();` and `bitmap.Dispose();` when you’re done to
      free native resources.
    question: How do I release resources after saving?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing के साथ आर्क ड्रॉ करना और इमेज PNG सहेजना कैसे करें
url: /hi/net/lines-curves-and-shapes/draw-arc/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing के साथ आर्क कैसे बनाएं और PNG इमेज सहेजें

## परिचय

यदि आपको एक .NET प्रोजेक्ट में **आर्क ड्रॉ करना और PNG इमेज सहेजना** है, तो Aspose.Drawing प्रक्रिया को सरल और उच्च‑प्रदर्शन बनाता है। इस ट्यूटोरियल में हम C# में एक bitmap बनाना, लाइन का रंग सेट करना, आर्क इमेज जनरेट करना, और अंत में bitmap को PNG फ़ाइल के रूप में सहेजना दिखाएंगे। चाहे आप रिपोर्टिंग टूल, कस्टम UI कॉम्पोनेंट बना रहे हों, या सिर्फ ग्राफ़िक्स का अन्वेषण कर रहे हों, ये कदम आपको एक ठोस, क्रॉस‑प्लेटफ़ॉर्म ड्रॉइंग आधार प्रदान करेंगे।

## त्वरित उत्तर
- **.NET में आर्क ड्रॉ करने के लिए सबसे अच्छा लाइब्रेरी कौन सा है?** Aspose.Drawing for .NET  
- **आर्क बनाने वाली मेथड कौन सी है?** `Graphics.DrawArc`  
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए फ्री ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **क्या मैं परिणाम को PNG के रूप में सहेज सकता हूँ?** हाँ—`.png` एक्सटेंशन के साथ `Bitmap.Save` का उपयोग करके **इमेज PNG सहेजें**।  
- **कौन से .NET संस्करण समर्थित हैं?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7।  

## Aspose.Drawing में “आर्क कैसे बनाएं” क्या है?

Aspose.Drawing में आर्क ड्रॉ करना का मतलब है एक एलिप्स या सर्कल के हिस्से को bitmap या अन्य ग्राफ़िक्स सतह पर रेंडर करना। आप `Bitmap` से एक `Graphics` ऑब्जेक्ट लोड करते हैं, बाउंडिंग रेक्टेंगल, स्टार्ट एंगल, और स्वीप एंगल निर्दिष्ट करते हैं, और लाइब्रेरी पिक्सेल‑परफेक्ट सटीकता के साथ कर्व्ड सेगमेंट पेंट करती है।  
`Graphics.DrawArc` एक एलिप्स या सर्कल के कर्व्ड सेगमेंट को ग्राफ़िक्स सतह पर ड्रॉ करता है।

## आर्क के लिए Aspose.Drawing क्यों उपयोग करें?

Aspose.Drawing Windows, Linux, और macOS पर लगातार रेंडरिंग प्रदान करता है, बिना System.Drawing.Common पर निर्भर हुए, जिससे यह आधुनिक .NET Core और .NET 5+ एप्लिकेशन्स के लिए आदर्श बनता है। यह हाई‑रेज़ोल्यूशन इमेज, एंटी‑एलियासिंग, और ड्रॉइंग प्रिमिटिव्स का समृद्ध सेट सपोर्ट करता है, जिससे आर्क्स स्मूद और सटीक दिखते हैं चाहे ऑपरेटिंग सिस्टम कुछ भी हो।

## पूर्वापेक्षाएँ

- Visual Studio (कोई भी नवीनतम संस्करण)  
- Aspose.Drawing for .NET – इसे [website](https://releases.aspose.com/drawing/net/) से डाउनलोड करें।  
- बेसिक C# ज्ञान (वेरिएबल्स, ऑब्जेक्ट्स, और मेथड कॉल्स)।  

## नेमस्पेस इम्पोर्ट करें

`Graphics` वह कोर क्लास है जो bitmap सतह के लिए ड्रॉइंग मेथड्स प्रदान करता है।  

`Bitmap` एक इन‑मेमोरी इमेज को दर्शाता है जिस पर आप ड्रॉ कर सकते हैं।  

`Pen` ड्रॉइंग ऑपरेशन्स के लिए लाइन स्टाइल, चौड़ाई, और रंग को परिभाषित करता है।  

```csharp
using System.Drawing;
```

## चरण‑दर‑चरण गाइड

### चरण 1: एक bitmap C# ऑब्जेक्ट बनाएं

हम पहले एक `Bitmap` बनाते हैं जो हमारे ड्रॉइंग के लिए कैनवास के रूप में काम करेगा।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

*व्याख्या*: bitmap का आकार (1000 × 800) हमें पर्याप्त जगह देता है, और पिक्सेल फ़ॉर्मेट हाई‑क्वालिटी अल्फा ब्लेंडिंग सुनिश्चित करता है।

### चरण 2: पेन सेट करें और पेन का रंग निर्धारित करें

अब हम एक `Pen` परिभाषित करते हैं जो लाइन की उपस्थिति तय करेगा। यहाँ हम **पेन का रंग** नीला सेट करते हैं और चौड़ाई 2 पिक्सेल चुनते हैं।

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

आप `KnownColor.Blue` को किसी भी अन्य ज्ञात रंग या कस्टम `Color.FromArgb` वैल्यू से बदल सकते हैं।

### चरण 3: bitmap पर आर्क ड्रॉ करें

ग्राफ़िक्स सतह और पेन तैयार होने के बाद, हम **bitmap पर आर्क ड्रॉ** कर सकते हैं।

```csharp
graphics.DrawArc(pen, 0, 0, 700, 700, 0, 180);
```

पैरामीटर हैं:

- `pen` – हमने जो स्टाइल परिभाषित किया।  
- `0, 0` – बाउंडिंग रेक्टेंगल का टॉप‑लेफ़्ट कोना।  
- `700, 700` – रेक्टेंगल की चौड़ाई और ऊँचाई (एक परिपूर्ण सर्कल बनाता है)।  
- `0` – डिग्री में स्टार्ट एंगल।  
- `180` – स्वीप एंगल, जो आधा सर्कल आर्क बनाता है।

### चरण 4: bitmap PNG सहेजें

bitmap को मेमोरी में लोड करें और `.png` एक्सटेंशन के साथ `Save` कॉल करें ताकि **इमेज PNG सहेजें** डिस्क पर हो सके। अपने प्रोजेक्ट के आउटपुट फ़ोल्डर के अनुसार पाथ समायोजित करें।

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawArc_out.png");
```

सहेजी गई फ़ाइल (`DrawArc_out.png`) में जनरेट किया गया आर्क इमेज होता है, जिसे UI, रिपोर्ट्स, या आगे की प्रोसेसिंग में उपयोग किया जा सकता है।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **Arc appears distorted** | सुनिश्चित करें कि सच्चे सर्कल के लिए चौड़ाई और ऊँचाई मान बराबर हों; अन्यथा आपको एलिप्टिकल आर्क मिलेगा। |
| **File not found exception** | यह पुष्टि करें कि लक्ष्य डायरेक्टरी मौजूद है या `Save` कॉल करने से पहले प्रोग्रामेटिकली इसे बनाएं। |
| **Colors look different on Linux** | प्लेटफ़ॉर्म‑क्रॉस संगतता के लिए स्पष्ट RGBA मान वाले `Color.FromArgb` का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं आर्क का रंग कस्टमाइज़ कर सकता हूँ?

A1: हाँ, आप `Pen` ऑब्जेक्ट बनाते समय रंग पैरामीटर को बदल सकते हैं।

### प्रश्न 2: क्या मैं आर्क के लिए अलग स्टार्ट एंगल सेट कर सकता हूँ?

A2: `DrawArc` मेथड में स्टार्ट एंगल पैरामीटर को अपनी आवश्यकता अनुसार बदलें।

### प्रश्न 3: क्या Aspose.Drawing अन्य ग्राफ़िक एलिमेंट्स के लिए भी उपयुक्त है?

A3: बिल्कुल। Aspose.Drawing लाइन्स, कर्व्स, और शैप्स सहित कई ग्राफ़िक एलिमेंट्स को सपोर्ट करता है।

### प्रश्न 4: क्या मैं Aspose.Drawing को अन्य .NET लाइब्रेरीज़ के साथ इंटीग्रेट कर सकता हूँ?

A4: हाँ, Aspose.Drawing अन्य .NET लाइब्रेरीज़ के साथ सहजता से इंटीग्रेट होता है, जिससे आपके विकास में लचीलापन मिलता है।

### प्रश्न 5: अतिरिक्त सपोर्ट या कम्युनिटी डिस्कशन कहाँ मिल सकते हैं?

A5: कम्युनिटी सपोर्ट और डिस्कशन के लिए [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) देखें।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या यह .NET 6 और बाद के संस्करणों के साथ काम करता है?**  
**उत्तर:** हाँ, Aspose.Drawing पूरी तरह से .NET 6, .NET 7, और .NET 8 रनटाइम्स को सपोर्ट करता है।

**प्रश्न: bitmap का आकार कितना बड़ा हो सकता है?**  
**उत्तर:** आकार केवल उपलब्ध मेमोरी पर निर्भर करता है; बहुत बड़ी इमेज के लिए स्ट्रीमिंग या टाइलिंग तकनीकें उपयोग करने पर विचार करें।

**प्रश्न: क्या मैं एक ही bitmap पर कई आर्क ड्रॉ कर सकता हूँ?**  
**उत्तर:** बिल्कुल—विभिन्न कॉर्डिनेट्स या एंगल्स के साथ `graphics.DrawArc` को कई बार कॉल करें।

**प्रश्न: क्या एंटी‑एलियासिंग स्वतः लागू होता है?**  
**उत्तर:** ड्रॉ करने से पहले `graphics.SmoothingMode = SmoothingMode.AntiAlias;` सेट करके इसे सक्षम कर सकते हैं।

**प्रश्न: सहेजने के बाद संसाधन कैसे रिलीज़ करें?**  
**उत्तर:** काम समाप्त होने पर `graphics.Dispose();` और `bitmap.Dispose();` कॉल करके नेटिव रिसोर्सेज़ को फ्री करें।

## निष्कर्ष

अब आप Aspose.Drawing का उपयोग करके **आर्क ड्रॉ करना और PNG इमेज सहेजना** जानते हैं, bitmap C# ऑब्जेक्ट बनाना, लाइन का रंग सेट करना, आर्क जनरेट करना, और परिणाम को PNG फ़ाइल के रूप में सहेजना। विभिन्न एंगल्स, रंगों, और लाइन चौड़ाइयों के साथ प्रयोग करें ताकि आपके एप्लिकेशन में कस्टम ग्राफ़िक्स जोड़ सकें।

---

**अंतिम अपडेट:** 2026-05-29  
**परीक्षण किया गया:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.Drawing for .NET के साथ आर्क और अन्य आकार कैसे बनाएं](/drawing/net/lines-curves-and-shapes/)
- [Aspose.Drawing for .NET के साथ एलिप्स कैसे बनाएं](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [bitmap aspose.drawing बनाएं – .NET में पॉलीगॉन ड्रॉ करें](/drawing/net/lines-curves-and-shapes/draw-polygon/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}