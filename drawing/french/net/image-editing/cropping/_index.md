---
date: 2026-10-13
description: Apprenez à recadrer en lot des images en PNG en utilisant l'API Aspose.Drawing,
  l'alternative multiplateforme à System.Drawing pour les développeurs .NET.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: Tutoriel de recadrage d'images – Aspose.Drawing
og_description: Apprenez à recadrer rapidement des images en PNG en lot avec Aspose.Drawing,
  l'alternative multiplateforme à System.Drawing pour les développeurs .NET. Suivez
  les instructions étape par étape pour traiter plusieurs fichiers efficacement.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Comment recadrer en lot des images en PNG avec Aspose.Drawing pour .NET
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Comment recadrer en lot des images en PNG avec Aspose.Drawing pour .NET
url: /fr/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment recadrer en lot des images en PNG avec Aspose.Drawing pour .NET

Si vous devez **crop image to PNG** rapidement, de manière fiable et à grande échelle dans un environnement .NET, vous êtes au bon endroit. Dans ce tutoriel, nous passerons en revue les étapes exactes pour charger une image, définir la zone de recadrage et enregistrer le résultat sous forme de fichier PNG — le tout en utilisant Aspose.Drawing, une **alternative à System.Drawing** moderne qui fonctionne sur plusieurs plates‑formes. Vous verrez également comment étendre le flux d’une seule image en un pipeline complet de **recadrage en lot**.

## Réponses rapides
- **Quelle bibliothèque devrais-je utiliser ?** Aspose.Drawing for .NET (une alternative complète à System.Drawing.Common)  
- **Combien de temps prend le recadrage de base ?** Généralement moins d'une seconde pour une image unique sur un CPU moderne  
- **Puis-je recadrer en PNG ?** Oui – enregistrez le bitmap recadré sous forme de fichier PNG (voir Step 6)  
- **Ai-je besoin d'une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production  
- **Le traitement par lots est‑il possible ?** Absolument – encapsulez les mêmes étapes dans une boucle pour traiter plusieurs fichiers en quelques secondes  

## Comment recadrer en lot des images en PNG ?

Chargez chaque fichier source avec `new Bitmap(path)`, créez un `Bitmap` vierge correspondant à la zone de recadrage, dessinez le rectangle sélectionné à l'aide de `Graphics.DrawImage`, puis appelez `Save("output.png", ImageFormat.Png)`. Enveloppez ces six lignes dans une boucle `foreach` qui parcourt un répertoire et vous obtenez une solution complète de recadrage en lot qui traite des dizaines d'images en quelques secondes.

## Pourquoi utiliser Aspose.Drawing pour le recadrage en lot ?

Aspose.Drawing fonctionne sur **Windows, Linux et macOS**, traite des images de **plus de 500 pixels en moins de 0,5 seconde** sur un CPU de type serveur typique, et prend en charge **plus de 50 formats d'image** avec une préservation complète du canal alpha. Comme il élimine les dépendances natives GDI+, vous pouvez déployer le même code dans des conteneurs, Azure App Service ou AWS Lambda sans bibliothèques supplémentaires, ce qui le rend idéal pour les pipelines d'images à grande échelle.

## Qu’est‑ce que « crop image to PNG » ?

L'opération `crop image to PNG` extrait une région rectangulaire d'un bitmap source et écrit cette région dans un fichier PNG. PNG préserve tout canal alpha, offrant une compression sans perte, ce qui rend l'image résultante idéale pour les miniatures, icônes, actifs UI, ou toute situation où la qualité et la transparence sont requises.

## Pourquoi Aspose.Drawing est‑il une alternative à System.Drawing ?

Aspose.Drawing sert de remplacement direct à System.Drawing en offrant une compatibilité multiplateforme complète, éliminant le besoin de bibliothèques natives GDI+. Il prend en charge un large éventail de formats de pixels, offre une manipulation d'image haute performance et inclut des fonctionnalités avancées telles que la gestion du canal alpha et un support étendu des formats, le rendant adapté tant aux éditions simples qu'au traitement par lots à grande échelle.

## Prérequis

Avant de commencer, assurez‑vous d'avoir :

- **Bibliothèque Aspose.Drawing** intégrée à votre projet .NET. Vous pouvez la télécharger depuis la [page de téléchargement d'Aspose.Drawing](https://releases.aspose.com/drawing/net/).  
- Un dossier contenant les images sources que vous souhaitez recadrer. Remplacez `"Your Document Directory"` dans les extraits de code par le chemin réel sur votre machine.

## Importer les espaces de noms

L'espace de noms `System.Drawing` nous donne accès à `Bitmap`, `Graphics` et aux types associés que Aspose.Drawing étend.

```csharp
using System.Drawing;
```

## Guide étape par étape

### Étape 1 : Créer un canevas bitmap

`Bitmap` est la représentation en mémoire d'une image par Aspose.Drawing, offrant un accès pixel par pixel et le contrôle du format.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Nous commençons avec un canevas vierge dimensionné pour contenir le résultat recadré. Ajustez la largeur et la hauteur pour correspondre aux dimensions de la zone que vous prévoyez d'extraire.

### Étape 2 : Créer un objet graphics

`Graphics` est la surface de dessin qui vous permet de rendre des formes, du texte ou d'autres images sur un Bitmap.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Un objet `Graphics` nous permet de dessiner sur le canevas. Le `InterpolationMode` contrôle la façon dont les valeurs de pixels sont calculées lors du redimensionnement ou de la transformation — `NearestNeighbor` fonctionne bien pour les bords nets.

### Étape 3 : Charger l'image à recadrer

`Image` (ou `Bitmap`) charge le fichier source en mémoire, prêt pour la manipulation.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Chargez l'image source. Assurez‑vous que le chemin pointe vers un fichier existant ; sinon une exception sera levée.

### Étape 4 : Définir les rectangles source et destination

Les objets `Rectangle` décrivent la région de l'image source à conserver et où elle doit être placée sur le canevas de destination.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` indique à l'API quelle partie de l'image originale conserver. Ici nous sélectionnons la zone de 50 × 40 pixels en haut à gauche. En assignant le même rectangle à `destinationRectangle`, nous conservons la région recadrée à sa taille originale.

### Étape 5 : Effectuer l'opération de recadrage

`Graphics.DrawImage` copie la portion définie de `image` sur notre `bitmap` vierge.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

Ceci est l'opération principale **crop image to PNG**. La méthode respecte le rectangle source et n'écrit que les pixels sélectionnés dans le bitmap de destination.

### Étape 6 : Enregistrer l'image recadrée (crop image to PNG)

`Bitmap.Save` écrit le bitmap en mémoire dans un fichier en utilisant le format spécifié.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Enfin, écrivez le canevas sur le disque sous forme de fichier PNG. PNG préserve tout canal alpha et offre une qualité sans perte — idéal pour les actifs UI.

## Comment recadrer en lot des images dans une boucle ?

Itérez sur chaque chemin de fichier avec `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, répétez les Étapes 1‑6 à l'intérieur de la boucle, et stockez chaque résultat dans un dossier cible. Ce modèle s'échelonne linéairement, peut être parallélisé avec `Parallel.ForEach` pour un débit encore plus rapide, et traite les images de manière efficace et rapide.

## Pièges courants et conseils

- **Incompatibilités de format de pixel** – assurez‑vous que l'image source et le bitmap du canevas partagent un format de pixel compatible pour éviter les décalages de couleur.  
- **Libération des objets GDI** – encapsulez `Bitmap` et `Graphics` dans des instructions `using` ou appelez `Dispose()` manuellement ; sinon vous risquez de fuir des ressources non gérées.  
- **Erreurs de coordonnées** – les coordonnées des rectangles sont basées sur zéro. Sélectionner un rectangle qui dépasse les limites de l'image source déclenchera une exception.  

## Questions fréquemment posées

**Q : Puis‑je recadrer des images de n'importe quel format avec Aspose.Drawing ?**  
R : Oui, Aspose.Drawing prend en charge un large éventail de formats (PNG, JPEG, BMP, GIF, TIFF, etc.), vous pouvez donc recadrer pratiquement n'importe quel type d'image.

**Q : Existe‑t‑il des options de recadrage avancées ?**  
R : Absolument. Vous pouvez combiner `GraphicsPath`, les transformations `Matrix`, ou utiliser la classe `ImageProcessor` pour des sélections plus complexes comme les recadrages circulaires.

**Q : Puis‑je appliquer plusieurs opérations de recadrage à une même image ?**  
R : Oui. Après le premier recadrage, vous pouvez réutiliser le bitmap résultant comme nouvelle source et répéter le processus pour enchaîner plusieurs recadrages.

**Q : Aspose.Drawing est‑il adapté au traitement d'images par lots ?**  
R : En effet. Son API légère et l'absence de dépendances natives le rendent parfait pour le traitement de grandes collections d'images sur les serveurs.

**Q : Comment puis‑je obtenir du support pour les questions liées à Aspose.Drawing ?**  
R : Rendez‑vous sur le [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pour demander de l'aide et rejoindre la communauté.

---

**Dernière mise à jour :** 2026-10-13  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Charger, convertir BMP en PNG et autres formats avec Aspose.Drawing](/drawing/net/image-editing/load-save/)
- [Comment licencier Aspose.Drawing pour .NET – comment licencier aspose.drawing](/drawing/net/licensing/)
- [Comment dessiner un rectangle – transformation du système de coordonnées (Transformation de page) avec l'API Aspose.Drawing pour .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}