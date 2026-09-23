---
date: 2026-09-23
description: Aprenda cómo dibujar texto en una imagen usando Aspose.Drawing para .NET.
  Genere una imagen con texto, añada texto a un bitmap y guarde el bitmap como PNG
  con fuentes personalizadas.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Cómo dibujar texto con Aspose.Drawing
og_description: Aprenda cómo dibujar texto en una imagen usando Aspose.Drawing para
  .NET. Este tutorial le muestra cómo generar una imagen con texto, añadir texto a
  un bitmap y guardar el bitmap como PNG con fuentes personalizadas.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Dibujar texto en una imagen con Aspose.Drawing para .NET – Guía rápida
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
title: Cómo dibujar texto en una imagen con Aspose.Drawing para .NET
url: /es/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo dibujar texto en una imagen con Aspose.Drawing para .NET

## Introducción

In this step‑by‑step guide you’ll learn **cómo dibujar texto en una imagen** using Aspose.Drawing for .NET. Whether you need to create a *imagen de texto dinámico*, add text to an existing bitmap, or generate a graphic with custom fonts, this tutorial walks you through every detail so you can start drawing text in minutes. The library supports over 30 GDI+ methods, runs on Windows, Linux, and macOS, and has **cero dependencias externas**, making it a reliable choice for server‑side image generation.

## Respuestas rápidas
- **¿Qué biblioteca se usa?** Aspose.Drawing for .NET  
- **¿Tarea principal?** Dibujar texto en una imagen (crear imagen con texto)  
- **¿Método clave?** `Graphics.DrawString` (dibujar cadena en la imagen)  
- **¿Formato de salida?** PNG (guardar bitmap como PNG)  
- **¿Requisitos previos?** Entorno de desarrollo .NET y biblioteca Aspose.Drawing  

## ¿Qué es dibujar texto con Aspose.Drawing?

Dibujar texto con Aspose.Drawing significa usar la API compatible con GDI+ de la biblioteca para renderizar cadenas Unicode en un lienzo raster. El método `Graphics.DrawString` escribe el texto en un bitmap, permitiéndote controlar la fuente, el color, la alineación y el anti‑aliasing. Este enfoque te permite generar imágenes de alta calidad sin instalar System.Drawing.Common.

## ¿Por qué usar Aspose.Drawing para añadir texto a imágenes?

Aspose.Drawing ofrece una forma fiable y multiplataforma de renderizar texto en imágenes sin necesitar bibliotecas nativas GDI+, proporcionando calidad y rendimiento consistentes en cualquier sistema operativo. Soporta anti‑aliasing avanzado, caracteres Unicode y fuentes personalizadas, e integra sin problemas con aplicaciones .NET, lo que lo hace ideal para la generación de imágenes del lado del servidor y herramientas de escritorio por igual.

- **Confiabilidad multiplataforma** – funciona en Windows, Linux y macOS.  
- **Renderizado avanzado** – anti‑aliasing y suavizado de texto subpíxel para una salida nítida.  
- **Sin dependencias externas** – la biblioteca incluye todo lo necesario para *crear imagen con texto*.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Aspose.Drawing for .NET** – descárgala desde la [documentación de Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **Un IDE .NET** como Visual Studio o VS Code.  

## Importar espacios de nombres

Comienza importando los espacios de nombres requeridos:

Estos espacios de nombres proporcionan los tipos centrales de GDI+ como `Bitmap`, `Graphics` y utilidades de renderizado de texto.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Paso 1: crear objetos bitmap y graphics

`Bitmap` es el contenedor de imagen raster de Aspose.Drawing para datos de píxeles, y `Graphics` proporciona métodos de dibujo para renderizar formas y texto sobre él.

`Bitmap` representa una imagen en memoria, mientras que `Graphics` ofrece métodos de dibujo para renderizar sobre ese bitmap.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Aquí creamos un `Bitmap` que contendrá la imagen final y un objeto `Graphics` que nos permite dibujar sobre él. La pista de anti‑aliasing asegura que el texto se vea suave.

## Paso 2: configurar brush, pen y font

`Brush` define el color de relleno, `Pen` delimita las formas, y `Font` especifica la tipografía, tamaño y estilo para renderizar texto.

`Brush` rellena las formas con color, `Pen` delimita las formas, y `Font` define la tipografía y el tamaño para el renderizado de texto.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** define el color del texto.  
- **Pen** se usa más adelante para dibujar un rectángulo alrededor del texto (opcional).  
- **Font** especifica la tipografía, tamaño y estilo para la operación de *dibujar cadena en la imagen*.

## Paso 3: definir texto y rectángulo

`Rectangle` define el cuadro delimitador donde se colocará el texto, especificando coordenadas X/Y y ancho/alto.

`Rectangle` especifica la posición y el tamaño de un área rectangular, usada aquí para delimitar el texto dibujado.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

El `Rectangle` determina dónde se colocará el texto. Ajusta las coordenadas y el tamaño según tu diseño.

## Paso 4: dibujar rectángulo y texto

`Graphics.DrawString` renderiza el texto especificado dentro del rectángulo dado usando la fuente y el brush proporcionados.

`Graphics.DrawString` renderiza una cadena de texto dentro de un rectángulo especificado usando la fuente y el brush dados.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Primero delineamos el área con un rectángulo azul, luego **añadimos texto al bitmap** llamando a `DrawString`. Este es el núcleo de *dibujar texto* en la imagen.

## Paso 5: guardar el resultado

La imagen se guarda como archivo PNG, cumpliendo el requisito de *guardar bitmap como PNG*. Reemplaza la ruta de marcador de posición con la carpeta real donde deseas almacenar el archivo.

`bitmap.Save` escribe la imagen en un archivo en el formato elegido, como PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Casos de uso comunes

- **Generar certificados** con nombres personalizados.  
- **Crear miniaturas con marca de agua** para galerías web.  
- **Construir gráficos dinámicos** que incluyan etiquetas o anotaciones.  

## Solución de problemas y consejos

- **¿Fuente no encontrada?** Asegúrate de que la fuente esté instalada en la máquina host o usa una colección de fuentes privada.  
- **¿Texto recortado?** Aumenta el tamaño del rectángulo o reduce el tamaño de la fuente.  
- **¿Preocupaciones de rendimiento?** Reutiliza el mismo objeto `Graphics` para múltiples operaciones de dibujo cuando sea posible.  

## Preguntas frecuentes

**P: ¿Cómo cambio el formato de salida a JPEG?**  
R: Reemplaza la extensión `.png` por `.jpg` en el método `Save` y, opcionalmente, especifica un `ImageCodecInfo` para la calidad JPEG.

**P: ¿Puedo dibujar texto multilínea?**  
R: Sí, incluye caracteres de salto de línea (`\n`) en la cadena o usa `StringFormat` con `FormatFlags.LineLimit`.

**P: ¿Hay una forma de medir el tamaño del texto antes de dibujar?**  
R: Usa `Graphics.MeasureString` para obtener las dimensiones exactas del texto renderizado.

**P: ¿Aspose.Drawing admite caracteres Unicode?**  
R: Absolutamente. Proporciona una fuente que contenga los glifos necesarios y la biblioteca los renderizará correctamente.

**P: ¿Qué versión de Aspose.Drawing se usó para las pruebas?**  
R: Los ejemplos se probaron con Aspose.Drawing 24.11 para .NET.

---

**Última actualización:** 2026-09-23  
**Probado con:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Crear gráficos Bitmap C# – Guardar imagen PNG y trabajar con fuentes instaladas en Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Cómo guardar un bitmap como PNG usando la API Aspose.Drawing para .NET](/drawing/net/image-editing/display/)
- [Texto en Imagen](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}