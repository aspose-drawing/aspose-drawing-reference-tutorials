---
date: 2026-07-22
description: Aspose.Drawing के साथ bitmap को PNG के रूप में सहेजना और छवि को JPEG
  में निर्यात करना सीखें। चरण‑दर‑चरण गाइड में drawing paths, इमेज बनाना, और फ़ॉर्मेट
  निर्यात दिखाए गए हैं।
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: Aspose.Drawing में Drawing Paths
og_description: Aspose.Drawing for .NET का उपयोग करके bitmap को PNG के रूप में सहेजें
  और छवि को JPEG में निर्यात करें। इस ट्यूटोरियल का पालन करें ताकि complex paths को
  ड्रॉ किया जा सके, उच्च‑गुणवत्ता वाली इमेज बनाई जा सके, और कई फ़ॉर्मेट आउटपुट किए
  जा सकें।
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: Bitmap को PNG के रूप में सहेजें – Aspose.Drawing के साथ Drawing Paths
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: Bitmap को PNG के रूप में सहेजें – Aspose.Drawing में GraphicsPath का उपयोग
  करके
url: /hi/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing में पाथ ड्रॉ करना

## GraphicsPath का उपयोग कैसे करें – परिचय

**Save bitmap as PNG** अक्सर पहला कदम होता है जब आपको आगे की प्रोसेसिंग या प्रकाशन के लिए एक लॉसलेस इमेज चाहिए। इस ट्यूटोरियल में आप सीखेंगे कि `GraphicsPath` के साथ जटिल वेक्टर पाथ कैसे ड्रॉ करें, उन्हें बिटमैप पर रेंडर करें, और फिर **save bitmap as PNG** या यहाँ तक कि **export image to JPEG** भी करें। चाहे आप रिपोर्टिंग इंजन, कस्टम चार्टिंग लाइब्रेरी बना रहे हों, या सिर्फ डायनामिक ग्राफ़िक्स जेनरेट करना चाहते हों, Aspose.Drawing आपको एक पूरी तरह मैनेज्ड, क्रॉस‑प्लेटफ़ॉर्म API देता है जो System.Drawing.Common को रिप्लेस करता है।

## त्वरित उत्तर
- **GraphicsPath से आप क्या ड्रॉ कर सकते हैं?** Lines, rectangles, ellipses, curves, and custom shapes.  
- **क्या मुझे लाइसेंस चाहिए?** ट्रायल मुफ्त है; प्रोडक्शन के लिए कमर्शियल लाइसेंस आवश्यक है।  
- **कौन से .NET संस्करण समर्थित हैं?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **क्या System.Drawing.Common आवश्यक है?** नहीं, Aspose.Drawing स्वतंत्र रूप से काम करता है।  
- **क्या मैं विभिन्न फॉर्मैट में सहेज सकता हूँ?** हाँ – PNG, JPEG, BMP, GIF, और अधिक।

## GraphicsPath क्या है?
`GraphicsPath` Aspose.Drawing का वेक्टर कंटेनर है जो लाइन्स, आर्क्स, और कर्व्स जैसे ड्रॉइंग प्रिमिटिव्स की श्रृंखला को एक ही ऑब्जेक्ट में स्टोर करता है। इन प्रिमिटिव्स को ग्रुप करके आप ट्रांसफ़ॉर्मेशन, फ़िल रूल्स, और स्ट्रोक सेटिंग्स को समान रूप से लागू कर सकते हैं, जिससे जटिल ग्राफ़िक्स बनाना आसान हो जाता है और विभिन्न आउटपुट फॉर्मैट्स में रेंडरिंग सुसंगत रहती है।

## Aspose.Drawing के साथ GraphicsPath का उपयोग क्यों करें?
GraphicsPath को Aspose.Drawing के साथ उपयोग करने से आपको सटीक, लचीली, और हाई‑परफ़ॉर्मेंस वेक्टर ड्रॉइंग क्षमताएँ मिलती हैं। यह आपको जटिल शैप्स बनाने, ट्रांसफ़ॉर्मेशन लागू करने, और उन्हें कुशलता से रेंडर करने की सुविधा देता है, जबकि क्रॉस‑प्लेटफ़ॉर्म कंसिस्टेंसी बनाए रखता है और बड़े‑पैमाने पर इमेज प्रोसेसिंग को सपोर्ट करता है। साथ ही, यह अन्य .NET लाइब्रेरीज़ के साथ सहजता से इंटीग्रेट होता है, जिससे आप एक ही एप्लिकेशन में रास्टर और वेक्टर वर्कफ़्लो को मिलाकर काम कर सकते हैं।

- **Precision:** 50+ वेक्टर प्रिमिटिव्स को सब‑पिक्सेल सटीकता के साथ हैंडल करता है, यह सुनिश्चित करता है कि जब आप **save bitmap as PNG** करें तो आउटपुट किसी भी रिज़ॉल्यूशन पर तेज़ रहे।  
- **Flexibility:** लाइन्स, आर्क्स, और Bezier कर्व्स को एक पाथ में कॉम्बाइन करें, फिर एक ही `Graphics.DrawPath` कॉल से रेंडर करें।  
- **Performance:** ऑप्टिमाइज़्ड रेंडरिंग पाइपलाइन 400 MP तक की इमेजेज को पूरी फ़ाइल को मेमोरी में लोड किए बिना प्रोसेस करती है, जिससे बड़े‑पैमाने के बैच जॉब्स संभव होते हैं।  
- **Cross‑Platform:** Windows, Linux, और macOS रनटाइम्स पर समान परिणाम देता है, प्लेटफ़ॉर्म‑स्पेसिफिक बग्स को खत्म करता है।

## पूर्वापेक्षाएँ

ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित प्री‑रिक्विज़िट्स हैं:

- **Aspose.Drawing Library:** Aspose.Drawing लाइब्रेरी डाउनलोड और इंस्टॉल करें। आप लाइब्रेरी [here](https://releases.aspose.com/drawing/net/) पर पा सकते हैं।  
- **Other Aspose Products:** अतिरिक्त Aspose उत्पादों का अन्वेषण करें [here](https://releases.aspose.com/)।  
- **Development Environment:** आवश्यक टूल्स (Visual Studio, .NET SDK, आदि) के साथ अपना .NET डेवलपमेंट एनवायरनमेंट सेट अप करें।

## नेमस्पेस आयात करें

अपने प्रोजेक्ट में आवश्यक नेमस्पेस आयात करके शुरू करें:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## चरण 1: बिटमैप और ग्राफ़िक्स बनाएं

Bitmap मेमोरी में इमेज का प्रतिनिधित्व करता है, जबकि Graphics ड्रॉइंग मेथड्स प्रदान करता है जिससे आप उस इमेज पर रेंडर कर सकते हैं। एक `Bitmap` और एक `Graphics` ऑब्जेक्ट बनाकर शुरू करें। यह बिटमैप वह कैनवास होगा जिस पर `GraphicsPath` रेंडर होगा, और बाद में आप **save bitmap as PNG** करेंगे:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## चरण 2: पेन और GraphicsPath परिभाषित करें

Pen लाइन का रंग, चौड़ाई और स्टाइल निर्धारित करता है; GraphicsPath ड्रॉइंग प्रिमिटिव्स का कलेक्शन एक ही वेक्टर ऑब्जेक्ट के रूप में स्टोर करता है। अगला, ड्रॉइंग एट्रिब्यूट्स निर्दिष्ट करने के लिए एक `Pen` परिभाषित करें और एक `GraphicsPath` इंस्टैंसिएट करें। `GraphicsPath` ऑब्जेक्ट वेक्टर डेटा को रखता है इससे पहले कि वह ड्रॉ किया जाए:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## चरण 3: लाइन्स और शैप्स जोड़ें

AddLine, AddRectangle, और AddEllipse क्रमशः शैप्स को GraphicsPath में जोड़ते हैं ताकि बाद में रेंडर किया जा सके। `GraphicsPath` में लाइन्स, रेक्टैंगल्स, और एलिप्सेज़ जोड़ें ताकि एक जटिल पाथ बन सके। आप कस्टम Bezier कर्व्स भी जोड़ सकते हैं ताकि स्मूद शैप्स बनें:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## चरण 4: पाथ ड्रॉ करें

DrawPath निर्दिष्ट Pen का उपयोग करके Graphics सतह पर GraphicsPath से वेक्टर डेटा रेंडर करता है। निर्दिष्ट `Pen` के साथ `Graphics` ऑब्जेक्ट पर पाथ ड्रॉ करें। यह ऑपरेशन वेक्टर डेटा को बिटमैप कैनवास पर रास्टराइज़ करता है:

```csharp
graphics.DrawPath(pen, path);
```

## चरण 5: इमेज सहेजें – PNG या JPEG में एक्सपोर्ट करें

Bitmap.Save मेथड चुने हुए फॉर्मैट (जैसे PNG या JPEG) में इमेज को डिस्क पर लिखता है। ड्रॉइंग के बाद आप **save bitmap as PNG** करके लॉसलेस क्वालिटी प्राप्त कर सकते हैं या **export image to JPEG** करके छोटे फ़ाइल साइज के लिए एक्सपोर्ट कर सकते हैं। अपनी डाउनस्ट्रीम आवश्यकता के अनुसार फॉर्मैट चुनें:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

इन चरणों को आवश्यकतानुसार दोहराएँ ताकि जटिल और दृश्यात्मक रूप से आकर्षक पाथ्स बन सकें।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **पाथ दिखाई नहीं दे रहा** | सुनिश्चित करें कि Pen का रंग बैकग्राउंड के साथ कंट्रास्ट में है और बिटमैप सही तरीके से सहेजा गया है। |
| **अनपेक्षित इमेज आकार** | बिटमैप की डाइमेंशन्स और पिक्सेल फॉर्मैट को अपनी आवश्यकताओं के अनुसार जाँचें। |
| **लाइसेंस अपवाद** | टेस्टिंग के लिए ट्रायल लाइसेंस उपयोग करें; प्रोडक्शन में डिप्लॉय करने से पहले वैध लाइसेंस लागू करें। |

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं Aspose.Drawing को अन्य .NET लाइब्रेरीज़ के साथ उपयोग कर सकता हूँ?

A1: हाँ, Aspose.Drawing अन्य .NET लाइब्रेरीज़ के साथ सहजता से इंटीग्रेट होता है, जिससे आपके विकास प्रोजेक्ट्स में बहुमुखी प्रतिभा मिलती है।

### प्रश्न 2: क्या कोई ट्रायल वर्ज़न उपलब्ध है?

A2: हाँ, आप मुफ्त ट्रायल [here](https://releases.aspose.com/) पर एक्सेस कर सकते हैं।

### प्रश्न 3: मैं Aspose.Drawing के लिए सपोर्ट कहाँ पा सकता हूँ?

A3: सहायता और कम्युनिटी सपोर्ट के लिए Aspose.Drawing [forum](https://forum.aspose.com/c/drawing/44) देखें।

### प्रश्न 4: मैं टेम्पररी लाइसेंस कैसे प्राप्त करूँ?

A4: टेम्पररी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त करें।

### प्रश्न 5: क्या मैं Aspose.Drawing खरीद सकता हूँ?

A5: हाँ, आप Aspose.Drawing [here](https://purchase.aspose.com/buy) से खरीद सकते हैं।

**अतिरिक्त प्रश्नोत्तर**

**Q: क्या मैं GraphicsPath के साथ कस्टम Bezier कर्व्स ड्रॉ कर सकता हूँ?**  
A: बिल्कुल – स्मूद कर्व्स परिभाषित करने के लिए `path.AddBezier(...)` का उपयोग करें।

**Q: मैं GraphicsPath को पुनः उपयोग करने से पहले कैसे क्लियर करूँ?**  
A: सभी फ़िगर्स हटाने और नई शुरुआत करने के लिए `path.Reset()` कॉल करें।

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक **GraphicsPath का उपयोग करके पाथ्स ड्रॉ करना** और फिर **save bitmap as PNG** या **export image to JPEG** Aspose.Drawing for .NET के साथ किया। इस ट्यूटोरियल में बिटमैप बनाना, पेन परिभाषित करना, `GraphicsPath` बनाना, विभिन्न शैप्स रेंडर करना, और कई फॉर्मैट्स में अंतिम इमेज एक्सपोर्ट करना शामिल था। विभिन्न कोऑर्डिनेट्स, रंग, और लाइन विड्थ के साथ प्रयोग करें और Aspose.Drawing की पूरी क्रिएटिव पोटेंशियल को अनलॉक करें।

---

**अंतिम अपडेट:** 2026-07-22  
**परीक्षण किया गया:** Aspose.Drawing 24.12 for .NET  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Save Bitmap as PNG & Draw Closed Curves with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Save Bitmap C# – Draw Bezier Splines with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [How to Save Image and Draw Cardinal Splines in Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}