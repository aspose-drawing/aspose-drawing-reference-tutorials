---
date: 2026-03-02
description: Améliorez les illustrations de vos documents avec Aspose.Drawing pour
  .NET ! Apprenez étape par étape comment ajouter des annotations pour des visuels
  plus clairs et informatifs.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Comment ajouter des annotations avec Aspose.Drawing pour .NET
url: /fr/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer des callouts dans Aspose.Drawing

## Introduction
Si vous vous demandez **comment ajouter des callouts** à vos images ou diagrammes en utilisant Aspose.Drawing pour .NET, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons l’ensemble du processus — du chargement d’une image au dessin de callouts magnifiquement stylisés—afin que vous puissiez rendre vos illustrations plus claires et plus informatives.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.Drawing pour .NET (téléchargeable depuis le site officiel).  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Combien de temps prend l’implémentation ?** Généralement moins de 10 minutes pour un callout de base.  
- **Puis‑je personnaliser les couleurs et les polices ?** Oui — tout est piloté par les objets GDI+ standards (Pen, Font, Brush).

## Comment ajouter des callouts dans Aspose.Drawing
Voici un guide concis, étape par étape, qui montre exactement **comment ajouter des callouts** à une image. N’hésitez pas à copier le code, à expérimenter les positions et à adapter le style pour correspondre à votre identité visuelle.

## Prérequis
Avant de commencer, assurez‑vous d’avoir :

- Des connaissances de base en langage de programmation C#.  
- La bibliothèque Aspose.Drawing installée. Vous pouvez la télécharger [ici](https://releases.aspose.com/drawing/net/).  
- Un document ou une image sur laquelle vous souhaitez ajouter des callouts.

## Importer les espaces de noms
Assurez‑vous d’inclure les espaces de noms nécessaires dans votre projet :

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Étape 1 : charger l’image
Commencez par charger l’image dans laquelle vous voulez ajouter des callouts. Remplacez `"Your Document Directory"` et `"gears.png"` par votre répertoire réel et le nom de fichier de l’image.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Étape 2 : créer l’objet Graphics
Créez un objet `Graphics` à partir de l’image pour effectuer les opérations de dessin.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Étape 3 : définir les positions des callouts
Définissez les points de départ et d’arrivée pour chaque callout ainsi que la valeur et l’unité du callout.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## Étape 4 : dessiner les callouts
Implémentez la méthode `DrawCallOut` pour dessiner les callouts sur l’image.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Étape 5 : enregistrer l’image
Enregistrez l’image contenant les callouts dans le répertoire de votre choix.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Code source du callout
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## Problèmes courants et astuces
- **Coordonnées d’ancrage incorrectes** – assurez‑vous que les points de départ et d’arrivée se trouvent à l’intérieur des limites de l’image ; sinon le callout pourrait être tronqué.  
- **Chevauchement du texte** – ajustez `spaceSize` ou la taille de la police si l’étiquette entre en collision avec d’autres graphiques.  
- **Performance** – pour les images très volumineuses, pensez à libérer les objets `Pen`, `Font` et `Brush` après utilisation afin de libérer les ressources.

## Conclusion
Félicitations ! Vous savez maintenant **comment ajouter des callouts** à une image en utilisant Aspose.Drawing pour .NET. N’hésitez pas à expérimenter différentes positions, couleurs et polices pour adapter le rendu à votre style visuel.

## FAQ

### Puis‑je utiliser Aspose.Drawing pour d’autres types d’illustrations ?
Oui, Aspose.Drawing prend en charge un large éventail d’opérations de dessin pour divers types d’illustrations.

### Aspose.Drawing est‑il compatible avec différents formats d’image ?
Absolument ! Aspose.Drawing supporte les formats d’image populaires tels que PNG, JPEG, GIF, et bien d’autres.

### Où puis‑je trouver plus d’exemples et de documentation ?
Explorez la documentation complète [ici](https://reference.aspose.com/drawing/net/).

### Comment obtenir de l’aide si je rencontre des problèmes ?
Visitez le [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pour obtenir du support communautaire.

### Puis‑je essayer Aspose.Drawing avant d’acheter ?
Bien sûr ! Commencez avec un essai gratuit [ici](https://releases.aspose.com/).

**Questions supplémentaires & Réponses**

**Q : Puis‑je changer le style de ligne du callout (pointillé, tireté) ?**  
**R :** Oui—il suffit de configurer la propriété `Pen.DashStyle` avant de tracer la ligne.

**Q : Est‑il possible d’ajouter une couleur d’arrière‑plan à l’étiquette du callout ?**  
**R :** Tout à fait. Créez un `SolidBrush` avec la couleur souhaitée et remplissez un rectangle derrière le texte avant d’appeler `DrawString`.

**Q : Comment garantir que le callout ait le même aspect sur des écrans haute‑DPI ?**  
**R :** Définissez `graphics.PageUnit = GraphicsUnit.Pixel` (comme indiqué) et utilisez des mesures basées sur des vecteurs pour conserver une mise à l’échelle cohérente.

---

**Dernière mise à jour :** 2026-03-02  
**Testé avec :** Aspose.Drawing 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}