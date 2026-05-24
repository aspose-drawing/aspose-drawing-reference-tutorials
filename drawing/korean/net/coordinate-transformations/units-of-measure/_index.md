---
date: 2026-05-24
description: Aspose.Drawing for .NET에서 단위를 설정하는 방법을 배우고, 그래픽 단위를 쉽게 변환하며, 그래픽 렌더링을
  위한 정밀 측정을 마스터하세요.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Aspose.Drawing의 Units of Measure
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET에서 단위 설정 방법 – Units of Measure
url: /ko/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET에서 단위 설정 방법 – 측정 단위

## 소개

Aspose.Drawing for .NET의 세계에 오신 것을 환영합니다. 여기서는 정밀도와 유연성이 그래픽 조작에서 만나게 됩니다. 이 튜토리얼에서는 그림의 **단위 설정 방법**을 발견하고, 포인트, 밀리미터, 인치 간의 **그래픽 단위 변환**을 배우며, 이미지를 픽셀 완벽하게 만드는 실제 예제를 확인하게 됩니다. 보고서, 썸네일 또는 맞춤 차트를 만들든, 측정 단위를 마스터하는 것은 장치 전반에 걸쳐 일관된 렌더링을 위해 필수적입니다.

## 빠른 답변
- **단위를 변경하는 기본 방법은 무엇인가요?** `Graphics` 객체에서 `graphics.PageUnit = PageUnit.Point` (또는 `.Millimeter`, `.Inch`)를 호출합니다.  
- **1/72 인치에 해당하는 단위는 무엇인가요?** 포인트.  
- **인치당 몇 밀리미터인가요?** 25.4 mm = 1 inch.  
- **단위를 사용하기 위해 추가 라이브러리가 필요합니까?** 필요 없습니다. Aspose.Drawing 핵심 라이브러리가 모든 단위 상수를 제공합니다.  
- **하나의 이미지에서 단위를 혼합할 수 있나요?** `Graphics` 인스턴스당 한 번 단위를 설정하고, 일관성을 위해 모든 그리기를 해당 단위로 수행하십시오.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 준비되어 있는지 확인하십시오:

- Aspose.Drawing for .NET: 라이브러리가 설치되어 있는지 확인하십시오. [여기](https://releases.aspose.com/drawing/net/)에서 다운로드할 수 있습니다.
- 문서 디렉터리: 생성된 문서를 저장할 지정된 디렉터리를 준비하십시오.
- 기본 C# 지식: 이 가이드를 최대한 활용하려면 C#에 대한 기본적인 이해가 권장됩니다.

## 네임스페이스 가져오기

시작하기 전에 Aspose.Drawing을 효과적으로 사용하기 위해 필요한 네임스페이스를 가져오겠습니다:

```csharp
using System.Drawing;
```

이제 각 예제를 여러 단계로 나눠 살펴보겠습니다:

## 단위를 포인트로 설정하는 방법?

`Bitmap` 클래스는 그리기 캔버스로 사용되는 메모리 내 이미지를 나타냅니다. 비트맵을 로드하고 `Graphics` 객체를 만든 다음 페이지 단위를 포인트로 설정하면 — 이는 Aspose.Drawing에게 모든 좌표를 1/72 인치 값으로 해석하도록 지시합니다. 포인트를 사용하면 인쇄 준비 그래픽에 대한 세밀한 제어가 가능하고 선 너비를 높은 정밀도로 지정할 수 있습니다.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 단계 1: 비트맵 생성  
`Bitmap` 클래스는 그리기 캔버스로 사용되는 메모리 내 이미지를 나타냅니다.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 단계 2: Graphics 객체 생성  
`Graphics`는 `Bitmap`에 도형과 텍스트를 렌더링하기 위한 그리기 메서드를 제공합니다.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### 단계 3: 페이지 단위를 포인트로 설정  
`PageUnit`은 페이지 좌표의 측정 단위를 지정하는 열거형입니다. `PageUnit.Point`는 포인트를 측정 단위로 정의합니다 (1 포인트 = 1/72 인치). 이 설정은 이후 모든 그리기 호출에 적용됩니다.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### 단계 4: 포인트 단위로 사각형 그리기  
단위를 설정한 후 사각형을 그리면 지정한 치수가 포인트로 해석되어 정확한 크기를 보장합니다.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## 단위를 밀리미터로 설정하는 방법?

`PageUnit`은 페이지 좌표의 측정 단위를 지정하는 열거형입니다. 밀리미터로 전환하면 엔지니어링 도면을 생성하는 등 메트릭 치수가 필요할 때 유용합니다. Aspose.Drawing은 1 mm를 1/25.4 인치로 처리하여 제조 및 기술 문서에 사용되는 물리적 측정값과 그래픽을 정렬할 수 있게 합니다.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### 단계 1: 페이지 단위를 밀리미터로 설정  
`Graphics` 객체에 `PageUnit.Millimeter`를 할당하면 모든 좌표가 메트릭 시스템에 매핑됩니다.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 단계 2: 밀리미터 단위로 사각형 그리기  
이제 사각형의 너비와 높이가 밀리미터로 표시되어 물리적 측정값에 맞추기 쉽고 인쇄된 출력이 실제 크기와 일치하도록 보장합니다.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 단위를 인치로 설정하는 방법?

`Graphics`는 `Bitmap`에 도형과 텍스트를 렌더링하기 위한 그리기 메서드를 제공합니다. 인치는 많은 미국 기반 디자인 도구의 기본 단위입니다. 단위를 인치로 설정하면 UI 요소를 배치할 때 익숙한 단위로 생각할 수 있으며, 화면 디자인에서 인치가 일반적으로 사용되는 인쇄로 전환하는 것이 간단해집니다.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### 단계 1: 페이지 단위를 인치로 설정  
`PageUnit.Inch`는 좌표 시스템을 변경하여 1 단위가 1 인치가 되도록 하며, 인쇄 지향 레이아웃의 요소 크기를 지정하는 간단한 방법을 제공합니다.

CODE_BLOCK_PLACEHOLDER_10_END

### 단계 2: 인치 단위로 사각형 그리기  
이제 그리는 모든 도형은 인치를 측정 기준으로 사용하므로 인쇄 레이아웃에 이상적이며, 제국 단위에 익숙한 이해관계자에게 치수를 전달하는 데도 적합합니다.

CODE_BLOCK_PLACEHOLDER_11_END

## 결과 저장

예제를 모두 완료한 후, 결과 이미지를 문서 디렉터리에 저장하십시오. `Bitmap.Save` 메서드는 지정한 형식(PNG, JPEG 등)으로 파일을 기록합니다.

CODE_BLOCK_PLACEHOLDER_12_END

이제 Aspose.Drawing for .NET에서 다양한 측정 단위를 성공적으로 활용하여 포인트, 밀리미터, 인치를 사용한 사각형의 시각적 표현을 만들었습니다.

## 왜 Aspose.Drawing의 단위 시스템을 사용해야 할까요?

Aspose.Drawing은 **30개 이상의 이미지 형식**을 지원하며 전체 파일을 메모리에 로드하지 않고 **5000 × 5000 픽셀**까지의 이미지를 처리할 수 있어 대규모 그래픽 생성에 높은 성능을 제공합니다. 단위를 명시적으로 설정하면 추측을 없애고 변환 오류를 줄이며 모든 플랫폼에서 출력이 정확한 물리적 치수와 일치하도록 보장합니다.

## 일반적인 문제와 해결책

- **저장 후 예상치 못한 크기** – `graphics.PageUnit`을 모든 그리기 호출 **이전에** 설정했는지 확인하십시오; 나중에 단위를 변경해도 기존 도형의 크기가 자동으로 조정되지 않습니다.  
- **고 DPI 화면에서 흐릿한 출력** – 목표 DPI에 맞추기 위해 비트맵 해상도를 높이십시오(예: `new Bitmap(width, height, 300)`).  
- **하나의 이미지에서 혼합 단위** – 각 단위마다 별도의 `Graphics` 인스턴스를 만들거나 그리기 전에 수동으로 변환하십시오.

## 자주 묻는 질문

### Q1: Aspose.Drawing for .NET을 다른 .NET 프레임워크와 함께 사용할 수 있나요?
A1: 예, Aspose.Drawing은 다양한 .NET 프레임워크와 호환되어 개발 환경에 유연성을 제공합니다.

### Q2: 무료 체험판을 이용할 수 있나요?
A2: 예, 무료 체험판을 통해 Aspose.Drawing을 살펴볼 수 있습니다 [here](https://releases.aspose.com/).

### Q3: Aspose.Drawing for .NET에 대한 지원은 어떻게 받나요?
A3: 커뮤니티 지원 및 토론을 위해 [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)을 방문하십시오.

### Q4: 단기 프로젝트를 위한 임시 라이선스를 구매할 수 있나요?
A4: 예, 임시 라이선스를 [here](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

### Q5: Aspose.Drawing에 대한 자세한 문서는 어디서 찾을 수 있나요?
A5: 포괄적인 문서는 [here](https://reference.aspose.com/drawing/net/)에서 확인할 수 있습니다.

---

**마지막 업데이트:** 2026-05-24  
**테스트 환경:** Aspose.Drawing 24.11 for .NET  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [좌표계 변환 – Aspose.Drawing for .NET의 페이지 변환](/drawing/net/coordinate-transformations/page-transformation/)
- [행렬 변환 튜토리얼: Aspose.Drawing for .NET의 행렬 변환](/drawing/net/coordinate-transformations/matrix-transformations/)
- [변환 적용 방법: Aspose.Drawing for .NET의 로컬 변환](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}