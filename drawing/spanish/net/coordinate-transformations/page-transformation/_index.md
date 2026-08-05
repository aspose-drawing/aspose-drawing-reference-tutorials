---
date: 2026-05-19
description: Aprenda a dibujar gráficos de rectángulos mientras realiza la transformación
  del sistema de coordenadas en .NET con Aspose.Drawing. Esta guía paso a paso muestra
  cómo convertir pulgadas a píxeles y establecer unidades de página.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Transformación del sistema de coordenadas en Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Cómo dibujar un rectángulo – Transformación del sistema de coordenadas (Transformación
  de página) en Aspose.Drawing para .NET
url: /es/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo dibujar un rectángulo – Transformación del sistema de coordenadas (Transformación de página) en Aspose.Drawing para .NET

## Introducción

¡Bienvenido! En este tutorial descubrirás **cómo dibujar rectángulos** gráficos mientras transformas las coordenadas de la página usando Aspose.Drawing para .NET. Ya sea que estés creando una aplicación intensiva en gráficos o necesites un control preciso sobre las unidades de dibujo, esta guía te acompañará paso a paso—desde la configuración del lienzo hasta el dibujo de un elemento rectángulo. Al final, podrás aplicar estas técnicas en tus propios proyectos con confianza.

## Respuestas rápidas
- **¿Qué es la transformación del sistema de coordenadas?** Mapeo de unidades a nivel de página (como pulgadas) a píxeles a nivel de dispositivo.  
- **¿Por qué usar Aspose.Drawing?** Ofrece una alternativa totalmente administrada y multiplataforma a System.Drawing.Common.  
- **¿Cuánto tiempo lleva implementar el ejemplo?** Aproximadamente 5‑10 minutos para una transformación de página básica.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## ¿Qué es Aspose.Drawing?

`Aspose.Drawing` es una biblioteca gráfica .NET que proporciona una **API independiente del dispositivo** para crear y manipular imágenes raster, vectores y dibujos a nivel de página sin depender de GDI+. Soporta **más de 30 formatos de imagen** y puede procesar imágenes de hasta **10 000 × 10 000 píxeles** sin cargar todo el archivo en memoria.

## ¿Por qué usar la transformación del sistema de coordenadas con Aspose.Drawing?

La transformación del sistema de coordenadas te permite diseñar gráficos en unidades del mundo real mientras la biblioteca se encarga del escalado de píxeles para cualquier dispositivo de salida. Esto garantiza un tamaño consistente en pantallas e impresoras y simplifica los cálculos de diseño.

- **Diseño independiente del dispositivo:** Escribe el código una vez y deja que Aspose.Drawing maneje el escalado de píxeles para cualquier pantalla o impresora.  
- **Dibujo de precisión:** Ideal para diagramas técnicos, bocetos estilo CAD o cualquier escenario donde las medidas exactas importen.  
- **Confiabilidad multiplataforma:** Funciona de forma consistente en Windows, Linux y macOS sin las limitaciones de GDI+ de System.Drawing.  
- **Datos de rendimiento:** En una CPU típica de 2.5 GHz, dibujar un rectángulo de 5 pulgadas a 300 DPI tarda menos de **15 ms**, y la biblioteca puede renderizar **50 fotogramas por segundo** en escenarios de vista previa en tiempo real.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Biblioteca Aspose.Drawing:** Descarga la última versión desde el sitio oficial [here](https://releases.aspose.com/drawing/net/).  
- **Entorno de desarrollo:** Visual Studio, Rider o cualquier IDE compatible con .NET.  
- **Tu directorio de documentos:** Reemplaza `"Your Document Directory"` en el código con la carpeta donde deseas guardar la imagen de salida.  
- **Soporte ASP.NET (opcional):** Puedes usar Aspose.Drawing en proyectos ASP.NET Core añadiendo el paquete NuGet a tu aplicación web—esto sigue el mismo patrón **how to use aspnet** que cualquier otra biblioteca .NET.

Ahora que todo está listo, vamos a sumergirnos en la guía paso a paso.

## ¿Cómo dibujar un rectángulo con transformación de página?

Carga un bitmap en blanco, establece la unidad de página en pulgadas y dibuja un rectángulo usando un lápiz azul delgado—esto completa el dibujo del rectángulo en solo unas pocas líneas de código. La propiedad `Graphics.PageUnit` indica al motor que interprete todas las coordenadas como pulgadas, de modo que puedas pensar en medidas del mundo real en lugar de píxeles crudos.

### Paso 1: Importar espacios de nombres

Las sentencias `using` te dan acceso a las clases centrales de dibujo.

```csharp
using System.Drawing;
```

### Paso 2: Crear un Bitmap

`Bitmap` representa una imagen en memoria sobre la que puedes dibujar. Comenzamos creando un bitmap en blanco que servirá como superficie de dibujo. El formato de píxel `Format32bppPArgb` nos brinda soporte de alfa premultiplicada de alta calidad.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Paso 3: Crear un objeto Graphics

Un objeto `Graphics` proporciona la API de dibujo para el bitmap. Es el puente entre tu código y el búfer de píxeles.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Paso 4: Limpiar el lienzo

Da al lienzo un fondo neutro para que las formas dibujadas resalten. Aquí lo rellenamos con un gris claro.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Paso 5: Establecer la transformación (Cómo establecer la unidad)

`Graphics.PageUnit` especifica la unidad de medida utilizada para las coordenadas de la página. Para mapear coordenadas de página a píxeles del dispositivo, establece la propiedad `PageUnit`. En este ejemplo elegimos pulgadas, pero también podrías usar `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` o `GraphicsUnit.Pixel`. Establecer la unidad en pulgadas permite **convertir pulgadas a píxeles** automáticamente según el DPI del bitmap (96 DPI por defecto, 300 DPI para impresión de alta resolución).

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Paso 6: Dibujar un rectángulo – draw rectangle graphics

`Pen` define el color, ancho y estilo de las líneas dibujadas sobre una superficie gráfica. Ahora dibujamos un rectángulo usando un lápiz azul delgado. Como cambiamos a pulgadas, el tamaño y la posición del rectángulo se expresan en pulgadas, lo que hace que el código sea más legible para diseños orientados a impresión.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Paso 7: Guardar la imagen

Finalmente, escribe el bitmap en un archivo PNG en la carpeta que especificaste anteriormente.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## ¿Cómo escalar gráficos para una impresora?

Establece el DPI del bitmap a la resolución objetivo de la impresora (p. ej., 300 DPI) antes de dibujar. Esto automáticamente **escala la salida gráfica de la impresora** de modo que una pulgada en tu código equivalga a una pulgada en la página impresa. Después de llamar a `bitmap.SetResolution(300, 300)`, el mismo rectángulo aparecerá más grande en la hoja impresa manteniendo sus dimensiones exactas.

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **Archivo de salida no creado** | Ruta incorrecta o carpeta inexistente | Asegúrate de que el directorio de destino exista o usa `Directory.CreateDirectory` antes de guardar. |
| **El rectángulo aparece distorsionado** | `PageUnit` incorrecto o DPI no coincidente | Verifica que `graphics.PageUnit` coincida con la unidad que pretendes usar y que el DPI del bitmap esté configurado adecuadamente (por defecto 96 DPI). |
| **Excepción de licencia** | Ejecutar sin una licencia válida en producción | Aplica tu licencia temporal o permanente de Aspose.Drawing antes de crear objetos gráficos. |

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.Drawing de forma gratuita?**  
R: Sí, hay una prueba gratuita disponible [here](https://releases.aspose.com/).

**P: ¿Dónde encuentro documentación detallada de Aspose.Drawing?**  
R: La referencia completa de la API está ubicada [here](https://reference.aspose.com/drawing/net/).

**P: ¿Cómo obtengo soporte para Aspose.Drawing?**  
R: Visita el [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) para ayuda de la comunidad y asistencia oficial.

**P: ¿Existe una licencia temporal para Aspose.Drawing?**  
R: Por supuesto—obtén una [here](https://purchase.aspose.com/temporary-license/).

**P: ¿Dónde puedo comprar una licencia completa de Aspose.Drawing?**  
R: Puedes adquirirla [here](https://purchase.aspose.com/buy).

## Conclusión

En esta guía cubrimos todo lo que necesitas para **cómo dibujar rectángulos** gráficos con Aspose.Drawing: configurar el lienzo, configurar unidades de página, dibujar formas precisas y guardar el resultado. Usa estas técnicas para crear gráficos escalables e independientes del dispositivo para informes, dibujos estilo CAD o cualquier aplicación donde la precisión de medidas sea crucial. A continuación, explora transformaciones avanzadas como rotación, escalado y orígenes de coordenadas personalizados para desbloquear escenarios de dibujo aún más potentes.

---

**Última actualización:** 2026-05-19  
**Probado con:** Aspose.Drawing 24.12 para .NET  
**Autor:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
