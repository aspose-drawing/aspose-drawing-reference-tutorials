---
date: 2026-05-19
description: Aspose.Drawing（.NET 開発者向けの System.Drawing の代替）を使用して、画像をバッチで PNG にクロップする手順をステップバイステップで解説します。
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: 画像クロップチュートリアル – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
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
title: Aspose.Drawing for .NET を使用して画像をバッチで PNG にクロップする方法
url: /ja/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET を使用した PNG へのバッチ画像クロップ方法

.NET 環境で画像を迅速かつ確実に、かつスケールして **crop image to PNG** したい場合、ここが適切な場所です。このチュートリアルでは、画像の読み込み、クロップ領域の定義、結果を PNG ファイルとして保存する手順を正確に解説します—すべて Aspose.Drawing を使用します。これは、クロスプラットフォームで動作する最新の **alternative to System.Drawing** です。また、単一画像のフローをフル **batch crop** パイプラインに拡張する方法も示します。

## クイック回答
- **どのライブラリを使用すべきですか？** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **基本的なクロップにどれくらい時間がかかりますか？** Usually under a second for a single image on a modern CPU  
- **PNG にクロップできますか？** Yes – save the cropped bitmap as a PNG file (see Step 6)  
- **ライセンスは必要ですか？** A free trial works for development; a commercial license is required for production  
- **バッチ処理は可能ですか？** Absolutely – wrap the same steps in a loop to process multiple files  

## PNG へのバッチ画像クロップ方法

各ソースファイルを `new Bitmap(path)` で読み込み、クロップ領域用の空の `Bitmap` を作成し、`Graphics.DrawImage` で選択した矩形を描画し、最後に `Save("output.png", ImageFormat.Png)` を呼び出します。これら 6 行をディレクトリを走査する `foreach` ループで包むことで、数十枚の画像を数秒で処理できる完全なバッチクロップソリューションが得られます。

## バッチクロップに Aspose.Drawing を使用する理由

Aspose.Drawing は **3 つの主要なオペレーティングシステム**（Windows、Linux、macOS）をサポートし、一般的なサーバークラス CPU で **0.5 秒未満で 500 ピクセル以上の画像** を処理できます。その API はネイティブ GDI+ 依存性を回避するため、同じコードをコンテナ、Azure App Service、または AWS Lambda に追加ライブラリなしでデプロイできます。また、ライブラリは **50 以上の画像フォーマット** と **フルアルファチャンネル保持** を提供し、スケールした透明 PNG クロップに最適です。

## “crop image to PNG” とは何ですか？

`crop image to PNG` 操作は、ソースビットマップから矩形領域を抽出し、その領域を PNG ファイルに書き出します。PNG はアルファチャンネルを保持し、ロスレス圧縮を提供するため、サムネイル、アイコン、UI アセット、または品質と透過性が必要なあらゆる状況に最適な画像となります。

## Aspose.Drawing が System.Drawing の代替となる理由

Aspose.Drawing は、完全なクロスプラットフォーム互換性を提供し、ネイティブ GDI+ ライブラリの必要性を排除することで System.Drawing のドロップイン置換として機能します。幅広いピクセルフォーマットをサポートし、高性能な画像操作を実現し、アルファチャンネル処理や豊富なフォーマットサポートなどの高度な機能を含むため、シンプルな編集から大規模なバッチ処理まで適しています。

## 前提条件

本題に入る前に、以下が揃っていることを確認してください：

- **Aspose.Drawing ライブラリ** を .NET プロジェクトに統合する。ダウンロードは [here](https://releases.aspose.com/drawing/net/) から可能です。  
- クロップしたいソース画像が入っているフォルダー。コードスニペット中の `"Your Document Directory"` を実際のパスに置き換えてください。

## 名前空間のインポート

`System.Drawing` 名前空間は、Aspose.Drawing が拡張する `Bitmap`、`Graphics`、および関連型へのアクセスを提供します。

```csharp
using System.Drawing;
```

## ステップバイステップガイド

### 手順 1: Bitmap キャンバスの作成

`Bitmap` は Aspose.Drawing の画像のメモリ内表現で、ピクセルレベルのアクセスとフォーマット制御を提供します。  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

クロップ結果を保持できるサイズの空白キャンバスから開始します。幅と高さは抽出予定の領域の寸法に合わせて調整してください。

### 手順 2: Graphics オブジェクトの作成

`Graphics` は、Bitmap 上に形状、テキスト、または他の画像を描画できる描画サーフェスです。  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` オブジェクトを使用してキャンバスに描画できます。`InterpolationMode` はスケーリングや変換時のピクセル値計算方法を制御し、`NearestNeighbor` はシャープなエッジに適しています。

### 手順 3: クロップする画像の読み込み

`Image`（または `Bitmap`）はソースファイルをメモリに読み込み、操作の準備をします。  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

ソース画像を読み込みます。パスが既存のファイルを指していることを確認してください。そうでない場合は例外がスローされます。

### 手順 4: ソースおよびデスティネーション矩形の定義

`Rectangle` オブジェクトは、ソース画像の保持領域とそれをデスティネーションキャンバス上のどこに配置するかを記述します。  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` は、元画像のどの部分を保持するか API に指示します。ここでは左上の 50 × 40 ピクセル領域を選択しています。同じ矩形を `destinationRectangle` に割り当てることで、クロップ領域を元のサイズのまま保持します。

### 手順 5: クロップ操作の実行

`Graphics.DrawImage` は、`image` の定義された部分を空の `bitmap` にコピーします。  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` は、`image` の定義された部分を空の `bitmap` にコピーします。これはコアな **crop image to PNG** 操作です。

### 手順 6: クロップ画像の保存 (Crop Image to PNG)

`Bitmap.Save` は、メモリ内のビットマップを指定されたフォーマットでファイルに書き出します。  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

最後に、キャンバスを PNG ファイルとしてディスクに書き出します。PNG はアルファチャンネルを保持し、ロスレス品質を提供するため、UI アセットに最適です。

## ループで画像をバッチクロップする方法

`foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` で各ファイルパスを反復し、ループ内で手順 1‑6 を繰り返し、結果をターゲットフォルダーに保存します。このパターンは線形にスケールし、`Parallel.ForEach` で並列化すればさらに高速なスループットが得られ、画像を効率的かつ迅速に処理します。

## よくある落とし穴とヒント

- **Pixel format mismatches** – ソース画像とキャンバスのビットマップが互換性のあるピクセルフォーマットを共有していることを確認し、色ずれを防止してください。  
- **Disposal of GDI objects** – `Bitmap` と `Graphics` を `using` ステートメントでラップするか、手動で `Dispose()` を呼び出してください。そうしないとアンマネージドリソースがリークする可能性があります。  
- **Coordinate errors** – 矩形座標はゼロベースです。ソース画像の境界を超える矩形を選択すると例外が発生します。  

## よくある質問

**Q: Aspose.Drawing を使用して任意の形式の画像をクロップできますか？**  
A: はい、Aspose.Drawing は幅広いフォーマット（PNG、JPEG、BMP、GIF、TIFF など）をサポートしているため、事実上すべての画像タイプをクロップできます。

**Q: 高度なクロップオプションは利用可能ですか？**  
A: もちろんです。`GraphicsPath`、`Matrix` 変換を組み合わせたり、`ImageProcessor` クラスを使用して円形クロップなどの複雑な選択を行うことができます。

**Q: 単一画像に複数のクロップ操作を適用できますか？**  
A: はい。最初のクロップ後、結果のビットマップを新しいソースとして再利用し、プロセスを繰り返すことで複数のクロップを連鎖させることができます。

**Q: Aspose.Drawing はバッチ画像処理に適していますか？**  
A: はい。その軽量な API とネイティブ依存性の欠如により、サーバー上で大量の画像コレクションを処理するのに最適です。

**Q: Aspose.Drawing に関する質問のサポートはどうすれば得られますか？**  
A: [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) にアクセスして支援を求め、コミュニティとつながってください。

---

**最終更新日:** 2026-05-19  
**テスト済みバージョン:** Aspose.Drawing 24.11 for .NET  
**著者:** Aspose

## 関連チュートリアル

- [Aspose.Drawing for .NET を使用した PNG への画像クロップ方法](/drawing/net/image-editing/cropping/)
- [Aspose.Drawing for .NET を使用した画像のスケーリング方法](/drawing/net/image-editing/scale/)
- [Aspose.Drawing を使用した BMP から PNG への変換とその他フォーマット](/drawing/net/image-editing/load-save/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}