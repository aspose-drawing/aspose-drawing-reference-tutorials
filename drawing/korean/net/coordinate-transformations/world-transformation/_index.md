---
date: 2026-10-18
description: world transformations를 적용하면서 Aspose.Drawing을 사용해 drawing을 PNG로 변환합니다.
  C#에서 translate, rotate 및 scale 예제를 배우고 투명 PNG를 내보내세요.
keywords:
- convert drawing to png
- save graphics as png
- rotate image .net
- scale graphics .net
- transparent png bitmap
lastmod: 2026-10-18
linktitle: Aspose.Drawing의 world transformation
og_description: Aspose.Drawing을 사용해 drawing을 PNG로 변환하고, world transformations를 적용하여
  투명 PNG를 내보냅니다. .NET용 C# translate, rotate 및 scale 예제를 배우세요.
og_image_alt: Tutorial showing how to convert drawing to PNG using Aspose.Drawing
  with world transformation
og_title: Aspose.Drawing을 사용하여 drawing을 PNG로 변환하는 방법 – world transformation
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  headline: How to convert drawing to PNG with Aspose.Drawing – world transformation
  type: TechArticle
- description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  name: How to convert drawing to PNG with Aspose.Drawing – world transformation
  steps:
  - name: create a bitmap
    text: '**Definition:** `Bitmap` is Aspose.Drawing’s in‑memory representation of
      a raster image that you can draw on or save to disk. We start by creating a
      blank canvas that will hold our drawing. `new Bitmap(width, height, PixelFormat.Format32bppPArgb)`
      creates a 32‑bit per pixel bitmap with premultiplied'
  - name: set the world transformation (graphics translate example)
    text: '**Definition:** `Graphics` is the drawing surface that renders shapes onto
      a `Bitmap`. `TranslateTransform` moves the origin of the coordinate system to
      a new location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height
      / 2)` shifts the (0,0) point to the canvas centre. After this call, an'
  - name: draw a rectangle using the transformed coordinates
    text: '**Definition:** `DrawRectangle` is a method of `Graphics` that renders
      a rectangular outline or filled shape based on the supplied pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width'
  - name: save the result – convert graphics to PNG
    text: '**Definition:** `ImageFormat` is an enumeration that tells the `Save` method
      which file format to use. `Save` writes the bitmap to a file in the specified
      image format. `bitmap.Save(outputPath, ImageFormat.Png)` writes a lossless PNG
      file that can be used directly in web pages or UI components. - PN'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- convert drawing to png
- Aspose.Drawing
- .NET graphics
- PNG export
- world transformation
title: Aspose.Drawing을 사용하여 drawing을 PNG로 변환하는 방법 – world transformation
url: /ko/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing으로 드로잉을 PNG로 변환하기 – 월드 변환

## 비트맵을 PNG로 저장 – 소개

**How to convert drawing to PNG**를 Aspose.Drawing을 사용하여 고품질의 투명 이미지를 실시간으로 생성해야 할 때 흔히 요구되는 작업입니다. 이 튜토리얼에서는 **save bitmap as PNG**를 배우고, translate, rotate, scale과 같은 월드 변환을 적용한 뒤, 그래픽을 PNG로 변환하는 방법을 깨끗하고 유지보수 가능한 C# 코드로 수행하는 방법을 배웁니다. 보고서 엔진, 차트 컴포넌트, 혹은 맞춤 UI 렌더러를 구축하든, 이 단계를 마스터하면 모든 디바이스에서 보기 좋은 동적 이미지를 만들 수 있습니다.

## 빠른 답변
- **What does “world transformation” mean?** 그것은 드로잉의 논리적(월드) 좌표를 페이지(디바이스) 좌표에 매핑하여 단일 매트릭스로 모든 것을 재배치, 회전 또는 스케일링할 수 있게 합니다.  
- **Can I export the result as PNG?** 예 – 드로잉 후에 `bitmap.Save(...)`에 `.png` 확장자를 지정하면 됩니다.  
- **Do I need a license for Aspose.Drawing?** 개발에는 무료 체험판을 사용할 수 있지만, 운영 환경에서는 상용 라이선스가 필요합니다.  
- **Is this compatible with .NET 6/7?** 물론입니다 – Aspose.Drawing은 .NET Framework 4.5+ 및 .NET Core/5/6/7을 지원하며, 현재 .NET 배포의 90 % 이상을 포괄합니다.  
- **How many transformations can I chain?** **multiple graphics transformations**을 순차적으로 적용(translate, rotate, scale 등)해도 성능 저하가 없습니다.

## Aspose.Drawing에서 월드 변환이란?

월드 변환은 드로잉 명령이 사용하는 좌표계를 변경합니다. 기본적으로 (0,0)은 비트맵의 왼쪽 위 모서리입니다. `TranslateTransform`, `RotateTransform`, `ScaleTransform`를 사용하면 원점을 재배치하거나, 도형을 회전하거나, 원본 기하학을 변경하지 않고 크기를 조정할 수 있습니다. 이를 통해 한 번 설계한 후 어떤 크기나 방향에서도 렌더링할 수 있습니다.

## Aspose.Drawing을 사용하여 PNG 저장 방법

`Bitmap` 객체를 로드하고, 해당 `Graphics` 인스턴스에 원하는 월드 변환을 설정한 뒤, 도형을 그리고 마지막으로 `bitmap.Save("output.png", ImageFormat.Png)`를 호출합니다. 이 한 줄 저장 호출은 투명도와 색 정확성을 유지하는 무손실 PNG 파일을 작성하므로 웹 자산 및 UI 오버레이에 이상적입니다. API가 모든 저수준 인코딩을 처리하므로 일반적인 캔버스 크기에서는 1초 이내에 바로 사용할 수 있는 PNG를 얻을 수 있습니다.

## 그래픽 translate 예제를 사용하는 이유

그래픽 translate 예제는 모든 점을 다시 계산하는 대신 드로잉 원점을 한 번 이동할 수 있게 해줍니다. 원점을 캔버스 중앙으로 이동하면 기하학을 단순화하고 코드 중복을 줄이며, 그래픽 엔진이 네이티브 코드에서 행렬 곱셈을 수행하도록 하여 대형 캔버스에서 렌더링 속도를 최대 30 %까지 향상시킬 수 있습니다. 이 패턴은 나중에 회전이나 스케일링을 추가할 때 코드 유지보수를 쉽게 해줍니다.

## 그래픽 translate 예제

**graphics translate example**은 원점을 이동하면 위치 지정이 어떻게 단순해지는지 보여줍니다. 모든 점을 다시 계산하는 대신 좌표계를 한 번 이동하고, 새로운 원점이 캔버스 중앙에 있는 것처럼 그립니다.

## 전제 조건

- **Aspose.Drawing library**를 .NET 프로젝트에 통합 – 공식 [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/)에서 다운로드합니다.  
- 출력 이미지가 저장될 **document directory**.  
- **C#** 구문 및 Visual Studio 또는 선호하는 IDE에 대한 기본적인 이해.  

이제 코드를 살펴보겠습니다!

## 네임스페이스 가져오기

`Bitmap`, `Graphics`, 및 Aspose 드로잉 유틸리티는 이러한 네임스페이스에 포함됩니다.  
**Definition:** `System.Drawing`은 핵심 GDI+ 타입을 제공하고, `Aspose.Drawing`은 이를 크로스‑플랫폼 기능으로 확장하여 Windows, Linux, macOS에서 추가 종속성 없이 동일한 코드를 실행할 수 있게 합니다.

## 단계별 가이드

### Step 1: 비트맵 생성

**Definition:** `Bitmap`은 Aspose.Drawing이 메모리 내에서 래스터 이미지를 나타내는 객체로, 그 위에 그리거나 디스크에 저장할 수 있습니다.

우리는 드로잉을 담을 빈 캔버스를 생성하는 것으로 시작합니다.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`는 프리멀티플라이드 알파를 가진 32비트 픽셀 비트맵을 생성합니다. 이는 투명도를 유지하면서 추가 변환 없이 PNG 출력에 최적화된 포맷입니다.

- **Why 32bppPArgb?** 이 픽셀 포맷은 알파 투명도와 고품질 색 렌더링을 지원하여 PNG 출력에 적합합니다.  
- **Pro tip:** 목표 이미지 크기에 맞게 width/height를 조정하세요; 일반 개발자 노트북에서 1920 × 1080 캔버스는 0.2초 미만에 렌더링됩니다.

### Step 2: 월드 변환 설정 (graphics translate example)

**Definition:** `Graphics`는 `Bitmap` 위에 도형을 렌더링하는 드로잉 표면입니다.

`TranslateTransform`은 좌표계의 원점을 새로운 위치로 이동시킵니다.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`는 (0,0) 점을 캔버스 중앙으로 이동시킵니다. 이 호출 이후에 (0,0) 좌표를 사용해 그린 모든 도형은 이미지 중앙에 나타납니다.

- 이는 (0,0) 점을 (500, 400)으로 이동시켜 1000 × 800 캔버스의 중앙에 배치합니다.  
- 추가 변환을 체인할 수 있습니다: `RotateTransform`은 좌표계를 회전시키고, `ScaleTransform`은 스케일링합니다. 이를 통해 **multiple graphics transformations**을 단일 파이프라인에서 사용할 수 있습니다.

### Step 3: 변환된 좌표를 사용해 사각형 그리기

**Definition:** `DrawRectangle`는 제공된 펜과 좌표를 기반으로 사각형 윤곽선 또는 채워진 도형을 렌더링하는 `Graphics` 메서드입니다.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)`는 변환된 원점으로부터 가로·세로 절반씩 오프셋된 위치에 사각형을 그리므로 캔버스 중앙에 사각형이 배치됩니다.

- 사각형의 왼쪽 위 모서리는 변환된 원점(이미지 중앙)에서 시작합니다.  
- 다른 도형(타원, 선, 사용자 정의 경로)도 자유롭게 실험해 보세요.

### Step 4: 결과 저장 – 그래픽을 PNG로 변환

**Definition:** `ImageFormat`은 `Save` 메서드에 사용할 파일 형식을 알려주는 열거형입니다.

`Save`는 지정된 이미지 형식으로 비트맵을 파일에 기록합니다.  
`bitmap.Save(outputPath, ImageFormat.Png)`는 웹 페이지나 UI 컴포넌트에서 직접 사용할 수 있는 무손실 PNG 파일을 작성합니다.

- PNG는 앞서 설정한 정확한 색상과 투명도를 보존합니다.  
- `"Your Document Directory"`를 실제 머신의 경로로 교체하세요.  
- 배치 처리를 위해 `Bitmap` 객체 컬렉션을 순회하면서 루프 안에서 `Save`를 호출하면, 라이브러리는 200 MB 미만의 RAM으로 수천 개의 이미지를 처리할 수 있습니다.

## 일반적인 문제와 해결책

| Issue | Why it happens | Fix |
|-------|----------------|-----|
| **File not found error** 저장 시 | 대상 폴더가 존재하지 않습니다. | `Save` 호출 전에 프로그램적으로 폴더를 생성합니다 (`Directory.CreateDirectory`). |
| **Blank image** 변환 후 | `TranslateTransform`이 그리기 후에 호출되었습니다. | 변환이 모든 그리기 명령 **이전**에 설정되었는지 확인하세요. |
| **Distorted colors** | 호환되지 않는 픽셀 포맷을 사용했습니다. | PNG 출력에는 `Format32bppPArgb`를 사용하세요. |
| **Out‑of‑memory on large canvases** | 전체 비트맵을 메모리에 로드했습니다. | `Bitmap` 스트리밍 옵션을 사용하거나 이미지를 타일로 분할하세요; Aspose.Drawing은 타일을 독립적으로 렌더링할 수 있습니다. |

## 자주 묻는 질문

**Q: Can I apply more than one transformation?**  
A: 예 – `TranslateTransform`, `RotateTransform`, `ScaleTransform`를 체인하여 단일 그래픽 파이프라인에서 복합 효과를 구현할 수 있습니다.

**Q: Is Aspose.Drawing free for commercial projects?**  
A: 평가용 무료 체험판은 제공되지만, 운영 환경에서는 상용 라이선스가 필요합니다.

**Q: Does this work with .NET Core and .NET 5/6/7?**  
A: 물론입니다. Aspose.Drawing은 .NET Core, .NET 5, .NET 6, .NET 7을 포함한 모든 최신 .NET 런타임을 지원합니다.

**Q: Where can I find the full API reference?**  
A: 전체 문서는 [Aspose.Drawing .NET API 참조](https://reference.aspose.com/drawing/net/)에서 확인할 수 있습니다.

**Q: How do I troubleshoot a missing output file?**  
A: 경로 문자열을 확인하고, 쓰기 권한을 보장하며, `Save` 호출 전에 디렉터리가 존재하는지 확인하세요.

## 결론

이제 Aspose.Drawing을 사용하여 **how to convert drawing to PNG**를 배우고, **world transformation**을 적용했으며, 회전이나 스케일링으로 확장 가능한 **graphics translate example**을 수행했습니다. 이러한 기본 요소를 마스터하면 동적 이미지를 생성하고, 맞춤 차트를 만들며, 모든 .NET 애플리케이션을 위한 실시간 그래픽을 구축할 수 있습니다. 다음으로 매트릭스 기반 변환 튜토리얼을 살펴보면 여러 작업을 단일 매트릭스로 결합하여 성능을 더욱 향상시킬 수 있습니다.

---

**마지막 업데이트:** 2026-10-18  
**테스트 대상:** Aspose.Drawing 24.11 for .NET  
**작성자:** Aspose  
**관련 리소스:** [Aspose.Drawing API 참조](https://reference.aspose.com/drawing/net/) | [무료 체험판 다운로드](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## 관련 튜토리얼

- [매트릭스 변환 튜토리얼: Aspose.Drawing for .NET의 매트릭스 변환](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Aspose.Drawing 글로벌 변환으로 이미지 회전하기](/drawing/net/coordinate-transformations/global-transformation/)
- [좌표계 변환 – Aspose.Drawing for .NET의 페이지 변환](/drawing/net/coordinate-transformations/page-transformation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}