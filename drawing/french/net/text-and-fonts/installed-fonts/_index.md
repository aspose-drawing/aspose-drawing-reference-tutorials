---
date: 2026-02-25
description: Apprenez à créer des graphiques bitmap en C# et à enregistrer des images
  PNG tout en répertoriant les polices installées, en dessinant du texte avec les
  polices et en ajustant la résolution du bitmap à l’aide d’Aspose.Drawing pour .NET.
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Créer des graphiques bitmap C# – Enregistrer une image PNG et travailler avec
  les polices installées dans Aspose.Drawing
url: /fr/net/text-and-fonts/installed-fonts/
weight: 13
---

 intégrez des polices personnalisées dans votre application. |
| **Fichier enregistré corrompu** | Format de pixel incorrect ou permissions d’écriture manquantes. | Assurez‑vous que le dossier cible existe et que l’application a les droits d’écriture ; conservez `Format32bppPArgb`. |
| **Le texte apparaît flou** | Paramètres DPI faibles. | Augmentez les dimensions du bitmap ou définissez `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

Make sure to keep backticks.

Now final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer une image PNG et travailler avec les polices installées dans Aspose.Drawing

## Introduction

Si vous devez **save PNG image** tout en **create bitmap graphics C#**, Aspose.Drawing pour .NET vous offre une méthode propre et multiplateforme pour le faire. Dans ce tutoriel, nous passerons en revue **list installed fonts**, **show font families**, la création de graphiques à partir d’un bitmap et le **draw text with fonts** — le tout en enregistrant finalement le résultat sous forme d’image PNG. À la fin, vous disposerez d’un extrait réutilisable que vous pourrez intégrer à n’importe quel projet .NET.

## Réponses rapides
- **What does this tutorial create?** Une image PNG qui répertorie les familles de polices installées.  
- **Which library is required?** Aspose.Drawing pour .NET (pas besoin de System.Drawing.Common).  
- **Can I use custom fonts?** Oui – il suffit de les charger dans un `InstalledFontCollection`.  
- **Is the output resolution adjustable?** Absolument – modifiez la taille du bitmap ou le format de pixel pour **adjust bitmap resolution C#**.  
- **Do I need a license to run the code?** Une licence temporaire suffit pour l’évaluation ; une licence complète est requise pour la production.

## Qu’est‑ce que “save PNG image” dans le contexte d’Aspose.Drawing ?

Enregistrer une image PNG signifie rendre votre surface de dessin (un `Bitmap`) dans un fichier avec l’extension `.png`. Aspose.Drawing gère l’encodage pour vous, vous n’avez donc qu’à appeler `bitmap.Save(...)` avec le chemin souhaité.

## Pourquoi répertorier les polices installées et afficher les familles de polices ?

Savoir quelles polices sont disponibles vous permet de créer des graphiques dynamiques qui s’adaptent à l’environnement de l’utilisateur final. C’est particulièrement utile pour générer des rapports, des certificats ou tout contenu visuel qui doit correspondre à l’identité visuelle de l’entreprise sans devoir fournir les fichiers de police.

## Comment créer des bitmap graphics C# avec Aspose.Drawing ?

Voici un guide pratique, étape par étape, qui montre exactement comment **create bitmap graphics C#**, dessiner du texte avec des polices et ajuster la résolution du bitmap si nécessaire.

## Prérequis

- **Aspose.Drawing Library** – téléchargez la dernière version depuis la [page de téléchargement Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider ou tout éditeur compatible .NET.  
- **Basic C# knowledge** – vous devez être à l’aise avec les classes, les objets et les boucles simples.

## Importer les espaces de noms
Pour travailler avec les polices et les graphiques, importez ces espaces de noms en haut de votre fichier C# :

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Guide étape par étape

### Étape 1 : Créer un bitmap (le canevas)
Tout d’abord, nous créons un bitmap qui contiendra l’image finale. La taille du bitmap et le format de pixel déterminent la qualité du PNG enregistré et vous permettent de **adjust bitmap resolution C#**.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Étape 2 : Créer un objet Graphics à partir du bitmap
Ensuite, nous obtenons un objet `Graphics` à partir du bitmap. Cet objet nous permet de dessiner des formes, du texte et des images sur le canevas.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Étape 3 : Configurer le pinceau et la police (draw text with fonts)
Nous avons besoin d’un pinceau pour la couleur du texte et d’un objet `Font` qui définit la police, la taille et le style. C’est ici que nous **draw text with fonts**.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Étape 4 : List installed fonts et show font families
Nous affichons maintenant le nombre de familles de polices et les premiers noms directement sur le bitmap. Cela démontre les capacités de **list installed fonts** et **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Étape 5 : Save PNG image
Enfin, nous écrivons le bitmap sur le disque sous forme de fichier PNG. Il s’agit de l’opération principale **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Astuce :** Utilisez `Path.Combine` pour construire les chemins de fichiers afin d’éviter les problèmes de séparateurs de répertoires sur différents systèmes d’exploitation.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Aucune police affichée** | `InstalledFontCollection` non remplie (par ex., exécution sur un serveur sans tête dépourvu de polices). | Installez les polices requises sur le serveur ou intégrez des polices personnalisées dans votre application. |
| **Fichier enregistré corrompu** | Format de pixel incorrect ou permissions d’écriture manquantes. | Assurez‑vous que le dossier cible existe et que l’application a les droits d’écriture ; conservez `Format32bppPArgb`. |
| **Le texte apparaît flou** | Paramètres DPI faibles. | Augmentez les dimensions du bitmap ou définissez `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Questions fréquentes

**Q : Puis‑je utiliser des polices personnalisées qui ne sont pas installées sur la machine ?**  
R : Oui. Chargez le fichier de police dans une `PrivateFontCollection` et créez une `Font` à partir de cette collection.

**Q : Comment gérer les exceptions liées aux polices ?**  
R : Enveloppez la création de la police dans un bloc `try/catch` et examinez `ArgumentException` pour les familles manquantes.

**Q : Aspose.Drawing est‑il adapté aux applications web ?**  
R : Absolument. La bibliothèque fonctionne dans ASP.NET Core, Azure Functions et d’autres environnements côté serveur.

**Q : Puis‑je changer la couleur ou le style du texte ?**  
R : Oui. Utilisez différents types de `Brush` (par ex., `LinearGradientBrush`) et modifiez l’énumération `FontStyle`.

**Q : Où puis‑je obtenir une licence temporaire pour les tests ?**  
R : Téléchargez une licence d’essai depuis la [page de licence temporaire Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusion

En suivant ces étapes, vous avez appris à **save PNG image** des fichiers qui **list installed fonts** dynamiquement, **show font families**, **create graphics from bitmap**, et **draw text with fonts** en utilisant Aspose.Drawing pour .NET. Vous savez maintenant comment **create bitmap graphics C#**, ajuster la résolution du bitmap et incorporer des polices personnalisées si nécessaire. N’hésitez pas à expérimenter d’autres polices, couleurs et tailles de bitmap pour répondre aux exigences visuelles de votre projet.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose