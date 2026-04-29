---
date: 2026-02-09
description: Apprenez à configurer la licence Aspose.Drawing dans .NET. Maîtrisez
  les méthodes de licence pour débloquer toutes les fonctionnalités sans filigranes.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Définir la licence Aspose.Drawing – Comment définir la licence Aspose.Drawing
url: /fr/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la licence Aspose.Drawing

## Introduction

Si vous développez des applications .NET qui s'appuient sur des graphiques puissants et la manipulation d'images, **définir une licence Aspose.Drawing** est la première étape pour supprimer les limitations d'évaluation et accéder à l'ensemble complet des fonctionnalités. Dans ce tutoriel, vous apprendrez trois méthodes pratiques pour définir la licence Aspose.Drawing — chargement depuis un fichier, chargement depuis un flux, et utilisation du modèle d'utilisation mesurée—afin d'intégrer la bibliothèque en toute confiance.

## Quick Answers
- **Quelle est la façon principale d'activer Aspose.Drawing ?** Chargez un fichier de licence en utilisant `License.SetLicense("Aspose.Drawing.lic")`.  
- **Puis-je appliquer une licence à l'exécution ?** Oui, vous pouvez charger la licence depuis un `Stream` pour des scénarios dynamiques.  
- **Une licence mesurée est‑elle prise en charge ?** Absolument ; utilisez `Metered.SetMeteredKey(publicKey, privateKey)` pour activer la facturation basée sur la consommation.  
- **Ai‑je besoin d'une licence pour les builds de développement ?** Une version d'essai fonctionne pour les tests, mais une licence valide supprime les filigranes et débloque toutes les API.  
- **Quelles versions de .NET sont compatibles ?** Aspose.Drawing prend en charge .NET Framework 4.x, .NET Core 3.1+ et .NET 5/6+.

## Prerequisites

Avant de commencer, assurez‑vous d'avoir :

- **Bibliothèque Aspose.Drawing** – téléchargez le dernier package depuis [here](https://releases.aspose.com/drawing/net/).  
- **Fichier de licence** – obtenez un fichier `.lic` valide depuis [Aspose](https://purchase.aspose.com/buy).  
- **Environnement de développement .NET** – Visual Studio, Rider, ou tout IDE ciblant .NET Framework/.NET Core.

## Import Namespaces

Nous avons besoin des espaces de noms .NET standard ainsi que de l'espace de noms Aspose.Drawing pour la licence. Ajoutez les instructions `using` suivantes en haut de votre fichier C# :

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Loading License from a File

Charger une licence depuis un fichier est l'approche la plus simple. Suivez ces trois étapes :

### Étape 1 : Initialiser l'objet License

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Étape 2 : Définir la licence depuis le fichier `.lic`

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Étape 3 : Confirmer le succès

```csharp
Console.WriteLine("License set successfully.");
```

> **Astuce :** Placez le fichier `.lic` dans le même dossier que votre exécutable ou fournissez un chemin absolu pour éviter les erreurs « file not found ».

## Loading License from a Stream

Lorsque votre fichier de licence est intégré en tant que ressource ou récupéré depuis un emplacement distant, le charger depuis un `Stream` vous offre de la flexibilité.

### Étape 1 : Initialiser l'objet License

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Étape 2 : Charger la licence en utilisant un `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Étape 3 : Confirmer le succès

```csharp
Console.WriteLine("License set successfully.");
```

> **Avertissement** : N'oubliez pas de libérer le `FileStream` (ou d'utiliser un bloc `using`) pour libérer les poignées de fichier.

## Using Metered License

La licence mesurée est idéale pour les scénarios SaaS ou pay‑per‑use. Elle suit la consommation et vous facture en fonction de l'utilisation réelle.

### Étape 1 : Initialiser l'objet Metered

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Étape 2 : Définir les clés publiques et privées

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Étape 3 : Effectuer votre traitement d'image

```csharp
// Your image processing logic here
```

### Étape 4 : Récupérer les informations de consommation

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Étape 5 : Afficher les détails de consommation

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Piège courant** : Si vous oubliez d'appeler `SetMeteredKey`, l'API reviendra en mode d'essai et vous verrez des filigranes dans la sortie.

## Why Set the Aspose.Drawing License Correctly?

- **Supprime les filigranes** qui apparaissent en mode d'essai.  
- **Débloque les API premium** telles que les filtres d'image avancés et la conversion PDF.  
- **Assure la conformité** aux conditions de licence d'Aspose pour la distribution commerciale.  
- **Active la facturation mesurée**, vous permettant de ne payer que ce que vous utilisez.

## Common Issues and Solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| “License file not found” error | Chemin incorrect ou fichier manquant dans le dossier de sortie | Utilisez un chemin absolu ou définissez la propriété *Copy to Output Directory* du fichier sur *Copy always*. |
| Le filigrane apparaît toujours après la définition de la licence | Licence non chargée avant le premier appel API | Chargez la licence **avant** toute opération Aspose.Drawing. |
| La consommation mesurée est toujours zéro | Clés non définies ou variables d'environnement incorrectes | Vérifiez les clés publiques/privées et assurez-vous d'une connectivité Internet pour le serveur de licence mesurée d'Aspose. |

## Frequently Asked Questions

**Q1 : Puis‑je utiliser Aspose.Drawing sans licence ?**  
R1 : Oui, une licence d'essai fonctionne pour le développement et l'évaluation, mais elle ajoute des filigranes et limite certaines fonctionnalités.

**Q2 : À quelle fréquence dois‑je renouveler ma licence Aspose.Drawing ?**  
R2 : Les licences sont perpétuelles pour la version achetée. Le renouvellement n'est requis que pour le support et les mises à jour.

**Q3 : Qu'est‑ce que la licence mesurée, et quand devrais‑je l'utiliser ?**  
R3 : La licence mesurée facture en fonction de l'utilisation (opérations ou données traitées). Elle est idéale pour les services cloud ou les modèles pay‑per‑use.

**Q4 : Puis‑je utiliser Aspose.Drawing dans des projets commerciaux ?**  
R4 : Absolument—une fois que vous avez une licence valide, vous pouvez intégrer Aspose.Drawing dans n'importe quelle application commerciale.

**Q5 : Où puis‑je trouver du support communautaire pour Aspose.Drawing ?**  
R5 : Consultez le [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) pour obtenir de l'aide communautaire, des exemples et des discussions.

## Conclusion

Maîtriser la façon de **définir la licence Aspose.Drawing**—que ce soit depuis un fichier, un flux, ou via l'utilisation mesurée—vous assure de tirer le meilleur parti de cette puissante bibliothèque graphique .NET. Suivez les étapes ci‑dessus, évitez les pièges courants, et vous serez prêt à créer des solutions de traitement d'images robustes sans aucun obstacle de licence.

---

**Dernière mise à jour :** 2026-02-09  
**Testé avec :** Aspose.Drawing 24.11 for .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}