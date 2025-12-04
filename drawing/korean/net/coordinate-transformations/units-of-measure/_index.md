---
title: .NET용 Aspose. Drawing의 측정 단위
linktitle: Aspose. Drawing의 측정 단위
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: 정밀 그래픽을 위한 측정 단위를 마스터하는 심층 튜토리얼에서 .NET용 Aspose.드로잉의 다양성을 살펴보세요.
weight: 14
url: /ko/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose. Drawing의 측정 단위

## 소개

그래픽 조작의 정확성과 유연성이 만나는 Aspose. Drawing for .NET의 세계에 오신 것을 환영합니다. 이 튜토리얼에서는 Aspose. Drawing 내의 측정 단위의 복잡성을 탐구하여 이 놀라운 라이브러리의 기능을 활용할 수 있는 단계별 가이드를 제공합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.드로잉: 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/drawing/net/).

- 문서 디렉터리: 생성된 문서를 저장할 지정된 디렉터리가 있습니다.

- 기본 C# 지식: 이 가이드를 최대한 활용하려면 C#에 대한 기본적인 이해가 권장됩니다.

## 네임스페이스 가져오기

시작하기 전에 Aspose.드로잉을 효과적으로 사용하는 데 필요한 네임스페이스를 가져와 보겠습니다.

```csharp
using System.Drawing;
```

이제 각 예를 여러 단계로 나누어 보겠습니다.

## 측정 단위로서의 포인트

1. 비트맵 생성: 지정된 너비와 높이로 비트맵을 초기화합니다.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. 그래픽 만들기: 비트맵에서 그릴 그래픽 개체를 생성합니다.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. 페이지 단위를 포인트로 설정: 포인트를 측정 단위로 정의합니다(1포인트 = 1/72인치).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. 직사각형 그리기: 점을 단위로 하여 직사각형을 그립니다.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## 측정 단위로서의 밀리미터

1. 페이지 단위를 밀리미터로 설정: 측정 단위를 밀리미터(1mm = 1/25.4인치)로 변경합니다.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. 밀리미터 단위로 직사각형 그리기: 밀리미터를 단위로 사용하여 또 다른 직사각형을 그립니다.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## 측정 단위로서의 인치

1. 페이지 단위를 인치로 설정: 측정 단위를 인치로 전환합니다.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. 인치 단위로 직사각형 그리기: 인치를 단위로 사용하여 직사각형을 그립니다.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 결과 저장

예제를 완료한 후 결과 이미지를 문서 디렉터리에 저장합니다.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

이제 Aspose. Drawing for .NET에서 다양한 측정 단위를 성공적으로 탐색하여 포인트, 밀리미터, 인치를 사용하여 직사각형의 시각적 표현을 만들었습니다.

## 결론

이 튜토리얼에서는 .NET용 Aspose. Drawing이 다양한 측정 단위를 처리하는 방법을 살펴보았습니다. 포인트, 밀리미터, 인치를 조작하여 그래픽 제작 시 정확성과 적응성을 얻을 수 있습니다. Aspose.드로잉의 잠재력을 최대한 활용하려면 이러한 개념을 실험해 보세요.

## FAQ

### Q1: 다른 .NET 프레임워크와 함께 .NET용 Aspose. Drawing을 사용할 수 있습니까?

A1: 예, Aspose. Drawing은 다양한 .NET 프레임워크와 호환되어 개발 환경에 유연성을 제공합니다.

### Q2: 무료 평가판을 이용할 수 있나요?

 A2: 예, 무료 평가판을 통해 Aspose. Drawing을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: .NET용 Aspose. Drawing에 대한 지원을 받으려면 어떻게 해야 합니까?

 A3: 다음을 방문하세요.[Aspose.드로잉 포럼](https://forum.aspose.com/c/drawing/44) 커뮤니티 지원 및 토론을 위해.

### Q4: 단기 프로젝트를 위해 임시 라이선스를 구입할 수 있나요?

 A4: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose. Drawing에 대한 자세한 문서는 어디서 찾을 수 있나요?

 A5: 포괄적인 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
