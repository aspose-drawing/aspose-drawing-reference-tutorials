---
title: Aspose.드로잉에서 콜아웃 만들기
linktitle: Aspose.드로잉에서 콜아웃 만들기
second_title: Aspose.드로잉 .NET API - System.드로잉.Common의 대안
description: .NET용 Aspose.드로잉을 사용하여 문서 일러스트레이션을 향상시키세요! 더욱 명확하고 유익한 시각적 자료를 위해 콜아웃을 추가하는 방법을 단계별로 알아보세요.
type: docs
weight: 10
url: /ko/net/use-cases/make-callout/
---
## 소개
.NET용 Aspose.드로잉에서 콜아웃을 만드는 방법에 대한 단계별 가이드에 오신 것을 환영합니다! 설명선을 사용하여 문서 일러스트레이션을 향상시키려는 경우 올바른 위치에 오셨습니다. 이 튜토리얼에서는 Aspose. Drawing 라이브러리를 사용하여 프로세스를 관리 가능한 단계로 분류합니다.
## 전제 조건
튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
- C# 프로그래밍 언어에 대한 기본 지식.
-  Aspose.드로잉 라이브러리가 설치되었습니다. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/drawing/net/).
- 설명선을 추가하려는 문서 또는 이미지입니다.
## 네임스페이스 가져오기
프로젝트에 필요한 네임스페이스가 포함되어 있는지 확인하세요.
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## 1단계: 이미지 로드
 콜아웃을 추가하려는 이미지를 로드하는 것부터 시작하세요. 바꾸다`"Your Document Directory"` 그리고`"gears.png"` 실제 디렉터리와 이미지 파일 이름을 사용하세요.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // 여기에 귀하의 코드가 있습니다
}
```
## 2단계: 그래픽 객체 생성
 만들기`Graphics` 이미지의 개체를 사용하여 그리기 작업을 수행합니다.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## 3단계: 콜아웃 위치 정의
콜아웃 값 및 단위와 함께 각 콜아웃의 시작점과 끝점을 정의합니다.
```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```
## 4단계: 콜아웃 그리기
 구현`DrawCallOut` 이미지에 설명선을 그리는 방법입니다.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## 5단계: 이미지 저장
콜아웃과 함께 이미지를 원하는 디렉토리에 저장합니다.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## 콜아웃 소스 코드 그리기
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```
## 결론

축하해요! .NET용 Aspose.드로잉을 사용하여 이미지에 콜아웃을 성공적으로 추가했습니다. 콜아웃을 추가로 맞춤설정하려면 다양한 위치와 값을 자유롭게 실험해 보세요.

## 자주 묻는 질문

### 다른 유형의 일러스트레이션에 Aspose. Drawing을 사용할 수 있나요?

예, Aspose. Drawing은 다양한 유형의 일러스트레이션에 대한 광범위한 그리기 작업을 지원합니다.

### Aspose.드로잉은 다른 이미지 형식과 호환됩니까?

전적으로! Aspose. Drawing은 PNG, JPEG, GIF 등과 같은 널리 사용되는 이미지 형식을 지원합니다.

### 더 많은 예제와 문서는 어디에서 찾을 수 있나요?

 포괄적인 문서 살펴보기[여기](https://reference.aspose.com/drawing/net/).

### 문제가 발생하면 어떻게 지원을 받을 수 있나요?

 방문하다[Aspose.드로잉 포럼](https://forum.aspose.com/c/diagram/17) 지역 사회 지원을 위해.

### 구매하기 전에 Aspose. Drawing을 사용해 볼 수 있나요?

 틀림없이! 무료 평가판 시작하기[여기](https://releases.aspose.com/).