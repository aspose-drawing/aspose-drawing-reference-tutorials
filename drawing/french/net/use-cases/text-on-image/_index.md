---
title: Ajout de texte sur les images dans Aspose.Drawing
linktitle: Ajout de texte sur les images dans Aspose.Drawing
second_title: API Aspose.Drawing .NET - Alternative à System.Drawing.Common
description: Explorez l'intégration transparente du texte dans les images avec Aspose.Drawing pour .NET. Suivez notre guide étape par étape pour une manipulation d'image sans effort. Télécharger maintenant!
weight: 12
url: /fr/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajout de texte sur les images dans Aspose.Drawing

## Introduction
Dans le monde dynamique du développement .NET, Aspose.Drawing s'impose comme un outil puissant pour manipuler facilement les images. L'ajout de texte aux images est une exigence courante, qu'il s'agisse de filigrane, d'annotations ou de création de graphiques personnalisés. Dans ce didacticiel, nous explorerons comment exploiter Aspose.Drawing pour intégrer de manière transparente du texte dans vos images à l'aide de C#.
## Conditions préalables
Avant de plonger dans le didacticiel, assurez-vous d'avoir mis en place les éléments suivants :
1.  Bibliothèque Aspose.Drawing : téléchargez et installez la bibliothèque Aspose.Drawing à partir du[Documentation Aspose.Drawing pour .NET](https://reference.aspose.com/drawing/net/).
2. Environnement de développement : disposer d'un environnement de développement .NET fonctionnel, comprenant Visual Studio ou tout autre IDE compatible.
Commençons maintenant par le guide étape par étape.
## Importer des espaces de noms
Commencez par importer les espaces de noms nécessaires dans votre projet C# :
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## Étape 1 : Charger l'image
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Ici, nous chargeons l'image à partir du chemin de fichier spécifié et initialisons l'objet graphique pour un traitement ultérieur.
## Étape 2 : définir les propriétés du texte
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Définissez les propriétés du texte telles que la couleur, la police et le remplissage. Ajustez ces paramètres selon vos préférences.
## Étape 3 : Mesurer la taille du texte
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Calculez la taille requise pour le texte en mesurant chaque mot individuellement. Cela garantit un placement correct et évite le chevauchement du texte.
## Étape 4 : dessiner du texte sur l'image
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Maintenant, positionnez le texte sur l'image en fonction de la taille calculée et dessinez-le en utilisant la police et la couleur spécifiées.
## Étape 5 : Enregistrez l'image
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Enregistrez l'image modifiée dans le répertoire de votre choix.
Ce guide étape par étape montre un processus simple d'ajout de texte aux images à l'aide d'Aspose.Drawing pour .NET. Expérimentez avec différentes polices, couleurs et contenus de texte pour obtenir l'effet visuel souhaité.
## Conclusion
Aspose.Drawing simplifie les tâches de manipulation d'images dans .NET, fournissant aux développeurs une boîte à outils robuste. L'ajout de texte aux images n'est qu'un exemple de ses capacités, démontrant la polyvalence de la bibliothèque dans la gestion des éléments graphiques.
## Questions fréquemment posées
### Aspose.Drawing est-il compatible avec tous les formats d’image ?
 Aspose.Drawing prend en charge un large éventail de formats d'image, y compris les formats populaires tels que JPEG, PNG et GIF. Se référer au[Documentation](https://reference.aspose.com/drawing/net/) pour une liste complète.
### Puis-je utiliser Aspose.Drawing pour des projets commerciaux ?
Oui, Aspose.Drawing convient aux projets personnels et commerciaux. Pour plus de détails sur les licences, visitez le[page d'achat](https://purchase.aspose.com/buy).
### Des licences temporaires sont-elles disponibles à des fins de test ?
 Oui, vous pouvez obtenir une licence temporaire pour tester en visitant[Permis temporaire](https://purchase.aspose.com/temporary-license/).
### Où puis-je trouver le soutien de la communauté pour Aspose.Drawing ?
 Engagez-vous avec la communauté et obtenez du soutien sur le[Forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17).
### Comment démarrer avec Aspose.Drawing ?
 Commencez par télécharger la bibliothèque depuis[ici](https://releases.aspose.com/drawing/net/) et explorez l'ensemble[Documentation](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
