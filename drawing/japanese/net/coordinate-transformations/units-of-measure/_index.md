---
date: 2026-05-24
description: Aspose.Drawing for .NET で unit を設定する方法を学び、graphics units を簡単に変換し、graphics
  rendering のための正確な測定をマスターしましょう。
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Aspose.Drawing の Units of Measure
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET で単位を設定する方法 – 計測単位
url: /ja/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET の単位設定方法 – 測定単位

## はじめに

Aspose.Drawing for .NET の世界へようこそ。ここでは、精度と柔軟性がグラフィック操作で融合します。このチュートリアルでは、描画の **単位の設定方法** を学び、ポイント、ミリメートル、インチ間の **グラフィック単位の変換** を習得し、画像をピクセル単位で完璧にする実例をご紹介します。レポート、サムネイル、カスタムチャートの作成に関わらず、測定単位をマスターすることは、デバイス間で一貫したレンダリングを実現するために不可欠です。

## クイック回答
- **単位を変更する主な方法は何ですか？** `Graphics` オブジェクトで `graphics.PageUnit = PageUnit.Point`（または `.Millimeter`、`.Inch`）を呼び出します。  
- **1/72 インチに相当する単位はどれですか？** ポイント。  
- **1 インチは何ミリメートルですか？** 25.4 mm = 1 inch。  
- **単位を使用するために追加のライブラリが必要ですか？** いいえ、Aspose.Drawing のコアライブラリがすべての単位定数を提供します。  
- **1 つの画像で単位を混在させることはできますか？** `Graphics` インスタンスごとに単位を一度設定し、その単位で全て描画して一貫性を保ちます。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください：

- Aspose.Drawing for .NET: ライブラリがインストールされていることを確認してください。[こちら](https://releases.aspose.com/drawing/net/)からダウンロードできます。
- Document Directory: 作成したドキュメントを保存したい指定ディレクトリを用意してください。
- Basic C# Knowledge: 本ガイドを最大限に活用するために、C# の基本的な知識があることが推奨されます。

## 名前空間のインポート

開始する前に、Aspose.Drawing を効果的に使用するために必要な名前空間をインポートしましょう：

```csharp
using System.Drawing;
```

それでは、各例を複数のステップに分解してみましょう：

## 単位をポイントに設定する方法

`Bitmap` クラスは、描画キャンバスとして機能するメモリ内画像を表します。ビットマップをロードし、`Graphics` オブジェクトを作成してページ単位をポイントに設定します — これにより Aspose.Drawing はすべての座標を 1/72 インチ の値として解釈します。ポイントを使用すると、印刷用グラフィックに対して細かな制御が可能になり、線幅を高精度で指定できます。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 手順 1: ビットマップの作成  
`Bitmap` クラスは、描画キャンバスとして機能するメモリ内画像を表します。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 手順 2: Graphics オブジェクトの作成  
`Graphics` は、`Bitmap` 上に形状やテキストを描画するためのメソッドを提供します。

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### 手順 3: ページ単位をポイントに設定  
`PageUnit` はページ座標の測定単位を指定する列挙型です。`PageUnit.Point` はポイントを測定単位として定義します（1 ポイント = 1/72 インチ）。この設定は以降のすべての描画呼び出しに適用されます。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### 手順 4: ポイント単位で矩形を描画  
単位を設定した後に矩形を描画すると、指定した寸法はポイントとして解釈され、正確なサイズが保証されます。

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## 単位をミリメートルに設定する方法

`PageUnit` はページ座標の測定単位を指定する列挙型です。ミリメートルに切り替えると、エンジニアリング図面の作成など、メートル法の寸法が必要な場合に便利です。Aspose.Drawing は 1 mm を 1/25.4 インチ として扱い、製造や技術文書で使用される実際の測定値とグラフィックを合わせることができます。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### 手順 1: ページ単位をミリメートルに設定  
`Graphics` オブジェクトに `PageUnit.Millimeter` を割り当てます。これにより、すべての座標がメートル法にマッピングされます。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 手順 2: ミリメートル単位で矩形を描画  
矩形の幅と高さはミリメートルで表されるため、実際の測定値と合わせやすく、印刷結果が実寸と一致することが保証されます。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 単位をインチに設定する方法

`Graphics` は、`Bitmap` 上に形状やテキストを描画するメソッドを提供します。インチは多くの米国ベースのデザインツールのデフォルト単位です。単位をインチに設定すると、UI 要素のレイアウト時に馴染みのある単位で考えることができ、画面デザインから印刷への移行が容易になります（インチは一般的に使用されます）。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### 手順 1: ページ単位をインチに設定  
`PageUnit.Inch` は座標系を変更し、1 単位が 1 インチになるようにします。これにより、印刷向けレイアウトの要素サイズをシンプルに指定できます。

CODE_BLOCK_PLACEHOLDER_10_END

### 手順 2: インチ単位で矩形を描画  
これで描画するすべての形状がインチを測定基準として使用するため、印刷レイアウトや、帝国単位に慣れたステークホルダーへの寸法伝達に最適です。

CODE_BLOCK_PLACEHOLDER_11_END

## 結果の保存

例をすべて実行したら、生成された画像をドキュメントディレクトリに保存します。`Bitmap.Save` メソッドは、指定した形式（PNG、JPEG など）でファイルを書き出します。

CODE_BLOCK_PLACEHOLDER_12_END

これで、Aspose.Drawing for .NET のさまざまな測定単位をうまく扱い、ポイント、ミリメートル、インチを使用した矩形のビジュアル表現を作成できました。

## なぜ Aspose.Drawing の単位システムを使用するのか

Aspose.Drawing は **30 以上の画像フォーマット** をサポートし、**5000 × 5000 ピクセル** までの画像をファイル全体をメモリに読み込むことなく処理でき、大規模なグラフィック生成でも高性能を実現します。単位を明示的に設定することで、推測を排除し、変換エラーを減らし、すべてのプラットフォームで出力が正確な物理寸法と一致することを保証します。

## よくある問題と解決策

- **保存後のサイズが予期せぬものになる** – 描画呼び出しの **前に** `graphics.PageUnit` を設定したことを確認してください。後から単位を変更しても、既存の形状のサイズは遡って変更されません。  
- **高 DPI 画面でのぼやけた出力** – ビットマップの解像度を上げます（例: `new Bitmap(width, height, 300)`）ことで、ターゲット DPI に合わせます。  
- **1 つの画像で単位が混在する** – 単位ごとに別々の `Graphics` インスタンスを作成するか、描画前に手動で変換を行ってください。

## よくある質問

### Q1: Aspose.Drawing for .NET を他の .NET フレームワークと併用できますか？

A1: はい、Aspose.Drawing はさまざまな .NET フレームワークと互換性があり、開発環境に柔軟性を提供します。

### Q2: 無料トライアルは利用できますか？

A2: はい、[こちら](https://releases.aspose.com/) から無料トライアルで Aspose.Drawing をお試しできます。

### Q3: Aspose.Drawing for .NET のサポートはどのように受けられますか？

A3: コミュニティサポートやディスカッションは、[Aspose.Drawing フォーラム](https://forum.aspose.com/c/drawing/44)をご覧ください。

### Q4: 短期プロジェクト向けに一時ライセンスを購入できますか？

A4: はい、[こちら](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得できます。

### Q5: Aspose.Drawing の詳細なドキュメントはどこで見つけられますか？

A5: 包括的なドキュメントは[こちら](https://reference.aspose.com/drawing/net/)で利用できます。

---

**最終更新日:** 2026-05-24  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
