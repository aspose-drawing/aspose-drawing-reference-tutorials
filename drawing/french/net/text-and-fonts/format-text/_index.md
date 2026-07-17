---
date: 2026-07-17
description: Apprenez comment empêcher le débordement de texte en définissant l'alignement
  du texte dans Aspose.Drawing pour .NET et ajouter du texte aux images. Guide étape
  par étape avec des exemples.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Définir l'alignement du texte avec Aspose.Drawing pour .NET
og_description: Empêchez le débordement de texte en définissant l'alignement du texte
  dans Aspose.Drawing pour .NET. Apprenez à dessiner une chaîne sur une image, centrer
  le texte dans un rectangle et remplacer System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Empêcher le débordement de texte – Définir l'alignement du texte avec Aspose.Drawing
  pour .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Empêcher le débordement de texte – Définir l'alignement du texte avec Aspose.Drawing
  pour .NET
url: /fr/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Empêcher le débordement de texte – Définir l'alignement du texte avec Aspose.Drawing

## Introduction

Lorsque vous devez **empêcher le débordement de texte** lors du rendu de graphiques en .NET, Aspose.Drawing vous offre un contrôle précis sur le placement du texte, son alignement et son enveloppement. Que vous créiez un générateur de badges, un rapport dynamique ou toute sortie basée sur des images, maîtriser l'alignement du texte garantit que votre texte reste à l'intérieur du rectangle prévu et a un aspect soigné. Dans ce guide, nous parcourrons la création d'un canevas bitmap, la configuration de `StringFormat`, le dessin d'un rectangle avec du texte centré, la gestion du débordement, puis l'enregistrement de l'image.

## Réponses rapides
- **Que signifie “set text alignment” ?** Il définit comment le texte est positionné horizontalement et verticalement à l'intérieur d'un rectangle de dessin.  
- **Quelle classe contrôle l'alignement ?** `StringFormat` vous permet de définir `Alignment` et `LineAlignment`.  
- **Puis-je dessiner une chaîne et un rectangle ensemble ?** Oui — utilisez `Graphics.DrawRectangle` suivi de `Graphics.DrawString`.  
- **Comment empêcher le débordement de texte ?** Ajustez la taille du rectangle ou divisez le texte en plusieurs lignes manuellement.  
- **Ai-je besoin d'une licence pour la production ?** Une licence commerciale Aspose.Drawing est requise pour une utilisation non‑évaluation.

## Qu'est-ce que **set text alignment** dans Aspose.Drawing ?

`set text alignment` configure le placement horizontal (`StringAlignment`) et vertical (`LineAlignment`) du texte à l'intérieur d'un `Rectangle` ou d'une région de dessin. En ajustant ces propriétés, vous contrôlez si le texte apparaît aligné à gauche, centré, aligné à droite, aligné en haut, au milieu ou en bas, permettant une mise en page précise dans les graphiques, badges et rapports générés avec Aspose.Drawing.

## Pourquoi utiliser Aspose.Drawing pour l'alignement du texte ?

Aspose.Drawing élimine les limitations de GDI+ qui affectent `System.Drawing.Common`. Il prend en charge **5 principaux runtimes .NET** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 et .NET 7 – et peut rendre des images jusqu'à **4000 × 4000 px** (≈ 100 Mo) sans épuiser la mémoire. L'anti‑aliasing, le redimensionnement haute‑DPI et la pleine compatibilité avec les conteneurs Linux vous permettent de générer des graphiques pixel‑parfait dans n'importe quel scénario de déploiement.

## Prérequis

1. **Bibliothèque Aspose.Drawing** – téléchargez‑la [ici](https://releases.aspose.com/drawing/net/).  
2. **Environnement de développement** – Visual Studio 2022 (ou tout IDE C#).  
3. **Connaissances de base en .NET** – vous devez être à l'aise avec les projets C# et les packages NuGet.

## Importer les espaces de noms

Pour commencer, importez les espaces de noms requis. Ceux‑ci vous donnent accès aux graphiques, au rendu du texte et aux primitives de dessin.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Comment empêcher le débordement de texte avec Aspose.Drawing ?

Bitmap est une classe représentant une image stockée en mémoire, tandis que `RectangleF` définit une zone rectangulaire à virgule flottante pour le dessin. En utilisant un `StringFormat` avec `Trimming` réglé sur `StringTrimming.EllipsisCharacter`, les caractères excédentaires sont automatiquement remplacés par une ellipse, garantissant que le texte ne dépasse jamais les limites du rectangle. Mesurer la chaîne d'abord vous permet de décider de réduire le rectangle ou de diviser le texte en plusieurs lignes, assurant une mise en page propre sans débordement.

Chargez votre bitmap, définissez un `RectangleF` de taille appropriée, et utilisez un `StringFormat` avec `Trimming` réglé sur `StringTrimming.EllipsisCharacter` pour couper automatiquement les caractères excédentaires. Pour un contrôle complet, mesurez la chaîne avec `Graphics.MeasureString` et réduisez le rectangle ou divisez le texte en lignes avant le dessin. Cette approche garantit qu'aucun caractère ne déborde des limites visuelles.

## Étape 1 : Créer des objets Bitmap et Graphics

Bitmap représente une image en mémoire, tandis que Graphics fournit les méthodes de dessin pour ce bitmap. Créer un bitmap fournit une toile sur laquelle vous pouvez dessiner. L'objet `Graphics` est la surface de dessin, et nous activons le rendu de texte haute qualité avec `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Étape 2 : Définir **StringFormat** et le style

StringFormat spécifie les options de mise en page du texte telles que l'alignement, l'espacement des lignes et le rognage. Ici nous **set text alignment** en configurant une instance de `StringFormat`. Nous préparons également les pinceaux, les stylos et une police qui seront utilisés lors du dessin de la chaîne.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Étape 3 : Créer et formater le texte – **how to draw string** et **draw rectangle with text**

Graphics.DrawString rend le texte sur la toile, et Graphics.DrawRectangle dessine une forme de rectangle. Nous composons le texte, définissons le rectangle qui le contiendra, puis dessinons à la fois la bordure du rectangle et la chaîne elle-même.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Comment gérer le débordement de texte

Si le `text` fourni dépasse les limites du rectangle, vous avez deux options courantes :

1. **Redimensionner le rectangle** – augmenter `rectangle.Width` ou `rectangle.Height`.  
2. **Diviser le texte** – couper la chaîne en lignes qui tiennent, puis appeler `DrawString` pour chaque ligne avec des coordonnées Y ajustées.

## Comment dessiner une chaîne sur une image avec Aspose.Drawing ?

Graphics.DrawString dessine le texte spécifié en utilisant une police et des options de formatage. Instanciez un objet `Graphics` à partir de votre bitmap, puis appelez `DrawString` avec le `StringFormat` préparé. Cet appel unique rend le texte exactement à l'endroit souhaité, en respectant l'alignement, le rognage et toute matrice de transformation appliquée. Ajouter un indice de rendu haute qualité garantit que la sortie reste nette sur les écrans haute‑DPI.

## Comment centrer le texte dans un rectangle ?

StringAlignment détermine l'alignement horizontal du texte à l'intérieur d'un rectangle de mise en page. Définissez `stringFormat.Alignment = StringAlignment.Center` et `stringFormat.LineAlignment = StringAlignment.Center`. Cela centre le texte horizontalement et verticalement à l'intérieur du rectangle, ce qui le rend idéal pour les badges, les boutons ou les superpositions d'étiquettes. Le placement centré fonctionne de manière cohérente sur différentes tailles d'image et réglages DPI, offrant une apparence visuelle équilibrée.

## Comment obtenir un alignement vertical du texte ?

LineAlignment contrôle le placement vertical du texte à l'intérieur du rectangle. Utilisez `stringFormat.LineAlignment` avec les valeurs `StringAlignment.Near`, `Center` ou `Far` pour positionner le texte en haut, au milieu ou en bas du rectangle. Combinez cela avec `Graphics.TranslateTransform` si vous devez faire pivoter le texte tout en préservant l'alignement vertical. Ajuster l'alignement de ligne garantit que les blocs multi‑lignes s'alignent exactement où vous l'attendez, même après les transformations.

## Étape 4 : Enregistrer la sortie – **add text to image**

Enfin, écrivez le bitmap sur le disque. Cette étape montre **add text to image** en un seul appel.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Le texte apparaît flou** | Assurez‑vous que `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` est défini. |
| **Le texte est tronqué** | Augmentez la taille du rectangle ou activez la logique de retour à la ligne en mesurant la taille de la chaîne (`Graphics.MeasureString`). |
| **Police introuvable** | Vérifiez que la police est installée sur la machine hôte ou intégrez une police privée avec `PrivateFontCollection`. |
| **Couleurs inattendues** | Revérifiez les couleurs du pinceau et du stylo ; rappelez‑vous que `Color.FromKnownColor` utilise des couleurs définies par le système. |

## Questions fréquemment posées

**Q1 : Aspose.Drawing est‑il compatible avec toutes les versions .NET ?**  
R1 : Oui, Aspose.Drawing est conçu pour être compatible avec un large éventail de versions .NET, assurant une flexibilité pour les développeurs.

**Q2 : Puis‑je personnaliser davantage le style de police ?**  
R2 : Absolument ! Ajustez les paramètres de l'objet `Font` pour obtenir la taille, le style et la famille de police souhaités.

**Q3 : Comment gérer le débordement de texte dans le rectangle défini ?**  
R3 : Vous pouvez gérer le débordement de texte en ajustant la taille du rectangle ou en implémentant une logique personnalisée pour traiter les textes longs.

**Q4 : Existe‑t‑il d'autres options de formatage disponibles dans Aspose.Drawing ?**  
R4 : Oui, Aspose.Drawing offre un ensemble complet d'outils pour la manipulation graphique, incluant diverses options de formatage pour le texte, les formes, et plus encore.

**Q5 : Où puis‑je trouver un support supplémentaire pour Aspose.Drawing ?**  
R5 : Explorez le forum Aspose.Drawing [ici](https://forum.aspose.com/c/drawing/44) pour le support communautaire et les discussions.

**Q : Comment dessiner une chaîne sans rectangle entourant ?**  
R : Omettez l'appel `DrawRectangle` et transmettez la position `PointF` souhaitée à `Graphics.DrawString`.

**Q : Puis‑je faire pivoter le texte tout en conservant l'alignement ?**  
R : Oui—appliquez une transformation `Matrix` à l'objet `Graphics` avant le dessin, puis réinitialisez‑la ensuite.

**Q : Est‑il possible d'exporter l'image en JPEG au lieu de PNG ?**  
R : Il suffit de changer l'extension du fichier dans `bitmap.Save` et éventuellement spécifier `ImageFormat.Jpeg`.

**Dernière mise à jour :** 2026-07-17  
**Testé avec :** Aspose.Drawing 24.11 for .NET  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [How to Draw Text with Aspose.Drawing for .NET](/drawing/net/text-and-fonts/draw-text/)
- [Adding Text on Images in Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [How to Draw Text and Fonts with Aspose.Drawing for .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}