---
date: 2026-09-23
description: Aprenda como salvar imagem PNG em C# usando Aspose.Drawing, listar fontes
  instaladas, desenhar texto com fontes personalizadas e ajustar a resolução do bitmap
  para gráficos de alta qualidade.
keywords:
- save png image c#
- installed fonts aspnet
- aspose.drawing bitmap graphics
- c# font collection
- png export .net
lastmod: 2026-09-23
linktitle: Salvar imagem PNG em C# com Aspose.Drawing e fontes instaladas
og_description: Salvar imagem PNG em C# usando Aspose.Drawing. Este guia mostra como
  listar fontes instaladas, desenhar texto e controlar a resolução do bitmap para
  gráficos profissionais.
og_image_alt: Developer guide showing C# code that creates a bitmap, lists system
  fonts, and saves a PNG file with Aspose.Drawing
og_title: Salvar imagem PNG em C# com Aspose.Drawing e fontes instaladas
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  headline: Save PNG image in C# with Aspose.Drawing and installed fonts
  type: TechArticle
- description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  name: Save PNG image in C# with Aspose.Drawing and installed fonts
  steps:
  - name: Create a bitmap (the canvas)
    text: '`Bitmap` is the raster image object that holds pixel data for the canvas.'
  - name: Create graphics from bitmap
    text: '`Graphics` is the object that supplies drawing functions such as drawing
      shapes and text onto a bitmap.'
  - name: Set up brush and font (draw text with fonts)
    text: '`Brush` defines how shapes and text are filled with colour, while `Font`
      specifies the typeface, size, and style for text rendering.'
  - name: List installed fonts and show font families
    text: '`InstalledFontCollection` provides access to all font families installed
      on the host system.'
  - name: Save PNG image
    text: '`bitmap.Save` writes the bitmap to a file in the chosen image format, such
      as PNG. > **Pro tip:** Use `Path.Combine` for building file paths to avoid issues
      with directory separators on different operating systems.'
  type: HowTo
- questions:
  - answer: Yes. Load the font file into a `PrivateFontCollection` and create a `Font`
      from that collection, then draw it the same way as system fonts.
    question: Can I use custom fonts that are not installed on the machine?
  - answer: Wrap font creation in a `try/catch` block and inspect `ArgumentException`
      for missing families; provide a fallback font such as `Arial`.
    question: How do I handle font‑related exceptions?
  - answer: Absolutely. The library works in ASP.NET Core, Azure Functions, and other
      server‑side .NET environments without needing GDI+.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify
      the `FontStyle` enum to apply bold, italic, or underline.
    question: Can I change the text colour or style?
  - answer: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – bitmap graphics and font handling
tags:
- save png
- aspose.drawing
- c# graphics
- installed fonts
- bitmap
title: Salvar imagem PNG em C# com Aspose.Drawing e fontes instaladas
url: /pt/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar imagem PNG em C# com Aspose.Drawing e fontes instaladas

## Introdução

Se você precisa **salvar imagem PNG em C#** enquanto também **cria gráficos bitmap**, o Aspose.Drawing para .NET oferece uma maneira limpa e multiplataforma de fazer isso. Neste tutorial, percorreremos a listagem de fontes instaladas, a exibição de famílias de fontes, a criação de gráficos a partir de um bitmap e o desenho de texto com fontes — tudo isso culminando na gravação do resultado como uma imagem PNG. Ao final, você terá um trecho reutilizável que pode ser inserido em qualquer projeto .NET, seja ele executado no Windows, Linux ou macOS.

## Respostas rápidas
- **O que este tutorial cria?** Uma imagem PNG que lista as famílias de fontes instaladas na máquina host.  
- **Qual biblioteca é necessária?** Aspose.Drawing para .NET (sem dependência de System.Drawing.Common).  
- **Posso usar fontes personalizadas?** Sim – carregue-as em um `InstalledFontCollection` ou em um `PrivateFontCollection`.  
- **A resolução de saída é ajustável?** Absolutamente – altere o tamanho do bitmap ou o formato de pixel para controlar a resolução.  
- **Preciso de licença para executar o código?** Uma licença temporária funciona para avaliação; uma licença completa é necessária para produção.

## O que significa “salvar imagem PNG” no contexto do Aspose.Drawing?

`Bitmap` é o contêiner de imagem raster do Aspose.Drawing que armazena dados de pixel.  
Salvar uma imagem PNG significa renderizar sua superfície de desenho — um `Bitmap` — para um arquivo com a extensão `.png`. O Aspose.Drawing realiza compressão PNG sem perdas e pode lidar com imagens de até **10 000 × 10 000 pixels** sem esgotar a memória, tornando‑a adequada para gráficos de alta resolução. O arquivo resultante pode ser usado em páginas da web, relatórios ou em pipelines adicionais de processamento de imagens.

## Por que listar fontes instaladas e mostrar famílias de fontes?

Listar fontes instaladas permite que sua aplicação se adapte ao ambiente do usuário final, garantindo que os gráficos gerados correspondam à identidade visual corporativa ou às preferências do usuário sem precisar distribuir arquivos de fonte adicionais. `InstalledFontCollection` enumera as fontes instaladas no sistema operacional. Isso é especialmente útil para geração automática de relatórios, certificados ou qualquer conteúdo visual que deva respeitar a tipografia do sistema.

## Como criar gráficos bitmap em C# com Aspose.Drawing?

`Bitmap` representa uma tela de imagem; `Graphics` fornece métodos de desenho para essa tela; `Font` descreve a tipografia usada para renderização de texto. Você pode produzir um PNG completo em apenas algumas linhas: criar um `Bitmap`, obter um objeto `Graphics`, desenhar texto usando uma `Font` da coleção instalada e, finalmente, chamar `bitmap.Save`. O guia passo a passo a seguir detalha cada parte e adiciona dicas práticas.

## Pré-requisitos

- **Biblioteca Aspose.Drawing** – faça download da versão mais recente na [página de download do Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider ou qualquer editor compatível com .NET.  
- **Conhecimento básico de C#** – você deve estar confortável com classes, objetos e loops simples.  
- **Runtime .NET** – .NET 6+ ou .NET Core 3.1+ é recomendado para suporte total multiplataforma.

## Importar namespaces

Adicione as seguintes instruções `using` no topo do seu arquivo C# para que o compilador possa localizar os tipos de gráficos e fontes:

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Text;
using System.IO;
```

## Guia passo a passo

### Etapa 1: Criar um bitmap (a tela)

`Bitmap` é o objeto de imagem raster que contém os dados de pixel da tela.  

```csharp
using System.Drawing;
using System.Drawing.Text;
```

### Etapa 2: Criar gráficos a partir do bitmap

`Graphics` é o objeto que fornece funções de desenho, como desenhar formas e texto em um bitmap.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Etapa 3: Configurar pincel e fonte (desenhar texto com fontes)

`Brush` define como formas e texto são preenchidos com cor, enquanto `Font` especifica a tipografia, tamanho e estilo para a renderização de texto.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Etapa 4: Listar fontes instaladas e mostrar famílias de fontes

`InstalledFontCollection` fornece acesso a todas as famílias de fontes instaladas no sistema host.  

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Etapa 5: Salvar imagem PNG

`bitmap.Save` grava o bitmap em um arquivo no formato de imagem escolhido, como PNG.  

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

> **Dica profissional:** Use `Path.Combine` para construir caminhos de arquivos e evitar problemas com separadores de diretório em diferentes sistemas operacionais.

## Problemas comuns e soluções
| Problema | Causa | Correção |
|----------|-------|----------|
| **Nenhuma fonte exibida** | `InstalledFontCollection` não está populado (por exemplo, executando em um servidor sem interface gráfica sem fontes). | Instale as fontes necessárias no servidor ou incorpore fontes personalizadas na sua aplicação. |
| **Arquivo salvo está corrompido** | Formato de pixel incorreto ou permissões de gravação ausentes. | Certifique-se de que a pasta de destino exista e que o aplicativo tenha permissão de escrita; mantenha `PixelFormat.Format32bppPArgb`. |
| **Texto parece borrado** | Configurações de DPI baixas ou dimensões pequenas do bitmap. | Aumente as dimensões do bitmap ou defina `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Perguntas frequentes

**P: Posso usar fontes personalizadas que não estão instaladas na máquina?**  
R: Sim. Carregue o arquivo de fonte em um `PrivateFontCollection` e crie uma `Font` a partir dessa coleção, então desenhe-a da mesma forma que as fontes do sistema.

**P: Como lidar com exceções relacionadas a fontes?**  
R: Envolva a criação da fonte em um bloco `try/catch` e verifique `ArgumentException` para famílias ausentes; forneça uma fonte alternativa como `Arial`.

**P: O Aspose.Drawing é adequado para aplicações web?**  
R: Absolutamente. A biblioteca funciona em ASP.NET Core, Azure Functions e outros ambientes .NET do lado do servidor sem necessidade de GDI+.

**P: Posso mudar a cor ou o estilo do texto?**  
R: Sim. Use diferentes tipos de `Brush` (por exemplo, `LinearGradientBrush`) e modifique o enum `FontStyle` para aplicar negrito, itálico ou sublinhado.

**P: Onde posso obter uma licença temporária para teste?**  
R: Baixe uma licença de avaliação na [página de licença temporária da Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusão

Seguindo estas etapas, você aprendeu como **salvar imagem PNG em C#** que lista dinamicamente **as fontes instaladas**, **mostra famílias de fontes**, **cria gráficos a partir de um bitmap** e **desenha texto com fontes** usando Aspose.Drawing para .NET. Agora você sabe como **criar gráficos bitmap em C#**, ajustar a resolução do bitmap e incorporar fontes personalizadas quando necessário. Experimente diferentes cores, tamanhos de fonte e dimensões do bitmap para atender aos requisitos visuais do seu projeto, e explore outros recursos do Aspose.Drawing, como desenho de formas e manipulação de imagens para gráficos mais ricos.

---

**Última atualização:** 2026-09-23  
**Testado com:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

## Tutoriais Relacionados

- [Como desenhar texto com Aspose.Drawing para .NET](/drawing/net/text-and-fonts/draw-text/)
- [Melhorar a qualidade da imagem com antialiasing no Aspose.Drawing](/drawing/net/rendering/antialiasing/)
- [Como salvar PNG com Aspose.Drawing – Transformação Mundial](/drawing/net/coordinate-transformations/world-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}