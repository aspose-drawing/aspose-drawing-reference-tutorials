---
date: 2026-03-02
description: Melhore as ilustrações dos seus documentos usando Aspose.Drawing para
  .NET! Aprenda passo a passo como adicionar balões de chamada para visualizações
  mais claras e informativas.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Como adicionar balões de chamada com Aspose.Drawing para .NET
url: /pt/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criando Callouts no Aspose.Drawing

## Introdução
Se você está se perguntando **como adicionar callouts** às suas imagens ou diagramas usando Aspose.Drawing para .NET, chegou ao lugar certo. Neste tutorial vamos percorrer todo o processo — desde o carregamento de uma imagem até o desenho de callouts elegantemente estilizados — para que você possa tornar suas ilustrações mais claras e informativas.

## Respostas Rápidas
- **Qual biblioteca eu preciso?** Aspose.Drawing para .NET (disponível para download no site oficial).  
- **Quais versões do .NET são suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Preciso de uma licença?** Uma avaliação gratuita funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **Quanto tempo leva a implementação?** Normalmente menos de 10 minutos para um callout básico.  
- **Posso personalizar cores e fontes?** Sim — tudo é controlado por objetos padrão do GDI+ (Pen, Font, Brush).

## Como Adicionar Callouts no Aspose.Drawing
A seguir, um guia conciso, passo a passo, que mostra exatamente **como adicionar callouts** a uma imagem. Sinta-se à vontade para copiar o código, experimentar as posições e adaptar o estilo para combinar com sua marca.

## Pré-requisitos
Antes de começar, certifique‑se de que você tem:

- Conhecimento básico da linguagem de programação C#.  
- Biblioteca Aspose.Drawing instalada. Você pode baixá‑la [aqui](https://releases.aspose.com/drawing/net/).  
- Um documento ou imagem onde deseja adicionar callouts.

## Importar Namespaces
Certifique‑se de que os namespaces necessários estejam incluídos no seu projeto:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Etapa 1: Carregar a Imagem
Comece carregando a imagem onde você quer adicionar os callouts. Substitua `"Your Document Directory"` e `"gears.png"` pelos seus diretórios e nomes de arquivo reais.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Etapa 2: Criar o Objeto Graphics
Crie um objeto `Graphics` a partir da imagem para executar as operações de desenho.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Etapa 3: Definir as Posicoes do Callout
Defina os pontos de início e fim para cada callout, juntamente com o valor e a unidade do callout.

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

## Etapa 4: Desenhar Callouts
Implemente o método `DrawCallOut` para desenhar os callouts na imagem.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Etapa 5: Salvar a Imagem
Salve a imagem com os callouts no diretório desejado.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Código Fonte do Draw Callout
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

## Problemas Comuns & Dicas
- **Coordenadas de ancoragem incorretas** – verifique se os pontos de início e fim estão dentro dos limites da imagem; caso contrário, o callout pode ser cortado.  
- **Sobreposição de texto** – ajuste `spaceSize` ou o tamanho da fonte se o rótulo colidir com outros gráficos.  
- **Desempenho** – para imagens muito grandes, considere descartar os objetos `Pen`, `Font` e `Brush` após o uso para liberar recursos.

## Conclusão
Parabéns! Agora você sabe **como adicionar callouts** a uma imagem usando Aspose.Drawing para .NET. Sinta‑se livre para experimentar diferentes posições, cores e fontes para combinar com seu estilo visual.

## Perguntas Frequentes

### Posso usar Aspose.Drawing para outros tipos de ilustrações?
Sim, o Aspose.Drawing suporta uma ampla gama de operações de desenho para diversos tipos de ilustrações.

### O Aspose.Drawing é compatível com diferentes formatos de imagem?
Absolutamente! O Aspose.Drawing suporta formatos de imagem populares como PNG, JPEG, GIF e muitos outros.

### Onde posso encontrar mais exemplos e documentação?
Explore a documentação completa [aqui](https://reference.aspose.com/drawing/net/).

### Como obtenho suporte se encontrar problemas?
Visite o [fórum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para suporte da comunidade.

### Posso experimentar o Aspose.Drawing antes de comprar?
Certamente! Comece com uma avaliação gratuita [aqui](https://releases.aspose.com/).

**Perguntas e Respostas Adicionais**

**Q: Posso mudar o estilo da linha do callout (tracejada, pontilhada)?**  
A: Sim — basta configurar a propriedade `Pen.DashStyle` antes de desenhar a linha.

**Q: É possível adicionar uma cor de fundo ao rótulo do callout?**  
A: Com certeza. Crie um `SolidBrush` com a cor desejada e preencha um retângulo atrás do texto antes de chamar `DrawString`.

**Q: Como garantir que o callout tenha a mesma aparência em telas de alta DPI?**  
A: Defina `graphics.PageUnit = GraphicsUnit.Pixel` (conforme mostrado) e use medidas baseadas em vetor para manter a escala consistente.

---

**Última atualização:** 2026-03-02  
**Testado com:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}