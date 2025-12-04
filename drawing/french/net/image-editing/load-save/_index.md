---
date: 2025-12-04
description: Maîtrisez le chargement d'images, la conversion d'images par lots et
  les changements de format dans .NET avec Aspose.Drawing. Apprenez à convertir BMP
  en PNG et bien plus encore.
language: fr
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Convertir BMP en PNG et autres formats avec Aspose.Drawing
url: /net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir BMP en PNG et autres formats avec Aspose.Drawing

## Introduction

Bienvenue dans notre guide étape par étape sur la façon de **convertir BMP en PNG** (et de nombreux autres formats d'image) en utilisant Aspose.Drawing pour .NET. Que vous ayez besoin de **modifier le format d'image** pour un seul fichier ou d'exécuter une **conversion d'images par lots** sur des dizaines de photos, ce tutoriel vous montre exactement comment charger, transformer et enregistrer des images avec un code propre et maintenable.

## Quick Answers
- **Aspose.Drawing peut‑il convertir BMP en PNG ?** Oui – il suffit de charger le BMP et d’appeler `Save` avec une extension .png.  
- **La conversion par lots est‑elle prise en charge ?** Absolument ; parcourez les fichiers et réutilisez la même méthode `LoadAndSave`.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence est requise pour une utilisation en production ; une licence temporaire est disponible pour l’évaluation.  
- **Quelles versions de .NET sont compatibles ?** Fonctionne avec .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Où puis‑je télécharger la bibliothèque ?** Obtenez le dernier package Aspose.Drawing depuis la page de téléchargement officielle.

## Qu'est‑ce que la conversion de format d'image en C# avec Aspose.Drawing ?

Aspose.Drawing est une bibliothèque .NET hautes performances, entièrement gérée, qui remplace l'ancienne `System.Drawing.Common`. Elle vous donne un contrôle complet sur les scénarios **load image ASP.NET**, prend en charge plus de 100 formats d'image et élimine les limitations spécifiques à la plateforme.

## Pourquoi utiliser Aspose.Drawing pour la conversion d'images par lots ?

- **Fiabilité multiplateforme** – aucune dépendance GDI+.  
- **Prise en charge riche des formats** – BMP, GIF, JPG, PNG, TIFF, et bien d’autres.  
- **API cohérente** – le même code fonctionne sous Windows, Linux et macOS.  
- **Performance** – optimisée pour les pipelines de traitement d'images à grande échelle.

## Prerequisites

Avant de commencer, assurez‑vous d'avoir :

- **Aspose.Drawing pour .NET** – téléchargez‑le [ici](https://releases.aspose.com/drawing/net/).  
- Un environnement de développement **.NET** fonctionnel (Visual Studio, VS Code ou Rider).  

Maintenant que tout est prêt, importons les espaces de noms requis et commençons à coder.

## Importer les espaces de noms

Dans votre projet .NET, commencez par importer l'espace de noms nécessaire :

```csharp
using System.Drawing;
```

Ces classes fournissent la fonctionnalité de base pour charger et enregistrer des images.

## Étape 1 : Chargement d'une image

La première étape consiste à charger un fichier image. L'exemple ci‑dessous montre le chargement d'images de différents formats, y compris BMP, que nous convertirons ensuite en PNG.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## Comment convertir BMP en PNG avec Aspose.Drawing

La méthode `LoadAndSave` gère à la fois le chargement du fichier source et son enregistrement dans le format de sortie souhaité. En passant `"bmp"` comme argument, la méthode produira automatiquement un fichier PNG lorsque vous modifierez l'extension dans `outputPath`.

### Étape 2.1 : Charger l'image

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Étape 2.2 : Enregistrer l'image (changer le format d'image)

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

Répétez l'appel `LoadAndSave` pour chaque format d'image que vous souhaitez traiter. En ajustant l'extension de `outputPath`, vous pouvez **convertir BMP en PNG**, **changer le format d'image** en GIF, JPG, etc., le tout avec la même méthode.

## Pièges courants et astuces

- **Séparateurs de chemin de fichier** – Utilisez `Path.Combine` pour la sécurité multiplateforme au lieu de concaténer manuellement les chaînes.  
- **Libération des Bitmaps** – Encapsulez le `Bitmap` dans un bloc `using` pour libérer rapidement les ressources natives.  
- **Paramètres de qualité** – Lors de l'enregistrement de JPEG, envisagez de spécifier un objet `EncoderParameters` pour contrôler la qualité de compression.  
- **Traitement par lots** – Placez vos fichiers image dans un dossier et parcourez `Directory.GetFiles` pour automatiser les conversions à grande échelle.

## Questions fréquentes

### Q1 : Aspose.Drawing est‑il compatible avec tous les formats d'image ?

R1 : Aspose.Drawing prend en charge un large éventail de formats, y compris BMP, GIF, JPG, PNG et TIFF.

### Q2 : Où puis‑je trouver la documentation détaillée d'Aspose.Drawing ?

R2 : Consultez la documentation officielle [ici](https://reference.aspose.com/drawing/net/).

### Q3 : Comment obtenir une licence temporaire pour Aspose.Drawing ?

R3 : Visitez [ici](https://purchase.aspose.com/temporary-license/) pour les détails de la licence temporaire.

### Q4 : Que faire si je rencontre des problèmes ou ai des questions pendant l'implémentation ?

R4 : Demandez de l'aide à la communauté Aspose.Drawing sur [Aspose Forum](https://forum.aspose.com/c/diagram/17).

### Q5 : Où puis‑je acheter la bibliothèque Aspose.Drawing ?

R5 : Vous pouvez l'acheter [ici](https://purchase.aspose.com/buy).

**Questions supplémentaires**

**Q : Puis‑je utiliser ce code dans une application web ASP.NET ?**  
R : Oui – la même logique `LoadAndSave` fonctionne dans ASP.NET, MVC ou Razor Pages ; assurez‑vous simplement que les chemins de fichiers sont accessibles au processus web.

**Q : Est‑il possible de traiter les images en parallèle pour accélérer la conversion par lots ?**  
R : Absolument. Encapsulez les appels `LoadAndSave` dans une boucle `Parallel.ForEach`, mais pensez à gérer la libération sécurisée des objets `Bitmap`.

## Conclusion

Vous avez maintenant appris comment **convertir BMP en PNG**, effectuer une **conversion d'images par lots** et **changer le format d'image** en utilisant Aspose.Drawing pour .NET. Appliquez ces modèles pour automatiser les pipelines d'images, générer des vignettes ou préparer des ressources pour la diffusion web. Expérimentez avec différents formats, intégrez le code dans vos services et profitez de la fiabilité d'une bibliothèque de dessin entièrement gérée.

---

**Dernière mise à jour :** 2025-12-04  
**Testé avec :** Aspose.Drawing 24.12 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}