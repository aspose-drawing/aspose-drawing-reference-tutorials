---
date: 2026-02-27
description: Apprenez à créer une image de carte d'anniversaire avec Aspose.Drawing
  pour .NET. Ce guide vous montre comment dessiner du texte sur une image, superposer
  du texte sur une photo et ajouter rapidement une légende à la photo.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Comment créer une image de carte d'anniversaire avec Aspose.Drawing
url: /fr/net/use-cases/text-on-image/
weight: 12
---

 produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer une image de carte d'anniversaire avec Aspose.Drawing

## Introduction
Dans le monde dynamique du développement .NET, Aspose.Drawing se démarque comme un outil puissant pour manipuler les images avec facilité. Que vous ayez besoin de **créer une image de carte d'anniversaire**, d'ajouter un filigrane ou simplement de superposer du texte sur une photo, ce tutoriel vous guide pas à pas pour dessiner du texte sur une image en C#. À la fin de ce guide, vous disposerez d'une carte d'anniversaire personnalisée prête à être partagée.

## Réponses rapides
- **Quelle bibliothèque dois‑je utiliser ?** Aspose.Drawing for .NET  
- **Puis‑je ajouter une légende à la photo ?** Oui – utilisez `Graphics.DrawString` avec des polices personnalisées.  
- **Une licence est‑elle requise pour la production ?** Oui, une licence commerciale est nécessaire.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Combien de temps prend l'implémentation ?** Généralement moins de 10 minutes pour une carte simple.

## Qu’est‑ce qu’une image de carte d’anniversaire ?
Une image de carte d’anniversaire est une photo personnalisée qui combine une image de fond avec du texte sur mesure — tel qu’un message de vœux, le nom du destinataire ou un texte festif. Avec Aspose.Drawing, vous pouvez générer ces cartes de façon programmatique sans recourir à des outils de conception graphique manuels.

## Pourquoi utiliser Aspose.Drawing pour superposer du texte sur une image ?
- **Prise en charge multiplateforme :** Fonctionne sous Windows, Linux et macOS.  
- **API de dessin riche :** Contrôle complet des polices, des couleurs et de la mise en page.  
- **Aucune dépendance externe :** Remplace `System.Drawing.Common` par une bibliothèque entièrement gérée.  
- **Haute performance :** Optimisé pour le traitement d’images en masse.

## Prérequis
Avant de plonger dans le tutoriel, assurez‑vous d’avoir les éléments suivants :

1. Bibliothèque Aspose.Drawing : Téléchargez et installez la bibliothèque Aspose.Drawing depuis la [documentation Aspose.Drawing pour .NET](https://reference.aspose.com/drawing/net/).  
2. Environnement de développement : Un environnement de développement .NET fonctionnel, tel que Visual Studio ou Visual Studio Code, avec le SDK .NET 6 ou ultérieur installé.

Maintenant, parcourons le guide étape par étape pour ajouter du texte à une image et l’enregistrer comme une carte d’anniversaire.

## Importer les espaces de noms
Commencez par importer les espaces de noms nécessaires dans votre projet C# :

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## Étape 1 : Charger l’image
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Ici, nous chargeons l’image depuis le chemin de fichier spécifié et initialisons l’objet Graphics pour le traitement ultérieur.

## Étape 2 : Définir les propriétés du texte
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Définissez les propriétés du texte telles que la couleur, la police et le remplissage. Ajustez ces paramètres selon vos préférences de conception.

## Étape 3 : Mesurer la taille du texte
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
Calculez la taille requise du texte en mesurant chaque mot individuellement. Cela garantit un placement correct et évite le chevauchement du texte.

## Étape 4 : Dessiner le texte sur l’image
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Maintenant, positionnez le texte sur l’image en fonction de la taille calculée et dessinez‑le en utilisant la police et la couleur spécifiées.

## Étape 5 : Enregistrer l’image
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Enregistrez l’image modifiée dans le répertoire de votre choix. Le fichier résultant est une image de carte d’anniversaire prête à être envoyée.

## Cas d’utilisation courants et conseils
- **Ajouter une légende à la photo :** Remplacez `text` par la légende souhaitée, par exemple « Celebrating 30 Years! ».  
- **Dessiner du texte sur un bitmap :** La même approche fonctionne pour les objets `Bitmap` créés à partir de zéro.  
- **Superposer plusieurs lignes :** Parcourez un tableau de chaînes et ajustez la coordonnée Y du `Rectangle` pour chaque ligne.  
- **Astuce pro :** Utilisez `Graphics.SmoothingMode = SmoothingMode.AntiAlias` pour un rendu du texte encore plus lisse.

## Conclusion
Aspose.Drawing simplifie les tâches de manipulation d’images dans .NET, offrant aux développeurs une boîte à outils robuste. Ajouter du texte aux images—que ce soit pour **créer une image de carte d’anniversaire**, **draw string on image**, ou **add caption to photo**—n’est qu’un exemple de sa polyvalence dans la gestion des éléments graphiques.

## Questions fréquentes
### Aspose.Drawing est‑il compatible avec tous les formats d’image ?
Aspose.Drawing prend en charge un large éventail de formats d’image, y compris les plus populaires comme JPEG, PNG et GIF. Consultez la [documentation](https://reference.aspose.com/drawing/net/) pour la liste complète.

### Puis‑je utiliser Aspose.Drawing pour des projets commerciaux ?
Oui, Aspose.Drawing convient à la fois aux projets personnels et commerciaux. Pour les détails de licence, consultez la [page d’achat](https://purchase.aspose.com/buy).

### Des licences temporaires sont‑elles disponibles à des fins de test ?
Oui, vous pouvez obtenir une licence temporaire pour les tests en visitant [Licence temporaire](https://purchase.aspose.com/temporary-license/).

### Où puis‑je trouver du support communautaire pour Aspose.Drawing ?
Rejoignez la communauté et obtenez du support sur le [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

### Comment démarrer avec Aspose.Drawing ?
Commencez par télécharger la bibliothèque depuis [ici](https://releases.aspose.com/drawing/net/) et explorez la [documentation](https://reference.aspose.com/drawing/net/) complète.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-02-27  
**Testé avec :** Aspose.Drawing 24.11 for .NET  
**Auteur :** Aspose