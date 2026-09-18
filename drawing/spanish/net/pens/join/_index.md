---
date: 2026-09-18
description: Aprenda a dibujar rutas y unir rutas con plumas en Aspose.Drawing, luego
  guarde la imagen como PNG usando código simple en C#.
keywords:
- save image as png
- server side image rendering
- raster image from vector
- export graphics to png
- alternative to system drawing
lastmod: 2026-09-18
linktitle: Unir rutas con plumas en Aspose.Drawing
og_description: Guarde la imagen como PNG con Aspose.Drawing. Aprenda a dibujar rutas,
  aplicar estilos de unión de líneas y exportar gráficos raster de alta calidad a
  partir de datos vectoriales en el servidor.
og_image_alt: Developer guide showing how to draw and join paths with pens, then save
  the result as a PNG file using Aspose.Drawing
og_title: Cómo dibujar una ruta, unir rutas con plumas y guardar la imagen como PNG
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to draw path and join paths with pens in Aspose.Drawing,
    then save the image as PNG using simple C# code.
  headline: How to draw path, join paths with pens and save image as PNG
  type: TechArticle
- questions:
  - answer: Aspose.Drawing is a commercial product, but you can explore its capabilities
      with a **[free trial](https://releases.aspose.com/)**.
    question: Can I use Aspose.Drawing for free?
  - answer: Refer to the **[documentation](https://reference.aspose.com/drawing/net/)**
      for comprehensive guidance.
    question: Where can I find Aspose.Drawing documentation?
  - answer: Visit the **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)**
      for community help and official assistance.
    question: How can I get support for Aspose.Drawing?
  - answer: Yes, you can obtain a **[temporary license](https://purchase.aspose.com/temporary-license/)**
      for short‑term usage.
    question: Are temporary licenses available for Aspose.Drawing?
  - answer: Purchase Aspose.Drawing **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.
    question: Where can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- C# graphics
- save PNG
- vector to raster
- server side rendering
title: Cómo dibujar una ruta, unir rutas con plumas y guardar la imagen como PNG
url: /es/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo dibujar rutas, unir rutas con lápices y guardar la imagen como PNG

## Introducción

En este tutorial aprenderá a **draw path** objetos, unirlos con diferentes estilos de unión de líneas, y **save image as PNG** usando Aspose.Drawing para .NET. Ya sea que esté construyendo un motor de informes, un editor de diseño, o necesite renderizado de imágenes del lado del servidor para un servicio web, dominar el dibujo de rutas con lápices le brinda un control preciso sobre la conversión de vector a raster.

## Respuestas rápidas
- **¿Qué significa “draw path”?** Crea definiciones de líneas o formas basadas en vectores que un objeto `Graphics` puede renderizar.  
- **¿Qué uniones de línea están disponibles?** `Bevel`, `Miter`, `Round` y `BevelClipped`.  
- **¿Puedo exportar el resultado como PNG?** Sí—use `Bitmap.Save` con una extensión `.png`.  
- **¿Necesito una licencia?** Una prueba funciona para evaluación; se requiere una licencia comercial para producción.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.6+, .NET Core 3.1+ y .NET 6+.

## ¿Qué es “draw path” en Aspose.Drawing?

**Draw path** significa construir un `GraphicsPath` que contiene una serie de líneas, curvas o formas.  
`GraphicsPath` es el contenedor de Aspose.Drawing para geometría vectorial; luego puede renderizarlo con un `Pen` o rellenarlo con un brush. Este enfoque le permite aplicar transformaciones, recortes y estilos de unión de líneas consistentes a toda la forma en lugar de dibujar cada segmento individualmente.

## ¿Por qué usar Aspose.Drawing para renderizado de imágenes del lado del servidor?

Aspose.Drawing proporciona un motor de renderizado robusto del lado del servidor que funciona en cualquier sistema operativo sin depender de GDI+, lo que lo hace ideal para servicios en la nube, aplicaciones en contenedores y APIs web de alto rendimiento donde se requiere compatibilidad multiplataforma y operación sin interfaz gráfica, garantizando un rendimiento escalable.

- **Compatibilidad total con .NET** – soporta .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Opciones ricas de unión de líneas** – `Bevel`, `Miter`, `Round`, `BevelClipped`.  
- **Salida raster de alta calidad** – puede exportar a **más de 10 formatos raster** (PNG, JPEG, BMP, GIF, TIFF, etc.) directamente desde datos vectoriales.  
- **Sin limitaciones de GDI+** – ideal para servicios en la nube, contenedores y entornos sin interfaz gráfica.

## Requisitos previos

Antes de sumergirnos en el código, asegúrese de tener:

1. **Aspose.Drawing Library** – descárguela desde la **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.  
2. **Entorno de desarrollo .NET** – Visual Studio, VS Code, o cualquier IDE que soporte C#.

Ahora que todo está listo, repasemos cada paso.

## Importar espacios de nombres

Los espacios de nombres `System.Drawing` y `System.Drawing.Drawing2D` contienen los tipos gráficos centrales usados por Aspose.Drawing.  

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Paso 1: Crear un bitmap y un objeto graphics

`Bitmap` es el lienzo raster en memoria de Aspose.Drawing. Representa una imagen raster que puede dibujarse usando una superficie `Graphics`.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Comenzamos con un lienzo en blanco (`Bitmap`) de tamaño 1000 × 800 píxeles y obtenemos un objeto `Graphics` que renderizará nuestras órdenes de dibujo.

## Paso 2: Definir el método drawPath

`Pen` es la herramienta de Aspose.Drawing para trazar contornos vectoriales; define color, grosor y estilo de unión de línea.  

`LineJoin` controla cómo se conectan dos segmentos de línea en una esquina.  

`GraphicsPath` es el contenedor vectorial que almacena la serie de líneas que uniremos.  

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

Este método auxiliar encapsula la lógica de dibujo:

- **Pen** – establece el color y el grosor (30 px).  
- **GraphicsPath** – define dos líneas conectadas que forman una forma de “L”.  
- **LineJoin** – controla cómo se renderiza la esquina entre las dos líneas (`Bevel`, `Round`, etc.).  

Puede llamar a este método con cualquier valor de `LineJoin` para ver la diferencia visual.

## Paso 3: Unir rutas con unión de línea bevel

`LineJoin.Bevel` crea una esquina aplanada donde se encuentran las dos líneas, lo cual es útil cuando se desea una unión nítida y sin superposición.

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

## Paso 4: Unir rutas con unión de línea round

`LineJoin.Round` produce una esquina suave y redondeada—perfecta para un aspecto más pulido.

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

## Paso 5: Guardar el resultado como PNG

La llamada `Save` escribe el bitmap en un archivo en formato PNG, completando el flujo de trabajo **save image as PNG**. Ajuste la ruta para que coincida con su entorno.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **La imagen aparece en blanco** | El objeto `Graphics` no se limpió o el tamaño del bitmap es demasiado pequeño. | Llame a `graphics.Clear(Color.White);` antes de dibujar, o aumente las dimensiones del bitmap. |
| **La esquina se ve dentada** | Uso de un bitmap de baja resolución con un lápiz grueso. | Aumente el DPI del bitmap (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) o reduzca el grosor del lápiz. |
| **Error de archivo no encontrado** | Ruta de guardado inválida. | Use `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.Drawing de forma gratuita?**  
R: Aspose.Drawing es un producto comercial, pero puede explorar sus capacidades con una **[free trial](https://releases.aspose.com/)**.

**P: ¿Dónde puedo encontrar la documentación de Aspose.Drawing?**  
R: Consulte la **[documentation](https://reference.aspose.com/drawing/net/)** para obtener una guía completa.

**P: ¿Cómo puedo obtener soporte para Aspose.Drawing?**  
R: Visite el **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)** para obtener ayuda de la comunidad y asistencia oficial.

**P: ¿Están disponibles licencias temporales para Aspose.Drawing?**  
R: Sí, puede obtener una **[temporary license](https://purchase.aspose.com/temporary-license/)** para uso a corto plazo.

**P: ¿Dónde puedo comprar Aspose.Drawing?**  
R: Compre Aspose.Drawing en la **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.

## Conclusión

En esta guía cubrimos cómo **draw path** objetos, aplicar diferentes estilos `LineJoin`, y **save image as PNG** usando Aspose.Drawing para .NET. Al dominar estos pasos puede generar gráficos vectoriales sofisticados, íconos personalizados o gráficos dinámicos directamente desde código del lado del servidor, proporcionando una solución fiable de **export graphics to PNG** que funciona en cualquier plataforma.

---

**Last Updated:** 2026-09-18  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Tutoriales relacionados

- [Cómo dibujar arco y guardar imagen PNG con Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-arc/)
- [Cómo guardar bitmap como PNG mientras se dibujan múltiples líneas con Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [Cómo guardar un bitmap como PNG usando la API Aspose.Drawing para .NET](/drawing/net/image-editing/display/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}