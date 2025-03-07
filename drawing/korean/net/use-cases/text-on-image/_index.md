---
title: Aspose. Drawing의 이미지에 텍스트 추가
linktitle: Aspose. Drawing의 이미지에 텍스트 추가
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: .NET용 Aspose.드로잉을 사용하여 텍스트를 이미지에 완벽하게 통합하는 방법을 살펴보세요. 간편한 이미지 조작을 위한 단계별 가이드를 따르세요. 지금 다운로드하세요!
weight: 12
url: /ko/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose. Drawing의 이미지에 텍스트 추가

## 소개
.NET 개발의 역동적인 세계에서 Aspose. Drawing은 이미지를 쉽게 조작할 수 있는 강력한 도구로 돋보입니다. 워터마킹, 주석, 개인화된 그래픽 생성 등을 위해 이미지에 텍스트를 추가하는 것은 일반적인 요구 사항입니다. 이 튜토리얼에서는 C#을 사용하여 Aspose. Drawing을 활용하여 텍스트를 이미지에 원활하게 통합하는 방법을 살펴보겠습니다.
## 전제 조건
튜토리얼을 시작하기 전에 다음 사항이 준비되어 있는지 확인하세요.
1.  Aspose.드로잉 라이브러리: 다음에서 Aspose.드로잉 라이브러리를 다운로드하고 설치하세요.[.NET 문서용 Aspose.드로잉](https://reference.aspose.com/drawing/net/).
2. 개발 환경: Visual Studio 또는 기타 호환 가능한 IDE를 포함하여 작동하는 .NET 개발 환경을 갖추고 있습니다.
이제 단계별 가이드를 시작해 보겠습니다.
## 네임스페이스 가져오기
필요한 네임스페이스를 C# 프로젝트로 가져오는 것부터 시작합니다.
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## 1단계: 이미지 로드
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
여기서는 지정된 파일 경로에서 이미지를 로드하고 추가 처리를 위해 그래픽 객체를 초기화합니다.
## 2단계: 텍스트 속성 설정
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
색상, 글꼴, 패딩 등의 텍스트 속성을 정의합니다. 원하는 대로 이 매개변수를 조정하세요.
## 3단계: 텍스트 크기 측정
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
각 단어를 개별적으로 측정하여 텍스트에 필요한 크기를 계산합니다. 이렇게 하면 적절한 배치가 보장되고 텍스트가 겹치는 것을 방지할 수 있습니다.
## 4단계: 이미지에 텍스트 그리기
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
이제 계산된 크기를 기준으로 이미지 위에 텍스트를 배치하고 지정된 글꼴과 색상을 사용하여 그립니다.
## 5단계: 이미지 저장
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
수정된 이미지를 원하는 디렉토리에 저장하세요.
이 단계별 가이드는 .NET용 Aspose.드로잉을 사용하여 이미지에 텍스트를 추가하는 간단한 프로세스를 보여줍니다. 원하는 시각적 효과를 얻으려면 다양한 글꼴, 색상, 텍스트 콘텐츠를 실험해 보세요.
## 결론
Aspose.드로잉은 .NET에서 이미지 조작 작업을 단순화하여 개발자에게 강력한 툴킷을 제공합니다. 이미지에 텍스트를 추가하는 것은 그 기능의 한 예일 뿐이며 그래픽 요소를 처리하는 데 있어서 라이브러리의 다양성을 보여줍니다.
## 자주 묻는 질문
### Aspose. Drawing은 모든 이미지 형식과 호환됩니까?
 Aspose. Drawing은 JPEG, PNG, GIF와 같은 널리 사용되는 이미지 형식을 포함하여 광범위한 이미지 형식을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/drawing/net/) 전체 목록을 보려면.
### 상업용 프로젝트에 Aspose. Drawing을 사용할 수 있나요?
예, Aspose. Drawing은 개인 및 상업 프로젝트 모두에 적합합니다. 라이선스에 대한 자세한 내용은 다음을 참조하세요.[구매 페이지](https://purchase.aspose.com/buy).
### 테스트 목적으로 임시 라이센스를 사용할 수 있습니까?
 네, 다음 사이트를 방문하시면 테스트용 임시 라이센스를 받으실 수 있습니다.[임시면허](https://purchase.aspose.com/temporary-license/).
### Aspose. Drawing에 대한 커뮤니티 지원은 어디에서 찾을 수 있나요?
 커뮤니티에 참여하고 지원을 받으세요.[Aspose.드로잉 포럼](https://forum.aspose.com/c/diagram/17).
### Aspose.드로잉을 시작하려면 어떻게 해야 하나요?
 다음에서 라이브러리를 다운로드하여 시작하세요.[여기](https://releases.aspose.com/drawing/net/) 그리고 포괄적인 탐색[선적 서류 비치](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
