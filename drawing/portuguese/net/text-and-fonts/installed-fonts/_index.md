---
date: 2026-02-25
description: Aprenda a criar gráficos bitmap em C# e salvar imagens PNG enquanto lista
  fontes instaladas, desenha texto com fontes e ajusta a resolução do bitmap usando
  Aspose.Drawing para .NET.
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Criar Gráficos Bitmap em C# – Salvar Imagem PNG e Trabalhar com Fontes Instaladas
  no Aspose.Drawing
url: /pt/net/text-and-fonts/installed-fonts/
weight: 13
---

 naturally to Portuguese. So yes.

Thus:

**Última atualização:** 2026-02-25  
**Testado com:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

Make sure markdown formatting preserved.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar Imagem PNG e Trabalhar com Fontes Instaladas no Aspose.Drawing

## Introdução

Se você precisar **salvar arquivos de imagem PNG** enquanto também **cria gráficos bitmap C#**, Aspose.Drawing para .NET oferece uma maneira limpa e multiplataforma de fazer isso. Neste tutorial, percorreremos a listagem de fontes instaladas, exibição de famílias de fontes, criação de gráficos a partir de um bitmap e desenho de texto com fontes — tudo isso finalizando com a gravação do resultado como uma imagem PNG. Ao final, você terá um trecho reutilizável que pode ser inserido em qualquer projeto .NET.

## Respostas Rápidas
- **O que este tutorial cria?** Uma imagem PNG que lista as famílias de fontes instaladas.  
- **Qual biblioteca é necessária?** Aspose.Drawing para .NET (não é necessário System.Drawing.Common).  
- **Posso usar fontes personalizadas?** Sim – basta carregá‑las em um `InstalledFontCollection`.  
- **A resolução de saída é ajustável?** Absolutamente – altere o tamanho do bitmap ou o formato de pixel para **adjust bitmap resolution C#** style.  
- **Preciso de licença para executar o código?** Uma licença temporária funciona para avaliação; uma licença completa é necessária para produção.

## O que significa “salvar imagem PNG” no contexto do Aspose.Drawing?
Salvar uma imagem PNG significa renderizar sua superfície de desenho (um `Bitmap`) para um arquivo com a extensão `.png`. Aspose.Drawing cuida da codificação para você, então você só precisa chamar `bitmap.Save(...)` com o caminho desejado.

## Por que listar fontes instaladas e mostrar famílias de fontes?
Saber quais fontes estão disponíveis permite criar gráficos dinâmicos que se adaptam ao ambiente do usuário final. Isso é especialmente útil para gerar relatórios, certificados ou qualquer conteúdo visual que precise corresponder à identidade corporativa sem precisar distribuir arquivos de fonte.

## Como criar gráficos bitmap C# com Aspose.Drawing?
Abaixo está um passo a passo prático que mostra exatamente como **criar gráficos bitmap C#**, desenhar texto com fontes e ajustar a resolução do bitmap, se necessário.

## Pré‑requisitos

- **Biblioteca Aspose.Drawing** – faça o download da versão mais recente na [página de download do Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider ou qualquer editor compatível com .NET.  
- **Conhecimento básico de C#** – você deve estar confortável com classes, objetos e loops simples.

## Importar Namespaces
Para trabalhar com fontes e gráficos, importe estes namespaces no topo do seu arquivo C#:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Guia Passo a Passo

### Etapa 1: Criar um bitmap (a tela)
Primeiro, criamos um bitmap que conterá a imagem final. O tamanho do bitmap e o formato de pixel determinam a qualidade do PNG salvo e permitem que você **adjust bitmap resolution C#** style.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Etapa 2: Criar gráficos a partir do bitmap
Em seguida, obtemos um objeto `Graphics` a partir do bitmap. Esse objeto permite desenhar formas, texto e imagens na tela.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Etapa 3: Configurar brush e fonte (desenhar texto com fontes)
Precisamos de um brush para a cor do texto e de um objeto `Font` que define a tipografia, tamanho e estilo. É aqui que **draw text with fonts**.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Etapa 4: Listar fontes instaladas e mostrar famílias de fontes
Agora exibimos o número de famílias de fontes e os primeiros nomes diretamente no bitmap. Isso demonstra as capacidades de **list installed fonts** e **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Etapa 5: Salvar imagem PNG
Finalmente, gravamos o bitmap no disco como um arquivo PNG. Esta é a operação central de **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Dica profissional:** Use `Path.Combine` para construir caminhos de arquivos e evitar problemas com separadores de diretório em diferentes sistemas operacionais.

## Problemas Comuns e Soluções
| Problema | Causa | Solução |
|-------|-------|-----|
| **Nenhuma fonte exibida** | `InstalledFontCollection` não está populado (por exemplo, executando em um servidor sem interface gráfica sem fontes). | Instale as fontes necessárias no servidor ou incorpore fontes personalizadas na sua aplicação. |
| **Arquivo salvo está corrompido** | Formato de pixel incorreto ou falta de permissões de gravação. | Certifique-se de que a pasta de destino exista e que o aplicativo tenha acesso de escrita; mantenha `Format32bppPArgb`. |
| **Texto parece borrado** | Configurações de DPI baixas. | Aumente as dimensões do bitmap ou defina `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Perguntas Frequentes

**Q: Posso usar fontes personalizadas que não estão instaladas na máquina?**  
A: Sim. Carregue o arquivo de fonte em um `PrivateFontCollection` e crie um `Font` a partir dessa coleção.

**Q: Como lidar com exceções relacionadas a fontes?**  
A: Envolva a criação da fonte em um bloco `try/catch` e inspecione `ArgumentException` para famílias ausentes.

**Q: O Aspose.Drawing é adequado para aplicações web?**  
A: Absolutamente. A biblioteca funciona em ASP.NET Core, Azure Functions e outros ambientes server‑side.

**Q: Posso mudar a cor ou o estilo do texto?**  
A: Sim. Use diferentes tipos de `Brush` (por exemplo, `LinearGradientBrush`) e modifique o enum `FontStyle`.

**Q: Onde posso obter uma licença temporária para testes?**  
A: Baixe uma licença de avaliação na [página de licença temporária da Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusão

Ao seguir estas etapas, você aprendeu como **salvar arquivos de imagem PNG** que listam dinamicamente **fontes instaladas**, **mostram famílias de fontes**, **criam gráficos a partir de bitmap** e **desenham texto com fontes** usando Aspose.Drawing para .NET. Agora você sabe como **criar gráficos bitmap C#**, ajustar a resolução do bitmap e incorporar fontes personalizadas quando necessário. Sinta-se à vontade para experimentar outras fontes, cores e tamanhos de bitmap para atender aos requisitos visuais do seu projeto.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2026-02-25  
**Testado com:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose