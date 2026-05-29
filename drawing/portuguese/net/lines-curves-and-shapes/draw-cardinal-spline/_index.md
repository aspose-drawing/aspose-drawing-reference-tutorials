---
date: 2026-05-29
description: Aprenda como salvar PNG e desenhar splines cardinais em .NET com Aspose.Drawing.
  Salve a curva como PNG, crie gráficos suaves e gere bitmap para arquivo sem esforço.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Desenhando splines cardinais no Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Como salvar PNG e desenhar splines cardinais com Aspose.Drawing
url: /pt/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como salvar PNG e desenhar splines cardinais com Aspose.Drawing

## Introdução

Neste tutorial você descobrirá **como salvar arquivos PNG** enquanto desenha splines cardinais suaves usando Aspose.Drawing para .NET. Seja construindo um componente de gráficos, um editor de diagramas ou simplesmente precisando exportar uma curva personalizada como PNG, os passos abaixo orientam você a criar uma tela bitmap, desenhar um spline com uma caneta e persistir o resultado no disco. Você também verá por que o Aspose.Drawing é uma alternativa confiável e multiplataforma ao System.Drawing.Common.

## Respostas Rápidas
- **O que o método principal faz?** `Graphics.DrawCurve` interpola uma série de pontos em um spline cardinal suave.  
- **Qual formato é usado para salvar a imagem?** PNG via `Bitmap.Save`.  
- **Preciso de uma licença para salvar imagens?** Uma versão de avaliação funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **Posso mudar a tensão da curva?** Sim, sobrecargas de `DrawCurve` permitem especificar a tensão.  
- **O Aspose.Drawing é compatível com .NET 6+?** Absolutamente – ele suporta .NET Framework e .NET Core/5/6.

## O que significa “como salvar PNG” no contexto do Aspose.Drawing?

Salvar um PNG significa converter o bitmap em memória no qual você desenha em um arquivo PNG físico no disco. O processo grava os dados de pixel usando compressão sem perdas, preservando as cores exatas e quaisquer informações de canal alfa. O método `Bitmap.Save` do Aspose.Drawing lida com a codificação PNG automaticamente, portanto você não precisa gerenciar os detalhes do formato manualmente.

## Por que desenhar um spline cardinal com Aspose.Drawing?

Um spline cardinal produz uma curva suave e fluida que segue de perto um conjunto de pontos de controle, tornando‑o perfeito para visualizações de dados, gráficos de UI e formas personalizadas. O Aspose.Drawing suporta **mais de 30 formatos de imagem** e pode renderizar gráficos de centenas de páginas sem carregar todo o arquivo na memória, oferecendo velocidade e flexibilidade.

## Pré-requisitos

Antes de começarmos, certifique‑se de que você tem:

- Visual Studio (qualquer versão recente) instalado.  
- Biblioteca Aspose.Drawing para .NET. Você pode baixá‑la [aqui](https://releases.aspose.com/drawing/net/).  
- Conhecimento básico de programação em C#.

## Importar namespaces

No seu arquivo C#, comece importando o namespace necessário:

O namespace `Aspose.Drawing` contém todos os tipos principais, como `Bitmap`, `Graphics` e `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Passo 1: Criar um Bitmap (Canvas)

Primeiro, crie um bitmap que atuará como a tela para o seu desenho. Este bitmap é onde o spline será renderizado antes de você **salvar a imagem**.

Bitmap representa uma imagem em memória com um formato de pixel e dimensões definidos.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Passo 2: Criar um objeto Graphics

Em seguida, obtenha um objeto `Graphics` a partir do bitmap. Esse objeto fornece a superfície de desenho.

Graphics fornece uma superfície de desenho para renderizar formas, texto e imagens em um bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Passo 3: Definir Pen e Desenhar Curva

Defina uma `Pen` com a cor e largura desejadas e, então, desenhe o spline cardinal usando `DrawCurve`. Isso demonstra a técnica de **desenhar curva com caneta** e serve como um **exemplo de spline cardinal**.

Pen encapsula a cor, largura e estilo de linha usados para desenhar linhas e curvas.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Passo 4: Salvar a Imagem (Salvar Curva como PNG)

Finalmente, persista o bitmap em um arquivo PNG. Este é o núcleo de **como salvar PNG** neste tutorial.

`Bitmap.Save` grava a imagem em um arquivo no formato especificado, como PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Dica profissional:** Use `Path.Combine` para construir caminhos de arquivo de forma segura em diferentes plataformas.

Parabéns! Você desenhou com sucesso um spline cardinal e salvou o resultado como uma imagem PNG usando Aspose.Drawing para .NET. Sinta‑se à vontade para experimentar diferentes arrays de pontos, cores de caneta ou larguras de linha para personalizar suas curvas.

## Casos de Uso Comuns

- **Visualizações de dados** – gráficos de linhas suaves que precisam de pontos de controle precisos.  
- **Componentes de UI personalizados** – desenhando botões, sliders ou bordas decorativas.  
- **Gráficos exportáveis** – gerar ativos PNG sob demanda para relatórios ou conteúdo web.

## Solução de Problemas e Dicas

- **A imagem aparece em branco?** Certifique‑se de que o formato de pixel do bitmap suporta alfa (`Format32bppPArgb`) e que você chama `graphics.Clear(Color.Transparent)` se necessário.  
- **Forma da curva inesperada?** Ajuste o parâmetro de tensão usando a sobrecarga `DrawCurve(pen, points, tension)`.  
- **Erros de acesso ao arquivo?** Verifique se o diretório de destino existe e se sua aplicação tem permissões de gravação.

## Perguntas Frequentes

**Q1: Posso usar o Aspose.Drawing em projetos comerciais?**  
A1: Sim, o Aspose.Drawing é adequado tanto para projetos pessoais quanto comerciais. Verifique os detalhes de licenciamento na [página de compra](https://purchase.aspose.com/buy).

**Q2: Como posso obter uma licença temporária para teste?**  
A2: Obtenha uma licença temporária para fins de teste [aqui](https://purchase.aspose.com/temporary-license/).

**Q3: Onde posso encontrar suporte adicional?**  
A3: Visite o [fórum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para suporte da comunidade e discussões.

**Q4: Existe uma versão de avaliação gratuita disponível?**  
A4: Sim, explore os recursos com a versão de [avaliação gratuita](https://releases.aspose.com/) antes de efetuar a compra.

**Q5: Como acesso a documentação?**  
A5: Consulte a abrangente [documentação](https://reference.aspose.com/drawing/net/) para informações detalhadas e exemplos.

---

**Última atualização:** 2026-05-29  
**Testado com:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Salvar Bitmap como PNG e desenhar curvas fechadas com Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Salvar Bitmap C# – Desenhar Splines Bézier com Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Salvar Bitmap como PNG com Pincéis Sólidos no Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}