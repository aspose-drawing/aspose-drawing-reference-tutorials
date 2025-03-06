---
title: Unités de mesure dans Aspose.Drawing pour .NET
linktitle: Unités de mesure dans Aspose.Drawing
second_title: API Aspose.Drawing .NET - Alternative à System.Drawing.Common
description: Explorez la polyvalence d'Aspose.Drawing pour .NET dans ce didacticiel approfondi, maîtrisant les unités de mesure pour les graphiques de précision.
weight: 14
url: /fr/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unités de mesure dans Aspose.Drawing pour .NET

## Introduction

Bienvenue dans le monde d'Aspose.Drawing pour .NET, où précision et flexibilité se rencontrent dans la manipulation graphique. Dans ce didacticiel, nous approfondirons les subtilités des unités de mesure dans Aspose.Drawing, en vous fournissant un guide étape par étape pour exploiter la puissance de cette bibliothèque remarquable.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.Drawing pour .NET : assurez-vous que la bibliothèque est installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/drawing/net/).

- Répertoire de documents : disposez d'un répertoire désigné dans lequel vous souhaitez enregistrer vos documents créés.

- Connaissances de base de C# : une compréhension fondamentale de C# est recommandée pour tirer le meilleur parti de ce guide.

## Importer des espaces de noms

Avant de commencer, importons les espaces de noms nécessaires pour utiliser efficacement Aspose.Drawing :

```csharp
using System.Drawing;
```

Maintenant, décomposons chaque exemple en plusieurs étapes :

## Points comme unités de mesure

1. Créer un bitmap : initialisez un bitmap avec une largeur et une hauteur spécifiées.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Créer des graphiques : générez un objet graphique à partir du bitmap pour dessiner dessus.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Définir l'unité de page sur points : définissez les points comme unité de mesure (1 point = 1/72 de pouce).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Dessiner un rectangle : dessinez un rectangle en utilisant des points comme unité.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Millimètres comme unités de mesure

1. Définir l'unité de page sur millimètres : modifiez l'unité de mesure en millimètres (1 mm = 1/25,4 pouce).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Dessiner un rectangle en millimètres : dessinez un autre rectangle en utilisant les millimètres comme unité.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Pouces comme unités de mesure

1. Définir l’unité de page sur pouces : changez l’unité de mesure en pouces.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Dessiner un rectangle en pouces : dessinez un rectangle en utilisant les pouces comme unité.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Enregistrez le résultat

Après avoir terminé les exemples, enregistrez l'image résultante dans votre répertoire de documents :

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Vous avez désormais parcouru avec succès les différentes unités de mesure dans Aspose.Drawing pour .NET, créant ainsi une représentation visuelle de rectangles à l'aide de points, de millimètres et de pouces.

## Conclusion

Dans ce didacticiel, nous avons exploré comment Aspose.Drawing for .NET gère différentes unités de mesure. En manipulant des points, des millimètres et des pouces, vous pouvez obtenir précision et adaptabilité dans vos créations graphiques. Expérimentez avec ces concepts pour libérer tout le potentiel d’Aspose.Drawing.

## FAQ

### Q1 : Puis-je utiliser Aspose.Drawing pour .NET avec d’autres frameworks .NET ?

A1 : Oui, Aspose.Drawing est compatible avec divers frameworks .NET, offrant ainsi une flexibilité dans votre environnement de développement.

### Q2 : Existe-t-il un essai gratuit ?

 A2 : Oui, vous pouvez explorer Aspose.Drawing avec un essai gratuit[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir une assistance pour Aspose.Drawing pour .NET ?

 A3 : Visitez le[Forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17) pour le soutien et les discussions de la communauté.

### Q4 : Puis-je acheter une licence temporaire pour des projets à court terme ?

 A4 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je trouver une documentation détaillée pour Aspose.Drawing ?

 A5 : La documentation complète est disponible[ici](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
