---
date: 2025-11-30
description: Apprenez à appliquer la transformation du système de coordonnées, à dessiner
  un bitmap rectangle et à transformer les pages à l’aide d’Aspose.Drawing pour .NET.
language: fr
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Transformation du système de coordonnées (Transformation de page) dans Aspose.Drawing
  pour .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Transformation du système de coordonnées (Transformation de page) dans Aspose.Drawing pour .NET

## Introduction

Bienvenue ! Dans ce tutoriel, vous découvrirez **comment effectuer une transformation du système de coordonnées** sur une page à l’aide d’Aspose.Drawing pour .NET. Que vous ayez besoin de **dessiner des objets rectangle bitmap**, de mettre à l’échelle des dessins, ou simplement de faire correspondre les unités de page aux unités du dispositif, les étapes ci‑dessous vous guideront à travers tout le processus—clair, concis, et prêt à être copié‑collé dans votre projet.

## Réponses rapides
- **Quelle est la classe principale pour le dessin ?** `Graphics` d’Aspose.Drawing.
- **Comment définir les unités de page ?** Utilisez `graphics.PageUnit = GraphicsUnit.Inch;`.
- **Puis‑je dessiner un rectangle sur une page transformée ?** Oui—créez un `Pen` et appelez `DrawRectangle`.
- **Où le résultat est‑il enregistré ?** Dans le dossier que vous spécifiez avec `bitmap.Save`.
- **Ai‑je besoin d’une licence pour la production ?** Une licence valide d’Aspose.Drawing est requise pour une utilisation commerciale.

## Qu’est‑ce qu’une transformation du système de coordonnées ?

Une **transformation du système de coordonnées** modifie la façon dont les coordonnées logiques de la page (comme les pouces ou les millimètres) sont mappées aux coordonnées physiques du dispositif (pixels). En ajustant la transformation, vous contrôlez le redimensionnement, la rotation et la translation de toutes les opérations de dessin, ce qui facilite la création de graphiques indépendants de la résolution.

## Pourquoi utiliser Aspose.Drawing pour les transformations de page ?

- **Compatibilité .NET complète** – fonctionne avec .NET Framework, .NET Core et .NET 5/6.  
- **API graphique riche** – offre les mêmes fonctionnalités que System.Drawing.Common sans restrictions de plateforme.  
- **Gestion simple des unités** – passez d’un pouce, millimètre, point, etc., avec une seule propriété.  
- **Sortie de haute qualité** – générez PNG, JPEG, BMP et autres formats avec un contrôle précis.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Bibliothèque Aspose.Drawing** – téléchargez la dernière version depuis le site officiel [ici](https://releases.aspose.com/drawing/net/).  
- **Environnement de développement** – Visual Studio (toute édition) ou un autre IDE .NET.  
- **Accès en écriture** – un dossier sur votre machine où l’image transformée sera enregistrée (remplacez `"Your Document Directory"` dans le code par le chemin réel).

Maintenant que tout est prêt, parcourons chaque étape.

## Importer les espaces de noms

Tout d’abord, importez l’espace de noms requis :

```csharp
using System.Drawing;
```

> *Pourquoi c’est important* : `System.Drawing` contient les structures `Bitmap`, `Graphics`, `Pen` et les couleurs que nous utiliserons tout au long du tutoriel.

## Étape 1 : Créer un Bitmap

Créez une toile vierge qui accueillera le dessin transformé. Nous spécifions une taille de **1000 × 800 pixels** et un format de pixel qui prend en charge la transparence alpha.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> Ce bitmap sert de surface de dessin. Le format de pixel choisi (`Format32bppPArgb`) garantit un rendu de haute qualité avec un alpha prémultiplié.

## Étape 2 : Créer un objet Graphics

Un objet `Graphics` fournit les méthodes de dessin (lignes, formes, texte). Nous l’obtenons à partir du bitmap que nous venons de créer.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> L’objet `Graphics` est le cœur de toutes les opérations de rendu ; il respecte les paramètres de transformation que nous appliquerons ensuite.

## Étape 3 : Effacer la toile

Avant de dessiner quoi que ce soit, effacez la toile avec une couleur d’arrière‑plan neutre (gris dans cet exemple). Cette étape montre également comment remplir l’ensemble du bitmap avec une couleur unie.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Étape 4 : Définir la transformation (Appliquer la transformation de page)

Ici nous **appliquons la transformation de page** en définissant `PageUnit` sur les pouces. Cela indique au moteur graphique d’interpréter toutes les coordonnées suivantes comme des pouces plutôt que des pixels.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *Astuce* : Modifier `PageUnit` est une façon simple de **transformer les coordonnées de page** sans calculer manuellement les valeurs en pixels.

## Étape 5 : Dessiner un rectangle (Draw rectangle bitmap)

Nous dessinons maintenant un rectangle de **1 pouce × 1 pouce** à la position (1, 1) pouces. L’épaisseur du `Pen` est fixée à `0.1f` pouces, donnant une ligne fine mais visible.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> Cela montre **draw rectangle bitmap** après l’application de la transformation — notez que la taille du rectangle est définie en pouces, pas en pixels.

## Étape 6 : Enregistrer l’image

Enfin, persistez le bitmap transformé sur le disque. Remplacez `"Your Document Directory"` par le chemin réel du dossier sur votre machine.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> Le fichier de sortie (`PageTransformation_out.png`) contiendra le rectangle dessiné à l’aide de la transformation du système de coordonnées que nous avons définie précédemment.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **L’image apparaît vide** | Toile non effacée ou dessin effectué en dehors de la zone visible. | Vérifiez `graphics.PageUnit` et les valeurs de coordonnées ; assurez‑vous que le rectangle se trouve à l’intérieur des limites du bitmap. |
| **Mise à l’échelle incorrecte** | Utilisation du mauvais `GraphicsUnit`. | Revérifiez que `graphics.PageUnit` correspond à l’unité que vous souhaitez (par ex., `GraphicsUnit.Inch`). |
| **Erreurs de chemin de fichier** | Dossier manquant ou caractères invalides. | Créez le dossier cible au préalable ou utilisez `Path.Combine` pour construire le chemin de façon sécurisée. |

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.Drawing gratuitement ?**  
R : Aspose.Drawing propose une version d’essai gratuite que vous pouvez obtenir [ici](https://releases.aspose.com/).

**Q : Où puis‑je trouver la documentation détaillée d’Aspose.Drawing ?**  
R : La documentation est disponible [ici](https://reference.aspose.com/drawing/net/).

**Q : Comment obtenir du support pour Aspose.Drawing ?**  
R : Pour le support, visitez le [Forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17).

**Q : Existe‑t‑il une licence temporaire pour Aspose.Drawing ?**  
R : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je acheter Aspose.Drawing ?**  
R : Vous pouvez acheter Aspose.Drawing [ici](https://purchase.aspose.com/buy).

## Conclusion

Vous avez maintenant appris comment **appliquer une transformation du système de coordonnées**, **dessiner des objets rectangle bitmap**, et **enregistrer le résultat** avec Aspose.Drawing pour .NET. Ces blocs de construction vous permettent de créer des graphiques indépendants de la résolution, parfaits pour les rapports, les éléments d’interface utilisateur, ou tout scénario où la précision des dimensions est cruciale. Expérimentez avec d’autres valeurs de `GraphicsUnit` (comme `Millimeter` ou `Point`) pour voir comment elles influencent vos dessins.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2025-11-30  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose