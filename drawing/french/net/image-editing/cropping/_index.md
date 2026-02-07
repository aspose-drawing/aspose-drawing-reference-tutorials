---
date: 2026-02-07
description: Tutoriel pas à pas pour recadrer une image en PNG à l'aide d'Aspose.Drawing,
  l'alternative à System.Drawing pour les développeurs .NET. Inclut le recadrage par
  lots et les techniques essentielles.
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Comment recadrer une image au format PNG avec Aspose.Drawing pour .NET
url: /fr/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment recadrer une image en PNG avec Aspose.Drawing pour .NET

Si vous devez **recadrer une image en PNG** rapidement et de manière fiable dans un environnement .NET, vous êtes au bon endroit. Dans ce tutoriel, nous passerons en revue les étapes exactes pour charger une image, définir la zone de recadrage et enregistrer le résultat sous forme de fichier PNG — le tout en utilisant Aspose.Drawing, une **alternative moderne à System.Drawing** qui fonctionne sur plusieurs plateformes.

## Réponses rapides
- **Quelle bibliothèque devrais-je utiliser ?** Aspose.Drawing pour .NET (une alternative complète à System.Drawing.Common)  
- **Combien de temps prend le recadrage de base ?** Généralement moins d’une seconde pour une image unique sur un CPU moderne  
- **Puis-je recadrer en PNG ?** Oui – enregistrez le bitmap recadré sous forme de fichier PNG (voir Étape 6)  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production  
- **Le traitement par lots est‑il possible ?** Absolument – encapsulez les mêmes étapes dans une boucle pour traiter plusieurs fichiers  

## Qu’est‑ce que le « recadrer une image en PNG » ?

Recadrer une image signifie extraire une région rectangulaire du bitmap original. Lorsque vous enregistrez cette région au format PNG, vous conservez la transparence et bénéficiez d’une compression sans perte — idéal pour les miniatures, les icônes ou tout autre élément d’interface utilisateur.

## Pourquoi Aspose.Drawing est‑il une alternative à System.Drawing ?

- **Prise en charge multiplateforme** – fonctionne sous Windows, Linux et macOS sans dépendances natives GDI+.  
- **Gestion riche des formats de pixels** – 32 bits, 24 bits, indexés, etc.  
- **API axée sur la performance** – idéale tant pour les modifications d’une seule image que pour les traitements par lots à grande échelle.  

## Prérequis

Avant de commencer, assurez-vous d’avoir :

- **Bibliothèque Aspose.Drawing** intégrée à votre projet .NET. Vous pouvez la télécharger [ici](https://releases.aspose.com/drawing/net/).  
- Un dossier contenant les images sources que vous souhaitez recadrer. Remplacez `"Your Document Directory"` dans les extraits de code par le chemin réel sur votre machine.

## Importer les espaces de noms

```csharp
using System.Drawing;
```

L’espace de noms `System.Drawing` nous donne accès aux types `Bitmap`, `Graphics` et associés que Aspose.Drawing étend.

## Guide étape par étape

### Étape 1 : Créer un canevas Bitmap

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Nous commençons avec un canevas vierge dimensionné pour contenir le résultat recadré. Ajustez la largeur et la hauteur pour correspondre aux dimensions de la zone que vous prévoyez d’extraire.

### Étape 2 : Créer un objet Graphics

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Un objet `Graphics` nous permet de dessiner sur le canevas. Le `InterpolationMode` contrôle la façon dont les valeurs de pixels sont calculées lors du redimensionnement ou de la transformation — `NearestNeighbor` fonctionne bien pour les bords nets.

### Étape 3 : Charger l’image à recadrer

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Chargez l’image source. Assurez‑vous que le chemin pointe vers un fichier existant ; sinon une exception sera levée.

### Étape 4 : Définir les rectangles source et destination

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

Le `sourceRectangle` indique à l’API quelle partie de l’image originale conserver. Ici nous sélectionnons la zone de 50 × 40 pixels en haut à gauche. En assignant le même rectangle à `destinationRectangle`, nous conservons la région recadrée à sa taille d’origine.

### Étape 5 : Effectuer l’opération de recadrage

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` copie la portion définie de `image` sur notre `bitmap` vierge. C’est l’opération principale de **recadrer une image en PNG**.

### Étape 6 : Enregistrer l’image recadrée (Recadrer une image en PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Enfin, écrivez le canevas sur le disque sous forme de fichier PNG. Le PNG préserve tout canal alpha et offre une qualité sans perte — idéal pour les éléments d’interface utilisateur.

## Comment recadrer des images dans un scénario par lots

Lorsque vous avez des dizaines ou des centaines d’images, placez simplement l’ensemble du fragment de code à l’intérieur d’une boucle `foreach` qui parcourt une collection de chemins de fichiers. La même logique `Graphics.DrawImage` s’applique, rendant le **recadrage d’images par lots** une extension triviale de ce tutoriel.

## Pièges courants et conseils

- **Incompatibilités de format de pixel** – assurez‑vous que l’image source et le bitmap du canevas partagent un format de pixel compatible pour éviter les décalages de couleur.  
- **Libération des objets GDI** – encapsulez `Bitmap` et `Graphics` dans des instructions `using` ou appelez `Dispose()` manuellement ; sinon vous risquez de fuir des ressources non gérées.  
- **Erreurs de coordonnées** – les coordonnées des rectangles commencent à zéro. Sélectionner un rectangle qui dépasse les limites de l’image source déclenchera une exception.  

## Foire aux questions

**Q : Puis‑je recadrer des images de n’importe quel format avec Aspose.Drawing ?**  
R : Oui, Aspose.Drawing prend en charge un large éventail de formats (PNG, JPEG, BMP, GIF, TIFF, etc.), vous pouvez donc recadrer pratiquement n’importe quel type d’image.

**Q : Existe‑t‑il des options de recadrage avancées ?**  
R : Absolument. Vous pouvez combiner `GraphicsPath`, les transformations `Matrix`, ou utiliser la classe `ImageProcessor` pour des sélections plus complexes comme les recadrages circulaires.

**Q : Puis‑je appliquer plusieurs opérations de recadrage à une même image ?**  
R : Oui. Après le premier recadrage, vous pouvez réutiliser le bitmap résultant comme nouvelle source et répéter le processus pour enchaîner plusieurs recadrages.

**Q : Aspose.Drawing est‑il adapté au traitement d’images par lots ?**  
R : En effet. Son API légère et l’absence de dépendances natives le rendent parfait pour traiter de grandes collections d’images sur les serveurs.

**Q : Comment obtenir de l’aide pour les questions liées à Aspose.Drawing ?**  
R : Rendez‑vous sur le [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pour demander de l’assistance et rejoindre la communauté.

---

**Dernière mise à jour :** 2026-02-07  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}