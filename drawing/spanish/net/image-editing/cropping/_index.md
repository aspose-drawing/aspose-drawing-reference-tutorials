---
date: 2025-12-02
description: Aprende a recortar imágenes en .NET con Aspose.Drawing. Este tutorial
  de recorte de imágenes muestra paso a paso cómo guardar la imagen recortada, trabajar
  con bitmap y manejar el recorte de imágenes por lotes.
language: es
linktitle: How to Crop Image .NET Using Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cómo recortar una imagen en .NET usando Aspose.Drawing
url: /net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo recortar una imagen en .NET usando Aspose.Drawing

## Introducción

Si estás desarrollando una aplicación .NET que necesita una manipulación precisa de imágenes, aprender **cómo recortar imágenes** es esencial. Aspose.Drawing ofrece una API rica y totalmente gestionada que te permite **recortar imágenes en .NET** sin depender de la antigua biblioteca System.Drawing.Common. En este tutorial verás un ejemplo completo, de extremo a extremo, que te guía a través de la carga de un bitmap, la definición del área de recorte, la ejecución de la operación y, finalmente, **guardar la imagen recortada**. Al terminar, estarás listo para integrar el recorte de imágenes en cualquier solución .NET—ya sea una sola foto o un flujo de trabajo de **recorte masivo de imágenes**.

## Respuestas rápidas
- **¿Qué biblioteca debo usar?** Aspose.Drawing para .NET  
- **¿Puedo recortar cualquier formato de imagen?** Sí—se admiten la mayoría de los formatos comunes (PNG, JPEG, BMP, etc.).  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia para producción.  
- **¿Es posible el procesamiento por lotes?** Absolutamente—puedes ejecutar el mismo código sobre una colección de archivos.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## ¿Qué es “crop image .net”?

Recortar una imagen significa extraer una región rectangular de una foto más grande. En .NET, esta operación se realiza típicamente sobre un objeto `Bitmap`. Aspose.Drawing simplifica el proceso proporcionando primitivas gráficas de alto rendimiento que funcionan de manera consistente en todas las plataformas.

## ¿Por qué usar Aspose.Drawing para recortar imágenes?

- **Confiabilidad multiplataforma** – Sin dependencias nativas, funciona en Windows, Linux y macOS.  
- **Amplio soporte de formatos de píxel** – Maneja ARGB de 32 bits, PArgb y muchos otros formatos.  
- **Rendimiento optimizado** – Dibujo e interpolación optimizados para imágenes grandes.  
- **Integración sin fisuras** – Funciona junto a otros productos Aspose para PDF, Slides, etc.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Biblioteca Aspose.Drawing** – Añade el paquete NuGet `Aspose.Drawing` a tu proyecto o descárgalo desde el [sitio oficial](https://releases.aspose.com/drawing/net/).  
- **Carpeta de imágenes** – Un directorio que contenga las imágenes de origen que deseas recortar. Reemplaza `"Your Document Directory"` en los fragmentos de código con la ruta real en tu máquina.

## Importar espacios de nombres

Primero, importa el espacio de nombres que contiene las clases de dibujo:

```csharp
using System.Drawing;
```

Esto te brinda acceso a `Bitmap`, `Graphics`, `Rectangle` y otros tipos esenciales.

## Guía paso a paso

### Paso 1: Crear un lienzo Bitmap (crop image bitmap)

Comenzamos creando un bitmap en blanco que contendrá el resultado recortado. Ajusta el ancho, alto y formato de píxel para que coincidan con el tamaño de la región que planeas extraer.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Consejo:** El formato `Format32bppPArgb` conserva la transparencia alfa y ofrece renderizado de alta calidad.

### Paso 2: Crear un objeto Graphics

Un objeto `Graphics` nos permite dibujar sobre el lienzo bitmap. Configurar el `InterpolationMode` influye en cómo se re-muestrea la imagen durante el recorte.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

> **Pro tip:** Para resultados más suaves en imágenes escaladas, considera `InterpolationMode.HighQualityBicubic`.

### Paso 3: Cargar la imagen de origen

Carga la imagen que deseas recortar. La ruta combina tu directorio de documentos con el nombre del archivo.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

> **Nota:** Aspose.Drawing puede leer PNG, JPEG, BMP, GIF, TIFF y muchos otros formatos directamente.

### Paso 4: Definir rectángulos de origen y destino

El `sourceRectangle` selecciona la parte de la imagen original que se conservará. Aquí elegimos el área de 50 × 40 píxeles en la esquina superior izquierda. El `destinationRectangle` indica al motor gráfico dónde colocar la región recortada en el nuevo bitmap.

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

> **¿Por qué ambos rectángulos?** Usar rectángulos idénticos realiza un recorte simple. Puedes cambiar `destinationRectangle` para reposicionar o escalar el fragmento recortado.

### Paso 5: Ejecutar la operación de recorte

El método `DrawImage` copia la región seleccionada de la imagen de origen al bitmap de destino.

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

> **Error común:** Olvidar disponer de `Graphics` puede bloquear el archivo bitmap. Gestionaremos la disposición automáticamente al finalizar el método.

### Paso 6: Guardar la imagen recortada (save cropped image)

Finalmente, escribe el resultado en disco. Cambia el nombre del archivo y la ruta según sea necesario.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

> **Resultado:** Ahora tienes un nuevo archivo PNG que contiene solo la región de 50 × 40 píxeles que especificaste.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| **Archivo de salida en blanco** | Rectángulo de origen fuera de los límites de la imagen | Verifica las coordenadas y el tamaño de `sourceRectangle`. |
| **Excepción de falta de memoria** | Imágenes de origen muy grandes | Procesa las imágenes en fragmentos o usa sentencias `using` para liberar recursos rápidamente. |
| **Colores incorrectos** | Formato de píxel no coincidente | Igualar el formato de píxel del bitmap de origen o convertir usando `Bitmap.Clone`. |

## Preguntas frecuentes

**P: ¿Puedo recortar imágenes de cualquier formato con Aspose.Drawing?**  
R: Sí, Aspose.Drawing admite PNG, JPEG, BMP, GIF, TIFF y muchos otros formatos, por lo que puedes **cómo recortar imágenes** sin importar su tipo original.

**P: ¿Existen opciones avanzadas de recorte?**  
R: Absolutamente. Puedes combinar `GraphicsPath` para recortes no rectangulares, aplicar rotación o usar `ImageAttributes` para ajustes de color.

**P: ¿Puedo aplicar múltiples recortes a una sola imagen?**  
R: Sí—simplemente repite la llamada a `DrawImage` con diferentes rectángulos de origen, o encádnalas en un bucle para transformaciones complejas.

**P: ¿Aspose.Drawing es adecuado para recorte masivo de imágenes?**  
R: Así es. Envuelve los pasos anteriores en un bucle `foreach` sobre una colección de rutas de archivo para procesar decenas o cientos de imágenes automáticamente.

**P: ¿Cómo puedo obtener soporte para consultas relacionadas con Aspose.Drawing?**  
R: Visita el [Foro de Aspose.Drawing](https://forum.aspose.com/c/diagram/17) para hacer preguntas, compartir código y recibir ayuda de la comunidad y los ingenieros del producto.

## Conclusión

En este tutorial demostramos un flujo de trabajo completo de **crop image .net** usando Aspose.Drawing. Ahora sabes **cómo recortar imágenes**, definir rectángulos de origen precisos y **guardar imágenes recortadas**. Con estos fundamentos puedes ampliar el código para manejar **recorte masivo de imágenes**, aplicar transformaciones personalizadas o integrar la lógica en pipelines de procesamiento de imágenes más grandes.

---  

**Última actualización:** 2025-12-02  
**Probado con:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}