---
title: .NET용 Aspose. Drawing의 페이지 변환
linktitle: Aspose.드로잉의 페이지 변환
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: Aspose.드로잉을 사용하여 .NET에서 단계별 페이지 변환을 알아보세요. 이 포괄적인 튜토리얼을 통해 그래픽 기술을 향상시키세요.
weight: 13
url: /ko/net/coordinate-transformations/page-transformation/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose. Drawing의 페이지 변환

## 소개

.NET용 Aspose.드로잉을 사용한 페이지 변환에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. 그래픽 및 비트맵 변환 작업 기술을 향상시키려는 경우 올바른 위치에 있습니다. 이 튜토리얼에서는 Aspose. Drawing을 사용하여 페이지를 변환하는 과정을 안내하여 각 단계를 명확하게 이해할 수 있도록 합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Aspose.드로잉 라이브러리: Aspose.드로잉 라이브러리를 다운로드하여 설치하세요. 최신 버전을 찾을 수 있습니다[여기](https://releases.aspose.com/drawing/net/).

- 개발 환경: Visual Studio 또는 기타 선호하는 .NET 개발 도구를 사용하여 개발 환경을 설정합니다.

- 문서 디렉터리: 코드의 "문서 디렉터리"를 변환된 이미지를 저장하려는 실제 디렉터리로 바꿉니다.

이제 전제 조건이 준비되었으므로 단계별 가이드를 진행해 보겠습니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 필요한 네임스페이스를 가져오는 것부터 시작합니다.

```csharp
using System.Drawing;
```

## 1단계: 비트맵 생성

특정 치수와 픽셀 형식을 사용하여 새 비트맵을 만드는 것부터 시작하세요.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

그러면 변환을 위한 빈 캔버스가 초기화됩니다.

## 2단계: 그래픽 객체 생성

비트맵에서 그래픽 개체를 만들어 그 위에 그립니다.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 3단계: 캔버스 지우기

특정 색상(이 경우 회색)으로 캔버스를 채워서 캔버스를 지웁니다.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## 4단계: 변환 설정

페이지 좌표를 장치 좌표로 매핑하는 변환을 설정합니다. 이 예에서는 인치를 사용합니다.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

## 5단계: 직사각형 그리기

지정된 펜으로 직사각형을 그리려면 Graphics 객체를 사용하십시오.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

## 6단계: 이미지 저장

변환된 이미지를 지정된 디렉터리에 저장합니다.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

축하해요! .NET용 Aspose. Drawing을 사용하여 페이지를 성공적으로 변환했습니다.

## 결론

이 튜토리얼에서는 Aspose. Drawing을 사용하여 페이지 변환을 수행하는 기본 단계를 다루었습니다. 다음 단계를 수행하면 이러한 변환을 .NET 애플리케이션에 원활하게 통합할 수 있습니다.

## FAQ

### Q1: Aspose. Drawing을 무료로 사용할 수 있나요?

 A1: Aspose. Drawing은 액세스할 수 있는 무료 평가판을 제공합니다.[여기](https://releases.aspose.com/).

### Q2: Aspose. Drawing에 대한 자세한 문서는 어디서 찾을 수 있나요?

 A2: 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/drawing/net/).

### Q3: Aspose. Drawing에 대한 지원은 어떻게 받을 수 있나요?

 A3: 지원을 받으려면 다음을 방문하세요.[Aspose.드로잉 포럼](https://forum.aspose.com/c/diagram/17).

### Q4: Aspose. Drawing에 임시 라이선스를 사용할 수 있나요?

 A4: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.드로잉은 어디서 구매할 수 있나요?

 A5: Aspose. Drawing을 구매할 수 있습니다.[여기](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
