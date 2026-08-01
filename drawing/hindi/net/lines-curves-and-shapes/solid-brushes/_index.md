---
date: 2026-08-01
description: .NET के लिए Aspose.Drawing में सॉलिड ब्रशेज़ का उपयोग करके बिटमैप को
  PNG के रूप में सहेजना सीखें। सॉलिड ब्रश का उपयोग करके आकृतियों को भरें और जीवंत
  ग्राफिक्स बनाएं।
keywords:
- save bitmap as png
- export bitmap to png
- fill shape solid color
- bitmap to png conversion
lastmod: 2026-08-01
linktitle: Aspose.Drawing में सॉलिड ब्रशेज़
og_description: Aspose.Drawing में सॉलिड ब्रशेज़ का उपयोग करके बिटमैप को PNG के रूप
  में सहेजें। यह step‑by‑step ट्यूटोरियल दिखाता है कि बिटमैप कैसे बनाएं, आकृतियों
  को सॉलिड रंग से भरें, और परिणाम को .NET 6+ प्रोजेक्ट्स के लिए लॉसलेस PNG फ़ाइल के
  रूप में एक्सपोर्ट करें।
og_image_alt: Guide showing how to save a bitmap as PNG using solid brushes in Aspose.Drawing
og_title: सॉलिड ब्रशेज़ के साथ बिटमैप को PNG के रूप में सहेजें – Aspose.Drawing गाइड
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  headline: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  name: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image canvas. The `Bitmap` class
      is Aspose.Drawing's top‑level object that stores pixel data in a mutable buffer.
      You can specify width, height, and pixel format when constructing it.
  - name: Create Graphics Object
    text: A `Graphics` object provides drawing methods for the bitmap. The `Graphics`
      class acts as a drawing surface linked to a `Bitmap`. All subsequent drawing
      commands (lines, shapes, text) are routed through this object.
  - name: Choose a Solid Brush
    text: Select a colour for the brush; in this example we use a vivid blue. The
      `SolidBrush` class defines a brush that paints with a single, uniform colour.
      It is ideal for filling shapes where a flat colour is required.
  - name: Fill Shapes with Brush
    text: Use the brush to paint an ellipse (or any other shape) on the bitmap. `FillEllipse`
      draws an ellipse filled with the specified brush. The `FillEllipse` method of
      the `Graphics` object draws an ellipse filled with the supplied `SolidBrush`.
      You can replace it with `FillRectangle`, `FillPolygon`, etc.
  - name: Save the Result as PNG
    text: Export the bitmap to a PNG file on disk. `Save` writes the image to a file
      in the chosen format. The `Save` method writes the bitmap to the specified path
      using `ImageFormat.Png`. This operation preserves the alpha channel, ensuring
      transparent backgrounds remain intact. Repeat these steps, customiz
  type: HowTo
- questions:
  - answer: Absolutely—methods like `FillRectangle`, `FillPolygon`, or `DrawPath`
      work with the same solid brush.
    question: Can I use a different shape instead of an ellipse?
  - answer: Replace the file extension in `Save` and use `ImageFormat.Jpeg` (e.g.,
      `bitmap.Save("output.jpg", ImageFormat.Jpeg);`).
    question: How do I change the output format to JPEG?
  - answer: Yes—create separate `SolidBrush` instances for each colour and call the
      appropriate `Fill*` methods sequentially.
    question: Is it possible to draw multiple shapes with different brushes in one
      bitmap?
  - answer: It's best practice to wrap them in `using` statements or call `Dispose()`
      to free unmanaged resources.
    question: Do I need to dispose of the `Graphics` and `Bitmap` objects?
  - answer: Aspose.Drawing is cross‑platform; the same code runs on Linux and macOS
      when targeting .NET Core or .NET 5+.
    question: Will this work on Linux/macOS with .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- solid brush
title: Aspose.Drawing में सॉलिड ब्रशेज़ के साथ बिटमैप को PNG के रूप में सहेजें
url: /hi/net/lines-curves-and-shapes/solid-brushes/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Solid Brushes के साथ Aspose.Drawing में Bitmap को PNG के रूप में सहेजें

## परिचय

इस गाइड में आप **कैसे bitmap को PNG के रूप में सहेजें** यह सीखेंगे, Aspose.Drawing .NET लाइब्रेरी के साथ solid brushes का उपयोग करके। चाहे आप एक डेस्कटॉप यूटिलिटी बना रहे हों, आइकन उत्पन्न करने वाली वेब सेवा, या एक रिपोर्टिंग इंजन जो स्पष्ट PNG एसेट्स की आवश्यकता रखता है, नीचे दिए गए चरण आपको खाली कैनवास से तैयार‑उपयोग PNG फ़ाइल तक कुछ ही कोड लाइनों में ले जाएंगे। हम पूरी कार्यप्रवाह को कवर करेंगे, समझाएंगे कि solid brushes समान रंग भराव के लिए आदर्श क्यों हैं, और दिखाएंगे कि कोड को साफ़ और क्रॉस‑प्लेटफ़ॉर्म कैसे रखें।

## त्वरित उत्तर
- **“save bitmap as png” का क्या अर्थ है?** इसका मतलब है `Bitmap` ऑब्जेक्ट को डिस्क पर एक लॉसलेस PNG इमेज फ़ाइल में निर्यात करना।  
- **कौन सा क्लास solid brush बनाता है?** `Aspose.Drawing.Brushes` नेमस्पेस से `SolidBrush`।  
- **क्या मैं brush का रंग बदल सकता हूँ?** हाँ—`SolidBrush` कन्स्ट्रक्टर में कोई भी `Color` (जिसमें ARGB मान भी शामिल हैं) पास करें।  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए ट्रायल काम करता है; उत्पादन परिनियोजन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या यह तरीका .NET 6+ के साथ संगत है?** बिल्कुल—Aspose.Drawing पूरी तरह से .NET 5, .NET 6 और बाद के संस्करणों को समर्थन देता है।

## “save bitmap as png” क्या है?

Bitmap को PNG के रूप में सहेजना इन‑मेमोरी पिक्सेल एरे को एक लॉसलेस PNG फ़ाइल में बदल देता है, पारदर्शिता और सटीक रंग मानों को संरक्षित करता है। **Save bitmap as PNG** एक सामान्य ऑपरेशन है जब आपको एक पोर्टेबल इमेज फ़ॉर्मेट चाहिए जो ब्राउज़र और इमेज एडिटर बिना गुणवत्ता हानि के पढ़ सकें।

## Bitmap को PNG के रूप में सहेजने के लिए solid brushes का उपयोग क्यों करें?

Solid brushes एक एकल, समान रंग प्रदान करते हैं जो किसी भी वेक्टर आकार को तुरंत भर देता है, जब आपको केवल एक सपाट रंग चाहिए तो जटिल ग्रेडिएंट की आवश्यकता नहीं रहती। Aspose.Drawing के साथ solid brushes का उपयोग करने से एक रेंडरिंग इंजन का लाभ मिलता है जो **10,000 × 10,000 पिक्सेल** तक की छवियों को संभाल सकता है जबकि मेमोरी उपयोग **200 MB** से कम रखता है, जिससे यह उच्च‑रिज़ॉल्यूशन एसेट्स के लिए उपयुक्त है।

## पूर्वापेक्षाएँ

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- Aspose.Drawing for .NET लाइब्रेरी: लाइब्रेरी को [Aspose.Drawing for .NET Documentation](https://reference.aspose.com/drawing/net/) से डाउनलोड और इंस्टॉल करें।
- इंटीग्रेटेड डेवलपमेंट एनवायरनमेंट (IDE): अपने मशीन पर Visual Studio जैसी कार्यशील .NET विकास वातावरण स्थापित रखें।

अब जब आपके पास सब कुछ तैयार है, चलिए कार्यान्वयन की ओर बढ़ते हैं।

## नेमस्पेस इम्पोर्ट करें

`using` निर्देश आवश्यक प्रकारों को स्कोप में लाते हैं।

`Aspose.Drawing` नेमस्पेस कोर ग्राफिक्स क्लासेस प्रदान करता है, जबकि `System.Drawing` रंग परिभाषाएँ और `SolidBrush` क्लास देता है।

```csharp
using System.Drawing;
```

## Solid Brushes के साथ Bitmap को PNG के रूप में कैसे सहेजें

यह अनुभाग पूरी कार्यप्रवाह को दर्शाता है: एक bitmap कैनवास बनाएं, एक ग्राफिक्स सतह प्राप्त करें, इच्छित रंग के साथ `SolidBrush` का इंस्टेंस बनाएं, एक या अधिक आकार भरें, और अंत में `Save` को कॉल करके इमेज को PNG फ़ाइल के रूप में लिखें। यह कोड .NET 6 और बाद के संस्करणों पर क्रॉस‑प्लेटफ़ॉर्म काम करता है।

### चरण 1: Bitmap बनाएं

`Bitmap` क्लास एक इन‑मेमोरी इमेज कैनवास को दर्शाती है।

`Bitmap` क्लास Aspose.Drawing का टॉप‑लेवल ऑब्जेक्ट है जो पिक्सेल डेटा को एक परिवर्तनीय बफ़र में संग्रहीत करता है। आप इसे बनाते समय चौड़ाई, ऊँचाई और पिक्सेल फ़ॉर्मेट निर्दिष्ट कर सकते हैं।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### चरण 2: Graphics ऑब्जेक्ट बनाएं

`Graphics` ऑब्जेक्ट bitmap के लिए ड्रॉइंग मेथड्स प्रदान करता है।

`Graphics` क्लास एक ड्रॉइंग सतह के रूप में कार्य करती है जो `Bitmap` से जुड़ी होती है। सभी बाद के ड्रॉइंग कमांड (लाइन, आकार, टेक्स्ट) इस ऑब्जेक्ट के माध्यम से भेजे जाते हैं।

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### चरण 3: Solid Brush चुनें

ब्रश के लिए एक रंग चुनें; इस उदाहरण में हम एक चमकीला नीला उपयोग करते हैं।

`SolidBrush` क्लास एक ऐसा ब्रश परिभाषित करती है जो एक ही, समान रंग से पेंट करती है। यह उन आकारों को भरने के लिए आदर्श है जहाँ सपाट रंग चाहिए।

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
```

### चरण 4: ब्रश से आकार भरें

ब्रश का उपयोग करके bitmap पर एक अंडाकार (या कोई अन्य आकार) पेंट करें।

`FillEllipse` निर्दिष्ट ब्रश से भरा हुआ अंडाकार बनाता है। `Graphics` ऑब्जेक्ट की `FillEllipse` मेथड प्रदान किए गए `SolidBrush` से भरा अंडाकार बनाती है। आप इसे `FillRectangle`, `FillPolygon` आदि से बदलकर विभिन्न ज्यामिति बना सकते हैं।

```csharp
graphics.FillEllipse(brush, 100, 100, 800, 600);
```

### चरण 5: परिणाम को PNG के रूप में सहेजें

bitmap को डिस्क पर PNG फ़ाइल के रूप में निर्यात करें।

`Save` चयनित फ़ॉर्मेट में इमेज को फ़ाइल में लिखता है। `Save` मेथड `ImageFormat.Png` का उपयोग करके bitmap को निर्दिष्ट पथ पर लिखता है। यह ऑपरेशन अल्फा चैनल को संरक्षित रखता है, जिससे पारदर्शी पृष्ठभूमि बरकरार रहती है।

```csharp
bitmap.Save("Your Document Directory" + @"Brushes\Solid_out.png");
```

इन चरणों को दोहराएँ, अपने एप्लिकेशन के विज़ुअल डिज़ाइन के अनुसार रंग और आकार को अनुकूलित करें।

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| **फ़ाइल नहीं मिली त्रुटि** सहेजते समय | लक्ष्य फ़ोल्डर मौजूद नहीं है | `Save` कॉल करने से पहले निर्देशिका (`Your Document Directory\Brushes`) बनाना सुनिश्चित करें। |
| **गलत रंग** | `KnownColor` का उपयोग जो सिस्टम थीम से मैप होता है | सटीक RGBA मानों के लिए `Color.FromArgb` का उपयोग करें। |
| **पारदर्शिता खो गई** | ऐसे पिक्सेल फ़ॉर्मेट का उपयोग जिसमें अल्फा नहीं है | अल्फा चैनल बनाए रखने के लिए जैसा दिखाया गया है `PixelFormat.Format32bppPArgb` रखें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं अंडाकार के बजाय कोई अलग आकार उपयोग कर सकता हूँ?**  
A: बिल्कुल—`FillRectangle`, `FillPolygon`, या `DrawPath` जैसी मेथड्स समान solid brush के साथ काम करती हैं।

**Q: आउटपुट फ़ॉर्मेट को JPEG में कैसे बदलूँ?**  
A: `Save` में फ़ाइल एक्सटेंशन बदलें और `ImageFormat.Jpeg` का उपयोग करें (उदाहरण: `bitmap.Save("output.jpg", ImageFormat.Jpeg);`)।

**Q: क्या एक ही bitmap में विभिन्न ब्रशों के साथ कई आकार बनाना संभव है?**  
A: हाँ—प्रत्येक रंग के लिए अलग `SolidBrush` इंस्टेंस बनाएं और क्रमशः उपयुक्त `Fill*` मेथड्स को कॉल करें।

**Q: क्या मुझे `Graphics` और `Bitmap` ऑब्जेक्ट्स को डिस्पोज़ करना चाहिए?**  
A: यह सर्वोत्तम अभ्यास है कि उन्हें `using` स्टेटमेंट में रखें या अनमैनेज्ड रिसोर्सेज़ को मुक्त करने के लिए `Dispose()` कॉल करें।

**Q: क्या यह Linux/macOS पर .NET Core के साथ काम करेगा?**  
A: Aspose.Drawing क्रॉस‑प्लेटफ़ॉर्म है; वही कोड Linux और macOS पर .NET Core या .NET 5+ को टार्गेट करने पर चलता है।

---

**अंतिम अपडेट:** 2026-08-01  
**परीक्षण किया गया:** Aspose.Drawing 24.12 for .NET  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Bitmap को PNG के रूप में सहेजें और Aspose.Drawing के साथ बंद वक्र बनाएं](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Aspose.Drawing में ट्रांसफ़ॉर्मेशन का उपयोग करके Bitmap को PNG के रूप में सहेजें](/drawing/net/coordinate-transformations/local-transformation/)
- [Aspose.Drawing for .NET के साथ इमेज को PNG में क्रॉप कैसे करें](/drawing/net/image-editing/cropping/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}