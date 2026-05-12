---
date: 2026-02-12
description: Apprenez à enregistrer un bitmap en C# et à tracer des courbes de Bézier
  avec Aspose.Drawing pour .NET. Suivez notre guide pas à pas pour créer rapidement
  des graphiques époustouflants.
linktitle: Save Bitmap C# – Draw Bezier Splines with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Enregistrer un bitmap C# – Dessiner des splines de Bézier avec Aspose.Drawing
url: /fr/net/lines-curves-and-shapes/draw-bezier-spline/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer un Bitmap C# – Dessiner des Splines de Bézier avec Aspose.Drawing

Bienvenue dans notre tutoriel pas à pas sur **comment enregistrer un bitmap C#** et dessiner des splines de Bézier en utilisant Aspose.Drawing pour .NET ! Les splines de Bézier sont des courbes polyvalentes largement utilisées en infographie. Avec Aspose.Drawing, une puissante bibliothèque .NET, vous pouvez créer des graphiques époustouflants en toute simplicité. Ce tutoriel vous guidera à travers le processus de dessin de splines de Bézier de manière simple et efficace.

## Réponses rapides
- **Que fait la méthode `Save` ?** Elle écrit le bitmap dans un fichier au format que vous spécifiez.  
- **Quel espace de noms est requis ?** `System.Drawing` fournit les classes graphiques de base.  
- **Puis-je modifier l'épaisseur de la ligne ?** Oui, définissez la largeur du `Pen` lors de sa création.  
- **Ai-je besoin d'une licence Aspose pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise pour la production.  
- **Cette fonctionnalité est‑elle compatible avec .NET 6 ?** Absolument – Aspose.Drawing prend en charge .NET 5/6 et .NET Core.

## Qu’est‑ce que « enregistrer un bitmap C# » ?
En C#, *enregistrer un bitmap* signifie persister une image en mémoire (`Bitmap` object) dans un fichier physique (par ex., PNG, JPEG). La méthode `Bitmap.Save` gère l’encodage et écrit les données sur le disque.

## Pourquoi dessiner une spline de Bézier avec Aspose.Drawing ?
- **Précision** – Les points de contrôle vous permettent de façonner la courbe exactement comme vous le souhaitez.  
- **Performance** – Aspose.Drawing est optimisé pour le rendu côté serveur, vous permettant de générer des images rapidement.  
- **Multi‑plateforme** – Fonctionne sous Windows, Linux et macOS sans les limitations héritées de System.Drawing.Common.

## Prérequis

- Une connaissance pratique du développement C# et .NET.  
- Bibliothèque Aspose.Drawing pour .NET installée. Vous pouvez la télécharger [ici](https://releases.aspose.com/drawing/net/).  
- Un environnement de développement intégré (IDE) tel que Visual Studio.

## Comment dessiner une spline de Bézier en C#
Si vous vous demandez **comment dessiner des courbes de Bézier**, la première étape consiste à définir le point de départ, deux points de contrôle et le point d’arrivée. Ces points déterminent la forme de la spline.

## Importer les espaces de noms
Commencez par importer les espaces de noms nécessaires dans votre projet. Cela garantit que vous avez accès aux classes et méthodes requises pour dessiner des splines de Bézier.

```csharp
using System.Drawing;
```

## Étape 1 : Créer un Bitmap
Commencez par créer un bitmap, le canevas sur lequel vous dessinerez la spline de Bézier. Définissez la largeur, la hauteur et le format de pixel selon les besoins de votre application.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Étape 2 : Configurer le Pen et les points de contrôle
Définissez un `Pen` pour spécifier la couleur et la largeur de la spline de Bézier. De plus, configurez les points de contrôle pour la courbe de Bézier.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
PointF p1 = new PointF(0, 0);      // start point
PointF c1 = new PointF(0, 800);    // first control point
PointF c2 = new PointF(1000, 0);   // second control point
PointF p2 = new PointF(1000, 800);  // end point
```

## Étape 3 : Dessiner la spline de Bézier
Utilisez la méthode `DrawBezier` pour dessiner la spline de Bézier sur l’objet `Graphics`.

```csharp
graphics.DrawBezier(pen, p1, c1, c2, p2);
```

## Étape 4 : Enregistrer la sortie
Lorsque vous appelez `bitmap.Save`, vous **enregistrez le bitmap en C#** à l’emplacement que vous spécifiez. Cela écrit l’image sur le disque au format PNG.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawBezierSpline_out.png");
```

## Conseils pour dessiner une courbe de Bézier en C#
- Expérimentez avec différentes coordonnées de points de contrôle pour voir comment la courbe change.  
- Utilisez un `Pen` plus épais (`new Pen(..., 4)`) pour une meilleure visibilité lors du débogage.  
- N’oubliez pas de libérer les objets `Graphics`, `Pen` et `Bitmap` dans un bloc `using` pour un code efficace en mémoire.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **L'image apparaît vide** | Assurez‑vous que le format de pixel du bitmap prend en charge l'alpha (`Format32bppPArgb`). |
| **Erreur fichier introuvable** | Vérifiez que le répertoire cible existe ou créez‑le avec `Directory.CreateDirectory`. |
| **Forme de courbe inattendue** | Vérifiez l'ordre des points de contrôle ; interchanger `c1` et `c2` inverse la courbe. |

## Questions fréquemment posées

**Q : Puis‑je utiliser Aspose.Drawing pour .NET avec d’autres bibliothèques .NET ?**  
R : Oui, Aspose.Drawing s’intègre parfaitement à diverses bibliothèques .NET, améliorant vos capacités graphiques.

**Q : Aspose.Drawing convient‑il aux débutants ?**  
R : Absolument ! Aspose.Drawing offre une interface conviviale, accessible tant aux débutants qu’aux développeurs expérimentés.

**Q : Où puis‑je trouver du support pour Aspose.Drawing ?**  
R : Pour toute question ou assistance, consultez notre [forum de support](https://forum.aspose.com/c/drawing/44).

**Q : Une version d’essai gratuite est‑elle disponible ?**  
R : Oui, vous pouvez explorer Aspose.Drawing avec notre version d’essai gratuite [ici](https://releases.aspose.com/).

**Q : Comment puis‑je acheter Aspose.Drawing pour .NET ?**  
R : Pour acheter, rendez‑vous sur notre [page d’achat](https://purchase.aspose.com/buy).

**Q : Comment changer le format de l’image de sortie ?**  
R : Passez un `ImageFormat` différent (par ex., `ImageFormat.Jpeg`) à la méthode `Save`.

**Q : Puis‑je dessiner plusieurs splines de Bézier sur le même bitmap ?**  
R : Oui, il suffit d’appeler à nouveau `graphics.DrawBezier` avec de nouveaux points avant d’enregistrer.

---

**Dernière mise à jour :** 2026-02-12  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}