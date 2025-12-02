---
date: 2025-12-02
description: Apprenez à recadrer des images en .NET avec Aspose.Drawing. Ce tutoriel
  de recadrage d’images montre, étape par étape, comment enregistrer l’image recadrée,
  travailler avec les bitmaps et gérer le recadrage d’images en lot.
language: fr
linktitle: How to Crop Image .NET Using Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Comment recadrer une image .NET avec Aspose.Drawing
url: /net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment recadrer une image .NET avec Aspose.Drawing

## Introduction

Si vous développez une application .NET qui nécessite une manipulation précise des images, apprendre **comment recadrer des images** est essentiel. Aspose.Drawing fournit une API riche, entièrement gérée, qui vous permet de **recadrer des images .net** sans dépendre de la bibliothèque plus ancienne System.Drawing.Common. Dans ce tutoriel, vous verrez un exemple complet, de bout en bout, qui vous guide à travers le chargement d’un bitmap, la définition de la zone de recadrage, l’exécution de l’opération, puis **l’enregistrement de l’image recadrée**. À la fin, vous serez prêt à intégrer le recadrage d’images dans n’importe quelle solution .NET—qu’il s’agisse d’une seule image ou d’un **workflow de recadrage d’images en lot**.

## Réponses rapides
- **Quelle bibliothèque dois‑je utiliser ?** Aspose.Drawing pour .NET  
- **Puis‑je recadrer n’importe quel format d’image ?** Oui—la plupart des formats courants (PNG, JPEG, BMP, etc.) sont pris en charge.  
- **Ai‑je besoin d’une licence ?** Une version d’essai gratuite suffit pour le développement ; une licence est requise en production.  
- **Le traitement par lots est‑il possible ?** Absolument—bouclez le même code sur une collection de fichiers.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Qu’est‑ce que le “crop image .net” ?

Recadrer une image signifie extraire une région rectangulaire d’une image plus grande. En .NET, cette opération est généralement effectuée sur un objet `Bitmap`. Aspose.Drawing simplifie le processus en fournissant des primitives graphiques haute performance qui fonctionnent de manière cohérente sur toutes les plateformes.

## Pourquoi utiliser Aspose.Drawing pour le recadrage d’images ?

- **Fiabilité multiplateforme** – Aucun dépendance native, fonctionne sous Windows, Linux et macOS.  
- **Prise en charge riche des formats de pixels** – Gère le ARGB 32 bits, PArgb, et de nombreux autres formats.  
- **Optimisé pour la performance** – Dessin et interpolation optimisés pour les images volumineuses.  
- **Intégration transparente** – Fonctionne de pair avec les autres produits Aspose pour PDF, Slides, etc.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Bibliothèque Aspose.Drawing** – Ajoutez le package NuGet `Aspose.Drawing` à votre projet ou téléchargez‑le depuis le [site officiel](https://releases.aspose.com/drawing/net/).  
- **Dossier d’images** – Un répertoire contenant les images sources que vous souhaitez recadrer. Remplacez `"Your Document Directory"` dans les extraits de code par le chemin réel sur votre machine.

## Importer les espaces de noms

Tout d’abord, importez l’espace de noms qui contient les classes de dessin :

```csharp
using System.Drawing;
```

Cela vous donne accès à `Bitmap`, `Graphics`, `Rectangle` et aux autres types essentiels.

## Guide étape par étape

### Étape 1 : Créer un canvas Bitmap (crop image bitmap)

Nous commençons par créer un bitmap vierge qui contiendra le résultat recadré. Ajustez la largeur, la hauteur et le format de pixel pour correspondre à la taille de la région que vous prévoyez d’extraire.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Astuce :** Le format `Format32bppPArgb` préserve la transparence alpha et offre un rendu de haute qualité.

### Étape 2 : Créer un objet Graphics

Un objet `Graphics` nous permet de dessiner sur le canvas bitmap. Le réglage de `InterpolationMode` influence la façon dont l’image est rééchantillonnée pendant le recadrage.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

> **Pro tip :** Pour des résultats plus lisses sur les images redimensionnées, envisagez `InterpolationMode.HighQualityBicubic`.

### Étape 3 : Charger l’image source

Chargez l’image que vous souhaitez recadrer. Le chemin combine votre répertoire de documents avec le nom du fichier.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

> **Remarque :** Aspose.Drawing peut lire directement les formats PNG, JPEG, BMP, GIF, TIFF, et bien d’autres.

### Étape 4 : Définir les rectangles source et destination

Le `sourceRectangle` sélectionne la partie de l’image originale à conserver. Ici, nous prenons la zone de 50 × 40 pixels en haut à gauche. Le `destinationRectangle` indique au moteur graphique où placer la région recadrée sur le nouveau bitmap.

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

> **Pourquoi deux rectangles ?** Utiliser des rectangles identiques réalise un simple recadrage. Vous pouvez modifier `destinationRectangle` pour repositionner ou redimensionner la partie recadrée.

### Étape 5 : Effectuer l’opération de recadrage

La méthode `DrawImage` copie la région sélectionnée de l’image source dans le bitmap de destination.

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

> **Erreur fréquente :** Oublier de libérer le `Graphics` peut verrouiller le fichier bitmap. Nous gérerons la libération automatiquement à la fin de la méthode.

### Étape 6 : Enregistrer l’image recadrée (save cropped image)

Enfin, écrivez le résultat sur le disque. Modifiez le nom de fichier et le chemin selon vos besoins.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

> **Résultat :** Vous disposez maintenant d’un nouveau fichier PNG qui ne contient que la région de 50 × 40 pixels que vous avez spécifiée.

## Problèmes courants & solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Fichier de sortie vide** | Rectangle source hors des limites de l’image | Vérifiez les coordonnées et la taille de `sourceRectangle`. |
| **Exception out‑of‑memory** | Images sources très volumineuses | Traitez les images par morceaux ou utilisez des instructions `using` pour libérer rapidement les ressources. |
| **Couleurs incorrectes** | Format de pixel non correspondant | Faites correspondre le format de pixel du bitmap source ou convertissez avec `Bitmap.Clone`. |

## Questions fréquentes

**Q : Puis‑je recadrer des images de n’importe quel format avec Aspose.Drawing ?**  
R : Oui, Aspose.Drawing prend en charge PNG, JPEG, BMP, GIF, TIFF, et bien d’autres formats, vous pouvez donc **how to crop image** quels que soient leurs types d’origine.

**Q : Existe‑t‑il des options de recadrage avancées ?**  
R : Absolument. Vous pouvez combiner `GraphicsPath` pour des découpes non rectangulaires, appliquer une rotation, ou utiliser `ImageAttributes` pour des ajustements de couleur.

**Q : Puis‑je appliquer plusieurs opérations de recadrage à une même image ?**  
R : Oui—répétez simplement l’appel `DrawImage` avec différents rectangles source, ou enchaînez‑les dans une boucle pour des transformations complexes.

**Q : Aspose.Drawing convient‑il au recadrage d’images en lot ?**  
R : En effet. Enveloppez les étapes ci‑dessus dans une boucle `foreach` parcourant une collection de chemins de fichiers pour traiter automatiquement des dizaines ou des centaines d’images.

**Q : Comment obtenir du support pour les questions liées à Aspose.Drawing ?**  
R : Visitez le [forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17) pour poser des questions, partager du code et obtenir de l’aide de la communauté et des ingénieurs produit.

## Conclusion

Dans ce tutoriel, nous avons démontré un workflow complet **crop image .net** avec Aspose.Drawing. Vous savez maintenant **how to crop image**, définir des rectangles source précis, et **save cropped image**. Avec ces bases, vous pouvez étendre le code pour gérer le **batch image cropping**, appliquer des transformations personnalisées, ou intégrer la logique dans des pipelines de traitement d’images plus larges.

---  

**Dernière mise à jour :** 2025-12-02  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}