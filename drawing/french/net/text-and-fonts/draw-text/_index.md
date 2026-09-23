---
date: 2026-09-23
description: Apprenez à dessiner du texte sur une image en utilisant Aspose.Drawing
  pour .NET. Générez une image avec du texte, ajoutez du texte à un bitmap et enregistrez
  le bitmap au format PNG avec des polices personnalisées.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Comment dessiner du texte avec Aspose.Drawing
og_description: Apprenez à dessiner du texte sur une image en utilisant Aspose.Drawing
  pour .NET. Ce tutoriel vous montre comment générer une image avec du texte, ajouter
  du texte à un bitmap et enregistrer le bitmap au format PNG avec des polices personnalisées.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Dessiner du texte sur une image avec Aspose.Drawing pour .NET – Guide rapide
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Comment dessiner du texte sur une image avec Aspose.Drawing pour .NET
url: /fr/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment dessiner du texte sur une image avec Aspose.Drawing pour .NET

## Introduction

Dans ce guide étape par étape, vous apprendrez **comment dessiner du texte sur une image** en utilisant Aspose.Drawing pour .NET. Que vous ayez besoin de créer une *image texte dynamique*, d’ajouter du texte à un bitmap existant, ou de générer un graphique avec des polices personnalisées, ce tutoriel vous accompagne dans chaque détail afin que vous puissiez commencer à dessiner du texte en quelques minutes. La bibliothèque prend en charge plus de 30 méthodes GDI+, fonctionne sous Windows, Linux et macOS, et possède **zéro dépendance externe**, ce qui en fait un choix fiable pour la génération d’images côté serveur.

## Réponses rapides
- **Quelle bibliothèque est utilisée ?** Aspose.Drawing for .NET  
- **Tâche principale ?** Dessiner du texte sur une image (créer une image avec du texte)  
- **Méthode clé ?** `Graphics.DrawString` (dessiner une chaîne sur l'image)  
- **Format de sortie ?** PNG (enregistrer le bitmap en PNG)  
- **Prérequis ?** Environnement de développement .NET et bibliothèque Aspose.Drawing  

## Qu’est‑ce que le dessin de texte avec Aspose.Drawing ?

Dessiner du texte avec Aspose.Drawing signifie utiliser l’API compatible GDI+ de la bibliothèque pour rendre des chaînes Unicode sur un canevas raster. La méthode `Graphics.DrawString` écrit le texte dans un bitmap, vous permettant de contrôler la police, la couleur, l’alignement et l’anti‑aliasing. Cette approche vous permet de générer des images de haute qualité sans installer System.Drawing.Common.

## Pourquoi utiliser Aspose.Drawing pour ajouter du texte aux images ?

Aspose.Drawing offre une méthode fiable et multiplateforme pour rendre du texte sur des images sans nécessiter les bibliothèques GDI+ natives, garantissant une qualité et des performances constantes sur tout système d’exploitation. Elle prend en charge l’anti‑aliasing avancé, les caractères Unicode et les polices personnalisées, et s’intègre parfaitement aux applications .NET, ce qui la rend idéale tant pour la génération d’images côté serveur que pour les outils de bureau.

- **Fiabilité multiplateforme** – fonctionne sous Windows, Linux et macOS.  
- **Rendu avancé** – anti‑aliasing et lissage du texte sous‑pixel pour une sortie nette.  
- **Aucune dépendance externe** – la bibliothèque regroupe tout ce dont vous avez besoin pour *créer une image avec du texte*.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Aspose.Drawing pour .NET** – téléchargez-le depuis la [documentation Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **Un IDE .NET** tel que Visual Studio ou VS Code.  

## Importer les espaces de noms

Commencez par importer les espaces de noms requis :

Ces espaces de noms fournissent les types GDI+ de base tels que `Bitmap`, `Graphics` et les utilitaires de rendu de texte.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Étape 1 : créer les objets bitmap et graphics

`Bitmap` est le conteneur d’image raster d’Aspose.Drawing pour les données de pixels, et `Graphics` fournit les méthodes de dessin pour rendre des formes et du texte dessus.  

`Bitmap` représente une image en mémoire, tandis que `Graphics` fournit des méthodes de dessin pour rendre sur ce bitmap.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Ici, nous créons un `Bitmap` qui contiendra l’image finale et un objet `Graphics` qui nous permet de dessiner dessus. L’indice d’anti‑aliasing garantit que le texte apparaît lisse.

## Étape 2 : configurer le pinceau, le crayon et la police

`Brush` définit la couleur de remplissage, `Pen` trace les contours des formes, et `Font` spécifie la police, la taille et le style pour le rendu du texte.  

`Brush` remplit les formes avec une couleur, `Pen` trace les contours des formes, et `Font` définit la police et la taille pour le rendu du texte.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** définit la couleur du texte.  
- **Pen** est utilisé plus tard pour dessiner un rectangle autour du texte (optionnel).  
- **Font** spécifie la police, la taille et le style pour l’opération *draw string on image*.

## Étape 3 : définir le texte et le rectangle

`Rectangle` définit la boîte englobante où le texte sera placé, en précisant les coordonnées X/Y ainsi que la largeur/hauteur.  

`Rectangle` indique la position et la taille d’une zone rectangulaire, utilisée ici pour encadrer le texte dessiné.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

Le `Rectangle` détermine où le texte sera placé. Ajustez les coordonnées et la taille selon votre mise en page.

## Étape 4 : dessiner le rectangle et le texte

`Graphics.DrawString` rend le texte spécifié à l’intérieur du rectangle donné en utilisant la police et le pinceau fournis.  

`Graphics.DrawString` rend une chaîne de texte à l’intérieur d’un rectangle spécifié en utilisant la police et le pinceau fournis.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

D’abord, nous délimitons la zone avec un rectangle bleu, puis nous **ajoutons du texte au bitmap** en appelant `DrawString`. C’est le cœur du *drawing text* sur l’image.

## Étape 5 : enregistrer le résultat

L’image est enregistrée sous forme de fichier PNG, répondant à l’exigence *save bitmap as PNG*. Remplacez le chemin de substitution par le dossier réel où vous souhaitez stocker le fichier.  

`bitmap.Save` écrit l’image dans un fichier au format choisi, tel que PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Cas d’utilisation courants

- **Génération de certificats** avec des noms personnalisés.  
- **Création de miniatures filigranées** pour les galeries web.  
- **Construction de graphiques dynamiques** incluant des libellés ou des annotations.  

## Dépannage et astuces

- **Police introuvable ?** Assurez‑vous que la police est installée sur la machine hôte ou utilisez une collection de polices privées.  
- **Texte tronqué ?** Augmentez la taille du rectangle ou réduisez la taille de la police.  
- **Problèmes de performance ?** Réutilisez le même objet `Graphics` pour plusieurs opérations de dessin lorsque c’est possible.  

## Questions fréquemment posées

**Q : Comment changer le format de sortie en JPEG ?**  
R : Remplacez l’extension `.png` par `.jpg` dans la méthode `Save` et, éventuellement, spécifiez un `ImageCodecInfo` pour la qualité JPEG.

**Q : Puis‑je dessiner du texte multi‑lignes ?**  
R : Oui, incluez des caractères de saut de ligne (`\n`) dans la chaîne ou utilisez `StringFormat` avec `FormatFlags.LineLimit`.

**Q : Existe‑t‑il un moyen de mesurer la taille du texte avant de le dessiner ?**  
R : Utilisez `Graphics.MeasureString` pour obtenir les dimensions exactes du texte rendu.

**Q : Aspose.Drawing prend‑il en charge les caractères Unicode ?**  
R : Absolument. Fournissez une police contenant les glyphes requis et la bibliothèque les rendra correctement.

**Q : Quelle version d’Aspose.Drawing a été utilisée pour les tests ?**  
R : Les exemples ont été testés avec Aspose.Drawing 24.11 pour .NET.

---

**Dernière mise à jour :** 2026-09-23  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Créer des graphiques bitmap C# – Enregistrer une image PNG et travailler avec les polices installées dans Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Comment enregistrer un bitmap en PNG en utilisant l’API Aspose.Drawing pour .NET](/drawing/net/image-editing/display/)
- [Texte sur image](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}