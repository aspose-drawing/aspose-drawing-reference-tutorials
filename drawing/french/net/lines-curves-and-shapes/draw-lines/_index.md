---
date: 2026-06-13
description: Apprenez comment enregistrer un bitmap au format PNG et dessiner plusieurs
  lignes dans les applications .NET en utilisant Aspose.Drawing. Ce guide étape par
  étape couvre le dessin de lignes en .NET, les techniques de dessin de lignes sur
  bitmap, et les meilleures pratiques.
keywords:
- save bitmap as png
- draw multiple lines
- how to draw lines
linktitle: Dessiner plusieurs lignes avec Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  headline: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  name: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  steps:
  - name: Create a Bitmap (draw line bitmap)
    text: The `Bitmap` class represents an in‑memory raster image that you can draw
      onto. Start by creating a new bitmap with the desired width and height. This
      will be the canvas on which you draw your lines.
  - name: Get Graphics Object
    text: The `Graphics` object provides drawing methods such as lines, shapes, and
      text for a bitmap. Obtain a `Graphics` object from the created bitmap. This
      object provides methods for drawing on the bitmap.
  - name: Define a Pen
    text: A `Pen` defines the color, width, and style of lines drawn by the `Graphics`
      object. Create a `Pen` object that defines the attributes of the line you want
      to draw. In this case, we've chosen a blue color with a thickness of 2 pixels.
  - name: Draw Lines
    text: Use the `DrawLine` method to draw lines on the bitmap. The coordinates `(x1,
      y1)` to `(x2, y2)` represent the starting and ending points of each line. By
      calling the method twice, we effectively **draw multiple lines** that form a
      simple “V” shape.
  - name: Save the Image
    text: The `Bitmap.Save` method writes the in‑memory image to a file in the format
      you specify—PNG being the most common loss‑less option. Specify the directory
      where you want to save the output image. Make sure to replace `"Your Document
      Directory"` with the actual path.
  type: HowTo
- questions:
  - answer: Yes, simply modify the `Color` parameter when creating the `Pen` object.
    question: Can I change the color of the lines?
  - answer: Aspose.Drawing supports rectangles, ellipses, curves, polygons, and more.
      Check the official documentation for a complete list.
    question: What other shapes can I draw with Aspose.Drawing?
  - answer: Absolutely. It works in ASP.NET Core, MVC, and other web frameworks, allowing
      server‑side image generation without additional dependencies.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Wrap your drawing code in a `try‑catch` block and consult the Aspose.Drawing
      forum (https://forum.aspose.com/c/drawing/44) for community support.
    question: How should I handle errors while using Aspose.Drawing?
  - answer: Yes, you can use Aspose.Drawing for commercial projects. Visit the [purchase
      page](https://purchase.aspose.com/buy) for licensing details.
    question: Can I use Aspose.Drawing for a commercial project?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Comment enregistrer un bitmap au format PNG tout en dessinant plusieurs lignes
  avec Aspose.Drawing
url: /fr/net/lines-curves-and-shapes/draw-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer le bitmap au format PNG tout en dessinant plusieurs lignes avec Aspose.Drawing

## Introduction

Dans ce tutoriel, vous apprendrez **comment enregistrer le bitmap au format PNG** et dessiner plusieurs lignes en utilisant Aspose.Drawing pour .NET. Que vous créiez un graphique simple, un contrôle UI personnalisé ou que vous génériez des graphiques sur un serveur, la capacité de rendre des lignes nettes et anti‑aliasées puis de les enregistrer en fichiers PNG est une compétence essentielle. Nous parcourrons l’ensemble du flux de travail — de la préparation du canevas à l’exportation de l’image finale — afin que vous puissiez commencer à créer des composants visuels immédiatement.

## Réponses rapides

- **Que puis‑je dessiner ?** Toute ligne droite, polyligne ou forme sur un bitmap.  
- **Quelle bibliothèque ?** Aspose.Drawing for .NET (no System.Drawing.Common required).  
- **Combien de lignes ?** Draw as many as you need – the same `Graphics.DrawLine` call can be repeated.  
- **Prérequis ?** .NET development environment and the Aspose.Drawing library.  
- **Format de sortie ?** PNG, JPEG, BMP, or any format supported by Aspose.Drawing.  

## Qu’est‑ce que le dessin de plusieurs lignes ?

Dessiner plusieurs lignes signifie rendre deux segments de ligne droite ou plus sur le même canevas d’image. Dans Aspose.Drawing, vous y parvenez en réutilisant un seul objet `Graphics` et en appelant `DrawLine` pour chaque paire de coordonnées, ce qui offre un rendu rapide et efficace en mémoire pour les sorties raster et vectorielles.

## Pourquoi utiliser Aspose.Drawing pour le dessin de lignes en .NET ?

Aspose.Drawing fournit une API moderne, multiplateforme qui prend en charge **plus de 30 formats de sortie** et peut traiter des images jusqu’à **10 000 × 10 000 pixels** sans charger le fichier complet en mémoire. Elle offre un anti‑aliasing intégré, un contrôle précis des pixels et une compatibilité totale avec .NET Core/5+, éliminant les dépendances héritées de `System.Drawing.Common`.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous d’avoir les prérequis suivants en place :

- Aspose.Drawing Library : Téléchargez et installez la bibliothèque Aspose.Drawing depuis [here](https://releases.aspose.com/drawing/net/).
- Environnement de développement : Assurez‑vous d’avoir un environnement de développement .NET configuré sur votre machine.
- Répertoire de documents : Créez un répertoire sur votre système où vous souhaitez enregistrer les images de sortie.

## Importer les espaces de noms

Dans votre application .NET, vous devez importer les espaces de noms nécessaires pour travailler avec Aspose.Drawing. Ajoutez les espaces de noms suivants au début de votre code :

```csharp
using System.Drawing;
```

Maintenant, décomposons l’exemple en plusieurs étapes pour vous guider à travers le processus de dessin de lignes avec Aspose.Drawing.

## Comment dessiner plusieurs lignes avec Aspose.Drawing

Chargez un bitmap, obtenez un objet `Graphics`, configurez un `Pen`, appelez `DrawLine` pour chaque segment, puis enregistrez le canevas au format PNG – le tout en cinq étapes concises qui peuvent être répétées ou étendues pour des dessins plus complexes. Chaque étape est illustrée par des extraits de code démontrant les appels d’API requis et les paramètres optionnels tels que l’anti‑aliasing.

### Étape 1 : Créer un Bitmap (bitmap de ligne)

La classe `Bitmap` représente une image raster en mémoire sur laquelle vous pouvez dessiner.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, PixelFormat.Format32bppPArgb);
```

Commencez par créer un nouveau bitmap avec la largeur et la hauteur souhaitées. Ce sera le canevas sur lequel vous dessinerez vos lignes.

### Étape 2 : Obtenir l’objet Graphics

L’objet `Graphics` fournit des méthodes de dessin telles que lignes, formes et texte pour un bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

Obtenez un objet `Graphics` à partir du bitmap créé. Cet objet fournit des méthodes pour dessiner sur le bitmap.

### Étape 3 : Définir un Pen

Un `Pen` définit la couleur, la largeur et le style des lignes dessinées par l’objet `Graphics`.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

Créez un objet `Pen` qui définit les attributs de la ligne que vous souhaitez dessiner. Dans ce cas, nous avons choisi une couleur bleue avec une épaisseur de 2 pixels.

### Étape 4 : Dessiner des lignes

Utilisez la méthode `DrawLine` pour dessiner des lignes sur le bitmap. Les coordonnées `(x1, y1)` à `(x2, y2)` représentent les points de départ et d’arrivée de chaque ligne. En appelant la méthode deux fois, nous **dessinons plusieurs lignes** qui forment une simple forme en « V ».

```csharp
graphics.DrawLine(pen, 10, 700, 500, 10);
graphics.DrawLine(pen, 500, 10, 990, 700);
```

### Étape 5 : Enregistrer l’image

La méthode `Bitmap.Save` écrit l’image en mémoire dans un fichier au format que vous spécifiez — le PNG étant l’option sans perte la plus courante.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawLines_out.png");
```

Spécifiez le répertoire où vous souhaitez enregistrer l’image de sortie. Assurez‑vous de remplacer `"Your Document Directory"` par le chemin réel.

## Comment enregistrer le bitmap au format PNG

Enregistrer un bitmap au format PNG est une opération en une seule ligne : appelez `bitmap.Save("output.png", ImageFormat.Png)` sur l’instance `Bitmap` sur laquelle vous avez déjà dessiné. La classe `ImageFormat` spécifie le format de fichier pour l’enregistrement des images, tel que PNG, JPEG ou BMP. Aspose.Drawing gère automatiquement la compression et préserve la transparence, ce qui rend le PNG idéal pour les actifs web et UI.

## Problèmes courants et solutions

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **L’image apparaît vide** | Objet Graphics non lié au bitmap ou format de pixel incorrect. | Assurez‑vous d’utiliser `Graphics.FromImage(bitmap)` et que le bitmap est créé avec un format de pixel pris en charge. |
| **Les lignes sont dentelées** | Anti‑aliasing désactivé. | Définissez `graphics.SmoothingMode = SmoothingMode.AntiAlias;` avant le dessin (requiert `using System.Drawing.Drawing2D;`). |
| **Chemin introuvable lors de l’enregistrement** | Chaîne de répertoire invalide. | Utilisez `Path.Combine` pour construire le chemin et vérifiez que le dossier existe. |

L’énumération `SmoothingMode` contrôle la qualité de rendu des lignes, `AntiAlias` offrant des bords plus lisses.

## Questions fréquentes

**Q : Puis‑je changer la couleur des lignes ?**  
R : Oui, il suffit de modifier le paramètre `Color` lors de la création de l’objet `Pen`.

**Q : Quelles autres formes puis‑je dessiner avec Aspose.Drawing ?**  
R : Aspose.Drawing prend en charge les rectangles, ellipses, courbes, polygones, et plus encore. Consultez la documentation officielle pour une liste complète.

**Q : Aspose.Drawing convient‑il aux applications web ?**  
R : Absolument. Il fonctionne avec ASP.NET Core, MVC et d’autres frameworks web, permettant la génération d’images côté serveur sans dépendances supplémentaires.

**Q : Comment gérer les erreurs lors de l’utilisation d’Aspose.Drawing ?**  
R : Enveloppez votre code de dessin dans un bloc `try‑catch` et consultez le forum Aspose.Drawing (https://forum.aspose.com/c/drawing/44) pour le support communautaire.

**Q : Puis‑je utiliser Aspose.Drawing pour un projet commercial ?**  
R : Oui, vous pouvez utiliser Aspose.Drawing pour des projets commerciaux. Visitez la [page d’achat](https://purchase.aspose.com/buy) pour les détails de licence.

## Conclusion

Dans ce guide, nous avons couvert tout ce dont vous avez besoin pour **enregistrer le bitmap au format PNG tout en dessinant plusieurs lignes** avec Aspose.Drawing pour .NET : créer un bitmap, obtenir un contexte graphique, configurer un pen, rendre des lignes et persister le résultat. Avec cette base, vous pouvez étendre à des graphiques dynamiques, des éléments UI personnalisés ou la génération d’images côté serveur — tout scénario nécessitant un rendu de lignes de haute qualité et évolutif.

---

**Dernière mise à jour :** 2026-06-13  
**Testé avec :** Aspose.Drawing 24.12 pour .NET  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Enregistrer le bitmap au format PNG et dessiner des courbes fermées avec Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Enregistrer le bitmap C# – Dessiner des splines de Bézier avec Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Enregistrer le bitmap au format PNG avec des pinceaux solides dans Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}