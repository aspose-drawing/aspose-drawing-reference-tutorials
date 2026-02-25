---
date: 2026-02-25
description: Aspose.Drawing for .NET を使用してテキストの描画と動的テキスト画像の作成方法を学びましょう。このステップバイステップガイドでは、ビットマップにテキストを追加し、画像上に文字列を描画し、ビットマップを
  PNG として保存する方法を示します。
linktitle: How to Draw Text with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: .NET 用 Aspose.Drawing でテキストを描画する方法
url: /ja/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET でテキストを描画する方法

## Introduction

このステップバイステップガイドでは、Aspose.Drawing for .NET を使用して画像に **テキストを描画する方法** を学びます。*動的テキスト画像* を作成したり、既存のビットマップにテキストを追加したり、カスタムフォントでグラフィックを生成したりする必要がある場合でも、このチュートリアルはすべての詳細を解説し、数分でテキスト描画を開始できるようにします。

## Quick Answers
- **使用ライブラリは？** Aspose.Drawing for .NET  
- **主なタスクは？** 画像にテキストを描画する（テキスト付き画像を作成）  
- **主要メソッドは？** `Graphics.DrawString`（画像上に文字列を描画）  
- **出力形式は？** PNG（ビットマップを PNG で保存）  
- **前提条件は？** .NET 開発環境と Aspose.Drawing ライブラリ  

## What is drawing text with Aspose.Drawing?
Aspose.Drawing は、従来の GDI+ モデルを鏡写しにした完全マネージド API を提供し、クロスプラットフォーム対応を追加します。System.Drawing.Common に依存せずに、高品質なテキスト、シェイプ、画像をレンダリングできます。

## Why use Aspose.Drawing to add text to images?
- **クロスプラットフォームの信頼性** – Windows、Linux、macOS で動作  
- **高度なレンダリング** – アンチエイリアスとサブピクセルテキストスムージングにより鮮明な出力  
- **外部依存なし** – ライブラリに *テキスト付き画像を作成* するために必要なすべてが含まれています  

## Prerequisites

開始する前に、以下を用意してください。

- **Aspose.Drawing for .NET** – [Aspose.Drawing ドキュメント](https://reference.aspose.com/drawing/net/) からダウンロード  
- **.NET IDE**（Visual Studio や VS Code など）  

## Import Namespaces

必要な名前空間をインポートします。

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step 1: Create Bitmap and Graphics Objects

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

ここでは、最終的な画像を保持する `Bitmap` と、描画を行う `Graphics` オブジェクトを作成します。アンチエイリアスのヒントによりテキストが滑らかに表示されます。

## Step 2: Set Up Brush, Pen, and Font

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** はテキストの色を定義します。  
- **Pen** は後でテキストの周囲に矩形を描くために使用します（任意）。  
- **Font** は *画像上に文字列を描画* する操作のために、フォントファミリー、サイズ、スタイルを指定します。

## Step 3: Define Text and Rectangle

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` はテキストを配置する領域を決定します。座標とサイズはレイアウトに合わせて調整してください。

## Step 4: Draw Rectangle and Text

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

まず青い矩形で領域をアウトラインし、次に `DrawString` を呼び出して **ビットマップにテキストを追加** します。これが画像上で *テキストを描画* する核心部分です。

## Step 5: Save the Result

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

画像は PNG ファイルとして保存され、*ビットマップを PNG で保存* する要件を満たします。プレースホルダーのパスは、実際にファイルを保存したいフォルダーに置き換えてください。

## Common Use Cases

- **個人名入り証明書** の生成  
- **ウェブギャラリー用の透かし付きサムネイル** の作成  
- **ラベルや注釈を含む動的チャート** の構築  

## Troubleshooting & Tips

- **フォントが見つからない場合** – ホストマシンにフォントがインストールされているか確認するか、プライベートフォントコレクションを使用してください。  
- **テキストが切り取られる場合** – 矩形サイズを大きくするか、フォントサイズを小さくしてください。  
- **パフォーマンスが気になる場合** – 可能な限り同じ `Graphics` オブジェクトを再利用して複数の描画操作を行ってください。

## FAQ's

### Q1: Can I use custom fonts with Aspose.Drawing for .NET?

A1: Yes, you can specify custom fonts when creating the `Font` object in your code.

### Q2: How can I add text effects like bold or italic?

A2: Adjust the `FontStyle` property of the `Font` object. For example, use `FontStyle.Bold` for bold text.

### Q3: Is Aspose.Drawing compatible with .NET Core?

A3: Yes, Aspose.Drawing supports .NET Core, allowing you to use it in cross‑platform applications.

### Q4: Can I draw text on an existing image?

A4: Certainly! Load the existing image using `Bitmap.FromFile()` and then proceed with the text‑drawing steps.

### Q5: Is there a community forum for Aspose.Drawing support?

A5: Yes, you can find support and discuss issues on the [Aspose.Drawing フォーラム](https://forum.aspose.com/c/drawing/44)。

## Frequently Asked Questions

**Q: How do I change the output format to JPEG?**  
A: Replace the `.png` extension with `.jpg` in the `Save` method and optionally specify an `ImageCodecInfo` for JPEG quality.

**Q: Can I draw multi‑line text?**  
A: Yes, include line‑break characters (`\n`) in the string or use `StringFormat` with `FormatFlags.LineLimit`.

**Q: Is there a way to measure text size before drawing?**  
A: Use `Graphics.MeasureString` to get the exact dimensions of the rendered text.

**Q: Does Aspose.Drawing support Unicode characters?**  
A: Absolutely. Provide a font that contains the required glyphs and the library will render them correctly.

**Q: What version of Aspose.Drawing was used for testing?**  
A: The examples were tested with Aspose.Drawing 24.11 for .NET.

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}