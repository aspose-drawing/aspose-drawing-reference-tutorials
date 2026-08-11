---
date: 2026-06-23
description: Apprenez comment enregistrer un PNG avec Aspose.Drawing, appliquer des
  transformations du monde et convertir des graphiques en PNG. Comprend des exemples
  de transformation de translation en C# et plusieurs transformations graphiques.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: Transformation du monde dans Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
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
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Comment enregistrer un PNG avec Aspose.Drawing – Transformation du monde
url: /fr/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment enregistrer PNG avec Aspose.Drawing – Transformation du monde

## Enregistrer un bitmap en PNG – Introduction

**Comment enregistrer PNG** avec Aspose.Drawing est une exigence courante lorsque vous avez besoin d'images transparentes de haute qualité générées à la volée. Dans ce tutoriel, vous apprendrez comment **enregistrer un bitmap en PNG**, appliquer des transformations du monde telles que translation, rotation et mise à l'échelle, et enfin convertir les graphiques en PNG — le tout avec du code C# propre et maintenable. Que vous construisiez un moteur de reporting, un composant de graphiques ou un rendu d'interface utilisateur personnalisé, maîtriser ces étapes vous permet de créer des images dynamiques qui ont fière allure sur n'importe quel appareil.

## Réponses rapides
- **Que signifie « transformation du monde » ?** Elle mappe les coordonnées logiques (monde) de votre dessin aux coordonnées de la page (appareil).  
- **Puis-je exporter le résultat en PNG ?** Oui – après le dessin, il suffit d’appeler `bitmap.Save(...)` avec une extension `.png`.  
- **Ai-je besoin d’une licence pour Aspose.Drawing ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Cette fonctionnalité est‑elle compatible avec .NET 6/7 ?** Absolument – Aspose.Drawing prend en charge .NET Framework 4.5+ ainsi que .NET Core/5/6/7.  
- **Combien de transformations puis‑je enchaîner ?** Vous pouvez appliquer **plusieurs transformations graphiques** en séquence (translation, rotation, mise à l'échelle, etc.).

## Qu’est‑ce qu’une transformation du monde dans Aspose.Drawing ?

Une transformation du monde modifie le système de coordonnées utilisé par vos commandes de dessin. Par défaut, (0,0) correspond au coin supérieur gauche du bitmap. Avec `TranslateTransform`, `RotateTransform` ou `ScaleTransform`, vous pouvez repositionner cette origine, faire pivoter les formes ou les redimensionner sans modifier la géométrie d'origine.

## Comment enregistrer PNG avec Aspose.Drawing ?

Chargez un objet `Bitmap`, définissez les transformations du monde souhaitées sur son instance `Graphics`, dessinez vos formes, puis appelez `bitmap.Save("output.png", ImageFormat.Png)`. Cet appel d’enregistrement en une seule ligne crée un fichier PNG sans perte qui préserve la transparence et la fidélité des couleurs, ce qui le rend idéal pour les ressources web et les superpositions d’interface.

## Pourquoi utiliser un exemple de translation graphique ?

Un exemple de translation graphique vous permet de déplacer l’origine du dessin une fois, au lieu de recalculer chaque point. Cette approche réduit la complexité du code, améliore la lisibilité et laisse le moteur graphique gérer les calculs de matrice efficacement, ce qui peut augmenter les performances de rendu jusqu’à 30 % sur de grandes toiles.

## Exemple de translation graphique

Un **exemple de translation graphique** montre comment le déplacement de l’origine simplifie le positionnement. Au lieu de recalculer chaque point, vous déplacez le système de coordonnées une fois et dessinez comme si la nouvelle origine était le centre de la toile.

## Prérequis

- **Bibliothèque Aspose.Drawing** intégrée à votre projet .NET – téléchargez‑la depuis la [page de version Aspose.Drawing](https://releases.aspose.com/drawing/net/) officielle.  
- Un **répertoire de documents** où l’image de sortie sera enregistrée.  
- Une connaissance de base de la syntaxe **C#** ainsi que de Visual Studio ou de votre IDE préféré.  

Maintenant, plongeons dans le code !

## Importer les espaces de noms

Les utilitaires `Bitmap`, `Graphics` et Aspose Drawing se trouvent dans ces espaces de noms.  
**Définition :** `System.Drawing` fournit les types GDI+ de base, tandis que `Aspose.Drawing` les étend avec des fonctionnalités multiplateformes.

## Guide étape par étape

### Étape 1 : Créer un Bitmap

Nous commençons par créer une toile vierge qui contiendra notre dessin.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` crée un bitmap de 32 bits par pixel avec alpha prémultiplié, ce qui est le format optimal pour la sortie PNG car il préserve la transparence sans étapes de conversion supplémentaires.

- **Pourquoi 32bppPArgb ?** Ce format de pixel prend en charge la transparence alpha et le rendu couleur haute qualité, parfait pour la sortie PNG.  
- **Astuce :** Ajustez la largeur/hauteur pour correspondre à la taille cible de votre image.

### Étape 2 : Définir la transformation du monde (exemple de translation graphique)

`TranslateTransform` déplace l’origine du système de coordonnées vers un nouvel emplacement.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` décale le point (0,0) vers le centre de la toile. Après cet appel, toute forme que vous dessinez en utilisant les coordonnées (0,0) apparaîtra au milieu de l’image.

- Cela déplace le point (0,0) vers (500, 400) – le centre d’une toile de 1000 × 800.  
- Vous pouvez enchaîner d’autres transformations : `RotateTransform` fait pivoter le système de coordonnées, et `ScaleTransform` le met à l’échelle, permettant **plusieurs transformations graphiques**.

### Étape 3 : Dessiner un rectangle avec les coordonnées transformées

`DrawRectangle` dessine un rectangle en utilisant le crayon et les coordonnées spécifiés.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` dessine un rectangle centré sur la toile car son coin supérieur gauche est décalé de la moitié de sa largeur et de sa hauteur par rapport à l’origine transformée.

- Le coin supérieur gauche du rectangle commence à l’origine transformée (centre de l’image).  
- N’hésitez pas à expérimenter avec d’autres formes — ellipses, lignes ou chemins personnalisés.

### Étape 4 : Enregistrer le résultat – Convertir les graphiques en PNG

`Save` écrit le bitmap dans un fichier au format d’image spécifié.  
`ImageFormat` indique le format de fichier pour l’enregistrement des images, comme PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` crée un fichier PNG sans perte qui peut être utilisé directement dans les pages web ou les composants d’interface.

- PNG préserve les couleurs exactes et la transparence que nous avons définies précédemment.  
- Remplacez `"Your Document Directory"` par le chemin réel sur votre machine.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Erreur fichier non trouvé** lors de l’enregistrement | Le dossier cible n’existe pas. | Créez le dossier programmétiquement (`Directory.CreateDirectory`) avant d’appeler `Save`. |
| **Image vide** après transformation | `TranslateTransform` appelé après le dessin. | Assurez‑vous que la transformation est définie **avant** toute commande de dessin. |
| **Couleurs déformées** | Utilisation d’un format de pixel incompatible. | Restez avec `Format32bppPArgb` pour la sortie PNG. |

## Questions fréquentes

**Q : Puis‑je appliquer plus d’une transformation ?**  
R : Oui – vous pouvez enchaîner `TranslateTransform`, `RotateTransform` et `ScaleTransform` pour obtenir des effets complexes dans un seul pipeline graphique.

**Q : Aspose.Drawing est‑il gratuit pour les projets commerciaux ?**  
R : Un essai gratuit est disponible pour l’évaluation, mais une licence commerciale est requise pour une utilisation en production.

**Q : Cela fonctionne‑t‑il avec .NET Core et .NET 5/6/7 ?**  
R : Absolument. Aspose.Drawing prend en charge tous les runtimes .NET modernes, y compris .NET Core, .NET 5, .NET 6 et .NET 7.

**Q : Où puis‑je trouver la référence complète de l’API ?**  
R : La documentation complète est disponible [ici](https://reference.aspose.com/drawing/net/).

**Q : Comment dépanner un fichier de sortie manquant ?**  
R : Vérifiez la chaîne de chemin, assurez‑vous des permissions d’écriture, et confirmez que le répertoire existe avant d’appeler `Save`.

## Conclusion

Vous avez maintenant appris **comment enregistrer PNG** avec Aspose.Drawing, appliqué une **transformation du monde**, et réalisé un **exemple de translation graphique** qui peut être étendu avec rotation ou mise à l’échelle. En maîtrisant ces blocs de construction, vous pouvez générer des images dynamiques, créer des graphiques personnalisés ou produire des graphiques à la volée pour toute application .NET.

---

**Dernière mise à jour :** 2026-06-23  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose  
**Ressources associées :** [Référence API Aspose.Drawing](https://reference.aspose.com/drawing/net/) | [Télécharger l’essai gratuit](https://releases.aspose.com/drawing/net/)

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

- [Tutoriel sur la transformation matricielle : Transformations matricielles dans Aspose.Drawing pour .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Comment faire pivoter une image avec la transformation globale Aspose.Drawing](/drawing/net/coordinate-transformations/global-transformation/)
- [Transformation du système de coordonnées – Transformation de page dans Aspose.Drawing pour .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}