---
title: Aspose. Drawing에 설치된 글꼴 작업
linktitle: Aspose. Drawing에 설치된 글꼴 작업
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: 설치된 글꼴을 조작하는 데 있어 Aspose. Drawing for .NET의 강력한 기능을 살펴보세요. 이 포괄적인 튜토리얼을 통해 이미지 처리 기술을 향상시키세요.
weight: 13
url: /ko/net/text-and-fonts/installed-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose. Drawing에 설치된 글꼴 작업

## 소개

.NET 개발 영역에서 Aspose. Drawing은 이미지를 조작하고 작업하기 위한 강력한 도구로 등장합니다. 이 튜토리얼은 .NET용 Aspose. Drawing을 사용하여 설치된 글꼴로 작업하는 특정 측면에 중점을 둡니다. 글꼴은 디자인과 프리젠테이션에서 중요한 역할을 하며 글꼴 활용을 익히면 이미지 처리 기능이 크게 향상될 수 있습니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  Aspose.드로잉 라이브러리: Aspose.드로잉 라이브러리가 설치되어 있는지 확인하세요. 그렇지 않은 경우 다운로드할 수 있습니다.[여기](https://releases.aspose.com/drawing/net/).

2. 통합 개발 환경(IDE): Visual Studio와 같은 작동 가능한 .NET 개발 환경을 설정합니다.

3. 기본 C# 지식: 제공된 예제를 이해하고 구현하려면 C# 프로그래밍 언어에 대한 지식이 필수적입니다.

## 네임스페이스 가져오기

Aspose. Drawing에 설치된 글꼴 작업을 시작하려면 필요한 네임스페이스를 가져와야 합니다. C# 코드에 다음을 포함합니다.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 1단계: 비트맵 생성

이미지의 캔버스인 비트맵을 만드는 것부터 시작하세요.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 2단계: 그래픽 생성

다음으로 비트맵에서 그래픽을 만들어 그 위에 그립니다.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## 3단계: 브러시 및 글꼴 설정

텍스트의 브러시와 글꼴을 정의합니다.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## 4단계: 설치된 글꼴 정보 표시

이미지에 설치된 글꼴에 대한 정보를 표시합니다.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

## 5단계: 이미지 저장

원하는 디렉터리에 이미지를 저장합니다.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

축하해요! .NET용 Aspose.드로잉을 사용하여 설치된 글꼴에 대한 정보를 표시하는 이미지를 성공적으로 만들었습니다.

## 결론

Aspose. Drawing에 설치된 글꼴 조작을 마스터하면 .NET 애플리케이션에서 시각적으로 매력적인 이미지를 생성할 수 있는 새로운 가능성이 열립니다. 그래픽 콘텐츠의 미학을 향상시키기 위해 다양한 글꼴과 스타일을 실험해보세요.

## FAQ

### Q1: Aspose. Drawing에서 사용자 정의 글꼴을 사용할 수 있습니까?

A1: 예, Font 개체를 생성하는 동안 글꼴 파일의 경로를 지정하여 사용자 정의 글꼴을 사용할 수 있습니다.

### Q2: 글꼴 관련 오류는 어떻게 처리합니까?

A2: 글꼴 관련 문제와 관련된 오류 처리 전략은 Aspose. Drawing 문서를 확인하세요.

### Q3: Aspose.드로잉은 웹 애플리케이션에 적합합니까?

A3: 물론이죠! Aspose.드로잉은 동적 이미지 생성을 위해 웹 애플리케이션에 완벽하게 통합될 수 있습니다.

### Q4: 텍스트 모양을 추가로 사용자 정의할 수 있나요?

A4: 물론이죠! 더 많은 사용자 정의 옵션을 보려면 Font 및 Brush 클래스의 추가 속성을 살펴보세요.

### Q5: 테스트 목적으로 임시 라이센스를 사용할 수 있습니까?

 A5: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/) 평가를 위해.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
