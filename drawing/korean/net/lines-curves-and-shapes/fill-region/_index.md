---
title: Aspose. Drawing의 영역 채우기
linktitle: Aspose. Drawing의 영역 채우기
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: 이 단계별 튜토리얼을 통해 .NET용 Aspose. Drawing에서 영역을 채우는 방법을 알아보세요. 그래픽 디자인 기술을 쉽게 향상시킬 수 있습니다.
type: docs
weight: 20
url: /ko/net/lines-curves-and-shapes/fill-region/
---
## 소개

시각적으로 매력적인 그래픽을 만들려면 영역을 색상, 패턴 또는 그라데이션으로 채우는 작업이 포함되는 경우가 많습니다. Aspose. Drawing for .NET은 이를 효율적으로 달성할 수 있는 강력한 도구를 제공합니다. 이 튜토리얼에서는 .NET 애플리케이션에서 그래픽 작업을 단순화하는 다목적 라이브러리인 Aspose. Drawing을 사용하여 영역을 채우는 프로세스를 자세히 살펴보겠습니다.

## 전제 조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  Aspose.드로잉 라이브러리: Aspose.드로잉 라이브러리를 다운로드하여 설치하세요. 라이브러리와 해당 문서를 찾을 수 있습니다[여기](https://reference.aspose.com/drawing/net/).

2. 개발 환경: Aspose. Drawing을 프로젝트에 통합하려면 Visual Studio와 같은 .NET 개발 환경을 설정하세요.

## 네임스페이스 가져오기

필요한 네임스페이스를 프로젝트로 가져오는 것부터 시작하세요. 이러한 네임스페이스는 Aspose.드로잉 작업에 필요한 클래스 및 메서드에 대한 액세스를 제공합니다.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


이제 명확하고 포괄적인 이해를 위해 예제 코드를 여러 단계로 나누어 보겠습니다.

## 1단계: 비트맵 및 그래픽 개체 만들기

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

이 단계에서는 새 비트맵과 여기에 그릴 그래픽 객체를 초기화합니다.

## 2단계: GraphicsPath 정의 및 영역 생성

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

점 세트로 다각형을 지정하여 그래픽 경로를 정의합니다. 이 경로를 사용하여 지역을 만듭니다.

## 3단계: 내부 지역 제외

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

내부 직사각형을 나타내는 다른 그래픽 경로를 만들고 기본 영역에서 제외합니다.

## 4단계: 브러시를 선택하고 영역 채우기

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

브러시(이 경우 단색 파란색)를 선택하고 이전에 정의한 영역을 선택한 브러시로 채웁니다.

## 5단계: 결과 이미지 저장

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

최종 이미지를 원하는 디렉터리에 저장합니다.

## 결론

.NET용 Aspose. Drawing에서 영역 채우기는 복잡하고 시각적으로 매력적인 그래픽을 생성할 수 있는 유연성을 제공하는 간단한 프로세스입니다. 다양한 모양, 색상, 패턴을 실험하여 창의력을 발휘해보세요.

## FAQ

### Q1: Aspose. Drawing을 상업용 프로젝트에 사용할 수 있나요?

 A1: 예, Aspose. Drawing은 개인 및 상업 프로젝트 모두에 사용할 수 있습니다. 라이선스에 대한 자세한 내용을 보려면 다음을 방문하세요.[여기](https://purchase.aspose.com/buy).

### Q2: 무료 평가판을 이용할 수 있나요?

 A2: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose. Drawing에 대한 지원은 어떻게 받을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.드로잉 포럼](https://forum.aspose.com/c/diagram/17) 지역사회와 전문가로부터 도움을 받으세요.

### Q4: Aspose. Drawing을 사용하여 동적 이미지를 생성할 수 있나요?

A4: 물론이죠. Aspose. Drawing을 사용하면 .NET 애플리케이션에서 이미지를 동적으로 생성하고 조작할 수 있습니다.

### Q5: 임시 라이센스를 사용할 수 있습니까?

 A5: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).