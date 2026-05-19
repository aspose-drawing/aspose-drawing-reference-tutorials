---
date: 2026-05-19
description: Aspose.Drawing का उपयोग करके PNG में इमेजेज को बैच में क्रॉप करने के
  लिए चरण-दर-चरण ट्यूटोरियल, जो .NET डेवलपर्स के लिए System.Drawing का विकल्प है।
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: इमेज क्रॉपिंग ट्यूटोरियल – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
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
title: Aspose.Drawing for .NET का उपयोग करके PNG में इमेजेज को बैच में क्रॉप करने
  की विधि
url: /hi/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET का उपयोग करके PNG में बैच क्रॉप इमेज कैसे करें

यदि आपको .NET वातावरण में जल्दी, भरोसेमंद और बड़े पैमाने पर **crop image to PNG** करने की आवश्यकता है, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम एक इमेज लोड करने, क्रॉप एरिया परिभाषित करने, और परिणाम को PNG फ़ाइल के रूप में सहेजने के सटीक चरणों को दिखाएंगे—सभी Aspose.Drawing का उपयोग करके, जो System.Drawing का एक आधुनिक **alternative to System.Drawing** है और क्रॉस‑प्लेटफ़ॉर्म काम करता है। आप यह भी देखेंगे कि कैसे एकल‑इमेज प्रवाह को पूर्ण **batch crop** पाइपलाइन में विस्तारित किया जाए।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी उपयोग करनी चाहिए?** Aspose.Drawing for .NET (System.Drawing.Common का एक पूर्ण‑विशेष विकल्प)  
- **बेसिक क्रॉप करने में कितना समय लगता है?** आमतौर पर आधुनिक CPU पर एक सिंगल इमेज के लिए एक सेकंड से कम  
- **क्या मैं PNG में क्रॉप कर सकता हूँ?** हाँ – क्रॉप किया गया बिटमैप PNG फ़ाइल के रूप में सहेजें (Step 6 देखें)  
- **क्या मुझे लाइसेंस चाहिए?** डेवलपमेंट के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है  
- **क्या बैच प्रोसेसिंग संभव है?** बिल्कुल – कई फ़ाइलों को प्रोसेस करने के लिए वही चरणों को लूप में रैप करें  

## PNG में बैच क्रॉप इमेज कैसे करें?
प्रत्येक स्रोत फ़ाइल को `new Bitmap(path)` से लोड करें, क्रॉप एरिया के लिए एक समान खाली `Bitmap` बनाएं, चयनित आयत को `Graphics.DrawImage` से ड्रॉ करें, और अंत में `Save("output.png", ImageFormat.Png)` कॉल करें। इन छह लाइनों को एक `foreach` लूप में रैप करें जो किसी डायरेक्टरी पर इटररेट करता है और आपके पास एक पूर्ण बैच‑क्रॉप समाधान होगा जो सेकंडों में दर्जनों इमेज प्रोसेस करता है।

## बैच क्रॉपिंग के लिए Aspose.Drawing क्यों उपयोग करें?
Aspose.Drawing **3 प्रमुख ऑपरेटिंग सिस्टम** (Windows, Linux, macOS) को सपोर्ट करता है और सामान्य सर्वर‑क्लास CPU पर **0.5 सेकंड से कम समय में 500‑प्लस‑पिक्सेल इमेज** को संभाल सकता है। इसका API नेटीव GDI+ डिपेंडेंसीज़ से बचता है, जिसका मतलब है कि आप वही कोड कंटेनर्स, Azure App Service, या AWS Lambda पर अतिरिक्त लाइब्रेरीज़ के बिना डिप्लॉय कर सकते हैं। लाइब्रेरी **50+ इमेज फ़ॉर्मैट** और **पूर्ण अल्फा‑चैनल प्रिज़र्वेशन** भी प्रदान करती है, जिससे यह स्केल पर ट्रांसपेरेंट PNG क्रॉपिंग के लिए आदर्श है।

## “crop image to PNG” क्या है?
`crop image to PNG` ऑपरेशन स्रोत बिटमैप से एक आयताकार क्षेत्र निकालता है और उस क्षेत्र को PNG फ़ाइल में लिखता है। PNG किसी भी अल्फा चैनल को संरक्षित रखता है, लॉसलैस कम्प्रेशन प्रदान करता है, जिससे प्राप्त इमेज थंबनेल, आइकन, UI एसेट्स, या किसी भी स्थिति में जहाँ क्वालिटी और ट्रांसपेरेंसी आवश्यक है, के लिए आदर्श बनती है।

## Aspose.Drawing System.Drawing का विकल्प क्यों है?
Aspose.Drawing System.Drawing के लिए एक ड्रॉप‑इन रिप्लेसमेंट के रूप में कार्य करता है, पूरी क्रॉस‑प्लेटफ़ॉर्म संगतता प्रदान करके, नेटीव GDI+ लाइब्रेरीज़ की आवश्यकता को समाप्त करता है। यह विभिन्न पिक्सेल फ़ॉर्मैट्स को सपोर्ट करता है, हाई‑परफ़ॉर्मेंस इमेज मैनिपुलेशन देता है, और उन्नत फीचर्स जैसे अल्फा‑चैनल हैंडलिंग और विस्तृत फ़ॉर्मैट सपोर्ट शामिल करता है, जिससे यह सरल एडिट्स और बड़े‑पैमाने पर बैच प्रोसेसिंग दोनों के लिए उपयुक्त है।

## पूर्वापेक्षाएँ
शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

- **Aspose.Drawing लाइब्रेरी** आपके .NET प्रोजेक्ट में इंटीग्रेटेड। आप इसे [यहाँ](https://releases.aspose.com/drawing/net/) से डाउनलोड कर सकते हैं।  
- एक फ़ोल्डर जिसमें वह स्रोत इमेजेज़ हों जिन्हें आप क्रॉप करना चाहते हैं। कोड स्निपेट्स में `"Your Document Directory"` को अपने मशीन पर वास्तविक पाथ से बदलें।

## नेमस्पेस इम्पोर्ट करें
`System.Drawing` नेमस्पेस हमें `Bitmap`, `Graphics`, और संबंधित टाइप्स तक पहुंच देता है, जिन्हें Aspose.Drawing विस्तारित करता है।

```csharp
using System.Drawing;
```

## चरण‑दर‑चरण गाइड

### चरण 1: एक Bitmap कैनवास बनाएं
`Bitmap` Aspose.Drawing की इमेज की इन‑मेमोरी प्रतिनिधित्व है, जो पिक्सेल‑लेवल एक्सेस और फ़ॉर्मैट कंट्रोल प्रदान करता है।  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### चरण 2: एक Graphics ऑब्जेक्ट बनाएं
`Graphics` वह ड्रॉइंग सतह है जो आपको शेप्स, टेक्स्ट, या अन्य इमेजेज़ को Bitmap पर रेंडर करने देती है।  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

### चरण 3: क्रॉप करने के लिए इमेज लोड करें
`Image` (या `Bitmap`) स्रोत फ़ाइल को मेमोरी में लोड करता है, जिससे वह मैनिपुलेशन के लिए तैयार हो जाता है।  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

### चरण 4: स्रोत और गंतव्य आयतें परिभाषित करें
`Rectangle` ऑब्जेक्ट्स स्रोत इमेज के उस क्षेत्र को वर्णित करते हैं जिसे रखना है और इसे गंतव्य कैनवास पर कहाँ रखना है।  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

### चरण 5: क्रॉप ऑपरेशन करें
`Graphics.DrawImage` `image` के परिभाषित हिस्से को हमारे खाली `bitmap` पर कॉपी करता है।  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

### चरण 6: क्रॉप की गई इमेज सहेजें (Crop Image to PNG)
`Bitmap.Save` इन‑मेमोरी bitmap को निर्दिष्ट फ़ॉर्मैट का उपयोग करके फ़ाइल में लिखता है।  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

## लूप में इमेजेज़ को बैच क्रॉप कैसे करें?
`foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` के साथ प्रत्येक फ़ाइल पाथ पर इटररेट करें, लूप के अंदर चरण 1‑6 दोहराएँ, और प्रत्येक परिणाम को लक्ष्य फ़ोल्डर में सहेजें। यह पैटर्न रैखिक रूप से स्केल करता है, `Parallel.ForEach` के साथ समानांतर किया जा सकता है जिससे थ्रूपुट और तेज़ हो जाता है, और इमेजेज़ को कुशलता और तेजी से प्रोसेस करता है।

## सामान्य समस्याएँ और टिप्स
- **Pixel format mismatches** – सुनिश्चित करें कि स्रोत इमेज और कैनवास bitmap एक संगत पिक्सेल फ़ॉर्मैट साझा करते हों ताकि रंग शिफ्ट से बचा जा सके।  
- **Disposal of GDI objects** – `Bitmap` और `Graphics` को `using` स्टेटमेंट्स में रैप करें या मैन्युअली `Dispose()` कॉल करें; अन्यथा आप अनमैनेज्ड रिसोर्सेज़ लीक कर सकते हैं।  
- **Coordinate errors** – आयत के कोऑर्डिनेट्स ज़ीरो‑बेस्ड होते हैं। ऐसा आयत चुनना जो स्रोत इमेज की सीमाओं से बाहर हो, एक एक्सेप्शन उठाएगा।  

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.Drawing का उपयोग करके किसी भी फ़ॉर्मैट की इमेज को क्रॉप कर सकता हूँ?**  
A: हाँ, Aspose.Drawing विभिन्न फ़ॉर्मैट्स (PNG, JPEG, BMP, GIF, TIFF, आदि) को सपोर्ट करता है, इसलिए आप लगभग किसी भी इमेज टाइप को क्रॉप कर सकते हैं।

**Q: क्या उन्नत क्रॉपिंग विकल्प उपलब्ध हैं?**  
A: बिल्कुल। आप `GraphicsPath`, `Matrix` ट्रांसफ़ॉर्मेशन को संयोजित कर सकते हैं, या अधिक जटिल चयन जैसे सर्कुलर क्रॉप्स के लिए `ImageProcessor` क्लास का उपयोग कर सकते हैं।

**Q: क्या मैं एक ही इमेज पर कई क्रॉप ऑपरेशन्स लागू कर सकता हूँ?**  
A: हाँ। पहले क्रॉप के बाद, आप प्राप्त bitmap को नई स्रोत के रूप में पुनः उपयोग कर सकते हैं और प्रक्रिया को दोहरा कर कई क्रॉप्स को चेन कर सकते हैं।

**Q: क्या Aspose.Drawing बैच इमेज प्रोसेसिंग के लिए उपयुक्त है?**  
A: बिल्कुल। इसका हल्का API और नेटीव डिपेंडेंसीज़ की कमी इसे सर्वरों पर बड़ी इमेज कलेक्शन प्रोसेस करने के लिए परफेक्ट बनाती है।

**Q: Aspose.Drawing‑से संबंधित प्रश्नों के लिए मैं समर्थन कैसे प्राप्त कर सकता हूँ?**  
A: सहायता के लिए [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) पर जाएँ और समुदाय से जुड़ें।

**अंतिम अपडेट:** 2026-05-19  
**परीक्षण किया गया:** Aspose.Drawing 24.11 for .NET  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल्स

- [Aspose.Drawing for .NET के साथ इमेज को PNG में कैसे क्रॉप करें](/drawing/net/image-editing/cropping/)
- [Aspose.Drawing for .NET के साथ इमेज को स्केल कैसे करें](/drawing/net/image-editing/scale/)
- [Aspose.Drawing के साथ BMP को PNG और अन्य फ़ॉर्मैट्स में कैसे कनवर्ट करें](/drawing/net/image-editing/load-save/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}