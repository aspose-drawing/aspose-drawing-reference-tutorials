---
date: 2026-05-24
description: Aspose.Drawing for .NET में यूनिट सेट करना सीखें, ग्राफ़िक्स यूनिट्स
  को आसानी से बदलें, और ग्राफ़िक्स रेंडरिंग के लिए सटीक मापों में महारत हासिल करें।
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Aspose.Drawing में Units of Measure
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET में यूनिट कैसे सेट करें – Units of Measure
url: /hi/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET में यूनिट सेट कैसे करें – माप की इकाइयाँ

## परिचय

Aspose.Drawing for .NET की दुनिया में आपका स्वागत है, जहाँ सटीकता और लचीलापन ग्राफ़िक हेरफेर में मिलते हैं। इस ट्यूटोरियल में आप **यूनिट सेट करने का तरीका** खोजेंगे, **ग्राफ़िक्स इकाइयों को बदलना** पॉइंट्स, मिलीमीटर और इंच के बीच सीखेंगे, और वास्तविक दुनिया के उदाहरण देखेंगे जो आपकी छवियों को पिक्सेल‑परफेक्ट बनाते हैं। चाहे आप रिपोर्ट, थंबनेल या कस्टम चार्ट बना रहे हों, माप की इकाइयों में महारत हासिल करना विभिन्न डिवाइसों पर स्थिर रेंडरिंग के लिए आवश्यक है।

## त्वरित उत्तर
- **यूनिट बदलने का मुख्य तरीका क्या है?** `graphics.PageUnit = PageUnit.Point` (या `.Millimeter`, `.Inch`) को `Graphics` ऑब्जेक्ट पर कॉल करें।  
- **कौन सी इकाई 1/72 इंच के बराबर है?** पॉइंट्स।  
- **एक इंच में कितने मिलीमीटर होते हैं?** 25.4 mm = 1 inch।  
- **क्या यूनिट उपयोग करने के लिए अतिरिक्त लाइब्रेरी की आवश्यकता है?** नहीं, Aspose.Drawing कोर लाइब्रेरी सभी यूनिट कॉन्स्टेंट्स प्रदान करती है।  
- **क्या मैं एक इमेज में विभिन्न यूनिट्स मिला सकता हूँ?** प्रत्येक `Graphics` इंस्टेंस के लिए यूनिट एक बार सेट करें; सभी ड्रॉइंग उसी यूनिट का उपयोग करके करें ताकि स्थिरता बनी रहे।

## आवश्यकताएँ

ट्यूटोरियल में डुबकी लगाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यकताएँ मौजूद हैं:

- Aspose.Drawing for .NET: सुनिश्चित करें कि आपके पास लाइब्रेरी स्थापित है। आप इसे [यहाँ](https://releases.aspose.com/drawing/net/) डाउनलोड कर सकते हैं।  
- डॉक्यूमेंट डायरेक्टरी: एक निर्धारित फ़ोल्डर रखें जहाँ आप बनाए गए दस्तावेज़ सहेजना चाहते हैं।  
- बेसिक C# नॉलेज: इस गाइड का अधिकतम उपयोग करने के लिए C# की बुनियादी समझ की सलाह दी जाती है।

## नेमस्पेस इम्पोर्ट करें

शुरू करने से पहले, Aspose.Drawing का प्रभावी उपयोग करने के लिए आवश्यक नेमस्पेस इम्पोर्ट करें:

```csharp
using System.Drawing;
```

अब, प्रत्येक उदाहरण को कई चरणों में विभाजित करते हैं:

## पॉइंट्स में यूनिट कैसे सेट करें?

`Bitmap` क्लास एक इन‑मेरी इमेज का प्रतिनिधित्व करती है जो ड्रॉइंग कैनवास के रूप में कार्य करती है। अपना बिटमैप लोड करें, एक `Graphics` ऑब्जेक्ट बनाएं, और पेज यूनिट को पॉइंट्स पर सेट करें — यह Aspose.Drawing को सभी निर्देशांक को 1/72 इंच मानों के रूप में व्याख्या करने को बताता है। पॉइंट्स का उपयोग करने से आपको प्रिंट‑रेडी ग्राफ़िक्स के लिए सूक्ष्म नियंत्रण मिलता है और आप लाइन की चौड़ाई को उच्च सटीकता के साथ निर्दिष्ट कर सकते हैं।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### चरण 1: बिटमैप बनाएं  
`Bitmap` क्लास एक इन‑मेरी इमेज का प्रतिनिधित्व करती है जो ड्रॉइंग कैनवास के रूप में कार्य करती है।

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### चरण 2: ग्राफ़िक्स ऑब्जेक्ट बनाएं  
`Graphics` `Bitmap` पर आकार और टेक्स्ट रेंडर करने के लिए ड्रॉइंग मेथड प्रदान करता है।

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### चरण 3: पेज यूनिट को पॉइंट्स पर सेट करें  
`PageUnit` एक एनेमरेशन है जो पेज निर्देशांक के माप की इकाई निर्दिष्ट करता है। `PageUnit.Point` पॉइंट्स को माप की इकाई के रूप में परिभाषित करता है (1 पॉइंट = 1/72 इंच)। यह सेटिंग सभी बाद के ड्रॉइंग कॉल्स पर लागू होती है।

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### चरण 4: पॉइंट्स में एक आयत बनाएं  
जब आप यूनिट सेट करने के बाद एक आयत बनाते हैं, तो आप जो आयाम निर्दिष्ट करते हैं वे पॉइंट्स के रूप में व्याख्या होते हैं, जिससे सटीक आकार सुनिश्चित होता है।

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## मिलीमीटर में यूनिट कैसे सेट करें?

`PageUnit` एक एनेमरेशन है जो पेज निर्देशांक के माप की इकाई निर्दिष्ट करता है। मिलीमीटर में स्विच करना उपयोगी होता है जब आपको मीट्रिक आयाम चाहिए, उदाहरण के लिए इंजीनियरिंग डायग्राम बनाते समय। Aspose.Drawing 1 mm को 1/25.4 इंच मानता है, जिससे आप निर्माण और तकनीकी दस्तावेज़ीकरण में उपयोग किए जाने वाले भौतिक मापों के साथ ग्राफ़िक्स को संरेखित कर सकते हैं।

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### चरण 1: पेज यूनिट को मिलीमीटर पर सेट करें  
`PageUnit.Millimeter` को `Graphics` ऑब्जेक्ट को असाइन करें; अब सभी निर्देशांक मीट्रिक सिस्टम से मैप होते हैं।

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### चरण 2: मिलीमीटर में एक आयत बनाएं  
आयत की चौड़ाई और ऊँचाई अब मिलीमीटर में व्यक्त की गई हैं, जिससे भौतिक मापों के साथ संरेखित करना आसान हो जाता है और सुनिश्चित होता है कि प्रिंट आउटपुट वास्तविक आकारों से मेल खाता है।

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## इंच में यूनिट कैसे सेट करें?

`Graphics` `Bitmap` पर आकार और टेक्स्ट रेंडर करने के लिए ड्रॉइंग मेथड प्रदान करता है। इंच कई अमेरिकी‑आधारित डिज़ाइन टूल्स की डिफ़ॉल्ट इकाई है। यूनिट को इंच पर सेट करने से UI एलिमेंट्स लेआउट करते समय परिचित शब्दों में सोचना आसान हो जाता है, और स्क्रीन डिज़ाइन से प्रिंट में परिवर्तन सरल हो जाता है जहाँ इंच आमतौर पर उपयोग होते हैं।

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### चरण 1: पेज यूनिट को इंच पर सेट करें  
`PageUnit.Inch` कोऑर्डिनेट सिस्टम को बदलता है ताकि 1 यूनिट = 1 इंच हो, जिससे प्रिंट‑उन्मुख लेआउट के लिए एलिमेंट्स का आकार निर्धारित करना सीधा हो जाता है।

CODE_BLOCK_PLACEHOLDER_10_END

### चरण 2: इंच में एक आयत बनाएं  
अब आप जो भी आकार बनाते हैं वह इंच को अपने माप आधार के रूप में उपयोग करता है, जो प्रिंट लेआउट और इम्पीरियल यूनिट्स के आदी स्टेकहोल्डर्स को आयाम संप्रेषित करने के लिए आदर्श है।

CODE_BLOCK_PLACEHOLDER_11_END

## परिणाम सहेजें

उदाहरण पूर्ण करने के बाद, परिणामी इमेज को अपने डॉक्यूमेंट डायरेक्टरी में सहेजें। `Bitmap.Save` मेथड फ़ाइल को उस फॉर्मेट में लिखता है जिसे आप निर्दिष्ट करते हैं (PNG, JPEG, आदि)।

CODE_BLOCK_PLACEHOLDER_12_END

अब, आपने Aspose.Drawing for .NET में विभिन्न माप की इकाइयों को सफलतापूर्वक नेविगेट कर लिया है, पॉइंट्स, मिलीमीटर और इंच का उपयोग करके आयतों का दृश्य प्रतिनिधित्व बनाया है।

## Aspose.Drawing के यूनिट सिस्टम का उपयोग क्यों करें?

Aspose.Drawing **30+ इमेज फॉर्मेट्स** को सपोर्ट करता है और **5000 × 5000 पिक्सेल** तक की इमेजेज को पूरी फ़ाइल को मेमोरी में लोड किए बिना प्रोसेस कर सकता है, जिससे बड़े‑पैमाने पर ग्राफ़िक्स जनरेशन के लिए उच्च प्रदर्शन मिलता है। यूनिट को स्पष्ट रूप से सेट करके आप अनुमान को समाप्त करते हैं, रूपांतरण त्रुटियों को कम करते हैं, और सुनिश्चित करते हैं कि आपका आउटपुट सभी प्लेटफ़ॉर्म पर सटीक भौतिक आयामों से मेल खाता हो।

## सामान्य समस्याएँ और समाधान

- **सेव करने के बाद अप्रत्याशित आकार** – सुनिश्चित करें कि आपने किसी भी ड्रॉइंग कॉल से **पहले** `graphics.PageUnit` सेट किया है; बाद में यूनिट बदलने से मौजूदा आकारों का आकार retroactively नहीं बदलता।  
- **हाई‑DPI स्क्रीन पर धुंधला आउटपुट** – लक्ष्य DPI से मेल खाने के लिए बिटमैप की रेज़ॉल्यूशन बढ़ाएँ (जैसे, `new Bitmap(width, height, 300)`)।  
- **एक इमेज में मिश्रित यूनिट्स** – प्रत्येक यूनिट के लिए अलग `Graphics` इंस्टेंस बनाएं या ड्रॉइंग से पहले मैन्युअल रूपांतरण करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं Aspose.Drawing for .NET को अन्य .NET फ्रेमवर्क्स के साथ उपयोग कर सकता हूँ?
A1: हाँ, Aspose.Drawing विभिन्न .NET फ्रेमवर्क्स के साथ संगत है, जिससे आपके विकास वातावरण में लचीलापन मिलता है।

### प्रश्न 2: क्या कोई मुफ्त ट्रायल उपलब्ध है?
A2: हाँ, आप Aspose.Drawing को एक मुफ्त ट्रायल के साथ आज़मा सकते हैं [यहाँ](https://releases.aspose.com/)।

### प्रश्न 3: Aspose.Drawing for .NET के लिए समर्थन कैसे प्राप्त करें?
A3: समुदाय समर्थन और चर्चा के लिए [Aspose.Drawing फ़ोरम](https://forum.aspose.com/c/drawing/44) पर जाएँ।

### प्रश्न 4: क्या मैं अल्पकालिक प्रोजेक्ट्स के लिए अस्थायी लाइसेंस खरीद सकता हूँ?
A4: हाँ, आप एक अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

### प्रश्न 5: Aspose.Drawing के विस्तृत दस्तावेज़ कहाँ मिल सकते हैं?
A5: व्यापक दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/drawing/net/) उपलब्ध है।

---

**अंतिम अद्यतन:** 2026-05-24  
**परीक्षण किया गया:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [कोऑर्डिनेट सिस्टम ट्रांसफ़ॉर्मेशन – पेज ट्रांसफ़ॉर्मेशन Aspose.Drawing for .NET में](/drawing/net/coordinate-transformations/page-transformation/)
- [मैट्रिक्स ट्रांसफ़ॉर्मेशन ट्यूटोरियल: Aspose.Drawing for .NET में मैट्रिक्स ट्रांसफ़ॉर्मेशन](/drawing/net/coordinate-transformations/matrix-transformations/)
- [ट्रांसफ़ॉर्मेशन कैसे लागू करें: Aspose.Drawing for .NET में लोकल ट्रांसफ़ॉर्मेशन](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}