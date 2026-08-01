---
date: 2026-08-01
description: C# でビットマップ画像を作成し、Aspose.Drawing を使用してビットマップ上に矩形を描画する方法を学びます。.NET 開発者向けのステップバイステップガイドです。
keywords:
- create bitmap image c#
- draw rectangle on bitmap
- replace system.drawing
lastmod: 2026-08-01
linktitle: Aspose.Drawing で矩形を描画
og_description: C# でビットマップ画像を作成し、Aspose.Drawing を使用してビットマップ上に矩形を描画します。このチュートリアルでは、.NET
  で矩形グラフィックを generate、style、save する方法を示します。
og_image_alt: Guide to drawing rectangles on a bitmap with Aspose.Drawing for .NET
og_title: C# でビットマップ画像を作成 – Aspose.Drawing で矩形を描画
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to create bitmap image C# and draw rectangle on bitmap using
    Aspose.Drawing. Step‑by‑step guide for .NET developers.
  headline: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)`
      before or after drawing the outline.
    question: Can I fill the rectangle with a solid color?
  - answer: Loop through a collection of `Rectangle` structs and call `DrawRectangle`
      for each iteration.
    question: How do I draw multiple rectangles?
  - answer: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform
      after.
    question: Is there a way to rotate the rectangle?
  - answer: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat`
      parameter.
    question: What image formats are supported for saving?
  - answer: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and
      later versions.
    question: Does Aspose.Drawing work on .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- create bitmap image
- Aspose.Drawing
- .NET graphics
- draw rectangle
title: C# でビットマップ画像を作成 – Aspose.Drawing for .NET を使用して矩形を描画
url: /ja/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET で矩形を描画する方法

## はじめに

このチュートリアルでは、Aspose.Drawing を使用して **矩形を描画する方法** と **C# でビットマップ画像を作成する方法** をマスターします。シンプルな UI 要素が必要な場合でも、レポート用の高解像度グラフィックが必要な場合でも、ビットマップの作成、Graphics オブジェクトの設定、矩形の描画、最終画像の保存までを順を追って解説します。この手法は Windows、Linux、macOS で動作し、従来の `System.Drawing.Common` API を完全なクロスプラットフォーム ソリューションに置き換えます。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.Drawing for .NET  
- **どのメソッドが図形を描画しますか？** `Graphics.DrawRectangle`  
- **ライセンスは必要ですか？** トライアルは無料ですが、商用利用には商用ライセンスが必要です。  
- **矩形のサイズを変更できますか？** はい – 幅、高さ、位置のパラメータを調整します。  
- **コードは .NET 6+ と互換性がありますか？** はい、Aspose.Drawing は最新の .NET バージョンをサポートしています。

## Aspose.Drawing の文脈で「矩形を描画する」とは何ですか？

Aspose.Drawing で矩形を描画するには、`Graphics` クラスを使用してビットマップキャンバス上に矩形の輪郭または塗りつぶし形状を描画します。これにより、サイズ、色、線の太さ、画像形式を完全に制御でき、オンザフライのグラフィックに最適です。Aspose.Drawing は純粋にマネージドなエンジン上で動作するため、`System.Drawing.Common` のネイティブ GDI+ の制限を回避できます。

## なぜ矩形作成に Aspose.Drawing を使用するのか？

Aspose.Drawing を使用すると、**ビットマップ上に矩形を描画** でき、プラットフォーム固有の DLL が不要です。また、**30 以上の出力形式**（PNG、JPEG、BMP、GIF、TIFF など）をサポートします。最大 **10,000 × 10,000 ピクセル** の画像を処理でき、メモリ使用量は **100 MB 未満** に抑えられ、レガシーな System.Drawing 実装よりも 2‑3 倍効率的です。

## 前提条件

コードに取り掛かる前に、以下を用意してください。

- **Aspose.Drawing ライブラリ** – 公式サイトの[here](https://releases.aspose.com/drawing/net/)からダウンロードしてください。  
- **開発環境** – Visual Studio 2022 または任意の .NET 対応 IDE。  
- **基本的な .NET 知識** – C# の構文とプロジェクト構成に慣れていること。

## 名前空間のインポート

`using` ディレクティブは必須クラスをスコープに持ち込みます。描画操作には必ず必要です。

```csharp
using System.Drawing;
```

## 手順 1: ビットマップ画像の作成

`Bitmap` はメモリ上のラスタ画像を表し、描画対象となります。作成時にキャンバスサイズとピクセル形式を指定します。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 手順 2: Graphics オブジェクトの作成

`Graphics` はビットマップ表面上で描画コマンドを実行するエンジンです。取得後は図形、テキスト、画像をレンダリングできます。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 手順 3: 矩形用 Pen の定義

`Pen` は矩形の輪郭色と太さを指定します。また、破線スタイルやラインジョインも制御できます。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## 手順 4: ビットマップ上に矩形を描画

`Graphics.DrawRectangle` は先に定義した Pen を使用して矩形を描画します。X、Y 座標に加えて幅と高さを指定し、形状を正確に配置します。

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## 手順 5: 描画した画像の保存

`Bitmap.Save` メソッドは選択した形式（例: PNG、JPEG）で画像を **ディスク** に書き込みます。この手順で **描画画像の保存** 機能を示し、ビットマップを再利用できるようにします。

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

おめでとうございます！Aspose.Drawing for .NET を使用して **矩形を描画する方法** を正常に完了し、**C# でビットマップ画像を作成する方法** も学びました。

## よくある問題と解決策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| 画像が空白になる | Bitmap が破棄されていない、または graphics がフラッシュされていない | 保存前に `graphics.Dispose();` を呼び出すか、`using` ブロックを使用してください。 |
| エッジが低品質 | デフォルトのスムージングモード | `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;` を設定してください。 |
| ファイルパスエラー | 無効なディレクトリ | 対象フォルダーが存在することを確認するか、`Path.Combine` を使用して安全なパスを作成してください。 |

## よくある質問

**Q: 矩形を単色で塗りつぶすことはできますか？**  
A: はい、`SolidBrush` を作成し、輪郭を描画する前後に `graphics.FillRectangle(brush, …)` を呼び出します。

**Q: 複数の矩形を描画するにはどうすればよいですか？**  
A: `Rectangle` 構造体のコレクションをループし、各イテレーションで `DrawRectangle` を呼び出します。

**Q: 矩形を回転させる方法はありますか？**  
A: 描画前に `graphics.RotateTransform(angle)` を使用し、描画後に変換をリセットします。

**Q: 保存に対応している画像フォーマットは何ですか？**  
A: PNG、JPEG、BMP、GIF、TIFF がすべて、適切な `ImageFormat` パラメータでサポートされています。

**Q: Aspose.Drawing は .NET Core で動作しますか？**  
A: はい、このライブラリは .NET Core、.NET 5、.NET 6 以降のバージョンと完全に互換性があります。

**最終更新日:** 2026-08-01  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose  

## 関連チュートリアル

- [Aspose.Drawing for .NET で楕円を描く方法](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [Aspose.Drawing で複数の線を描く](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [Aspose.Drawing でビットマップを作成 – .NET で多角形を描く](/drawing/net/lines-curves-and-shapes/draw-polygon/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}