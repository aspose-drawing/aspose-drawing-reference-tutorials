---
date: 2026-09-23
description: Aprenda a desenhar texto em imagem usando Aspose.Drawing para .NET. Gere
  imagem com texto, adicione texto ao bitmap e salve o bitmap como PNG com custom
  fonts.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Como desenhar texto com Aspose.Drawing
og_description: Aprenda a desenhar texto em imagem usando Aspose.Drawing para .NET.
  Este tutorial mostra como gerar imagem com texto, adicionar texto ao bitmap e salvar
  o bitmap como PNG com custom fonts.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Desenhar texto em imagem com Aspose.Drawing para .NET – Guia rápido
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Como desenhar texto em imagem com Aspose.Drawing para .NET
url: /pt/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como desenhar texto em imagem com Aspose.Drawing para .NET

## Introdução

Neste guia passo a passo, você aprenderá **como desenhar texto em imagem** usando Aspose.Drawing para .NET. Seja para criar uma *imagem de texto dinâmica*, adicionar texto a um bitmap existente ou gerar um gráfico com fontes personalizadas, este tutorial o conduz por todos os detalhes para que você possa começar a desenhar texto em minutos. A biblioteca suporta mais de 30 métodos GDI+, funciona em Windows, Linux e macOS, e tem **zero dependências externas**, tornando‑a uma escolha confiável para geração de imagens no lado do servidor.

## Respostas rápidas
- **Qual biblioteca é usada?** Aspose.Drawing for .NET  
- **Tarefa principal?** Desenhar texto em uma imagem (criar imagem com texto)  
- **Método principal?** `Graphics.DrawString` (desenhar string na imagem)  
- **Formato de saída?** PNG (salvar bitmap como PNG)  
- **Pré‑requisitos?** ambiente de desenvolvimento .NET e biblioteca Aspose.Drawing  

## O que é desenhar texto com Aspose.Drawing?

Desenhar texto com Aspose.Drawing significa usar a API compatível com GDI+ da biblioteca para renderizar strings Unicode em uma tela raster. O método `Graphics.DrawString` grava o texto em um bitmap, permitindo controlar fonte, cor, alinhamento e anti‑aliasing. Essa abordagem permite gerar imagens de alta qualidade sem instalar System.Drawing.Common.

## Por que usar Aspose.Drawing para adicionar texto a imagens?

O Aspose.Drawing oferece uma maneira confiável e multiplataforma de renderizar texto em imagens sem precisar de bibliotecas nativas GDI+, proporcionando qualidade e desempenho consistentes em qualquer sistema operacional. Ele suporta anti‑aliasing avançado, caracteres Unicode e fontes personalizadas, e integra‑se perfeitamente com aplicações .NET, tornando‑o ideal para geração de imagens no lado do servidor e ferramentas de desktop.

- **Confiabilidade multiplataforma** – funciona em Windows, Linux e macOS.  
- **Renderização avançada** – anti‑aliasing e suavização de texto subpixel para saída nítida.  
- **Sem dependências externas** – a biblioteca inclui tudo que você precisa para *criar imagem com texto*.

## Pré‑requisitos

Antes de mergulhar, certifique‑se de que você tem:

- **Aspose.Drawing for .NET** – faça o download a partir da [documentação do Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **Um IDE .NET** como Visual Studio ou VS Code.  

## Importar namespaces

Comece importando os namespaces necessários:

Esses namespaces fornecem os tipos principais do GDI+, como `Bitmap`, `Graphics` e utilitários de renderização de texto.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Etapa 1: criar objetos bitmap e graphics

`Bitmap` é o contêiner de imagem raster da Aspose.Drawing para dados de pixel, e `Graphics` fornece métodos de desenho para renderizar formas e texto nele.  

`Bitmap` representa uma imagem na memória, enquanto `Graphics` fornece métodos de desenho para renderizar sobre esse bitmap.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Aqui criamos um `Bitmap` que armazenará a imagem final e um objeto `Graphics` que nos permite desenhar sobre ele. A dica de anti‑aliasing garante que o texto fique suave.

## Etapa 2: configurar brush, pen e font

`Brush` define a cor de preenchimento, `Pen` contorna formas, e `Font` especifica a tipografia, tamanho e estilo para renderizar texto.  

`Brush` preenche formas com cor, `Pen` contorna formas, e `Font` define a tipografia e o tamanho para renderização de texto.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** define a cor do texto.  
- **Pen** é usado posteriormente para desenhar um retângulo ao redor do texto (opcional).  
- **Font** especifica a tipografia, tamanho e estilo para a operação de *desenhar string na imagem*.

## Etapa 3: definir texto e retângulo

`Rectangle` define a caixa delimitadora onde o texto será colocado, especificando coordenadas X/Y e largura/altura.  

`Rectangle` especifica a posição e o tamanho de uma área retangular, usada aqui para limitar o texto desenhado.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

O `Rectangle` determina onde o texto será colocado. Ajuste as coordenadas e o tamanho conforme sua disposição.

## Etapa 4: desenhar retângulo e texto

`Graphics.DrawString` renderiza o texto especificado dentro do retângulo fornecido usando a fonte e brush fornecidos.  

`Graphics.DrawString` renderiza uma string de texto dentro de um retângulo especificado usando a fonte e brush fornecidos.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Primeiro delineamos a área com um retângulo azul, então **adicionamos texto ao bitmap** chamando `DrawString`. Este é o núcleo de *desenhar texto* na imagem.

## Etapa 5: salvar o resultado

A imagem é salva como um arquivo PNG, atendendo ao requisito de *salvar bitmap como PNG*. Substitua o caminho placeholder pela pasta real onde deseja armazenar o arquivo.  

`bitmap.Save` grava a imagem em um arquivo no formato escolhido, como PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Casos de uso comuns

- **Gerar certificados** com nomes personalizados.  
- **Criar miniaturas com marca d'água** para galerias web.  
- **Construir gráficos dinâmicos** que incluam rótulos ou anotações.  

## Resolução de problemas e dicas

- **Fonte não encontrada?** Certifique‑se de que a fonte esteja instalada na máquina host ou use uma coleção de fontes privada.  
- **Texto cortado?** Aumente o tamanho do retângulo ou reduza o tamanho da fonte.  
- **Preocupações de desempenho?** Reutilize o mesmo objeto `Graphics` para múltiplas operações de desenho quando possível.  

## Perguntas frequentes

**Q: Como mudar o formato de saída para JPEG?**  
A: Substitua a extensão `.png` por `.jpg` no método `Save` e, opcionalmente, especifique um `ImageCodecInfo` para a qualidade JPEG.

**Q: Posso desenhar texto em várias linhas?**  
A: Sim, inclua caracteres de quebra de linha (`\n`) na string ou use `StringFormat` com `FormatFlags.LineLimit`.

**Q: Existe uma maneira de medir o tamanho do texto antes de desenhar?**  
A: Use `Graphics.MeasureString` para obter as dimensões exatas do texto renderizado.

**Q: O Aspose.Drawing suporta caracteres Unicode?**  
A: Absolutamente. Forneça uma fonte que contenha os glifos necessários e a biblioteca os renderizará corretamente.

**Q: Qual versão do Aspose.Drawing foi usada nos testes?**  
A: Os exemplos foram testados com Aspose.Drawing 24.11 para .NET.

---

**Última atualização:** 2026-09-23  
**Testado com:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

## Tutoriais relacionados

- [Criar Gráficos Bitmap C# – Salvar Imagem PNG e Trabalhar com Fontes Instaladas no Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Como salvar um bitmap como PNG usando a API Aspose.Drawing para .NET](/drawing/net/image-editing/display/)
- [Texto em Imagem](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}