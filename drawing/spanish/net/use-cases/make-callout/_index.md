---
date: 2026-08-01
description: Aprenda cómo agregar callouts a imágenes usando Aspose.Drawing for .NET
  – guía paso a paso con marcadores de código, consejos y preguntas frecuentes.
keywords:
- how to add callouts
- Aspose.Drawing callout tutorial
- .NET image annotation
lastmod: 2026-08-01
linktitle: Crear Callouts en Aspose.Drawing
og_description: Descubra cómo agregar callouts en Aspose.Drawing for .NET. Este tutorial
  cubre los requisitos previos, la implementación paso a paso, consejos y preguntas
  frecuentes para desarrolladores.
og_image_alt: Screenshot showing callout annotation on an image using Aspose.Drawing
og_title: Cómo agregar Callouts con Aspose.Drawing for .NET – Guía rápida
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to add callouts to images using Aspose.Drawing for .NET –
    step‑by‑step guide with code placeholders, tips, and FAQs.
  headline: How to Add Callouts with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of drawing operations for diagrams,
      charts, and custom graphics beyond simple callouts.
    question: Can I use Aspose.Drawing for other types of illustrations?
  - answer: Absolutely! Aspose.Drawing handles PNG, JPEG, GIF, BMP, TIFF, and many
      more formats.
    question: Is Aspose.Drawing compatible with different image formats?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find more examples and documentation?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      for community assistance and official support.
    question: How do I get support if I encounter issues?
  - answer: Certainly! Get started with a free trial [here](https://releases.aspose.com/).
    question: Can I try Aspose.Drawing before purchasing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- callout
- Aspose.Drawing
- .NET graphics
- image annotation
title: Cómo agregar Callouts con Aspose.Drawing for .NET
url: /es/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo agregar callouts con Aspose.Drawing para .NET

## Introducción
Si estás buscando **cómo agregar callouts** a tus imágenes o diagramas usando Aspose.Drawing para .NET, has llegado al lugar correcto. En este tutorial recorreremos cada paso—desde cargar un bitmap, crear un lienzo `Graphics`, definir la geometría del callout, hasta renderizar callouts con estilo—para que tus visuales sean más claros y más informativos.

## Respuestas rápidas
- **¿Qué biblioteca necesito?** Aspose.Drawing for .NET (descargable del sitio oficial).  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para un callout básico.  
- **¿Puedo personalizar colores y fuentes?** Sí—todo se basa en objetos estándar de GDI+ (Pen, Font, Brush).

## ¿Qué es un callout?
Un callout es una anotación gráfica que combina una línea (o flecha) con una etiqueta de texto para resaltar una parte específica de una imagen. Se usa comúnmente en diagramas técnicos, capturas de pantalla y presentaciones para llamar la atención sobre un elemento particular, explicar una característica o proporcionar información de medida, haciendo la comunicación visual más clara y efectiva.

## ¿Por qué usar Aspose.Drawing para callouts?
Aspose.Drawing está diseñado para el procesamiento de imágenes de alto rendimiento y soporta una amplia gama de formatos, lo que lo hace ideal para agregar callouts a gráficos grandes o complejos. Su arquitectura eficiente en memoria puede manejar archivos de hasta **500 MB** sin cargar todo el bitmap en RAM, y ofrece control granular sobre primitivas de dibujo, colores y renderizado de texto, garantizando anotaciones nítidas y de aspecto profesional.

## Requisitos previos
Antes de sumergirte, asegúrate de tener:

- Conocimientos básicos del lenguaje de programación C#.  
- Biblioteca Aspose.Drawing instalada. Puedes descargarla [aquí](https://releases.aspose.com/drawing/net/).  
- Un documento o imagen donde quieras agregar callouts.

## Importar espacios de nombres
Los siguientes espacios de nombres te dan acceso a las clases principales de dibujo:

`System.Drawing` proporciona tipos GDI+ como `Bitmap`, `Graphics`, `Pen`, `Font` y `Brush`. Impórtalos antes de comenzar a programar.

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Cómo agregar callouts en Aspose.Drawing
Carga tu imagen fuente, crea un lienzo `Graphics`, define los puntos de inicio/fin, e invoca un método auxiliar que dibuja la línea, la punta de flecha y la etiqueta—todo en unas pocas instrucciones concisas. Este enfoque funciona para archivos PNG, JPEG, BMP y GIF y te permite personalizar completamente colores, fuentes y estilos de línea.

## Paso 1: Cargar la imagen
`Image` representa una imagen raster y proporciona métodos para cargar, guardar y manipular datos de bitmap. Comienza cargando la imagen donde deseas agregar callouts. Reemplaza `"Your Document Directory"` y `"gears.png"` con tu directorio real y el nombre de archivo de la imagen.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Paso 2: Crear objeto Graphics
`Graphics` proporciona métodos de superficie de dibujo para renderizar formas, texto e imágenes sobre un bitmap. Un objeto `Graphics` a partir de la imagen te permite realizar operaciones de dibujo.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Paso 3: Definir posiciones del callout
`PointF` define un punto en un espacio bidimensional usando coordenadas de punto flotante. Especifica los puntos de inicio (ancla) y fin (etiqueta) para cada callout. Estas coordenadas deben estar dentro de los límites de la imagen; de lo contrario el callout será recortado.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## Paso 4: Dibujar callouts
Implementa el método `DrawCallOut` para renderizar la línea, la punta de flecha opcional y la etiqueta de texto. El método usa `Pen` para la línea, `Font` para la etiqueta y `SolidBrush` para los colores de relleno.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Paso 5: Guardar la imagen
Persistir el bitmap anotado en disco. Puedes elegir cualquier formato compatible como PNG o JPEG.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Código fuente del callout
El código fuente completo que une todos los pasos se encuentra en el marcador de posición a continuación. Inserta tus propios detalles de implementación donde se indique.

```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## Problemas comunes y consejos
- **Coordenadas de ancla incorrectas** – asegúrate de que los puntos de inicio y fin estén dentro de los límites de la imagen; de lo contrario el callout puede ser recortado.  
- **Superposición de texto** – ajusta `spaceSize` o el tamaño de la fuente si la etiqueta colisiona con otros gráficos.  
- **Rendimiento** – para imágenes muy grandes, considera disponer de los objetos `Pen`, `Font` y `Brush` después de usarlos para liberar recursos.

## Conclusión
Ahora tienes un patrón completo y listo para producción para **cómo agregar callouts** a cualquier imagen usando Aspose.Drawing para .NET. Siéntete libre de experimentar con diferentes colores, estilos de línea y familias de fuentes para que coincidan con tu marca.

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.Drawing para otros tipos de ilustraciones?**  
R: Sí, Aspose.Drawing soporta una amplia gama de operaciones de dibujo para diagramas, gráficos y gráficos personalizados más allá de los callouts simples.

**P: ¿Aspose.Drawing es compatible con diferentes formatos de imagen?**  
R: ¡Absolutamente! Aspose.Drawing maneja PNG, JPEG, GIF, BMP, TIFF y muchos más formatos.

**P: ¿Dónde puedo encontrar más ejemplos y documentación?**  
R: Explora la documentación completa [aquí](https://reference.aspose.com/drawing/net/).

**P: ¿Cómo obtengo soporte si encuentro problemas?**  
R: Visita el [foro de Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para asistencia de la comunidad y soporte oficial.

**P: ¿Puedo probar Aspose.Drawing antes de comprar?**  
R: ¡Claro! Comienza con una prueba gratuita [aquí](https://releases.aspose.com/).

---

**Última actualización:** 2026-08-01  
**Probado con:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriales relacionados

- [Cómo dibujar arcos y otras formas con Aspose.Drawing para .NET](/drawing/net/lines-curves-and-shapes/)
- [Tutorial de transformación de matrices: Transformaciones de matrices en Aspose.Drawing para .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Cómo unir rutas con Pen en Aspose.Drawing .NET](/drawing/net/pens/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}