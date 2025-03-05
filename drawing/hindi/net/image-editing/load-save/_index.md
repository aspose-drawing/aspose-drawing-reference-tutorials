---
title: Aspose.Drawing में छवियाँ लोड करना और सहेजना
linktitle: Aspose.Drawing में छवियाँ लोड करना और सहेजना
second_title: Aspose.Drawing .NET API - System.Drawing.Common का विकल्प
description: Aspose.Drawing के साथ .NET में इमेज लोडिंग और सेविंग में महारत हासिल करें। बीएमपी, जीआईएफ, जेपीजी, पीएनजी, टीआईएफएफ प्रारूपों को आसानी से एक्सप्लोर करें।
type: docs
weight: 13
url: /hi/net/image-editing/load-save/
---
## परिचय

.NET के लिए Aspose.Drawing का उपयोग करके छवि लोडिंग और सेविंग में महारत हासिल करने के बारे में हमारी चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है! यदि आप विभिन्न छवि प्रारूपों में सहजता से हेरफेर करने में अपने कौशल को बढ़ाना चाह रहे हैं, तो आप सही जगह पर हैं। .NET के लिए Aspose.Drawing एक शक्तिशाली लाइब्रेरी है जो छवियों के साथ काम करने की प्रक्रिया को सरल बनाती है, और इस ट्यूटोरियल में, हम विभिन्न प्रारूपों में छवियों को लोड करने और सहेजने के बारे में जानेंगे।

## आवश्यक शर्तें

इससे पहले कि हम इस सीखने की यात्रा पर निकलें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

-  .NET के लिए Aspose.Drawing: सुनिश्चित करें कि आपके पास लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/drawing/net/).

- .NET वातावरण: यह ट्यूटोरियल मानता है कि आपको .NET विकास का कार्यसाधक ज्ञान है।

अब जब हम तैयार हैं, तो आइए आवश्यक नामस्थानों का पता लगाएं और चरण-दर-चरण मार्गदर्शिका पर ध्यान दें।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System.Drawing;
```

ये नामस्थान छवि हेरफेर के लिए आवश्यक मूलभूत कक्षाएं और विधियां प्रदान करते हैं।

## चरण 1: एक छवि लोड करना

आइए एक छवि लोड करके प्रारंभ करें। यह उदाहरण बीएमपी, जीआईएफ, जेपीजी, पीएनजी और टीआईएफएफ जैसे विभिन्न प्रारूपों में छवियों को लोड करता है।

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## चरण 2: LoadAndSave विधि को लागू करना

 अब, तोड़ दो`LoadAndSave` कई चरणों में विधि:

### चरण 2.1: छवि लोड करें

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### चरण 2.2: छवि सहेजें

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // छवि सहेजें
    loadedImage.Save(outputPath);
}
```

प्रत्येक छवि प्रारूप के लिए इन चरणों को दोहराएँ जिसका आप समर्थन करना चाहते हैं।

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.Drawing का उपयोग करके छवियों को लोड करने और सहेजने की कला में महारत हासिल कर ली है। विविध छवि प्रारूपों के साथ काम करने वाले डेवलपर्स के लिए यह कौशल अमूल्य है। इस ज्ञान का प्रयोग करें, अन्वेषण करें और इसे अपनी परियोजनाओं में एकीकृत करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Drawing सभी छवि प्रारूपों के साथ संगत है?

A1: Aspose.Drawing BMP, GIF, JPG, PNG और TIFF सहित कई प्रकार के प्रारूपों का समर्थन करता है।

### Q2: मुझे Aspose.Drawing के लिए विस्तृत दस्तावेज़ कहाँ मिल सकते हैं?

A2: आधिकारिक दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/drawing/net/).

### Q3: मैं Aspose.Drawing के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 ए3: विजिट करें[यहाँ](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस विवरण के लिए.

### Q4: यदि कार्यान्वयन के दौरान मुझे कोई समस्या आती है या मेरे मन में कोई प्रश्न है तो क्या होगा?

 A4: Aspose.Drawing समुदाय से सहायता लें[एस्पोज़ फोरम](https://forum.aspose.com/c/diagram/17).

### Q5: मैं Aspose.Drawing लाइब्रेरी कहां से खरीद सकता हूं?

 A5: आप इसे खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).