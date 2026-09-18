---
date: 2026-09-18
description: Aprenda a desenhar caminhos e unir caminhos com canetas no Aspose.Drawing,
  e depois salvar a imagem como PNG usando código C# simples.
keywords:
- save image as png
- server side image rendering
- raster image from vector
- export graphics to png
- alternative to system drawing
lastmod: 2026-09-18
linktitle: Unindo caminhos com canetas no Aspose.Drawing
og_description: Salve a imagem como PNG com Aspose.Drawing. Aprenda a desenhar caminhos,
  aplicar estilos de line‑join e exportar gráficos raster de alta qualidade a partir
  de dados vetoriais no servidor.
og_image_alt: Developer guide showing how to draw and join paths with pens, then save
  the result as a PNG file using Aspose.Drawing
og_title: Como desenhar caminho, unir caminhos com canetas e salvar a imagem como
  PNG
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to draw path and join paths with pens in Aspose.Drawing,
    then save the image as PNG using simple C# code.
  headline: How to draw path, join paths with pens and save image as PNG
  type: TechArticle
- questions:
  - answer: Aspose.Drawing is a commercial product, but you can explore its capabilities
      with a **[free trial](https://releases.aspose.com/)**.
    question: Can I use Aspose.Drawing for free?
  - answer: Refer to the **[documentation](https://reference.aspose.com/drawing/net/)**
      for comprehensive guidance.
    question: Where can I find Aspose.Drawing documentation?
  - answer: Visit the **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)**
      for community help and official assistance.
    question: How can I get support for Aspose.Drawing?
  - answer: Yes, you can obtain a **[temporary license](https://purchase.aspose.com/temporary-license/)**
      for short‑term usage.
    question: Are temporary licenses available for Aspose.Drawing?
  - answer: Purchase Aspose.Drawing **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.
    question: Where can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- C# graphics
- save PNG
- vector to raster
- server side rendering
title: Como desenhar caminho, unir caminhos com canetas e salvar a imagem como PNG
url: /pt/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como desenhar caminhos, unir caminhos com canetas e salvar imagem como PNG

## Introdução

Neste tutorial você aprenderá como **draw path** objetos, uni‑los com diferentes estilos de line‑join, e **save image as PNG** usando Aspose.Drawing para .NET. Seja construindo um mecanismo de relatórios, um editor de design ou precisando de renderização de imagens no lado do servidor para um serviço web, dominar o desenho de caminhos com canetas lhe dá controle preciso sobre a conversão de vetor para raster.

## Respostas rápidas
- **What does “draw path” mean?** Ele cria definições de linhas ou formas baseadas em vetor que um objeto `Graphics` pode renderizar.  
- **Which line joins are available?** `Bevel`, `Miter`, `Round`, and `BevelClipped`.  
- **Can I export the result as PNG?** Sim—use `Bitmap.Save` com a extensão `.png`.  
- **Do I need a license?** Uma versão de avaliação funciona para avaliação; uma licença comercial é necessária para produção.  
- **What .NET versions are supported?** .NET Framework 4.6+, .NET Core 3.1+, and .NET 6+.

## O que é “draw path” no Aspose.Drawing?

**Draw path** significa construir um `GraphicsPath` que contém uma série de linhas, curvas ou formas.  
`GraphicsPath` é o contêiner do Aspose.Drawing para geometria vetorial; você pode renderizá‑lo posteriormente com uma `Pen` ou preenchê‑lo com um brush. Essa abordagem permite aplicar transformações, recorte e estilos de line‑join consistentes a toda a forma, em vez de desenhar cada segmento individualmente.

## Por que usar Aspose.Drawing para renderização de imagens no lado do servidor?

Aspose.Drawing fornece um mecanismo robusto de renderização no lado do servidor que funciona em qualquer sistema operacional sem depender do GDI+, tornando‑o ideal para serviços em nuvem, aplicações em contêineres e APIs web de alto desempenho onde a compatibilidade multiplataforma e a operação sem interface gráfica são necessárias, garantindo desempenho escalável.

- **Full .NET compatibility** – suporta .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Opções avançadas de line‑join** – `Bevel`, `Miter`, `Round`, `BevelClipped`.  
- **Saída raster de alta qualidade** – pode exportar para **mais de 10 formatos raster** (PNG, JPEG, BMP, GIF, TIFF, etc.) diretamente a partir de dados vetoriais.  
- **Sem limitações do GDI+** – ideal para serviços em nuvem, contêineres e ambientes sem interface gráfica.

## Pré-requisitos

Antes de mergulharmos no código, certifique‑se de que você tem:

1. **Aspose.Drawing Library** – faça o download a partir da **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.  
2. **.NET Development Environment** – Visual Studio, VS Code ou qualquer IDE que suporte C#.

Agora que tudo está pronto, vamos percorrer cada passo.

## Importar namespaces

Os namespaces `System.Drawing` e `System.Drawing.Drawing2D` contêm os tipos gráficos principais usados pelo Aspose.Drawing.  

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Etapa 1: Criar um bitmap e objeto graphics

`Bitmap` é a tela raster em memória do Aspose.Drawing. Representa uma imagem raster que você pode desenhar usando uma superfície `Graphics`.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Começamos com uma tela em branco (`Bitmap`) com tamanho de 1000 × 800 pixels e obtemos um objeto `Graphics` que renderizará nossos comandos de desenho.

## Etapa 2: Definir o método drawPath

`Pen` é a ferramenta do Aspose.Drawing para traçar contornos vetoriais; define cor, espessura e estilo de line‑join.  

`LineJoin` controla como dois segmentos de linha são conectados em um canto.  

`GraphicsPath` é o contêiner vetorial que contém a série de linhas que iremos unir.

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

Este método auxiliar encapsula a lógica de desenho:

- **Pen** – define a cor e a espessura (30 px).  
- **GraphicsPath** – define duas linhas conectadas que formam um formato de “L”.  
- **LineJoin** – controla como o canto entre as duas linhas é renderizado (`Bevel`, `Round`, etc.).  

Você pode chamar este método com qualquer valor `LineJoin` para ver a diferença visual.

## Etapa 3: Unir caminhos com line join bevel

`LineJoin.Bevel` cria um canto achatado onde as duas linhas se encontram, útil quando você deseja uma junção nítida e sem sobreposição.

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

## Etapa 4: Unir caminhos com line join round

`LineJoin.Round` produz um canto suave e arredondado — perfeito para um visual mais refinado.

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

## Etapa 5: Salvar o resultado como PNG

A chamada `Save` grava o bitmap em um arquivo no formato PNG, completando o fluxo de trabalho de **save image as PNG**. Ajuste o caminho para corresponder ao seu ambiente.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

## Problemas comuns e soluções

| Problema | Por que acontece | Solução |
|----------|------------------|---------|
| **Image appears blank** | O objeto `Graphics` não foi limpo ou o tamanho do bitmap é muito pequeno. | Chame `graphics.Clear(Color.White);` antes de desenhar, ou aumente as dimensões do bitmap. |
| **Corner looks jagged** | Uso de um bitmap de baixa resolução com uma caneta grossa. | Aumente o DPI do bitmap (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) ou reduza a espessura da caneta. |
| **File not found error** | Caminho de salvamento inválido. | Use `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## Perguntas frequentes

**Q: Posso usar o Aspose.Drawing gratuitamente?**  
A: Aspose.Drawing é um produto comercial, mas você pode explorar suas funcionalidades com um **[free trial](https://releases.aspose.com/)**.

**Q: Onde posso encontrar a documentação do Aspose.Drawing?**  
A: Consulte a **[documentation](https://reference.aspose.com/drawing/net/)** para orientação completa.

**Q: Como posso obter suporte para o Aspose.Drawing?**  
A: Visite o **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)** para ajuda da comunidade e assistência oficial.

**Q: Licenças temporárias estão disponíveis para o Aspose.Drawing?**  
A: Sim, você pode obter uma **[temporary license](https://purchase.aspose.com/temporary-license/)** para uso de curto prazo.

**Q: Onde posso comprar o Aspose.Drawing?**  
A: Compre o Aspose.Drawing na **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.

## Conclusão

Neste guia cobrimos como **draw path** objetos, aplicar diferentes estilos `LineJoin` e **save image as PNG** usando Aspose.Drawing para .NET. Ao dominar estas etapas, você pode gerar gráficos vetoriais sofisticados, ícones personalizados ou gráficos dinâmicos diretamente a partir de código no lado do servidor, oferecendo uma solução confiável de **export graphics to PNG** que funciona em qualquer plataforma.

---

**Última atualização:** 2026-09-18  
**Testado com:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

## Tutoriais relacionados

- [Como desenhar arco e salvar imagem PNG com Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-arc/)
- [Como salvar bitmap como PNG ao desenhar múltiplas linhas com Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [Como salvar um bitmap como PNG usando a API Aspose.Drawing para .NET](/drawing/net/image-editing/display/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}