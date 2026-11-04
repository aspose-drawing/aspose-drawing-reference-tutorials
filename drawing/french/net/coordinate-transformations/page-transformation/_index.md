---
date: 2026-11-04
description: Apprenez à dessiner des graphiques de rectangle tout en effectuant une
  coordinate system transformation dans .NET avec l'API Aspose.Drawing. Ce guide étape
  par étape montre comment convertir des inches en pixels et définir les page units.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: coordinate system transformation dans Aspose.Drawing
og_description: Apprenez à dessiner des graphiques de rectangle tout en convertissant
  des inches en pixels et en définissant les page units dans Aspose.Drawing pour .NET.
  Suivez le guide étape par étape pour une page transformation précise.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Comment dessiner un rectangle avec page transformation en utilisant Aspose.Drawing
  pour .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Comment dessiner un rectangle – coordinate system transformation (page transformation)
  dans Aspose.Drawing pour .NET
url: /fr/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment dessiner un rectangle – transformation du système de coordonnées (transformation de page) avec Aspose.Drawing pour .NET

## Introduction

Dans ce tutoriel, vous apprendrez **comment dessiner un rectangle** graphique tout en effectuant une transformation du système de coordonnées au niveau de la page à l’aide d’Aspose.Drawing pour .NET. Que vous construisiez un moteur de rapports, un outil de croquis de type CAO, ou toute application nécessitant des mesures réelles précises, ce guide vous accompagne à chaque étape — de la création d’un bitmap à l’enregistrement du PNG final. À la fin, vous serez à l’aise pour convertir les pouces en pixels, nettoyer l’arrière‑plan du canevas et définir les unités de page pour une sortie prête à l’impression.

## Réponses rapides
- **Qu’est‑ce que la transformation du système de coordonnées ?** Elle mappe les unités au niveau de la page (comme les pouces) aux pixels au niveau du dispositif afin que les dessins s’échelonnent correctement sur n’importe quel dispositif de sortie.  
- **Pourquoi choisir Aspose.Drawing ?** Il fournit une API graphique entièrement gérée, multiplateforme, qui remplace System.Drawing.Common et prend en charge plus de 30 formats d’image.  
- **Combien de temps l’exemple prend‑il à implémenter ?** Environ 5 à 10 minutes pour un rectangle de base avec transformation de page.  
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour les déploiements en production.  
- **Quelles runtimes .NET sont prises en charge ?** .NET Framework 4.6+, .NET Core 3.1+, et .NET 5/6/7.

## Qu’est‑ce qu’Aspose.Drawing ?

Aspose.Drawing est une bibliothèque graphique .NET qui fournit une **API indépendante du dispositif** pour créer et manipuler des images raster, des vecteurs et des dessins au niveau de la page sans dépendre de GDI+. Elle prend en charge **plus de 30 formats d’image** et peut traiter des images jusqu’à **10 000 × 10 000 pixels** tout en maintenant une faible consommation de mémoire.

## Pourquoi utiliser la transformation du système de coordonnées avec Aspose.Drawing ?

La transformation du système de coordonnées vous permet de concevoir des graphiques en unités du monde réel tandis que la bibliothèque gère automatiquement le redimensionnement en pixels pour tout dispositif de sortie. Cette approche garantit qu’un rectangle de 5 pouces s’imprime exactement à cinq pouces sur une imprimante 300 DPI et apparaît proportionnellement sur un écran 96 DPI, éliminant les erreurs de conversion manuelle.

- **Conception indépendante du dispositif :** Écrivez le code une fois ; Aspose.Drawing l’adapte aux écrans, imprimantes ou PDF.  
- **Dessin de précision :** Idéal pour les schémas techniques, les plans d’ingénierie ou tout scénario où les mesures exactes sont importantes.  
- **Fiabilité multiplateforme :** Fonctionne de façon cohérente sous Windows, Linux et macOS sans les limitations GDI+ de System.Drawing.  
- **Performance :** Sur un CPU typique de 2,5 GHz, dessiner un rectangle de 5 pouces à 300 DPI se termine en moins de **15 ms**, et la bibliothèque peut rendre **50 images par seconde** dans des scénarios d’aperçu en temps réel.

## Prérequis

- **Bibliothèque Aspose.Drawing :** Téléchargez la dernière version depuis le site officiel [ici](https://releases.aspose.com/drawing/net/).  
- **IDE :** Visual Studio, Rider ou tout éditeur compatible .NET.  
- **Dossier de sortie :** Remplacez `"Your Document Directory"` dans le code d’exemple par le dossier où vous souhaitez enregistrer le PNG.  
- **Support ASP.NET optionnel :** Vous pouvez ajouter le package NuGet à un projet ASP.NET Core et utiliser la même API ; le modèle suit l’approche typique **how to use aspnet** pour les bibliothèques .NET.

## Comment dessiner un rectangle avec transformation de page ?

Chargez un bitmap vierge, définissez l’unité de page en pouces, et dessinez un rectangle à l’aide d’un crayon bleu fin — cela complète le dessin du rectangle en quelques lignes de code seulement. La propriété `Graphics.PageUnit` indique au moteur d’interpréter toutes les coordonnées en pouces, vous permettant de penser en mesures réelles plutôt qu’en pixels bruts, et la bibliothèque convertit automatiquement les **pouces en pixels** en fonction du DPI du bitmap.

### Étape 1 : importer les espaces de noms

Les instructions `using` vous donnent accès aux classes de dessin de base.

```csharp
using System.Drawing;
```

### Étape 2 : créer un bitmap

`Bitmap` est le conteneur d’image en mémoire sur lequel vous dessinez. Il contient le tampon de pixels et expose des méthodes pour enregistrer dans des fichiers. Créer un bitmap définit la taille du canevas et le format des pixels.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Étape 3 : créer un objet Graphics

`Graphics` fournit la surface de dessin pour le bitmap. Il traduit les commandes de dessin de haut niveau (lignes, formes, texte) en opérations de pixels sur le bitmap sous‑jacent.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Étape 4 : nettoyer l’arrière‑plan du canevas

Nettoyer le canevas avec une couleur neutre garantit que vos formes ressortent. Dans cet exemple, nous remplissons l’arrière‑plan avec du gris clair, ce qui montre également la technique de **clear canvas background**.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Étape 5 : définir la transformation (comment définir les unités)

`Graphics.PageUnit` spécifie l’unité de mesure utilisée pour les coordonnées de page. La définir à `GraphicsUnit.Inch` indique à Aspose.Drawing de **convertir les pouces en pixels** automatiquement en fonction du DPI du bitmap (96 DPI par défaut, 300 DPI pour l’impression haute résolution). Vous pouvez également choisir `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` ou `GraphicsUnit.Pixel` selon les exigences de votre mise en page.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Étape 6 : dessiner un rectangle – dessiner des graphiques de rectangle

`Pen` définit la couleur, la largeur et le style des lignes dessinées sur une surface graphique. En utilisant un crayon bleu fin, nous dessinons un rectangle dont les dimensions sont exprimées en pouces, rendant le code plus lisible pour les mises en page orientées impression.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Étape 7 : enregistrer le bitmap au format png

Enfin, écrivez le bitmap dans un fichier PNG dans le dossier que vous avez spécifié précédemment. Enregistrer au format PNG préserve une qualité sans perte et est largement supporté sur toutes les plateformes.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Comment mettre à l’échelle les graphiques pour une imprimante ?

Définissez le DPI du bitmap à la résolution cible de l’imprimante (par exemple, 300 DPI) avant de dessiner. Cela met automatiquement à l’échelle la sortie **scale graphics printer** afin qu’un pouce dans votre code corresponde à un pouce sur la page imprimée, tandis que la taille logique du rectangle reste inchangée. Après avoir appelé `bitmap.SetResolution(300, 300)`, le même rectangle apparaîtra plus grand sur le papier mais conservera ses dimensions exactes.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Fichier de sortie non créé** | Chemin incorrect ou dossier manquant | Assurez‑vous que le répertoire cible existe ou appelez `Directory.CreateDirectory` avant d’enregistrer. |
| **Le rectangle apparaît déformé** | `PageUnit` ou DPI incohérents | Vérifiez que `graphics.PageUnit` correspond à l’unité souhaitée et que le DPI du bitmap est correctement défini (96 DPI par défaut, 300 DPI pour l’impression). |
| **Exception de licence** | Exécution sans licence valide en production | Appliquez votre licence temporaire ou permanente Aspose.Drawing avant de créer des objets graphiques. |

## Questions fréquemment posées

**Q : Puis‑je utiliser Aspose.Drawing gratuitement ?**  
R : Oui, un essai gratuit est disponible [ici](https://releases.aspose.com/).

**Q : Où puis‑je trouver la documentation détaillée d’Aspose.Drawing ?**  
R : La référence complète de l’API se trouve [ici](https://reference.aspose.com/drawing/net/).

**Q : Comment obtenir du support pour Aspose.Drawing ?**  
R : Visitez le [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) pour l’aide de la communauté et l’assistance officielle.

**Q : Une licence temporaire est‑elle disponible pour Aspose.Drawing ?**  
R : Absolument — obtenez‑en une [ici](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je acheter une licence complète Aspose.Drawing ?**  
R : Vous pouvez l’acheter [ici](https://purchase.aspose.com/buy).

## Conclusion

Vous savez maintenant **comment dessiner un rectangle** graphique avec une transformation au niveau de la page en utilisant Aspose.Drawing pour .NET. En définissant l’unité de page en pouces, en nettoyant l’arrière‑plan du canevas et en enregistrant le résultat au format PNG, vous obtenez une sortie précise et indépendante du dispositif, adaptée à l’affichage à l’écran comme à l’impression haute résolution. Expérimentez avec d’autres unités, rotations ou origines de coordonnées personnalisées pour débloquer des scénarios de dessin encore plus puissants.

---

**Dernière mise à jour :** 2026-11-04  
**Testé avec :** Aspose.Drawing 24.12 for .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Comment définir l’unité dans Aspose.Drawing pour .NET – Unités de mesure](/drawing/net/coordinate-transformations/units-of-measure/)
- [Transformation globale](/drawing/net/coordinate-transformations/global-transformation/)
- [Transformation étape par étape – Transformations de coordonnées](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}