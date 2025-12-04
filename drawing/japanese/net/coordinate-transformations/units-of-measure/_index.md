---
title: Aspose.Drawing for .NET の測定単位
linktitle: Aspose.Drawing の測定単位
second_title: Aspose.Drawing .NET API - System.Drawing.Common の代替
description: この詳細なチュートリアルで Aspose.Drawing for .NET の多用途性を探り、高精度グラフィックスの測定単位をマスターしてください。
weight: 14
url: /ja/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET の測定単位

## 導入

グラフィック操作の精度と柔軟性が融合する Aspose.Drawing for .NET の世界へようこそ。このチュートリアルでは、Aspose.Drawing 内の複雑な測定単位について詳しく説明し、この優れたライブラリの力を活用するためのステップバイステップのガイドを提供します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.Drawing for .NET: ライブラリがインストールされていることを確認してください。ダウンロードできます[ここ](https://releases.aspose.com/drawing/net/).

- ドキュメント ディレクトリ: 作成したドキュメントを保存するディレクトリを指定します。

- C# の基本知識: このガイドを最大限に活用するには、C# の基本を理解することをお勧めします。

## 名前空間のインポート

始める前に、Aspose.Drawing を効果的に使用するために必要な名前空間をインポートしましょう。

```csharp
using System.Drawing;
```

ここで、各例を複数のステップに分けてみましょう。

## 測定単位としてのポイント

1. ビットマップの作成: 指定した幅と高さでビットマップを初期化します。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. グラフィックの作成: ビットマップからグラフィック オブジェクトを生成して、その上に描画します。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. ページ単位をポイントに設定: ポイントを測定単位として定義します (1 ポイント = 1/72 インチ)。

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. 長方形の描画: ポイントを単位として長方形を描画します。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## 測定単位としてのミリメートル

1. ページ単位をミリメートルに設定: 測定単位をミリメートル (1 mm = 1/25.4 インチ) に変更します。

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. ミリメートルで長方形を描画: ミリメートルを単位として別の長方形を描画します。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## 測定単位としてのインチ

1. ページ単位をインチに設定: 測定単位をインチに切り替えます。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. インチで長方形を描画: インチを単位として使用して長方形を描画します。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 結果を保存する

例を完了したら、結果の画像をドキュメント ディレクトリに保存します。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

これで、Aspose.Drawing for .NET でさまざまな測定単位を正しく操作し、ポイント、ミリメートル、インチを使用して長方形の視覚的表現を作成できました。

## 結論

このチュートリアルでは、Aspose.Drawing for .NET がさまざまな測定単位をどのように処理するかを調べました。ポイント、ミリメートル、インチを操作することで、グラフィック作成の精度と適応性を実現できます。これらの概念を試して、Aspose.Drawing の可能性を最大限に引き出してください。

## よくある質問

### Q1: Aspose.Drawing for .NET を他の .NET フレームワークと一緒に使用できますか?

A1: はい、Aspose.Drawing はさまざまな .NET フレームワークと互換性があり、開発環境に柔軟性をもたらします。

### Q2: 無料トライアルはありますか?

 A2: はい、無料トライアルで Aspose.Drawing を探索できます。[ここ](https://releases.aspose.com/).

### Q3: Aspose.Drawing for .NET のサポートを取得するにはどうすればよいですか?

 A3: にアクセスしてください。[Aspose.Drawing フォーラム](https://forum.aspose.com/c/drawing/44)コミュニティのサポートとディスカッションのために。

### Q4: 短期プロジェクトのために一時ライセンスを購入できますか?

 A4: はい、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.Drawing の詳細なドキュメントはどこで見つけられますか?

 A5: 包括的なドキュメントが入手可能です[ここ](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
