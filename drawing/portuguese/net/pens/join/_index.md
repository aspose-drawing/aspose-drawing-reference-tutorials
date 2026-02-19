---
date: 2026-02-19
description: Aprenda a desenhar caminhos e unir caminhos com canetas no Aspose.Drawing
  e, em seguida, salvar a imagem como PNG usando código C# simples.
linktitle: Joining Paths with Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Como desenhar caminhos e unir caminhos com canetas no Aspose.Drawing
url: /pt/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como desenhar Path e unir Paths com Pens no Aspose.Drawing

## Introdução

Bem‑vindo ao mundo do **Aspose.Drawing for .NET**! Neste tutorial, você descobrirá **how to draw path** objetos, unirá eles com diferentes estilos de line‑join e, finalmente, **save the image as PNG**. Seja construindo uma ferramenta de relatórios, um editor de design ou apenas precisando de gráficos vetoriais nítidos, dominar o desenho de paths com pens lhe dá controle granular sobre a saída visual.

## Respostas rápidas
- **O que significa “draw path”?** Cria definições de linhas ou formas baseadas em vetor que um objeto `Graphics` pode renderizar.  
- **Quais junções de linha estão disponíveis?** `Bevel`, `Miter`, `Round` e `BevelClipped`.  
- **Posso exportar o resultado como PNG?** Sim—use `Bitmap.Save` com a extensão `.png`.  
- **Preciso de licença?** Uma avaliação funciona para teste; uma licença comercial é necessária para produção.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.6+, .NET Core 3.1+ e .NET 6+.

## O que é “how to draw path” no Aspose.Drawing?

Desenhar um path significa construir um `GraphicsPath` que contém uma série de linhas, curvas ou formas. Depois que o path é criado, você o pinta em uma superfície `Graphics` usando um `Pen`. Essa abordagem é mais flexível que desenhar linhas individuais porque permite aplicar transformações, recortes e diferentes estilos de junção ao shape completo.

## Por que usar Aspose.Drawing para unir caminhos?

- **Compatibilidade total com .NET** – funciona no Windows, Linux e macOS.  
- **Opções avançadas de line‑join** – crie cantos chanfrados, arredondados ou em meia‑esquadria com uma única propriedade.  
- **Saída raster de alta qualidade** – salve diretamente em PNG, JPEG, BMP, etc., sem etapas de conversão adicionais.  
- **Sem limitações do GDI+** – ideal para renderização no lado do servidor onde `System.Drawing.Common` pode ser restrito.

## Pré-requisitos

Antes de mergulharmos no código, certifique‑se de que você tem:

1. **Biblioteca Aspose.Drawing** – faça o download **[aqui](https://releases.aspose.com/drawing/net/)**.  
2. **Ambiente de desenvolvimento .NET** – Visual Studio, VS Code ou qualquer IDE que suporte C#.

Agora que tudo está pronto, vamos percorrer cada etapa.

## Importar Namespaces

Adicione os namespaces necessários no topo do seu arquivo para que o compilador saiba onde encontrar as classes de gráficos:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Etapa 1: Criar um Bitmap e um objeto Graphics

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Começamos com uma tela em branco (`Bitmap`) de tamanho 1000 × 800 pixels e obtém‑se um objeto `Graphics` que renderizará nossos comandos de desenho.

## Etapa 2: Definir o método DrawPath

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

## Etapa 3: Unir caminhos com LineJoin Bevel

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

Usar `LineJoin.Bevel` cria um canto achatado onde as duas linhas se encontram.

## Etapa 4: Unir caminhos com LineJoin Round

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

`LineJoin.Round` produz um canto suave e arredondado—perfeito para um visual mais polido.

## Etapa 5: Salvar o resultado como PNG

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

A chamada `Save` grava o bitmap em um arquivo no formato PNG. Ajuste o caminho para corresponder ao seu ambiente.

## Problemas comuns e soluções

| Problema | Por que acontece | Correção |
|----------|------------------|----------|
| **Image appears blank** | O objeto `Graphics` não foi limpo ou o tamanho do bitmap é muito pequeno. | Chame `graphics.Clear(Color.White);` antes de desenhar, ou aumente as dimensões do bitmap. |
| **Corner looks jagged** | Uso de bitmap de baixa resolução com uma caneta espessa. | Aumente o DPI do bitmap (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) ou reduza a espessura da caneta. |
| **File not found error** | Caminho de salvamento inválido. | Use `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## Perguntas Frequentes

### Q1: Posso usar o Aspose.Drawing gratuitamente?

A1: O Aspose.Drawing é um produto comercial, mas você pode explorar seus recursos com um **[teste gratuito](https://releases.aspose.com/)**.

### Q2: Onde posso encontrar a documentação do Aspose.Drawing?

A2: Consulte a **[documentação](https://reference.aspose.com/drawing/net/)** para orientação completa.

### Q3: Como posso obter suporte para o Aspose.Drawing?

A3: Visite o **[fórum Aspose.Drawing](https://forum.aspose.com/c/drawing/44)** para ajuda da comunidade e suporte oficial.

### Q4: Licenças temporárias estão disponíveis para o Aspose.Drawing?

A4: Sim, você pode obter uma **[licença temporária](https://purchase.aspose.com/temporary-license/)** para uso de curto prazo.

### Q5: Onde posso comprar o Aspose.Drawing?

A5: Compre o Aspose.Drawing **[aqui](https://purchase.aspose.com/buy)**.

## Conclusão

Neste guia cobrimos **how to draw path** objetos, aplicamos diferentes estilos `LineJoin` e salvamos o gráfico final como um arquivo PNG usando Aspose.Drawing para .NET. Ao dominar essas etapas, você pode criar gráficos vetoriais sofisticados, ícones personalizados ou gráficos dinâmicos diretamente a partir do seu código server‑side.

---

**Last Updated:** 2026-02-19  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}