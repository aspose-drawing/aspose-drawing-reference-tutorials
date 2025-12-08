---
date: 2025-12-06
description: Aspose.Drawing for .NET का उपयोग करके स्थापित फ़ॉन्ट्स की सूची बनाते
  हुए, फ़ॉन्ट परिवार दिखाते हुए, बिटमैप से ग्राफ़िक्स बनाते हुए, और फ़ॉन्ट्स के साथ
  टेक्स्ट ड्रॉ करते हुए PNG इमेज फ़ाइलें कैसे सहेजें, सीखें।
language: hi
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing में PNG इमेज सहेजें और स्थापित फ़ॉन्ट्स के साथ काम करें
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG इमेज सहेजें और Aspose.Drawing में स्थापित फ़ॉन्ट्स के साथ काम करें

## Introduction

यदि आपको **save PNG image** फ़ाइलें चाहिए जो मशीन पर स्थापित फ़ॉन्ट्स की जानकारी भी प्रदर्शित करती हों, तो Aspose.Drawing for .NET आपको इसे करने का एक साफ़, क्रॉस‑प्लेटफ़ॉर्म तरीका देता है। इस ट्यूटोरियल में हम स्थापित फ़ॉन्ट्स की सूची बनाना, फ़ॉन्ट फ़ैमिलीज़ दिखाना, बिटमैप से ग्राफ़िक्स बनाना, और फ़ॉन्ट्स के साथ टेक्स्ट ड्रॉ करना सीखेंगे—और अंत में परिणाम को PNG इमेज के रूप में सहेजेंगे। अंत तक आपके पास एक पुन: उपयोग योग्य स्निपेट होगा जिसे आप किसी भी .NET प्रोजेक्ट में डाल सकते हैं।

## Quick Answers
- **What does this tutorial create?** एक PNG इमेज जो स्थापित फ़ॉन्ट फ़ैमिलीज़ की सूची देती है।  
- **Which library is required?** Aspose.Drawing for .NET (System.Drawing.Common की आवश्यकता नहीं)।  
- **Can I use custom fonts?** हाँ – बस उन्हें `InstalledFontCollection` में लोड करें।  
- **Is the output resolution adjustable?** बिल्कुल – बिटमैप का आकार या पिक्सेल फ़ॉर्मेट बदलें।  
- **Do I need a license to run the code?** मूल्यांकन के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।

## What is “save PNG image” in the context of Aspose.Drawing?
PNG इमेज सहेजना का मतलब है आपके ड्रॉइंग सतह (`Bitmap`) को `.png` एक्सटेंशन वाली फ़ाइल में रेंडर करना। Aspose.Drawing आपके लिए एन्कोडिंग संभालता है, इसलिए आपको केवल `bitmap.Save(...)` को इच्छित पाथ के साथ कॉल करना है।

## Why list installed fonts and show font families?
कौन से फ़ॉन्ट उपलब्ध हैं, यह जानने से आप ऐसी डायनामिक ग्राफ़िक्स बना सकते हैं जो अंतिम उपयोगकर्ता के वातावरण के अनुसार अनुकूल हों। यह रिपोर्ट, प्रमाणपत्र, या कोई भी विज़ुअल कंटेंट बनाने में उपयोगी है जिसे कॉर्पोरेट ब्रांडिंग के साथ मेल खाना चाहिए बिना फ़ॉन्ट फ़ाइलें शिप किए।

## Prerequisites

- **Aspose.Drawing Library** – नवीनतम संस्करण [Aspose Drawing download page](https://releases.aspose.com/drawing/net/) से डाउनलोड करें।  
- **IDE** – Visual Studio, Rider, या कोई भी .NET‑संगत एडिटर।  
- **Basic C# knowledge** – आपको क्लासेज़, ऑब्जेक्ट्स, और सरल लूप्स में सहज होना चाहिए।

## Import Namespaces
फ़ॉन्ट्स और ग्राफ़िक्स के साथ काम करने के लिए, अपने C# फ़ाइल के शीर्ष पर इन नेमस्पेसेज़ को इम्पोर्ट करें:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step‑by‑Step Guide

### Step 1: Create a bitmap (the canvas)
पहले, हम एक बिटमैप बनाते हैं जो अंतिम इमेज को रखेगा। बिटमैप का आकार और पिक्सेल फ़ॉर्मेट सहेजी गई PNG की गुणवत्ता निर्धारित करते हैं।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Step 2: Create graphics from bitmap
अगला, हम बिटमैप से एक `Graphics` ऑब्जेक्ट प्राप्त करते हैं। यह ऑब्जेक्ट हमें कैनवास पर आकार, टेक्स्ट, और इमेज ड्रॉ करने की अनुमति देता है।

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Step 3: Set up brush and font (draw text with fonts)
टेक्स्ट का रंग देने के लिए हमें एक ब्रश चाहिए और एक `Font` ऑब्जेक्ट चाहिए जो टाइपफ़ेस, आकार, और स्टाइल को परिभाषित करता है।

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Step 4: List installed fonts and show font families
अब हम फ़ॉन्ट फ़ैमिलीज़ की संख्या और पहले कुछ नाम सीधे बिटमैप पर प्रदर्शित करते हैं। यह **list installed fonts** और **show font families** क्षमताओं को दर्शाता है।

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Step 5: Save PNG image
अंत में, हम बिटमैप को डिस्क पर PNG फ़ाइल के रूप में लिखते हैं। यही मूल **save png image** ऑपरेशन है।

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tip:** विभिन्न ऑपरेटिंग सिस्टम पर डायरेक्टरी सेपरेटर समस्याओं से बचने के लिए फ़ाइल पाथ बनाने में `Path.Combine` का उपयोग करें।

## Common Issues and Solutions
| Issue | Cause | Fix |
|-------|-------|-----|
| **No fonts displayed** | `InstalledFontCollection` नहीं भरा गया (उदाहरण के लिए, हेडलेस सर्वर पर फ़ॉन्ट्स नहीं हैं)। | सर्वर पर आवश्यक फ़ॉन्ट्स इंस्टॉल करें या अपनी एप्लिकेशन में कस्टम फ़ॉन्ट्स एम्बेड करें। |
| **Saved file is corrupted** | गलत पिक्सेल फ़ॉर्मेट या लिखने की अनुमति नहीं है। | सुनिश्चित करें कि लक्ष्य फ़ोल्डर मौजूद है और एप्लिकेशन को लिखने की अनुमति है; `Format32bppPArgb` रखें। |
| **Text looks blurry** | कम DPI सेटिंग्स। | बिटमैप के आयाम बढ़ाएँ या `graphics.SmoothingMode = SmoothingMode.AntiAlias` सेट करें। |

## Frequently Asked Questions

**Q: क्या मैं उन कस्टम फ़ॉन्ट्स का उपयोग कर सकता हूँ जो मशीन पर स्थापित नहीं हैं?**  
A: हाँ। फ़ॉन्ट फ़ाइल को `PrivateFontCollection` में लोड करें और उस कलेक्शन से `Font` बनाएं।

**Q: फ़ॉन्ट‑संबंधी एक्सेप्शन को कैसे हैंडल करूँ?**  
A: फ़ॉन्ट निर्माण को `try/catch` ब्लॉक में रखें और गायब फ़ैमिलीज़ के लिए `ArgumentException` की जाँच करें।

**Q: क्या Aspose.Drawing वेब एप्लिकेशन्स के लिए उपयुक्त है?**  
A: बिल्कुल। यह लाइब्रेरी ASP.NET Core, Azure Functions, और अन्य सर्वर‑साइड वातावरण में काम करती है।

**Q: क्या मैं टेक्स्ट का रंग या स्टाइल बदल सकता हूँ?**  
A: हाँ। विभिन्न `Brush` प्रकार (जैसे `LinearGradientBrush`) का उपयोग करें और `FontStyle` enum को संशोधित करें।

**Q: परीक्षण के लिए अस्थायी लाइसेंस कहाँ से प्राप्त करूँ?**  
A: [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/) से ट्रायल लाइसेंस डाउनलोड करें।

## Conclusion

इन चरणों का पालन करके आपने **save PNG image** फ़ाइलें बनाना सीखा जो डायनामिक रूप से **list installed fonts**, **show font families**, **create graphics from bitmap**, और **draw text with fonts** को Aspose.Drawing for .NET के साथ उपयोग करती हैं। अन्य फ़ॉन्ट्स, रंग, और बिटमैप आकारों के साथ प्रयोग करने के लिए स्वतंत्र महसूस करें ताकि आपके प्रोजेक्ट की विज़ुअल आवश्यकताओं को पूरा किया जा सके।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose