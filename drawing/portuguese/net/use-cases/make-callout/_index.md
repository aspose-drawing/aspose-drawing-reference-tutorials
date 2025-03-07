---
title: Fazendo chamadas em Aspose.Drawing
linktitle: Fazendo chamadas em Aspose.Drawing
second_title: API Aspose.Drawing .NET - Alternativa ao System.Drawing.Common
description: Aprimore as ilustrações de seus documentos usando Aspose.Drawing for .NET! Aprenda passo a passo como adicionar textos explicativos para obter visuais mais claros e informativos.
weight: 10
url: /pt/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Fazendo chamadas em Aspose.Drawing

## Introdução
Bem-vindo ao nosso guia passo a passo sobre como fazer chamadas no Aspose.Drawing for .NET! Se você deseja aprimorar as ilustrações de seus documentos com textos explicativos, você está no lugar certo. Neste tutorial, dividiremos o processo em etapas gerenciáveis usando a biblioteca Aspose.Drawing.
## Pré-requisitos
Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos:
- Conhecimento básico da linguagem de programação C#.
-  Biblioteca Aspose.Drawing instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/drawing/net/).
- Um documento ou imagem onde você deseja adicionar frases de destaque.
## Importar namespaces
Certifique-se de ter os namespaces necessários incluídos em seu projeto:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Etapa 1: carregar a imagem
 Comece carregando a imagem onde deseja adicionar textos explicativos. Substituir`"Your Document Directory"` e`"gears.png"` com seu diretório real e nome de arquivo de imagem.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Seu código aqui
}
```
## Etapa 2: criar objeto gráfico
 Criar uma`Graphics` objeto da imagem para realizar operações de desenho.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Etapa 3: definir posições de texto explicativo
Defina os pontos inicial e final de cada texto explicativo, juntamente com o valor e a unidade do texto explicativo.
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
## Etapa 4: desenhar frases de destaque
 Implementar o`DrawCallOut` método para desenhar textos explicativos na imagem.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Etapa 5: salve a imagem
Salve a imagem com textos explicativos no diretório desejado.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Desenhar código-fonte do texto explicativo
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
## Conclusão

Parabéns! Você adicionou textos explicativos à sua imagem com sucesso usando Aspose.Drawing for .NET. Sinta-se à vontade para experimentar diferentes posições e valores para personalizar ainda mais suas frases de destaque.

## Perguntas frequentes

### Posso usar o Aspose.Drawing para outros tipos de ilustrações?

Sim, Aspose.Drawing oferece suporte a uma ampla gama de operações de desenho para vários tipos de ilustrações.

### O Aspose.Drawing é compatível com diferentes formatos de imagem?

Absolutamente! Aspose.Drawing suporta formatos de imagem populares como PNG, JPEG, GIF e muito mais.

### Onde posso encontrar mais exemplos e documentação?

 Explore a documentação abrangente[aqui](https://reference.aspose.com/drawing/net/).

### Como posso obter suporte se encontrar problemas?

 Visite a[Fórum Aspose.Drawing](https://forum.aspose.com/c/diagram/17) para apoio comunitário.

### Posso experimentar o Aspose.Drawing antes de comprar?

 Certamente! Comece com um teste gratuito[aqui](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
