---
date: 2025-12-06
description: Aprenda a guardar archivos de imagen PNG mientras enumera las fuentes
  instaladas, muestra familias de fuentes, crea gráficos a partir de mapas de bits
  y dibuja texto con fuentes usando Aspose.Drawing para .NET.
language: es
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Guardar imagen PNG y trabajar con fuentes instaladas en Aspose.Drawing
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar imagen PNG y trabajar con fuentes instaladas en Aspose.Drawing

## Introducción

Si necesitas **guardar archivos de imagen PNG** que también muestren información sobre las fuentes instaladas en una máquina, Aspose.Drawing para .NET te ofrece una forma limpia y multiplataforma de hacerlo. En este tutorial recorreremos cómo enumerar fuentes instaladas, mostrar familias de fuentes, crear gráficos a partir de un bitmap y dibujar texto con fuentes, todo mientras finalmente guardamos el resultado como una imagen PNG. Al final tendrás un fragmento reutilizable que podrás insertar en cualquier proyecto .NET.

## Respuestas rápidas
- **¿Qué crea este tutorial?** Una imagen PNG que enumera las familias de fuentes instaladas.  
- **¿Qué biblioteca se requiere?** Aspose.Drawing para .NET (no se necesita System.Drawing.Common).  
- **¿Puedo usar fuentes personalizadas?** Sí, solo cárgalas en una `InstalledFontCollection`.  
- **¿Se puede ajustar la resolución de salida?** Por supuesto, cambia el tamaño del bitmap o el formato de píxel.  
- **¿Necesito una licencia para ejecutar el código?** Una licencia temporal funciona para evaluación; se requiere una licencia completa para producción.

## ¿Qué significa “guardar imagen PNG” en el contexto de Aspose.Drawing?
Guardar una imagen PNG implica renderizar tu superficie de dibujo (un `Bitmap`) a un archivo con la extensión `.png`. Aspose.Drawing se encarga de la codificación, por lo que solo necesitas llamar a `bitmap.Save(...)` con la ruta deseada.

## ¿Por qué enumerar fuentes instaladas y mostrar familias de fuentes?
Saber qué fuentes están disponibles te permite crear gráficos dinámicos que se adapten al entorno del usuario final. Es especialmente útil para generar informes, certificados o cualquier contenido visual que deba coincidir con la identidad corporativa sin distribuir archivos de fuentes.

## Requisitos previos

- **Biblioteca Aspose.Drawing** – descarga la última versión desde la [página de descarga de Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider o cualquier editor compatible con .NET.  
- **Conocimientos básicos de C#** – deberías estar cómodo con clases, objetos y bucles simples.

## Importar espacios de nombres
Para trabajar con fuentes y gráficos, importa estos espacios de nombres al inicio de tu archivo C#:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Guía paso a paso

### Paso 1: Crear un bitmap (el lienzo)
Primero, creamos un bitmap que contendrá la imagen final. El tamaño del bitmap y el formato de píxel determinan la calidad del PNG guardado.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Paso 2: Crear gráficos a partir del bitmap
A continuación, obtenemos un objeto `Graphics` del bitmap. Este objeto nos permite dibujar formas, texto e imágenes sobre el lienzo.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Paso 3: Configurar pincel y fuente (dibujar texto con fuentes)
Necesitamos un pincel para el color del texto y un objeto `Font` que defina el tipo de letra, tamaño y estilo.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Paso 4: Enumerar fuentes instaladas y mostrar familias de fuentes
Ahora mostramos el número de familias de fuentes y los primeros nombres directamente en el bitmap. Esto demuestra las capacidades de **enumerar fuentes instaladas** y **mostrar familias de fuentes**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Paso 5: Guardar imagen PNG
Finalmente, escribimos el bitmap en disco como un archivo PNG. Esta es la operación central de **guardar imagen PNG**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Consejo profesional:** Usa `Path.Combine` para construir rutas de archivo y evitar problemas con los separadores de directorio en diferentes sistemas operativos.

## Problemas comunes y soluciones
| Problema | Causa | Solución |
|----------|-------|----------|
| **No se muestran fuentes** | `InstalledFontCollection` no se pobló (p. ej., se ejecuta en un servidor sin cabeza sin fuentes). | Instala las fuentes necesarias en el servidor o incrusta fuentes personalizadas en tu aplicación. |
| **El archivo guardado está corrupto** | Formato de píxel incorrecto o permisos de escritura insuficientes. | Asegúrate de que la carpeta de destino exista y la aplicación tenga acceso de escritura; mantén `Format32bppPArgb`. |
| **El texto se ve borroso** | Configuración de DPI baja. | Incrementa las dimensiones del bitmap o establece `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Preguntas frecuentes

**P: ¿Puedo usar fuentes personalizadas que no estén instaladas en la máquina?**  
R: Sí. Carga el archivo de fuente en una `PrivateFontCollection` y crea un `Font` a partir de esa colección.

**P: ¿Cómo manejo excepciones relacionadas con fuentes?**  
R: Envuelve la creación de fuentes en un bloque `try/catch` y examina `ArgumentException` para detectar familias faltantes.

**P: ¿Es Aspose.Drawing adecuado para aplicaciones web?**  
R: Absolutamente. La biblioteca funciona en ASP.NET Core, Azure Functions y otros entornos del lado del servidor.

**P: ¿Puedo cambiar el color o estilo del texto?**  
R: Sí. Usa diferentes tipos de `Brush` (p. ej., `LinearGradientBrush`) y modifica el enumerado `FontStyle`.

**P: ¿Dónde puedo obtener una licencia temporal para pruebas?**  
R: Descarga una licencia de prueba desde la [página de licencia temporal de Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusión

Al seguir estos pasos has aprendido cómo **guardar archivos de imagen PNG** que enumeren dinámicamente **fuentes instaladas**, **muestren familias de fuentes**, **creen gráficos a partir de un bitmap** y **dibujen texto con fuentes** usando Aspose.Drawing para .NET. Siéntete libre de experimentar con otras fuentes, colores y tamaños de bitmap para adaptarlos a los requisitos visuales de tu proyecto.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2025-12-06  
**Probado con:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose