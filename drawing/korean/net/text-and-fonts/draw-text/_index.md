---
date: 2026-09-23
description: Aspose.Drawing for .NET을 사용하여 이미지에 텍스트를 그리는 방법을 배웁니다. 텍스트가 포함된 이미지를 생성하고,
  bitmap에 텍스트를 추가하며, custom fonts를 사용해 bitmap을 PNG로 저장합니다.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Aspose.Drawing으로 텍스트 그리기
og_description: Aspose.Drawing for .NET을 사용하여 이미지에 텍스트를 그리는 방법을 배웁니다. 이 튜토리얼에서는 텍스트가
  포함된 이미지를 생성하고, bitmap에 텍스트를 추가하며, custom fonts를 사용해 bitmap을 PNG로 저장하는 과정을 보여줍니다.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Aspose.Drawing for .NET을 사용하여 이미지에 텍스트 그리기 – 빠른 가이드
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Aspose.Drawing for .NET을 사용하여 이미지에 텍스트 그리기
url: /ko/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET을 사용하여 이미지에 텍스트 그리기

## 소개

이 단계별 가이드에서는 Aspose.Drawing for .NET을 사용하여 **이미지에 텍스트 그리는 방법**을 배웁니다. 동적 텍스트 이미지(*동적 텍스트 이미지*)를 만들든, 기존 비트맵에 텍스트를 추가하든, 맞춤 폰트로 그래픽을 생성하든, 이 튜토리얼은 모든 세부 사항을 안내하여 몇 분 안에 텍스트 그리기를 시작할 수 있도록 도와줍니다. 이 라이브러리는 30개 이상의 GDI+ 메서드를 지원하고 Windows, Linux, macOS에서 실행되며 **외부 종속성 없음**을 제공하므로 서버 측 이미지 생성에 신뢰할 수 있는 선택입니다.

## 빠른 답변
- **사용된 라이브러리는?** Aspose.Drawing for .NET  
- **주요 작업?** 이미지에 텍스트 그리기 (텍스트가 포함된 이미지 생성)  
- **핵심 메서드?** `Graphics.DrawString` (이미지에 문자열 그리기)  
- **출력 형식?** PNG (비트맵을 PNG로 저장)  
- **전제 조건?** .NET 개발 환경 및 Aspose.Drawing 라이브러리  

## Aspose.Drawing으로 텍스트를 그리는 것이란?
Aspose.Drawing으로 텍스트를 그린다는 것은 라이브러리의 GDI+ 호환 API를 사용하여 유니코드 문자열을 래스터 캔버스에 렌더링하는 것을 의미합니다. `Graphics.DrawString` 메서드는 텍스트를 비트맵에 기록하여 폰트, 색상, 정렬 및 안티앨리어싱을 제어할 수 있게 합니다. 이 접근 방식은 System.Drawing.Common을 설치하지 않고도 고품질 이미지를 생성할 수 있게 합니다.

## 이미지에 텍스트를 추가하기 위해 Aspose.Drawing을 사용하는 이유는?
Aspose.Drawing은 네이티브 GDI+ 라이브러리가 필요 없이 이미지에 텍스트를 렌더링하는 신뢰할 수 있는 크로스‑플랫폼 방식을 제공하여 모든 운영 체제에서 일관된 품질과 성능을 제공합니다. 고급 안티앨리어싱, 유니코드 문자 및 맞춤 폰트를 지원하며 .NET 애플리케이션과 원활하게 통합되어 서버‑사이드 이미지 생성 및 데스크톱 도구 모두에 이상적입니다.

- **크로스‑플랫폼 신뢰성** – Windows, Linux, macOS에서 작동합니다.  
- **고급 렌더링** – 선명한 출력을 위한 안티앨리어싱 및 서브픽셀 텍스트 스무딩.  
- **외부 종속성 없음** – 라이브러리는 *텍스트가 포함된 이미지 생성*에 필요한 모든 것을 포함합니다.

## 전제 조건

Before diving in, make sure you have:

- **Aspose.Drawing for .NET** – [Aspose.Drawing 문서](https://reference.aspose.com/drawing/net/)에서 다운로드하십시오.  
- **.NET IDE** – Visual Studio 또는 VS Code와 같은 IDE.

## 네임스페이스 가져오기

필요한 네임스페이스를 가져오는 것으로 시작합니다:

이 네임스페이스는 `Bitmap`, `Graphics` 및 텍스트 렌더링 유틸리티와 같은 핵심 GDI+ 타입을 제공합니다.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 1단계: 비트맵 및 그래픽 객체 생성

`Bitmap`은 픽셀 데이터를 위한 Aspose.Drawing의 래스터 이미지 컨테이너이며, `Graphics`는 그 위에 도형과 텍스트를 렌더링하는 그리기 메서드를 제공합니다.

`Bitmap`은 메모리상의 이미지를 나타내고, `Graphics`는 해당 비트맵에 렌더링하는 그리기 메서드를 제공합니다.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

여기서는 최종 이미지를 담을 `Bitmap`과 그 위에 그릴 수 있는 `Graphics` 객체를 생성합니다. 안티앨리어싱 힌트는 텍스트가 부드럽게 보이도록 보장합니다.

## 2단계: 브러시, 펜 및 폰트 설정

`Brush`는 채우기 색을 정의하고, `Pen`은 도형의 외곽선을 그리고, `Font`는 텍스트 렌더링을 위한 서체, 크기 및 스타일을 지정합니다.

`Brush`는 색으로 도형을 채우고, `Pen`은 도형의 외곽선을 그리며, `Font`는 텍스트 렌더링을 위한 서체와 크기를 정의합니다.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** 는 텍스트 색을 정의합니다.  
- **Pen** 은 나중에 텍스트 주위에 사각형을 그리는 데 사용됩니다 (선택 사항).  
- **Font** 은 *이미지에 문자열 그리기* 작업을 위한 서체, 크기 및 스타일을 지정합니다.

## 3단계: 텍스트 및 사각형 정의

`Rectangle`은 텍스트가 배치될 경계 상자를 정의하며, X/Y 좌표와 너비/높이를 지정합니다.

`Rectangle`은 사각형 영역의 위치와 크기를 지정하며, 여기서는 그려진 텍스트를 제한하는 데 사용됩니다.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle`은 텍스트가 배치될 위치를 결정합니다. 레이아웃에 맞게 좌표와 크기를 조정하십시오.

## 4단계: 사각형 및 텍스트 그리기

`Graphics.DrawString`은 제공된 폰트와 브러시를 사용하여 지정된 사각형 안에 지정된 텍스트를 렌더링합니다.

`Graphics.DrawString`은 주어진 폰트와 브러시를 사용하여 지정된 사각형 안에 텍스트 문자열을 렌더링합니다.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

먼저 파란색 사각형으로 영역을 윤곽하고, 그 다음 `DrawString`을 호출하여 **비트맵에 텍스트를 추가**합니다. 이것이 이미지에 *텍스트 그리기*의 핵심입니다.

## 5단계: 결과 저장

이미지는 PNG 파일로 저장되며, *비트맵을 PNG로 저장* 요구사항을 충족합니다. 자리표시자 경로를 파일을 저장하려는 실제 폴더 경로로 교체하십시오.

`bitmap.Save`는 선택한 형식(PNG 등)으로 이미지를 파일에 기록합니다.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## 일반적인 사용 사례

- **개인화된 이름이 포함된 인증서 생성**.  
- **웹 갤러리를 위한 워터마크 썸네일 생성**.  
- **레이블이나 주석이 포함된 동적 차트 구축**.  

## 문제 해결 및 팁

- **폰트를 찾을 수 없나요?** 호스트 머신에 폰트가 설치되어 있는지 확인하거나 개인 폰트 컬렉션을 사용하십시오.  
- **텍스트가 잘리나요?** 사각형 크기를 늘리거나 폰트 크기를 줄이십시오.  
- **성능 문제가 있나요?** 가능한 경우 동일한 `Graphics` 객체를 여러 그리기 작업에 재사용하십시오.  

## 자주 묻는 질문

**Q: 출력 형식을 JPEG로 변경하려면 어떻게 해야 하나요?**  
A: `Save` 메서드에서 `.png` 확장자를 `.jpg`로 교체하고, 필요에 따라 JPEG 품질을 지정하기 위해 `ImageCodecInfo`를 지정하십시오.

**Q: 다중 라인 텍스트를 그릴 수 있나요?**  
A: 예, 문자열에 줄바꿈 문자(`\n`)를 포함하거나 `StringFormat`을 `FormatFlags.LineLimit`와 함께 사용하십시오.

**Q: 그리기 전에 텍스트 크기를 측정할 방법이 있나요?**  
A: `Graphics.MeasureString`을 사용하여 렌더링된 텍스트의 정확한 크기를 얻을 수 있습니다.

**Q: Aspose.Drawing이 유니코드 문자를 지원하나요?**  
A: 물론입니다. 필요한 글리프를 포함하는 폰트를 제공하면 라이브러리가 올바르게 렌더링합니다.

**Q: 테스트에 사용된 Aspose.Drawing 버전은 무엇인가요?**  
A: 예제는 Aspose.Drawing 24.11 for .NET으로 테스트되었습니다.

---

**마지막 업데이트:** 2026-09-23  
**테스트 환경:** Aspose.Drawing 24.11 for .NET  
**작성자:** Aspose

## 관련 튜토리얼

- [Bitmap 그래픽 만들기 C# – PNG 이미지 저장 및 Aspose.Drawing에서 설치된 폰트 사용](/drawing/net/text-and-fonts/installed-fonts/)
- [Aspose.Drawing API for .NET을 사용하여 비트맵을 PNG로 저장하는 방법](/drawing/net/image-editing/display/)
- [이미지에 텍스트](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}