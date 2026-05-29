---
date: 2026-05-29
description: Aprenda cómo guardar PNG y dibujar splines cardinales en .NET con Aspose.Drawing.
  Guarde la curva como PNG, cree gráficos suaves y genere un mapa de bits en un archivo
  sin esfuerzo.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Dibujando splines cardinales en Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cómo guardar PNG y dibujar splines cardinales con Aspose.Drawing
url: /es/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo guardar PNG y dibujar splines cardinales con Aspose.Drawing

## Introducción

En este tutorial descubrirás **cómo guardar PNG** mientras dibujas splines cardinales suaves usando Aspose.Drawing para .NET. Ya sea que estés construyendo un componente de gráficos, un editor de diagramas o simplemente necesites exportar una curva personalizada como PNG, los pasos a continuación te guiarán a través de la creación de un lienzo bitmap, el dibujo de un spline con un lápiz y la persistencia del resultado en disco. También verás por qué Aspose.Drawing es una alternativa multiplataforma confiable a System.Drawing.Common.

## Respuestas rápidas
- **¿Qué hace el método principal?** `Graphics.DrawCurve` interpola una serie de puntos en un spline cardinal suave.  
- **¿Qué formato se utiliza para guardar la imagen?** PNG mediante `Bitmap.Save`.  
- **¿Necesito una licencia para guardar imágenes?** Una versión de prueba funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Puedo cambiar la tensión de la curva?** Sí, las sobrecargas de `DrawCurve` permiten especificar la tensión.  
- **¿Es Aspose.Drawing compatible con .NET 6+?** Absolutamente – soporta .NET Framework y .NET Core/5/6.

## ¿Qué significa “cómo guardar PNG” en el contexto de Aspose.Drawing?

Guardar un PNG implica convertir el bitmap en memoria en el que dibujas en un archivo PNG físico en disco. El proceso escribe los datos de píxeles usando compresión sin pérdida, preservando los colores exactos y cualquier información de canal alfa. El método `Bitmap.Save` de Aspose.Drawing maneja la codificación PNG automáticamente, por lo que no necesitas gestionar los detalles del formato tú mismo.

## ¿Por qué dibujar un spline cardinal con Aspose.Drawing?

Un spline cardinal produce una curva suave y fluida que sigue de cerca un conjunto de puntos de control, lo que lo hace perfecto para **visualizaciones de datos**, **gráficos de UI** y **formas personalizadas**. Aspose.Drawing soporta **más de 30 formatos de imagen** y puede renderizar gráficos de cientos de páginas sin cargar todo el archivo en memoria, brindándote velocidad y flexibilidad.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- Visual Studio (cualquier versión reciente) instalado.  
- Biblioteca Aspose.Drawing para .NET. Puedes descargarla [aquí](https://releases.aspose.com/drawing/net/).  
- Conocimientos básicos de programación en C#.

## Importar espacios de nombres

En tu archivo C#, comienza importando el espacio de nombres necesario:

El espacio de nombres `Aspose.Drawing` contiene todos los tipos principales como `Bitmap`, `Graphics` y `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Paso 1: Crear un Bitmap (Lienzo)

Primero, crea un bitmap que actuará como lienzo para tu dibujo. Este bitmap es donde se renderizará el spline antes de **guardar la imagen**.

Bitmap representa una imagen en memoria con un formato de píxel y dimensiones definidos.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Paso 2: Crear un objeto Graphics

A continuación, obtén un objeto `Graphics` del bitmap. Este objeto proporciona la superficie de dibujo.

Graphics ofrece una superficie de dibujo para renderizar formas, texto e imágenes sobre un bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Paso 3: Definir Pen y dibujar la curva

Define un `Pen` con el color y ancho deseados, luego dibuja el spline cardinal usando `DrawCurve`. Esto demuestra la técnica de **dibujar curva con lápiz** y sirve como **ejemplo de spline cardinal**.

Pen encapsula el color, ancho y estilo de línea usados para dibujar líneas y curvas.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Paso 4: Guardar la imagen (Guardar la curva como PNG)

Finalmente, persiste el bitmap en un archivo PNG. Este es el núcleo de **cómo guardar PNG** en este tutorial.

Bitmap.Save escribe la imagen en un archivo con el formato especificado, como PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Consejo:** Usa `Path.Combine` para construir rutas de archivo de forma segura en todas las plataformas.

¡Felicidades! Has dibujado con éxito un spline cardinal y guardado el resultado como una imagen PNG usando Aspose.Drawing para .NET. Siéntete **libre** de experimentar con diferentes arreglos de puntos, colores de lápiz o anchos de línea para personalizar tus curvas.

## Casos de uso comunes

- **Visualizaciones de datos** – gráficos de líneas suaves que requieren puntos de control precisos.  
- **Componentes UI personalizados** – dibujar perillas, deslizadores o bordes decorativos.  
- **Gráficos exportables** – generar activos PNG al vuelo para **informes** o **contenido web**.

## Solución de problemas y consejos

- **¿La imagen aparece en blanco?** Asegúrate de que el formato de píxel del bitmap soporte alfa (`Format32bppPArgb`) y de llamar a `graphics.Clear(Color.Transparent)` si es necesario.  
- **¿Forma de la curva inesperada?** Ajusta el parámetro de tensión usando la sobrecarga `DrawCurve(pen, points, tension)`.  
- **¿Errores de acceso al archivo?** Verifica que el directorio de destino exista y que tu aplicación tenga permisos de escritura.

## Preguntas frecuentes

**P1: ¿Puedo usar Aspose.Drawing en proyectos comerciales?**  
R1: Sí, Aspose.Drawing es adecuado tanto para proyectos personales como comerciales. Consulta los detalles de licenciamiento en la [página de compra](https://purchase.aspose.com/buy).

**P2: ¿Cómo puedo obtener una licencia temporal para pruebas?**  
R2: Obtén una licencia temporal para propósitos de prueba [aquí](https://purchase.aspose.com/temporary-license/).

**P3: ¿Dónde puedo encontrar soporte adicional?**  
R3: Visita el [foro de Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para soporte comunitario y discusiones.

**P4: ¿Hay una versión de prueba gratuita disponible?**  
R4: Sí, explora las funciones con la versión de [prueba gratuita](https://releases.aspose.com/) antes de realizar una compra.

**P5: ¿Cómo accedo a la documentación?**  
R5: Consulta la completa [documentación](https://reference.aspose.com/drawing/net/) para información detallada y ejemplos.

---

**Última actualización:** 2026-05-29  
**Probado con:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriales relacionados

- [Guardar bitmap como PNG y dibujar curvas cerradas con Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Guardar bitmap C# – Dibujar splines Bézier con Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Guardar bitmap como PNG con pinceles sólidos en Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}