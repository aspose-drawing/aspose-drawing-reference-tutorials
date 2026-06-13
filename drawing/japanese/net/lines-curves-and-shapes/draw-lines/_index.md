---
date: 2026-06-13
description: Aspose.Drawing を使用して .NET アプリケーションでビットマップを PNG として保存し、複数の線を描画する方法を学びます。このステップバイステップガイドでは、.NET
  の線描画、ビットマップ上での線の描画手法、およびベストプラクティスを取り上げています。
keywords:
- save bitmap as png
- draw multiple lines
- how to draw lines
linktitle: Aspose.Drawing で複数の線を描画
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  headline: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  name: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  steps:
  - name: Create a Bitmap (draw line bitmap)
    text: The `Bitmap` class represents an in‑memory raster image that you can draw
      onto. Start by creating a new bitmap with the desired width and height. This
      will be the canvas on which you draw your lines.
  - name: Get Graphics Object
    text: The `Graphics` object provides drawing methods such as lines, shapes, and
      text for a bitmap. Obtain a `Graphics` object from the created bitmap. This
      object provides methods for drawing on the bitmap.
  - name: Define a Pen
    text: A `Pen` defines the color, width, and style of lines drawn by the `Graphics`
      object. Create a `Pen` object that defines the attributes of the line you want
      to draw. In this case, we've chosen a blue color with a thickness of 2 pixels.
  - name: Draw Lines
    text: Use the `DrawLine` method to draw lines on the bitmap. The coordinates `(x1,
      y1)` to `(x2, y2)` represent the starting and ending points of each line. By
      calling the method twice, we effectively **draw multiple lines** that form a
      simple “V” shape.
  - name: Save the Image
    text: The `Bitmap.Save` method writes the in‑memory image to a file in the format
      you specify—PNG being the most common loss‑less option. Specify the directory
      where you want to save the output image. Make sure to replace `"Your Document
      Directory"` with the actual path.
  type: HowTo
- questions:
  - answer: Yes, simply modify the `Color` parameter when creating the `Pen` object.
    question: Can I change the color of the lines?
  - answer: Aspose.Drawing supports rectangles, ellipses, curves, polygons, and more.
      Check the official documentation for a complete list.
    question: What other shapes can I draw with Aspose.Drawing?
  - answer: Absolutely. It works in ASP.NET Core, MVC, and other web frameworks, allowing
      server‑side image generation without additional dependencies.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Wrap your drawing code in a `try‑catch` block and consult the Aspose.Drawing
      forum (https://forum.aspose.com/c/drawing/44) for community support.
    question: How should I handle errors while using Aspose.Drawing?
  - answer: Yes, you can use Aspose.Drawing for commercial projects. Visit the [purchase
      page](https://purchase.aspose.com/buy) for licensing details.
    question: Can I use Aspose.Drawing for a commercial project?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing を使用して複数の線を描画しながらビットマップを PNG として保存する方法
url: /ja/net/lines-curves-and-shapes/draw-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing を使用して複数の線を描画しながらビットマップを PNG として保存する

## はじめに

このチュートリアルでは、**ビットマップを PNG として保存する方法** と Aspose.Drawing for .NET を使用した複数の線の描画方法を学びます。シンプルなチャートやカスタム UI コントロールの作成、サーバー上でのグラフィック生成など、鮮明でアンチエイリアス処理された線を描画し、PNG ファイルとして保存できる能力は重要なスキルです。キャンバスの準備から最終画像のエクスポートまで、全工程を順に解説するので、すぐにビジュアルコンポーネントの構築を始められます。

## クイック回答
- **What can I draw?** 任意の直線、ポリライン、またはビットマップ上の形状を描画できます。  
- **Which library?** Aspose.Drawing for .NET (no System.Drawing.Common required)。  
- **How many lines?** 必要なだけ描画できます – 同じ `Graphics.DrawLine` 呼び出しを繰り返すだけです。  
- **Prerequisites?** .NET 開発環境と Aspose.Drawing ライブラリ。  
- **Output format?** PNG、JPEG、BMP、または Aspose.Drawing がサポートする任意の形式。

## 複数の線を描画するとは何ですか？

複数の線を描画するとは、同じ画像キャンバス上に2本以上の直線セグメントを描くことを指します。Aspose.Drawing では、単一の `Graphics` オブジェクトを再利用し、各座標ペアに対して `DrawLine` を呼び出すことで、ラスタおよびベクタ出力の両方に対して高速かつメモリ効率の良い描画を実現します。

## .NET の線描画に Aspose.Drawing を使用する理由

Aspose.Drawing は、**30 以上の出力フォーマット** をサポートし、**10,000 × 10,000 ピクセル** までの画像をメモリに全体を読み込まずに処理できる、モダンでクロスプラットフォームな API を提供します。組み込みのアンチエイリアス、ピクセル単位の精密な制御、そして .NET Core/5+ との完全な互換性を備えており、`System.Drawing.Common` のレガシー依存性を排除します。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

- Aspose.Drawing ライブラリ: [here](https://releases.aspose.com/drawing/net/) から Aspose.Drawing ライブラリをダウンロードしてインストールします。
- 開発環境: マシンに .NET 開発環境が設定されていることを確認してください。
- ドキュメントディレクトリ: 出力画像を保存したい場所にディレクトリを作成します。

## 名前空間のインポート

.NET アプリケーションでは、Aspose.Drawing を使用するために必要な名前空間をインポートする必要があります。コードの先頭に以下の名前空間を追加してください。

```csharp
using System.Drawing;
```

それでは、例を複数のステップに分解し、Aspose.Drawing を使用した線の描画プロセスを案内します。

## Aspose.Drawing で複数の線を描画する方法

ビットマップをロードし、`Graphics` オブジェクトを取得し、`Pen` を設定し、各セグメントに対して `DrawLine` を呼び出し、最後にキャンバスを PNG として保存します。これらはすべて、繰り返しや拡張が可能な5つの簡潔なステップで実行できます。各ステップは、必要な API 呼び出しとアンチエイリアスなどのオプション設定を示すコードスニペットで説明しています。

### 手順 1: ビットマップの作成 (線描画ビットマップ)

`Bitmap` クラスは、描画可能なメモリ内ラスタ画像を表します。  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, PixelFormat.Format32bppPArgb);
```

まず、目的の幅と高さで新しいビットマップを作成します。これが線を描画するキャンバスになります。

### 手順 2: Graphics オブジェクトの取得

`Graphics` オブジェクトは、ビットマップに対して線、形状、テキストなどの描画メソッドを提供します。  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

作成したビットマップから `Graphics` オブジェクトを取得します。このオブジェクトはビットマップ上で描画するためのメソッドを提供します。

### 手順 3: ペンの定義

`Pen` は、`Graphics` オブジェクトが描画する線の色、幅、スタイルを定義します。  
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

描画したい線の属性を定義する `Pen` オブジェクトを作成します。この例では、青色で太さ 2 ピクセルのペンを選択しています。

### 手順 4: 線の描画

`DrawLine` メソッドを使用してビットマップ上に線を描画します。座標 `(x1, y1)` から `(x2, y2)` は各線の開始点と終了点を表します。メソッドを2回呼び出すことで、シンプルな “V” 形状を構成する **複数の線** を実質的に描画します。  
```csharp
graphics.DrawLine(pen, 10, 700, 500, 10);
graphics.DrawLine(pen, 500, 10, 990, 700);
```

### 手順 5: 画像の保存

`Bitmap.Save` メソッドは、メモリ内の画像を指定した形式でファイルに書き込みます。PNG は最も一般的なロスレスオプションです。  
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawLines_out.png");
```

出力画像を保存したいディレクトリを指定します。`"Your Document Directory"` を実際のパスに置き換えてください。

## ビットマップを PNG として保存する方法

ビットマップを PNG として保存するのは1行の操作です。すでに描画した `Bitmap` インスタンスで `bitmap.Save("output.png", ImageFormat.Png)` を呼び出します。`ImageFormat` クラスは PNG、JPEG、BMP などの保存形式を指定します。Aspose.Drawing は圧縮を自動的に処理し、透過性を保持するため、PNG はウェブや UI アセットに最適です。

## よくある問題と解決策

| 問題 | 発生原因 | 対策 |
|------|----------|------|
| **画像が空白になる** | Graphics オブジェクトがビットマップにリンクされていない、またはピクセル形式が間違っている。 | `Graphics.FromImage(bitmap)` を使用し、ビットマップがサポートされたピクセル形式で作成されていることを確認してください。 |
| **線がギザギザになる** | アンチエイリアスが無効になっている。 | 描画前に `graphics.SmoothingMode = SmoothingMode.AntiAlias;` を設定します（`using System.Drawing.Drawing2D;` が必要）。 |
| **保存時にパスが見つからない** | ディレクトリ文字列が無効です。 | `Path.Combine` を使用してパスを構築し、フォルダーが存在することを確認してください。 |

`SmoothingMode` 列挙体は線の描画品質を制御し、`AntiAlias` はより滑らかなエッジを提供します。

## よくある質問

**Q: 線の色を変更できますか？**  
A: はい、`Pen` オブジェクト作成時に `Color` パラメータを変更すれば簡単に変更できます。

**Q: Aspose.Drawing で他にどんな形状を描画できますか？**  
A: Aspose.Drawing は矩形、楕円、曲線、多角形などをサポートしています。完全な一覧は公式ドキュメントをご確認ください。

**Q: Aspose.Drawing はウェブアプリケーションに適していますか？**  
A: はい。ASP.NET Core、MVC、その他のウェブフレームワークで動作し、追加の依存関係なしでサーバーサイドの画像生成が可能です。

**Q: Aspose.Drawing 使用時のエラーはどのように処理すべきですか？**  
A: 描画コードを `try‑catch` ブロックで囲み、コミュニティサポートは Aspose.Drawing フォーラム (https://forum.aspose.com/c/drawing/44) を参照してください。

**Q: 商用プロジェクトで Aspose.Drawing を使用できますか？**  
A: はい、商用プロジェクトで Aspose.Drawing を使用できます。ライセンスの詳細は [purchase page](https://purchase.aspose.com/buy) をご覧ください。

## 結論

このガイドでは、Aspose.Drawing for .NET を使用して **ビットマップを PNG として保存しながら複数の線を描画** するために必要なすべてをカバーしました：ビットマップの作成、Graphics コンテキストの取得、ペンの設定、線の描画、結果の保存です。この基礎をもとに、動的チャートやカスタム UI 要素、サーバーサイドのグラフィック生成など、高品質でスケーラブルな線描画が求められるあらゆるシナリオへ拡張できます。

---

**最終更新日:** 2026-06-13  
**テスト環境:** Aspose.Drawing 24.12 for .NET  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [ビットマップを PNG として保存し、閉曲線を描画する (Aspose.Drawing)](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [ビットマップを保存 C# – Bezier スプラインを描画する (Aspose.Drawing)](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [ビットマップを PNG として保存し、ソリッドブラシを使用する (Aspose.Drawing)](/drawing/net/lines-curves-and-shapes/solid-brushes/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}