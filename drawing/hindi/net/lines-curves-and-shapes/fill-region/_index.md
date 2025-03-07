---
title: Aspose.Drawing में क्षेत्र भरना
linktitle: Aspose.Drawing में क्षेत्र भरना
second_title: Aspose.Drawing .NET API - System.Drawing.Common का विकल्प
description: इस चरण-दर-चरण ट्यूटोरियल से जानें कि .NET के लिए Aspose.Drawing में क्षेत्रों को कैसे भरें। अपने ग्राफ़िक डिज़ाइन कौशल को सहजता से बढ़ाएं।
weight: 20
url: /hi/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing में क्षेत्र भरना

## परिचय

देखने में आकर्षक ग्राफ़िक्स बनाने में अक्सर क्षेत्रों को रंगों, पैटर्नों या ग्रेडिएंट से भरना शामिल होता है। .NET के लिए Aspose.Drawing इसे कुशलतापूर्वक प्राप्त करने के लिए शक्तिशाली उपकरण प्रदान करता है। इस ट्यूटोरियल में, हम Aspose.Drawing, एक बहुमुखी लाइब्रेरी का उपयोग करके क्षेत्रों को भरने की प्रक्रिया में गहराई से उतरेंगे जो .NET अनुप्रयोगों में ग्राफिक संचालन को सरल बनाती है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1.  Aspose.Drawing लाइब्रेरी: Aspose.Drawing लाइब्रेरी डाउनलोड और इंस्टॉल करें। आप पुस्तकालय और उसके दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/drawing/net/).

2. विकास परिवेश: Aspose.Drawing को अपनी परियोजनाओं में एकीकृत करने के लिए विजुअल स्टूडियो जैसा एक .NET विकास परिवेश स्थापित करें।

## नामस्थान आयात करें

अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करके प्रारंभ करें। ये नेमस्पेस Aspose.Drawing के साथ काम करने के लिए आवश्यक कक्षाओं और विधियों तक पहुंच प्रदान करते हैं।

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


अब, आइए स्पष्ट और व्यापक समझ के लिए उदाहरण कोड को कई चरणों में विभाजित करें।

## चरण 1: एक बिटमैप और ग्राफ़िक्स ऑब्जेक्ट बनाएं

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

इस चरण में, हम उस पर चित्र बनाने के लिए एक नया बिटमैप और एक ग्राफ़िक्स ऑब्जेक्ट प्रारंभ करते हैं।

## चरण 2: एक ग्राफ़िक्सपाथ परिभाषित करें और एक क्षेत्र बनाएं

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

बिंदुओं के एक सेट के साथ बहुभुज निर्दिष्ट करके ग्राफ़िक्स पथ परिभाषित करें। इस पथ का उपयोग करके एक क्षेत्र बनाएं.

## चरण 3: एक आंतरिक क्षेत्र को बाहर करें

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

एक आंतरिक आयत का प्रतिनिधित्व करने वाला एक अन्य ग्राफ़िक्स पथ बनाएं और इसे मुख्य क्षेत्र से बाहर रखें।

## चरण 4: एक ब्रश चुनें और क्षेत्र भरें

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

एक ब्रश चुनें (इस मामले में, एक ठोस नीला रंग) और पहले से परिभाषित क्षेत्र को चुने हुए ब्रश से भरें।

## चरण 5: परिणामी छवि सहेजें

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

अंतिम छवि को अपनी इच्छित निर्देशिका में सहेजें।

## निष्कर्ष

.NET के लिए Aspose.Drawing में क्षेत्रों को भरना एक सीधी प्रक्रिया है, जो आपको जटिल और देखने में आकर्षक ग्राफिक्स बनाने की सुविधा प्रदान करती है। अपनी रचनात्मकता को उजागर करने के लिए विभिन्न आकृतियों, रंगों और पैटर्न के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं व्यावसायिक परियोजनाओं के लिए Aspose.Drawing का उपयोग कर सकता हूँ?

 A1: हाँ, Aspose.Drawing का उपयोग व्यक्तिगत और व्यावसायिक दोनों परियोजनाओं के लिए किया जा सकता है। लाइसेंसिंग विवरण के लिए, यहां जाएं[यहाँ](https://purchase.aspose.com/buy).

### Q2: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ2: हाँ, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं Aspose.Drawing के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A3: पर जाएँ[Aspose.ड्राइंग फोरम](https://forum.aspose.com/c/diagram/17) समुदाय और विशेषज्ञों से सहायता प्राप्त करने के लिए।

### Q4: क्या मैं Aspose.Drawing का उपयोग करके गतिशील छवियां उत्पन्न कर सकता हूं?

उ4: बिल्कुल. Aspose.Drawing आपको अपने .NET अनुप्रयोगों में छवियों को गतिशील रूप से बनाने और हेरफेर करने में सक्षम बनाता है।

### Q5: क्या अस्थायी लाइसेंस उपलब्ध हैं?

 A5: हां, अस्थायी लाइसेंस प्राप्त किया जा सकता है[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
