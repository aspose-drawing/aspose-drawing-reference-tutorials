---
date: 2025-12-06
description: Aprenda a salvar arquivos de imagem PNG enquanto lista fontes instaladas,
  exibe famílias de fontes, cria gráficos a partir de bitmap e desenha texto com fontes
  usando Aspose.Drawing para .NET.
language: pt
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Salvar imagem PNG e trabalhar com fontes instaladas no Aspose.Drawing
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar Imagem PNG e Trabalhar com Fontes Instaladas no Aspose.Drawing

## Introdução

Se você precisa **salvar arquivos de imagem PNG** que também exibam informações sobre as fontes instaladas em uma máquina, o Aspose.Drawing para .NET oferece uma maneira limpa e multiplataforma de fazer isso. Neste tutorial, percorreremos a listagem de fontes instaladas, a exibição de famílias de fontes, a criação de gráficos a partir de um bitmap e o desenho de texto com fontes — tudo isso culminando na gravação do resultado como uma imagem PNG. Ao final, você terá um trecho reutilizável que pode ser inserido em qualquer projeto .NET.

## Respostas Rápidas
- **O que este tutorial cria?** Uma imagem PNG que lista as famílias de fontes instaladas.  
- **Qual biblioteca é necessária?** Aspose.Drawing para .NET (não é preciso o System.Drawing.Common).  
- **Posso usar fontes personalizadas?** Sim – basta carregá‑las em um `InstalledFontCollection`.  
- **A resolução da saída é ajustável?** Absolutamente – altere o tamanho do bitmap ou o formato de pixel.  
- **Preciso de licença para executar o código?** Uma licença temporária funciona para avaliação; uma licença completa é necessária para produção.

## O que significa “salvar imagem PNG” no contexto do Aspose.Drawing?
Salvar uma imagem PNG significa renderizar sua superfície de desenho (um `Bitmap`) para um arquivo com a extensão `.png`. O Aspose.Drawing cuida da codificação para você, bastando chamar `bitmap.Save(...)` com o caminho desejado.

## Por que listar fontes instaladas e exibir famílias de fontes?
Saber quais fontes estão disponíveis permite criar gráficos dinâmicos que se adaptam ao ambiente do usuário final. Isso é especialmente útil para gerar relatórios, certificados ou qualquer conteúdo visual que precise corresponder à identidade corporativa sem precisar distribuir arquivos de fonte.

## Pré‑requisitos

- **Biblioteca Aspose.Drawing** – baixe a versão mais recente na [página de download do Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider ou qualquer editor compatível com .NET.  
- **Conhecimento básico de C#** – você deve estar confortável com classes, objetos e loops simples.

## Importar Namespaces
Para trabalhar com fontes e gráficos, importe estes namespaces no topo do seu arquivo C#:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Guia Passo a Passo

### Passo 1: Criar um bitmap (a tela)
Primeiro, criamos um bitmap que armazenará a imagem final. O tamanho do bitmap e o formato de pixel determinam a qualidade do PNG salvo.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Passo 2: Criar graphics a partir do bitmap
Em seguida, obtemos um objeto `Graphics` a partir do bitmap. Esse objeto permite desenhar formas, texto e imagens na tela.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Passo 3: Configurar brush e font (desenhar texto com fontes)
Precisamos de um brush para a cor do texto e de um objeto `Font` que define a família, o tamanho e o estilo da fonte.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Passo 4: Listar fontes instaladas e exibir famílias de fontes
Agora exibimos o número de famílias de fontes e os primeiros nomes diretamente no bitmap. Isso demonstra as funcionalidades de **list installed fonts** e **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Passo 5: Salvar imagem PNG
Por fim, gravamos o bitmap no disco como um arquivo PNG. Esta é a operação central de **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Dica profissional:** Use `Path.Combine` para montar caminhos de arquivos e evitar problemas com separadores de diretório em diferentes sistemas operacionais.

## Problemas Comuns e Soluções
| Problema | Causa | Correção |
|----------|-------|----------|
| **Nenhuma fonte exibida** | `InstalledFontCollection` não foi preenchido (por exemplo, ao executar em um servidor sem interface gráfica). | Instale as fontes necessárias no servidor ou incorpore fontes personalizadas na sua aplicação. |
| **Arquivo salvo está corrompido** | Formato de pixel incorreto ou falta de permissões de gravação. | Garanta que a pasta de destino exista e que a aplicação tenha acesso de escrita; mantenha `Format32bppPArgb`. |
| **Texto parece borrado** | Configurações de DPI baixas. | Aumente as dimensões do bitmap ou defina `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Perguntas Frequentes

**P: Posso usar fontes personalizadas que não estão instaladas na máquina?**  
R: Sim. Carregue o arquivo de fonte em um `PrivateFontCollection` e crie um `Font` a partir dessa coleção.

**P: Como lidar com exceções relacionadas a fontes?**  
R: Envolva a criação da fonte em um bloco `try/catch` e verifique `ArgumentException` para famílias ausentes.

**P: O Aspose.Drawing é adequado para aplicações web?**  
R: Absolutamente. A biblioteca funciona em ASP.NET Core, Azure Functions e outros ambientes server‑side.

**P: Posso mudar a cor ou o estilo do texto?**  
R: Sim. Use diferentes tipos de `Brush` (por exemplo, `LinearGradientBrush`) e modifique o enum `FontStyle`.

**P: Onde posso obter uma licença temporária para testes?**  
R: Baixe uma licença de avaliação na [página de licença temporária da Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusão

Seguindo estes passos, você aprendeu a **salvar arquivos de imagem PNG** que listam dinamicamente **fontes instaladas**, **exibem famílias de fontes**, **criam gráficos a partir de bitmap** e **desenham texto com fontes** usando o Aspose.Drawing para .NET. Sinta‑se à vontade para experimentar outras fontes, cores e tamanhos de bitmap para atender aos requisitos visuais do seu projeto.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2025-12-06  
**Testado com:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose