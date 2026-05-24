---
date: 2026-05-24
description: Apprenez à définir l'unité dans Aspose.Drawing pour .NET, à convertir
  facilement les unités graphiques et à maîtriser les mesures précises pour le rendu
  graphique.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Unités de mesure dans Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Comment définir l'unité dans Aspose.Drawing pour .NET – Unités de mesure
url: /fr/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment définir l'unité dans Aspose.Drawing pour .NET – Unités de mesure

## Introduction

Bienvenue dans le monde d'Aspose.Drawing pour .NET, où précision et flexibilité se rencontrent dans la manipulation graphique. Dans ce tutoriel, vous découvrirez **comment définir l'unité** pour vos dessins, apprendrez à **convertir les unités graphiques** entre points, millimètres et pouces, et verrez des exemples concrets qui rendent vos images pixel‑parfaites. Que vous créiez des rapports, des vignettes ou des graphiques personnalisés, maîtriser les unités de mesure est essentiel pour un rendu cohérent sur tous les appareils.

## Réponses rapides
- **Quelle est la façon principale de changer les unités ?** Appelez `graphics.PageUnit = PageUnit.Point` (ou `.Millimeter`, `.Inch`) sur l'objet `Graphics`.  
- **Quelle unité équivaut à 1/72 pouce ?** Points.  
- **Combien de millimètres y a‑t‑il dans un pouce ?** 25,4 mm = 1 pouce.  
- **Ai‑je besoin de bibliothèques supplémentaires pour utiliser les unités ?** Non, la bibliothèque principale d'Aspose.Drawing fournit toutes les constantes d'unités.  
- **Puis‑je mélanger des unités dans une même image ?** Définissez l'unité une fois par instance `Graphics` ; dessinez tout en utilisant cette unité pour garantir la cohérence.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous d'avoir les prérequis suivants en place :

- Aspose.Drawing pour .NET : assurez‑vous que la bibliothèque est installée. Vous pouvez la télécharger [ici](https://releases.aspose.com/drawing/net/).
- Répertoire de documents : disposez d'un répertoire désigné où vous souhaitez enregistrer vos documents créés.
- Connaissances de base en C# : une compréhension fondamentale du C# est recommandée pour tirer le meilleur parti de ce guide.

## Importer les espaces de noms

Avant de commencer, importons les espaces de noms nécessaires pour utiliser efficacement Aspose.Drawing :

```csharp
using System.Drawing;
```

Maintenant, détaillons chaque exemple en plusieurs étapes :

## Comment définir l'unité en points ?

La classe `Bitmap` représente une image en mémoire qui sert de canevas de dessin. Chargez votre bitmap, créez un objet `Graphics` et définissez l'unité de page sur les points — cela indique à Aspose.Drawing d'interpréter toutes les coordonnées comme des valeurs de 1/72 pouce. Utiliser les points vous donne un contrôle fin pour les graphiques prêts à imprimer et vous permet de spécifier les épaisseurs de ligne avec une grande précision.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Étape 1 : Créer un Bitmap  
La classe `Bitmap` représente une image en mémoire qui sert de canevas de dessin.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Étape 2 : Créer un objet Graphics  
`Graphics` fournit des méthodes de dessin pour rendre des formes et du texte sur un `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Étape 3 : Définir l'unité de page sur les points  
`PageUnit` est une énumération qui spécifie l'unité de mesure pour les coordonnées de la page. `PageUnit.Point` définit les points comme unité de mesure (1 point = 1/72 pouce). Ce réglage s'applique à tous les appels de dessin ultérieurs.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Étape 4 : Dessiner un rectangle en points  
Lorsque vous dessinez un rectangle après avoir défini l'unité, les dimensions que vous spécifiez sont interprétées en points, garantissant une taille précise.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Comment définir l'unité en millimètres ?

`PageUnit` est une énumération qui spécifie l'unité de mesure pour les coordonnées de la page. Passer aux millimètres est utile lorsque vous avez besoin de dimensions métriques, par exemple lors de la génération de schémas d'ingénierie. Aspose.Drawing considère 1 mm comme 1/25,4 pouce, vous permettant d'aligner les graphiques avec les mesures physiques utilisées dans la fabrication et la documentation technique.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Étape 1 : Définir l'unité de page sur les millimètres  
Attribuez `PageUnit.Millimeter` à l'objet `Graphics` ; toutes les coordonnées sont désormais mappées au système métrique.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Étape 2 : Dessiner un rectangle en millimètres  
La largeur et la hauteur du rectangle sont maintenant exprimées en millimètres, ce qui facilite l'alignement avec les mesures physiques et garantit que la sortie imprimée correspond aux tailles réelles.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Comment définir l'unité en pouces ?

`Graphics` fournit des méthodes de dessin pour rendre des formes et du texte sur un `Bitmap`. Les pouces sont l'unité par défaut pour de nombreux outils de conception basés aux États‑Unis. Définir l'unité en pouces vous permet de penser en termes familiers lors de la mise en page d'éléments d'interface, et simplifie la transition du design d'écran à l'impression où les pouces sont couramment utilisés.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Étape 1 : Définir l'unité de page sur les pouces  
`PageUnit.Inch` modifie le système de coordonnées de sorte que 1 unité équivaut à 1 pouce, offrant une façon simple de dimensionner les éléments pour des mises en page orientées impression.

CODE_BLOCK_PLACEHOLDER_10_END

### Étape 2 : Dessiner un rectangle en pouces  
Désormais, toute forme que vous dessinez utilise les pouces comme base de mesure, ce qui est idéal pour les mises en page d'impression et pour communiquer les dimensions aux parties prenantes habituées aux unités impériales.

CODE_BLOCK_PLACEHOLDER_11_END

## Enregistrer le résultat

Après avoir terminé les exemples, enregistrez l'image résultante dans votre répertoire de documents. La méthode `Bitmap.Save` écrit le fichier dans le format que vous spécifiez (PNG, JPEG, etc.).

CODE_BLOCK_PLACEHOLDER_12_END

Vous avez maintenant parcouru avec succès les différentes unités de mesure dans Aspose.Drawing pour .NET, créant une représentation visuelle de rectangles en utilisant les points, les millimètres et les pouces.

## Pourquoi utiliser le système d'unités d'Aspose.Drawing ?

Aspose.Drawing prend en charge **plus de 30 formats d'image** et peut traiter des images jusqu'à **5000 × 5000 pixels** sans charger le fichier complet en mémoire, offrant des performances élevées pour la génération de graphiques à grande échelle. En définissant explicitement l'unité, vous éliminez les approximations, réduisez les erreurs de conversion et assurez que votre sortie correspond aux dimensions physiques exactes sur toutes les plateformes.

## Problèmes courants et solutions

- **Taille inattendue après l'enregistrement** – Vérifiez que vous avez défini `graphics.PageUnit` **avant** tout appel de dessin ; changer l'unité plus tard ne redimensionne pas rétroactivement les formes existantes.  
- **Sortie floue sur des écrans haute DPI** – Augmentez la résolution du bitmap (par ex., `new Bitmap(width, height, 300)`) pour correspondre à la DPI cible.  
- **Unités mixtes dans une même image** – Créez des instances `Graphics` séparées pour chaque unité ou effectuez une conversion manuelle avant le dessin.

## Questions fréquentes

### Q1: Puis‑je utiliser Aspose.Drawing pour .NET avec d'autres frameworks .NET ?
A1: Oui, Aspose.Drawing est compatible avec divers frameworks .NET, offrant une flexibilité dans votre environnement de développement.

### Q2: Existe-t-il une version d'essai gratuite ?
A2: Oui, vous pouvez explorer Aspose.Drawing avec une version d'essai gratuite [ici](https://releases.aspose.com/).

### Q3: Comment obtenir du support pour Aspose.Drawing pour .NET ?
A3: Visitez le [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pour le support communautaire et les discussions.

### Q4: Puis‑je acheter une licence temporaire pour des projets à court terme ?
A4: Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q5: Où puis‑je trouver la documentation détaillée d'Aspose.Drawing ?
A5: La documentation complète est disponible [ici](https://reference.aspose.com/drawing/net/).

---

**Last Updated:** 2026-05-24  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Transformation du système de coordonnées – Transformation de page dans Aspose.Drawing pour .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Tutoriel de transformation matricielle : Transformations matricielles dans Aspose.Drawing pour .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Comment appliquer une transformation : Transformation locale dans Aspose.Drawing pour .NET](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}