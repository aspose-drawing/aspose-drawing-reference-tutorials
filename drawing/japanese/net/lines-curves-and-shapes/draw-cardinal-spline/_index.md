---
date: 2026-02-12
description: .NET と Aspose.Drawing を使用して画像を保存し、カーディナルスプラインを描画する方法を学びましょう。曲線を PNG として保存し、スムーズなグラフィックを簡単に作成できます。
linktitle: Drawing Cardinal Splines in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawingで画像を保存し、カーディナルスプラインを描く方法
url: /ja/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawingで画像を保存し、カーディナルスプラインを描く方法

## Introduction

このチュートリアルでは、Aspose.Drawing for .NET を使用して、滑らかなカーディナルスプラインを描画しながら **画像を保存** する方法を紹介します。チャートコンポーネントやダイアグラムエディタを構築する場合、またはカスタム曲線を PNG としてエクスポートしたい場合でも、以下の手順でペンで曲線を描き、スプラインをカスタマイズし、結果をディスクに永続化する方法が正確に示されています。

## Quick Answers
- **主なメソッドは何をしますか？** `Graphics.DrawCurve` は一連のポイントを滑らかなカーディナルスプラインに補間します。  
- **画像の保存形式は何ですか？** `Bitmap.Save` を使用した PNG。  
- **画像を保存するのにライセンスは必要ですか？** 開発段階ではトライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **曲線のテンションを変更できますか？** はい、`DrawCurve` のオーバーロードでテンションを指定できます。  
- **Aspose.Drawing は .NET 6+ と互換性がありますか？** 完全に対応しています – .NET Framework と .NET Core/5/6 の両方をサポートします。

## What is “how to save image” in the context of Aspose.Drawing?
画像を保存することは、描画したメモリ上のビットマップを PNG、JPEG、BMP などの物理ファイルに変換することを意味します。Aspose.Drawing はエンコード処理を自動で行うシンプルな `Bitmap.Save` メソッドを提供しています。

## Why draw a cardinal spline with Aspose.Drawing?
カーディナルスプラインは、制御点の近くを滑らかに通過する曲線を生成でき、データ可視化、UI グラフィック、カスタムシェイプに最適です。Aspose.Drawing を使用すれば `System.Drawing.Common` の制限を回避し、クロスプラットフォームで一貫した描画が可能になります。

## Prerequisites

開始する前に以下を用意してください：

- Visual Studio（最近のバージョン）をインストール済み。  
- Aspose.Drawing for .NET ライブラリ。ダウンロードは [here](https://releases.aspose.com/drawing/net/) から。  
- C# の基本的なプログラミング知識。

## Import Namespaces

C# ファイルの先頭で必要な名前空間をインポートします：

```csharp
using System.Drawing;
```

## Step 1: Create a Bitmap (Canvas)

まず、描画用キャンバスとして機能するビットマップを作成します。このビットマップ上でスプラインが描画され、**画像を保存** する前の中間結果となります。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Step 2: Create a Graphics Object

次に、ビットマップから `Graphics` オブジェクトを取得します。このオブジェクトが描画サーフェスを提供します。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Step 3: Define Pen and Draw Curve

希望する色と幅で `Pen` を定義し、`DrawCurve` を使用してカーディナルスプラインを描画します。これは **ペンで曲線を描く** テクニックのデモであり、**カーディナルスプラインの例** でもあります。

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

## Step 4: Save the Image (Save Curve as PNG)

最後に、ビットマップを PNG ファイルとして永続化します。これが本チュートリアルの **画像を保存する方法** の核心です。

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Pro tip:** `Path.Combine` を使用して、プラットフォーム間で安全にファイルパスを構築しましょう。

Congratulations! You have successfully drawn a cardinal spline and saved the result as a PNG image using Aspose.Drawing for .NET. Feel free to experiment with different point arrays, pen colors, or line widths to customize your curves.

## Common Use Cases

- **データ可視化** – 正確な制御点が必要な滑らかな折れ線グラフ。  
- **カスタム UI コンポーネント** – ノブ、スライダー、装飾的なボーダーの描画。  
- **エクスポート可能なグラフィック** – レポートやウェブコンテンツ向けに PNG アセットをリアルタイム生成。

## Troubleshooting & Tips

- **画像が空白になっている？** ビットマップのピクセル形式がアルファをサポートしているか (`Format32bppPArgb`) を確認し、必要に応じて `graphics.Clear(Color.Transparent)` を呼び出してください。  
- **曲線の形状が予期せぬものになった？** `DrawCurve(pen, points, tension)` のオーバーロードでテンションパラメータを調整します。  
- **ファイルアクセスエラーが出る？** 目的のディレクトリが存在し、アプリケーションに書き込み権限があることを確認してください。

## Frequently Asked Questions

### Q1: Can I use Aspose.Drawing for commercial projects?
A1: Yes, Aspose.Drawing is suitable for both personal and commercial projects. Check the licensing details on the [purchase page](https://purchase.aspose.com/buy).

### Q2: How can I get a temporary license for testing?
A2: Obtain a temporary license for testing purposes [here](https://purchase.aspose.com/temporary-license/).

### Q3: Where can I find additional support?
A3: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) for community support and discussions.

### Q4: Is there a free trial available?
A4: Yes, explore the features with the [free trial](https://releases.aspose.com/) version before making a purchase.

### Q5: How do I access the documentation?
A5: Refer to the comprehensive [documentation](https://reference.aspose.com/drawing/net/) for detailed information and examples.

### Q6: Can I change the output format to JPEG?
A6: Absolutely. Replace the `.png` extension with `.jpg` and specify `ImageFormat.Jpeg` in the `Save` method.

### Q7: Is it possible to draw multiple splines on the same bitmap?
A7: Yes, simply call `graphics.DrawCurve` multiple times with different point arrays and pens.

## Conclusion

In this guide we covered **how to save image** files after drawing a cardinal spline, demonstrated a practical **draw curve using C#**, and highlighted common scenarios where this technique shines. You now have a solid foundation to integrate smooth spline graphics into any .NET application.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}