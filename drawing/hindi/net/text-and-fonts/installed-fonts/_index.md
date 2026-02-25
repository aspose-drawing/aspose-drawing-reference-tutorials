---
date: 2026-02-25
description: C# में बिटमैप ग्राफ़िक्स बनाना सीखें और PNG इमेजेज़ को सहेजें, साथ ही
  स्थापित फ़ॉन्ट्स की सूची बनाते हुए, फ़ॉन्ट्स के साथ टेक्स्ट ड्रॉ करें, और Aspose.Drawing
  for .NET का उपयोग करके बिटमैप रिज़ॉल्यूशन को समायोजित करें।
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: C# में बिटमैप ग्राफ़िक्स बनाएं – PNG इमेज सहेजें और Aspose.Drawing में इंस्टॉल
  किए गए फ़ॉन्ट्स के साथ काम करें
url: /hi/net/text-and-fonts/installed-fonts/
weight: 13
---

 Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

But we need Hindi for labels:

**Last Updated:** -> "**अंतिम अपडेट:**". Keep bold.

**Tested With:** -> "**परीक्षण किया गया:**". 

**Author:** -> "**लेखक:**".

Let's produce final content.

Make sure to preserve markdown formatting.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG इमेज सहेजें और Aspose.Drawing में स्थापित फ़ॉन्ट्स के साथ काम करें

## Introduction

यदि आपको **save PNG image** फ़ाइलें सहेजनी हैं और साथ ही **create bitmap graphics C#** बनानी है, तो Aspose.Drawing for .NET आपको एक साफ़, क्रॉस‑प्लेटफ़ॉर्म तरीका प्रदान करता है। इस ट्यूटोरियल में हम स्थापित फ़ॉन्ट्स की सूची बनाना, फ़ॉन्ट फ़ैमिली दिखाना, बिटमैप से ग्राफ़िक्स बनाना, और फ़ॉन्ट्स के साथ टेक्स्ट ड्रॉ करना—इन सभी चरणों को कवर करेंगे और अंत में परिणाम को PNG इमेज के रूप में सहेजेंगे। अंत तक आपके पास एक पुन: उपयोग योग्य स्निपेट होगा जिसे आप किसी भी .NET प्रोजेक्ट में डाल सकते हैं।

## Quick Answers
- **What does this tutorial create?** स्थापित फ़ॉन्ट फ़ैमिली की सूची वाली एक PNG इमेज।  
- **Which library is required?** Aspose.Drawing for .NET (कोई System.Drawing.Common आवश्यक नहीं)।  
- **Can I use custom fonts?** हाँ – बस उन्हें `InstalledFontCollection` में लोड करें।  
- **Is the output resolution adjustable?** बिल्कुल – बिटमैप आकार या पिक्सेल फ़ॉर्मेट बदलें ताकि **adjust bitmap resolution C#** शैली में समायोजित किया जा सके।  
- **Do I need a license to run the code?** मूल्यांकन के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।

## What is “save PNG image” in the context of Aspose.Drawing?

PNG इमेज सहेजना का मतलब है आपके ड्रॉइंग सतह (एक `Bitmap`) को `.png` एक्सटेंशन वाली फ़ाइल में रेंडर करना। Aspose.Drawing आपके लिए एन्कोडिंग संभालता है, इसलिए आपको केवल इच्छित पथ के साथ `bitmap.Save(...)` कॉल करना है।

## Why list installed fonts and show font families?

कौन से फ़ॉन्ट उपलब्ध हैं, यह जानना आपको गतिशील ग्राफ़िक्स बनाने में मदद करता है जो अंतिम उपयोगकर्ता के वातावरण के अनुसार अनुकूलित होते हैं। यह रिपोर्ट, प्रमाणपत्र, या किसी भी दृश्य सामग्री को बनाते समय उपयोगी है जिसे कॉरपोरेट ब्रांडिंग से मेल खाना चाहिए बिना फ़ॉन्ट फ़ाइलें भेजे।

## How to create bitmap graphics C# with Aspose.Drawing?

नीचे एक व्यावहारिक, चरण‑दर‑चरण मार्गदर्शिका है जो दिखाती है कि कैसे **create bitmap graphics C#** किया जाए, फ़ॉन्ट्स के साथ टेक्स्ट ड्रॉ किया जाए, और आवश्यकता पड़ने पर बिटमैप रिज़ॉल्यूशन को समायोजित किया जाए।

## Prerequisites

- **Aspose.Drawing Library** – नवीनतम संस्करण [Aspose Drawing download page](https://releases.aspose.com/drawing/net/) से डाउनलोड करें।  
- **IDE** – Visual Studio, Rider, या कोई भी .NET‑compatible एडिटर।  
- **Basic C# knowledge** – आपको क्लासेस, ऑब्जेक्ट्स, और सरल लूप्स में सहज होना चाहिए।

## Import Namespaces
फ़ॉन्ट्स और ग्राफ़िक्स के साथ काम करने के लिए, अपने C# फ़ाइल के शीर्ष पर इन नेमस्पेसेस को इम्पोर्ट करें:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step‑by‑Step Guide

### Step 1: Create a bitmap (the canvas)
पहले, हम एक बिटमैप बनाते हैं जो अंतिम इमेज को रखेगा। बिटमैप का आकार और पिक्सेल फ़ॉर्मेट सहेजी गई PNG की गुणवत्ता निर्धारित करते हैं और आपको **adjust bitmap resolution C#** शैली में समायोजित करने की अनुमति देते हैं।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Step 2: Create graphics from bitmap
अगला, हम बिटमैप से एक `Graphics` ऑब्जेक्ट प्राप्त करते हैं। यह ऑब्जेक्ट हमें कैनवास पर आकार, टेक्स्ट और इमेज ड्रॉ करने की अनुमति देता है।

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Step 3: Set up brush and font (draw text with fonts)
हमें टेक्स्ट रंग के लिए एक ब्रश और एक `Font` ऑब्जेक्ट चाहिए जो टाइपफ़ेस, आकार और शैली को परिभाषित करता है। यही वह जगह है जहाँ हम **draw text with fonts** करते हैं।

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Step 4: List installed fonts and show font families
अब हम बिटमैप पर सीधे फ़ॉन्ट फ़ैमिली की संख्या और पहले कुछ नाम प्रदर्शित करते हैं। यह **list installed fonts** और **show font families** क्षमताओं को दर्शाता है।

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Step 5: Save PNG image
अंत में, हम बिटमैप को डिस्क पर PNG फ़ाइल के रूप में लिखते हैं। यह मुख्य **save png image** ऑपरेशन है।

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tip:** विभिन्न ऑपरेटिंग सिस्टम पर डायरेक्टरी सेपरेटर समस्याओं से बचने के लिए फ़ाइल पाथ बनाने हेतु `Path.Combine` का उपयोग करें।

## Common Issues and Solutions
| Issue | Cause | Fix |
|-------|-------|-----|
| **फ़ॉन्ट नहीं दिख रहे हैं** | `InstalledFontCollection` नहीं भरा गया (उदाहरण के लिए, बिना फ़ॉन्ट्स वाले हेडलेस सर्वर पर चल रहा है)। | सर्वर पर आवश्यक फ़ॉन्ट्स इंस्टॉल करें या अपने एप्लिकेशन में कस्टम फ़ॉन्ट्स एम्बेड करें। |
| **सहेजी गई फ़ाइल भ्रष्ट है** | गलत पिक्सेल फ़ॉर्मेट या लिखने की अनुमति नहीं है। | सुनिश्चित करें कि लक्ष्य फ़ोल्डर मौजूद है और एप्लिकेशन को लिखने की अनुमति है; `Format32bppPArgb` रखें। |
| **टेक्स्ट धुंधला दिख रहा है** | कम DPI सेटिंग्स। | बिटमैप आयाम बढ़ाएँ या `graphics.SmoothingMode = SmoothingMode.AntiAlias` सेट करें। |

## Frequently Asked Questions

**Q: क्या मैं उन कस्टम फ़ॉन्ट्स का उपयोग कर सकता हूँ जो मशीन पर इंस्टॉल नहीं हैं?**  
A: हाँ। फ़ॉन्ट फ़ाइल को `PrivateFontCollection` में लोड करें और उस कलेक्शन से `Font` बनाएं।

**Q: फ़ॉन्ट‑संबंधी अपवादों को कैसे संभालूँ?**  
A: फ़ॉन्ट निर्माण को `try/catch` ब्लॉक में रैप करें और गायब फ़ैमिली के लिए `ArgumentException` की जाँच करें।

**Q: क्या Aspose.Drawing वेब एप्लिकेशन के लिए उपयुक्त है?**  
A: बिल्कुल। यह लाइब्रेरी ASP.NET Core, Azure Functions, और अन्य सर्वर‑साइड वातावरण में काम करती है।

**Q: क्या मैं टेक्स्ट का रंग या शैली बदल सकता हूँ?**  
A: हाँ। विभिन्न `Brush` प्रकार (जैसे `LinearGradientBrush`) का उपयोग करें और `FontStyle` एनोम को संशोधित करें।

**Q: परीक्षण के लिए अस्थायी लाइसेंस कहाँ प्राप्त कर सकता हूँ?**  
A: [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/) से ट्रायल लाइसेंस डाउनलोड करें।

## Conclusion

इन चरणों का पालन करके आपने सीखा कि Aspose.Drawing for .NET का उपयोग करके **save PNG image** फ़ाइलें कैसे बनाई जाएँ जो गतिशील रूप से **list installed fonts**, **show font families**, **create graphics from bitmap**, और **draw text with fonts** करती हैं। अब आप जानते हैं कि **create bitmap graphics C#** कैसे किया जाए, बिटमैप रिज़ॉल्यूशन को समायोजित किया जाए, और आवश्यकता पड़ने पर कस्टम फ़ॉन्ट्स को शामिल किया जाए। अपने प्रोजेक्ट की दृश्य आवश्यकताओं के अनुसार अन्य फ़ॉन्ट्स, रंग, और बिटमैप आकारों के साथ प्रयोग करने में संकोच न करें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2026-02-25  
**परीक्षण किया गया:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose