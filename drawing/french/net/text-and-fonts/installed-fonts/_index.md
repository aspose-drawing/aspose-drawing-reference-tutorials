---
date: 2026-09-23
description: Apprenez comment enregistrer une image PNG en C# en utilisant Aspose.Drawing,
  lister les installed fonts, dessiner du texte avec des custom fonts, et ajuster
  la bitmap resolution pour des graphiques de haute qualité.
keywords:
- save png image c#
- installed fonts aspnet
- aspose.drawing bitmap graphics
- c# font collection
- png export .net
lastmod: 2026-09-23
linktitle: Enregistrer une image PNG en C# avec Aspose.Drawing et les installed fonts
og_description: Enregistrez une image PNG en C# avec Aspose.Drawing. Ce guide montre
  comment lister les installed fonts, dessiner du texte et contrôler la bitmap resolution
  pour des graphiques professionnels.
og_image_alt: Developer guide showing C# code that creates a bitmap, lists system
  fonts, and saves a PNG file with Aspose.Drawing
og_title: Enregistrer une image PNG en C# avec Aspose.Drawing et les installed fonts
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  headline: Save PNG image in C# with Aspose.Drawing and installed fonts
  type: TechArticle
- description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  name: Save PNG image in C# with Aspose.Drawing and installed fonts
  steps:
  - name: Create a bitmap (the canvas)
    text: '`Bitmap` is the raster image object that holds pixel data for the canvas.'
  - name: Create graphics from bitmap
    text: '`Graphics` is the object that supplies drawing functions such as drawing
      shapes and text onto a bitmap.'
  - name: Set up brush and font (draw text with fonts)
    text: '`Brush` defines how shapes and text are filled with colour, while `Font`
      specifies the typeface, size, and style for text rendering.'
  - name: List installed fonts and show font families
    text: '`InstalledFontCollection` provides access to all font families installed
      on the host system.'
  - name: Save PNG image
    text: '`bitmap.Save` writes the bitmap to a file in the chosen image format, such
      as PNG. > **Pro tip:** Use `Path.Combine` for building file paths to avoid issues
      with directory separators on different operating systems.'
  type: HowTo
- questions:
  - answer: Yes. Load the font file into a `PrivateFontCollection` and create a `Font`
      from that collection, then draw it the same way as system fonts.
    question: Can I use custom fonts that are not installed on the machine?
  - answer: Wrap font creation in a `try/catch` block and inspect `ArgumentException`
      for missing families; provide a fallback font such as `Arial`.
    question: How do I handle font‑related exceptions?
  - answer: Absolutely. The library works in ASP.NET Core, Azure Functions, and other
      server‑side .NET environments without needing GDI+.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify
      the `FontStyle` enum to apply bold, italic, or underline.
    question: Can I change the text colour or style?
  - answer: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – bitmap graphics and font handling
tags:
- save png
- aspose.drawing
- c# graphics
- installed fonts
- bitmap
title: Enregistrer une image PNG en C# avec Aspose.Drawing et les installed fonts
url: /fr/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer une image PNG en C# avec Aspose.Drawing et les polices installées

## Introduction

Si vous devez **enregistrer une image PNG en C#** tout en **créant des graphiques bitmap**, Aspose.Drawing pour .NET vous offre une méthode propre et multiplateforme pour le faire. Dans ce tutoriel, nous passerons en revue la liste des polices installées, l’affichage des familles de polices, la création de graphiques à partir d’un bitmap et le dessin de texte avec des polices — le tout pour finalement enregistrer le résultat sous forme d’image PNG. À la fin, vous disposerez d’un extrait réutilisable que vous pourrez intégrer à n’importe quel projet .NET, qu’il s’exécute sous Windows, Linux ou macOS.

## Réponses rapides
- **Que crée ce tutoriel ?** Une image PNG qui répertorie les familles de polices installées sur la machine hôte.  
- **Quelle bibliothèque est requise ?** Aspose.Drawing pour .NET (sans dépendance à System.Drawing.Common).  
- **Puis‑je utiliser des polices personnalisées ?** Oui – chargez‑les dans une `InstalledFontCollection` ou une `PrivateFontCollection`.  
- **La résolution de sortie est‑elle réglable ?** Absolument – modifiez la taille du bitmap ou le format de pixel pour contrôler la résolution.  
- **Ai‑je besoin d’une licence pour exécuter le code ?** Une licence temporaire suffit pour l’évaluation ; une licence complète est requise en production.

## Qu’est‑ce que « enregistrer une image PNG » dans le contexte d’Aspose.Drawing ?

`Bitmap` est le conteneur d’image raster d’Aspose.Drawing qui stocke les données de pixels.  
Enregistrer une image PNG signifie rendre votre surface de dessin – un `Bitmap` – dans un fichier avec l’extension `.png`. Aspose.Drawing effectue une compression PNG sans perte et peut gérer des images jusqu’à **10 000 × 10 000 pixels** sans épuiser la mémoire, ce qui le rend adapté aux graphiques haute résolution. Le fichier résultant peut être utilisé dans des pages web, des rapports ou des pipelines de traitement d’image ultérieurs.

## Pourquoi lister les polices installées et afficher les familles de polices ?

Lister les polices installées permet à votre application de s’adapter à l’environnement de l’utilisateur final, garantissant que les graphiques générés respectent l’identité visuelle de l’entreprise ou les préférences de l’utilisateur sans devoir fournir de fichiers de polices supplémentaires. `InstalledFontCollection` énumère les polices installées sur le système d’exploitation. Ceci est particulièrement utile pour la génération automatisée de rapports, de certificats ou tout contenu visuel qui doit respecter la typographie du système.

## Comment créer des graphiques bitmap en C# avec Aspose.Drawing ?

`Bitmap` représente une toile d’image ; `Graphics` fournit les méthodes de dessin pour cette toile ; `Font` décrit la police utilisée pour le rendu du texte. Vous pouvez produire un PNG complet en quelques lignes : créer un `Bitmap`, obtenir un objet `Graphics`, dessiner du texte avec une `Font` provenant de la collection installée, puis appeler `bitmap.Save`. Le guide étape par étape ci‑dessous développe chaque partie et ajoute des astuces pratiques.

## Prérequis

- **Bibliothèque Aspose.Drawing** – téléchargez la dernière version depuis la [page de téléchargement Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider ou tout éditeur compatible .NET.  
- **Connaissances de base en C#** – vous devez être à l’aise avec les classes, les objets et les boucles simples.  
- **Runtime .NET** – .NET 6+ ou .NET Core 3.1+ est recommandé pour un support multiplateforme complet.

## Importer les espaces de noms

Ajoutez les instructions `using` suivantes en haut de votre fichier C# afin que le compilateur puisse localiser les types graphiques et de police :

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Text;
using System.IO;
```

## Guide étape par étape

### Étape 1 : Créer un bitmap (le canevas)

`Bitmap` est l’objet image raster qui contient les données de pixels pour le canevas.  

```csharp
using System.Drawing;
using System.Drawing.Text;
```

### Étape 2 : Créer un objet Graphics à partir du bitmap

`Graphics` est l’objet qui fournit les fonctions de dessin telles que le tracé de formes et de texte sur un bitmap.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Étape 3 : Configurer le pinceau et la police (dessiner du texte avec des polices)

`Brush` définit comment les formes et le texte sont remplis de couleur, tandis que `Font` spécifie la famille, la taille et le style de la police pour le rendu du texte.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Étape 4 : Lister les polices installées et afficher les familles de polices

`InstalledFontCollection` donne accès à toutes les familles de polices installées sur le système hôte.  

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Étape 5 : Enregistrer l’image PNG

`bitmap.Save` écrit le bitmap dans un fichier au format d’image choisi, tel que PNG.  

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

> **Astuce :** Utilisez `Path.Combine` pour construire les chemins de fichiers afin d’éviter les problèmes de séparateurs de répertoires sur différents systèmes d’exploitation.

## Problèmes courants et solutions
| Problème | Cause | Solution |
|----------|-------|----------|
| **Aucune police affichée** | `InstalledFontCollection` non remplie (par ex., exécution sur un serveur sans tête dépourvu de polices). | Installez les polices requises sur le serveur ou intégrez des polices personnalisées dans votre application. |
| **Le fichier enregistré est corrompu** | Format de pixel incorrect ou permissions d’écriture manquantes. | Assurez‑vous que le dossier cible existe et que l’application possède les droits d’écriture ; conservez `PixelFormat.Format32bppPArgb`. |
| **Le texte apparaît flou** | Paramètres DPI faibles ou dimensions du bitmap trop petites. | Augmentez les dimensions du bitmap ou définissez `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Questions fréquemment posées

**Q : Puis‑je utiliser des polices personnalisées qui ne sont pas installées sur la machine ?**  
R : Oui. Chargez le fichier de police dans une `PrivateFontCollection` et créez une `Font` à partir de cette collection, puis dessinez‑la de la même façon que les polices système.

**Q : Comment gérer les exceptions liées aux polices ?**  
R : Enveloppez la création de la police dans un bloc `try/catch` et examinez `ArgumentException` pour les familles manquantes ; prévoyez une police de secours comme `Arial`.

**Q : Aspose.Drawing convient‑il aux applications web ?**  
R : Absolument. La bibliothèque fonctionne sous ASP.NET Core, Azure Functions et autres environnements .NET côté serveur sans nécessiter GDI+.

**Q : Puis‑je changer la couleur ou le style du texte ?**  
R : Oui. Utilisez différents types de `Brush` (par ex., `LinearGradientBrush`) et modifiez l’énumération `FontStyle` pour appliquer du gras, de l’italique ou du soulignement.

**Q : Où puis‑je obtenir une licence temporaire pour les tests ?**  
R : Téléchargez une licence d’essai depuis la [page de licence temporaire Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusion

En suivant ces étapes, vous avez appris à **enregistrer une image PNG en C#** qui répertorie dynamiquement les **polices installées**, **affiche les familles de polices**, **crée des graphiques à partir d’un bitmap** et **dessine du texte avec des polices** en utilisant Aspose.Drawing pour .NET. Vous savez maintenant comment **créer des graphiques bitmap en C#**, ajuster la résolution du bitmap et incorporer des polices personnalisées si nécessaire. Expérimentez avec différentes couleurs, tailles de police et dimensions de bitmap pour répondre aux exigences visuelles de votre projet, et explorez d’autres fonctionnalités d’Aspose.Drawing telles que le dessin de formes et la manipulation d’images pour des graphiques plus riches.

---

**Dernière mise à jour :** 2026-09-23  
**Testé avec :** Aspose.Drawing 24.11 for .NET  
**Auteur :** Aspose

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

## Tutoriels associés

- [Comment dessiner du texte avec Aspose.Drawing pour .NET](/drawing/net/text-and-fonts/draw-text/)
- [Améliorer la qualité d’image avec l’anticrénelage dans Aspose.Drawing](/drawing/net/rendering/antialiasing/)
- [Comment enregistrer un PNG avec Aspose.Drawing – Transformation du monde](/drawing/net/coordinate-transformations/world-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}