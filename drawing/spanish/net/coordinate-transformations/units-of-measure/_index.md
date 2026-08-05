---
date: 2026-05-24
description: Aprenda cómo establecer la unidad en Aspose.Drawing para .NET, convierta
  unidades gráficas fácilmente y domine mediciones precisas para la renderización
  de gráficos.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Unidades de medida en Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cómo establecer la unidad en Aspose.Drawing para .NET – Unidades de medida
url: /es/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo establecer la unidad en Aspose.Drawing para .NET – Unidades de medida

## Introducción

Bienvenido al mundo de Aspose.Drawing para .NET, donde la precisión y la flexibilidad se encuentran en la manipulación gráfica. En este tutorial descubrirá **cómo establecer la unidad** para sus dibujos, aprenderá a **convertir unidades gráficas** entre puntos, milímetros y pulgadas, y verá ejemplos del mundo real que hacen que sus imágenes sean perfectas píxel a píxel. Ya sea que esté creando informes, miniaturas o gráficos personalizados, dominar las unidades de medida es esencial para una renderización coherente en todos los dispositivos.

## Respuestas rápidas
- **¿Cuál es la forma principal de cambiar unidades?** Llame a `graphics.PageUnit = PageUnit.Point` (o `.Millimeter`, `.Inch`) en el objeto `Graphics`.  
- **¿Qué unidad equivale a 1/72 de pulgada?** Puntos.  
- **¿Cuántos milímetros hay en una pulgada?** 25.4 mm = 1 inch.  
- **¿Necesito bibliotecas adicionales para usar unidades?** No, la biblioteca central de Aspose.Drawing proporciona todas las constantes de unidad.  
- **¿Puedo mezclar unidades en una sola imagen?** Establezca la unidad una vez por instancia de `Graphics`; dibuje todo usando esa unidad para mantener la consistencia.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de que tenga los siguientes requisitos previos:

- Aspose.Drawing para .NET: Asegúrese de que tenga la biblioteca instalada. Puede descargarla [aquí](https://releases.aspose.com/drawing/net/).
- Directorio de documentos: Tenga un directorio designado donde desee guardar sus documentos creados.
- Conocimientos básicos de C#: Se recomienda una comprensión fundamental de C# para aprovechar al máximo esta guía.

## Importar espacios de nombres

Antes de comenzar, importemos los espacios de nombres necesarios para usar Aspose.Drawing de manera eficaz:

```csharp
using System.Drawing;
```

Ahora, desglosaremos cada ejemplo en varios pasos:

## Cómo establecer la unidad en puntos?

La clase `Bitmap` representa una imagen en memoria que sirve como lienzo de dibujo. Cargue su bitmap, cree un objeto `Graphics` y establezca la unidad de página en puntos — esto indica a Aspose.Drawing que interprete todas las coordenadas como valores de 1/72 pulgada. Usar puntos le brinda un control fino para gráficos listos para imprimir y le permite especificar anchos de línea con alta precisión.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Paso 1: Crear un Bitmap  
La clase `Bitmap` representa una imagen en memoria que sirve como lienzo de dibujo.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Paso 2: Crear un objeto Graphics  
`Graphics` proporciona métodos de dibujo para renderizar formas y texto sobre un `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Paso 3: Establecer la unidad de página en puntos  
`PageUnit` es una enumeración que especifica la unidad de medida para las coordenadas de la página. `PageUnit.Point` define los puntos como la unidad de medida (1 punto = 1/72 pulgada). Esta configuración se aplica a todas las llamadas de dibujo posteriores.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Paso 4: Dibujar un rectángulo en puntos  
Cuando dibuja un rectángulo después de establecer la unidad, las dimensiones que especifica se interpretan como puntos, garantizando un tamaño preciso.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Cómo establecer la unidad en milímetros?

`PageUnit` es una enumeración que especifica la unidad de medida para las coordenadas de la página. Cambiar a milímetros es útil cuando necesita dimensiones métricas, por ejemplo al generar diagramas de ingeniería. Aspose.Drawing trata 1 mm como 1/25.4 pulgada, lo que le permite alinear los gráficos con medidas físicas usadas en la fabricación y documentación técnica.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Paso 1: Establecer la unidad de página en milímetros  
Asigne `PageUnit.Millimeter` al objeto `Graphics`; todas las coordenadas ahora se mapean al sistema métrico.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Paso 2: Dibujar un rectángulo en milímetros  
El ancho y la altura del rectángulo ahora se expresan en milímetros, lo que facilita la alineación con medidas físicas y asegura que la salida impresa coincida con tamaños del mundo real.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Cómo establecer la unidad en pulgadas?

`Graphics` proporciona métodos de dibujo para renderizar formas y texto sobre un `Bitmap`. Las pulgadas son la unidad predeterminada para muchas herramientas de diseño basadas en EE. UU. Establecer la unidad en pulgadas le permite pensar en términos familiares al diseñar elementos de UI, y simplifica la transición del diseño de pantalla a la impresión donde las pulgadas se usan comúnmente.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Paso 1: Establecer la unidad de página en pulgadas  
`PageUnit.Inch` cambia el sistema de coordenadas de modo que 1 unidad equivale a 1 pulgada, proporcionando una forma sencilla de dimensionar elementos para diseños orientados a la impresión.

CODE_BLOCK_PLACEHOLDER_10_END

### Paso 2: Dibujar un rectángulo en pulgadas  
Ahora cualquier forma que dibuje usa pulgadas como base de medida, lo cual es ideal para diseños de impresión y para comunicar dimensiones a los interesados acostumbrados a unidades imperiales.

CODE_BLOCK_PLACEHOLDER_11_END

## Guardar el resultado

Después de completar los ejemplos, guarde la imagen resultante en su directorio de documentos. El método `Bitmap.Save` escribe el archivo en el formato que especifique (PNG, JPEG, etc.).

CODE_BLOCK_PLACEHOLDER_12_END

Ahora, ha navegado con éxito las diversas unidades de medida en Aspose.Drawing para .NET, creando una representación visual de rectángulos usando puntos, milímetros y pulgadas.

## ¿Por qué usar el sistema de unidades de Aspose.Drawing?

Aspose.Drawing soporta **más de 30 formatos de imagen** y puede procesar imágenes de hasta **5000 × 5000 píxeles** sin cargar todo el archivo en memoria, ofreciendo alto rendimiento para la generación de gráficos a gran escala. Al establecer explícitamente la unidad, elimina la conjetura, reduce los errores de conversión y asegura que su salida coincida con dimensiones físicas exactas en todas las plataformas.

## Problemas comunes y soluciones

- **Tamaño inesperado después de guardar** – Verifique que haya establecido `graphics.PageUnit` **antes** de cualquier llamada de dibujo; cambiar la unidad después no redimensiona retroactivamente las formas existentes.  
- **Salida borrosa en pantallas de alta DPI** – Aumente la resolución del bitmap (p.ej., `new Bitmap(width, height, 300)`) para que coincida con la DPI objetivo.  
- **Unidades mixtas en una imagen** – Cree instancias separadas de `Graphics` para cada unidad o realice conversiones manuales antes de dibujar.

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.Drawing para .NET con otros frameworks .NET?
A1: Sí, Aspose.Drawing es compatible con varios frameworks .NET, proporcionando flexibilidad en su entorno de desarrollo.

### Q2: ¿Hay una prueba gratuita disponible?
A2: Sí, puede explorar Aspose.Drawing con una prueba gratuita [aquí](https://releases.aspose.com/).

### Q3: ¿Cómo obtengo soporte para Aspose.Drawing para .NET?
A3: Visite el [Foro de Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para soporte comunitario y discusiones.

### Q4: ¿Puedo adquirir una licencia temporal para proyectos a corto plazo?
A4: Sí, puede obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### Q5: ¿Dónde puedo encontrar documentación detallada de Aspose.Drawing?
A5: La documentación completa está disponible [aquí](https://reference.aspose.com/drawing/net/).

---

**Última actualización:** 2026-05-24  
**Probado con:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
