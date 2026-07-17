---
date: 2026-03-02
description: Aspose.Drawing for .NET का उपयोग करके अपने दस्तावेज़ चित्रण को बेहतर
  बनाएं! स्पष्ट और सूचनात्मक दृश्यों के लिए कॉलआउट कैसे जोड़ें, यह चरण-दर-चरण सीखें।
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: .NET के लिए Aspose.Drawing के साथ कॉलआउट कैसे जोड़ें
url: /hi/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing में कॉलआउट बनाना

## परिचय
यदि आप **कॉलआउट कैसे जोड़ें** इस बारे में सोच रहे हैं कि Aspose.Drawing for .NET का उपयोग करके अपनी छवियों या आरेखों में कैसे जोड़ें, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम पूरी प्रक्रिया को चरण‑बद्ध तरीके से देखेंगे—छवि लोड करने से लेकर सुंदर शैली वाले कॉलआउट ड्रॉ करने तक—ताकि आप अपनी चित्रण को अधिक स्पष्ट और सूचनात्मक बना सकें।

## त्वरित उत्तर
- **मुझे कौन सी लाइब्रेरी चाहिए?** Aspose.Drawing for .NET (आधिकारिक साइट से डाउनलोड योग्य)।  
- **कौन‑से .NET संस्करण समर्थित हैं?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए मुफ्त ट्रायल काम करता है; उत्पादन के लिए व्यावसायिक लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक कॉलआउट के लिए आमतौर पर 10 मिनट से कम।  
- **क्या मैं रंग और फ़ॉन्ट कस्टमाइज़ कर सकता हूँ?** हाँ—सब कुछ मानक GDI+ ऑब्जेक्ट्स (Pen, Font, Brush) द्वारा नियंत्रित होता है।

## Aspose.Drawing में कॉलआउट कैसे जोड़ें
नीचे एक संक्षिप्त, चरण‑बद्ध गाइड है जो दिखाता है **कॉलआउट कैसे जोड़ें** किसी छवि में। कोड को कॉपी करें, पोज़िशन के साथ प्रयोग करें, और स्टाइलिंग को अपने ब्रांड के अनुसार अनुकूलित करें।

## पूर्वापेक्षाएँ
शुरू करने से पहले सुनिश्चित करें कि आपके पास हैं:

- C# प्रोग्रामिंग भाषा का बुनियादी ज्ञान।  
- Aspose.Drawing लाइब्रेरी स्थापित है। आप इसे [यहाँ](https://releases.aspose.com/drawing/net/) से डाउनलोड कर सकते हैं।  
- वह दस्तावेज़ या छवि जहाँ आप कॉलआउट जोड़ना चाहते हैं।

## नेमस्पेस आयात करें
सुनिश्चित करें कि आपके प्रोजेक्ट में आवश्यक नेमस्पेस शामिल हैं:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## चरण 1: छवि लोड करें
उस छवि को लोड करके शुरू करें जहाँ आप कॉलआउट जोड़ना चाहते हैं। `"Your Document Directory"` और `"gears.png"` को अपने वास्तविक डायरेक्टरी और फ़ाइलनाम से बदलें।

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## चरण 2: ग्राफ़िक्स ऑब्जेक्ट बनाएं
छवि से एक `Graphics` ऑब्जेक्ट बनाएं ताकि ड्रॉइंग ऑपरेशन्स किए जा सकें।

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## चरण 3: कॉलआउट स्थितियों को परिभाषित करें
प्रत्येक कॉलआउट के लिए प्रारंभ और समाप्त बिंदु, साथ ही कॉलआउट मान और इकाई को परिभाषित करें।

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## चरण 4: कॉलआउट ड्रॉ करें
`DrawCallOut` मेथड को इम्प्लीमेंट करें ताकि छवि पर कॉलआउट ड्रॉ किए जा सकें।

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## चरण 5: छवि सहेजें
कॉलआउट वाले छवि को अपनी इच्छित डायरेक्टरी में सहेजें।

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## कॉलआउट स्रोत कोड ड्रॉ करें
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## सामान्य समस्याएँ और सुझाव
- **गलत एंकर निर्देशांक** – सुनिश्चित करें कि प्रारंभ और समाप्त बिंदु छवि की सीमा के भीतर हों; अन्यथा कॉलआउट क्लिप हो सकता है।  
- **टेक्स्ट ओवरलैप** – यदि लेबल अन्य ग्राफ़िक्स से टकराता है तो `spaceSize` या फ़ॉन्ट आकार को समायोजित करें।  
- **परफ़ॉर्मेंस** – बहुत बड़ी छवियों के लिए, उपयोग के बाद `Pen`, `Font`, और `Brush` ऑब्जेक्ट्स को डिस्पोज़ करना न भूलें ताकि संसाधन मुक्त हो सकें।

## निष्कर्ष
बधाई हो! अब आप जानते हैं **कॉलआउट कैसे जोड़ें** किसी छवि में Aspose.Drawing for .NET का उपयोग करके। विभिन्न पोज़िशन, रंग, और फ़ॉन्ट के साथ प्रयोग करें ताकि आपका विज़ुअल स्टाइल मेल खाए।

## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं Aspose.Drawing को अन्य प्रकार की चित्रणों के लिए उपयोग कर सकता हूँ?
हाँ, Aspose.Drawing विभिन्न प्रकार की चित्रणों के लिए विस्तृत ड्रॉइंग ऑपरेशन्स का समर्थन करता है।

### क्या Aspose.Drawing विभिन्न इमेज फ़ॉर्मेट्स के साथ संगत है?
बिल्कुल! Aspose.Drawing लोकप्रिय इमेज फ़ॉर्मेट्स जैसे PNG, JPEG, GIF, और अधिक को सपोर्ट करता है।

### मैं अधिक उदाहरण और दस्तावेज़ीकरण कहाँ पा सकता हूँ?
व्यापक दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/drawing/net/) देखें।

### यदि मुझे समस्याएँ आती हैं तो समर्थन कैसे प्राप्त करूँ?
समुदाय समर्थन के लिए [Aspose.Drawing फ़ोरम](https://forum.aspose.com/c/drawing/44) पर जाएँ।

### क्या मैं खरीदने से पहले Aspose.Drawing आज़मा सकता हूँ?
निश्चित रूप से! मुफ्त ट्रायल के लिए [यहाँ](https://releases.aspose.com/) शुरू करें।

**अतिरिक्त प्रश्न‑उत्तर**

**प्र: क्या मैं कॉलआउट लाइन स्टाइल (डैश्ड, डॉटेड) बदल सकता हूँ?**  
**उ: हाँ—लाइन ड्रॉ करने से पहले `Pen.DashStyle` प्रॉपर्टी को कॉन्फ़िगर करें।**

**प्र: क्या कॉलआउट लेबल में बैकग्राउंड रंग जोड़ना संभव है?**  
**उ: बिल्कुल। अपनी इच्छित रंग के साथ `SolidBrush` बनाएं और `DrawString` कॉल करने से पहले टेक्स्ट के पीछे एक रेक्टेंगल भरें।**

**प्र: हाई‑DPI डिस्प्ले पर कॉलआउट समान दिखाने के लिए क्या करना चाहिए?**  
**उ: `graphics.PageUnit = GraphicsUnit.Pixel` सेट करें (जैसा दिखाया गया है) और स्केलिंग को स्थिर रखने के लिए वेक्टर‑आधारित मापों का उपयोग करें।**

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}