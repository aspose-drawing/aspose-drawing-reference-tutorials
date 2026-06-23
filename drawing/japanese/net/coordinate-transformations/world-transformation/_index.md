---
date: 2026-06-23
description: Aspose.Drawing を使用して PNG を保存し、world transformations を適用し、グラフィックを PNG
  に変換する方法を学びます。translate transform C# の例と multiple graphics transformations が含まれています。
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: Aspose.Drawing の World Transformation
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing を使用した PNG の保存方法 – World Transformation
url: /ja/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.DrawingでPNGを保存する方法 – ワールド変換

## ビットマップをPNGとして保存 – はじめに

**PNGの保存方法** を Aspose.Drawing で使用することは、オンザフライで高品質かつ透過画像を生成する必要がある場合に一般的な要件です。このチュートリアルでは、**ビットマップをPNGとして保存**する方法、translate、rotate、scale などのワールド変換を適用する方法、そして最終的にグラフィックスを PNG に変換する方法を、クリーンで保守しやすい C# コードで学びます。レポートエンジン、チャートコンポーネント、またはカスタム UI レンダラーを構築する場合でも、これらの手順を習得すれば、あらゆるデバイスで見栄えの良い動的画像を作成できます。

## クイック回答

- **「ワールド変換」とは何ですか？** 描画の論理（ワールド）座標をページ（デバイス）座標にマッピングします。  
- **結果を PNG としてエクスポートできますか？** はい – 描画後に単に `bitmap.Save(...)` を `.png` 拡張子で呼び出すだけです。  
- **Aspose.Drawing のライセンスは必要ですか？** 開発には無料トライアルで動作しますが、製品版には商用ライセンスが必要です。  
- **.NET 6/7 と互換性がありますか？** もちろんです – Aspose.Drawing は .NET Framework 4.5 以降および .NET Core/5/6/7 をサポートしています。  
- **何個の変換をチェーンできますか？** **複数のグラフィック変換** を順に適用できます（translate、rotate、scale など）。

## Aspose.Drawing のワールド変換とは何ですか？

ワールド変換は、描画コマンドが使用する座標系を変更します。デフォルトでは、(0,0) はビットマップの左上隅です。`TranslateTransform`、`RotateTransform`、または `ScaleTransform` を使用すると、原点を再配置したり、形状を回転させたり、元のジオメトリを変更せずにサイズを変更したりできます。

## Aspose.Drawing を使用して PNG を保存する方法は？

`Bitmap` オブジェクトをロードし、その `Graphics` インスタンスに必要なワールド変換を設定し、形状を描画し、最後に `bitmap.Save("output.png", ImageFormat.Png)` を呼び出します。このワンラインの保存呼び出しは、透過性と色の忠実度を保持したロスレス PNG ファイルを書き出し、Web 資産や UI オーバーレイに最適です。

## なぜ Graphics Translate の例を使用するのですか？

Graphics Translate の例を使用すると、各ポイントを再計算する代わりに描画原点を一度だけ移動できます。このアプローチはコードの複雑さを減らし、可読性を向上させ、グラフィックエンジンに行列計算を効率的に処理させるため、大規模なキャンバスではレンダリング性能が最大 30 % 向上する可能性があります。

## Graphics Translate の例

**Graphics Translate の例** は、原点を移動することで位置決めがシンプルになることを示しています。各ポイントを再計算する代わりに、座標系を一度シフトし、あたかも新しい原点がキャンバスの中心であるかのように描画できます。

## 前提条件

- **Aspose.Drawing ライブラリ** を .NET プロジェクトに統合します – 公式の [Aspose.Drawing リリースページ](https://releases.aspose.com/drawing/net/) からダウンロードしてください。  
- 出力画像が保存される **ドキュメント ディレクトリ**。  
- **C#** の構文と Visual Studio またはお好みの IDE に関する基本的な知識。  

それでは、コードを見ていきましょう！

## 名前空間のインポート

`Bitmap`、`Graphics`、および Aspose の描画ユーティリティはこれらの名前空間にあります。  
**定義:** `System.Drawing` はコア GDI+ 型を提供し、`Aspose.Drawing` はそれらをクロスプラットフォーム機能で拡張します。

## ステップバイステップ ガイド

### 手順 1: ビットマップの作成

まず、描画を保持する空白のキャンバスを作成します。

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` は、事前乗算アルファ付きの 32 ビット/ピクセル ビットマップを作成します。これは透過性を保持し、余分な変換ステップなしで PNG 出力に最適なフォーマットです。

- **なぜ 32bppPArgb なのか？** このピクセルフォーマットはアルファ透過と高品質なカラー描画をサポートし、PNG 出力に最適です。  
- **プロのコツ:** 幅/高さを目的の画像サイズに合わせて調整してください。

### 手順 2: ワールド変換の設定 (Graphics Translate の例)

`TranslateTransform` は座標系の原点を新しい位置に移動します。  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` は (0,0) ポイントをキャンバスの中心にシフトします。この呼び出しの後、座標 (0,0) を使用して描画する任意の形状は画像の中央に表示されます。

- これにより (0,0) ポイントが (500, 400) に移動し、1000 × 800 キャンバスの中央になります。  
- 追加の変換をチェーンできます: `RotateTransform` は座標系を回転させ、`ScaleTransform` はスケーリングします。これにより **複数のグラフィック変換** が可能になります。

### 手順 3: 変換された座標で矩形を描画

`DrawRectangle` は指定されたペンと座標で矩形を描画します。  
`graphics.DrawRectangle(pen, -150, -100, 300, 200)` は、変換された原点から幅と高さの半分だけオフセットされた左上隅になるため、キャンバスの中心に矩形が描かれます。

- 矩形の左上隅は変換された原点（画像の中心）から始まります。  
- 楕円、線、カスタムパスなど、他の形状でも自由に試してみてください。

### 手順 4: 結果の保存 – グラフィックスを PNG に変換

`Save` はビットマップを指定された画像形式のファイルに書き込みます。  
`ImageFormat` は PNG など、画像を保存するファイル形式を指定します。  
`bitmap.Save(outputPath, ImageFormat.Png)` はロスレス PNG ファイルを書き出し、Web ページや UI コンポーネントで直接使用できます。

- PNG は以前設定した正確な色と透過性を保持します。  
- `"Your Document Directory"` を実際のマシン上のパスに置き換えてください。

## よくある問題と解決策

| 問題 | 発生原因 | 対策 |
|-------|----------------|-----|
| **保存時のファイルが見つからないエラー** | 対象フォルダーが存在しません。 | `Save` を呼び出す前に、プログラムでフォルダーを作成します（`Directory.CreateDirectory`）。 |
| **変換後の空白画像** | `TranslateTransform` が描画後に呼び出されています。 | 変換はすべての描画コマンドの **前** に設定してください。 |
| **色が歪む** | 互換性のないピクセルフォーマットを使用しています。 | PNG 出力には `Format32bppPArgb` を使用してください。 |

## よくある質問

**Q: 複数の変換を適用できますか？**  
A: はい – `TranslateTransform`、`RotateTransform`、`ScaleTransform` をチェーンして、単一のグラフィック パイプラインで複雑な効果を実現できます。

**Q: Aspose.Drawing は商用プロジェクトで無料ですか？**  
A: 評価用の無料トライアルは利用可能ですが、製品環境で使用するには商用ライセンスが必要です。

**Q: .NET Core と .NET 5/6/7 でも動作しますか？**  
A: もちろんです。Aspose.Drawing は .NET Core、.NET 5、.NET 6、.NET 7 を含むすべての最新 .NET ランタイムをサポートしています。

**Q: 完全な API リファレンスはどこで見つけられますか？**  
A: 完全なドキュメントは [here](https://reference.aspose.com/drawing/net/) で入手できます。

**Q: 出力ファイルが見つからない場合のトラブルシューティングは？**  
A: `Save` を呼び出す前に、パス文字列を確認し、書き込み権限があることを確認し、ディレクトリが存在するか確認してください。

## 結論

これで、Aspose.Drawing を使用した **PNG の保存方法**、**ワールド変換** の適用、そして回転やスケーリングで拡張できる **Graphics Translate の例** を実行する方法を学びました。これらの基本をマスターすれば、動的画像の生成、カスタムチャートの作成、または任意の .NET アプリケーション向けにオンザフライのグラフィックを構築できます。

---

**最終更新日:** 2026-06-23  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose  
**関連リソース:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## 関連チュートリアル

- [マトリックス変換チュートリアル: Aspose.Drawing の .NET 用マトリックス変換](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Aspose.Drawing グローバル変換で画像を回転する方法](/drawing/net/coordinate-transformations/global-transformation/)
- [座標系変換 – Aspose.Drawing の .NET 用ページ変換](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}