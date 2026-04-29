---
date: 2026-02-07
description: Tutorial paso a paso para recortar una imagen a PNG usando Aspose.Drawing,
  la alternativa a System.Drawing para desarrolladores .NET. Incluye recorte por lotes
  y técnicas esenciales.
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Cómo recortar una imagen a PNG con Aspose.Drawing para .NET
url: /es/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo recortar una imagen a PNG con Aspose.Drawing para .NET

Si necesitas **recortar una imagen a PNG** de forma rápida y fiable en un entorno .NET, estás en el lugar correcto. En este tutorial recorreremos paso a paso los pasos exactos para cargar una imagen, definir el área de recorte y guardar el resultado como archivo PNG, todo usando Aspose.Drawing, una **alternativa moderna a System.Drawing** que funciona multiplataforma.

## Respuestas rápidas
- **¿Qué biblioteca debo usar?** Aspose.Drawing para .NET (una alternativa completa a System.Drawing.Common)  
- **¿Cuánto tiempo lleva el recorte básico?** Normalmente menos de un segundo para una sola imagen en una CPU moderna  
- **¿Puedo recortar a PNG?** Sí – guarda el bitmap recortado como archivo PNG (ver Paso 6)  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción  
- **¿Es posible el procesamiento por lotes?** Absolutamente – envuelve los mismos pasos en un bucle para procesar varios archivos  

## ¿Qué es “recortar imagen a PNG”?

Recortar una imagen significa extraer una región rectangular del bitmap original. Cuando guardas esa región como PNG, preservas la transparencia y obtienes compresión sin pérdidas, ideal para miniaturas, íconos o cualquier recurso de UI.

## ¿Por qué Aspose.Drawing es una alternativa a System.Drawing?

- **Compatibilidad multiplataforma** – funciona en Windows, Linux y macOS sin dependencias nativas de GDI+.  
- **Manejo rico de formatos de píxel** – 32‑bit, 24‑bit, indexado y más.  
- **API enfocada en rendimiento** – ideal tanto para ediciones de una sola imagen como para trabajos por lotes a gran escala.  

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Biblioteca Aspose.Drawing** integrada en tu proyecto .NET. Puedes descargarla [here](https://releases.aspose.com/drawing/net/).  
- Una carpeta que contenga las imágenes fuente que deseas recortar. Reemplaza `"Your Document Directory"` en los fragmentos de código con la ruta real en tu máquina.

## Importar espacios de nombres

```csharp
using System.Drawing;
```

El espacio de nombres `System.Drawing` nos brinda acceso a `Bitmap`, `Graphics` y tipos relacionados que Aspose.Drawing amplía.

## Guía paso a paso

### Paso 1: Crear un lienzo Bitmap

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Comenzamos con un lienzo en blanco dimensionado para contener el resultado recortado. Ajusta el ancho y la altura para que coincidan con las dimensiones del área que planeas extraer.

### Paso 2: Crear un objeto Graphics

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Un objeto `Graphics` nos permite dibujar sobre el lienzo. La propiedad `InterpolationMode` controla cómo se calculan los valores de píxel durante el escalado o la transformación—`NearestNeighbor` funciona bien para bordes nítidos.

### Paso 3: Cargar la imagen a recortar

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Carga la imagen fuente. Asegúrate de que la ruta apunte a un archivo existente; de lo contrario se lanzará una excepción.

### Paso 4: Definir rectángulos de origen y destino

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

El `sourceRectangle` indica a la API qué parte de la imagen original conservar. Aquí seleccionamos el área de 50 × 40 píxeles en la esquina superior izquierda. Al asignar el mismo rectángulo a `destinationRectangle`, mantenemos la región recortada con su tamaño original.

### Paso 5: Ejecutar la operación de recorte

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` copia la porción definida de `image` a nuestro `bitmap` en blanco. Esta es la operación central de **recortar imagen a PNG**.

### Paso 6: Guardar la imagen recortada (Recortar imagen a PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Finalmente, escribe el lienzo en disco como archivo PNG. PNG preserva cualquier canal alfa y ofrece calidad sin pérdidas—ideal para recursos de UI.

## Cómo recortar imágenes en un escenario por lotes

Cuando tienes decenas o cientos de imágenes, simplemente coloca todo el fragmento dentro de un bucle `foreach` que itere sobre una colección de rutas de archivo. La misma lógica de `Graphics.DrawImage` se aplica, convirtiendo el **recorte de imágenes por lotes** en una extensión trivial de este tutorial.

## Problemas comunes y consejos

- **Desajustes de formato de píxel** – asegura que la imagen fuente y el bitmap del lienzo compartan un formato de píxel compatible para evitar cambios de color.  
- **Liberación de objetos GDI** – envuelve `Bitmap` y `Graphics` en sentencias `using` o llama a `Dispose()` manualmente; de lo contrario podrías filtrar recursos no administrados.  
- **Errores de coordenadas** – las coordenadas del rectángulo son base cero. Seleccionar un rectángulo que exceda los límites de la imagen fuente generará una excepción.  

## Preguntas frecuentes

**P: ¿Puedo recortar imágenes de cualquier formato usando Aspose.Drawing?**  
R: Sí, Aspose.Drawing admite una amplia gama de formatos (PNG, JPEG, BMP, GIF, TIFF, etc.), por lo que puedes recortar prácticamente cualquier tipo de imagen.

**P: ¿Existen opciones avanzadas de recorte disponibles?**  
R: Absolutamente. Puedes combinar `GraphicsPath`, transformaciones `Matrix` o usar la clase `ImageProcessor` para selecciones más complejas, como recortes circulares.

**P: ¿Puedo aplicar múltiples operaciones de recorte a una sola imagen?**  
R: Sí. Después del primer recorte, puedes reutilizar el bitmap resultante como nueva fuente y repetir el proceso para encadenar varios recortes.

**P: ¿Es Aspose.Drawing adecuado para el procesamiento de imágenes por lotes?**  
R: De hecho. Su API ligera y la ausencia de dependencias nativas lo hacen perfecto para procesar grandes colecciones de imágenes en servidores.

**P: ¿Cómo puedo obtener soporte para consultas relacionadas con Aspose.Drawing?**  
R: Dirígete al [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) para buscar ayuda y conectar con la comunidad.

---

**Última actualización:** 2026-02-07  
**Probado con:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}