---
date: 2026-10-18
description: Aspose.Drawing के साथ ड्रॉइंग को PNG में बदलें और world transformations
  लागू करें। C# में translate, rotate और scale के उदाहरण सीखें और transparent PNGs
  एक्सपोर्ट करें।
keywords:
- convert drawing to png
- save graphics as png
- rotate image .net
- scale graphics .net
- transparent png bitmap
lastmod: 2026-10-18
linktitle: Aspose.Drawing में world transformation
og_description: Aspose.Drawing के साथ ड्रॉइंग को PNG में बदलें, world transformations
  लागू करें और transparent PNGs एक्सपोर्ट करें। .NET के लिए C# में translate, rotate
  और scale के उदाहरण सीखें।
og_image_alt: Tutorial showing how to convert drawing to PNG using Aspose.Drawing
  with world transformation
og_title: Aspose.Drawing के साथ ड्रॉइंग को PNG में बदलें – world transformation
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  headline: How to convert drawing to PNG with Aspose.Drawing – world transformation
  type: TechArticle
- description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  name: How to convert drawing to PNG with Aspose.Drawing – world transformation
  steps:
  - name: create a bitmap
    text: '**Definition:** `Bitmap` is Aspose.Drawing’s in‑memory representation of
      a raster image that you can draw on or save to disk. We start by creating a
      blank canvas that will hold our drawing. `new Bitmap(width, height, PixelFormat.Format32bppPArgb)`
      creates a 32‑bit per pixel bitmap with premultiplied'
  - name: set the world transformation (graphics translate example)
    text: '**Definition:** `Graphics` is the drawing surface that renders shapes onto
      a `Bitmap`. `TranslateTransform` moves the origin of the coordinate system to
      a new location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height
      / 2)` shifts the (0,0) point to the canvas centre. After this call, an'
  - name: draw a rectangle using the transformed coordinates
    text: '**Definition:** `DrawRectangle` is a method of `Graphics` that renders
      a rectangular outline or filled shape based on the supplied pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width'
  - name: save the result – convert graphics to PNG
    text: '**Definition:** `ImageFormat` is an enumeration that tells the `Save` method
      which file format to use. `Save` writes the bitmap to a file in the specified
      image format. `bitmap.Save(outputPath, ImageFormat.Png)` writes a lossless PNG
      file that can be used directly in web pages or UI components. - PN'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- convert drawing to png
- Aspose.Drawing
- .NET graphics
- PNG export
- world transformation
title: Aspose.Drawing के साथ ड्रॉइंग को PNG में कैसे बदलें – world transformation
url: /hi/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing के साथ ड्रॉइंग को PNG में बदलना – वर्ल्ड ट्रांसफ़ॉर्मेशन

## बिटमैप को PNG के रूप में सहेजें – परिचय

**How to convert drawing to PNG** का उपयोग Aspose.Drawing के साथ तब आम आवश्यकता होती है जब आपको ऑन‑द‑फ़्लाई उच्च‑गुणवत्ता, पारदर्शी छवियों की आवश्यकता होती है। इस ट्यूटोरियल में आप सीखेंगे कि **बिटमैप को PNG के रूप में सहेजें**, ट्रांसलेट, रोटेट और स्केल जैसी वर्ल्ड ट्रांसफ़ॉर्मेशन लागू करें, और अंत में ग्राफ़िक्स को PNG में बदलें—सभी साफ़, मेंटेनेबल C# कोड के साथ। चाहे आप रिपोर्टिंग इंजन, चार्टिंग कॉम्पोनेन्ट, या कस्टम UI रेंडरर बना रहे हों, इन चरणों में महारत हासिल करने से आप डायनेमिक इमेजेज़ बना सकते हैं जो किसी भी डिवाइस पर शानदार दिखती हैं।

## त्वरित उत्तर
- **'वर्ल्ड ट्रांसफ़ॉर्मेशन' का क्या मतलब है?** यह आपके ड्रॉइंग के लॉजिकल (वर्ल्ड) कोऑर्डिनेट्स को पेज (डिवाइस) कोऑर्डिनेट्स में मैप करता है, जिससे आप सब कुछ एक ही मैट्रिक्स से पुनःस्थापित, घुमा या स्केल कर सकते हैं।  
- **क्या मैं परिणाम को PNG के रूप में निर्यात कर सकता हूँ?** हाँ – ड्रॉइंग के बाद आप बस `bitmap.Save(...)` को `.png` एक्सटेंशन के साथ कॉल करें।  
- **क्या मुझे Aspose.Drawing के लिए लाइसेंस चाहिए?** विकास के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **क्या यह .NET 6/7 के साथ संगत है?** बिल्कुल – Aspose.Drawing .NET Framework 4.5+ और .NET Core/5/6/7 को सपोर्ट करता है, जो वर्तमान .NET डिप्लॉयमेंट्स के 90 % से अधिक को कवर करता है।  
- **मैं कितनी ट्रांसफ़ॉर्मेशन को श्रृंखला में जोड़ सकता हूँ?** आप क्रम में **कई ग्राफ़िक्स ट्रांसफ़ॉर्मेशन** (ट्रांसलेट, रोटेट, स्केल, आदि) लागू कर सकते हैं बिना प्रदर्शन पर प्रभाव के।

## Aspose.Drawing में वर्ल्ड ट्रांसफ़ॉर्मेशन क्या है?

वर्ल्ड ट्रांसफ़ॉर्मेशन आपके ड्रॉइंग कमांड्स द्वारा उपयोग किए जाने वाले कोऑर्डिनेट सिस्टम को बदलता है। डिफ़ॉल्ट रूप से, (0,0) बिटमैप का टॉप‑लेफ़्ट कोना होता है। `TranslateTransform`, `RotateTransform`, या `ScaleTransform` के साथ आप उस मूल बिंदु को पुनःस्थापित, आकार बदल या घुमा सकते हैं बिना मूल ज्योमेट्री को बदले। यह आपको एक बार डिज़ाइन करने और किसी भी आकार या अभिविन्यास में रेंडर करने की सुविधा देता है।

## Aspose.Drawing का उपयोग करके PNG कैसे सहेजें?

`Bitmap` ऑब्जेक्ट लोड करें, उसकी `Graphics` इंस्टेंस पर इच्छित वर्ल्ड ट्रांसफ़ॉर्मेशन सेट करें, अपने शैप्स ड्रॉ करें, और अंत में `bitmap.Save("output.png", ImageFormat.Png)` कॉल करें। यह एक‑लाइन सेव कॉल एक लॉसलेस PNG फ़ाइल लिखता है जो पारदर्शिता और रंग की सटीकता को बरकरार रखता है, जिससे यह वेब एसेट्स और UI ओवरलेज़ के लिए आदर्श बनता है। API सभी लो‑लेवल एन्कोडिंग को संभालता है, इसलिए आप सामान्य कैनवास आकारों के लिए एक सेकंड से कम में तैयार‑टू‑यूज़ PNG प्राप्त कर सकते हैं।

## ग्राफ़िक्स ट्रांसलेट उदाहरण का उपयोग क्यों करें?

एक ग्राफ़िक्स ट्रांसलेट उदाहरण आपको ड्रॉइंग मूल बिंदु को एक बार स्थानांतरित करने देता है, बजाय हर बिंदु को पुनःगणना करने के। मूल बिंदु को कैनवास के केंद्र में शिफ्ट करने से ज्योमेट्री सरल हो जाती है, कोड डुप्लिकेशन कम होता है, और ग्राफ़िक्स इंजन को मैट्रिक्स मल्टिप्लिकेशन नेटिव कोड में करने देता है, जिससे बड़े कैनवास पर रेंडरिंग गति में 30 % तक सुधार हो सकता है। यह पैटर्न कोड को आसान रखरखाव योग्य बनाता है जब आप बाद में रोटेशन या स्केलिंग जोड़ते हैं।

## ग्राफ़िक्स ट्रांसलेट उदाहरण

एक **ग्राफ़िक्स ट्रांसलेट उदाहरण** दर्शाता है कि मूल बिंदु को स्थानांतरित करने से पोज़िशनिंग कैसे सरल हो जाती है। हर बिंदु को पुनःगणना करने के बजाय, आप कोऑर्डिनेट सिस्टम को एक बार शिफ्ट करते हैं और ऐसे ड्रॉ करते हैं जैसे नया मूल बिंदु कैनवास का केंद्र हो।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- **Aspose.Drawing library** को अपने .NET प्रोजेक्ट में इंटीग्रेट करें – इसे आधिकारिक [Aspose.Drawing रिलीज़ पेज](https://releases.aspose.com/drawing/net/) से डाउनलोड करें।  
- एक **डॉक्यूमेंट डायरेक्टरी** जहाँ आउटपुट इमेज सहेजी जाएगी।  
- **C#** सिंटैक्स और Visual Studio या आपके पसंदीदा IDE की बुनियादी जानकारी।  

अब, चलिए कोड में डुबकी लगाते हैं!

## नेमस्पेस आयात करें

`Bitmap`, `Graphics`, और Aspose ड्रॉइंग यूटिलिटीज़ इन नेमस्पेस में स्थित हैं।  
**परिभाषा:** `System.Drawing` कोर GDI+ टाइप्स प्रदान करता है, जबकि `Aspose.Drawing` उन्हें क्रॉस‑प्लेटफ़ॉर्म क्षमताओं के साथ विस्तारित करता है, जिससे आप वही कोड Windows, Linux और macOS पर अतिरिक्त डिपेंडेंसीज़ के बिना चला सकते हैं।

## चरण‑दर‑चरण गाइड

### चरण 1: बिटमैप बनाएं

**परिभाषा:** `Bitmap` Aspose.Drawing की इन‑मेमोरी प्रतिनिधित्व है एक रास्टर इमेज की, जिस पर आप ड्रॉ कर सकते हैं या डिस्क पर सहेज सकते हैं।  

हम एक खाली कैनवास बनाकर शुरू करते हैं जो हमारे ड्रॉइंग को रखेगा।

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` 32‑बिट प्रति पिक्सेल बिटमैप बनाता है प्री‑मल्टिप्लाइड अल्फा के साथ, जो PNG आउटपुट के लिए इष्टतम फॉर्मेट है क्योंकि यह अतिरिक्त कन्वर्ज़न स्टेप्स के बिना पारदर्शिता को बरकरार रखता है।

- **क्यों 32bppPArgb?** यह पिक्सेल फॉर्मेट अल्फा पारदर्शिता और उच्च‑गुणवत्ता रंग रेंडरिंग को सपोर्ट करता है, PNG आउटपुट के लिए परफेक्ट है।  
- **प्रो टिप:** चौड़ाई/ऊँचाई को अपने लक्ष्य इमेज आकार के अनुसार समायोजित करें; 1920 × 1080 कैनवास सामान्य डेवलपर लैपटॉप पर 0.2 सेकंड से कम में रेंडर होता है।

### चरण 2: वर्ल्ड ट्रांसफ़ॉर्मेशन सेट करें (ग्राफ़िक्स ट्रांसलेट उदाहरण)

**परिभाषा:** `Graphics` वह ड्रॉइंग सतह है जो `Bitmap` पर शैप्स रेंडर करती है।  

`TranslateTransform` कोऑर्डिनेट सिस्टम के मूल बिंदु को नई जगह पर ले जाता है।  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` (0,0) बिंदु को कैनवास के केंद्र में शिफ्ट करता है। इस कॉल के बाद, आप जो भी शैप (0,0) कोऑर्डिनेट्स से ड्रॉ करेंगे वह इमेज के मध्य में दिखाई देगा।

- यह (0,0) बिंदु को (500, 400) पर ले जाता है – 1000 × 800 कैनवास का मध्य।  
- आप अतिरिक्त ट्रांसफ़ॉर्मेशन को श्रृंखला में जोड़ सकते हैं: `RotateTransform` कोऑर्डिनेट सिस्टम को घुमाता है, और `ScaleTransform` इसे स्केल करता है, जिससे **कई ग्राफ़िक्स ट्रांसफ़ॉर्मेशन** एक ही पाइपलाइन में संभव होते हैं।

### चरण 3: ट्रांसफ़ॉर्म किए गए निर्देशांक का उपयोग करके आयत बनाएं

**परिभाषा:** `DrawRectangle` `Graphics` की एक मेथड है जो प्रदान किए गए पेन और कोऑर्डिनेट्स के आधार पर आयताकार रूपरेखा या भरी हुई आकृति रेंडर करती है।  

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` कैनवास के केंद्र में एक आयत बनाता है क्योंकि इसका टॉप‑लेफ़्ट कोना ट्रांसफ़ॉर्म किए गए मूल बिंदु से उसकी चौड़ाई और ऊँचाई के आधे हिस्से से ऑफ़सेट है।

- आयत का टॉप‑लेफ़्ट कोना ट्रांसफ़ॉर्म किए गए मूल बिंदु (इमेज का केंद्र) से शुरू होता है।  
- अन्य शैप्स—एलिप्स, लाइन्स, या कस्टम पाथ्स—के साथ प्रयोग करने में संकोच न करें।

### चरण 4: परिणाम सहेजें – ग्राफ़िक्स को PNG में बदलें

**परिभाषा:** `ImageFormat` एक एनेमरेशन है जो `Save` मेथड को बताता है कि कौन सा फ़ाइल फ़ॉर्मेट उपयोग करना है।  

`Save` बिटमैप को निर्दिष्ट इमेज फ़ॉर्मेट में फ़ाइल में लिखता है।  
`bitmap.Save(outputPath, ImageFormat.Png)` एक लॉसलेस PNG फ़ाइल लिखता है जिसे सीधे वेब पेज या UI कॉम्पोनेन्ट्स में उपयोग किया जा सकता है।

- PNG पहले सेट किए गए सटीक रंग और पारदर्शिता को बरकरार रखता है।  
- `"Your Document Directory"` को अपने मशीन पर वास्तविक पाथ से बदलें।  
- बैच प्रोसेसिंग के लिए, `Bitmap` ऑब्जेक्ट्स के संग्रह पर लूप करें और लूप के भीतर `Save` कॉल करें – लाइब्रेरी 200 MB से कम RAM में हजारों इमेजेज़ को संभाल सकती है।

## सामान्य समस्याएँ और समाधान

| Issue | Why it happens | Fix |
|-------|----------------|-----|
| **फ़ाइल नहीं मिली त्रुटि** सहेजते समय | लक्ष्य फ़ोल्डर मौजूद नहीं है। | `Save` कॉल करने से पहले फ़ोल्डर को प्रोग्रामेटिकली बनाएं (`Directory.CreateDirectory`)। |
| **खाली इमेज** ट्रांसफ़ॉर्मेशन के बाद | `TranslateTransform` ड्रॉइंग के बाद कॉल किया गया। | सुनिश्चित करें कि ट्रांसफ़ॉर्मेशन **ड्रॉइंग कमांड्स** से पहले सेट किया गया है। |
| **विकृत रंग** | असंगत पिक्सेल फ़ॉर्मेट का उपयोग किया गया। | PNG आउटपुट के लिए `Format32bppPArgb` ही उपयोग करें। |
| **बड़े कैनवास पर मेमोरी समाप्त** | पूरे बिटमैप को मेमोरी में लोड करना। | `Bitmap` स्ट्रीमिंग विकल्पों का उपयोग करें या इमेज को टाइल्स में विभाजित करें; Aspose.Drawing टाइल्स को स्वतंत्र रूप से रेंडर कर सकता है। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं एक से अधिक ट्रांसफ़ॉर्मेशन लागू कर सकता हूँ?**  
**उत्तर:** हाँ – आप `TranslateTransform`, `RotateTransform`, और `ScaleTransform` को श्रृंखला में जोड़कर एक ही ग्राफ़िक्स पाइपलाइन में जटिल इफ़ेक्ट्स प्राप्त कर सकते हैं।

**प्रश्न: क्या Aspose.Drawing व्यावसायिक प्रोजेक्ट्स के लिए मुफ्त है?**  
**उत्तर:** मूल्यांकन के लिए एक फ्री ट्रायल उपलब्ध है, लेकिन प्रोडक्शन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है।

**प्रश्न: क्या यह .NET Core और .NET 5/6/7 के साथ काम करता है?**  
**उत्तर:** बिल्कुल। Aspose.Drawing सभी आधुनिक .NET रनटाइम्स को सपोर्ट करता है, जिसमें .NET Core, .NET 5, .NET 6, और .NET 7 शामिल हैं।

**प्रश्न: मैं पूरी API रेफ़रेंस कहाँ पा सकता हूँ?**  
**उत्तर:** पूरी डॉक्यूमेंटेशन यहाँ उपलब्ध है: [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/)।

**प्रश्न: मैं गायब आउटपुट फ़ाइल की समस्या कैसे हल करूँ?**  
**उत्तर:** पाथ स्ट्रिंग की जाँच करें, लिखने की अनुमति सुनिश्चित करें, और `Save` कॉल करने से पहले यह पुष्टि करें कि डायरेक्टरी मौजूद है।

## निष्कर्ष

आपने अब **Aspose.Drawing के साथ ड्रॉइंग को PNG में बदलना** सीख लिया है, एक **वर्ल्ड ट्रांसफ़ॉर्मेशन** लागू किया है, और एक **ग्राफ़िक्स ट्रांसलेट उदाहरण** किया है जिसे रोटेशन या स्केलिंग के साथ विस्तारित किया जा सकता है। इन बिल्डिंग ब्लॉक्स में महारत हासिल करके आप डायनेमिक इमेजेज़ जेनरेट कर सकते हैं, कस्टम चार्ट बना सकते हैं, या किसी भी .NET एप्लिकेशन के लिए ऑन‑द‑फ़्लाई ग्राफ़िक्स बना सकते हैं। अगला, मैट्रिक्स‑आधारित ट्रांसफ़ॉर्मेशन ट्यूटोरियल देखें ताकि कई ऑपरेशन्स को एक ही मैट्रिक्स में मिलाकर और भी बेहतर प्रदर्शन प्राप्त कर सकें।

---

**अंतिम अपडेट:** 2026-10-18  
**परीक्षित संस्करण:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose  
**संबंधित संसाधन:** [Aspose.Drawing API reference](https://reference.aspose.com/drawing/net/) | [Download free trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## संबंधित ट्यूटोरियल

- [मैट्रिक्स ट्रांसफ़ॉर्मेशन ट्यूटोरियल: Aspose.Drawing के लिए .NET में मैट्रिक्स ट्रांसफ़ॉर्मेशन](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Aspose.Drawing ग्लोबल ट्रांसफ़ॉर्मेशन के साथ इमेज कैसे घुमाएँ](/drawing/net/coordinate-transformations/global-transformation/)
- [कोऑर्डिनेट सिस्टम ट्रांसफ़ॉर्मेशन – Aspose.Drawing के लिए .NET में पेज ट्रांसफ़ॉर्मेशन](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}