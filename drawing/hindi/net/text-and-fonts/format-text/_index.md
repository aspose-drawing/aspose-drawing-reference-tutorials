---
date: 2026-02-25
description: Aspose.Drawing for .NET में टेक्स्ट अलाइनमेंट कैसे सेट करें और इमेज में
  टेक्स्ट जोड़ें, सीखें। उदाहरणों के साथ चरण‑दर‑चरण गाइड।
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET के साथ टेक्स्ट संरेखण सेट करें
url: /hi/net/text-and-fonts/format-text/
weight: 11
---

 sure to keep markdown tables with pipes.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing में टेक्स्ट एलाइनमेंट सेट करें

## परिचय

जब आपके .NET एप्लिकेशन में **टेक्स्ट एलाइनमेंट सेट करने** और टेक्स्ट को फॉर्मेट करने की बात आती है, तो Aspose.Drawing वह लाइब्रेरी है जिसे डेवलपर्स सटीकता, प्रदर्शन और समृद्ध API सतह के लिए चुनते हैं। चाहे आप एक रिपोर्टिंग इंजन, एक डायनामिक बैज जेनरेटर, या कोई भी ग्राफ़िक‑इंटेंसिव समाधान बना रहे हों, शेप्स के अंदर टेक्स्ट को कैसे लाइन अप किया जाए, इसे नियंत्रित करने से आपका आउटपुट पॉलिश्ड और प्रोफेशनल दिखता है। इस ट्यूटोरियल में हम पूरी प्रक्रिया को देखेंगे—बिटमैप कैनवास बनाने से लेकर टेक्स्ट के साथ आयत ड्रॉ करने, ओवरफ़्लो को हैंडल करने, और अंत में इमेज को सेव करने तक।

## त्वरित उत्तर
- **“set text alignment” का क्या अर्थ है?** यह निर्धारित करता है कि टेक्स्ट को ड्रॉइंग आयत के भीतर क्षैतिज और लंबवत कैसे स्थित किया जाता है।  
- **कौन सा क्लास एलाइनमेंट को नियंत्रित करता है?** `StringFormat` आपको `Alignment` और `LineAlignment` सेट करने देता है।  
- **क्या मैं स्ट्रिंग और आयत को साथ में ड्रॉ कर सकता हूँ?** हाँ—`Graphics.DrawRectangle` के बाद `Graphics.DrawString` का उपयोग करें।  
- **टेक्स्ट ओवरफ़्लो को कैसे रोकें?** आयत का आकार समायोजित करें या टेक्स्ट को मैन्युअल रूप से कई लाइनों में विभाजित करें।  
- **उत्पादन के लिए क्या लाइसेंस चाहिए?** गैर‑मूल्यांकन उपयोग के लिए एक व्यावसायिक Aspose.Drawing लाइसेंस आवश्यक है।

## Aspose.Drawing में **set text alignment** क्या है?

`set text alignment` का अर्थ है किसी `Rectangle` या किसी भी ड्रॉइंग क्षेत्र के अंदर टेक्स्ट की क्षैतिज (`StringAlignment`) और लंबवत (`LineAlignment`) पोजिशनिंग को कॉन्फ़िगर करना। इन सेटिंग्स को समायोजित करके आप नियंत्रित करते हैं कि टेक्स्ट बाएँ‑एलाइन, सेंटर‑एलाइन, दाएँ‑एलाइन, ऊपर‑एलाइन, मध्य‑एलाइन, या नीचे‑एलाइन दिखे।

## टेक्स्ट एलाइनमेंट के लिए Aspose.Drawing क्यों उपयोग करें?

- **पूर्ण .NET संगतता** – .NET Framework, .NET Core, और .NET 5/6+ के साथ काम करता है।  
- **पिक्सेल‑परफेक्ट रेंडरिंग** – एंटी‑एलियासिंग और हाई‑DPI सपोर्ट बॉक्स से बाहर।  
- **कोई GDI+ सीमाएँ नहीं** – `System.Drawing.Common` के विपरीत, Aspose.Drawing लिनक्स कंटेनरों में बिना नेटिव डिपेंडेंसी के चलता है।  
- **समृद्ध स्टाइलिंग** – फ़ॉन्ट, ब्रश, पेन, और कस्टम `StringFormat` ऑब्जेक्ट्स को मिलाकर परिष्कृत लेआउट बनाएं।

## पूर्वापेक्षाएँ

1. **Aspose.Drawing Library** – इसे [here](https://releases.aspose.com/drawing/net/) से डाउनलोड करें।  
2. **डेवलपमेंट एनवायरनमेंट** – Visual Studio 2022 (या कोई भी C# IDE)।  
3. **बेसिक .NET ज्ञान** – आपको C# प्रोजेक्ट्स और NuGet पैकेजेज़ के साथ सहज होना चाहिए।

## नेमस्पेस आयात करें

शुरू करने के लिए, आवश्यक नेमस्पेस को स्कोप में लाएँ। ये आपको ग्राफ़िक्स, टेक्स्ट रेंडरिंग, और ड्रॉइंग प्रिमिटिव्स तक पहुँच प्रदान करेंगे।

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## चरण 1: बिटमैप और ग्राफिक्स ऑब्जेक्ट बनाएं  

बिटमैप बनाना एक कैनवास प्रदान करता है जिस पर आप ड्रॉ कर सकते हैं। `Graphics` ऑब्जेक्ट ड्रॉइंग सतह है, और हम `TextRenderingHint` के साथ हाई‑क्वालिटी टेक्स्ट रेंडरिंग सक्षम करते हैं।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## चरण 2: **StringFormat** और स्टाइलिंग परिभाषित करें  

यहाँ हम `StringFormat` इंस्टेंस को कॉन्फ़िगर करके **set text alignment** सेट करते हैं। हम ब्रश, पेन, और फ़ॉन्ट भी तैयार करते हैं जो स्ट्रिंग ड्रॉ करने के समय उपयोग होगा।

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## चरण 3: टेक्स्ट बनाएं और फॉर्मेट करें – **how to draw string** और **draw rectangle with text**

हम टेक्स्ट तैयार करते हैं, वह आयत परिभाषित करते हैं जो इसे समाहित करेगा, और फिर आयत की बॉर्डर और स्वयं स्ट्रिंग दोनों को ड्रॉ करते हैं।

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### टेक्स्ट ओवरफ़्लो को कैसे संभालें

यदि प्रदान किया गया `text` आयत की सीमाओं से अधिक हो जाता है, तो आपके पास दो सामान्य विकल्प हैं:

1. **आयत का आकार बदलें** – `rectangle.Width` या `rectangle.Height` बढ़ाएँ।  
2. **टेक्स्ट को विभाजित करें** – स्ट्रिंग को उन लाइनों में तोड़ें जो फिट हों, फिर प्रत्येक लाइन के लिए समायोजित Y‑कोऑर्डिनेट्स के साथ `DrawString` कॉल करें।

## चरण 4: आउटपुट सहेजें – **add text to image**

अंत में, बिटमैप को डिस्क पर लिखें। यह चरण एक ही कॉल में **add text to image** को दर्शाता है।

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **टेक्स्ट धुंधला दिखता है** | सुनिश्चित करें कि `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` सेट किया गया है। |
| **टेक्स्ट कट रहा है** | आयत के आकार को बढ़ाएँ या स्ट्रिंग आकार मापकर (`Graphics.MeasureString`) शब्द‑रैप लॉजिक सक्षम करें। |
| **फ़ॉन्ट नहीं मिला** | जाँचें कि फ़ॉन्ट होस्ट मशीन पर स्थापित है या `PrivateFontCollection` का उपयोग करके निजी फ़ॉन्ट एम्बेड करें। |
| **अनपेक्षित रंग** | ब्रश और पेन के रंगों को दोबारा जांचें; याद रखें कि `Color.FromKnownColor` सिस्टम‑परिभाषित रंगों का उपयोग करता है। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Drawing सभी .NET संस्करणों के साथ संगत है?

A1: हाँ, Aspose.Drawing विभिन्न .NET संस्करणों के साथ संगत होने के लिए डिज़ाइन किया गया है, जिससे डेवलपर्स को लचीलापन मिलता है।

### Q2: क्या मैं फ़ॉन्ट स्टाइल को और कस्टमाइज़ कर सकता हूँ?

A2: बिल्कुल! इच्छित फ़ॉन्ट साइज, स्टाइल, और फ़ैमिली प्राप्त करने के लिए `Font` ऑब्जेक्ट पैरामीटर को समायोजित करें।

### Q3: परिभाषित आयत के भीतर टेक्स्ट ओवरफ़्लो को कैसे संभालें?

A3: आप आयत के आकार को समायोजित करके या लंबी टेक्स्ट को संभालने के लिए कस्टम लॉजिक लागू करके टेक्स्ट ओवरफ़्लो को प्रबंधित कर सकते हैं।

### Q4: क्या Aspose.Drawing में अन्य फॉर्मेटिंग विकल्प उपलब्ध हैं?

A4: हाँ, Aspose.Drawing ग्राफ़िक मैनिपुलेशन के लिए व्यापक टूल्स प्रदान करता है, जिसमें टेक्स्ट, शैप्स, और अधिक के विभिन्न फॉर्मेटिंग विकल्प शामिल हैं।

### Q5: Aspose.Drawing के लिए अतिरिक्त समर्थन कहाँ मिल सकता है?

A5: समुदाय समर्थन और चर्चाओं के लिए Aspose.Drawing फ़ोरम [here](https://forum.aspose.com/c/drawing/44) देखें।

**अतिरिक्त Q&A**

**Q: मैं बिना किसी आयत के स्ट्रिंग कैसे ड्रॉ करूँ?**  
A: `DrawRectangle` कॉल को छोड़ दें और `Graphics.DrawString` को इच्छित `PointF` लोकेशन पास करें।

**Q: क्या मैं एलाइनमेंट बनाए रखते हुए टेक्स्ट को घुमा सकता हूँ?**  
A: हाँ—ड्रॉइंग से पहले `Graphics` ऑब्जेक्ट पर `Matrix` ट्रांसफ़ॉर्मेशन लागू करें, फिर बाद में इसे रीसेट करें।

**Q: क्या इमेज को PNG के बजाय JPEG के रूप में एक्सपोर्ट करना संभव है?**  
A: `bitmap.Save` में फ़ाइल एक्सटेंशन बदलें और वैकल्पिक रूप से `ImageFormat.Jpeg` निर्दिष्ट करें।

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}