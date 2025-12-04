---
title: Unidades de medida em Aspose.Drawing para .NET
linktitle: Unidades de medida em Aspose.Drawing
second_title: API Aspose.Drawing .NET - Alternativa ao System.Drawing.Common
description: Explore a versatilidade do Aspose.Drawing for .NET neste tutorial detalhado, dominando unidades de medida para gráficos de precisão.
weight: 14
url: /pt/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unidades de medida em Aspose.Drawing para .NET

## Introdução

Bem-vindo ao mundo do Aspose.Drawing for .NET, onde precisão e flexibilidade se encontram na manipulação gráfica. Neste tutorial, nos aprofundaremos nas complexidades das unidades de medida no Aspose.Drawing, fornecendo a você um guia passo a passo para aproveitar o poder desta notável biblioteca.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.Drawing for .NET: Certifique-se de ter a biblioteca instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/drawing/net/).

- Diretório de documentos: tenha um diretório designado onde deseja salvar os documentos criados.

- Conhecimento básico de C#: Recomenda-se um conhecimento fundamental de C# para aproveitar ao máximo este guia.

## Importar namespaces

Antes de começar, vamos importar os namespaces necessários para usar Aspose.Drawing de forma eficaz:

```csharp
using System.Drawing;
```

Agora, vamos dividir cada exemplo em várias etapas:

## Pontos como unidades de medida

1. Criar um bitmap: Inicialize um bitmap com largura e altura especificadas.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Criar Gráficos: Gere um objeto Gráfico a partir do bitmap para desenhar nele.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Definir unidade da página para pontos: defina pontos como a unidade de medida (1 ponto = 1/72 polegada).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Desenhar retângulo: desenhe um retângulo usando pontos como unidade.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Milímetros como unidades de medida

1. Definir unidade da página para milímetros: altere a unidade de medida para milímetros (1 mm = 1/25,4 polegada).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Desenhar retângulo em milímetros: desenhe outro retângulo usando milímetros como unidade.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Polegadas como unidades de medida

1. Definir unidade da página para polegadas: Mude a unidade de medida para polegadas.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Desenhar retângulo em polegadas: desenhe um retângulo usando polegadas como unidade.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Salve o resultado

Após concluir os exemplos, salve a imagem resultante em seu diretório de documentos:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Agora, você navegou com sucesso pelas diversas unidades de medida no Aspose.Drawing for .NET, criando uma representação visual de retângulos usando pontos, milímetros e polegadas.

## Conclusão

Neste tutorial, exploramos como Aspose.Drawing for .NET lida com diferentes unidades de medida. Ao manipular pontos, milímetros e polegadas, você pode obter precisão e adaptabilidade em suas criações gráficas. Experimente esses conceitos para desbloquear todo o potencial do Aspose.Drawing.

## Perguntas frequentes

### Q1: Posso usar Aspose.Drawing for .NET com outras estruturas .NET?

A1: Sim, Aspose.Drawing é compatível com vários frameworks .NET, proporcionando flexibilidade em seu ambiente de desenvolvimento.

### P2: Existe um teste gratuito disponível?

 A2: Sim, você pode explorar o Aspose.Drawing com uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q3: Como obtenho suporte para Aspose.Drawing for .NET?

 A3: Visite o[Fórum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para apoio e discussões da comunidade.

### P4: Posso adquirir uma licença temporária para projetos de curto prazo?

 A4: Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso encontrar documentação detalhada para Aspose.Drawing?

 A5: A documentação abrangente está disponível[aqui](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
