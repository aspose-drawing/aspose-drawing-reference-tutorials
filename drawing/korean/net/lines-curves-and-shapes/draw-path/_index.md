---
title: Aspose.드로잉의 경로 그리기
linktitle: Aspose.드로잉의 경로 그리기
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: 이 단계별 가이드를 통해 .NET용 Aspose. Drawing에서 경로를 그리는 방법을 알아보세요. 손쉽게 멋진 그래픽을 만들어 보세요.
weight: 17
url: /ko/net/lines-curves-and-shapes/draw-path/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.드로잉의 경로 그리기

## 소개

.NET용 Aspose.드로잉의 그리기 경로에 대한 포괄적인 가이드에 오신 것을 환영합니다. 노련한 개발자이든 그래픽 프로그래밍을 처음 접하는 사람이든 이 튜토리얼은 Aspose. Drawing을 사용하여 복잡한 경로를 만드는 과정을 안내합니다. Aspose.드로잉은 .NET 애플리케이션에서 그래픽 작업을 단순화하고 이미지 생성, 편집 및 조작을 위한 광범위한 기능을 제공하는 강력한 라이브러리입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제조건이 충족되었는지 확인하십시오.

-  Aspose.드로잉 라이브러리: Aspose.드로잉 라이브러리를 다운로드하여 설치하세요. 도서관을 찾으실 수 있습니다[여기](https://releases.aspose.com/drawing/net/).

- 개발 환경: 필요한 도구를 사용하여 .NET 개발 환경을 설정합니다.

## 네임스페이스 가져오기

프로젝트에서 필수 네임스페이스를 가져오는 것부터 시작하세요.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 1단계: 비트맵 및 그래픽 만들기

작업할 비트맵 및 그래픽 개체를 만드는 것부터 시작합니다.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## 2단계: 펜 및 GraphicsPath 정의

다음으로, 그리기 속성을 지정하는 Pen과 경로를 나타내는 GraphicsPath를 정의합니다.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## 3단계: 선과 도형 추가

GraphicsPath에 선, 직사각형 및 타원을 추가하여 복잡한 경로를 만듭니다.

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## 4단계: 경로 그리기

지정된 Pen을 사용하여 Graphics 객체에 경로를 그립니다.

```csharp
graphics.DrawPath(pen, path);
```

## 5단계: 이미지 저장

마지막으로 생성된 이미지를 원하는 디렉터리에 저장합니다.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

복잡하고 시각적으로 매력적인 경로를 만들려면 필요에 따라 이러한 단계를 반복하십시오.

## 결론

축하해요! .NET용 Aspose.드로잉을 사용하여 경로를 그리는 방법을 성공적으로 배웠습니다. 이 튜토리얼에서는 비트맵 생성, 펜 정의, GraphicsPath 구성 및 다양한 모양 그리기의 기본 사항을 다루었습니다. Aspose.드로잉의 잠재력을 최대한 활용하기 위해 다양한 매개변수와 모양을 실험해 보세요.

## FAQ

### Q1: Aspose. Drawing을 다른 .NET 라이브러리와 함께 사용할 수 있습니까?

A1: 예, Aspose. Drawing은 다른 .NET 라이브러리와 완벽하게 통합되어 개발 프로젝트에 다양성을 제공합니다.

### Q2: 평가판을 사용할 수 있나요?

 A2: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose. Drawing에 대한 지원은 어디서 찾을 수 있나요?

 A3: Aspose. Drawing을 방문하세요.[법정](https://forum.aspose.com/c/drawing/44) 도움과 지역 사회 지원을 위해.

### Q4: 임시 라이센스는 어떻게 얻나요?

 A4: 임시 라이센스 취득[여기](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose. Drawing을 구매할 수 있나요?

 A5: 예, Aspose. Drawing을 구매할 수 있습니다.[여기](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
