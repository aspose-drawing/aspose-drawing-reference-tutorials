---
date: 2025-12-01
description: Aprenda a realizar a transformação de sistema de coordenadas e a desenhar
  gráficos de retângulo no .NET usando Aspose.Drawing. Guia passo a passo sobre como
  transformar as coordenadas da página.
language: pt
linktitle: Coordinate System Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Transformação de Sistema de Coordenadas – Transformação de Página no Aspose.Drawing
  para .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Transformação de Sistema de Coordenadas – Transformação de Página no Aspose.Drawing para .NET

## Introdução

Bem‑vindo! Neste tutorial você descobrirá **como transformar coordenadas de página** usando Aspose.Drawing para .NET e aprenderá o básico da **transformação de sistema de coordenadas**. Seja você quem está construindo um aplicativo intensivo em gráficos ou precisa de controle preciso sobre unidades de desenho, este guia o conduzirá por cada passo — desde a configuração da tela até o desenho de um elemento gráfico de retângulo. Ao final, você será capaz de aplicar essas técnicas em seus próprios projetos com confiança.

## Respostas Rápidas
- **O que é transformação de sistema de coordenadas?** Mapeamento de unidades ao nível da página (como polegadas) para pixels ao nível do dispositivo.  
- **Por que usar Aspose.Drawing?** Ele oferece uma alternativa totalmente gerenciada ao System.Drawing.Common com suporte multiplataforma.  
- **Quanto tempo leva para implementar o exemplo?** Cerca de 5‑10 minutos para uma transformação de página básica.  
- **Preciso de licença?** Um teste gratuito funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## O que é transformação de sistema de coordenadas?

Uma **transformação de sistema de coordenadas** define como unidades lógicas de página (como polegadas, centímetros ou pontos) são convertidas em pixels do dispositivo ao renderizar gráficos. Ao configurar a propriedade `Graphics.PageUnit`, você indica ao mecanismo de desenho como interpretar as coordenadas fornecidas, proporcionando controle detalhado sobre tamanho e layout.

## Por que usar transformação de sistema de coordenadas com Aspose.Drawing?

- **Design independente de dispositivo:** Escreva o código uma única vez e deixe o Aspose.Drawing lidar com o dimensionamento de pixels para qualquer tela ou impressora.  
- **Desenho de precisão:** Ideal para diagramas técnicos, esboços no estilo CAD ou qualquer cenário onde medições exatas são importantes.  
- **Confiabilidade multiplataforma:** Funciona de forma consistente no Windows, Linux e macOS sem as limitações do GDI+ do System.Drawing.

## Pré‑requisitos

Antes de começarmos, certifique‑se de que você tem:

- **Biblioteca Aspose.Drawing:** Baixe a versão mais recente no site oficial [here](https://releases.aspose.com/drawing/net/).  
- **Ambiente de Desenvolvimento:** Visual Studio, Rider ou qualquer IDE compatível com .NET.  
- **Seu Diretório de Documentos:** Substitua `"Your Document Directory"` no código pela pasta onde deseja salvar a imagem de saída.

Agora que tudo está pronto, vamos mergulhar no guia passo a passo.

## Importar Namespaces

Primeiro, traga o namespace necessário para o seu projeto:

```csharp
using System.Drawing;
```

## Etapa 1: Criar um Bitmap

Começamos criando um bitmap em branco que servirá como superfície de desenho. O formato de pixel `Format32bppPArgb` nos fornece suporte de alta qualidade e alfa pré‑multiplicado.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Etapa 2: Criar um Objeto Graphics

Um objeto `Graphics` fornece a API de desenho para o bitmap. Ele é a ponte entre seu código e o buffer de pixels.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Etapa 3: Limpar a Tela

Dê à tela um fundo neutro para que as formas desenhadas se destaquem. Aqui a preenchemos com um cinza claro.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Etapa 4: Definir a Transformação (Como transformar a página)

Para mapear coordenadas da página para pixels do dispositivo, defina a propriedade `PageUnit`. Neste exemplo escolhemos polegadas, mas você também pode usar `GraphicsUnit.Millimeter`, `Point`, etc.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

## Etapa 5: Desenhar um Retângulo – desenhar gráficos de retângulo

Agora desenhamos um retângulo usando uma caneta azul fina. Como mudamos para polegadas, o tamanho e a posição do retângulo são expressos em polegadas, tornando o código mais legível para layouts voltados à impressão.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

## Etapa 6: Salvar a Imagem

Finalmente, grave o bitmap em um arquivo PNG na pasta que você especificou anteriormente.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

Parabéns! Você acabou de executar uma **transformação de sistema de coordenadas**, definir a unidade de página para polegadas e **desenhar gráficos de retângulo** em um bitmap usando Aspose.Drawing.

## Problemas Comuns e Soluções

| Problema | Por que acontece | Correção |
|----------|------------------|----------|
| **Arquivo de saída não criado** | Caminho incorreto ou pasta inexistente | Certifique-se de que o diretório de destino exista ou use `Directory.CreateDirectory` antes de salvar. |
| **Retângulo aparece distorcido** | `PageUnit` errado ou DPI incompatível | Verifique se `graphics.PageUnit` corresponde às unidades que você pretende usar e se o DPI do bitmap está configurado adequadamente (o padrão é 96 DPI). |
| **Exceção de licença** | Executando sem uma licença válida em produção | Aplique sua licença temporária ou permanente do Aspose.Drawing antes de criar objetos graphics. |

## Perguntas Frequentes

**Q: Posso usar o Aspose.Drawing gratuitamente?**  
A: Sim, um teste gratuito está disponível [here](https://releases.aspose.com/).

**Q: Onde posso encontrar documentação detalhada do Aspose.Drawing?**  
A: A referência completa da API está localizada [here](https://reference.aspose.com/drawing/net/).

**Q: Como obtenho suporte para o Aspose.Drawing?**  
A: Visite o [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17) para ajuda da comunidade e assistência oficial.

**Q: Existe uma licença temporária disponível para o Aspose.Drawing?**  
A: Absolutamente — obtenha uma [here](https://purchase.aspose.com/temporary-license/).

**Q: Onde posso comprar uma licença completa do Aspose.Drawing?**  
A: Você pode adquiri‑la [here](https://purchase.aspose.com/buy).

## Conclusão

Neste guia cobrimos tudo o que você precisa saber sobre **transformação de sistema de coordenadas** no Aspose.Drawing: configurar a tela, definir unidades de página, desenhar gráficos de retângulo precisos e salvar o resultado. Use essas técnicas para criar gráficos escaláveis e independentes de dispositivo para relatórios, desenhos no estilo CAD ou qualquer aplicação onde a precisão de medição seja importante.

---

**Última atualização:** 2025-12-01  
**Testado com:** Aspose.Drawing 24.12 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}