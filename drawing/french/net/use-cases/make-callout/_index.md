---
title: Faire des légendes dans Aspose.Drawing
linktitle: Faire des légendes dans Aspose.Drawing
second_title: API Aspose.Drawing .NET - Alternative à System.Drawing.Common
description: Améliorez les illustrations de vos documents à l'aide d'Aspose.Drawing pour .NET ! Apprenez étape par étape comment ajouter des légendes pour des visuels plus clairs et informatifs.
weight: 10
url: /fr/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Faire des légendes dans Aspose.Drawing

## Introduction
Bienvenue dans notre guide étape par étape sur la création de légendes dans Aspose.Drawing pour .NET ! Si vous souhaitez améliorer les illustrations de vos documents avec des légendes, vous êtes au bon endroit. Dans ce didacticiel, nous décomposerons le processus en étapes gérables à l'aide de la bibliothèque Aspose.Drawing.
## Conditions préalables
Avant de plonger dans le didacticiel, assurez-vous d'avoir les prérequis suivants :
- Connaissance de base du langage de programmation C#.
-  Bibliothèque Aspose.Drawing installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/drawing/net/).
- Un document ou une image dans lequel vous souhaitez ajouter des légendes.
## Importer des espaces de noms
Assurez-vous que les espaces de noms nécessaires sont inclus dans votre projet :
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Étape 1 : Charger l'image
 Commencez par charger l’image à l’endroit où vous souhaitez ajouter des légendes. Remplacer`"Your Document Directory"` et`"gears.png"` avec votre répertoire actuel et le nom de fichier image.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Votre code ici
}
```
## Étape 2 : Créer un objet graphique
 Créer un`Graphics` objet de l’image pour effectuer des opérations de dessin.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Étape 3 : Définir les positions des légendes
Définissez les points de début et de fin de chaque légende ainsi que la valeur et l'unité de la légende.
```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```
## Étape 4 : dessiner des légendes
 Mettre en œuvre le`DrawCallOut` méthode pour dessiner des légendes sur l’image.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Étape 5 : Enregistrez l'image
Enregistrez l'image avec les légendes dans le répertoire de votre choix.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Dessiner le code source de la légende
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```
## Conclusion

Toutes nos félicitations! Vous avez ajouté avec succès des légendes à votre image à l'aide d'Aspose.Drawing pour .NET. N'hésitez pas à expérimenter différentes positions et valeurs pour personnaliser davantage vos légendes.

## FAQ

### Puis-je utiliser Aspose.Drawing pour d’autres types d’illustrations ?

Oui, Aspose.Drawing prend en charge un large éventail d’opérations de dessin pour différents types d’illustrations.

### Aspose.Drawing est-il compatible avec différents formats d’image ?

Absolument! Aspose.Drawing prend en charge les formats d'image populaires tels que PNG, JPEG, GIF, etc.

### Où puis-je trouver plus d’exemples et de documentation ?

 Explorez la documentation complète[ici](https://reference.aspose.com/drawing/net/).

### Comment puis-je obtenir de l'aide si je rencontre des problèmes ?

 Visiter le[Forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17) pour le soutien de la communauté.

### Puis-je essayer Aspose.Drawing avant d’acheter ?

 Certainement! Commencez avec un essai gratuit[ici](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
