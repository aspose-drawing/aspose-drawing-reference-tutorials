---
date: 2026-03-02
description: Aspose.Drawing for .NET를 사용하여 문서 일러스트레이션을 향상시키세요! 더 명확하고 유익한 시각 자료를 위해
  콜아웃을 추가하는 방법을 단계별로 배워보세요.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET으로 콜아웃 추가하는 방법
url: /ko/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing에서 호출선 만들기

## 소개
Aspose.Drawing for .NET을 사용하여 이미지나 다이어그램에 **호출선을 추가하는 방법**을 궁금해하신다면, 바로 여기입니다. 이 튜토리얼에서는 이미지를 로드하고 아름답게 스타일링된 호출선을 그리는 전체 과정을 단계별로 안내하므로, 일러스트를 더 명확하고 풍부하게 만들 수 있습니다.

## 빠른 답변
- **필요한 라이브러리는 무엇인가요?** Aspose.Drawing for .NET (공식 사이트에서 다운로드 가능).  
- **지원되는 .NET 버전은 무엇인가요?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **라이선스가 필요합니까?** 개발용으로는 무료 체험판을 사용할 수 있으며, 운영 환경에서는 상용 라이선스가 필요합니다.  
- **구현에 걸리는 시간은 얼마나 되나요?** 기본 호출선의 경우 보통 10분 이내에 완료됩니다.  
- **색상과 글꼴을 커스터마이징할 수 있나요?** 예—모든 것이 표준 GDI+ 객체(Pen, Font, Brush)로 제어됩니다.

## Aspose.Drawing에서 호출선 추가 방법
아래는 이미지에 **호출선을 추가하는 방법**을 정확히 보여주는 간결한 단계별 가이드입니다. 코드를 복사하고, 위치를 실험하며, 스타일을 브랜드에 맞게 조정해 보세요.

## 사전 요구 사항
시작하기 전에 다음을 준비하세요:

- C# 프로그래밍 언어에 대한 기본 지식.  
- Aspose.Drawing 라이브러리가 설치되어 있어야 합니다. [here](https://releases.aspose.com/drawing/net/)에서 다운로드할 수 있습니다.  
- 호출선을 추가하고자 하는 문서 또는 이미지.

## 네임스페이스 가져오기
프로젝트에 필요한 네임스페이스가 포함되어 있는지 확인하세요:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## 단계 1: 이미지 로드
호출선을 추가하려는 이미지를 먼저 로드합니다. `"Your Document Directory"`와 `"gears.png"`를 실제 디렉터리와 이미지 파일명으로 교체하세요.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## 단계 2: Graphics 객체 생성
이미지에서 `Graphics` 객체를 생성하여 그리기 작업을 수행합니다.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## 단계 3: 호출선 위치 정의
각 호출선의 시작점과 끝점, 그리고 호출선 값과 단위를 정의합니다.

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

## 단계 4: 호출선 그리기
`DrawCallOut` 메서드를 구현하여 이미지에 호출선을 그립니다.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## 단계 5: 이미지 저장
호출선이 포함된 이미지를 원하는 디렉터리에 저장합니다.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## 호출선 소스 코드
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

## 일반적인 문제 및 팁
- **잘못된 앵커 좌표** – 시작점과 끝점이 이미지 경계 내에 있는지 확인하세요; 그렇지 않으면 호출선이 잘릴 수 있습니다.  
- **텍스트 겹침** – 라벨이 다른 그래픽과 충돌하면 `spaceSize` 또는 글꼴 크기를 조정하세요.  
- **성능** – 매우 큰 이미지의 경우 사용 후 `Pen`, `Font`, `Brush` 객체를 해제하여 리소스를 확보하는 것이 좋습니다.

## 결론
축하합니다! 이제 Aspose.Drawing for .NET을 사용해 이미지에 **호출선을 추가하는 방법**을 알게 되었습니다. 다양한 위치, 색상, 글꼴을 실험하여 시각 스타일에 맞게 조정해 보세요.

## FAQ

### Aspose.Drawing을 다른 유형의 일러스트에 사용할 수 있나요?
예, Aspose.Drawing은 다양한 유형의 일러스트에 대한 광범위한 그리기 작업을 지원합니다.

### Aspose.Drawing이 다양한 이미지 형식과 호환되나요?
물론입니다! Aspose.Drawing은 PNG, JPEG, GIF 등 인기 있는 이미지 형식을 지원합니다.

### 더 많은 예제와 문서는 어디에서 찾을 수 있나요?
포괄적인 문서는 [here](https://reference.aspose.com/drawing/net/)에서 확인하세요.

### 문제가 발생했을 때 지원을 받으려면 어떻게 해야 하나요?
커뮤니티 지원을 위해 [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) 를 방문하세요.

### 구매 전에 Aspose.Drawing을 체험할 수 있나요?
물론입니다! 무료 체험은 [here](https://releases.aspose.com/)에서 시작하세요.

**Additional Q&A**

**Q: 호출선 스타일(점선, 대시)을 변경할 수 있나요?**  
A: 예—선을 그리기 전에 `Pen.DashStyle` 속성을 설정하면 됩니다.

**Q: 호출선 라벨에 배경색을 추가할 수 있나요?**  
A: 물론입니다. 원하는 색상의 `SolidBrush`를 생성하고 `DrawString`을 호출하기 전에 텍스트 뒤에 사각형을 채워 배경색을 적용하세요.

**Q: 고 DPI 디스플레이에서도 호출선이 동일하게 보이도록 하려면 어떻게 해야 하나요?**  
A: `graphics.PageUnit = GraphicsUnit.Pixel`(예시와 같이)로 설정하고 벡터 기반 측정을 사용하여 스케일링을 일관되게 유지하세요.

---

**마지막 업데이트:** 2026-03-02  
**테스트 환경:** Aspose.Drawing 24.11 for .NET  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}