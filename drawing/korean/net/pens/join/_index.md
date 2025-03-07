---
title: Aspose. Drawing에서 펜을 사용하여 경로 결합
linktitle: Aspose. Drawing에서 펜을 사용하여 경로 결합
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: .NET용 Aspose. Drawing에서 펜을 사용하여 경로를 연결하는 기술을 살펴보세요. LineJoin 옵션으로 멋진 그래픽을 만들어보세요.
weight: 11
url: /ko/net/pens/join/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose. Drawing에서 펜을 사용하여 경로 결합

## 소개

.NET용 Aspose. Drawing의 세계에 오신 것을 환영합니다! 이 튜토리얼에서는 .NET 애플리케이션에서 그래픽 및 이미지 작업을 위한 광범위한 기능을 제공하는 강력한 라이브러리인 Aspose. Drawing을 사용하여 펜으로 경로를 연결하는 기술을 자세히 살펴보겠습니다.

## 전제 조건

흥미진진한 경로 합류의 세계에 뛰어들기 전에 다음 사항이 준비되어 있는지 확인하세요.

1.  Aspose.드로잉 라이브러리: .NET용 Aspose.드로잉 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/drawing/net/).

2. .NET 개발 환경: 컴퓨터에 작동하는 .NET 개발 환경을 설정하십시오.

이제 모든 설정이 완료되었으므로 Aspose. Drawing에서 펜을 사용하여 경로를 연결하는 단계로 넘어가겠습니다.

## 네임스페이스 가져오기

코딩을 시작하기 전에 필요한 클래스와 메서드에 액세스하려면 필요한 네임스페이스를 가져와야 합니다. 코드 시작 부분에 다음 네임스페이스를 추가합니다.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 1단계: 비트맵 및 그래픽 개체 만들기

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

 여기서는 새로운 것을 초기화합니다.`Bitmap` 지정된 크기의 객체를 생성하고`Graphics` 해당 비트맵의 개체입니다.

## 2단계: DrawPath 메서드 정의

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

 이 단계에서는 다음과 같은 메서드를 정의합니다.`DrawPath` 그건 시간이 좀 걸려`Graphics` 객체, 에`LineJoin`열거형 및 수직 위치(`y` )를 매개변수로 사용합니다. 메소드 내부에서 우리는`Pen` 지정된 색상과 너비를 가진 객체`GraphicsPath` 개체를 선택하고 줄을 추가합니다.

## 3단계: Bevel LineJoin을 사용하여 경로 결합

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

 를 불러`DrawPath` 방법`LineJoin.Bevel` 경사선 연결로 경로를 연결합니다.

## 4단계: Round LineJoin을 사용하여 경로 결합

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

 이제`DrawPath` 방법`LineJoin.Round` 둥근 선 결합으로 경로를 결합합니다.

## 5단계: 결과 저장

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

결과 이미지를 원하는 디렉터리에 저장합니다.

이제 Aspose. Drawing에서 펜을 사용하여 결합된 경로를 성공적으로 만들었습니다! 다양한 선 결합 스타일을 실험하고 이를 그래픽에 통합하세요.

## 결론

이 튜토리얼에서는 .NET용 Aspose. Drawing에서 펜으로 경로를 결합하는 과정을 살펴보았습니다. 몇 단계만 거치면 그래픽을 향상하고 시각적으로 매력적인 디자인을 만들 수 있습니다.

## FAQ

### Q1: Aspose. Drawing을 무료로 사용할 수 있나요?

 A1: Aspose. Drawing은 상용 제품이지만 다음을 통해 그 기능을 탐색할 수 있습니다.[무료 시험판](https://releases.aspose.com/).

### Q2: Aspose.드로잉 문서는 어디서 찾을 수 있나요?

 A2: 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/drawing/net/) 종합적인 안내를 위해.

### Q3: Aspose. Drawing에 대한 지원은 어떻게 받을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.드로잉 포럼](https://forum.aspose.com/c/diagram/17) 커뮤니티와 지원을 위해.

### Q4: Aspose. Drawing에 임시 라이선스를 사용할 수 있나요?

 A4: 그렇습니다.[임시 면허증](https://purchase.aspose.com/temporary-license/) 단기 사용을 위해.

### Q5: Aspose.드로잉은 어디서 구매할 수 있나요?

 A5: Aspose.드로잉 구매[여기](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
