---
date: 2026-05-29
description: Apprenez à enregistrer un PNG et à tracer des splines cardinales en .NET
  avec Aspose.Drawing. Enregistrez la courbe au format PNG, créez des graphiques lisses
  et générez un bitmap dans un fichier sans effort.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Tracer des splines cardinales avec Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Comment enregistrer un PNG et tracer des splines cardinales avec Aspose.Drawing
url: /fr/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment enregistrer un PNG et tracer des splines cardinales avec Aspose.Drawing

## Introduction

Dans ce tutoriel, vous découvrirez **comment enregistrer un PNG** tout en dessinant des splines cardinales lisses à l'aide d'Aspose.Drawing pour .NET. Que vous construisiez un composant de graphiques, un éditeur de diagrammes, ou que vous ayez simplement besoin d'exporter une courbe personnalisée au format PNG, les étapes ci‑dessous vous guideront pour créer une toile bitmap, tracer une spline avec un crayon, et persister le résultat sur le disque. Vous verrez également pourquoi Aspose.Drawing est une alternative multiplateforme fiable à System.Drawing.Common.

## Réponses rapides
- **Que fait la méthode principale ?** `Graphics.DrawCurve` interpole une série de points en une spline cardinale lisse.  
- **Quel format est utilisé pour enregistrer l'image ?** PNG via `Bitmap.Save`.  
- **Ai-je besoin d'une licence pour enregistrer des images ?** Un essai fonctionne pour le développement ; une licence commerciale est requise pour la production.  
- **Puis-je modifier la tension de la courbe ?** Oui, les surcharges de `DrawCurve` vous permettent de spécifier la tension.  
- **Aspose.Drawing est‑il compatible avec .NET 6+ ?** Absolument – il prend en charge .NET Framework et .NET Core/5/6.

## Qu’est‑ce que « comment enregistrer un PNG » dans le contexte d’Aspose.Drawing ?

Enregistrer un PNG signifie convertir le bitmap en mémoire sur lequel vous dessinez en un fichier PNG physique sur le disque. Le processus écrit les données de pixels en utilisant une compression sans perte, préservant les couleurs exactes ainsi que les informations de canal alpha. La méthode `Bitmap.Save` d’Aspose.Drawing gère automatiquement l’encodage PNG, vous n’avez donc pas besoin de gérer les détails du format vous‑même.

## Pourquoi tracer une spline cardinale avec Aspose.Drawing ?

Une spline cardinale produit une courbe lisse et fluide qui suit de près un ensemble de points de contrôle, ce qui la rend idéale pour les visualisations de données, les graphiques d’interface utilisateur et les formes personnalisées. Aspose.Drawing prend en charge **plus de 30 formats d’image** et peut rendre des graphiques de plusieurs centaines de pages sans charger le fichier complet en mémoire, vous offrant à la fois rapidité et flexibilité.

## Prérequis

- Visual Studio (toute version récente) installé.  
- Bibliothèque Aspose.Drawing pour .NET. Vous pouvez la télécharger [ici](https://releases.aspose.com/drawing/net/).  
- Connaissances de base en programmation C#.

## Importer les espaces de noms

Dans votre fichier C#, commencez par importer l’espace de noms nécessaire :

L’espace de noms `Aspose.Drawing` contient tous les types de base tels que `Bitmap`, `Graphics` et `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Étape 1 : Créer un Bitmap (Canvas)

Tout d’abord, créez un bitmap qui servira de toile pour votre dessin. Ce bitmap est l’endroit où la spline sera rendue avant que vous **enregistriez l’image**.

Bitmap représente une image en mémoire avec un format de pixel et des dimensions définis.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Étape 2 : Créer un objet Graphics

Ensuite, obtenez un objet `Graphics` à partir du bitmap. Cet objet fournit la surface de dessin.

Graphics fournit une surface de dessin pour rendre des formes, du texte et des images sur un bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Étape 3 : Définir le Pen et tracer la courbe

Définissez un `Pen` avec la couleur et la largeur souhaitées, puis tracez la spline cardinale en utilisant `DrawCurve`. Cela démontre la technique de **tracer une courbe avec un pen** et sert d’**exemple de spline cardinale**.

Pen encapsule la couleur, la largeur et le style de ligne utilisés pour dessiner des lignes et des courbes.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Étape 4 : Enregistrer l’image (Enregistrer la courbe au format PNG)

Enfin, persistez le bitmap dans un fichier PNG. C’est le cœur de **comment enregistrer un PNG** dans ce tutoriel.

Bitmap.Save écrit l’image dans un fichier au format spécifié, tel que PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Astuce :** Utilisez `Path.Combine` pour construire les chemins de fichiers en toute sécurité sur toutes les plateformes.

Félicitations ! Vous avez tracé avec succès une spline cardinale et enregistré le résultat sous forme d’image PNG en utilisant Aspose.Drawing pour .NET. N’hésitez pas à expérimenter avec différents tableaux de points, couleurs de pen ou largeurs de ligne pour personnaliser vos courbes.

## Cas d’utilisation courants

- **Visualisations de données** – graphiques linéaires lisses nécessitant des points de contrôle précis.  
- **Composants UI personnalisés** – dessin de boutons rotatifs, curseurs ou bordures décoratives.  
- **Graphiques exportables** – générer des ressources PNG à la volée pour des rapports ou du contenu web.

## Dépannage et astuces

- **L’image apparaît vide ?** Assurez‑vous que le format de pixel du bitmap prend en charge l’alpha (`Format32bppPArgb`) et que vous appelez `graphics.Clear(Color.Transparent)` si nécessaire.  
- **Forme de courbe inattendue ?** Ajustez le paramètre de tension en utilisant la surcharge `DrawCurve(pen, points, tension)`.  
- **Erreurs d’accès au fichier ?** Vérifiez que le répertoire cible existe et que votre application dispose des autorisations d’écriture.

## Questions fréquentes

**Q1 : Puis‑je utiliser Aspose.Drawing pour des projets commerciaux ?**  
A1 : Oui, Aspose.Drawing convient aussi bien aux projets personnels qu’aux projets commerciaux. Consultez les détails de licence sur la [page d’achat](https://purchase.aspose.com/buy).

**Q2 : Comment obtenir une licence temporaire pour les tests ?**  
A2 : Obtenez une licence temporaire à des fins de test [ici](https://purchase.aspose.com/temporary-license/).

**Q3 : Où puis‑je trouver un support supplémentaire ?**  
A3 : Visitez le [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pour le support communautaire et les discussions.

**Q4 : Une version d’essai gratuite est‑elle disponible ?**  
A4 : Oui, explorez les fonctionnalités avec la version [essai gratuite](https://releases.aspose.com/) avant d’effectuer un achat.

**Q5 : Comment accéder à la documentation ?**  
A5 : Consultez la [documentation](https://reference.aspose.com/drawing/net/) complète pour des informations détaillées et des exemples.

---

**Dernière mise à jour :** 2026-05-29  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Enregistrer le bitmap en PNG & tracer des courbes fermées avec Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Enregistrer le bitmap C# – tracer des splines de Bézier avec Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Enregistrer le bitmap en PNG avec des pinceaux solides dans Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}