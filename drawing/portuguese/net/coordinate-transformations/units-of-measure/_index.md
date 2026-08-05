---
date: 2026-05-24
description: Aprenda a definir a unidade no Aspose.Drawing para .NET, converter unidades
  gráficas facilmente e dominar medições precisas para renderização de gráficos.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Unidades de Medida no Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Como definir unidade no Aspose.Drawing para .NET – Unidades de Medida
url: /pt/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Definir Unidade no Aspose.Drawing para .NET – Unidades de Medida

## Introdução

Bem‑vindo ao mundo do Aspose.Drawing para .NET, onde precisão e flexibilidade se encontram na manipulação gráfica. Neste tutorial você descobrirá **como definir unidade** para seus desenhos, aprenderá a **converter unidades gráficas** entre pontos, milímetros e polegadas, e verá exemplos do mundo real que tornam suas imagens pixel‑perfect. Seja construindo relatórios, miniaturas ou gráficos personalizados, dominar as unidades de medida é essencial para renderização consistente em diferentes dispositivos.

## Respostas Rápidas
- **Qual é a maneira principal de mudar unidades?** Chame `graphics.PageUnit = PageUnit.Point` (ou `.Millimeter`, `.Inch`) no objeto `Graphics`.  
- **Qual unidade equivale a 1/72 polegada?** Pontos.  
- **Quantos milímetros há em uma polegada?** 25,4 mm = 1 polegada.  
- **Preciso de bibliotecas extras para usar unidades?** Não, a biblioteca principal do Aspose.Drawing fornece todas as constantes de unidade.  
- **Posso misturar unidades em uma mesma imagem?** Defina a unidade uma única vez por instância `Graphics`; desenhe tudo usando essa unidade para garantir consistência.

## Pré‑requisitos

Antes de mergulharmos no tutorial, certifique‑se de que você tem os seguintes pré‑requisitos configurados:

- Aspose.Drawing for .NET: Garanta que a biblioteca esteja instalada. Você pode baixá‑la [aqui](https://releases.aspose.com/drawing/net/).
- Diretório de Documentos: Tenha um diretório designado onde deseja salvar os documentos criados.
- Conhecimento Básico de C#: Uma compreensão fundamental de C# é recomendada para aproveitar ao máximo este guia.

## Importar Namespaces

Antes de começarmos, vamos importar os namespaces necessários para usar o Aspose.Drawing de forma eficaz:

```csharp
using System.Drawing;
```

Agora, vamos dividir cada exemplo em várias etapas:

## Como definir a unidade para Pontos?

A classe `Bitmap` representa uma imagem em memória que serve como tela de desenho. Carregue seu bitmap, crie um objeto `Graphics` e defina a unidade da página para pontos — isso indica ao Aspose.Drawing que todas as coordenadas são valores de 1/72 polegada. Usar pontos oferece controle fino para gráficos prontos para impressão e permite especificar larguras de linha com alta precisão.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Passo 1: Criar um Bitmap  
A classe `Bitmap` representa uma imagem em memória que serve como tela de desenho.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Passo 2: Criar um Objeto Graphics  
`Graphics` fornece métodos de desenho para renderizar formas e texto em um `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Passo 3: Definir Page Unit para Pontos  
`PageUnit` é uma enumeração que especifica a unidade de medida para coordenadas de página. `PageUnit.Point` define pontos como a unidade de medida (1 ponto = 1/72 polegada). Essa configuração se aplica a todas as chamadas de desenho subsequentes.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Passo 4: Desenhar um Retângulo em Pontos  
Quando você desenha um retângulo após definir a unidade, as dimensões especificadas são interpretadas como pontos, garantindo dimensionamento preciso.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Como definir a unidade para Milímetros?

`PageUnit` é uma enumeração que especifica a unidade de medida para coordenadas de página. Trocar para milímetros é útil quando você precisa de dimensões métricas, por exemplo ao gerar diagramas de engenharia. O Aspose.Drawing trata 1 mm como 1/25,4 polegada, permitindo alinhar gráficos com medições físicas usadas na fabricação e documentação técnica.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Passo 1: Definir Page Unit para Milímetros  
Atribua `PageUnit.Millimeter` ao objeto `Graphics`; todas as coordenadas agora mapeiam para o sistema métrico.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Passo 2: Desenhar um Retângulo em Milímetros  
A largura e a altura do retângulo agora são expressas em milímetros, facilitando o alinhamento com medições físicas e garantindo que a saída impressa corresponda aos tamanhos reais.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Como definir a unidade para Polegadas?

`Graphics` fornece métodos de desenho para renderizar formas e texto em um `Bitmap`. Polegadas são a unidade padrão para muitas ferramentas de design baseadas nos EUA. Definir a unidade para polegadas permite que você pense em termos familiares ao organizar elementos de UI, e simplifica a transição do design de tela para impressão, onde polegadas são comumente usadas.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Passo 1: Definir Page Unit para Polegadas  
`PageUnit.Inch` altera o sistema de coordenadas de modo que 1 unidade equivale a 1 polegada, oferecendo uma maneira direta de dimensionar elementos para layouts orientados à impressão.

CODE_BLOCK_PLACEHOLDER_10_END

### Passo 2: Desenhar um Retângulo em Polegadas  
Agora qualquer forma que você desenhar usa polegadas como base de medição, o que é ideal para layouts de impressão e para comunicar dimensões a partes interessadas acostumadas ao sistema imperial.

CODE_BLOCK_PLACEHOLDER_11_END

## Salvar o Resultado

Após concluir os exemplos, salve a imagem resultante no seu diretório de documentos. O método `Bitmap.Save` grava o arquivo no formato que você especificar (PNG, JPEG, etc.).

CODE_BLOCK_PLACEHOLDER_12_END

Agora, você navegou com sucesso pelas diversas unidades de medida no Aspose.Drawing para .NET, criando uma representação visual de retângulos usando pontos, milímetros e polegadas.

## Por que usar o sistema de unidades do Aspose.Drawing?

O Aspose.Drawing suporta **30+ formatos de imagem** e pode processar imagens de até **5000 × 5000 pixels** sem carregar o arquivo inteiro na memória, oferecendo alto desempenho para geração de gráficos em larga escala. Ao definir explicitamente a unidade, você elimina suposições, reduz erros de conversão e garante que sua saída corresponda a dimensões físicas exatas em todas as plataformas.

## Problemas Comuns e Soluções

- **Tamanho inesperado após salvar** – Verifique se você definiu `graphics.PageUnit` **antes** de qualquer chamada de desenho; mudar a unidade depois não redimensiona retroativamente as formas existentes.  
- **Saída borrada em telas de alta DPI** – Aumente a resolução do bitmap (por exemplo, `new Bitmap(width, height, 300)`) para corresponder ao DPI alvo.  
- **Unidades misturadas em uma imagem** – Crie instâncias `Graphics` separadas para cada unidade ou realize conversão manual antes de desenhar.

## Perguntas Frequentes

### Q1: Posso usar o Aspose.Drawing para .NET com outras estruturas .NET?
A1: Sim, o Aspose.Drawing é compatível com várias estruturas .NET, oferecendo flexibilidade no seu ambiente de desenvolvimento.

### Q2: Existe uma versão de avaliação gratuita disponível?
A2: Sim, você pode explorar o Aspose.Drawing com uma avaliação gratuita [aqui](https://releases.aspose.com/).

### Q3: Como obtenho suporte para o Aspose.Drawing para .NET?
A3: Visite o [Fórum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para suporte da comunidade e discussões.

### Q4: Posso adquirir uma licença temporária para projetos de curto prazo?
A4: Sim, você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Onde encontro documentação detalhada do Aspose.Drawing?
A5: A documentação abrangente está disponível [aqui](https://reference.aspose.com/drawing/net/).

---

**Última atualização:** 2026-05-24  
**Testado com:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
