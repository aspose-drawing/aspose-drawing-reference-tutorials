---
title: Aspose.Drawing में आयत बनाना
linktitle: Aspose.Drawing में आयत बनाना
second_title: Aspose.Drawing .NET API - System.Drawing.Common का विकल्प
description: Aspose.Drawing का उपयोग करके .NET में आयत बनाना सीखें। कोड उदाहरणों के साथ चरण-दर-चरण मार्गदर्शिका।
weight: 19
url: /hi/net/lines-curves-and-shapes/draw-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing में आयत बनाना

## परिचय

.NET के लिए Aspose.Drawing का उपयोग करके आयत बनाने के इस व्यापक ट्यूटोरियल में आपका स्वागत है। चाहे आप एक अनुभवी डेवलपर हों या Aspose.Drawing में नए हों, यह मार्गदर्शिका आपको आपके .NET अनुप्रयोगों में आयत बनाने और हेरफेर करने की प्रक्रिया के बारे में बताएगी।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- Aspose.Drawing लाइब्रेरी: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.Drawing लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/drawing/net/).

- विकास परिवेश: अपनी मशीन पर विजुअल स्टूडियो जैसा कार्यशील .NET विकास परिवेश स्थापित करें।

- बुनियादी .NET ज्ञान: .NET प्रोग्रामिंग की बुनियादी बातों से खुद को परिचित करें।

## नामस्थान आयात करें

अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करके प्रारंभ करें। ये नामस्थान ग्राफ़िक्स और ड्राइंग संचालन के साथ काम करने के लिए आवश्यक हैं:

```csharp
using System.Drawing;
```

## चरण 1: एक बिटमैप बनाएं

एक बिटमैप ऑब्जेक्ट बनाकर शुरुआत करें, जो ड्राइंग सतह के रूप में काम करेगा। अपने एप्लिकेशन के लिए आवश्यकतानुसार आयाम और पिक्सेल प्रारूप सेट करें।

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## चरण 2: ग्राफ़िक्स ऑब्जेक्ट बनाएं

इसके बाद, बिटमैप से एक ग्राफ़िक्स ऑब्जेक्ट बनाएं। यह ऑब्जेक्ट आपको विभिन्न ड्राइंग ऑपरेशन करने की अनुमति देता है।

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## चरण 3: आयत के लिए पेन को परिभाषित करें

आयत रूपरेखा के रंग और मोटाई को निर्दिष्ट करने के लिए एक पेन ऑब्जेक्ट को परिभाषित करें।

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## चरण 4: आयत बनाएं

अब, परिभाषित पेन का उपयोग करके बिटमैप पर एक आयत बनाने के लिए ग्राफ़िक्स ऑब्जेक्ट का उपयोग करें। आयत की स्थिति और आयाम निर्दिष्ट करें।

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## चरण 5: छवि सहेजें

खींचे गए आयत को अपनी दस्तावेज़ निर्देशिका या किसी वांछित स्थान पर एक फ़ाइल में सहेजें।

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

बधाई हो! आपने .NET के लिए Aspose.Drawing का उपयोग करके सफलतापूर्वक एक आयत बना लिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.Drawing में आयत बनाने के बुनियादी चरणों का पता लगाया। यह लाइब्रेरी ग्राफिक हेरफेर के लिए शक्तिशाली उपकरण प्रदान करती है, जो इसे .NET डेवलपर्स के लिए एक मूल्यवान संपत्ति बनाती है।

 यदि आपको कोई चुनौती आती है या आपके कोई प्रश्न हैं, तो बेझिझक सहायता लें[Aspose.ड्राइंग फोरम](https://forum.aspose.com/c/diagram/17).

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.Drawing का निःशुल्क उपयोग कर सकता हूँ?

 A1: Aspose.Drawing एक व्यावसायिक लाइब्रेरी है, लेकिन आप इसकी विशेषताओं का पता लगा सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/).

### Q2: मुझे विस्तृत दस्तावेज कहां मिल सकते हैं?

 A2: देखें[प्रलेखन](https://reference.aspose.com/drawing/net/) गहन जानकारी के लिए.

### Q3: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 ए3: ए प्राप्त करें[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) परीक्षण प्रयोजनों के लिए.

### Q4:. क्या Aspose.Drawing जटिल ग्राफ़िक्स कार्यों के लिए उपयुक्त है?

उ4: बिल्कुल! Aspose.Drawing जटिल ग्राफिक संचालन को संभालने के लिए उन्नत सुविधाएँ प्रदान करता है।

### Q5: मैं Aspose.Drawing कहां से खरीद सकता हूं?

 ए5: विजिट करें[यहाँ](https://purchase.aspose.com/buy) लाइसेंस खरीदने के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
