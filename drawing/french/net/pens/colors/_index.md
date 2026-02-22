---
date: 2026-02-22
description: Apprenez à définir la couleur du stylo dans Aspose.Drawing pour .NET,
  à tracer des lignes colorées et à enregistrer des images PNG avec des exemples de
  code simples.
linktitle: Working with Colors in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Comment définir la couleur du stylo dans Aspose.Drawing pour .NET
url: /fr/net/pens/colors/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment définir la couleur du stylo dans Aspose.Drawing

## Introduction

Bienvenue dans notre guide étape par étape sur la façon de **définir la couleur du stylo** lors du dessin avec Aspose.Drawing pour .NET. Dans ce tutoriel, vous apprendrez à créer un objet graphics, tracer des lignes colorées et **enregistrer des images PNG** — le tout avec des exemples de code clairs et concrets. Que vous construisiez un utilitaire de bureau ou un service web qui génère des graphiques, maîtriser les couleurs du stylo est essentiel pour produire des graphiques d’aspect professionnel.

## Quick Answers
- **Quelle est la classe principale pour le dessin ?** `Graphics` créé à partir d’un `Bitmap`.
- **Comment changer la couleur d’un stylo ?** Utilisez `Color.FromKnownColor` ou `Color.FromArgb`.
- **Quel format est recommandé pour une sortie sans perte ?** PNG (`.png`).
- **Ai‑je besoin d’une licence pour le développement ?** Une licence temporaire est disponible pour l’évaluation.
- **Puis‑je l’utiliser dans ASP.NET Core ?** Oui, Aspose.Drawing fonctionne avec .NET Core et .NET 5+.

## What is “set pen color” in Aspose.Drawing?

Définir la couleur du stylo signifie attribuer une valeur `Color` à un objet `Pen` avant le dessin. La couleur détermine l’apparence des lignes, formes ou texte sur le canevas. Aspose.Drawing reflète l’API familière System.Drawing, vous pouvez donc utiliser `Color.FromKnownColor`, `Color.FromArgb` ou les propriétés `Color` prédéfinies.

## Why use Aspose.Drawing for color manipulation?

* **Prise en charge multiplateforme** – fonctionne sous Windows, Linux et macOS sans les limitations de System.Drawing.Common.  
* **Compatibilité .NET complète** – s’intègre parfaitement aux projets .NET 6, .NET Core et .NET Framework.  
* **API de couleur riches** – création facile de couleurs ARGB personnalisées, de couleurs connues et de pinceaux dégradés.  
* **Sortie PNG de haute qualité** – idéale pour les graphiques web, les rapports et les vignettes.

## Prerequisites

Before we dive into the code, ensure you have:

1. **Bibliothèque Aspose.Drawing** – téléchargez et installez depuis le site officiel **[here](https://releases.aspose.com/drawing/net/)**.  
2. **Un environnement de développement .NET** – Visual Studio, VS Code ou tout IDE de votre choix.  
3. **Connaissances de base en C#** – familiarité avec les classes, objets et espaces de noms.

## Import Namespaces

Dans votre fichier C#, importez l’espace de noms qui vous donne accès aux primitives de dessin d’Aspose.Drawing.

```csharp
using System.Drawing;
```

## Step 1: Create a Bitmap (the canvas)

Un `Bitmap` représente le tampon de pixels sur lequel nous allons dessiner. Ici, nous créons un canevas de 1000 × 800 avec un format de pixel ARGB 32 bits.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Step 2: Create a Graphics object

L’objet `Graphics` est la surface de dessin qui vous permet de rendre des formes, du texte et des images sur le bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Step 3: Draw a line with a blue pen (first colored line)

Nous **définissons la couleur du stylo** en bleu à l’aide de `Color.FromKnownColor`. L’épaisseur du stylo est réglée à 2 pixels.

```csharp
Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawLine(bluePen, 100, 100, 900, 100);
```

## Step 4: Draw a line with a custom red pen

Cet exemple montre comment **dessiner des lignes colorées** avec une valeur ARGB personnalisée, vous offrant un contrôle total sur l’opacité et la teinte exacte.

```csharp
Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
graphics.DrawLine(redPen, 100, 200, 900, 200);
```

## Step 5: Save the image as PNG

Enfin, nous **enregistrons l’image PNG** dans le dossier souhaité. Ajustez le chemin pour qu’il corresponde au répertoire de sortie de votre projet.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
```

## Common Issues and Solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **L’image apparaît vide** | Graphics non vidé avant l’enregistrement | Appelez `graphics.Dispose();` ou encapsulez `Graphics` dans un bloc `using`. |
| **Couleurs incorrectes** | Utilisation de `FromKnownColor` avec une mauvaise énumération | Vérifiez la valeur de l’énumération ou utilisez `FromArgb` pour un contrôle précis. |
| **Erreurs de chemin de fichier** | Répertoire invalide ou permissions manquantes | Assurez‑vous que le dossier cible existe et que l’application dispose des droits d’écriture. |

## Frequently Asked Questions

**Q : Puis‑je utiliser Aspose.Drawing avec d’autres bibliothèques .NET ?**  
R : Oui, Aspose.Drawing s’intègre parfaitement avec d’autres bibliothèques .NET, offrant un environnement polyvalent pour la manipulation graphique.

**Q : Comment obtenir une licence temporaire pour Aspose.Drawing ?**  
R : Vous pouvez obtenir une licence temporaire **[here](https://purchase.aspose.com/temporary-license/)**, vous permettant d’explorer le plein potentiel d’Aspose.Drawing.

**Q : Aspose.Drawing prend‑il en charge des formats d’image autres que PNG ?**  
R : Oui, Aspose.Drawing prend en charge divers formats d’image, y compris JPEG, GIF, BMP, etc. Consultez la documentation pour la liste complète.

**Q : Puis‑je utiliser Aspose.Drawing pour le développement web ?**  
R : Absolument ! Aspose.Drawing est polyvalent et peut être utilisé tant dans les applications de bureau que web, ajoutant des fonctionnalités graphiques dynamiques à vos sites.

**Q : Existe‑t‑il un essai gratuit pour Aspose.Drawing ?**  
R : Oui, vous pouvez explorer un essai gratuit **[here](https://releases.aspose.com/drawing/net/)**, vous permettant de découvrir les capacités d’Aspose.Drawing avant d’effectuer un achat.

## Conclusion

Dans ce tutoriel, nous avons vu comment **définir la couleur du stylo**, **dessiner des lignes colorées**, **créer un objet graphics** et **enregistrer le résultat en PNG** avec Aspose.Drawing pour .NET. Ces bases ouvrent la voie à des scénarios plus avancés tels que le dessin de formes, le rendu de texte et la génération dynamique de graphiques. Si vous rencontrez des difficultés, la **[documentation](https://reference.aspose.com/drawing/net/)** d’Aspose.Drawing et le **[forum de support](https://forum.aspose.com/c/drawing/44)** sont d’excellents endroits pour trouver des réponses.

---

**Last Updated:** 2026-02-22  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}