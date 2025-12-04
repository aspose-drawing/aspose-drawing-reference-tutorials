---
title: Aspose.Drawing で領域を塗りつぶす
linktitle: Aspose.Drawing で領域を塗りつぶす
second_title: Aspose.Drawing .NET API - System.Drawing.Common の代替
description: このステップバイステップのチュートリアルで、Aspose.Drawing for .NET で領域を塗りつぶす方法を学びましょう。グラフィック デザインのスキルを簡単に向上させます。
weight: 20
url: /ja/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing で領域を塗りつぶす

## 導入

視覚的に魅力的なグラフィックを作成するには、多くの場合、領域を色、パターン、またはグラデーションで塗りつぶす必要があります。 Aspose.Drawing for .NET は、これを効率的に実現するための強力なツールを提供します。このチュートリアルでは、.NET アプリケーションでのグラフィック操作を簡素化する多用途ライブラリである Aspose.Drawing を使用して領域を塗りつぶすプロセスについて詳しく説明します。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

1.  Aspose.Drawing ライブラリ: Aspose.Drawing ライブラリをダウンロードしてインストールします。ライブラリとそのドキュメントを見つけることができます[ここ](https://reference.aspose.com/drawing/net/).

2. 開発環境: Visual Studio などの .NET 開発環境をセットアップして、Aspose.Drawing をプロジェクトに統合します。

## 名前空間のインポート

まず、必要な名前空間をプロジェクトにインポートします。これらの名前空間は、Aspose.Drawing を操作するために必要なクラスとメソッドへのアクセスを提供します。

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


ここで、明確かつ包括的に理解できるように、サンプル コードを複数のステップに分割してみましょう。

## ステップ 1: ビットマップとグラフィックス オブジェクトを作成する

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

このステップでは、新しいビットマップとその上に描画するグラフィックス オブジェクトを初期化します。

## ステップ 2: GraphicsPath を定義し、リージョンを作成する

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

一連の点を含む多角形を指定して、グラフィックス パスを定義します。このパスを使用してリージョンを作成します。

## ステップ 3: 内部領域を除外する

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

内側の長方形を表す別のグラフィックス パスを作成し、それをメイン領域から除外します。

## ステップ 4: ブラシを選択して領域を塗りつぶす

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

ブラシ (この場合は青一色) を選択し、選択したブラシで以前に定義した領域を塗りつぶします。

## ステップ 5: 結果の画像を保存する

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

最終的なイメージを目的のディレクトリに保存します。

## 結論

Aspose.Drawing for .NET での領域の塗りつぶしは簡単なプロセスであり、複雑で視覚的に魅力的なグラフィックスを柔軟に作成できます。創造性を発揮するために、さまざまな形、色、パターンを試してください。

## よくある質問

### Q1: Aspose.Drawing を商用プロジェクトに使用できますか?

 A1: はい、Aspose.Drawing は個人プロジェクトと商用プロジェクトの両方に使用できます。ライセンスの詳細については、次のサイトを参照してください。[ここ](https://purchase.aspose.com/buy).

### Q2: 無料トライアルはありますか?

 A2: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q3: Aspose.Drawing のサポートを受けるにはどうすればよいですか?

 A3: にアクセスしてください。[Aspose.Drawing フォーラム](https://forum.aspose.com/c/drawing/44)コミュニティや専門家からの支援が得られます。

### Q4: Aspose.Drawing を使用して動的イメージを生成できますか?

A4: もちろんです。 Aspose.Drawing を使用すると、.NET アプリケーションでイメージを動的に作成および操作できます。

### Q5: 一時ライセンスは利用できますか?

 A5: はい、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
