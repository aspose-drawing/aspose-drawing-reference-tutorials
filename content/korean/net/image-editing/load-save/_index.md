---
title: Aspose. Drawing에서 이미지 로드 및 저장
linktitle: Aspose. Drawing에서 이미지 로드 및 저장
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: Aspose. Drawing을 사용하여 .NET에서 마스터 이미지 로드 및 저장. BMP, GIF, JPG, PNG, TIFF 형식을 손쉽게 탐색해 보세요.
type: docs
weight: 13
url: /ko/net/image-editing/load-save/
---
## 소개

.NET용 Aspose.드로잉을 사용하여 이미지 로딩 및 저장을 마스터하는 방법에 대한 단계별 가이드에 오신 것을 환영합니다! 다양한 이미지 형식을 쉽게 조작하는 기술을 향상시키고 싶다면 올바른 위치에 오셨습니다. Aspose. Drawing for .NET은 이미지 작업 프로세스를 단순화하는 강력한 라이브러리이며, 이 튜토리얼에서는 다양한 형식으로 이미지를 로드하고 저장하는 방법을 살펴보겠습니다.

## 전제 조건

이 학습 여정을 시작하기 전에 다음 전제 조건이 갖추어져 있는지 확인하십시오.

-  .NET용 Aspose.드로잉: 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/drawing/net/).

- .NET 환경: 이 튜토리얼에서는 사용자가 .NET 개발에 대한 실무 지식을 가지고 있다고 가정합니다.

이제 준비가 되었으므로 필수 네임스페이스를 살펴보고 단계별 가이드를 살펴보겠습니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 필요한 네임스페이스를 가져오는 것부터 시작하세요.

```csharp
using System.Drawing;
```

이러한 네임스페이스는 이미지 조작에 필요한 기본 클래스와 메서드를 제공합니다.

## 1단계: 이미지 로드

이미지를 로드하는 것부터 시작해 보겠습니다. 이 예에서는 BMP, GIF, JPG, PNG 및 TIFF와 같은 다양한 형식의 이미지를 로드합니다.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## 2단계: LoadAndSave 메서드 구현

 이제,`LoadAndSave` 방법을 여러 단계로 나누어:

### 2.1단계: 이미지 로드

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### 2.2단계: 이미지 저장

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // 이미지 저장
    loadedImage.Save(outputPath);
}
```

지원하려는 각 이미지 형식에 대해 이 단계를 반복합니다.

## 결론

축하해요! .NET용 Aspose.드로잉을 사용하여 이미지를 로드하고 저장하는 기술을 마스터했습니다. 이 기술은 다양한 이미지 형식으로 작업하는 개발자에게 매우 중요합니다. 이 지식을 실험하고 탐색하고 프로젝트에 통합하세요.

## FAQ

### Q1: Aspose. Drawing은 모든 이미지 형식과 호환됩니까?

A1: Aspose. Drawing은 BMP, GIF, JPG, PNG 및 TIFF를 포함한 광범위한 형식을 지원합니다.

### Q2: Aspose. Drawing에 대한 자세한 문서는 어디서 찾을 수 있나요?

A2: 공식 문서를 확인하세요.[여기](https://reference.aspose.com/drawing/net/).

### Q3: Aspose. Drawing에 대한 임시 라이선스를 어떻게 얻을 수 있나요?

 A3: 방문[여기](https://purchase.aspose.com/temporary-license/) 임시 라이선스 세부정보를 확인하세요.

### Q4: 구현 중에 문제가 발생하거나 질문이 있으면 어떻게 합니까?

 A4: Aspose.드로잉 커뮤니티에서 도움을 구하세요.[Aspose 포럼](https://forum.aspose.com/c/diagram/17).

### Q5: Aspose. Drawing 라이브러리는 어디서 구입할 수 있나요?

 A5: 당신은 그것을 살 수 있습니다[여기](https://purchase.aspose.com/buy).