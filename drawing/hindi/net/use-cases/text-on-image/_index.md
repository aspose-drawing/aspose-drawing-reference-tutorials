---
date: 2026-02-27
description: Aspose.Drawing for .NET का उपयोग करके जन्मदिन कार्ड छवि कैसे बनाएं, सीखें।
  यह गाइड आपको दिखाता है कि कैसे छवि पर स्ट्रिंग ड्रॉ करें, चित्र पर टेक्स्ट ओवरले
  करें, और फोटो में जल्दी से कैप्शन जोड़ें।
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing के साथ जन्मदिन कार्ड छवि कैसे बनाएं
url: /hi/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing के साथ जन्मदिन कार्ड इमेज कैसे बनाएं

## परिचय
.NET विकास की गतिशील दुनिया में, Aspose.Drawing एक शक्तिशाली टूल के रूप में उभरता है जो छवियों को आसानी से संशोधित करने में सक्षम है। चाहे आपको **जन्मदिन कार्ड इमेज बनानी** हो, वॉटरमार्क जोड़ना हो, या सिर्फ चित्र पर टेक्स्ट ओवरले करना हो, यह ट्यूटोरियल आपको C# का उपयोग करके इमेज पर स्ट्रिंग ड्रॉ करने के सटीक चरणों से परिचित कराता है। इस गाइड के अंत तक आपके पास एक व्यक्तिगत जन्मदिन कार्ड तैयार होगा जिसे आप साझा कर सकते हैं।

## त्वरित उत्तर
- **क्या लाइब्रेरी उपयोग करनी चाहिए?** Aspose.Drawing for .NET  
- **क्या मैं फोटो में कैप्शन जोड़ सकता हूँ?** हाँ – कस्टम फ़ॉन्ट्स के साथ `Graphics.DrawString` का उपयोग करें।  
- **क्या प्रोडक्शन के लिए लाइसेंस आवश्यक है?** हाँ, एक व्यावसायिक लाइसेंस की आवश्यकता है।  
- **कौन से .NET संस्करण समर्थित हैं?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** साधारण कार्ड के लिए आमतौर पर 10 मिनट से कम।

## जन्मदिन कार्ड इमेज क्या है?
जन्मदिन कार्ड इमेज एक व्यक्तिगत तस्वीर है जिसमें बैकग्राउंड फोटो के साथ कस्टम टेक्स्ट—जैसे अभिवादन, प्राप्तकर्ता का नाम, या उत्सव संदेश—जोड़ा जाता है। Aspose.Drawing का उपयोग करके आप इन कार्डों को प्रोग्रामेटिक रूप से बना सकते हैं बिना मैन्युअल ग्राफिक डिज़ाइन टूल्स के।

## चित्र पर टेक्स्ट ओवरले करने के लिए Aspose.Drawing क्यों उपयोग करें?
- **क्रॉस‑प्लेटफ़ॉर्म समर्थन:** Windows, Linux, और macOS पर काम करता है।  
- **रिच ड्राइंग API:** फ़ॉन्ट्स, रंगों और लेआउट पर पूर्ण नियंत्रण।  
- **कोई बाहरी निर्भरताएँ नहीं:** `System.Drawing.Common` को पूरी तरह मैनेज्ड लाइब्रेरी से बदलता है।  
- **उच्च प्रदर्शन:** बड़े पैमाने पर इमेज प्रोसेसिंग के लिए अनुकूलित।

## पूर्वापेक्षाएँ
ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित उपलब्ध हैं:

1. Aspose.Drawing लाइब्रेरी: Aspose.Drawing लाइब्रेरी को [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/) से डाउनलोड और इंस्टॉल करें।  
2. विकास वातावरण: Visual Studio या Visual Studio Code जैसे कार्यशील .NET विकास वातावरण, जिसमें .NET 6 SDK या बाद का संस्करण स्थापित हो।

अब, चलिए चरण‑बद्ध गाइड के माध्यम से इमेज में टेक्स्ट जोड़ते हैं और उसे जन्मदिन कार्ड के रूप में सहेजते हैं।

## नेमस्पेसेस आयात करें
अपने C# प्रोजेक्ट में आवश्यक नेमस्पेसेस आयात करके शुरू करें:

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## चरण 1: इमेज लोड करें
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
यहाँ, हम निर्दिष्ट फ़ाइल पाथ से इमेज लोड करते हैं और आगे की प्रोसेसिंग के लिए ग्राफ़िक्स ऑब्जेक्ट को इनिशियलाइज़ करते हैं।

## चरण 2: टेक्स्ट प्रॉपर्टीज़ सेट करें
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
रंग, फ़ॉन्ट और पैडिंग जैसी टेक्स्ट प्रॉपर्टीज़ को परिभाषित करें। अपने डिज़ाइन पसंद के अनुसार इन पैरामीटर्स को समायोजित करें।

## चरण 3: टेक्स्ट आकार मापें
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
प्रत्येक शब्द को अलग‑अलग मापकर टेक्स्ट के लिए आवश्यक आकार की गणना करें। यह उचित प्लेसमेंट सुनिश्चित करता है और टेक्स्ट ओवरलैप से बचाता है।

## चरण 4: इमेज पर टेक्स्ट ड्रॉ करें
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
अब, गणना किए गए आकार के आधार पर इमेज पर टेक्स्ट को पोज़िशन करें और निर्दिष्ट फ़ॉन्ट व रंग का उपयोग करके उसे ड्रॉ करें।

## चरण 5: इमेज सहेजें
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
परिवर्तित इमेज को अपनी इच्छित डायरेक्टरी में सहेजें। परिणामी फ़ाइल एक तैयार‑से‑भेजने योग्य जन्मदिन कार्ड इमेज है।

## सामान्य उपयोग केस और टिप्स
- **फोटो में कैप्शन जोड़ें:** `text` को अपनी आवश्यक कैप्शन से बदलें, जैसे “Celebrating 30 Years!”।  
- **बिटमैप पर टेक्स्ट ड्रॉ करें:** वही तरीका `Bitmap` ऑब्जेक्ट्स पर भी लागू होता है जो शून्य से बनाए गए हों।  
- **एकाधिक लाइनों को ओवरले करें:** स्ट्रिंग्स की एरे पर लूप करें और प्रत्येक लाइन के लिए `Rectangle` Y‑कोऑर्डिनेट को समायोजित करें।  
- **प्रो टिप:** स्मूथर टेक्स्ट रेंडरिंग के लिए `Graphics.SmoothingMode = SmoothingMode.AntiAlias` का उपयोग करें।

## निष्कर्ष
Aspose.Drawing .NET में इमेज मैनिपुलेशन कार्यों को सरल बनाता है, जिससे डेवलपर्स को एक मजबूत टूलकिट मिलता है। इमेज में टेक्स्ट जोड़ना—चाहे **जन्मदिन कार्ड इमेज बनाना**, **इमेज पर स्ट्रिंग ड्रॉ करना**, या **फोटो में कैप्शन जोड़ना**—इसकी ग्राफ़िकल एलिमेंट्स को संभालने की बहुमुखी क्षमता का एक उदाहरण है।

## अक्सर पूछे जाने वाले प्रश्न
### क्या Aspose.Drawing सभी इमेज फॉर्मैट्स के साथ संगत है?
Aspose.Drawing JPEG, PNG, GIF जैसे लोकप्रिय फॉर्मैट्स सहित विस्तृत रेंज के इमेज फॉर्मैट्स को सपोर्ट करता है। पूर्ण सूची के लिए [documentation](https://reference.aspose.com/drawing/net/) देखें।

### क्या मैं Aspose.Drawing को व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?
हाँ, Aspose.Drawing व्यक्तिगत और व्यावसायिक दोनों प्रोजेक्ट्स के लिए उपयुक्त है। लाइसेंस विवरण के लिए [purchase page](https://purchase.aspose.com/buy) देखें।

### क्या परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस उपलब्ध हैं?
हाँ, आप परीक्षण के लिए अस्थायी लाइसेंस प्राप्त कर सकते हैं, इसके लिए [Temporary License](https://purchase.aspose.com/temporary-license/) देखें।

### Aspose.Drawing के लिए समुदाय समर्थन कहाँ मिल सकता है?
समुदाय के साथ जुड़ें और समर्थन प्राप्त करें [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) पर।

### Aspose.Drawing के साथ कैसे शुरू करें?
लाइब्रेरी को [here](https://releases.aspose.com/drawing/net/) से डाउनलोड करें और व्यापक [documentation](https://reference.aspose.com/drawing/net/) का अन्वेषण करें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2026-02-27  
**परीक्षित संस्करण:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose  

---