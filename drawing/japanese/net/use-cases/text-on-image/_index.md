---
date: 2026-02-27
description: .NET 用 Aspose.Drawing を使用して誕生日カード画像の作成方法を学びましょう。このガイドでは、画像に文字列を描画し、写真にテキストを重ね、写真にキャプションをすばやく追加する方法を示します。
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing を使用して誕生日カード画像を作成する方法
url: /ja/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing で誕生日カード画像を作成する方法

## はじめに
.NET 開発の動的な世界で、Aspose.Drawing は画像操作を簡単に行える強力なツールとして際立っています。**誕生日カード画像を作成**したり、透かしを追加したり、画像にテキストをオーバーレイしたりする必要がある場合、本チュートリアルでは C# を使用して画像に文字列を描画する手順を詳しく解説します。このガイドを終える頃には、共有できるパーソナライズされた誕生日カードが完成しています。

## クイック回答
- **どのライブラリを使用すべきですか？** Aspose.Drawing for .NET  
- **写真にキャプションを追加できますか？** はい – カスタムフォントで `Graphics.DrawString` を使用します。  
- **本番環境でライセンスは必要ですか？** はい、商用ライセンスが必要です。  
- **対応している .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6 以上。  
- **実装にどれくらい時間がかかりますか？** シンプルなカードであれば通常 10 分未満です。

## 誕生日カード画像とは？
誕生日カード画像とは、背景写真に挨拶文や受取人の名前、祝福メッセージなどのカスタムテキストを組み合わせたパーソナライズ画像です。Aspose.Drawing を使用すれば、手作業のグラフィックデザインツールを使わずにプログラムでこれらのカードを生成できます。

## なぜ Aspose.Drawing で画像にテキストをオーバーレイするのか？
- **クロスプラットフォーム対応:** Windows、Linux、macOS で動作します。  
- **豊富な描画 API:** フォント、色、レイアウトをフルコントロールできます。  
- **外部依存なし:** `System.Drawing.Common` の代わりに完全にマネージドなライブラリです。  
- **高性能:** 大量画像処理に最適化されています。

## 前提条件
チュートリアルに入る前に、以下が準備できていることを確認してください。

1. Aspose.Drawing ライブラリ: [Aspose.Drawing for .NET ドキュメント](https://reference.aspose.com/drawing/net/) からダウンロードしてインストールします。  
2. 開発環境: Visual Studio または Visual Studio Code などの .NET 開発環境に、.NET 6 SDK 以降がインストールされていること。

それでは、画像にテキストを追加し、誕生日カードとして保存する手順を順に見ていきましょう。

## 名前空間のインポート
C# プロジェクトに必要な名前空間をインポートします。

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## 手順 1: 画像の読み込み
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
ここでは、指定したファイルパスから画像を読み込み、以降の処理に使用する Graphics オブジェクトを初期化します。

## 手順 2: テキストプロパティの設定
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
色、フォント、余白などのテキストプロパティを定義します。デザインの好みに合わせてパラメータを調整してください。

## 手順 3: テキストサイズの測定
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
各単語を個別に測定してテキストに必要なサイズを計算します。これにより正しい配置が保証され、テキストの重なりを防げます。

## 手順 4: 画像にテキストを描画
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
計算されたサイズに基づいて画像上のテキスト位置を決め、指定したフォントと色で描画します。

## 手順 5: 画像の保存
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
変更した画像を任意のディレクトリに保存します。生成されたファイルが送信可能な誕生日カード画像です。

## 主な利用シーンとヒント
- **写真にキャプションを追加:** `text` を「Celebrating 30 Years!」など任意のキャプションに置き換えます。  
- **ビットマップにテキストを描画:** 最初から作成した `Bitmap` オブジェクトでも同様の手順が使えます。  
- **複数行のオーバーレイ:** 文字列配列をループし、各行の `Rectangle` Y 座標を調整します。  
- **プロのコツ:** `Graphics.SmoothingMode = SmoothingMode.AntiAlias` を使用すると、テキストがさらに滑らかに描画されます。

## 結論
Aspose.Drawing は .NET における画像操作タスクをシンプルにし、開発者に強力なツールキットを提供します。**誕生日カード画像を作成**したり、**画像に文字列を描画**したり、**写真にキャプションを追加**したりすることは、グラフィック要素を扱う上での一例に過ぎません。

## よくある質問
### Aspose.Drawing はすべての画像形式に対応していますか？
Aspose.Drawing は JPEG、PNG、GIF などの一般的な画像形式を含む幅広いフォーマットをサポートしています。完全な一覧は [ドキュメント](https://reference.aspose.com/drawing/net/) を参照してください。

### 商用プロジェクトで Aspose.Drawing を使用できますか？
はい、Aspose.Drawing は個人・商用プロジェクトの両方で使用できます。ライセンスの詳細は [購入ページ](https://purchase.aspose.com/buy) をご覧ください。

### テスト用の一時ライセンスは取得できますか？
はい、[Temporary License](https://purchase.aspose.com/temporary-license/) からテスト用の一時ライセンスを取得できます。

### Aspose.Drawing のコミュニティサポートはどこで得られますか？
[Aspose.Drawing フォーラム](https://forum.aspose.com/c/drawing/44) でコミュニティと交流し、サポートを受けられます。

### Aspose.Drawing の使い始め方は？
[こちら](https://releases.aspose.com/drawing/net/) からライブラリをダウンロードし、包括的な [ドキュメント](https://reference.aspose.com/drawing/net/) を参照してください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-02-27  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose  

---