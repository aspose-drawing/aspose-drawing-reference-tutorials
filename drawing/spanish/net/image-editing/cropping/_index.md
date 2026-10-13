---
date: 2026-10-13
description: Aprenda cómo recortar imágenes en lote a PNG usando la API de Aspose.Drawing,
  la alternativa multiplataforma a System.Drawing para desarrolladores .NET.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: Tutorial de recorte de imágenes – Aspose.Drawing
og_description: Aprenda cómo recortar imágenes en lote a PNG rápidamente usando Aspose.Drawing,
  la alternativa multiplataforma a System.Drawing para desarrolladores .NET. Siga
  instrucciones paso a paso para procesar varios archivos de manera eficiente.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Cómo recortar imágenes en lote a PNG con Aspose.Drawing para .NET
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Cómo recortar imágenes en lote a PNG usando Aspose.Drawing para .NET
url: /es/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo recortar imágenes en lote a PNG usando Aspose.Drawing para .NET

Si necesitas **recortar imagen a PNG** rápida, fiable y a gran escala en un entorno .NET, estás en el lugar correcto. En este tutorial recorreremos los pasos exactos para cargar una imagen, definir el área de recorte y guardar el resultado como un archivo PNG, todo usando Aspose.Drawing, una **alternativa moderna a System.Drawing** que funciona multiplataforma. También verás cómo ampliar el flujo de una sola imagen a una **tubería de recorte por lotes** completa.

## Respuestas rápidas
- **¿Qué biblioteca debo usar?** Aspose.Drawing for .NET (una alternativa completa a System.Drawing.Common)  
- **¿Cuánto tiempo lleva el recorte básico?** Normalmente menos de un segundo para una sola imagen en una CPU moderna  
- **¿Puedo recortar a PNG?** Sí – guarda el bitmap recortado como un archivo PNG (ver Paso 6)  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción  
- **¿Es posible el procesamiento por lotes?** Absolutamente – envuelve los mismos pasos en un bucle para procesar varios archivos en segundos  

## Cómo recortar imágenes en lote a PNG?

Carga cada archivo fuente con `new Bitmap(path)`, crea un `Bitmap` en blanco correspondiente para el área de recorte, dibuja el rectángulo seleccionado usando `Graphics.DrawImage` y finalmente llama a `Save("output.png", ImageFormat.Png)`. Envuelve estas seis líneas dentro de un bucle `foreach` que itera sobre un directorio y tendrás una solución completa de recorte por lotes que procesa decenas de imágenes en segundos.

## Por qué usar Aspose.Drawing para recorte por lotes?

Aspose.Drawing se ejecuta en **Windows, Linux y macOS**, procesa **imágenes de más de 500 píxeles en menos de 0,5 segundos** en una CPU típica de clase servidor, y soporta **más de 50 formatos de imagen** con preservación completa del canal alfa. Debido a que elimina las dependencias nativas de GDI+, puedes desplegar el mismo código en contenedores, Azure App Service o AWS Lambda sin bibliotecas adicionales, lo que lo hace ideal para tuberías de imágenes a gran escala.

## Qué es “recortar imagen a PNG”?

La operación `crop image to PNG` extrae una región rectangular de un bitmap fuente y escribe esa región en un archivo PNG. PNG preserva cualquier canal alfa, ofreciendo compresión sin pérdidas, lo que hace que la imagen resultante sea ideal para miniaturas, íconos, recursos de UI o cualquier situación donde se requieran calidad y transparencia.

## Por qué Aspose.Drawing es una alternativa a System.Drawing?

Aspose.Drawing funciona como un reemplazo directo de System.Drawing al ofrecer compatibilidad total multiplataforma, eliminando la necesidad de bibliotecas nativas GDI+. Soporta una amplia gama de formatos de píxel, brinda manipulación de imágenes de alto rendimiento e incluye funciones avanzadas como el manejo de canales alfa y un amplio soporte de formatos, lo que lo hace adecuado tanto para ediciones simples como para procesamiento por lotes a gran escala.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Biblioteca Aspose.Drawing** integrada en tu proyecto .NET. Puedes descargarla desde la [página de descarga de Aspose.Drawing](https://releases.aspose.com/drawing/net/).  
- Una carpeta que contenga las imágenes fuente que deseas recortar. Reemplaza `"Your Document Directory"` en los fragmentos de código con la ruta real en tu máquina.

## Importar espacios de nombres

El espacio de nombres `System.Drawing` nos brinda acceso a `Bitmap`, `Graphics` y tipos relacionados que Aspose.Drawing amplía.

```csharp
using System.Drawing;
```

## Guía paso a paso

### Paso 1: Crear un lienzo bitmap

`Bitmap` es la representación en memoria de una imagen en Aspose.Drawing, proporcionando acceso a nivel de píxel y control de formato.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Comenzamos con un lienzo en blanco dimensionado para contener el resultado recortado. Ajusta el ancho y la altura para que coincidan con las dimensiones del área que planeas extraer.

### Paso 2: Crear un objeto graphics

`Graphics` es la superficie de dibujo que te permite renderizar formas, texto u otras imágenes sobre un Bitmap.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Un objeto `Graphics` nos permite dibujar sobre el lienzo. El `InterpolationMode` controla cómo se calculan los valores de píxel durante el escalado o la transformación—`NearestNeighbor` funciona bien para bordes nítidos.

### Paso 3: Cargar la imagen a recortar

`Image` (o `Bitmap`) carga el archivo fuente en memoria, listo para su manipulación.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Carga la imagen fuente. Asegúrate de que la ruta apunte a un archivo existente; de lo contrario se lanzará una excepción.

### Paso 4: Definir rectángulos de origen y destino

Los objetos `Rectangle` describen la región de la imagen fuente que se conservará y dónde debe colocarse en el lienzo de destino.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` indica a la API qué parte de la imagen original conservar. Aquí seleccionamos el área de 50 × 40 píxeles en la esquina superior izquierda. Al asignar el mismo rectángulo a `destinationRectangle`, mantenemos la región recortada en su tamaño original.

### Paso 5: Realizar la operación de recorte

`Graphics.DrawImage` copia la porción definida de `image` a nuestro `bitmap` en blanco.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

Esta es la operación central **crop image to PNG**. El método respeta el rectángulo de origen y escribe solo los píxeles seleccionados en el bitmap de destino.

### Paso 6: Guardar la imagen recortada (crop image to PNG)

`Bitmap.Save` escribe el bitmap en memoria a un archivo usando el formato especificado.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Finalmente, escribe el lienzo en disco como un archivo PNG. PNG preserva cualquier canal alfa y brinda calidad sin pérdidas, ideal para recursos de UI.

## Cómo recortar imágenes en lote en un bucle?

Itera sobre cada ruta de archivo con `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, repite los Pasos 1‑6 dentro del bucle y guarda cada resultado en una carpeta de destino. Este patrón escala linealmente, puede paralelizarse con `Parallel.ForEach` para un rendimiento aún más rápido, y procesa imágenes de manera eficiente y rápida.

## Problemas comunes y consejos
- **Desajustes de formato de píxel** – asegúrate de que la imagen fuente y el bitmap del lienzo compartan un formato de píxel compatible para evitar desplazamientos de color.  
- **Liberación de objetos GDI** – envuelve `Bitmap` y `Graphics` en sentencias `using` o llama a `Dispose()` manualmente; de lo contrario podrías filtrar recursos no administrados.  
- **Errores de coordenadas** – las coordenadas de los rectángulos son basadas en cero. Seleccionar un rectángulo que exceda los límites de la imagen fuente generará una excepción.  

## Preguntas frecuentes

**Q: ¿Puedo recortar imágenes de cualquier formato usando Aspose.Drawing?**  
A: Sí, Aspose.Drawing soporta una amplia gama de formatos (PNG, JPEG, BMP, GIF, TIFF, etc.), por lo que puedes recortar prácticamente cualquier tipo de imagen.

**Q: ¿Hay opciones avanzadas de recorte disponibles?**  
A: Absolutamente. Puedes combinar `GraphicsPath`, transformaciones `Matrix`, o usar la clase `ImageProcessor` para selecciones más complejas como recortes circulares.

**Q: ¿Puedo aplicar múltiples operaciones de recorte a una sola imagen?**  
A: Sí. Después del primer recorte, puedes reutilizar el bitmap resultante como la nueva fuente y repetir el proceso para encadenar varios recortes.

**Q: ¿Es Aspose.Drawing adecuado para el procesamiento por lotes de imágenes?**  
A: De hecho. Su API ligera y la ausencia de dependencias nativas lo hacen perfecto para procesar grandes colecciones de imágenes en servidores.

**Q: ¿Cómo puedo obtener soporte para consultas relacionadas con Aspose.Drawing?**  
A: Dirígete al [Foro de Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para buscar asistencia y conectar con la comunidad.

**Última actualización:** 2026-10-13  
**Probado con:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Cargar, convertir BMP a PNG y otros formatos con Aspose.Drawing](/drawing/net/image-editing/load-save/)
- [Cómo licenciar Aspose.Drawing para .NET – cómo licenciar aspose.drawing](/drawing/net/licensing/)
- [Cómo dibujar rectángulo – Transformación del sistema de coordenadas (Transformación de página) usando la API Aspose.Drawing para .NET](/drawing/net/coordinate-transformations/page-transformation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}