---
title: .NET के लिए Aspose.Drawing में माप की इकाइयाँ
linktitle: Aspose.Drawing में माप की इकाइयाँ
second_title: Aspose.Drawing .NET API - System.Drawing.Common का विकल्प
description: इस गहन ट्यूटोरियल में .NET के लिए Aspose.Drawing की बहुमुखी प्रतिभा का पता लगाएं, सटीक ग्राफिक्स के लिए माप की इकाइयों में महारत हासिल करें।
weight: 14
url: /hi/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Drawing में माप की इकाइयाँ

## परिचय

.NET के लिए Aspose.Drawing की दुनिया में आपका स्वागत है, जहां ग्राफिक हेरफेर में सटीकता और लचीलापन मिलता है। इस ट्यूटोरियल में, हम Aspose.Drawing के भीतर माप की इकाइयों की पेचीदगियों को समझेंगे, और आपको इस उल्लेखनीय लाइब्रेरी की शक्ति का उपयोग करने के लिए चरण-दर-चरण मार्गदर्शिका प्रदान करेंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET के लिए Aspose.Drawing: सुनिश्चित करें कि आपके पास लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/drawing/net/).

- दस्तावेज़ निर्देशिका: एक निर्दिष्ट निर्देशिका रखें जहाँ आप अपने बनाए गए दस्तावेज़ों को सहेजना चाहते हैं।

- बुनियादी सी# ज्ञान: इस गाइड से अधिकतम लाभ उठाने के लिए सी# की बुनियादी समझ की सिफारिश की जाती है।

## नामस्थान आयात करें

शुरू करने से पहले, आइए Aspose.Drawing को प्रभावी ढंग से उपयोग करने के लिए आवश्यक नामस्थान आयात करें:

```csharp
using System.Drawing;
```

अब, आइए प्रत्येक उदाहरण को कई चरणों में तोड़ें:

## माप की इकाइयों के रूप में अंक

1. एक बिटमैप बनाएं: एक निर्दिष्ट चौड़ाई और ऊंचाई के साथ एक बिटमैप प्रारंभ करें।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. ग्राफ़िक्स बनाएं: उस पर चित्र बनाने के लिए बिटमैप से एक ग्राफ़िक्स ऑब्जेक्ट जेनरेट करें।

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. पृष्ठ इकाई को बिंदुओं पर सेट करें: बिंदुओं को माप की इकाई के रूप में परिभाषित करें (1 बिंदु = 1/72 इंच)।

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. आयत बनाएं: बिंदुओं को इकाई मानकर एक आयत बनाएं।

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## माप की इकाइयों के रूप में मिलीमीटर

1. पेज इकाई को मिलीमीटर पर सेट करें: माप की इकाई को मिलीमीटर में बदलें (1 मिमी = 1/25.4 इंच)।

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. मिलीमीटर में आयत बनाएं: मिलीमीटर को इकाई के रूप में उपयोग करके एक और आयत बनाएं।

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## माप की इकाइयों के रूप में इंच

1. पेज इकाई को इंच पर सेट करें: माप की इकाई को इंच में बदलें।

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. इंच में आयत बनाएं: इंच को इकाई मानकर एक आयत बनाएं।

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## परिणाम सहेजें

उदाहरणों को पूरा करने के बाद, परिणामी छवि को अपनी दस्तावेज़ निर्देशिका में सहेजें:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

अब, आपने .NET के लिए Aspose.Drawing में माप की विविध इकाइयों को सफलतापूर्वक नेविगेट कर लिया है, और बिंदुओं, मिलीमीटर और इंच का उपयोग करके आयतों का एक दृश्य प्रतिनिधित्व तैयार किया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया है कि .NET के लिए Aspose.Drawing माप की विभिन्न इकाइयों को कैसे संभालता है। बिंदुओं, मिलीमीटर और इंच में हेरफेर करके, आप अपनी ग्राफिक रचनाओं में सटीकता और अनुकूलनशीलता प्राप्त कर सकते हैं। Aspose.Drawing की पूरी क्षमता को अनलॉक करने के लिए इन अवधारणाओं के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य .NET फ्रेमवर्क के साथ .NET के लिए Aspose.Drawing का उपयोग कर सकता हूँ?

A1: हां, Aspose.Drawing विभिन्न .NET फ्रेमवर्क के साथ संगत है, जो आपके विकास वातावरण में लचीलापन प्रदान करता है।

### Q2: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ2: हां, आप नि:शुल्क परीक्षण के साथ Aspose.Drawing का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं .NET के लिए Aspose.Drawing के लिए समर्थन कैसे प्राप्त करूं?

 A3: पर जाएँ[Aspose.ड्राइंग फोरम](https://forum.aspose.com/c/drawing/44) सामुदायिक समर्थन और चर्चा के लिए।

### Q4: क्या मैं अल्पकालिक परियोजनाओं के लिए अस्थायी लाइसेंस खरीद सकता हूँ?

 उ4: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: मुझे Aspose.Drawing के लिए विस्तृत दस्तावेज़ कहां मिल सकते हैं?

 A5: व्यापक दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
