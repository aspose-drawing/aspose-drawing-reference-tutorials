---
date: 2026-07-17
description: Aspose.Drawing for .NET में टेक्स्ट अलाइनमेंट सेट करके टेक्स्ट ओवरफ़्लो
  को रोकना और इमेज में टेक्स्ट जोड़ना सीखें। उदाहरणों के साथ चरण-दर-चरण गाइड।
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Aspose.Drawing for .NET के साथ टेक्स्ट अलाइनमेंट सेट करें
og_description: Aspose.Drawing for .NET में टेक्स्ट अलाइनमेंट सेट करके टेक्स्ट ओवरफ़्लो
  को रोकें। इमेज पर स्ट्रिंग ड्रॉ करना, आयत में टेक्स्ट को केंद्रित करना, और System.Drawing
  को बदलना सीखें।
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: टेक्स्ट ओवरफ़्लो को रोकें – Aspose.Drawing for .NET के साथ टेक्स्ट अलाइनमेंट
  सेट करें
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: टेक्स्ट ओवरफ़्लो को रोकें – Aspose.Drawing for .NET के साथ टेक्स्ट अलाइनमेंट
  सेट करें
url: /hi/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# पाठ ओवरफ़्लो को रोकें – Aspose.Drawing के साथ पाठ संरेखण सेट करें

## परिचय

जब आपको .NET में ग्राफ़िक्स रेंडर करते समय **पाठ ओवरफ़्लो को रोकने** की आवश्यकता होती है, Aspose.Drawing आपको पाठ की स्थिति, संरेखण और रैपिंग पर सूक्ष्म नियंत्रण देता है। चाहे आप बैज जेनरेटर, डायनेमिक रिपोर्ट, या किसी भी इमेज‑आधारित आउटपुट बना रहे हों, पाठ संरेखण में निपुणता यह सुनिश्चित करती है कि आपका पाठ इच्छित आयत के भीतर रहे और परिष्कृत दिखे। इस गाइड में हम एक बिटमैप कैनवास बनाना, `StringFormat` को कॉन्फ़िगर करना, केंद्रित पाठ के साथ आयत खींचना, ओवरफ़्लो को संभालना, और अंत में इमेज को सहेजना दिखाएंगे।

## त्वरित उत्तर
- **“पाठ संरेखण सेट करना” क्या मतलब है?** यह निर्धारित करता है कि पाठ को एक ड्राइंग आयत के भीतर क्षैतिज और लंबवत कैसे स्थित किया जाता है।  
- **कौन सा क्लास संरेखण को नियंत्रित करता है?** `StringFormat` आपको `Alignment` और `LineAlignment` सेट करने देता है।  
- **क्या मैं एक स्ट्रिंग और आयत को साथ में खींच सकता हूँ?** हाँ—`Graphics.DrawRectangle` का उपयोग करें और फिर `Graphics.DrawString`।  
- **मैं पाठ ओवरफ़्लो को कैसे रोकूँ?** आयत का आकार समायोजित करें या पाठ को कई लाइनों में मैन्युअल रूप से विभाजित करें।  
- **उत्पादन के लिए मुझे लाइसेंस की आवश्यकता है क्या?** गैर‑इवैल्यूएशन उपयोग के लिए एक व्यावसायिक Aspose.Drawing लाइसेंस आवश्यक है।

## Aspose.Drawing में **set text alignment** क्या है?

`set text alignment` क्षैतिज (`StringAlignment`) और लंबवत (`LineAlignment`) पाठ की स्थिति को एक `Rectangle` या ड्राइंग क्षेत्र के भीतर कॉन्फ़िगर करता है। इन गुणों को समायोजित करके आप नियंत्रित कर सकते हैं कि पाठ बाएँ‑संरेखित, केंद्रित, दाएँ‑संरेखित, ऊपर‑संरेखित, मध्य‑संरेखित, या नीचे‑संरेखित दिखे, जिससे Aspose.Drawing के साथ उत्पन्न ग्राफ़िक्स, बैज और रिपोर्ट में सटीक लेआउट संभव हो जाता है।

## पाठ संरेखण के लिए Aspose.Drawing का उपयोग क्यों करें?

Aspose.Drawing `System.Drawing.Common` की GDI+ सीमाओं को समाप्त करता है। यह **5 प्रमुख .NET रनटाइम** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6, और .NET 7 – को सपोर्ट करता है और **4000 × 4000 px** (≈ 100 MB) तक की इमेज रेंडर कर सकता है बिना मेमोरी समाप्त किए। एंटी‑एलियासिंग, हाई‑DPI स्केलिंग, और पूर्ण Linux कंटेनर संगतता आपको किसी भी डिप्लॉयमेंट परिदृश्य में पिक्सेल‑परफेक्ट ग्राफ़िक्स उत्पन्न करने देती है।

## पूर्वापेक्षाएँ

1. **Aspose.Drawing लाइब्रेरी** – इसे [यहाँ](https://releases.aspose.com/drawing/net/) डाउनलोड करें।  
2. **डेवलपमेंट एनवायरनमेंट** – Visual Studio 2022 (या कोई भी C# IDE)।  
3. **बेसिक .NET ज्ञान** – आपको C# प्रोजेक्ट्स और NuGet पैकेजों के साथ सहज होना चाहिए।

## नेमस्पेसेस आयात करें

शुरू करने के लिए, आवश्यक नेमस्पेसेस को स्कोप में लाएँ। ये आपको ग्राफ़िक्स, टेक्स्ट रेंडरिंग, और ड्राइंग प्रिमिटिव्स तक पहुँच प्रदान करते हैं।

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Aspose.Drawing के साथ पाठ ओवरफ़्लो को कैसे रोकें?

Bitmap एक क्लास है जो मेमोरी में संग्रहीत इमेज को दर्शाता है, जबकि `RectangleF` ड्राइंग के लिए फ्लोटिंग‑पॉइंट आयत क्षेत्र को परिभाषित करता है। `StringFormat` को `Trimming` को `StringTrimming.EllipsisCharacter` पर सेट करके उपयोग करने से अतिरिक्त अक्षर स्वचालित रूप से एलिप्सिस से बदल जाते हैं, जिससे पाठ कभी भी आयत की सीमाओं से बाहर नहीं जाता। पहले स्ट्रिंग को मापने से आप तय कर सकते हैं कि आयत को छोटा करना है या पाठ को कई लाइनों में विभाजित करना है, जिससे बिना ओवरफ़्लो के साफ़ लेआउट सुनिश्चित होता है।

अपना bitmap लोड करें, उपयुक्त आकार का `RectangleF` परिभाषित करें, और `StringFormat` को `Trimming` को `StringTrimming.EllipsisCharacter` पर सेट करके उपयोग करें ताकि अतिरिक्त अक्षर स्वचालित रूप से कट जाएँ। पूर्ण नियंत्रण के लिए, `Graphics.MeasureString` से स्ट्रिंग को मापें और ड्रॉ करने से पहले आयत को छोटा करें या पाठ को लाइनों में विभाजित करें। यह तरीका सुनिश्चित करता है कि कोई भी अक्षर दृश्य सीमाओं के बाहर न गिरे।

## चरण 1: Bitmap और Graphics ऑब्जेक्ट बनाएं  

Bitmap मेमोरी में मौजूद इमेज को दर्शाता है, जबकि Graphics उस bitmap के लिए ड्राइंग मेथड्स प्रदान करता है। एक bitmap बनाना एक कैनवास प्रदान करता है जिस पर आप ड्रॉ कर सकते हैं। `Graphics` ऑब्जेक्ट ड्राइंग सतह है, और हम `TextRenderingHint` के साथ उच्च‑गुणवत्ता वाला टेक्स्ट रेंडरिंग सक्षम करते हैं।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## चरण 2: **StringFormat** और स्टाइलिंग परिभाषित करें  

StringFormat टेक्स्ट लेआउट विकल्पों जैसे संरेखण, लाइन स्पेसिंग, और ट्रिमिंग को निर्दिष्ट करता है। यहाँ हम `StringFormat` इंस्टेंस को कॉन्फ़िगर करके **पाठ संरेखण सेट** करते हैं। हम ब्रश, पेन, और फ़ॉन्ट भी तैयार करते हैं जो स्ट्रिंग ड्रॉ करने पर उपयोग होगा।

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## चरण 3: टेक्स्ट बनाएं और फ़ॉर्मेट करें – **how to draw string** और **draw rectangle with text**

Graphics.DrawString कैनवास पर टेक्स्ट रेंडर करता है, और Graphics.DrawRectangle एक आयत आकार बनाता है। हम टेक्स्ट बनाते हैं, वह आयत परिभाषित करते हैं जो इसे समाहित करेगा, और फिर आयत की बॉर्डर और स्वयं स्ट्रिंग दोनों को ड्रॉ करते हैं।

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### पाठ ओवरफ़्लो को कैसे संभालें

यदि प्रदान किया गया `text` आयत की सीमाओं से अधिक हो जाता है, तो आपके पास दो सामान्य विकल्प हैं:

1. **आयत का आकार बदलें** – `rectangle.Width` या `rectangle.Height` बढ़ाएँ।  
2. **पाठ को विभाजित करें** – स्ट्रिंग को फिट होने वाली लाइनों में तोड़ें, फिर प्रत्येक लाइन के लिए समायोजित Y‑कोऑर्डिनेट्स के साथ `DrawString` कॉल करें।

## Aspose.Drawing का उपयोग करके इमेज पर स्ट्रिंग कैसे ड्रॉ करें?

Graphics.DrawString निर्दिष्ट फ़ॉन्ट और फ़ॉर्मेटिंग विकल्पों का उपयोग करके टेक्स्ट ड्रॉ करता है। अपने bitmap से एक `Graphics` ऑब्जेक्ट बनाएं, फिर तैयार `StringFormat` के साथ `DrawString` कॉल करें। यह एकल कॉल टेक्स्ट को ठीक उसी स्थान पर रेंडर करता है जहाँ आप चाहते हैं, संरेखण, ट्रिमिंग, और लागू किए गए किसी भी ट्रांसफ़ॉर्मेशन मैट्रिक्स का सम्मान करता है। उच्च‑गुणवत्ता वाला रेंडरिंग हिंट जोड़ने से आउटपुट हाई‑DPI डिस्प्ले पर भी स्पष्ट रहता है।

## आयत में टेक्स्ट को केंद्र में कैसे रखें?

StringAlignment लेआउट आयत के भीतर टेक्स्ट के क्षैतिज संरेखण को निर्धारित करता है। `stringFormat.Alignment = StringAlignment.Center` और `stringFormat.LineAlignment = StringAlignment.Center` सेट करें। यह टेक्स्ट को आयत के भीतर क्षैतिज और लंबवत दोनों रूप से केंद्रित करता है, जिससे यह बैज, बटन, या लेबल ओवरले के लिए आदर्श बन जाता है। केंद्रित प्लेसमेंट विभिन्न इमेज साइज और DPI सेटिंग्स में लगातार काम करता है, एक संतुलित दृश्य रूप प्रदान करता है।

## वर्टिकल टेक्स्ट संरेखण कैसे प्राप्त करें?

LineAlignment आयत के भीतर टेक्स्ट की लंबवत स्थिति को नियंत्रित करता है। `stringFormat.LineAlignment` को मान `StringAlignment.Near`, `Center`, या `Far` के साथ उपयोग करके टेक्स्ट को आयत के शीर्ष, मध्य, या नीचे स्थित करें। यदि आपको टेक्स्ट को घुमाते समय वर्टिकल संरेखण बनाए रखना है तो इसे `Graphics.TranslateTransform` के साथ संयोजित करें। लाइन अलाइनमेंट को समायोजित करने से यह सुनिश्चित होता है कि मल्टी‑लाइन ब्लॉक्स ठीक उसी स्थान पर संरेखित हों जहाँ आप अपेक्षा करते हैं, यहाँ तक कि ट्रांसफ़ॉर्मेशन के बाद भी।

## चरण 4: आउटपुट सहेजें – **add text to image**

अंत में, bitmap को डिस्क पर लिखें। यह चरण एक ही कॉल में **add text to image** को दर्शाता है।

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **Text appears blurry** | सुनिश्चित करें कि `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` सेट है। |
| **Text is clipped** | आयत का आकार बढ़ाएँ या स्ट्रिंग आकार मापकर (`Graphics.MeasureString`) शब्द‑रैप लॉजिक सक्षम करें। |
| **Font not found** | जांचें कि फ़ॉन्ट होस्ट मशीन पर स्थापित है या `PrivateFontCollection` का उपयोग करके प्राइवेट फ़ॉन्ट एम्बेड करें। |
| **Unexpected colors** | ब्रश और पेन के रंगों को दोबारा जांचें; याद रखें कि `Color.FromKnownColor` सिस्टम‑परिभाषित रंगों का उपयोग करता है। |

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या Aspose.Drawing सभी .NET संस्करणों के साथ संगत है?**  
A1: हाँ, Aspose.Drawing को विभिन्न .NET संस्करणों के साथ संगत रहने के लिए डिज़ाइन किया गया है, जिससे डेवलपर्स को लचीलापन मिलता है।

**Q2: क्या मैं फ़ॉन्ट स्टाइल को और कस्टमाइज़ कर सकता हूँ?**  
A2: बिल्कुल! इच्छित फ़ॉन्ट आकार, स्टाइल, और फ़ैमिली प्राप्त करने के लिए `Font` ऑब्जेक्ट पैरामीटर को समायोजित करें।

**Q3: परिभाषित आयत के भीतर टेक्स्ट ओवरफ़्लो को कैसे संभालूँ?**  
A3: आप आयत के आकार को समायोजित करके या लंबी टेक्स्ट को संभालने के लिए कस्टम लॉजिक लागू करके टेक्स्ट ओवरफ़्लो को प्रबंधित कर सकते हैं।

**Q4: क्या Aspose.Drawing में अन्य फ़ॉर्मेटिंग विकल्प उपलब्ध हैं?**  
A4: हाँ, Aspose.Drawing ग्राफ़िक मैनिपुलेशन के लिए व्यापक टूल्स का सेट प्रदान करता है, जिसमें टेक्स्ट, शैप्स और अधिक के विभिन्न फ़ॉर्मेटिंग विकल्प शामिल हैं।

**Q5: Aspose.Drawing के लिए अतिरिक्त समर्थन कहाँ मिल सकता है?**  
A5: समुदाय समर्थन और चर्चाओं के लिए Aspose.Drawing फ़ोरम [यहाँ](https://forum.aspose.com/c/drawing/44) देखें।

**अतिरिक्त प्रश्नोत्तर**

**Q: बिना किसी आयत के स्ट्रिंग कैसे ड्रॉ करूँ?**  
A: `DrawRectangle` कॉल को छोड़ दें और इच्छित `PointF` स्थान को `Graphics.DrawString` में पास करें।

**Q: क्या मैं संरेखण बनाए रखते हुए टेक्स्ट को घुमा सकता हूँ?**  
A: हाँ—ड्रॉ करने से पहले `Graphics` ऑब्जेक्ट पर `Matrix` ट्रांसफ़ॉर्मेशन लागू करें, फिर बाद में इसे रीसेट करें।

**Q: क्या इमेज को PNG के बजाय JPEG के रूप में एक्सपोर्ट करना संभव है?**  
A: बस `bitmap.Save` में फ़ाइल एक्सटेंशन बदलें और वैकल्पिक रूप से `ImageFormat.Jpeg` निर्दिष्ट करें।

---

**अंतिम अपडेट:** 2026-07-17  
**परीक्षण किया गया:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Aspose.Drawing के साथ .NET के लिए टेक्स्ट कैसे ड्रॉ करें](/drawing/net/text-and-fonts/draw-text/)
- [Aspose.Drawing में इमेज पर टेक्स्ट जोड़ना](/drawing/net/use-cases/text-on-image/)
- [Aspose.Drawing के साथ .NET के लिए टेक्स्ट और फ़ॉन्ट कैसे ड्रॉ करें](/drawing/net/text-and-fonts/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}