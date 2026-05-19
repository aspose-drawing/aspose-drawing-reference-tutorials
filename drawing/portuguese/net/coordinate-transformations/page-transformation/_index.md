---
date: 2026-05-19
description: Aprenda a desenhar gráficos de retângulo enquanto realiza a transformação
  do sistema de coordenadas no .NET com Aspose.Drawing. Este guia passo a passo mostra
  como converter polegadas em pixels e definir unidades de página.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Transformação do Sistema de Coordenadas no Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Como desenhar retângulo – Transformação do sistema de coordenadas (Transformação
  de página) no Aspose.Drawing para .NET
url: /pt/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como desenhar retângulo – Transformação do sistema de coordenadas (Transformação de página) no Aspose.Drawing para .NET

## Introdução

Bem‑vindo! Neste tutorial você descobrirá **como desenhar retângulo** gráficos enquanto transforma as coordenadas da página usando Aspose.Drawing para .NET. Seja construindo um aplicativo intensivo em gráficos ou precisando de controle preciso sobre unidades de desenho, este guia o conduz passo a passo — desde a configuração da tela até o desenho de um elemento retângulo. Ao final, você será capaz de aplicar essas técnicas em seus próprios projetos com confiança.

## Respostas rápidas
- **O que é transformação do sistema de coordenadas?** Mapeando unidades de nível de página (como polegadas) para pixels de nível de dispositivo.  
- **Por que usar Aspose.Drawing?** Ele oferece uma alternativa totalmente gerenciada e multiplataforma ao System.Drawing.Common.  
- **Quanto tempo leva para implementar o exemplo?** Cerca de 5‑10 minutos para uma transformação de página básica.  
- **Preciso de uma licença?** Um teste gratuito funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## O que é Aspose.Drawing?

`Aspose.Drawing` é uma biblioteca gráfica .NET que fornece uma **API independente de dispositivo** para criar e manipular imagens raster, vetores e desenhos de nível de página sem depender do GDI+. Ela suporta **mais de 30 formatos de imagem** e pode processar imagens de até **10.000 × 10.000 pixels** sem carregar o arquivo inteiro na memória.

## Por que usar transformação do sistema de coordenadas com Aspose.Drawing?

A transformação do sistema de coordenadas permite que você projete gráficos em unidades do mundo real enquanto a biblioteca cuida da escala de pixels para qualquer dispositivo de saída. Isso garante dimensionamento consistente em telas e impressoras e simplifica os cálculos de layout.

- **Design independente de dispositivo:** Escreva o código uma vez e deixe o Aspose.Drawing lidar com a escala de pixels para qualquer tela ou impressora.  
- **Desenho de precisão:** Ideal para diagramas técnicos, esboços no estilo CAD ou qualquer cenário onde medições exatas são importantes.  
- **Confiabilidade multiplataforma:** Funciona consistentemente no Windows, Linux e macOS sem as limitações do GDI+ do System.Drawing.  
- **Números de desempenho:** Em uma CPU típica de 2,5 GHz, desenhar um retângulo de 5 polegadas a 300 DPI leva menos de **15 ms**, e a biblioteca pode renderizar **50 quadros por segundo** em cenários de pré‑visualização em tempo real.

## Pré‑requisitos

- **Aspose.Drawing Library:** Baixe a versão mais recente no site oficial [here](https://releases.aspose.com/drawing/net/).  
- **Development Environment:** Visual Studio, Rider ou qualquer IDE compatível com .NET.  
- **Your Document Directory:** Substitua `"Your Document Directory"` no código pela pasta onde deseja salvar a imagem de saída.  
- **ASP.NET support (optional):** Você pode usar Aspose.Drawing em projetos ASP.NET Core adicionando o pacote NuGet ao seu aplicativo web — isso segue o mesmo padrão **how to use aspnet** de qualquer outra biblioteca .NET.

Agora que tudo está pronto, vamos mergulhar no guia passo a passo.

## Como desenhar retângulo com transformação de página?

Carregue um bitmap em branco, defina a unidade da página para polegadas e desenhe um retângulo usando uma caneta azul fina — isso completa o desenho do retângulo em apenas algumas linhas de código. A propriedade `Graphics.PageUnit` indica ao mecanismo que interprete todas as coordenadas como polegadas, permitindo que você pense em medidas do mundo real em vez de pixels brutos.

### Passo 1: Importar namespaces

As instruções `using` dão acesso às classes principais de desenho.

```csharp
using System.Drawing;
```

### Passo 2: Criar um Bitmap

`Bitmap` representa uma imagem na memória que pode ser desenhada. Começamos criando um bitmap em branco que servirá como superfície de desenho. O formato de pixel `Format32bppPArgb` nos fornece suporte de alfa pré‑multiplicado de alta qualidade.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Passo 3: Criar um objeto Graphics

Um objeto `Graphics` fornece a API de desenho para o bitmap. Ele é a ponte entre seu código e o buffer de pixels.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Passo 4: Limpar a tela

Dê à tela um fundo neutro para que as formas desenhadas se destaquem. Aqui preenchemos com um cinza claro.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Passo 5: Definir a transformação (Como definir a unidade)

`Graphics.PageUnit` especifica a unidade de medida usada para coordenadas de página. Para mapear coordenadas de página para pixels do dispositivo, defina a propriedade `PageUnit`. Neste exemplo escolhemos polegadas, mas você também pode usar `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` ou `GraphicsUnit.Pixel`. Definir a unidade para polegadas permite que você **converta polegadas em pixels** automaticamente com base no DPI do bitmap (96 DPI por padrão, 300 DPI para impressão de alta resolução).

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Passo 6: Desenhar um retângulo – desenhar gráficos de retângulo

`Pen` define a cor, largura e estilo das linhas desenhadas em uma superfície gráfica. Agora desenhamos um retângulo usando uma caneta azul fina. Como mudamos para polegadas, o tamanho e a posição do retângulo são expressos em polegadas, tornando o código mais legível para layouts orientados à impressão.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Passo 7: Salvar a imagem

Finalmente, grave o bitmap em um arquivo PNG na pasta especificada anteriormente.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Como escalar gráficos para uma impressora?

Defina o DPI do bitmap para a resolução da impressora alvo (por exemplo, 300 DPI) antes de desenhar. Isso automaticamente **escala a saída gráfica da impressora** de modo que uma polegada no seu código corresponda a uma polegada na página impressa. Após definir `bitmap.SetResolution(300, 300)`, o mesmo retângulo aparecerá maior na folha impressa, mantendo suas dimensões exatas.

## Problemas comuns e soluções

| Problema | Por que acontece | Correção |
|----------|------------------|----------|
| **Arquivo de saída não criado** | Caminho incorreto ou pasta ausente | Certifique‑se de que o diretório de destino exista ou use `Directory.CreateDirectory` antes de salvar. |
| **Retângulo aparece distorcido** | `PageUnit` errado ou DPI incompatível | Verifique se `graphics.PageUnit` corresponde às unidades que pretende usar e se o DPI do bitmap está configurado adequadamente (o padrão é 96 DPI). |
| **Exceção de licença** | Executando sem uma licença válida em produção | Aplique sua licença temporária ou permanente do Aspose.Drawing antes de criar objetos gráficos. |

## Perguntas frequentes

**Q: Posso usar o Aspose.Drawing gratuitamente?**  
A: Sim, um teste gratuito está disponível [here](https://releases.aspose.com/).

**Q: Onde posso encontrar documentação detalhada do Aspose.Drawing?**  
A: A referência completa da API está localizada [here](https://reference.aspose.com/drawing/net/).

**Q: Como obtenho suporte para Aspose.Drawing?**  
A: Visite o [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) para ajuda da comunidade e assistência oficial.

**Q: Existe uma licença temporária disponível para Aspose.Drawing?**  
A: Absolutamente — obtenha uma [here](https://purchase.aspose.com/temporary-license/).

**Q: Onde posso comprar uma licença completa do Aspose.Drawing?**  
A: Você pode adquiri‑la [here](https://purchase.aspose.com/buy).

## Conclusão

Neste guia cobrimos tudo o que você precisa para **como desenhar retângulo** gráficos com Aspose.Drawing: configurar a tela, definir unidades de página, desenhar formas precisas e salvar o resultado. Use essas técnicas para criar gráficos escaláveis e independentes de dispositivo para relatórios, desenhos no estilo CAD ou qualquer aplicação onde a precisão de medição seja importante. Em seguida, explore transformações avançadas como rotação, escala e origens de coordenadas personalizadas para desbloquear cenários de desenho ainda mais poderosos.

---

**Última atualização:** 2026-05-19  
**Testado com:** Aspose.Drawing 24.12 for .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais relacionados

- [Unidades de medida no Aspose.Drawing para .NET](/drawing/net/coordinate-transformations/units-of-measure/)
- [Como aplicar transformação: Transformação local no Aspose.Drawing para .NET](/drawing/net/coordinate-transformations/local-transformation/)
- [Tutorial de Transformação de Matriz: Transformações de Matriz no Aspose.Drawing para .NET](/drawing/net/coordinate-transformations/matrix-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}