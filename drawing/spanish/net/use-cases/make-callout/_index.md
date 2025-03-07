---
title: Realizar llamadas en Aspose.Drawing
linktitle: Realizar llamadas en Aspose.Drawing
second_title: Aspose.Drawing .NET API alternativa a System.Drawing.Common
description: ¡Mejore las ilustraciones de sus documentos usando Aspose.Drawing para .NET! Aprenda paso a paso cómo agregar leyendas para obtener imágenes más claras e informativas.
weight: 10
url: /es/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Realizar llamadas en Aspose.Drawing

## Introducción
¡Bienvenido a nuestra guía paso a paso sobre cómo realizar llamadas en Aspose.Drawing para .NET! Si buscas mejorar las ilustraciones de tus documentos con leyendas, estás en el lugar correcto. En este tutorial, dividiremos el proceso en pasos manejables utilizando la biblioteca Aspose.Drawing.
## Requisitos previos
Antes de sumergirse en el tutorial, asegúrese de tener los siguientes requisitos previos:
- Conocimientos básicos del lenguaje de programación C#.
-  Biblioteca Aspose.Drawing instalada. Puedes descargarlo[aquí](https://releases.aspose.com/drawing/net/).
- Un documento o imagen donde desea agregar leyendas.
## Importar espacios de nombres
Asegúrese de tener los espacios de nombres necesarios incluidos en su proyecto:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Paso 1: cargue la imagen
 Comience cargando la imagen donde desea agregar leyendas. Reemplazar`"Your Document Directory"` y`"gears.png"` con su directorio real y nombre de archivo de imagen.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Tu código aquí
}
```
## Paso 2: crear un objeto gráfico
 Crear un`Graphics` objeto de la imagen para realizar operaciones de dibujo.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Paso 3: definir posiciones de llamadas
Defina los puntos inicial y final de cada llamada junto con el valor y la unidad de la llamada.
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
## Paso 4: Dibujar notas
 Implementar el`DrawCallOut` Método para dibujar llamadas en la imagen.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Paso 5: guarde la imagen
Guarde la imagen con leyendas en el directorio que desee.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Dibujar código fuente de llamada
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
## Conclusión

¡Felicidades! Ha agregado exitosamente llamadas a su imagen usando Aspose.Drawing para .NET. Siéntete libre de experimentar con diferentes posiciones y valores para personalizar aún más tus textos destacados.

## Preguntas frecuentes

### ¿Puedo utilizar Aspose.Drawing para otro tipo de ilustraciones?

Sí, Aspose.Drawing admite una amplia gama de operaciones de dibujo para varios tipos de ilustraciones.

### ¿Aspose.Drawing es compatible con diferentes formatos de imagen?

¡Absolutamente! Aspose.Drawing admite formatos de imagen populares como PNG, JPEG, GIF y más.

### ¿Dónde puedo encontrar más ejemplos y documentación?

 Explora la documentación completa[aquí](https://reference.aspose.com/drawing/net/).

### ¿Cómo obtengo soporte si tengo problemas?

 Visita el[Aspose.Foro de dibujo](https://forum.aspose.com/c/diagram/17) para el apoyo de la comunidad.

### ¿Puedo probar Aspose.Drawing antes de comprarlo?

 ¡Ciertamente! Comience con una prueba gratuita[aquí](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
