---
date: 2026-09-23
description: Aspose.Drawing for .NET を使用して画像にテキストを描画する方法を学びます。テキスト付き画像を生成し、ビットマップにテキストを追加し、カスタムフォントで
  PNG としてビットマップを保存します。
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Aspose.Drawing でテキストを描画する方法
og_description: Aspose.Drawing for .NET を使用して画像にテキストを描画する方法を学びます。このチュートリアルでは、テキスト付き画像の生成、ビットマップへのテキスト追加、カスタムフォントで
  PNG としてビットマップを保存する手順を示します。
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Aspose.Drawing for .NET を使用した画像へのテキスト描画 – クイックガイド
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Aspose.Drawing for .NET を使用した画像へのテキスト描画方法
url: /ja/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET を使用して画像にテキストを描画する方法

## はじめに

このステップバイステップ ガイドでは、Aspose.Drawing for .NET を使用して **画像にテキストを描画する方法** を学びます。*動的テキスト画像* を作成したり、既存のビットマップにテキストを追加したり、カスタムフォントでグラフィックを生成したりしたい場合でも、このチュートリアルはすべての詳細を解説し、数分でテキスト描画を開始できるようにします。このライブラリは 30 以上の GDI+ メソッドをサポートし、Windows、Linux、macOS 上で動作し、**外部依存関係がゼロ** であるため、サーバーサイドの画像生成に信頼できる選択肢です。

## クイック回答
- **使用ライブラリは？** Aspose.Drawing for .NET  
- **主なタスクは？** 画像にテキストを描画する（テキスト付き画像の作成）  
- **主要メソッドは？** `Graphics.DrawString`（画像上に文字列を描画）  
- **出力形式は？** PNG（ビットマップを PNG として保存）  
- **前提条件は？** .NET 開発環境と Aspose.Drawing ライブラリ  

## Aspose.Drawing でテキストを描画するとは？

Aspose.Drawing でテキストを描画するとは、ライブラリの GDI+ 互換 API を使用して Unicode 文字列をラスタ キャンバスにレンダリングすることを意味します。`Graphics.DrawString` メソッドはテキストをビットマップに書き込み、フォント、色、配置、アンチエイリアスを制御できます。このアプローチにより、System.Drawing.Common をインストールせずに高品質な画像を生成できます。

## なぜ Aspose.Drawing を使用して画像にテキストを追加するのか？

Aspose.Drawing は、ネイティブ GDI+ ライブラリを必要とせずに画像上にテキストをレンダリングできる、信頼性の高いクロスプラットフォーム ソリューションを提供します。あらゆる OS で一貫した品質とパフォーマンスを実現し、先進的なアンチエイリアシング、Unicode 文字、カスタムフォントをサポートし、.NET アプリケーションとシームレスに統合できるため、サーバーサイドの画像生成やデスクトップ ツールに最適です。

- **クロスプラットフォームの信頼性** – Windows、Linux、macOS で動作  
- **高度なレンダリング** – アンチエイリアシングとサブピクセル テキスト スムージングで鮮明な出力  
- **外部依存関係なし** – ライブラリに必要なものがすべて含まれ、*テキスト付き画像の作成* が可能  

## 前提条件

開始する前に以下を用意してください。

- **Aspose.Drawing for .NET** – [Aspose.Drawing ドキュメント](https://reference.aspose.com/drawing/net/) からダウンロード  
- **.NET IDE**（例: Visual Studio または VS Code）  

## 名前空間のインポート

必要な名前空間をインポートします。

これらの名前空間は `Bitmap`、`Graphics`、テキスト描画ユーティリティなど、コア GDI+ 型を提供します。  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 手順 1: ビットマップとグラフィックス オブジェクトの作成

`Bitmap` は Aspose.Drawing のピクセル データを保持するラスタ 画像コンテナで、`Graphics` は形状やテキストを描画するメソッドを提供します。

`Bitmap` はメモリ上の画像を表し、`Graphics` はそのビットマップ上に描画するためのメソッドを提供します。  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

ここでは、最終的な画像を保持する `Bitmap` と、その上に描画できる `Graphics` オブジェクトを作成します。アンチエイリアス ヒントによりテキストが滑らかに表示されます。

## 手順 2: ブラシ、ペン、フォントの設定

`Brush` は塗りつぶし色、`Pen` は形状の輪郭、`Font` はテキスト描画用のフォント、サイズ、スタイルを指定します。

`Brush` は形状を色で塗りつぶし、`Pen` は形状の輪郭を描き、`Font` はテキスト描画のフォントとサイズを定義します。  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** はテキストの色を定義します。  
- **Pen** は後でテキストの周囲に矩形を描く際に使用します（任意）。  
- **Font** は *画像上に文字列を描画* する操作のためにフォント、サイズ、スタイルを指定します。

## 手順 3: テキストと矩形の定義

`Rectangle` はテキストを配置するバウンディング ボックスを定義し、X/Y 座標と幅/高さを指定します。

`Rectangle` は矩形領域の位置とサイズを指定し、ここでは描画するテキストの範囲を決めるために使用します。  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` がテキストの配置位置を決定します。レイアウトに合わせて座標とサイズを調整してください。

## 手順 4: 矩形とテキストの描画

`Graphics.DrawString` は指定されたフォントとブラシを使用して、指定された矩形内にテキストを描画します。

`Graphics.DrawString` は指定された矩形内に文字列を描画し、与えられたフォントとブラシを使用します。  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

まず青い矩形で領域をアウトラインし、次に `DrawString` を呼び出して **ビットマップにテキストを追加** します。これが画像上で *テキストを描画* する核心です。

## 手順 5: 結果の保存

画像は PNG ファイルとして保存され、*ビットマップを PNG として保存* する要件を満たします。プレースホルダー パスは実際に保存したいフォルダーに置き換えてください。

`bitmap.Save` は選択した形式（例: PNG）で画像をファイルに書き込みます。  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## 一般的な使用例

- **個人名入り証明書** の生成  
- **ウェブ ギャラリー用の透かし付きサムネイル** の作成  
- **ラベルや注釈を含む動的チャート** の構築  

## トラブルシューティングとヒント

- **フォントが見つからない場合** は、ホスト マシンにフォントがインストールされているか、プライベート フォント コレクションを使用してください。  
- **テキストが切り取られる場合** は、矩形サイズを大きくするかフォントサイズを小さくしてください。  
- **パフォーマンスが気になる場合** は、可能な限り同じ `Graphics` オブジェクトを再利用して複数の描画操作を行ってください。  

## よくある質問

**Q: 出力形式を JPEG に変更するには？**  
A: `Save` メソッドの拡張子を `.png` から `.jpg` に変更し、必要に応じて JPEG の品質を指定する `ImageCodecInfo` を指定してください。

**Q: 複数行のテキストを描画できますか？**  
A: はい、文字列に改行文字（`\n`）を含めるか、`StringFormat` と `FormatFlags.LineLimit` を使用してください。

**Q: 描画前にテキストサイズを測定する方法は？**  
A: `Graphics.MeasureString` を使用して、レンダリングされたテキストの正確な寸法を取得できます。

**Q: Aspose.Drawing は Unicode 文字をサポートしていますか？**  
A: もちろんです。必要なグリフを含むフォントを指定すれば、ライブラリは正しく描画します。

**Q: テストに使用した Aspose.Drawing のバージョンは？**  
A: Aspose.Drawing 24.11 for .NET でテストしました。

---

**最終更新日:** 2026-09-23  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts in Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [How to save a bitmap as PNG using the Aspose.Drawing API for .NET](/drawing/net/image-editing/display/)
- [Text On Image](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}