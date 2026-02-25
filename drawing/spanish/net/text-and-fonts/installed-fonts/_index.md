---
date: 2026-02-25
description: Aprende a crear gráficos bitmap en C# y guardar imágenes PNG mientras
  enumeras las fuentes instaladas, dibujas texto con fuentes y ajustas la resolución
  del bitmap usando Aspose.Drawing para .NET.
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Crear gráficos bitmap en C# – Guardar imagen PNG y trabajar con fuentes instaladas
  en Aspose.Drawing
url: /es/net/text-and-fonts/installed-fonts/
weight: 13
---

 answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar imagen PNG y trabajar con fuentes instaladas en Aspose.Drawing

## Introducción

Si necesita **save PNG image** archivos mientras también **create bitmap graphics C#**, Aspose.Drawing para .NET le ofrece una forma limpia y multiplataforma de hacerlo. En este tutorial recorreremos la lista de fuentes instaladas, mostraremos familias de fuentes, crearemos gráficos a partir de un bitmap y dibujaremos texto con fuentes, todo mientras finalmente guardamos el resultado como una imagen PNG. Al final tendrá un fragmento reutilizable que puede insertar en cualquier proyecto .NET.

## Respuestas rápidas
- **¿Qué crea este tutorial?** Una imagen PNG que enumera las familias de fuentes instaladas.  
- **¿Qué biblioteca se requiere?** Aspose.Drawing para .NET (no se necesita System.Drawing.Common).  
- **¿Puedo usar fuentes personalizadas?** Sí, solo cárguelas en un `InstalledFontCollection`.  
- **¿Es ajustable la resolución de salida?** Absolutamente – cambie el tamaño del bitmap o el formato de píxel para **adjust bitmap resolution C#**.  
- **¿Necesito una licencia para ejecutar el código?** Una licencia temporal funciona para evaluación; se requiere una licencia completa para producción.

## ¿Qué es “save PNG image” en el contexto de Aspose.Drawing?
Guardar una imagen PNG significa renderizar su superficie de dibujo (un `Bitmap`) a un archivo con la extensión `.png`. Aspose.Drawing se encarga de la codificación por usted, por lo que solo necesita llamar a `bitmap.Save(...)` con la ruta deseada.

## ¿Por qué listar fuentes instaladas y mostrar familias de fuentes?
Conocer qué fuentes están disponibles le permite crear gráficos dinámicos que se adapten al entorno del usuario final. Es especialmente útil para generar informes, certificados o cualquier contenido visual que deba coincidir con la identidad corporativa sin distribuir archivos de fuentes.

## ¿Cómo crear bitmap graphics C# con Aspose.Drawing?
A continuación se muestra una guía práctica paso a paso que explica exactamente cómo **create bitmap graphics C#**, dibujar texto con fuentes y ajustar la resolución del bitmap si es necesario.

## Requisitos previos

- **Biblioteca Aspose.Drawing** – descargue la última versión desde la [página de descarga de Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider o cualquier editor compatible con .NET.  
- **Conocimientos básicos de C#** – debe sentirse cómodo con clases, objetos y bucles simples.

## Importar espacios de nombres
Para trabajar con fuentes y gráficos, importe estos espacios de nombres al inicio de su archivo C#:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Guía paso a paso

### Paso 1: Crear un bitmap (el lienzo)
Primero, creamos un bitmap que contendrá la imagen final. El tamaño del bitmap y el formato de píxel determinan la calidad del PNG guardado y le permiten **adjust bitmap resolution C#**.

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

### Paso 3: Configurar pincel y fuente (draw text with fonts)
Necesitamos un pincel para el color del texto y un objeto `Font` que define el tipo de letra, tamaño y estilo. Aquí es donde **draw text with fonts**.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Paso 4: Listar fuentes instaladas y mostrar familias de fuentes
Ahora mostramos el número de familias de fuentes y los primeros nombres directamente en el bitmap. Esto demuestra las capacidades de **list installed fonts** y **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Paso 5: Guardar imagen PNG
Finalmente, escribimos el bitmap en disco como un archivo PNG. Esta es la operación central de **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Consejo profesional:** Use `Path.Combine` para construir rutas de archivo y evitar problemas con los separadores de directorios en diferentes sistemas operativos.

## Problemas comunes y soluciones
| Problema | Causa | Solución |
|----------|-------|----------|
| **No se muestran fuentes** | `InstalledFontCollection` no está poblado (p.ej., ejecutándose en un servidor sin cabeza sin fuentes). | Instale las fuentes requeridas en el servidor o incruste fuentes personalizadas en su aplicación. |
| **El archivo guardado está corrupto** | Formato de píxel incorrecto o permisos de escritura faltantes. | Asegúrese de que la carpeta de destino exista y la aplicación tenga acceso de escritura; mantenga `Format32bppPArgb`. |
| **El texto se ve borroso** | Configuración de DPI baja. | Aumente las dimensiones del bitmap o establezca `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Preguntas frecuentes

**Q: ¿Puedo usar fuentes personalizadas que no están instaladas en la máquina?**  
A: Sí. Cargue el archivo de fuente en una `PrivateFontCollection` y cree una `Font` a partir de esa colección.

**Q: ¿Cómo manejo excepciones relacionadas con fuentes?**  
A: Envuelva la creación de fuentes en un bloque `try/catch` y examine `ArgumentException` para familias faltantes.

**Q: ¿Es Aspose.Drawing adecuado para aplicaciones web?**  
A: Absolutamente. La biblioteca funciona en ASP.NET Core, Azure Functions y otros entornos del lado del servidor.

**Q: ¿Puedo cambiar el color o estilo del texto?**  
A: Sí. Use diferentes tipos de `Brush` (p.ej., `LinearGradientBrush`) y modifique el enum `FontStyle`.

**Q: ¿Dónde puedo obtener una licencia temporal para pruebas?**  
A: Descargue una licencia de prueba desde la [página de licencia temporal de Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusión

Al seguir estos pasos ha aprendido cómo **save PNG image** archivos que listan dinámicamente **installed fonts**, **show font families**, **create graphics from bitmap** y **draw text with fonts** usando Aspose.Drawing para .NET. Ahora sabe cómo **create bitmap graphics C#**, ajustar la resolución del bitmap e incorporar fuentes personalizadas cuando sea necesario. Siéntase libre de experimentar con otras fuentes, colores y tamaños de bitmap para adaptarse a los requisitos visuales de su proyecto.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2026-02-25  
**Probado con:** Aspose.Drawing 24.11 para .NET  
**Autor:** Aspose