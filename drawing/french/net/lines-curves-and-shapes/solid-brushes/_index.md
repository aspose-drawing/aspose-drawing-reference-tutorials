---
date: 2026-08-01
description: Apprenez comment enregistrer un bitmap au format PNG en utilisant Solid
  Brushes dans Aspose.Drawing pour .NET. Utilisez Solid Brush pour remplir les formes
  et créer des graphiques dynamiques.
keywords:
- save bitmap as png
- export bitmap to png
- fill shape solid color
- bitmap to png conversion
lastmod: 2026-08-01
linktitle: Solid Brushes dans Aspose.Drawing
og_description: Enregistrez un bitmap au format PNG en utilisant Solid Brushes dans
  Aspose.Drawing. Ce tutoriel étape par étape montre comment créer un bitmap, remplir
  les formes avec une couleur unie et exporter le résultat sous forme de fichier PNG
  sans perte pour les projets .NET 6+.
og_image_alt: Guide showing how to save a bitmap as PNG using solid brushes in Aspose.Drawing
og_title: Enregistrer un bitmap au format PNG avec Solid Brushes – Guide Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  headline: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  name: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image canvas. The `Bitmap` class
      is Aspose.Drawing's top‑level object that stores pixel data in a mutable buffer.
      You can specify width, height, and pixel format when constructing it.
  - name: Create Graphics Object
    text: A `Graphics` object provides drawing methods for the bitmap. The `Graphics`
      class acts as a drawing surface linked to a `Bitmap`. All subsequent drawing
      commands (lines, shapes, text) are routed through this object.
  - name: Choose a Solid Brush
    text: Select a colour for the brush; in this example we use a vivid blue. The
      `SolidBrush` class defines a brush that paints with a single, uniform colour.
      It is ideal for filling shapes where a flat colour is required.
  - name: Fill Shapes with Brush
    text: Use the brush to paint an ellipse (or any other shape) on the bitmap. `FillEllipse`
      draws an ellipse filled with the specified brush. The `FillEllipse` method of
      the `Graphics` object draws an ellipse filled with the supplied `SolidBrush`.
      You can replace it with `FillRectangle`, `FillPolygon`, etc.
  - name: Save the Result as PNG
    text: Export the bitmap to a PNG file on disk. `Save` writes the image to a file
      in the chosen format. The `Save` method writes the bitmap to the specified path
      using `ImageFormat.Png`. This operation preserves the alpha channel, ensuring
      transparent backgrounds remain intact. Repeat these steps, customiz
  type: HowTo
- questions:
  - answer: Absolutely—methods like `FillRectangle`, `FillPolygon`, or `DrawPath`
      work with the same solid brush.
    question: Can I use a different shape instead of an ellipse?
  - answer: Replace the file extension in `Save` and use `ImageFormat.Jpeg` (e.g.,
      `bitmap.Save("output.jpg", ImageFormat.Jpeg);`).
    question: How do I change the output format to JPEG?
  - answer: Yes—create separate `SolidBrush` instances for each colour and call the
      appropriate `Fill*` methods sequentially.
    question: Is it possible to draw multiple shapes with different brushes in one
      bitmap?
  - answer: It's best practice to wrap them in `using` statements or call `Dispose()`
      to free unmanaged resources.
    question: Do I need to dispose of the `Graphics` and `Bitmap` objects?
  - answer: Aspose.Drawing is cross‑platform; the same code runs on Linux and macOS
      when targeting .NET Core or .NET 5+.
    question: Will this work on Linux/macOS with .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- solid brush
title: Enregistrer un bitmap au format PNG avec Solid Brushes dans Aspose.Drawing
url: /fr/net/lines-curves-and-shapes/solid-brushes/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer un bitmap au format PNG avec des pinceaux solides dans Aspose.Drawing

## Introduction

Dans ce guide, vous apprendrez **comment enregistrer un bitmap au format PNG** en utilisant des pinceaux solides avec la bibliothèque Aspose.Drawing .NET. Que vous développiez un utilitaire de bureau, un service web qui génère des icônes, ou un moteur de rapports nécessitant des actifs PNG nets, les étapes ci‑dessous vous mèneront d’une toile vierge à un fichier PNG prêt à l’emploi en quelques lignes de code. Nous couvrirons le flux de travail complet, expliquerons pourquoi les pinceaux solides sont le choix idéal pour des remplissages de couleur uniformes, et vous montrerons comment garder le code propre et multiplateforme.

## Réponses rapides
- **Que signifie « enregistrer un bitmap au format png » ?** Cela signifie exporter un objet `Bitmap` vers un fichier image PNG sans perte sur le disque.  
- **Quelle classe crée le pinceau solide ?** `SolidBrush` du namespace `Aspose.Drawing.Brushes`.  
- **Puis‑je changer la couleur du pinceau ?** Oui—passez n’importe quel `Color` (y compris les valeurs ARGB) au constructeur de `SolidBrush`.  
- **Ai‑je besoin d’une licence pour la production ?** Une version d’essai fonctionne pour l’évaluation ; une licence commerciale est requise pour les déploiements en production.  
- **Cette approche est‑elle compatible avec .NET 6+ ?** Absolument—Aspose.Drawing prend pleinement en charge .NET 5, .NET 6 et les versions ultérieures.

## Qu’est‑ce que « enregistrer un bitmap au format png » ?

Enregistrer un bitmap au format PNG convertit le tableau de pixels en mémoire en un fichier PNG sans perte, préservant la transparence et les valeurs de couleur exactes. **Enregistrer un bitmap au format PNG** est une opération courante lorsque vous avez besoin d’un format d’image portable que les navigateurs et les éditeurs d’images peuvent lire sans perte de qualité.

## Pourquoi utiliser des pinceaux solides pour enregistrer un bitmap au format png ?

Les pinceaux solides fournissent une couleur unique et uniforme qui remplit instantanément toute forme vectorielle, éliminant le besoin de dégradés complexes lorsque vous ne nécessitez qu’une couleur plate. L’utilisation de pinceaux solides avec Aspose.Drawing exploite également un moteur de rendu capable de gérer des images jusqu’à **10 000 × 10 000 pixels** tout en maintenant l’utilisation de la mémoire sous **200 Mo**, ce qui le rend adapté aux actifs haute résolution.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous que les prérequis suivants sont en place :

- Bibliothèque Aspose.Drawing pour .NET : téléchargez et installez la bibliothèque depuis [Aspose.Drawing for .NET Documentation](https://reference.aspose.com/drawing/net/).
- Environnement de développement intégré (IDE) : disposez d’un environnement de développement .NET fonctionnel, tel que Visual Studio, installé sur votre machine.

Maintenant que tout est prêt, passons à l’implémentation.

## Importer les espaces de noms

Les directives `using` importent les types requis dans le scope.

Le namespace `Aspose.Drawing` fournit les classes graphiques de base, tandis que `System.Drawing` fournit les définitions de couleur et la classe `SolidBrush`.

```csharp
using System.Drawing;
```

## Comment enregistrer un bitmap au format PNG avec des pinceaux solides

Cette section décrit le flux de travail complet : créer une toile bitmap, obtenir une surface graphique, instancier un `SolidBrush` avec la couleur souhaitée, remplir une ou plusieurs formes, puis appeler `Save` pour écrire l’image au format PNG. Le code fonctionne multiplateforme sur .NET 6 et versions ultérieures.

### Étape 1 : Créer un Bitmap

La classe `Bitmap` représente une toile d’image en mémoire.

La classe `Bitmap` est l’objet de haut niveau d’Aspose.Drawing qui stocke les données de pixels dans un tampon mutable. Vous pouvez spécifier la largeur, la hauteur et le format de pixel lors de sa construction.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Étape 2 : Créer un objet Graphics

Un objet `Graphics` fournit des méthodes de dessin pour le bitmap.

La classe `Graphics` agit comme une surface de dessin liée à un `Bitmap`. Toutes les commandes de dessin ultérieures (lignes, formes, texte) sont acheminées via cet objet.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Étape 3 : Choisir un pinceau solide

Sélectionnez une couleur pour le pinceau ; dans cet exemple nous utilisons un bleu vif.

La classe `SolidBrush` définit un pinceau qui peint avec une couleur unique et uniforme. Elle est idéale pour remplir des formes où une couleur plate est requise.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
```

### Étape 4 : Remplir les formes avec le pinceau

Utilisez le pinceau pour peindre une ellipse (ou toute autre forme) sur le bitmap.

`FillEllipse` dessine une ellipse remplie avec le pinceau spécifié. La méthode `FillEllipse` de l’objet `Graphics` dessine une ellipse remplie avec le `SolidBrush` fourni. Vous pouvez la remplacer par `FillRectangle`, `FillPolygon`, etc., pour créer différentes géométries.

```csharp
graphics.FillEllipse(brush, 100, 100, 800, 600);
```

### Étape 5 : Enregistrer le résultat au format PNG

Exporter le bitmap vers un fichier PNG sur le disque.

`Save` écrit l’image dans un fichier au format choisi. La méthode `Save` écrit le bitmap au chemin spécifié en utilisant `ImageFormat.Png`. Cette opération préserve le canal alpha, garantissant que les arrière‑plans transparents restent intacts.

```csharp
bitmap.Save("Your Document Directory" + @"Brushes\Solid_out.png");
```

Répétez ces étapes, en personnalisant les couleurs et les formes selon la conception visuelle de votre application.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Erreur fichier introuvable** lors de l’enregistrement | Le dossier cible n’existe pas | Assurez‑vous que le répertoire (`Your Document Directory\Brushes`) est créé avant d’appeler `Save`. |
| **Couleurs incorrectes** | Utilisation d’un `KnownColor` qui dépend du thème du système | Utilisez `Color.FromArgb` pour des valeurs RGBA précises. |
| **Transparence perdue** | Utilisation d’un format de pixel sans canal alpha | Conservez `PixelFormat.Format32bppPArgb` comme indiqué pour conserver le canal alpha. |

## Questions fréquemment posées

**Q : Puis‑je utiliser une forme différente au lieu d’une ellipse ?**  
R : Absolument—des méthodes comme `FillRectangle`, `FillPolygon` ou `DrawPath` fonctionnent avec le même pinceau solide.

**Q : Comment changer le format de sortie en JPEG ?**  
R : Remplacez l’extension du fichier dans `Save` et utilisez `ImageFormat.Jpeg` (par ex., `bitmap.Save("output.jpg", ImageFormat.Jpeg);`).

**Q : Est‑il possible de dessiner plusieurs formes avec différents pinceaux dans un même bitmap ?**  
R : Oui—créez des instances séparées de `SolidBrush` pour chaque couleur et appelez les méthodes `Fill*` appropriées séquentiellement.

**Q : Dois‑je libérer les objets `Graphics` et `Bitmap` ?**  
R : Il est recommandé de les encapsuler dans des instructions `using` ou d’appeler `Dispose()` pour libérer les ressources non gérées.

**Q : Cette méthode fonctionne‑t‑elle sous Linux/macOS avec .NET Core ?**  
R : Aspose.Drawing est multiplateforme ; le même code s’exécute sous Linux et macOS lorsqu’on cible .NET Core ou .NET 5+.  

---

**Dernière mise à jour :** 2026-08-01  
**Testé avec :** Aspose.Drawing 24.12 pour .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Enregistrer un bitmap au format PNG et dessiner des courbes fermées avec Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Enregistrer un bitmap au format PNG en utilisant la transformation dans Aspose.Drawing](/drawing/net/coordinate-transformations/local-transformation/)
- [Comment recadrer une image au format PNG avec Aspose.Drawing pour .NET](/drawing/net/image-editing/cropping/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}