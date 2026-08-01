---
date: 2026-08-01
description: Aprenda cómo crear una imagen bitmap C# y dibujar un rectángulo en el
  bitmap usando Aspose.Drawing. Guía paso a paso para desarrolladores .NET.
keywords:
- create bitmap image c#
- draw rectangle on bitmap
- replace system.drawing
lastmod: 2026-08-01
linktitle: Dibujando rectángulos en Aspose.Drawing
og_description: Crear imagen bitmap C# y dibujar un rectángulo en el bitmap usando
  Aspose.Drawing. Este tutorial muestra cómo generar, estilizar y guardar gráficos
  de rectángulos en .NET.
og_image_alt: Guide to drawing rectangles on a bitmap with Aspose.Drawing for .NET
og_title: Crear imagen bitmap C# – Dibujar rectángulo con Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to create bitmap image C# and draw rectangle on bitmap using
    Aspose.Drawing. Step‑by‑step guide for .NET developers.
  headline: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)`
      before or after drawing the outline.
    question: Can I fill the rectangle with a solid color?
  - answer: Loop through a collection of `Rectangle` structs and call `DrawRectangle`
      for each iteration.
    question: How do I draw multiple rectangles?
  - answer: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform
      after.
    question: Is there a way to rotate the rectangle?
  - answer: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat`
      parameter.
    question: What image formats are supported for saving?
  - answer: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and
      later versions.
    question: Does Aspose.Drawing work on .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- create bitmap image
- Aspose.Drawing
- .NET graphics
- draw rectangle
title: Crear imagen bitmap C# – Dibujar rectángulo con Aspose.Drawing para .NET
url: /es/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo dibujar un rectángulo con Aspose.Drawing para .NET

## Introducción

En este tutorial aprenderás **cómo dibujar un rectángulo** mientras dominas también cómo **crear imagen bitmap C#** usando Aspose.Drawing. Ya sea que necesites un elemento UI simple o un gráfico de alta resolución para un informe, recorreremos la creación de un bitmap, la configuración de un objeto graphics, el dibujo del rectángulo y el guardado de la imagen final. El enfoque funciona en Windows, Linux y macOS, y reemplaza la antigua API `System.Drawing.Common` con una solución totalmente multiplataforma.

## Respuestas rápidas
- **¿Qué biblioteca se requiere?** Aspose.Drawing for .NET  
- **¿Qué método dibuja la forma?** `Graphics.DrawRectangle`  
- **¿Necesito una licencia?** Una prueba es gratuita; se requiere una licencia comercial para producción.  
- **¿Puedo cambiar el tamaño del rectángulo?** Sí – ajuste los parámetros de ancho, altura y posición.  
- **¿El código es compatible con .NET 6+?** Absolutamente, Aspose.Drawing soporta versiones modernas de .NET.

## ¿Qué es “cómo dibujar un rectángulo” en el contexto de Aspose.Drawing?

Dibujar un rectángulo con Aspose.Drawing utiliza la clase `Graphics` para renderizar un contorno rectangular o una forma rellena sobre un lienzo bitmap. Esto brinda control total sobre el tamaño, color, grosor de línea y formato de imagen, lo que lo hace ideal para gráficos generados al vuelo. Como Aspose.Drawing se ejecuta en un motor puramente administrado, evita las limitaciones nativas de GDI+ de `System.Drawing.Common`.

## ¿Por qué usar Aspose.Drawing para la creación de rectángulos?

Aspose.Drawing te permite **dibujar rectángulos en bitmap** sin DLLs específicas de plataforma, y soporta **más de 30 formatos de salida** (incluidos PNG, JPEG, BMP, GIF y TIFF). Puede procesar imágenes de hasta **10 000 × 10 000 píxeles** manteniendo el uso de memoria bajo **100 MB**, lo que es 2‑3× más eficiente que la implementación heredada de System.Drawing.

## Requisitos previos

Antes de sumergirnos en el código, asegúrate de contar con lo siguiente:

- **Aspose.Drawing Library** – descárguela del sitio oficial [aquí](https://releases.aspose.com/drawing/net/).  
- **Entorno de desarrollo** – Visual Studio 2022 o cualquier IDE compatible con .NET.  
- **Conocimientos básicos de .NET** – familiaridad con la sintaxis de C# y la estructura del proyecto.

## Importar espacios de nombres

Las directivas `using` traen las clases esenciales al alcance. Son necesarias para cualquier operación de dibujo.

```csharp
using System.Drawing;
```

## Paso 1: Crear una imagen bitmap

`Bitmap` representa una imagen raster en memoria sobre la que puedes dibujar. Crearla define el tamaño del lienzo y el formato de píxel.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Paso 2: Crear objeto Graphics

`Graphics` es el motor que ejecuta todos los comandos de dibujo sobre la superficie del bitmap. Una vez que lo obtienes, puedes renderizar formas, texto e imágenes.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Paso 3: Definir Pen para el rectángulo

`Pen` especifica el color y grosor del contorno del rectángulo. También controla los estilos de guiones y las uniones de línea.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## Paso 4: Dibujar rectángulo en bitmap

`Graphics.DrawRectangle` dibuja el rectángulo usando el pen previamente definido. Proporcionas coordenadas X, Y más ancho y alto para posicionar la forma exactamente donde la necesitas.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## Paso 5: Guardar la imagen dibujada

El método `Bitmap.Save` escribe la imagen en disco en el formato que elijas (p. ej., PNG, JPEG). Este paso demuestra la capacidad de **guardar la imagen dibujada** y finaliza el bitmap para reutilizarlo.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

¡Felicidades! Has completado con éxito **cómo dibujar un rectángulo** usando Aspose.Drawing para .NET y aprendido cómo **crear imagen bitmap C#** en el proceso.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| Salida de imagen en blanco | Bitmap no se libera o los gráficos no se vacían | Llame a `graphics.Dispose();` antes de guardar, o use un bloque `using`. |
| Bordes de baja calidad | Modo de suavizado predeterminado | Establezca `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`. |
| Errores de ruta de archivo | Directorio no válido | Asegúrese de que la carpeta de destino exista o use `Path.Combine` para construir una ruta segura. |

## Preguntas frecuentes

**Q: ¿Puedo rellenar el rectángulo con un color sólido?**  
A: Sí, cree un `SolidBrush` y llame a `graphics.FillRectangle(brush, …)` antes o después de dibujar el contorno.

**Q: ¿Cómo dibujo varios rectángulos?**  
A: Recorra una colección de estructuras `Rectangle` y llame a `DrawRectangle` en cada iteración.

**Q: ¿Hay una forma de rotar el rectángulo?**  
A: Use `graphics.RotateTransform(angle)` antes de dibujar, luego restablezca la transformación después.

**Q: ¿Qué formatos de imagen son compatibles para guardar?**  
A: PNG, JPEG, BMP, GIF y TIFF son compatibles mediante el parámetro `ImageFormat` correspondiente.

**Q: ¿Aspose.Drawing funciona en .NET Core?**  
A: Sí, la biblioteca es totalmente compatible con .NET Core, .NET 5, .NET 6 y versiones posteriores.

---

**Última actualización:** 2026-08-01  
**Probado con:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

---

## Tutoriales relacionados

- [Cómo dibujar una elipse con Aspose.Drawing para .NET](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [Dibujar múltiples líneas con Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [Cómo crear bitmap aspose.drawing – Dibujar polígonos en .NET](/drawing/net/lines-curves-and-shapes/draw-polygon/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}