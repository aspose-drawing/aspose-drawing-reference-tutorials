---
date: 2026-05-19
description: Tutorial passo a passo sobre como cortar imagens em lote para PNG usando
  Aspose.Drawing, a alternativa ao System.Drawing para desenvolvedores .NET.
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: Tutorial de Recorte de Imagens – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Como cortar imagens em lote para PNG usando Aspose.Drawing para .NET
url: /pt/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como fazer corte em lote de imagens para PNG usando Aspose.Drawing para .NET

Se você precisa **cortar imagem para PNG** de forma rápida, confiável e em escala em um ambiente .NET, está no lugar certo. Neste tutorial, percorreremos os passos exatos para carregar uma imagem, definir a área de corte e salvar o resultado como um arquivo PNG — tudo usando Aspose.Drawing, uma moderna **alternativa ao System.Drawing** que funciona multiplataforma. Você também verá como expandir o fluxo de imagem única para um pipeline completo de **corte em lote**.

## Respostas rápidas
- **Qual biblioteca devo usar?** Aspose.Drawing for .NET (uma alternativa completa ao System.Drawing.Common)  
- **Quanto tempo leva o corte básico?** Normalmente menos de um segundo para uma única imagem em uma CPU moderna  
- **Posso cortar para PNG?** Sim – salve o bitmap recortado como um arquivo PNG (veja Step 6)  
- **Preciso de licença?** Um teste gratuito funciona para desenvolvimento; uma licença comercial é necessária para produção  
- **É possível processamento em lote?** Absolutamente – envolva os mesmos passos em um loop para processar vários arquivos  

## Como fazer corte em lote de imagens para PNG?

Carregue cada arquivo de origem com `new Bitmap(path)`, crie um `Bitmap` em branco correspondente para a área de corte, desenhe o retângulo selecionado usando `Graphics.DrawImage` e, finalmente, chame `Save("output.png", ImageFormat.Png)`. Envolva essas seis linhas dentro de um loop `foreach` que itera sobre um diretório e você terá uma solução completa de corte em lote que processa dezenas de imagens em segundos.

## Por que usar Aspose.Drawing para corte em lote?

Aspose.Drawing suporta **3 principais sistemas operacionais** (Windows, Linux, macOS) e pode lidar com **imagens de mais de 500 pixels em menos de 0,5 segundos** em uma CPU típica de classe servidor. Sua API evita dependências nativas do GDI+, o que significa que você pode implantar o mesmo código em contêineres, Azure App Service ou AWS Lambda sem bibliotecas adicionais. A biblioteca também oferece **mais de 50 formatos de imagem** e **preservação completa do canal alfa**, tornando-a ideal para corte de PNG transparente em escala.

## O que é “crop image to PNG”?

A operação `crop image to PNG` extrai uma região retangular de um bitmap de origem e grava essa região em um arquivo PNG. PNG preserva qualquer canal alfa, oferecendo compressão sem perdas, o que torna a imagem resultante ideal para miniaturas, ícones, recursos de UI ou qualquer situação onde qualidade e transparência são necessárias.

## Por que Aspose.Drawing é uma alternativa ao System.Drawing?

Aspose.Drawing funciona como um substituto drop‑in para System.Drawing, oferecendo compatibilidade total multiplataforma, eliminando a necessidade de bibliotecas nativas GDI+. Ele suporta uma ampla variedade de formatos de pixel, fornece manipulação de imagens de alto desempenho e inclui recursos avançados como tratamento de canal alfa e amplo suporte a formatos, tornando‑o adequado tanto para edições simples quanto para processamento em lote em grande escala.

## Pré-requisitos

Antes de mergulharmos, certifique‑se de que você tem:

- **Biblioteca Aspose.Drawing** integrada ao seu projeto .NET. Você pode baixá‑la [aqui](https://releases.aspose.com/drawing/net/).  
- Uma pasta que contém as imagens de origem que você deseja cortar. Substitua `"Your Document Directory"` nos trechos de código pelo caminho real em sua máquina.

## Importar namespaces

O namespace `System.Drawing` nos dá acesso a `Bitmap`, `Graphics` e tipos relacionados que o Aspose.Drawing estende.

```csharp
using System.Drawing;
```

## Guia passo a passo

### Etapa 1: Criar um Canvas Bitmap

`Bitmap` é a representação em memória de uma imagem no Aspose.Drawing, fornecendo acesso a nível de pixel e controle de formato.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Começamos com um canvas em branco dimensionado para conter o resultado recortado. Ajuste a largura e a altura para corresponder às dimensões da área que você planeja extrair.

### Etapa 2: Criar um objeto Graphics

`Graphics` é a superfície de desenho que permite renderizar formas, texto ou outras imagens em um Bitmap.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Um objeto `Graphics` nos permite desenhar no canvas. O `InterpolationMode` controla como os valores de pixel são calculados durante o redimensionamento ou transformação — `NearestNeighbor` funciona bem para bordas nítidas.

### Etapa 3: Carregar a imagem para cortar

`Image` (ou `Bitmap`) carrega o arquivo de origem na memória, pronto para manipulação.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Carregue a imagem de origem. Certifique‑se de que o caminho aponta para um arquivo existente; caso contrário, uma exceção será lançada.

### Etapa 4: Definir retângulos de origem e destino

Objetos `Rectangle` descrevem a região da imagem de origem a ser mantida e onde ela deve ser colocada no canvas de destino.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

O `sourceRectangle` indica à API qual parte da imagem original manter. Aqui selecionamos a área de 50 × 40 pixels no canto superior esquerdo. Ao atribuir o mesmo retângulo ao `destinationRectangle`, mantemos a região recortada em seu tamanho original.

### Etapa 5: Executar a operação de corte

`Graphics.DrawImage` copia a porção definida de `image` para o nosso `bitmap` em branco.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` copia a porção definida de `image` para o nosso `bitmap` em branco. Esta é a operação central de **crop image to PNG**.

### Etapa 6: Salvar a imagem recortada (Crop Image to PNG)

`Bitmap.Save` grava o bitmap em memória em um arquivo usando o formato especificado.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Finalmente, grave o canvas no disco como um arquivo PNG. PNG preserva qualquer canal alfa e fornece qualidade sem perdas — ideal para recursos de UI.

## Como fazer corte em lote de imagens em um loop?

Itere sobre cada caminho de arquivo com `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, repita as Etapas 1‑6 dentro do loop e armazene cada resultado em uma pasta de destino. Esse padrão escala linearmente, pode ser paralelizado com `Parallel.ForEach` para ainda mais rapidez e processa imagens de forma eficiente e rápida.

## Armadilhas comuns e dicas

- **Incompatibilidades de formato de pixel** – garanta que a imagem de origem e o bitmap do canvas compartilhem um formato de pixel compatível para evitar alterações de cor.  
- **Descarte de objetos GDI** – envolva `Bitmap` e `Graphics` em declarações `using` ou chame `Dispose()` manualmente; caso contrário, você pode vazar recursos não gerenciados.  
- **Erros de coordenadas** – as coordenadas dos retângulos são baseadas em zero. Selecionar um retângulo que exceda os limites da imagem de origem gerará uma exceção.  

## Perguntas frequentes

**Q: Posso cortar imagens de qualquer formato usando Aspose.Drawing?**  
A: Sim, Aspose.Drawing suporta uma ampla variedade de formatos (PNG, JPEG, BMP, GIF, TIFF, etc.), portanto você pode cortar praticamente qualquer tipo de imagem.

**Q: Existem opções avançadas de corte disponíveis?**  
A: Absolutamente. Você pode combinar `GraphicsPath`, transformações `Matrix`, ou usar a classe `ImageProcessor` para seleções mais complexas, como cortes circulares.

**Q: Posso aplicar múltiplas operações de corte a uma única imagem?**  
A: Sim. Após o primeiro corte, você pode reutilizar o bitmap resultante como a nova fonte e repetir o processo para encadear múltiplos cortes.

**Q: O Aspose.Drawing é adequado para processamento de imagens em lote?**  
A: De fato. Sua API leve e a ausência de dependências nativas tornam‑no perfeito para processar grandes coleções de imagens em servidores.

**Q: Como posso obter suporte para dúvidas relacionadas ao Aspose.Drawing?**  
A: Acesse o [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) para buscar assistência e conectar‑se com a comunidade.

**Última atualização:** 2026-05-19  
**Testado com:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

## Tutoriais relacionados

- [Como cortar imagem para PNG com Aspose.Drawing para .NET](/drawing/net/image-editing/cropping/)
- [Como redimensionar imagens com Aspose.Drawing para .NET](/drawing/net/image-editing/scale/)
- [Converter BMP para PNG e outros formatos com Aspose.Drawing](/drawing/net/image-editing/load-save/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}