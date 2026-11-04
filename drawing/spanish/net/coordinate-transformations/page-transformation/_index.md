---
date: 2026-11-04
description: Aprenda cómo dibujar gráficos de rectángulos mientras realiza la transformación
  del sistema de coordenadas en .NET con la API de Aspose.Drawing. Esta guía paso
  a paso muestra cómo convertir inches a pixels y establecer page units.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Transformación del sistema de coordenadas en Aspose.Drawing
og_description: Aprenda cómo dibujar gráficos de rectángulos mientras convierte inches
  a pixels y establece page units en Aspose.Drawing para .NET. Siga la guía paso a
  paso para una transformación de página precisa.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Cómo dibujar un rectángulo con transformación de página usando Aspose.Drawing
  para .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Cómo dibujar un rectángulo – transformación del sistema de coordenadas (transformación
  de página) en Aspose.Drawing para .NET
url: /es/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo dibujar un rectángulo – transformación del sistema de coordenadas (transformación de página) en Aspose.Drawing para .NET

## Introducción

En este tutorial aprenderás **cómo dibujar un rectángulo** gráfico mientras realizas una transformación del sistema de coordenadas a nivel de página usando Aspose.Drawing para .NET. Ya sea que estés construyendo un motor de informes, una herramienta de bocetos estilo CAD, o cualquier aplicación que necesite mediciones del mundo real precisas, esta guía te lleva paso a paso—desde crear un bitmap hasta guardar el PNG final. Al final estarás cómodo convirtiendo pulgadas a píxeles, limpiando el fondo del lienzo y configurando unidades de página para una salida lista para imprimir.

## Respuestas rápidas
- **¿Qué es la transformación del sistema de coordenadas?** Mapea unidades a nivel de página (como pulgadas) a píxeles a nivel de dispositivo para que los dibujos se escalen correctamente en cualquier dispositivo de salida.  
- **¿Por qué elegir Aspose.Drawing?** Proporciona una API gráfica totalmente gestionada y multiplataforma que reemplaza System.Drawing.Common y soporta más de 30 formatos de imagen.  
- **¿Cuánto tiempo lleva implementar el ejemplo?** Aproximadamente 5‑10 minutos para un rectángulo básico con transformación de página.  
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para implementaciones en producción.  
- **¿Qué entornos de ejecución .NET son compatibles?** .NET Framework 4.6+, .NET Core 3.1+, y .NET 5/6/7.

## ¿Qué es Aspose.Drawing?

Aspose.Drawing es una biblioteca gráfica .NET que ofrece una **API independiente del dispositivo** para crear y manipular imágenes raster, vectores y dibujos a nivel de página sin depender de GDI+. Soporta **más de 30 formatos de imagen** y puede procesar imágenes de hasta **10,000 × 10,000 píxeles** manteniendo bajo el uso de memoria.

## ¿Por qué usar la transformación del sistema de coordenadas con Aspose.Drawing?

La transformación del sistema de coordenadas te permite diseñar gráficos en unidades del mundo real mientras la biblioteca maneja automáticamente el escalado de píxeles para cualquier dispositivo de salida. Este enfoque garantiza que un rectángulo de 5 pulgadas se imprima exactamente a cinco pulgadas en una impresora de 300 DPI y aparezca proporcionalmente en una pantalla de 96 DPI, eliminando errores de conversión manual.

- **Diseño independiente del dispositivo:** Escribe el código una sola vez; Aspose.Drawing lo escala para pantallas, impresoras o PDFs.  
- **Dibujo de precisión:** Ideal para diagramas técnicos, esquemas de ingeniería o cualquier escenario donde las medidas exactas importen.  
- **Confiabilidad multiplataforma:** Funciona de manera consistente en Windows, Linux y macOS sin las limitaciones de GDI+ de System.Drawing.  
- **Rendimiento:** En una CPU típica de 2.5 GHz, dibujar un rectángulo de 5 pulgadas a 300 DPI se completa en menos de **15 ms**, y la biblioteca puede renderizar **50 fotogramas por segundo** en escenarios de vista previa en tiempo real.

## Requisitos previos

- **Biblioteca Aspose.Drawing:** Descarga la última versión desde el sitio oficial [here](https://releases.aspose.com/drawing/net/).  
- **IDE:** Visual Studio, Rider o cualquier editor compatible con .NET.  
- **Carpeta de salida:** Reemplaza `"Your Document Directory"` en el código de ejemplo con la carpeta donde deseas guardar el PNG.  
- **Soporte opcional para ASP.NET:** Puedes agregar el paquete NuGet a un proyecto ASP.NET Core y usar la misma API; el patrón sigue el enfoque típico **how to use aspnet** para bibliotecas .NET.

## ¿Cómo dibujar un rectángulo con transformación de página?

Carga un bitmap en blanco, establece la unidad de página en pulgadas y dibuja un rectángulo usando un lápiz azul delgado—esto completa el dibujo del rectángulo en solo unas pocas líneas de código. La propiedad `Graphics.PageUnit` indica al motor que interprete todas las coordenadas como pulgadas, de modo que puedas pensar en medidas del mundo real en lugar de píxeles crudos, y la biblioteca convierte automáticamente **pulgadas a píxeles** según el DPI del bitmap.

### Paso 1: importar espacios de nombres

Las sentencias `using` te dan acceso a las clases centrales de dibujo.

```csharp
using System.Drawing;
```

### Paso 2: crear un bitmap

`Bitmap` es el contenedor de imagen en memoria sobre el que dibujas. Mantiene el búfer de píxeles y expone métodos para guardar en archivos. Crear un bitmap define el tamaño del lienzo y el formato de píxel.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Paso 3: crear un objeto Graphics

`Graphics` proporciona la superficie de dibujo para el bitmap. Traduce comandos de dibujo de alto nivel (líneas, formas, texto) en operaciones de píxeles sobre el bitmap subyacente.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Paso 4: limpiar el fondo del lienzo

Limpiar el lienzo con un color neutro asegura que tus formas destaquen. En este ejemplo rellenamos el fondo con gris claro, lo que también demuestra la técnica de **clear canvas background**.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Paso 5: establecer la transformación (cómo establecer unidades)

`Graphics.PageUnit` especifica la unidad de medida usada para las coordenadas de página. Configurarlo a `GraphicsUnit.Inch` indica a Aspose.Drawing que **convierta pulgadas a píxeles** automáticamente según el DPI del bitmap (96 DPI por defecto, 300 DPI para impresión de alta resolución). También podrías elegir `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` o `GraphicsUnit.Pixel` según los requisitos de tu diseño.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Paso 6: dibujar un rectángulo – dibujar gráficos de rectángulo

`Pen` define el color, ancho y estilo de las líneas dibujadas sobre una superficie gráfica. Usando un lápiz azul delgado, dibujamos un rectángulo cuyas dimensiones se expresan en pulgadas, haciendo el código más legible para diseños orientados a la impresión.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Paso 7: guardar bitmap como png

Finalmente, escribe el bitmap a un archivo PNG en la carpeta que especificaste antes. Guardar como PNG preserva la calidad sin pérdidas y es ampliamente compatible en todas las plataformas.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## ¿Cómo escalar gráficos para una impresora?

Establece el DPI del bitmap a la resolución de la impresora objetivo (por ejemplo, 300 DPI) antes de dibujar. Esto escala automáticamente la salida **scale graphics printer** para que una pulgada en tu código equivalga a una pulgada en la página impresa, mientras que el tamaño lógico del rectángulo permanece sin cambios. Después de llamar a `bitmap.SetResolution(300, 300)`, el mismo rectángulo aparecerá más grande en papel pero mantendrá sus dimensiones exactas.

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **Archivo de salida no creado** | Ruta incorrecta o carpeta inexistente | Asegúrate de que el directorio de destino exista o llama a `Directory.CreateDirectory` antes de guardar. |
| **El rectángulo aparece distorsionado** | `PageUnit` o DPI incongruentes | Verifica que `graphics.PageUnit` coincida con la unidad deseada y que el DPI del bitmap esté configurado apropiadamente (96 DPI por defecto, 300 DPI para impresión). |
| **Excepción de licencia** | Ejecutándose sin una licencia válida en producción | Aplica tu licencia temporal o permanente de Aspose.Drawing antes de crear objetos gráficos. |

## Preguntas frecuentes

**Q:** ¿Puedo usar Aspose.Drawing de forma gratuita?  
**A:** Sí, una prueba gratuita está disponible [here](https://releases.aspose.com/).

**Q:** ¿Dónde puedo encontrar la documentación detallada de Aspose.Drawing?  
**A:** La referencia completa de la API se encuentra [here](https://reference.aspose.com/drawing/net/).

**Q:** ¿Cómo obtengo soporte para Aspose.Drawing?  
**A:** Visita el [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) para ayuda de la comunidad y asistencia oficial.

**Q:** ¿Hay una licencia temporal disponible para Aspose.Drawing?  
**A:** Por supuesto—obtén una [here](https://purchase.aspose.com/temporary-license/).

**Q:** ¿Dónde puedo comprar una licencia completa de Aspose.Drawing?  
**A:** Puedes comprarla [here](https://purchase.aspose.com/buy).

## Conclusión

Ahora sabes **cómo dibujar un rectángulo** gráfico con transformación a nivel de página usando Aspose.Drawing para .NET. Al establecer la unidad de página en pulgadas, limpiar el fondo del lienzo y guardar el resultado como PNG, obtienes una salida precisa e independiente del dispositivo, adecuada tanto para la visualización en pantalla como para impresión de alta resolución. Experimenta con otras unidades, rotación o orígenes de coordenadas personalizados para desbloquear escenarios de dibujo aún más potentes.

---

**Última actualización:** 2026-11-04  
**Probado con:** Aspose.Drawing 24.12 for .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Cómo establecer la unidad en Aspose.Drawing para .NET – Unidades de medida](/drawing/net/coordinate-transformations/units-of-measure/)
- [Transformación global](/drawing/net/coordinate-transformations/global-transformation/)
- [Transformación paso a paso – Transformaciones de coordenadas](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}