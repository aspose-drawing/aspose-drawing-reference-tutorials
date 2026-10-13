---
date: 2026-10-13
description: Aspose.Drawing API를 사용하여 이미지를 PNG로 일괄 자르는 방법을 배우세요. .NET 개발자를 위한 System.Drawing의
  크로스‑플랫폼 대안입니다.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: 이미지 자르기 튜토리얼 – Aspose.Drawing
og_description: Aspose.Drawing을 사용하여 이미지를 PNG로 빠르게 일괄 자르는 방법을 배우세요. .NET 개발자를 위한 System.Drawing의
  크로스‑플랫폼 대안입니다. 여러 파일을 효율적으로 처리하기 위한 단계별 지침을 따르세요.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Aspose.Drawing for .NET을 사용하여 이미지를 PNG로 일괄 자르는 방법
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Aspose.Drawing for .NET을 사용하여 이미지를 PNG로 일괄 자르기
url: /ko/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET을 사용하여 PNG로 이미지 일괄 자르기

If you need to **crop image to PNG** quickly, reliably, and at scale in a .NET environment, you’re in the right place. In this tutorial we’ll walk through the exact steps to load an image, define the crop area, and save the result as a PNG file—all using Aspose.Drawing, a modern **alternative to System.Drawing** that works cross‑platform. You’ll also see how to extend the single‑image flow into a full **batch crop** pipeline.

## 빠른 답변
- **어떤 라이브러리를 사용해야 하나요?** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **기본 자르기 작업은 얼마나 걸리나요?** Usually under a second for a single image on a modern CPU  
- **PNG로 자를 수 있나요?** Yes – save the cropped bitmap as a PNG file (see Step 6)  
- **라이선스가 필요합니까?** A free trial works for development; a commercial license is required for production  
- **배치 처리도 가능한가요?** Absolutely – wrap the same steps in a loop to process multiple files in seconds  

## PNG로 이미지를 일괄 자르는 방법은?

`new Bitmap(path)`로 각 소스 파일을 로드하고, 자르기 영역에 맞는 빈 `Bitmap`을 생성한 뒤, `Graphics.DrawImage`를 사용해 선택한 사각형을 그립니다. 마지막으로 `Save("output.png", ImageFormat.Png)`를 호출합니다. 이러한 여섯 줄을 디렉터리를 순회하는 `foreach` 루프 안에 넣으면 수십 개의 이미지를 몇 초 만에 처리하는 완전한 배치‑크롭 솔루션이 완성됩니다.

## 배치 크롭에 Aspose.Drawing을 사용하는 이유는?

Aspose.Drawing은 **Windows, Linux, macOS**에서 실행되며, 일반 서버급 CPU에서 **500픽셀 이상의 이미지를 0.5초 미만**에 처리하고, **50개 이상의 이미지 포맷**을 전체 알파 채널 보존과 함께 지원합니다. 네이티브 GDI+ 의존성을 없애기 때문에 동일한 코드를 컨테이너, Azure App Service, AWS Lambda 등에 추가 라이브러리 없이 배포할 수 있어 대규모 이미지 파이프라인에 이상적입니다.

## “crop image to PNG”란 무엇인가요?

`crop image to PNG` 작업은 소스 비트맵에서 사각형 영역을 추출하여 해당 영역을 PNG 파일로 저장합니다. PNG는 알파 채널을 보존하며 무손실 압축을 제공하므로 썸네일, 아이콘, UI 자산 또는 품질과 투명도가 필요한 모든 상황에 이상적인 이미지가 됩니다.

## 왜 Aspose.Drawing이 System.Drawing의 대안인가요?

Aspose.Drawing은 전체 크로스‑플랫폼 호환성을 제공하고 네이티브 GDI+ 라이브러리 필요성을 없애는 System.Drawing의 즉시 대체품 역할을 합니다. 다양한 픽셀 포맷을 지원하고 고성능 이미지 조작을 제공하며, 알파 채널 처리 및 광범위한 포맷 지원과 같은 고급 기능을 포함하고 있어 간단한 편집부터 대규모 배치 처리까지 모두 적합합니다.

## 전제 조건

Before we dive in, make sure you have:

- **Aspose.Drawing 라이브러리**를 .NET 프로젝트에 통합하세요. [Aspose.Drawing 다운로드 페이지](https://releases.aspose.com/drawing/net/)에서 다운로드할 수 있습니다.  
- 자르려는 원본 이미지가 들어 있는 폴더. 코드 스니펫에서 `"Your Document Directory"`를 실제 머신의 경로로 교체하세요.

## 네임스페이스 가져오기

The `System.Drawing` namespace gives us access to `Bitmap`, `Graphics`, and related types that Aspose.Drawing extends.

```csharp
using System.Drawing;
```

## 단계별 가이드

### Step 1: 비트맵 캔버스 만들기

`Bitmap`은 Aspose.Drawing의 메모리 내 이미지 표현으로, 픽셀 수준 접근 및 포맷 제어를 제공합니다.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

We start with a blank canvas sized to hold the cropped result. Adjust the width and height to match the dimensions of the area you plan to extract.

우리는 잘라낸 결과를 담을 수 있는 빈 캔버스로 시작합니다. 너비와 높이를 추출하려는 영역의 크기에 맞게 조정하세요.

### Step 2: Graphics 객체 만들기

`Graphics`는 비트맵에 도형, 텍스트 또는 다른 이미지를 렌더링할 수 있는 그리기 표면입니다.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

A `Graphics` object lets us draw onto the canvas. The `InterpolationMode` controls how pixel values are calculated during scaling or transformation—`NearestNeighbor` works well for sharp edges.

`Graphics` 객체를 사용해 캔버스에 그릴 수 있습니다. `InterpolationMode`는 스케일링이나 변환 시 픽셀 값을 계산하는 방식을 제어하며, `NearestNeighbor`는 선명한 가장자리에 적합합니다.

### Step 3: 자를 이미지 로드하기

`Image`(또는 `Bitmap`)는 소스 파일을 메모리로 로드하여 조작할 준비를 합니다.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Load the source image. Make sure the path points to an existing file; otherwise an exception will be thrown.

소스 이미지를 로드합니다. 경로가 기존 파일을 가리키는지 확인하세요; 그렇지 않으면 예외가 발생합니다.

### Step 4: 소스 및 대상 사각형 정의하기

`Rectangle` 객체는 소스 이미지에서 유지할 영역과 대상 캔버스에 배치될 위치를 설명합니다.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

The `sourceRectangle` tells the API which part of the original image to keep. Here we pick the top‑left 50 × 40 pixel area. By assigning the same rectangle to `destinationRectangle`, we keep the cropped region at its original size.

`sourceRectangle`은 API에 원본 이미지 중 어느 부분을 유지할지 알려줍니다. 여기서는 좌상단 50 × 40 픽셀 영역을 선택합니다. 동일한 사각형을 `destinationRectangle`에 할당하면 잘라낸 영역을 원래 크기로 유지합니다.

### Step 5: 자르기 작업 수행하기

`Graphics.DrawImage`는 정의된 `image`의 부분을 빈 `bitmap`에 복사합니다.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

This is the core **crop image to PNG** operation. The method respects the source rectangle and writes only the selected pixels to the destination bitmap.

이것이 핵심 **crop image to PNG** 작업입니다. 메서드는 소스 사각형을 준수하고 선택된 픽셀만 대상 비트맵에 기록합니다.

### Step 6: 잘라낸 이미지 저장하기 (crop image to PNG)

`Bitmap.Save`는 메모리 내 비트맵을 지정된 포맷으로 파일에 저장합니다.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Finally, write the canvas to disk as a PNG file. PNG preserves any alpha channel and provides lossless quality—ideal for UI assets.

마지막으로 캔버스를 PNG 파일로 디스크에 저장합니다. PNG는 알파 채널을 보존하고 무손실 품질을 제공하므로 UI 자산에 이상적입니다.

## 루프에서 이미지를 일괄 자르는 방법은?

Iterate over each file path with `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, repeat Steps 1‑6 inside the loop, and store each result in a target folder. This pattern scales linearly, can be parallelised with `Parallel.ForEach` for even faster throughput, and processes images efficiently and quickly.

`foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`를 사용해 각 파일 경로를 순회하고, 루프 안에서 단계 1‑6을 반복하며 결과를 대상 폴더에 저장합니다. 이 패턴은 선형적으로 확장되며 `Parallel.ForEach`로 병렬화해 더욱 빠른 처리량을 얻을 수 있고, 이미지를 효율적이고 빠르게 처리합니다.

## 일반적인 함정 및 팁

- **픽셀 포맷 불일치** – 소스 이미지와 캔버스 비트맵이 호환 가능한 픽셀 포맷을 공유하도록 하여 색상 변형을 방지하세요.  
- **GDI 객체 해제** – `Bitmap`과 `Graphics`를 `using` 문으로 감싸거나 직접 `Dispose()`를 호출하세요; 그렇지 않으면 관리되지 않는 리소스가 누수될 수 있습니다.  
- **좌표 오류** – 사각형 좌표는 0부터 시작합니다. 소스 이미지 경계를 초과하는 사각형을 선택하면 예외가 발생합니다.  

## 자주 묻는 질문

**Q: Aspose.Drawing을 사용해 모든 포맷의 이미지를 자를 수 있나요?**  
A: 네, Aspose.Drawing은 PNG, JPEG, BMP, GIF, TIFF 등 다양한 포맷을 지원하므로 사실상 모든 이미지 유형을 자를 수 있습니다.

**Q: 고급 자르기 옵션을 사용할 수 있나요?**  
A: 물론입니다. `GraphicsPath`, `Matrix` 변환을 결합하거나 `ImageProcessor` 클래스를 사용해 원형 자르기와 같은 복잡한 선택을 수행할 수 있습니다.

**Q: 단일 이미지에 여러 번 자르기 작업을 적용할 수 있나요?**  
A: 네. 첫 번째 자르기 후 결과 비트맵을 새로운 소스로 재사용하고 과정을 반복하면 여러 번 자르기를 연쇄적으로 수행할 수 있습니다.

**Q: Aspose.Drawing이 배치 이미지 처리에 적합한가요?**  
A: 그렇습니다. 가벼운 API와 네이티브 의존성이 없어 서버에서 대량 이미지 컬렉션을 처리하기에 최적입니다.

**Q: Aspose.Drawing 관련 문의에 대한 지원을 어떻게 받을 수 있나요?**  
A: 지원 및 커뮤니티와 연결하려면 [Aspose.Drawing 포럼](https://forum.aspose.com/c/drawing/44)으로 이동하세요.

---

**마지막 업데이트:** 2026-10-13  
**테스트 환경:** Aspose.Drawing 24.11 for .NET  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.Drawing으로 BMP를 로드하고 PNG 및 기타 포맷으로 변환하기](/drawing/net/image-editing/load-save/)
- [Aspose.Drawing for .NET 라이선스 부여 방법 – aspose.drawing 라이선스 부여](/drawing/net/licensing/)
- [Aspose.Drawing API for .NET을 사용한 사각형 그리기 – 좌표계 변환(페이지 변환)](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}