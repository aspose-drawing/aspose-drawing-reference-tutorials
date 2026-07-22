---
date: 2026-07-22
description: Apprenez comment enregistrer un bitmap au format PNG et exporter l'image
  en JPEG avec Aspose.Drawing. Ce guide étape par étape montre comment tracer des
  chemins, créer des images et exporter les formats.
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: Tracer des chemins dans Aspose.Drawing
og_description: Enregistrez le bitmap au format PNG et exportez l'image en JPEG en
  utilisant Aspose.Drawing pour .NET. Suivez ce tutoriel pour tracer des chemins complexes,
  créer des images de haute qualité et générer plusieurs formats.
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: Enregistrer le bitmap au format PNG – Tracer des chemins avec Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: Enregistrer le bitmap au format PNG – Utilisation de GraphicsPath dans Aspose.Drawing
url: /fr/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tracer des chemins avec Aspose.Drawing

## Comment utiliser GraphicsPath – Introduction

**Save bitmap as PNG** est souvent la première étape lorsque vous avez besoin d'une image sans perte pour un traitement ou une publication ultérieure. Dans ce tutoriel, vous apprendrez à dessiner des chemins vectoriels sophistiqués avec `GraphicsPath`, à les rendre sur un bitmap, puis à **save bitmap as PNG** ou même à **export image to JPEG**. Que vous construisiez un moteur de reporting, une bibliothèque de graphiques personnalisée, ou que vous ayez simplement besoin de générer des graphiques dynamiques, Aspose.Drawing vous fournit une API entièrement gérée, multiplateforme, qui remplace System.Drawing.Common.

## Réponses rapides

- **Que puis‑je dessiner avec GraphicsPath ?** Lignes, rectangles, ellipses, courbes et formes personnalisées.  
- **Ai‑je besoin d’une licence ?** Un essai est gratuit ; une licence commerciale est requise pour la production.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **System.Drawing.Common est‑il requis ?** Non, Aspose.Drawing fonctionne de façon indépendante.  
- **Puis‑je enregistrer dans différents formats ?** Oui – PNG, JPEG, BMP, GIF, et plus.  

## Qu’est‑ce que GraphicsPath ?

`GraphicsPath` est le conteneur vectoriel d’Aspose.Drawing qui stocke une séquence de primitives de dessin telles que lignes, arcs et courbes sous forme d’un seul objet. En regroupant ces primitives, vous pouvez appliquer des transformations, des règles de remplissage et des paramètres de contour de manière uniforme, ce qui simplifie la création de graphiques complexes et assure un rendu cohérent sur différents formats de sortie.

## Pourquoi utiliser GraphicsPath avec Aspose.Drawing ?

L’utilisation de GraphicsPath avec Aspose.Drawing vous offre des capacités de dessin vectoriel précises, flexibles et haute performance. Elle vous permet de créer des formes complexes, d’appliquer des transformations et de les rendre efficacement, tout en maintenant une cohérence multiplateforme et en supportant le traitement d’images à grande échelle. De plus, elle s’intègre parfaitement aux autres bibliothèques .NET, vous permettant de combiner des flux de travail raster et vectoriel dans une même application.

- **Précision :** Gère plus de 50 primitives vectorielles avec une précision sub‑pixel, garantissant que lorsque vous **save bitmap as PNG** le rendu reste net à n’importe quelle résolution.  
- **Flexibilité :** Combinez lignes, arcs et courbes de Bézier en un seul chemin, puis rendez‑le avec un appel unique `Graphics.DrawPath`.  
- **Performance :** Le pipeline de rendu optimisé traite des images jusqu’à 400 MP sans charger le fichier complet en mémoire, rendant les traitements par lots à grande échelle réalisables.  
- **Multiplateforme :** Résultats identiques sur les environnements Windows, Linux et macOS, éliminant les bugs spécifiques à une plateforme.  

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous de disposer des prérequis suivants :

- **Aspose.Drawing Library :** Téléchargez et installez la bibliothèque Aspose.Drawing. Vous pouvez trouver la bibliothèque [ici](https://releases.aspose.com/drawing/net/).
- **Other Aspose Products :** Découvrez d’autres offres Aspose [ici](https://releases.aspose.com/).
- **Development Environment :** Configurez votre environnement de développement .NET avec les outils nécessaires (Visual Studio, .NET SDK, etc.).

## Importer les espaces de noms

Commencez par importer les espaces de noms requis dans votre projet :

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Étape 1 : Créer un Bitmap et un Graphics

`Bitmap` représente une image en mémoire, tandis que `Graphics` fournit des méthodes de dessin pour rendre sur cette image. Commencez par créer un `Bitmap` et un objet `Graphics` avec lesquels travailler. Ce bitmap sera le canevas sur lequel le `GraphicsPath` sera rendu, et plus tard vous **save bitmap as PNG** :

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Étape 2 : Définir le Pen et le GraphicsPath

Le `Pen` définit la couleur, la largeur et le style de la ligne ; `GraphicsPath` stocke une collection de primitives de dessin en tant qu’objet vectoriel unique. Ensuite, définissez un `Pen` pour spécifier les attributs de dessin et créez un `GraphicsPath`. L’objet `GraphicsPath` contient les données vectorielles avant le rendu :

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## Étape 3 : Ajouter des lignes et des formes

`AddLine`, `AddRectangle` et `AddEllipse` ajoutent les formes respectives au `GraphicsPath` pour un rendu ultérieur. Ajoutez des lignes, des rectangles et des ellipses au `GraphicsPath` pour créer un chemin complexe. Vous pouvez également ajouter des courbes de Bézier personnalisées pour des formes lisses :

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## Étape 4 : Dessiner le chemin

`DrawPath` rend les données vectorielles d’un `GraphicsPath` sur la surface `Graphics` en utilisant le `Pen` spécifié. Dessinez le chemin sur l’objet `Graphics` avec le `Pen` indiqué. Cette opération rasterise les données vectorielles sur le canevas bitmap :

```csharp
graphics.DrawPath(pen, path);
```

## Étape 5 : Enregistrer l’image – Exporter en PNG ou JPEG

La méthode `Bitmap.Save` écrit l’image sur le disque dans le format choisi tel que PNG ou JPEG. Après le dessin, vous pouvez **save bitmap as PNG** pour une qualité sans perte ou **export image to JPEG** pour une taille de fichier plus petite. Choisissez le format qui correspond le mieux à votre scénario en aval :

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

Répétez ces étapes au besoin pour créer des chemins complexes et visuellement attrayants.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Chemin non visible** | Assurez‑vous que la couleur du Pen contraste avec l’arrière‑plan et que le bitmap est enregistré correctement. |
| **Taille d’image inattendue** | Vérifiez que les dimensions du bitmap et le format de pixel correspondent à vos exigences. |
| **Exception de licence** | Utilisez une licence d’essai pour les tests ; appliquez une licence valide avant le déploiement en production. |

## Questions fréquemment posées

### Q1 : Puis‑je utiliser Aspose.Drawing avec d’autres bibliothèques .NET ?

A1 : Oui, Aspose.Drawing s’intègre parfaitement aux autres bibliothèques .NET, offrant une grande polyvalence dans vos projets de développement.

### Q2 : Une version d’essai est‑elle disponible ?

A2 : Oui, vous pouvez accéder à l’essai gratuit [ici](https://releases.aspose.com/).

### Q3 : Où puis‑je trouver du support pour Aspose.Drawing ?

A3 : Visitez le [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pour obtenir de l’aide et le support de la communauté.

### Q4 : Comment obtenir une licence temporaire ?

A4 : Obtenez une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Puis‑je acheter Aspose.Drawing ?

A5 : Oui, vous pouvez acheter Aspose.Drawing [ici](https://purchase.aspose.com/buy).

**Questions supplémentaires**

**Q : Puis‑je dessiner des courbes de Bézier personnalisées avec GraphicsPath ?**  
A : Absolument – utilisez `path.AddBezier(...)` pour définir des courbes lisses.

**Q : Comment puis‑je vider un GraphicsPath avant de le réutiliser ?**  
A : Appelez `path.Reset()` pour supprimer toutes les figures et repartir à zéro.

## Conclusion

Félicitations ! Vous avez appris avec succès **comment utiliser GraphicsPath** pour tracer des chemins puis **save bitmap as PNG** ou **export image to JPEG** en utilisant Aspose.Drawing pour .NET. Ce tutoriel a couvert la création d’un bitmap, la définition d’un pen, la construction d’un `GraphicsPath`, le rendu de diverses formes, et l’exportation de l’image finale dans plusieurs formats. Expérimentez avec différentes coordonnées, couleurs et largeurs de ligne pour libérer tout le potentiel créatif d’Aspose.Drawing.

---

**Dernière mise à jour :** 2026-07-22  
**Testé avec :** Aspose.Drawing 24.12 for .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Enregistrer le bitmap en PNG et tracer des courbes fermées avec Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Enregistrer le bitmap C# – tracer des splines de Bézier avec Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Comment enregistrer une image et tracer des splines cardinales dans Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}