---
date: 2026-02-04
description: .NET 用の Aspose.Drawing でビットマップを作成する方法、ポイントで矩形を描く方法、そして正確なグラフィックのための測定単位をマスターする方法を学びましょう。
linktitle: Units of Measure in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawingでビットマップを作成 – 測定単位
url: /ja/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing でビットマップを作成 – 単位

## はじめに

このチュートリアルでは、**Aspose.Drawing** を使用して .NET 用のビットマップを作成し、さまざまな測定単位が描画に与える影響を確認します。ポイント、ミリメートル、インチを使って矩形を描く手順を通じて、グラフィックが多用されるシナリオに最適な単位を選択できるようになります。最後まで学べば、単位を自由に切り替えてピクセル単位で正確な画像を生成できるようになります。

## クイック回答
- **このガイドの主な目的は何ですか？** Aspose.Drawing でビットマップを作成し、さまざまな測定単位で図形を描く方法を示すことです。  
- **どの単位がデモされていますか？** ポイント、ミリメートル、インチ。  
- **サンプルを実行するのにライセンスは必要ですか？** 評価用の無料トライアルで動作しますが、製品環境では商用ライセンスが必要です。  
- **対応している .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。  
- **Aspose.Drawing はどこからダウンロードできますか？** 以下の公式ダウンロードページから取得してください。

## 「Aspose.Drawing でビットマップを作成する」とは？
Aspose.Drawing でビットマップを作成するとは、`Bitmap` オブジェクトをインスタンス化し、Aspose.Drawing のグラフィックス API を使って描画できるようにすることです。System.Drawing とは異なり、Aspose.Drawing はすべての .NET プラットフォームで一貫して動作します。

## なぜ異なる測定単位を使用するのか？
ポイント、ミリメートル、インチといった単位を適切に選択することで、実際の寸法と合わせたグラフィックを作成でき、印刷物、PDF、UI レイアウトなど、物理的なサイズが重要になるシーンでの統合が容易になります。

## 前提条件

- **Aspose.Drawing for .NET** – [こちらからダウンロード](https://releases.aspose.com/drawing/net/)  
- **ドキュメントディレクトリ** – 生成した画像を保存するローカルフォルダー  
- **基本的な C# の知識** – クラス、オブジェクト、メソッド呼び出しに慣れていること

## 名前空間のインポート

まず、描画オブジェクトを使用できるように必須の名前空間をインポートします。

```csharp
using System.Drawing;
```

## Aspose.Drawing でビットマップを作成 – 測定単位の理解

### 手順 1: ビットマップの作成

キャンバスとして使用する 1000 × 800 ピクセルのビットマップを作成します。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 手順 2: Graphics オブジェクトの作成

`Graphics` オブジェクトはビットマップ上で描画機能を提供します。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## ポイントで矩形を描く

ポイントは従来の印刷単位です (1 ポイント = 1/72 インチ)。ページ単位をポイントに設定すると、タイポグラフィで慣れ親しんだ測定が可能になります。

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

次に、ポイント単位で矩形を描きます。ペン幅は 36 ポイント (½ インチ) に設定し、視認性を高めています。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

**プロのコツ:** 座標 `(72,72)` は左上隅から 1 インチオフセットに相当します。なぜなら 72 ポイント = 1 インチだからです。

## ミリメートルで矩形を描く

ミリメートルはエンジニアリング図面やメートル法の精度が必要な場合に最適です。

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

以下の矩形は 6.35 mm のペン (0.25 mm 相当) と、25.4 mm (1 インチ) の辺長を使用しています。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## インインチで矩形を描く

インチは米国の印刷や UI デザインで一般的です。インチ単位に切り替えることで、画面 DPI 設定と簡単に合わせられます。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

ここでは、0.125 インチ の細いペンで青い矩形を描きます。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 結果の保存

すべての図形を描いた後、ビットマップをファイルシステムに保存します。パスはご自身のドキュメントディレクトリに合わせて調整してください。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

保存した PNG を開くと、3 つの矩形が表示されます――それぞれ異なる測定単位で描画されています。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| **画像が空白になる** | 保存前に Graphics オブジェクトがフラッシュされていない | `bitmap.Save()` の前に `graphics.Dispose();` を呼び出す |
| **サイズが正しくない** | `PageUnit` の値が誤っている | `graphics.PageUnit` を目的の `GraphicsUnit` に設定しているか確認 |
| **ファイルパスエラー** | フォルダーが存在しない、または無効な文字が含まれる | 対象ディレクトリが存在することを確認し、`Path.Combine` を使用 |

## FAQ

### Q1: Aspose.Drawing for .NET は他の .NET フレームワークでも使用できますか？

A1: はい、Aspose.Drawing はさまざまな .NET フレームワークと互換性があり、開発環境に柔軟性を提供します。

### Q2: 無料トライアルはありますか？

A2: はい、[こちらから](https://releases.aspose.com/) 無料トライアルをご利用いただけます。

### Q3: Aspose.Drawing for .NET のサポートはどこで受けられますか？

A3: コミュニティサポートやディスカッションは [Aspose.Drawing フォーラム](https://forum.aspose.com/c/drawing/44) でご確認ください。

### Q4: 短期プロジェクト向けに一時ライセンスを購入できますか？

A4: はい、[こちらから](https://purchase.aspose.com/temporary-license/) 一時ライセンスをご取得いただけます。

### Q5: Aspose.Drawing の詳細ドキュメントはどこにありますか？

A5: 包括的なドキュメントは [こちら](https://reference.aspose.com/drawing/net/) で入手可能です。

## よくある質問

**Q: Aspose.Drawing は高 DPI のレンダリングをサポートしていますか？**  
A: はい。ライブラリはビットマップの DPI 設定を尊重し、高解像度ディスプレイでも鮮明な出力が可能です。

**Q: 1 つの描画内 は任意のタイミングで切り替え可能ですが、単位が混在しないよう現在の単位を把握しておく必要があります。

**Q: アンチエイリアスはデフォルトで有効ですか？**  
A: はい、`graphics.SmoothingMode` で明示的に無効化しない限り、Aspose.Drawing は形状とテキストにアンチエイリアスを適用します。

**Q: 描画後にリソースを解放するにはどうすればよいですか？**  
A: 終了時に `graphics.Dispose();` と `bitmap.Dispose();` を呼び出して、アンマネージドメモリを解放してください。

**Q: PNG 以外の形式でビットマップをエクスポートできますか？**  
A: `Bitmap.Save` メソッドは JPEG、BMP、GIF、TIFF もサポートしています。拡張子を変更すれば出力形式を切り替えられます。

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**最終更新日:** 2026-02-04  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose  

---