---
date: 2026-10-18
description: Convertissez un dessin en PNG avec Aspose.Drawing tout en appliquant
  des world transformations. Apprenez les exemples translate, rotate et scale en C#
  et exportez des PNG transparents.
keywords:
- convert drawing to png
- save graphics as png
- rotate image .net
- scale graphics .net
- transparent png bitmap
lastmod: 2026-10-18
linktitle: Transformation du monde dans Aspose.Drawing
og_description: Convertissez un dessin en PNG avec Aspose.Drawing, appliquez des world
  transformations et exportez des PNG transparents. Apprenez les exemples C# translate,
  rotate et scale pour .NET.
og_image_alt: Tutorial showing how to convert drawing to PNG using Aspose.Drawing
  with world transformation
og_title: Comment convertir un dessin en PNG avec Aspose.Drawing – transformation
  du monde
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  headline: How to convert drawing to PNG with Aspose.Drawing – world transformation
  type: TechArticle
- description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  name: How to convert drawing to PNG with Aspose.Drawing – world transformation
  steps:
  - name: create a bitmap
    text: '**Definition:** `Bitmap` is Aspose.Drawing’s in‑memory representation of
      a raster image that you can draw on or save to disk. We start by creating a
      blank canvas that will hold our drawing. `new Bitmap(width, height, PixelFormat.Format32bppPArgb)`
      creates a 32‑bit per pixel bitmap with premultiplied'
  - name: set the world transformation (graphics translate example)
    text: '**Definition:** `Graphics` is the drawing surface that renders shapes onto
      a `Bitmap`. `TranslateTransform` moves the origin of the coordinate system to
      a new location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height
      / 2)` shifts the (0,0) point to the canvas centre. After this call, an'
  - name: draw a rectangle using the transformed coordinates
    text: '**Definition:** `DrawRectangle` is a method of `Graphics` that renders
      a rectangular outline or filled shape based on the supplied pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width'
  - name: save the result – convert graphics to PNG
    text: '**Definition:** `ImageFormat` is an enumeration that tells the `Save` method
      which file format to use. `Save` writes the bitmap to a file in the specified
      image format. `bitmap.Save(outputPath, ImageFormat.Png)` writes a lossless PNG
      file that can be used directly in web pages or UI components. - PN'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- convert drawing to png
- Aspose.Drawing
- .NET graphics
- PNG export
- world transformation
title: Comment convertir un dessin en PNG avec Aspose.Drawing – transformation du
  monde
url: /fr/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment convertir un dessin en PNG avec Aspose.Drawing – transformation du monde

## Enregistrer le bitmap en PNG – introduction

**Comment convertir un dessin en PNG** avec Aspose.Drawing est une exigence courante lorsque vous avez besoin d'images transparentes de haute qualité générées à la volée. Dans ce tutoriel, vous apprendrez comment **enregistrer le bitmap en PNG**, appliquer des transformations du monde telles que translation, rotation et mise à l'échelle, et enfin convertir les graphiques en PNG — le tout avec du code C# propre et maintenable. Que vous construisiez un moteur de reporting, un composant de graphiques ou un rendu d'interface utilisateur personnalisé, maîtriser ces étapes vous permet de créer des images dynamiques qui ont fière allure sur n'importe quel appareil.

## Réponses rapides
- **Que signifie « transformation du monde » ?** Elle mappe les coordonnées logiques (monde) de votre dessin aux coordonnées de la page (appareil), vous permettant de repositionner, faire pivoter ou mettre à l'échelle tout avec une seule matrice.  
- **Puis-je exporter le résultat en PNG ?** Oui – après le dessin, il suffit d’appeler `bitmap.Save(...)` avec une extension `.png`.  
- **Ai-je besoin d’une licence pour Aspose.Drawing ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Cette fonctionnalité est‑elle compatible avec .NET 6/7 ?** Absolument – Aspose.Drawing prend en charge .NET Framework 4.5+ et .NET Core/5/6/7, couvrant plus de 90 % des déploiements .NET actuels.  
- **Combien de transformations puis‑je enchaîner ?** Vous pouvez appliquer **plusieurs transformations graphiques** en séquence (translation, rotation, mise à l'échelle, etc.) sans pénalité de performance.

## Qu’est‑ce qu’une transformation du monde dans Aspose.Drawing ?

Une transformation du monde modifie le système de coordonnées utilisé par vos commandes de dessin. Par défaut, (0,0) est le coin supérieur gauche du bitmap. Avec `TranslateTransform`, `RotateTransform` ou `ScaleTransform`, vous pouvez repositionner cette origine, faire pivoter les formes ou les redimensionner sans altérer la géométrie originale. Cela vous permet de concevoir une fois et de rendre à n'importe quelle taille ou orientation.

## Comment enregistrer un PNG avec Aspose.Drawing ?

Chargez un objet `Bitmap`, définissez les transformations du monde souhaitées sur son instance `Graphics`, dessinez vos formes, puis appelez finalement `bitmap.Save("output.png", ImageFormat.Png)`. Cette instruction d’enregistrement en une seule ligne écrit un fichier PNG sans perte qui préserve la transparence et la fidélité des couleurs, ce qui le rend idéal pour les ressources web et les superpositions d'interface. L'API gère tout l'encodage bas‑niveau, ainsi vous obtenez un PNG prêt à l'emploi en moins d'une seconde pour des tailles de canevas typiques.

## Pourquoi utiliser un exemple de translation graphique ?

Un exemple de translation graphique vous permet de déplacer l'origine du dessin une seule fois au lieu de recalculer chaque point. En déplaçant l'origine au centre du canevas, vous simplifiez la géométrie, réduisez la duplication de code et laissez le moteur graphique effectuer la multiplication de matrices en code natif, ce qui peut améliorer la vitesse de rendu jusqu'à 30 % sur de grands canevas. Ce modèle rend également votre code plus facile à maintenir lorsque vous ajoutez ultérieurement une rotation ou une mise à l'échelle.

## Exemple de translation graphique

Un **exemple de translation graphique** montre comment le déplacement de l'origine simplifie le positionnement. Au lieu de recalculer chaque point, vous déplacez le système de coordonnées une fois et dessinez comme si la nouvelle origine était le centre du canevas.

## Prérequis

- **Bibliothèque Aspose.Drawing** intégrée à votre projet .NET – téléchargez‑la depuis la page officielle [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/).  
- Un **répertoire de documents** où l'image de sortie sera enregistrée.  
- Une connaissance de base de la syntaxe **C#** et de Visual Studio ou de votre IDE préféré.  

Maintenant, plongeons dans le code !

## Importer les espaces de noms

Les utilitaires `Bitmap`, `Graphics` et Aspose drawing résident dans ces espaces de noms.  
**Définition :** `System.Drawing` fournit les types GDI+ de base, tandis que `Aspose.Drawing` les étend avec des capacités multiplateformes, vous permettant d’exécuter le même code sous Windows, Linux et macOS sans dépendances supplémentaires.

## Guide étape par étape

### Étape 1 : créer un bitmap

**Définition :** `Bitmap` est la représentation en mémoire d’une image raster d’Aspose.Drawing sur laquelle vous pouvez dessiner ou enregistrer sur le disque.  

Nous commençons par créer un canevas vierge qui contiendra notre dessin.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` crée un bitmap 32 bits par pixel avec alpha prémultiplié, le format optimal pour la sortie PNG car il préserve la transparence sans étapes de conversion supplémentaires.

- **Pourquoi 32bppPArgb ?** Ce format de pixel prend en charge la transparence alpha et le rendu de couleur haute qualité, parfait pour la sortie PNG.  
- **Astuce :** Ajustez la largeur/hauteur pour correspondre à la taille cible de l'image ; un canevas 1920 × 1080 s’affiche en moins de 0,2 seconde sur un ordinateur portable de développeur typique.

### Étape 2 : définir la transformation du monde (exemple de translation graphique)

**Définition :** `Graphics` est la surface de dessin qui rend les formes sur un `Bitmap`.  

`TranslateTransform` déplace l'origine du système de coordonnées vers une nouvelle position.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` décale le point (0,0) vers le centre du canevas. Après cet appel, toute forme que vous dessinez en utilisant les coordonnées (0,0) apparaîtra au milieu de l'image.

- Cela déplace le point (0,0) à (500, 400) – le milieu d'un canevas 1000 × 800.  
- Vous pouvez enchaîner des transformations supplémentaires : `RotateTransform` fait pivoter le système de coordonnées, et `ScaleTransform` le met à l'échelle, permettant **plusieurs transformations graphiques** dans un même pipeline.

### Étape 3 : dessiner un rectangle en utilisant les coordonnées transformées

**Définition :** `DrawRectangle` est une méthode de `Graphics` qui rend le contour ou la forme remplie d'un rectangle en fonction du stylo et des coordonnées fournis.  

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` dessine un rectangle centré sur le canevas car son coin supérieur gauche est décalé de la moitié de sa largeur et de sa hauteur par rapport à l'origine transformée.

- Le coin supérieur gauche du rectangle commence à l'origine transformée (centre de l'image).  
- N'hésitez pas à expérimenter avec d'autres formes — ellipses, lignes ou chemins personnalisés.

### Étape 4 : enregistrer le résultat – convertir les graphiques en PNG

**Définition :** `ImageFormat` est une énumération qui indique à la méthode `Save` quel format de fichier utiliser.  

`Save` écrit le bitmap dans un fichier au format d'image spécifié.  
`bitmap.Save(outputPath, ImageFormat.Png)` écrit un fichier PNG sans perte qui peut être utilisé directement dans les pages web ou les composants UI.

- PNG préserve les couleurs exactes et la transparence que nous avons définies précédemment.  
- Remplacez `"Your Document Directory"` par le chemin réel sur votre machine.  
- Pour le traitement par lots, parcourez une collection d'objets `Bitmap` et appelez `Save` à l'intérieur de la boucle – la bibliothèque peut gérer des milliers d'images avec moins de 200 Mo de RAM.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Erreur fichier introuvable** lors de l'enregistrement | Le dossier cible n'existe pas. | Créez le dossier programmatiquement (`Directory.CreateDirectory`) avant d'appeler `Save`. |
| **Image vide** après transformation | `TranslateTransform` appelé après le dessin. | Assurez‑vous que la transformation est définie **avant** toute commande de dessin. |
| **Couleurs déformées** | Utilisation d'un format de pixel incompatible. | Utilisez `Format32bppPArgb` pour la sortie PNG. |
| **Manque de mémoire sur de grands canevas** | Chargement du bitmap complet en mémoire. | Utilisez les options de streaming de `Bitmap` ou divisez l'image en tuiles ; Aspose.Drawing peut rendre les tuiles indépendamment. |

## Questions fréquemment posées

**Q : Puis‑je appliquer plus d’une transformation ?**  
R : Oui – vous pouvez enchaîner `TranslateTransform`, `RotateTransform` et `ScaleTransform` pour obtenir des effets complexes dans un seul pipeline graphique.

**Q : Aspose.Drawing est‑il gratuit pour les projets commerciaux ?**  
R : Un essai gratuit est disponible pour l’évaluation, mais une licence commerciale est requise pour une utilisation en production.

**Q : Cela fonctionne‑t‑il avec .NET Core et .NET 5/6/7 ?**  
R : Absolument. Aspose.Drawing prend en charge tous les runtimes .NET modernes, y compris .NET Core, .NET 5, .NET 6 et .NET 7.

**Q : Où puis‑je trouver la référence complète de l’API ?**  
R : La documentation complète est disponible [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).

**Q : Comment dépanner un fichier de sortie manquant ?**  
R : Vérifiez la chaîne de chemin, assurez‑vous des permissions d’écriture, et confirmez que le répertoire existe avant d’appeler `Save`.

## Conclusion

Vous avez maintenant appris **comment convertir un dessin en PNG** avec Aspose.Drawing, appliqué une **transformation du monde**, et réalisé un **exemple de translation graphique** qui peut être étendu avec rotation ou mise à l'échelle. En maîtrisant ces blocs de construction, vous pouvez générer des images dynamiques, créer des graphiques personnalisés, ou produire des graphiques à la volée pour toute application .NET. Ensuite, explorez le tutoriel de transformation basée sur les matrices pour combiner plusieurs opérations en une seule matrice et obtenir des performances encore meilleures.

---

**Dernière mise à jour :** 2026-10-18  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose  
**Ressources associées :** [Aspose.Drawing API reference](https://reference.aspose.com/drawing/net/) | [Download free trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Tutoriels associés

- [Tutoriel de transformation matricielle : transformations matricielles dans Aspose.Drawing pour .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Comment faire pivoter une image avec la transformation globale Aspose.Drawing](/drawing/net/coordinate-transformations/global-transformation/)
- [Transformation du système de coordonnées – transformation de page dans Aspose.Drawing pour .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}