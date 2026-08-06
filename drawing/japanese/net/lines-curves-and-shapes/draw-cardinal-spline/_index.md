---
date: 2026-05-29
description: .NET と Aspose.Drawing を使用して PNG を保存し、Cardinal Splines を描画する方法を学びます。曲線を
  PNG として保存し、滑らかなグラフィックを作成し、bitmap をファイルに簡単に生成します。
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Aspose.Drawing で Cardinal Splines を描画
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing で PNG を保存し、Cardinal Splines を描画する方法
url: /ja/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG を保存し、Aspose.Drawing でカーディナルスプラインを描く方法

## はじめに

このチュートリアルでは、Aspose.Drawing for .NET を使用して滑らかなカーディナルスプラインを描きながら **PNG を保存する方法** を学びます。チャートコンポーネントやダイアグラムエディタの作成、あるいはカスタム曲線を PNG としてエクスポートしたい場合など、以下の手順でビットマップキャンバスの作成、ペンでのスプライン描画、結果のディスクへの保存方法を順に説明します。また、Aspose.Drawing が System.Drawing.Common の信頼できるクロスプラットフォーム代替である理由もご紹介します。

## クイック回答
- **主なメソッドは何をしますか？** `Graphics.DrawCurve` は一連のポイントを滑らかなカーディナルスプラインに補間します。  
- **画像の保存に使用されるフォーマットは？** `Bitmap.Save` を使用した PNG。  
- **画像を保存するのにライセンスが必要ですか？** 開発にはトライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **曲線のテンションを変更できますか？** はい、`DrawCurve` のオーバーロードでテンションを指定できます。  
- **Aspose.Drawing は .NET 6 以降に対応していますか？** はい、.NET Framework と .NET Core/5/6 をサポートしています。

## Aspose.Drawing のコンテキストで「PNG を保存する方法」とは何ですか？

PNG を保存するとは、描画対象のメモリ上のビットマップをディスク上の実際の PNG ファイルに変換することを意味します。このプロセスはロスレス圧縮でピクセルデータを書き込み、正確な色とアルファチャンネル情報を保持します。Aspose.Drawing の `Bitmap.Save` メソッドが PNG エンコードを自動的に処理するため、フォーマットの詳細を自分で管理する必要はありません。

## なぜ Aspose.Drawing でカーディナルスプラインを描くのか？

カーディナルスプラインは、制御点のセットに沿って滑らかで流れるような曲線を生成し、データ可視化、UI グラフィック、カスタム形状に最適です。Aspose.Drawing は **30 以上の画像フォーマット** をサポートし、ファイル全体をメモリに読み込むことなく数百ページにわたるグラフィックをレンダリングできるため、速度と柔軟性の両方を提供します。

## 前提条件

- Visual Studio（最新バージョン）をインストール済み。  
- Aspose.Drawing for .NET ライブラリ。こちらからダウンロードできます [here](https://releases.aspose.com/drawing/net/)。  
- C# プログラミングの基本知識。

## 名前空間のインポート

C# ファイルで、まず必要な名前空間をインポートします。

`Aspose.Drawing` 名前空間には、`Bitmap`、`Graphics`、`Pen` などのコア型がすべて含まれています。  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## 手順 1: ビットマップ（キャンバス）を作成

まず、描画のキャンバスとなるビットマップを作成します。このビットマップはスプラインが描画され、**画像を保存**する前の領域です。

ビットマップは、定義されたピクセルフォーマットとサイズを持つメモリ上の画像を表します。  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 手順 2: Graphics オブジェクトを作成

次に、ビットマップから `Graphics` オブジェクトを取得します。このオブジェクトが描画面を提供します。

Graphics は、ビットマップ上に形状、テキスト、画像を描画するためのサーフェスを提供します。  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 手順 3: Pen を定義して曲線を描く

希望の色と幅で `Pen` を定義し、`DrawCurve` を使用してカーディナルスプラインを描画します。これにより **ペンで曲線を描く** 手法を示し、**カーディナルスプラインの例**となります。

Pen は、線や曲線の描画に使用される色、幅、ラインスタイルをカプセル化します。  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## 手順 4: 画像を保存（曲線を PNG として保存）

最後に、ビットマップを PNG ファイルとして保存します。これが本チュートリアルにおける **PNG を保存する方法** の核心です。

Bitmap.Save は、指定されたフォーマット（例: PNG）で画像をファイルに書き込みます。  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **プロのヒント:** `Path.Combine` を使用して、プラットフォーム間で安全にファイルパスを構築しましょう。

おめでとうございます！Aspose.Drawing for .NET を使用してカーディナルスプラインを描画し、結果を PNG 画像として保存できました。さまざまなポイント配列、ペンの色、線幅を試して、曲線をカスタマイズしてみてください。

## 一般的な使用例

- **データ可視化** – 正確な制御点が必要な滑らかな折れ線グラフ。  
- **カスタム UI コンポーネント** – ノブ、スライダー、装飾的なボーダーの描画。  
- **エクスポート可能なグラフィック** – レポートやウェブコンテンツ用に PNG アセットをリアルタイムで生成。

## トラブルシューティングとヒント

- **画像が空白になる場合** ビットマップのピクセルフォーマットがアルファをサポートしているか（`Format32bppPArgb`）を確認し、必要に応じて `graphics.Clear(Color.Transparent)` を呼び出してください。  
- **曲線の形状が予期せぬもの** オーバーロード `DrawCurve(pen, points, tension)` を使用してテンションパラメータを調整してください。  
- **ファイルアクセスエラー** ターゲットディレクトリが存在し、アプリケーションに書き込み権限があることを確認してください。

## よくある質問

**Q1: Aspose.Drawing を商用プロジェクトで使用できますか？**  
A1: はい、Aspose.Drawing は個人・商用プロジェクトの両方に適しています。ライセンス詳細は [購入ページ](https://purchase.aspose.com/buy) で確認してください。

**Q2: テスト用の一時ライセンスはどう取得できますか？**  
A2: テスト目的の一時ライセンスは [こちら](https://purchase.aspose.com/temporary-license/) で取得できます。

**Q3: 追加サポートはどこで得られますか？**  
A3: コミュニティサポートやディスカッションは [Aspose.Drawing フォーラム](https://forum.aspose.com/c/drawing/44) をご覧ください。

**Q4: 無料トライアルはありますか？**  
A4: はい、購入前に [無料トライアル](https://releases.aspose.com/) バージョンで機能をお試しください。

**Q5: ドキュメントへのアクセス方法は？**  
A5: 詳細情報やサンプルは包括的な [ドキュメント](https://reference.aspose.com/drawing/net/) を参照してください。

---

**最終更新日:** 2026-05-29  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
