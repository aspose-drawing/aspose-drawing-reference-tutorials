---
date: 2026-07-17
description: Aspose.Drawing for .NET에서 텍스트 정렬을 설정하여 텍스트 오버플로를 방지하고 이미지에 텍스트를 추가하는
  방법을 배웁니다. 단계별 예제와 가이드.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Aspose.Drawing for .NET으로 텍스트 정렬 설정
og_description: Aspose.Drawing for .NET에서 텍스트 정렬을 설정하여 텍스트 오버플로를 방지합니다. 이미지에 문자열을
  그리기, 사각형 안에 텍스트 중앙 정렬, 그리고 System.Drawing 대체 방법을 배워보세요.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: 텍스트 오버플로 방지 – Aspose.Drawing for .NET으로 텍스트 정렬 설정
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: 텍스트 오버플로 방지 – Aspose.Drawing for .NET으로 텍스트 정렬 설정
url: /ko/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 텍스트 오버플로 방지 – Aspose.Drawing으로 텍스트 정렬 설정

## 소개

.NET에서 그래픽을 렌더링하면서 **텍스트 오버플로를 방지**해야 할 때, Aspose.Drawing은 텍스트 위치 지정, 정렬 및 줄 바꿈에 대한 세밀한 제어를 제공합니다. 배지 생성기, 동적 보고서 또는 이미지 기반 출력물을 만들든, 텍스트 정렬을 마스터하면 텍스트가 의도한 사각형 안에 머무르고 깔끔하게 보입니다. 이 가이드에서는 비트맵 캔버스 생성, `StringFormat` 구성, 중앙 정렬된 텍스트가 있는 사각형 그리기, 오버플로 처리, 최종 이미지 저장 과정을 단계별로 안내합니다.

## 빠른 답변
- **“텍스트 정렬 설정”은 무엇을 의미합니까?** 텍스트가 그리기 사각형 내에서 수평 및 수직으로 어떻게 배치되는지를 정의합니다.  
- **어떤 클래스가 정렬을 제어합니까?** `StringFormat`을 사용하면 `Alignment`와 `LineAlignment`를 설정할 수 있습니다.  
- **문자열과 사각형을 함께 그릴 수 있나요?** 예—`Graphics.DrawRectangle`를 사용한 뒤 `Graphics.DrawString`을 호출합니다.  
- **텍스트 오버플로를 어떻게 방지합니까?** 사각형 크기를 조정하거나 텍스트를 여러 줄로 수동 분할합니다.  
- **프로덕션에 라이선스가 필요합니까?** 평가용이 아닌 경우 상업용 Aspose.Drawing 라이선스가 필요합니다.

## Aspose.Drawing에서 **텍스트 정렬 설정**이란 무엇입니까?

`set text alignment`은 `Rectangle` 또는 그리기 영역 내에서 텍스트의 수평(`StringAlignment`) 및 수직(`LineAlignment`) 배치를 구성합니다. 이러한 속성을 조정하면 텍스트가 왼쪽 정렬, 중앙 정렬, 오른쪽 정렬, 위쪽 정렬, 가운데 정렬 또는 아래쪽 정렬 중 어떻게 표시될지를 제어할 수 있어, Aspose.Drawing으로 생성된 그래픽, 배지 및 보고서에서 정밀한 레이아웃을 구현할 수 있습니다.

## 텍스트 정렬에 Aspose.Drawing을 사용하는 이유는 무엇입니까?

Aspose.Drawing은 `System.Drawing.Common`에서 발생하는 GDI+ 제한을 제거합니다. **5가지 주요 .NET 런타임** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6, .NET 7 – 을 지원하며 메모리를 소모하지 않고 **4000 × 4000 px**(≈ 100 MB)까지 이미지를 렌더링할 수 있습니다. 안티앨리어싱, 고 DPI 스케일링 및 완전한 Linux 컨테이너 호환성을 제공하여 어떤 배포 시나리오에서도 픽셀 단위로 완벽한 그래픽을 생성할 수 있습니다.

## 전제 조건

1. **Aspose.Drawing 라이브러리** – [여기](https://releases.aspose.com/drawing/net/)에서 다운로드하십시오.  
2. **개발 환경** – Visual Studio 2022(또는 기타 C# IDE).  
3. **기본 .NET 지식** – C# 프로젝트와 NuGet 패키지에 익숙해야 합니다.

## 네임스페이스 가져오기

시작하려면 필요한 네임스페이스를 범위에 포함시킵니다. 이를 통해 그래픽, 텍스트 렌더링 및 그리기 기본 요소에 접근할 수 있습니다.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Aspose.Drawing으로 텍스트 오버플로를 방지하는 방법은?

Bitmap은 메모리에 저장된 이미지를 나타내는 클래스이며, `RectangleF`는 그리기를 위한 부동 소수점 사각형 영역을 정의합니다. `StringFormat`을 사용하고 `Trimming`을 `StringTrimming.EllipsisCharacter`로 설정하면 초과 문자가 자동으로 생략 부호(…)로 대체되어 텍스트가 사각형 경계를 초과하지 않게 됩니다. 문자열을 먼저 측정하면 사각형을 축소하거나 텍스트를 여러 줄로 분할할지 결정할 수 있어, 넘침 없이 깔끔한 레이아웃을 보장합니다.

비트맵을 로드하고 적절한 크기의 `RectangleF`를 정의한 뒤 `StringTrimming.EllipsisCharacter`가 설정된 `StringFormat`을 사용하면 초과 문자를 자동으로 잘라냅니다. 완전한 제어를 위해 `Graphics.MeasureString`으로 문자열을 측정하고 사각형을 축소하거나 그리기 전에 텍스트를 줄로 분할합니다. 이 방법은 어떤 문자도 시각적 경계 밖으로 새어나가지 않도록 보장합니다.

## 단계 1: Bitmap 및 Graphics 객체 생성  

Bitmap은 메모리 내 이미지이며, Graphics는 해당 비트맵에 대한 그리기 메서드를 제공합니다. 비트맵을 생성하면 그 위에 그릴 수 있는 캔버스가 마련됩니다. `Graphics` 객체는 그리기 표면이며, `TextRenderingHint`를 사용해 고품질 텍스트 렌더링을 활성화합니다.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## 단계 2: **StringFormat** 및 스타일 정의  

StringFormat은 정렬, 줄 간격, 트리밍 등 텍스트 레이아웃 옵션을 지정합니다. 여기서는 `StringFormat` 인스턴스를 구성하여 **텍스트 정렬을 설정**합니다. 또한 문자열을 그릴 때 사용할 브러시, 펜 및 폰트를 준비합니다.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## 단계 3: 텍스트 생성 및 포맷 – **문자열 그리기** 및 **텍스트가 있는 사각형 그리기**  

Graphics.DrawString은 캔버스에 텍스트를 렌더링하고, Graphics.DrawRectangle는 사각형 형태를 그립니다. 텍스트를 구성하고 이를 포함할 사각형을 정의한 뒤, 사각형 테두리와 문자열을 모두 그립니다.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### 텍스트 오버플로 처리 방법

제공된 `text`가 사각형 경계를 초과하면 일반적으로 두 가지 옵션이 있습니다:

1. **사각형 크기 조정** – `rectangle.Width` 또는 `rectangle.Height`를 늘립니다.  
2. **텍스트 분할** – 문자열을 맞는 줄로 나눈 뒤, Y 좌표를 조정하여 각 줄마다 `DrawString`을 호출합니다.

## Aspose.Drawing을 사용해 이미지에 문자열을 그리는 방법은?

Graphics.DrawString은 지정된 폰트와 포맷 옵션을 사용해 텍스트를 그립니다. 비트맵에서 `Graphics` 객체를 인스턴스화한 뒤, 준비된 `StringFormat`을 사용해 `DrawString`을 호출합니다. 이 한 번의 호출로 텍스트를 원하는 정확한 위치에 렌더링하며, 정렬, 트리밍 및 적용된 변환 행렬을 모두 반영합니다. 고품질 렌더링 힌트를 추가하면 고 DPI 디스플레이에서도 출력이 선명하게 유지됩니다.

## 사각형 안에서 텍스트를 중앙에 배치하려면?

StringAlignment는 레이아웃 사각형 내 텍스트의 수평 정렬을 결정합니다. `stringFormat.Alignment = StringAlignment.Center`와 `stringFormat.LineAlignment = StringAlignment.Center`를 설정합니다. 이렇게 하면 텍스트가 사각형 안에서 수평 및 수직으로 중앙에 배치되어 배지, 버튼 또는 라벨 오버레이에 적합합니다. 중앙 배치는 다양한 이미지 크기와 DPI 설정에서도 일관되게 동작하여 균형 잡힌 시각적 모습을 제공합니다.

## 수직 텍스트 정렬을 달성하려면?

LineAlignment는 사각형 내부 텍스트의 수직 배치를 제어합니다. `stringFormat.LineAlignment`에 `StringAlignment.Near`, `Center`, `Far` 값을 사용해 텍스트를 사각형의 위쪽, 중간, 아래쪽에 배치합니다. 텍스트를 회전하면서 수직 정렬을 유지해야 할 경우 `Graphics.TranslateTransform`와 결합하십시오. 줄 정렬을 조정하면 변환 후에도 다중 줄 블록이 기대한 위치에 정확히 맞춰집니다.

## 단계 4: 출력 저장 – **이미지에 텍스트 추가**

마지막으로 비트맵을 디스크에 저장합니다. 이 단계에서는 **이미지에 텍스트 추가**를 한 번의 호출로 보여줍니다.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|----------|
| **텍스트가 흐릿하게 보임** | `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`가 설정되어 있는지 확인하십시오. |
| **텍스트가 잘림** | 사각형 크기를 늘리거나 문자열 크기(`Graphics.MeasureString`)를 측정하여 단어 자동 줄바꿈 로직을 활성화하십시오. |
| **폰트를 찾을 수 없음** | 호스트 머신에 폰트가 설치되어 있는지 확인하거나 `PrivateFontCollection`을 사용해 개인 폰트를 포함하십시오. |
| **예상치 못한 색상** | 브러시와 펜 색상을 다시 확인하십시오; `Color.FromKnownColor`는 시스템 정의 색상을 사용한다는 점을 기억하십시오. |

## 자주 묻는 질문

**Q1: Aspose.Drawing이 모든 .NET 버전과 호환됩니까?**  
A1: 예, Aspose.Drawing은 다양한 .NET 버전과 호환되도록 설계되어 개발자에게 유연성을 제공합니다.

**Q2: 폰트 스타일을 더 커스터마이즈할 수 있나요?**  
A2: 물론입니다! 원하는 폰트 크기, 스타일 및 패밀리를 얻기 위해 `Font` 객체 매개변수를 조정하십시오.

**Q3: 정의된 사각형 내에서 텍스트 오버플로를 어떻게 처리할 수 있나요?**  
A3: 사각형 크기를 조정하거나 긴 텍스트를 처리하는 맞춤 로직을 구현하여 텍스트 오버플로를 관리할 수 있습니다.

**Q4: Aspose.Drawing에서 사용할 수 있는 다른 포맷 옵션이 있나요?**  
A4: 예, Aspose.Drawing은 텍스트, 도형 및 기타 요소에 대한 다양한 포맷 옵션을 포함한 포괄적인 그래픽 조작 도구 세트를 제공합니다.

**Q5: Aspose.Drawing에 대한 추가 지원은 어디서 찾을 수 있나요?**  
A5: 커뮤니티 지원 및 토론을 위해 Aspose.Drawing 포럼을 [여기](https://forum.aspose.com/c/drawing/44)에서 확인하십시오.

**추가 Q&A**

**Q: 사각형 없이 문자열을 그리려면 어떻게 해야 하나요?**  
A: `DrawRectangle` 호출을 생략하고 원하는 `PointF` 위치를 `Graphics.DrawString`에 전달하십시오.

**Q: 정렬을 유지하면서 텍스트를 회전할 수 있나요?**  
A: 예—그리기 전에 `Graphics` 객체에 `Matrix` 변환을 적용하고, 그 후에 다시 초기화하십시오.

**Q: 이미지를 PNG 대신 JPEG로 내보낼 수 있나요?**  
A: `bitmap.Save`에서 파일 확장자를 변경하고 필요에 따라 `ImageFormat.Jpeg`을 지정하면 됩니다.

---

**마지막 업데이트:** 2026-07-17  
**테스트 환경:** Aspose.Drawing 24.11 for .NET  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.Drawing for .NET으로 텍스트 그리기](/drawing/net/text-and-fonts/draw-text/)
- [Aspose.Drawing에서 이미지에 텍스트 추가](/drawing/net/use-cases/text-on-image/)
- [Aspose.Drawing for .NET으로 텍스트와 폰트 그리기](/drawing/net/text-and-fonts/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}