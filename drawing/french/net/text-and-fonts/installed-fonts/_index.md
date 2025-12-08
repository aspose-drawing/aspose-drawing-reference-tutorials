---
date: 2025-12-06
description: Apprenez à enregistrer des fichiers image PNG tout en répertoriant les
  polices installées, en affichant les familles de polices, en créant des graphiques
  à partir d’un bitmap et en dessinant du texte avec des polices à l’aide d’Aspose.Drawing
  pour .NET.
language: fr
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Enregistrer une image PNG et travailler avec les polices installées dans Aspose.Drawing
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer une image PNG et travailler avec les polices installées dans Aspose.Drawing

## Introduction

Si vous devez **enregistrer des fichiers image PNG** qui affichent également des informations sur les polices installées sur une machine, Aspose.Drawing pour .NET vous offre une méthode propre et multiplateforme pour le faire. Dans ce tutoriel, nous passerons en revue la liste des polices installées, l’affichage des familles de polices, la création de graphiques à partir d’un bitmap, et le dessin de texte avec des polices — le tout en enregistrant finalement le résultat sous forme d’image PNG. À la fin, vous disposerez d’un extrait réutilisable que vous pourrez intégrer à n’importe quel projet .NET.

## Réponses rapides
- **Que crée ce tutoriel ?** Une image PNG qui répertorie les familles de polices installées.  
- **Quelle bibliothèque est requise ?** Aspose.Drawing pour .NET (pas besoin de System.Drawing.Common).  
- **Puis‑je utiliser des polices personnalisées ?** Oui – il suffit de les charger dans un `InstalledFontCollection`.  
- **La résolution de sortie est‑elle réglable ?** Absolument – modifiez la taille du bitmap ou le format de pixel.  
- **Ai‑je besoin d’une licence pour exécuter le code ?** Une licence temporaire suffit pour l’évaluation ; une licence complète est requise en production.

## Qu’est‑ce que « save PNG image » dans le contexte d’Aspose.Drawing ?
Enregistrer une image PNG signifie rendre votre surface de dessin (un `Bitmap`) dans un fichier avec l’extension `.png`. Aspose.Drawing se charge de l’encodage, vous n’avez qu’à appeler `bitmap.Save(...)` avec le chemin souhaité.

## Pourquoi lister les polices installées et afficher les familles de polices ?
Savoir quelles polices sont disponibles vous permet de créer des graphiques dynamiques qui s’adaptent à l’environnement de l’utilisateur final. C’est particulièrement utile pour générer des rapports, des certificats ou tout contenu visuel qui doit respecter l’identité visuelle de l’entreprise sans devoir distribuer les fichiers de police.

## Prérequis

- **Bibliothèque Aspose.Drawing** – téléchargez la dernière version depuis la [page de téléchargement Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider ou tout éditeur compatible .NET.  
- **Connaissances de base en C#** – vous devez être à l’aise avec les classes, les objets et les boucles simples.

## Importer les espaces de noms
Pour travailler avec les polices et les graphiques, importez ces espaces de noms en haut de votre fichier C# :

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Guide étape par étape

### Étape 1 : Créer un bitmap (le canevas)
Tout d’abord, nous créons un bitmap qui contiendra l’image finale. La taille du bitmap et le format de pixel déterminent la qualité du PNG enregistré.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Étape 2 : Créer un graphique à partir du bitmap
Ensuite, nous obtenons un objet `Graphics` à partir du bitmap. Cet objet nous permet de dessiner des formes, du texte et des images sur le canevas.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Étape 3 : Configurer le pinceau et la police (dessiner du texte avec des polices)
Nous avons besoin d’un pinceau pour la couleur du texte et d’un objet `Font` qui définit la police, la taille et le style.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Étape 4 : Lister les polices installées et afficher les familles de polices
Nous affichons maintenant le nombre de familles de polices et les premiers noms directement sur le bitmap. Cela illustre les capacités **list installed fonts** et **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Étape 5 : Enregistrer l’image PNG
Enfin, nous écrivons le bitmap sur le disque sous forme de fichier PNG. C’est l’opération centrale **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Astuce :** Utilisez `Path.Combine` pour construire les chemins de fichiers afin d’éviter les problèmes de séparateurs de répertoires sur différents systèmes d’exploitation.

## Problèmes courants et solutions
| Problème | Cause | Solution |
|----------|-------|----------|
| **Aucune police affichée** | `InstalledFontCollection` non remplie (par ex., exécution sur un serveur sans affichage). | Installez les polices requises sur le serveur ou intégrez des polices personnalisées dans votre application. |
| **Le fichier enregistré est corrompu** | Format de pixel incorrect ou permissions d’écriture manquantes. | Assurez‑vous que le dossier cible existe et que l’application possède les droits d’écriture ; conservez `Format32bppPArgb`. |
| **Le texte apparaît flou** | Paramètres DPI faibles. | Augmentez les dimensions du bitmap ou définissez `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Foire aux questions

**Q : Puis‑je utiliser des polices personnalisées qui ne sont pas installées sur la machine ?**  
R : Oui. Chargez le fichier de police dans un `PrivateFontCollection` et créez une `Font` à partir de cette collection.

**Q : Comment gérer les exceptions liées aux polices ?**  
R : Enveloppez la création de la police dans un bloc `try/catch` et examinez `ArgumentException` pour les familles manquantes.

**Q : Aspose.Drawing est‑il adapté aux applications web ?**  
R : Absolument. La bibliothèque fonctionne avec ASP.NET Core, Azure Functions et d’autres environnements côté serveur.

**Q : Puis‑je changer la couleur ou le style du texte ?**  
R : Oui. Utilisez différents types de `Brush` (par ex., `LinearGradientBrush`) et modifiez l’énumération `FontStyle`.

**Q : Où puis‑je obtenir une licence temporaire pour les tests ?**  
R : Téléchargez une licence d’essai depuis la [page de licence temporaire Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusion

En suivant ces étapes, vous avez appris à **enregistrer des fichiers image PNG** qui répertorient dynamiquement les **polices installées**, **affichent les familles de polices**, **créent des graphiques à partir d’un bitmap** et **dessinent du texte avec des polices** en utilisant Aspose.Drawing pour .NET. N’hésitez pas à expérimenter avec d’autres polices, couleurs et tailles de bitmap pour répondre aux exigences visuelles de votre projet.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2025-12-06  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose