---
date: 2026-02-25
description: Apprenez à définir l’alignement du texte dans Aspose.Drawing pour .NET
  et à ajouter du texte aux images. Guide étape par étape avec des exemples.
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Définir l’alignement du texte avec Aspose.Drawing pour .NET
url: /fr/net/text-and-fonts/format-text/
weight: 11
---

 block placeholders.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir l'alignement du texte dans Aspose.Drawing

## Introduction

Lorsqu'il s'agit de **définir l'alignement du texte** et de formater du texte dans vos applications .NET, Aspose.Drawing est la bibliothèque de référence pour les développeurs qui recherchent précision, performances et une API riche. Que vous construisiez un moteur de reporting, un générateur de badges dynamique ou toute solution graphique intensive, pouvoir contrôler la façon dont le texte s'aligne à l'intérieur des formes donne à votre rendu un aspect soigné et professionnel. Dans ce tutoriel, nous parcourrons l’ensemble du processus — de la création d’un canevas bitmap au dessin d’un rectangle avec texte, en passant par la gestion du dépassement, jusqu’à l’enregistrement de l’image.

## Réponses rapides
- **Que signifie « set text alignment » ?** Cela définit comment le texte est positionné horizontalement et verticalement à l'intérieur d'un rectangle de dessin.  
- **Quelle classe contrôle l'alignement ?** `StringFormat` vous permet de définir `Alignment` et `LineAlignment`.  
- **Puis‑je dessiner une chaîne et un rectangle ensemble ?** Oui — utilisez `Graphics.DrawRectangle` suivi de `Graphics.DrawString`.  
- **Comment éviter le dépassement du texte ?** Ajustez la taille du rectangle ou divisez le texte en plusieurs lignes manuellement.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence commerciale Aspose.Drawing est requise pour un usage non‑évaluation.

## Qu’est‑ce que **set text alignment** dans Aspose.Drawing ?

`set text alignment` fait référence à la configuration du positionnement horizontal (`StringAlignment`) et vertical (`LineAlignment`) du texte à l'intérieur d’un `Rectangle` ou de toute région de dessin. En ajustant ces paramètres, vous contrôlez si le texte apparaît aligné à gauche, centré, aligné à droite, en haut, au centre vertical ou en bas.

## Pourquoi utiliser Aspose.Drawing pour l'alignement du texte ?

- **Compatibilité .NET complète** – fonctionne avec .NET Framework, .NET Core et .NET 5/6+.  
- **Rendu pixel‑perfect** – anti‑aliasing et prise en charge du haut DPI dès le départ.  
- **Pas de limitations GDI+** – contrairement à `System.Drawing.Common`, Aspose.Drawing s’exécute dans des conteneurs Linux sans dépendances natives.  
- **Styling riche** – combinez polices, pinceaux, stylos et objets `StringFormat` personnalisés pour des mises en page sophistiquées.

## Prérequis

1. **Bibliothèque Aspose.Drawing** – téléchargez‑la [ici](https://releases.aspose.com/drawing/net/).  
2. **Environnement de développement** – Visual Studio 2022 (ou tout IDE C#).  
3. **Connaissances de base en .NET** – vous devez être à l’aise avec les projets C# et les packages NuGet.

## Importer les espaces de noms

Pour commencer, importez les espaces de noms requis. Ils vous donnent accès aux graphiques, au rendu du texte et aux primitives de dessin.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Étape 1 : Créer les objets Bitmap et Graphics  

Créer un bitmap fournit un canevas sur lequel vous pouvez dessiner. L’objet `Graphics` représente la surface de dessin, et nous activons le rendu texte haute qualité avec `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Étape 2 : Définir **StringFormat** et le style  

Ici nous **définissons l'alignement du texte** en configurant une instance `StringFormat`. Nous préparons également les pinceaux, stylos et la police qui seront utilisés lors du dessin de la chaîne.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Étape 3 : Créer et formater le texte – **how to draw string** et **draw rectangle with text**

Nous composons le texte, définissons le rectangle qui le contiendra, puis dessinons à la fois la bordure du rectangle et la chaîne elle‑même.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Comment gérer le dépassement du texte

Si le `text` fourni dépasse les limites du rectangle, vous avez deux options courantes :

1. **Redimensionner le rectangle** – augmentez `rectangle.Width` ou `rectangle.Height`.  
2. **Diviser le texte** – séparez la chaîne en lignes qui tiennent, puis appelez `DrawString` pour chaque ligne avec des coordonnées Y ajustées.

## Étape 4 : Enregistrer la sortie – **add text to image**

Enfin, écrivez le bitmap sur le disque. Cette étape montre **add text to image** en un seul appel.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Le texte apparaît flou** | Assurez‑vous que `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` est défini. |
| **Le texte est tronqué** | Augmentez la taille du rectangle ou activez la logique de retour à la ligne en mesurant la taille de la chaîne (`Graphics.MeasureString`). |
| **Police introuvable** | Vérifiez que la police est installée sur la machine hôte ou intégrez une police privée avec `PrivateFontCollection`. |
| **Couleurs inattendues** | Revérifiez les couleurs des pinceaux et stylos ; rappelez‑vous que `Color.FromKnownColor` utilise des couleurs définies par le système. |

## Questions fréquentes

### Q1 : Aspose.Drawing est‑il compatible avec toutes les versions .NET ?

R1 : Oui, Aspose.Drawing est conçu pour être compatible avec un large éventail de versions .NET, offrant ainsi une grande flexibilité aux développeurs.

### Q2 : Puis‑je personnaliser davantage le style de police ?

R2 : Absolument ! Ajustez les paramètres de l’objet `Font` pour obtenir la taille, le style et la famille de police souhaités.

### Q3 : Comment gérer le dépassement du texte dans le rectangle défini ?

R3 : Vous pouvez gérer le dépassement en ajustant la taille du rectangle ou en implémentant une logique personnalisée pour traiter les textes longs.

### Q4 : Existe‑t‑il d’autres options de formatage dans Aspose.Drawing ?

R4 : Oui, Aspose.Drawing propose un ensemble complet d’outils de manipulation graphique, incluant diverses options de formatage pour le texte, les formes, et plus encore.

### Q5 : Où puis‑je trouver un support supplémentaire pour Aspose.Drawing ?

R5 : Explorez le forum Aspose.Drawing [ici](https://forum.aspose.com/c/drawing/44) pour obtenir de l’aide communautaire et des discussions.

**Questions‑Réponses supplémentaires**

**Q : Comment dessiner une chaîne sans rectangle environnant ?**  
R : Omettez l’appel `DrawRectangle` et transmettez la position `PointF` souhaitée à `Graphics.DrawString`.

**Q : Puis‑je faire pivoter le texte tout en conservant l'alignement ?**  
R : Oui—appliquez une transformation `Matrix` à l’objet `Graphics` avant le dessin, puis réinitialisez‑la ensuite.

**Q : Est‑il possible d’exporter l’image en JPEG au lieu de PNG ?**  
R : Changez simplement l’extension du fichier dans `bitmap.Save` et spécifiez éventuellement `ImageFormat.Jpeg`.

---

**Dernière mise à jour :** 2026-02-25  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}