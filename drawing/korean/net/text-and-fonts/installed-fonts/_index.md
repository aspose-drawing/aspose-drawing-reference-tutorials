---
date: 2025-12-06
description: Aspose.Drawing for .NET를 사용하여 설치된 글꼴을 나열하고, 글꼴 패밀리를 표시하며, 비트맵에서 그래픽을
  생성하고, 글꼴로 텍스트를 그리는 동시에 PNG 이미지 파일을 저장하는 방법을 배웁니다.
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing에서 PNG 이미지 저장 및 설치된 폰트 작업
url: /ko/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG 이미지 저장 및 Aspose.Drawing에서 설치된 폰트 사용하기

## 소개

머신에 설치된 폰트 정보를 표시하는 **PNG 이미지** 파일을 저장해야 한다면, Aspose.Drawing for .NET이 깔끔하고 크로스‑플랫폼 방식으로 이를 제공합니다. 이 튜토리얼에서는 설치된 폰트를 나열하고, 폰트 패밀리를 표시하며, 비트맵에서 그래픽을 생성하고, 폰트를 사용해 텍스트를 그린 뒤 최종적으로 PNG 이미지로 저장하는 과정을 단계별로 살펴봅니다. 끝까지 진행하면 어떤 .NET 프로젝트에도 바로 넣어 사용할 수 있는 재사용 가능한 스니펫을 얻게 됩니다.

## 빠른 답변
- **이 튜토리얼이 만드는 것은?** 설치된 폰트 패밀리를 나열한 PNG 이미지.  
- **필요한 라이브러리는?** Aspose.Drawing for .NET (System.Drawing.Common은 필요 없음).  
- **커스텀 폰트를 사용할 수 있나요?** 예 – `InstalledFontCollection`에 로드하면 됩니다.  
- **출력 해상도를 조정할 수 있나요?** 물론 – 비트맵 크기나 픽셀 포맷을 변경하면 됩니다.  
- **코드를 실행하려면 라이선스가 필요한가요?** 평가용 임시 라이선스로 실행할 수 있지만, 프로덕션에서는 정식 라이선스가 필요합니다.

## Aspose.Drawing에서 “PNG 이미지 저장”이란?
PNG 이미지를 저장한다는 것은 그리기 표면(`Bitmap`)을 `.png` 확장자를 가진 파일로 인코딩하는 것을 의미합니다. Aspose.Drawing이 인코딩을 처리해 주므로 `bitmap.Save(...)`에 원하는 경로만 지정하면 됩니다.

## 설치된 폰트를 나열하고 폰트 패밀리를 표시하는 이유
어떤 폰트가 사용 가능한지 알면 최종 사용자의 환경에 맞춰 동적으로 그래픽을 생성할 수 있습니다. 보고서, 인증서 또는 기업 브랜드와 일치해야 하는 시각적 콘텐츠를 폰트 파일을 배포하지 않고도 만들 때 특히 유용합니다.

## 사전 요구 사항

- **Aspose.Drawing 라이브러리** – 최신 버전을 [Aspose Drawing 다운로드 페이지](https://releases.aspose.com/drawing/net/)에서 받으세요.  
- **IDE** – Visual Studio, Rider 또는 .NET을 지원하는 편집기.  
- **기본 C# 지식** – 클래스, 객체, 간단한 루프에 익숙해야 합니다.

## 네임스페이스 가져오기
폰트와 그래픽을 사용하려면 C# 파일 상단에 다음 네임스페이스를 추가합니다:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 단계별 가이드

### 단계 1: 비트맵 생성 (캔버스)
먼저 최종 이미지를 담을 비트맵을 생성합니다. 비트맵 크기와 픽셀 포맷이 저장되는 PNG의 품질을 결정합니다.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 단계 2: 비트맵에서 그래픽 객체 생성
다음으로 비트맵으로부터 `Graphics` 객체를 얻습니다. 이 객체를 사용해 캔버스에 도형, 텍스트, 이미지를 그릴 수 있습니다.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### 단계 3: 브러시와 폰트 설정 (폰트로 텍스트 그리기)
텍스트 색상을 위한 브러시와 타입페이스, 크기, 스타일을 정의하는 `Font` 객체가 필요합니다.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### 단계 4: 설치된 폰트 나열 및 폰트 패밀리 표시
이제 비트맵에 폰트 패밀리 수와 몇 개의 이름을 직접 표시합니다. 이는 **설치된 폰트 나열** 및 **폰트 패밀리 표시** 기능을 보여줍니다.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### 단계 5: PNG 이미지 저장
마지막으로 비트맵을 PNG 파일로 디스크에 씁니다. 이것이 핵심 **PNG 이미지 저장** 작업입니다.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **프로 팁:** 다양한 운영 체제에서 디렉터리 구분자 문제를 피하려면 `Path.Combine`을 사용해 파일 경로를 구성하세요.

## 일반적인 문제와 해결 방법
| 문제 | 원인 | 해결 방법 |
|------|------|-----------|
| **폰트가 표시되지 않음** | `InstalledFontCollection`이 채워지지 않음(예: 폰트가 없는 헤드리스 서버에서 실행). | 서버에 필요한 폰트를 설치하거나 애플리케이션에 커스텀 폰트를 포함하세요. |
| **저장된 파일이 손상됨** | 잘못된 픽셀 포맷 또는 쓰기 권한 부족. | 대상 폴더가 존재하고 앱에 쓰기 권한이 있는지 확인하고 `Format32bppPArgb`를 유지하세요. |
| **텍스트가 흐릿함** | 낮은 DPI 설정. | 비트맵 크기를 늘리거나 `graphics.SmoothingMode = SmoothingMode.AntiAlias`를 설정하세요. |

## 자주 묻는 질문

**Q: 머신에 설치되지 않은 커스텀 폰트를 사용할 수 있나요?**  
A: 예. 폰트 파일을 `PrivateFontCollection`에 로드하고 해당 컬렉션에서 `Font`를 생성하면 됩니다.

**Q: 폰트 관련 예외를 어떻게 처리하나요?**  
A: 폰트 생성 코드를 `try/catch` 블록으로 감싸고, 누락된 패밀리의 경우 `ArgumentException`을 확인하세요.

**Q: Aspose.Drawing을 웹 애플리케이션에서 사용할 수 있나요?**  
A: 물론입니다. 이 라이브러리는 ASP.NET Core, Azure Functions 등 서버‑사이드 환경에서 동작합니다.

**Q: 텍스트 색상이나 스타일을 바꿀 수 있나요?**  
A: 예. `LinearGradientBrush`와 같은 다양한 `Brush` 타입을 사용하고 `FontStyle` 열거형을 수정하면 됩니다.

**Q: 테스트용 임시 라이선스는 어디서 받을 수 있나요?**  
A: [Aspose 임시 라이선스 페이지](https://purchase.aspose.com/temporary-license/)에서 체험용 라이선스를 다운로드하세요.

## 결론

이 단계들을 따라 하면 Aspose.Drawing for .NET을 사용해 **PNG 이미지** 파일을 동적으로 **설치된 폰트 나열**, **폰트 패밀리 표시**, **비트맵에서 그래픽 생성**, **폰트로 텍스트 그리기**까지 수행하는 방법을 배웠습니다. 프로젝트의 시각적 요구에 맞게 다른 폰트, 색상, 비트맵 크기를 자유롭게 실험해 보세요.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2025-12-06  
**테스트 환경:** Aspose.Drawing 24.11 for .NET  
**작성자:** Aspose