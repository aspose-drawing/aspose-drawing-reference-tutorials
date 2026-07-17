---
date: 2026-03-02
description: ¡Mejora las ilustraciones de tus documentos con Aspose.Drawing para .NET!
  Aprende paso a paso cómo añadir anotaciones para obtener visuales más claros e informativos.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Cómo agregar cuadros de texto con Aspose.Drawing para .NET
url: /es/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Creando callouts en Aspose.Drawing

## Introducción
Si te preguntas **cómo agregar callouts** a tus imágenes o diagramas usando Aspose.Drawing para .NET, has llegado al lugar correcto. En este tutorial recorreremos todo el proceso—from cargar una imagen hasta dibujar callouts con estilo elegante—para que puedas hacer tus ilustraciones más claras e informativas.

## Respuestas rápidas
- **¿Qué biblioteca necesito?** Aspose.Drawing para .NET (descargable desde el sitio oficial).  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para un callout básico.  
- **¿Puedo personalizar colores y fuentes?** Sí—todo se controla mediante objetos estándar de GDI+ (Pen, Font, Brush).

## Cómo agregar callouts en Aspose.Drawing
A continuación tienes una guía concisa, paso a paso, que muestra exactamente **cómo agregar callouts** a una imagen. Siéntete libre de copiar el código, experimentar con las posiciones y adaptar el estilo para que coincida con tu marca.

## Requisitos previos
Antes de comenzar, asegúrate de tener:

- Conocimientos básicos del lenguaje de programación C#.  
- Biblioteca Aspose.Drawing instalada. Puedes descargarla [aquí](https://releases.aspose.com/drawing/net/).  
- Un documento o imagen donde deseas agregar callouts.

## Importar espacios de nombres
Asegúrate de que los espacios de nombres necesarios estén incluidos en tu proyecto:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Paso 1: Cargar la imagen
Comienza cargando la imagen donde deseas agregar callouts. Reemplaza `"Your Document Directory"` y `"gears.png"` con tu directorio real y el nombre de archivo de la imagen.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Paso 2: Crear objeto Graphics
Crea un objeto `Graphics` a partir de la imagen para realizar operaciones de dibujo.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Paso 3: Definir posiciones de los callouts
Define los puntos de inicio y fin para cada callout junto con el valor y la unidad del callout.

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

## Paso 4: Dibujar callouts
Implementa el método `DrawCallOut` para dibujar callouts en la imagen.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Paso 5: Guardar la imagen
Guarda la imagen con callouts en el directorio que desees.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Código fuente del callout
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

## Problemas comunes y consejos
- **Coordenadas de anclaje incorrectas** – asegúrate de que los puntos de inicio y fin estén dentro de los límites de la imagen; de lo contrario el callout podría recortarse.  
- **Superposición de texto** – ajusta `spaceSize` o el tamaño de la fuente si la etiqueta colisiona con otros gráficos.  
- **Rendimiento** – para imágenes muy grandes, considera disponer de los objetos `Pen`, `Font` y `Brush` después de usarlos para liberar recursos.

## Conclusión
¡Felicidades! Ahora sabes **cómo agregar callouts** a una imagen usando Aspose.Drawing para .NET. Siéntete libre de experimentar con diferentes posiciones, colores y fuentes para que coincidan con tu estilo visual.

## Preguntas frecuentes

### ¿Puedo usar Aspose.Drawing para otros tipos de ilustraciones?
Sí, Aspose.Drawing admite una amplia gama de operaciones de dibujo para varios tipos de ilustraciones.

### ¿Aspose.Drawing es compatible con diferentes formatos de imagen?
¡Absolutamente! Aspose.Drawing soporta formatos de imagen populares como PNG, JPEG, GIF y más.

### ¿Dónde puedo encontrar más ejemplos y documentación?
Explora la documentación completa [aquí](https://reference.aspose.com/drawing/net/).

### ¿Cómo obtengo soporte si encuentro problemas?
Visita el [foro de Aspose.Drawing](https://forum.aspose.com/c/drawing/44) para soporte de la comunidad.

### ¿Puedo probar Aspose.Drawing antes de comprar?
¡Claro! Comienza con una prueba gratuita [aquí](https://releases.aspose.com/).

**Preguntas y respuestas adicionales**

**Q: ¿Puedo cambiar el estilo de línea del callout (rayado, punteado)?**  
**A:** Sí—simplemente configura la propiedad `Pen.DashStyle` antes de dibujar la línea.

**Q: ¿Es posible agregar un color de fondo a la etiqueta del callout?**  
**A:** Absolutamente. Crea un `SolidBrush` con el color deseado y rellena un rectángulo detrás del texto antes de llamar a `DrawString`.

**Q: ¿Cómo aseguro que el callout se vea igual en pantallas de alta DPI?**  
**A:** Establece `graphics.PageUnit = GraphicsUnit.Pixel` (como se muestra) y usa medidas basadas en vectores para mantener la escala consistente.

---

**Última actualización:** 2026-03-02  
**Probado con:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}