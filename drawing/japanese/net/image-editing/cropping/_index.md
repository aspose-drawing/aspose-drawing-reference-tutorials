---
date: 2026-02-07
description: Aspose.Drawing を使用して画像を PNG にトリミングするステップバイステップチュートリアル（.NET 開発者向けの System.Drawing
  の代替）。バッチトリミングと必須テクニックを含む。
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: .NET 用 Aspose.Drawing で画像を PNG にトリミングする方法
url: /ja/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET を使用した PNG への画像トリミング方法

.NET 環境で **crop image to PNG** を迅速かつ確実に行いたい場合は、ここが最適です。このチュートリアルでは、画像の読み込み、トリミング領域の定義、結果を PNG ファイルとして保存する手順を、クロスプラットフォームで動作する最新の **alternative to System.Drawing** である Aspose.Drawing を使って詳しく解説します。

## Quick Answers
- **どのライブラリを使用すべきか？** Aspose.Drawing for .NET（System.Drawing.Common のフル機能代替）  
- **基本的なトリミングにかかる時間は？** 現代的な CPU で単一画像の場合、通常 1 秒未満  
- **PNG にトリミングできるか？** はい – トリミングしたビットマップを PNG ファイルとして保存します（Step 6 参照）  
- **ライセンスは必要か？** 開発用には無料トライアルで可、商用利用には製品ライセンスが必要です  
- **バッチ処理は可能か？** もちろん – 同じ手順をループで回すことで複数ファイルを一括処理できます  

## What is “crop image to PNG”?

画像のトリミングとは、元のビットマップから矩形領域を抽出することです。その領域を PNG として保存すれば、透過情報を保持しつつロスレス圧縮が得られるため、サムネイルやアイコン、各種 UI アセットに最適です。

## Why Aspose.Drawing Is an Alternative to System.Drawing?

- **クロスプラットフォーム対応** – Windows、Linux、macOS でネイティブ GDI+ 依存なしに動作します。  
- **豊富なピクセルフォーマット処理** – 32‑bit、24‑bit、インデックスカラーなどに対応。  
- **パフォーマンス重視の API** – 単一画像の編集から大規模バッチジョブまで理想的です。  

## Prerequisites

始める前に以下を用意してください。

- **Aspose.Drawing ライブラリ** を .NET プロジェクトに組み込む。ダウンロードは [here](https://releases.aspose.com/drawing/net/) から。  
- トリミング対象の画像が格納されたフォルダー。コードスニペット中の `"Your Document Directory"` を実際のパスに置き換えて使用します。

## Import Namespaces

```csharp
using System.Drawing;
```

`System.Drawing` 名前空間は、Aspose.Drawing が拡張する `Bitmap`、`Graphics` などの型へのアクセスを提供します。

## Step‑by‑Step Guide

### Step 1: Create a Bitmap Canvas

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

トリミング結果を保持するための空のキャンバスを作成します。幅と高さは抽出したい領域のサイズに合わせて調整してください。

### Step 2: Create a Graphics Object

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` オブジェクトはキャンバス上に描画するために使用します。`InterpolationMode` はスケーリングや変形時のピクセル計算方法を制御し、`NearestNeighbor` はシャープなエッジに適しています。

### Step 3: Load the Image to Crop

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

ソース画像を読み込みます。パスが実在するファイルを指していることを確認しないと例外がスローされます。

### Step 4: Define Source and Destination Rectangles

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` は元画像のどの部分を保持するかを API に指示します。ここでは左上の 50 × 40 ピクセル領域を選択しています。`destinationRectangle` に同じ矩形を割り当てることで、トリミング領域を元サイズのまま描画します。

### Step 5: Perform the Crop Operation

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` が `image` の指定部分を空の `bitmap` にコピーします。これが **crop image to PNG** の核心処理です。

### Step 6: Save the Cropped Image (Crop Image to PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

最後にキャンバスを PNG ファイルとしてディスクに書き出します。PNG はアルファチャンネルを保持し、ロスレス品質を提供するため UI アセットに最適です。

## How to Crop Images in a Batch Scenario

多数の画像を処理する場合は、上記コード全体を `foreach` ループで囲み、ファイルパスのコレクションを順に処理します。同じ `Graphics.DrawImage` ロジックが使えるので、**batch image cropping** はこのチュートリアルの自然な拡張となります。

## Common Pitfalls & Tips

- **Pixel format の不一致** – ソース画像とキャンバスビットマップが互換性のあるピクセルフォーマットであることを確認し、色ずれを防ぎます。  
- **GDI オブジェクトの破棄** – `Bitmap` と `Graphics` は `using` ステートメントで囲むか、手動で `Dispose()` を呼び出してリソースリークを防止してください。  
- **座標エラー** – 矩形座標は 0 ベースです。ソース画像の範囲を超える矩形を指定すると例外が発生します。  

## Frequently Asked Questions

**Q: Aspose.Drawing で任意の形式の画像をトリミングできますか？**  
A: はい、Aspose.Drawing は PNG、JPEG、BMP、GIF、TIFF など多数の形式をサポートしているため、実質すべての画像タイプをトリミング可能です。

**Q: 高度なトリミングオプションはありますか？**  
A: もちろんです。`GraphicsPath`、`Matrix` 変換、または `ImageProcessor` クラスを組み合わせて、円形トリミングなど複雑な選択も実現できます。

**Q: 1 枚の画像に対して複数回トリミングできますか？**  
A: はい。最初のトリミング後に得られたビットマップを新たなソースとして再利用すれば、連続してトリミングを行うことができます。

**Q: Aspose.Drawing はバッチ画像処理に向いていますか？**  
A: その通りです。軽量な API とネイティブ依存がない点が、サーバー上で大量の画像コレクションを処理するのに最適です。

**Q: Aspose.Drawing に関する質問のサポートはどこで受けられますか？**  
A: [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) へアクセスして、コミュニティやサポートチームに問い合わせてください。

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}