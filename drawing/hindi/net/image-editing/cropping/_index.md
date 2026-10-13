---
date: 2026-10-13
description: Aspose.Drawing API का उपयोग करके PNG में इमेजेज को बैच में क्रॉप करना
  सीखें, जो .NET डेवलपर्स के लिए System.Drawing का क्रॉस‑प्लेटफ़ॉर्म विकल्प है।
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: इमेज क्रॉपिंग ट्यूटोरियल – Aspose.Drawing
og_description: Aspose.Drawing का उपयोग करके PNG में इमेजेज को तेज़ी से बैच में क्रॉप
  करना सीखें, जो .NET डेवलपर्स के लिए System.Drawing का क्रॉस‑प्लेटफ़ॉर्म विकल्प है।
  कई फ़ाइलों को कुशलतापूर्वक प्रोसेस करने के लिए चरण‑दर‑चरण निर्देशों का पालन करें।
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Aspose.Drawing for .NET के साथ PNG में इमेजेज को बैच में क्रॉप कैसे करें
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Aspose.Drawing for .NET का उपयोग करके PNG में इमेजेज को बैच में क्रॉप कैसे
  करें
url: /hi/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET का उपयोग करके PNG में बैच क्रॉप इमेज कैसे करें

यदि आपको .NET वातावरण में तेज़, विश्वसनीय और बड़े पैमाने पर **crop image to PNG** करने की आवश्यकता है, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम एक इमेज लोड करने, क्रॉप एरिया निर्धारित करने, और परिणाम को PNG फ़ाइल के रूप में सहेजने के सटीक चरणों को देखेंगे—सभी Aspose.Drawing का उपयोग करके, जो **alternative to System.Drawing** का एक आधुनिक विकल्प है और क्रॉस‑प्लेटफ़ॉर्म काम करता है। आप यह भी देखेंगे कि कैसे सिंगल‑इमेज फ्लो को पूर्ण **batch crop** पाइपलाइन में विस्तारित किया जा सकता है।

## त्वरित उत्तर
- **मैं कौनसी लाइब्रेरी उपयोग करूँ?** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **बेसिक क्रॉप में कितना समय लगता है?** आमतौर पर आधुनिक CPU पर एक सिंगल इमेज के लिए एक सेकंड से कम  
- **क्या मैं PNG में क्रॉप कर सकता हूँ?** हाँ – क्रॉप की गई बिटमैप को PNG फ़ाइल के रूप में सहेजें (Step 6 देखें)  
- **क्या मुझे लाइसेंस चाहिए?** डेवलपमेंट के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है  
- **क्या बैच प्रोसेसिंग संभव है?** बिल्कुल – कई फ़ाइलों को सेकंडों में प्रोसेस करने के लिए वही चरणों को लूप में रैप करें  

## PNG में बैच क्रॉप इमेज कैसे करें?
प्रत्येक स्रोत फ़ाइल को `new Bitmap(path)` से लोड करें, क्रॉप एरिया के लिए एक मेल खाता खाली `Bitmap` बनाएं, चयनित आयत को `Graphics.DrawImage` से ड्रॉ करें, और अंत में `Save("output.png", ImageFormat.Png)` को कॉल करें। इन छह लाइनों को एक `foreach` लूप में रैप करें जो किसी डायरेक्टरी पर इटररेट करता है और आपके पास एक पूर्ण बैच‑क्रॉप समाधान होगा जो सेकंडों में दर्जनों इमेज प्रोसेस करता है।

## बैच क्रॉपिंग के लिए Aspose.Drawing का उपयोग क्यों करें?
Aspose.Drawing **Windows, Linux, और macOS** पर चलता है, सामान्य सर्वर‑क्लास CPU पर **0.5 सेकंड से कम समय में 500‑प्लस‑पिक्सेल इमेज** प्रोसेस करता है, और **50+ इमेज फॉर्मेट** को पूर्ण अल्फा‑चैनल प्रिज़र्वेशन के साथ सपोर्ट करता है। क्योंकि यह नेटिव GDI+ डिपेंडेंसी को समाप्त करता है, आप वही कोड कंटेनर्स, Azure App Service, या AWS Lambda पर अतिरिक्त लाइब्रेरीज़ के बिना डिप्लॉय कर सकते हैं, जिससे यह बड़े‑पैमाने पर इमेज पाइपलाइन के लिए आदर्श बनता है।

## “crop image to PNG” क्या है?
`crop image to PNG` ऑपरेशन स्रोत बिटमैप से एक आयताकार क्षेत्र निकालता है और उस क्षेत्र को PNG फ़ाइल में लिखता है। PNG किसी भी अल्फा चैनल को संरक्षित रखता है, लॉसलेस कम्प्रेशन प्रदान करता है, जिससे परिणामस्वरूप इमेज थंबनेल, आइकन, UI एसेट्स, या किसी भी स्थिति में जहाँ क्वालिटी और ट्रांसपेरेंसी आवश्यक है, के लिए आदर्श बनती है।

## Aspose.Drawing System.Drawing का विकल्प क्यों है?
Aspose.Drawing System.Drawing के लिए एक ड्रॉप‑इन रिप्लेसमेंट के रूप में कार्य करता है, पूर्ण क्रॉस‑प्लेटफ़ॉर्म संगतता प्रदान करके, नेटिव GDI+ लाइब्रेरीज़ की आवश्यकता को समाप्त करता है। यह पिक्सेल फ़ॉर्मेट्स की विस्तृत रेंज को सपोर्ट करता है, हाई‑परफ़ॉर्मेंस इमेज मैनिपुलेशन प्रदान करता है, और अल्फा‑चैनल हैंडलिंग तथा व्यापक फ़ॉर्मेट सपोर्ट जैसी एडवांस्ड फीचर्स शामिल करता है, जिससे यह सरल एडिट्स और बड़े‑पैमाने के बैच प्रोसेसिंग दोनों के लिए उपयुक्त है।

## पूर्वापेक्षाएँ
Before we dive in, make sure you have:

- **Aspose.Drawing लाइब्रेरी** को अपने .NET प्रोजेक्ट में इंटीग्रेट करें। आप इसे [Aspose.Drawing download page](https://releases.aspose.com/drawing/net/) से डाउनलोड कर सकते हैं।  
- एक फ़ोल्डर जिसमें वह स्रोत इमेजेज़ हों जिन्हें आप क्रॉप करना चाहते हैं। कोड स्निपेट्स में `"Your Document Directory"` को अपने मशीन पर वास्तविक पाथ से बदलें।

## नेमस्पेस इम्पोर्ट करें
`System.Drawing` नेमस्पेस हमें `Bitmap`, `Graphics`, और संबंधित टाइप्स तक पहुँच देता है जिन्हें Aspose.Drawing विस्तारित करता है।

```csharp
using System.Drawing;
```

## चरण‑दर‑चरण गाइड

### चरण 1: एक बिटमैप कैनवास बनाएं
`Bitmap` Aspose.Drawing की इमेज की इन‑मेमोरी प्रतिनिधित्व है, जो पिक्सेल‑लेवल एक्सेस और फ़ॉर्मेट कंट्रोल प्रदान करता है।  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

हम एक खाली कैनवास से शुरू करते हैं जिसका आकार क्रॉप किए गए परिणाम को रखने के लिए उपयुक्त है। चौड़ाई और ऊँचाई को उस क्षेत्र के आयामों के अनुसार समायोजित करें जिसे आप निकालने की योजना बना रहे हैं।

### चरण 2: एक ग्राफ़िक्स ऑब्जेक्ट बनाएं
`Graphics` वह ड्रॉइंग सतह है जो आपको शेप्स, टेक्स्ट, या अन्य इमेजेज़ को एक Bitmap पर रेंडर करने देती है।  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` ऑब्जेक्ट हमें कैनवास पर ड्रॉ करने देता है। `InterpolationMode` स्केलिंग या ट्रांसफ़ॉर्मेशन के दौरान पिक्सेल वैल्यूज़ की गणना को नियंत्रित करता है—`NearestNeighbor` तीखे किनारों के लिए अच्छा काम करता है।

### चरण 3: क्रॉप करने के लिए इमेज लोड करें
`Image` (या `Bitmap`) स्रोत फ़ाइल को मेमोरी में लोड करता है, जिससे वह मैनिपुलेशन के लिए तैयार हो जाता है।  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

स्रोत इमेज लोड करें। सुनिश्चित करें कि पाथ एक मौजूदा फ़ाइल की ओर इशारा कर रहा है; अन्यथा एक एक्सेप्शन थ्रो होगा।

### चरण 4: स्रोत और गंतव्य आयतें परिभाषित करें
`Rectangle` ऑब्जेक्ट्स स्रोत इमेज के उस क्षेत्र का वर्णन करते हैं जिसे रखना है और इसे गंतव्य कैनवास पर कहाँ रखा जाना चाहिए।  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` API को बताता है कि मूल इमेज का कौन सा भाग रखना है। यहाँ हम टॉप‑लेफ़्ट 50 × 40 पिक्सेल क्षेत्र चुनते हैं। वही आयत `destinationRectangle` को असाइन करके, हम क्रॉप किए गए क्षेत्र को उसके मूल आकार में रखते हैं।

### चरण 5: क्रॉप ऑपरेशन निष्पादित करें
`Graphics.DrawImage` `image` के परिभाषित हिस्से को हमारे खाली `bitmap` पर कॉपी करता है।  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

यह मुख्य **crop image to PNG** ऑपरेशन है। यह मेथड स्रोत आयत का सम्मान करता है और केवल चयनित पिक्सेल्स को गंतव्य बिटमैप में लिखता है।

### चरण 6: क्रॉप की गई इमेज को सहेजें (crop image to PNG)
`Bitmap.Save` इन‑मेमोरी बिटमैप को निर्दिष्ट फ़ॉर्मेट का उपयोग करके फ़ाइल में लिखता है।  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

अंत में, कैनवास को डिस्क पर PNG फ़ाइल के रूप में लिखें। PNG किसी भी अल्फा चैनल को संरक्षित रखता है और लॉसलेस क्वालिटी प्रदान करता है—UI एसेट्स के लिए आदर्श।

## लूप में इमेजेज़ को बैच क्रॉप कैसे करें?
`foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` के साथ प्रत्येक फ़ाइल पाथ पर इटररेट करें, लूप के अंदर चरण 1‑6 दोहराएँ, और प्रत्येक परिणाम को लक्ष्य फ़ोल्डर में स्टोर करें। यह पैटर्न रैखिक रूप से स्केल करता है, `Parallel.ForEach` के साथ समानांतर किया जा सकता है जिससे थ्रूपुट और तेज़ हो जाता है, और इमेजेज़ को कुशलता और तेजी से प्रोसेस करता है।

## सामान्य जाल और टिप्स
- **Pixel format mismatches** – सुनिश्चित करें कि स्रोत इमेज और कैनवास बिटमैप एक संगत पिक्सेल फ़ॉर्मेट साझा करते हों ताकि रंग शिफ्ट से बचा जा सके।  
- **Disposal of GDI objects** – `Bitmap` और `Graphics` को `using` स्टेटमेंट्स में रैप करें या मैन्युअली `Dispose()` कॉल करें; अन्यथा आप अनमैनेज्ड रिसोर्सेज़ लीक कर सकते हैं।  
- **Coordinate errors** – आयत के कोऑर्डिनेट्स ज़ीरो‑बेस्ड होते हैं। ऐसी आयत चुनना जो स्रोत इमेज की सीमाओं से बाहर हो, एक एक्सेप्शन उठाएगा।  

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.Drawing का उपयोग करके किसी भी फ़ॉर्मेट की इमेज को क्रॉप कर सकता हूँ?**  
A: हाँ, Aspose.Drawing विभिन्न फ़ॉर्मेट्स (PNG, JPEG, BMP, GIF, TIFF, आदि) को सपोर्ट करता है, इसलिए आप लगभग किसी भी इमेज टाइप को क्रॉप कर सकते हैं।

**Q: क्या उन्नत क्रॉपिंग विकल्प उपलब्ध हैं?**  
A: बिल्कुल। आप `GraphicsPath`, `Matrix` ट्रांसफ़ॉर्मेशन को मिलाकर, या `ImageProcessor` क्लास का उपयोग करके अधिक जटिल चयन जैसे सर्कुलर क्रॉप्स कर सकते हैं।

**Q: क्या मैं एक इमेज पर कई क्रॉप ऑपरेशन्स लागू कर सकता हूँ?**  
A: हाँ। पहले क्रॉप के बाद, आप परिणामस्वरूप बिटमैप को नए स्रोत के रूप में पुनः उपयोग कर सकते हैं और प्रक्रिया को दोहराकर कई क्रॉप्स को चेन कर सकते हैं।

**Q: क्या Aspose.Drawing बैच इमेज प्रोसेसिंग के लिए उपयुक्त है?**  
A: बिल्कुल। इसका हल्का API और नेटिव डिपेंडेंसीज़ की कमी इसे सर्वरों पर बड़ी इमेज कलेक्शन प्रोसेस करने के लिए परफेक्ट बनाती है।

**Q: Aspose.Drawing‑संबंधित प्रश्नों के लिए मैं समर्थन कैसे प्राप्त कर सकता हूँ?**  
A: सहायता के लिए [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) पर जाएँ और समुदाय से जुड़ें।

**अंतिम अपडेट:** 2026-10-13  
**परीक्षण किया गया:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल्स

- [Aspose.Drawing के साथ BMP को PNG और अन्य फ़ॉर्मेट में लोड और कनवर्ट करें](/drawing/net/image-editing/load-save/)
- [Aspose.Drawing for .NET को लाइसेंस कैसे करें – aspose.drawing को लाइसेंस करने का तरीका](/drawing/net/licensing/)
- [Aspose.Drawing API for .NET का उपयोग करके रेक्टैंगल ड्रॉ करना – कोऑर्डिनेट सिस्टम ट्रांसफ़ॉर्मेशन (पेज ट्रांसफ़ॉर्मेशन)](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}