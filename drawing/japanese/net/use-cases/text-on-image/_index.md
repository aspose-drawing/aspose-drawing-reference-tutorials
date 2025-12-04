---
title: Aspose.Drawing で画像にテキストを追加する
linktitle: Aspose.Drawing で画像にテキストを追加する
second_title: Aspose.Drawing .NET API - System.Drawing.Common の代替
description: Aspose.Drawing for .NET を使用して、テキストを画像にシームレスに統合する方法を試してください。ステップバイステップのガイドに従って、簡単に画像を操作してください。ダウンロード中！
weight: 12
url: /ja/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing で画像にテキストを追加する

## 導入
.NET 開発の動的な世界では、Aspose.Drawing は画像を簡単に操作するための強力なツールとして際立っています。透かし、注釈、またはパーソナライズされたグラフィックの作成など、画像にテキストを追加することは一般的な要件です。このチュートリアルでは、Aspose.Drawing を活用して、C# を使用してテキストを画像にシームレスに統合する方法を検討します。
## 前提条件
チュートリアルに入る前に、次のものが整っていることを確認してください。
1.  Aspose.Drawing ライブラリ: Aspose.Drawing ライブラリを次の場所からダウンロードしてインストールします。[Aspose.Drawing for .NET ドキュメント](https://reference.aspose.com/drawing/net/).
2. 開発環境: Visual Studio またはその他の互換性のある IDE を含む、動作する .NET 開発環境を用意します。
それでは、ステップバイステップのガイドを始めましょう。
## 名前空間のインポート
まず、必要な名前空間を C# プロジェクトにインポートします。
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## ステップ 1: 画像をロードする
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
ここでは、指定されたファイル パスから画像をロードし、さらなる処理のためにグラフィックス オブジェクトを初期化します。
## ステップ 2: テキストのプロパティを設定する
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
色、フォント、パディングなどのテキストのプロパティを定義します。好みに応じてこれらのパラメータを調整します。
## ステップ 3: テキストのサイズを測定する
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
各単語を個別に測定して、テキストに必要なサイズを計算します。これにより、適切な配置が確保され、テキストの重なりが回避されます。
## ステップ 4: 画像上にテキストを描画する
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
次に、計算されたサイズに基づいて画像上にテキストを配置し、指定したフォントと色を使用して描画します。
## ステップ 5: 画像を保存する
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
変更したイメージを目的のディレクトリに保存します。
このステップバイステップのガイドでは、Aspose.Drawing for .NET を使用して画像にテキストを追加する簡単なプロセスを示します。目的の視覚効果を実現するために、さまざまなフォント、色、テキスト コンテンツを試してください。
## 結論
Aspose.Drawing は、.NET での画像操作タスクを簡素化し、開発者に堅牢なツールキットを提供します。画像へのテキストの追加はその機能の一例にすぎず、グラフィック要素の処理におけるライブラリの多用途性を示しています。
## よくある質問
### Aspose.Drawing はすべての画像形式と互換性がありますか?
Aspose.Drawing は、JPEG、PNG、GIF などの一般的な画像形式を含む、幅広い画像形式をサポートしています。を参照してください。[ドキュメンテーション](https://reference.aspose.com/drawing/net/)完全なリストについては、
### Aspose.Drawing を商用プロジェクトに使用できますか?
はい、Aspose.Drawing は個人プロジェクトと商用プロジェクトの両方に適しています。ライセンスの詳細については、次のサイトを参照してください。[購入ページ](https://purchase.aspose.com/buy).
### 一時ライセンスはテスト目的で利用できますか?
はい。次のサイトにアクセスして、テスト用の一時ライセンスを取得できます。[仮免許](https://purchase.aspose.com/temporary-license/).
### Aspose.Drawing のコミュニティ サポートはどこで見つけられますか?
コミュニティに参加してサポートを受けましょう[Aspose.Drawing フォーラム](https://forum.aspose.com/c/diagram/17).
### Aspose.Drawing を使い始めるにはどうすればよいですか?
まずはライブラリをダウンロードしてください[ここ](https://releases.aspose.com/drawing/net/)包括的なものを探求します[ドキュメンテーション](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
