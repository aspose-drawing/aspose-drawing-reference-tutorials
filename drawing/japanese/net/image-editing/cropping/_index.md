---
date: 2026-10-13
description: Aspose.Drawing API（System.Drawing のクロスプラットフォーム代替）を使用して、画像を PNG にバッチクロップする方法を
  .NET 開発者向けに学びます。
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: 画像クロップチュートリアル – Aspose.Drawing
og_description: Aspose.Drawing（System.Drawing のクロスプラットフォーム代替）を使用して、画像を PNG に迅速にバッチクロップする方法を学びます。.NET
  開発者向けに、複数のファイルを効率的に処理するためのステップバイステップの手順をご案内します。
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: .NET 用 Aspose.Drawing で画像を PNG にバッチクロップする方法
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: .NET 用 Aspose.Drawing を使用して画像を PNG にバッチクロップする方法
url: /ja/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET を使用した画像のバッチクロップ（PNG へ）

.NET 環境で画像を **crop image to PNG** 素早く、確実に、かつ大量にクロップする必要があるなら、ここが適切な場所です。このチュートリアルでは、画像の読み込み、クロップ領域の定義、結果を PNG ファイルとして保存する手順を詳しく解説します—すべて Aspose.Drawing を使用します。Aspose.Drawing は **System.Drawing の代替** としてモダンでクロスプラットフォームです。また、単一画像のフローをフル **batch crop** パイプラインに拡張する方法も紹介します。

## クイック回答
- **どのライブラリを使用すべきですか？** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **基本的なクロップにどれくらい時間がかかりますか？** Usually under a second for a single image on a modern CPU  
- **PNG にクロップできますか？** Yes – save the cropped bitmap as a PNG file (see Step 6)  
- **ライセンスは必要ですか？** A free trial works for development; a commercial license is required for production  
- **バッチ処理は可能ですか？** Absolutely – wrap the same steps in a loop to process multiple files in seconds  

各ソースファイルを `new Bitmap(path)` で読み込み、クロップ領域用の空の `Bitmap` を作成し、`Graphics.DrawImage` で選択した矩形を描画し、最後に `Save("output.png", ImageFormat.Png)` を呼び出します。これら 6 行をディレクトリを走査する `foreach` ループで包むだけで、数秒で数十枚の画像を処理できる完全なバッチクロップソリューションが完成します。

## バッチクロップに Aspose.Drawing を使用する理由

Aspose.Drawing は **Windows, Linux, and macOS** 上で動作し、典型的なサーバークラス CPU で **500‑plus‑pixel images in under 0.5 seconds** を処理し、**50+ image formats** をフルアルファチャンネル保持でサポートします。ネイティブ GDI+ 依存性がないため、同じコードをコンテナ、Azure App Service、または AWS Lambda に追加ライブラリなしでデプロイでき、大規模な画像パイプラインに最適です。

## “crop image to PNG” とは何か

`crop image to PNG` 操作は、ソースビットマップから矩形領域を抽出し、その領域を PNG ファイルに書き出します。PNG はアルファチャンネルを保持し、ロスレス圧縮を提供するため、サムネイル、アイコン、UI アセット、または品質と透過性が求められるあらゆるシーンに最適です。

## Aspose.Drawing が System.Drawing の代替となる理由

Aspose.Drawing は System.Drawing のドロップイン置換として、完全なクロスプラットフォーム互換性を提供し、ネイティブ GDI+ ライブラリの必要性を排除します。幅広いピクセルフォーマットをサポートし、高性能な画像操作を実現し、アルファチャンネル処理や豊富なフォーマットサポートといった高度な機能も備えているため、シンプルな編集から大規模バッチ処理まで幅広く利用できます。

## 前提条件

開始する前に以下を確認してください：

- **Aspose.Drawing library** を .NET プロジェクトに統合します。ダウンロードは [Aspose.Drawing download page](https://releases.aspose.com/drawing/net/) から取得できます。  
- クロップしたいソース画像が格納されたフォルダーを用意します。コードスニペット中の `"Your Document Directory"` を実際のパスに置き換えてください。

## 名前空間のインポート

`System.Drawing` 名前空間は `Bitmap`、`Graphics`、および Aspose.Drawing が拡張する関連型へのアクセスを提供します。

```csharp
using System.Drawing;
```

## 手順ガイド

### 手順 1: ビットマップキャンバスの作成

`Bitmap` は Aspose.Drawing のメモリ内画像表現で、ピクセルレベルのアクセスとフォーマット制御を提供します。  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

まず、クロップ結果を保持できる空のキャンバスを作成します。幅と高さは抽出予定の領域の寸法に合わせて調整してください。

### 手順 2: Graphics オブジェクトの作成

`Graphics` は Bitmap 上に形状、テキスト、または他の画像を描画できる描画サーフェスです。  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` オブジェクトでキャンバスに描画します。`InterpolationMode` はスケーリングや変換時のピクセル値計算方法を制御し、`NearestNeighbor` はシャープなエッジに適しています。

### 手順 3: クロップする画像の読み込み

`Image`（または `Bitmap`）はソースファイルをメモリに読み込み、操作の準備をします。  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

ソース画像を読み込みます。パスが既存のファイルを指していることを確認してください。存在しない場合は例外がスローされます。

### 手順 4: ソースおよびデスティネーション矩形の定義

`Rectangle` オブジェクトは、ソース画像から保持する領域と、デスティネーションキャンバス上での配置位置を記述します。  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` は API に対し、元画像のどの部分を保持するか指示します。ここでは左上の 50 × 40 ピクセル領域を選択しています。同じ矩形を `destinationRectangle` に割り当てることで、クロップ領域を元のサイズのまま保持します。

### 手順 5: クロップ操作の実行

`Graphics.DrawImage` は `image` の定義された部分を空の `bitmap` にコピーします。  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

これはコアの **crop image to PNG** 操作です。メソッドはソース矩形を尊重し、選択されたピクセルだけをデスティネーションビットマップに書き込みます。

### 手順 6: クロップした画像の保存（crop image to PNG）

`Bitmap.Save` はメモリ内ビットマップを指定されたフォーマットでファイルに書き出します。  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

最後に、キャンバスを PNG ファイルとしてディスクに書き出します。PNG はアルファチャンネルを保持し、ロスレス品質を提供するため UI アセットに最適です。

## ループで画像をバッチクロップする方法は？

`foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` で各ファイルパスを走査し、ループ内で手順 1‑6 を繰り返し、結果をターゲットフォルダーに保存します。このパターンは線形にスケールし、`Parallel.ForEach` で並列化すればさらに高速なスループットが得られ、画像を効率的かつ迅速に処理できます。

## よくある落とし穴とヒント

- **Pixel format mismatches** – ソース画像とキャンバスビットマップが互換性のあるピクセルフォーマットを共有していることを確認し、色ずれを防止してください。  
- **Disposal of GDI objects** – `Bitmap` と `Graphics` を `using` 文で包むか、手動で `Dispose()` を呼び出してください。そうしないとアンマネージドリソースがリークします。  
- **Coordinate errors** – 矩形座標はゼロベースです。ソース画像の範囲を超える矩形を選択すると例外が発生します。  

## よくある質問

**Q: Aspose.Drawing を使用して任意のフォーマットの画像をクロップできますか？**  
A: はい、Aspose.Drawing は PNG、JPEG、BMP、GIF、TIFF など幅広いフォーマットをサポートしているため、事実上すべての画像タイプをクロップできます。

**Q: 高度なクロップオプションはありますか？**  
A: もちろんです。`GraphicsPath`、`Matrix` 変換、または `ImageProcessor` クラスを組み合わせて、円形クロップなどの複雑な選択も実現できます。

**Q: 単一画像に複数のクロップ操作を適用できますか？**  
A: はい。最初のクロップ後、結果のビットマップを新しいソースとして再利用し、プロセスを繰り返すことで複数のクロップを連鎖させられます。

**Q: Aspose.Drawing はバッチ画像処理に適していますか？**  
A: その通りです。軽量な API とネイティブ依存性の欠如により、サーバー上で大量の画像コレクションを処理するのに最適です。

**Q: Aspose.Drawing 関連の質問へのサポートはどこで受けられますか？**  
A: [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) にアクセスして支援を求め、コミュニティとつながってください。

**最終更新日:** 2026-10-13  
**テスト済み:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.Drawing を使用した BMP のロード、PNG への変換およびその他のフォーマット](/drawing/net/image-editing/load-save/)
- [Aspose.Drawing for .NET のライセンス取得方法 – aspose.drawing のライセンス手順](/drawing/net/licensing/)
- [Aspose.Drawing API for .NET を使用した矩形描画 – 座標系変換（ページ変換）](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}