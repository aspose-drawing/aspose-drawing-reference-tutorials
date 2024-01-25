---
title: Aspose.Drawing で吹き出しを作成する
linktitle: Aspose.Drawing で吹き出しを作成する
second_title: Aspose.Drawing .NET API - System.Drawing.Common の代替
description: Aspose.Drawing for .NET を使用してドキュメントのイラストを強化しましょう。コールアウトを追加して、より明確で有益なビジュアルを実現する方法を段階的に学習します。
type: docs
weight: 10
url: /ja/net/use-cases/make-callout/
---
## 導入
Aspose.Drawing for .NET でコールアウトを作成するためのステップバイステップ ガイドへようこそ。吹き出しを使用して文書のイラストを強化したい場合は、ここが正しい場所です。このチュートリアルでは、Aspose.Drawing ライブラリを使用して、プロセスを管理可能なステップに分割します。
## 前提条件
チュートリアルに入る前に、次の前提条件を満たしていることを確認してください。
- C# プログラミング言語の基本的な知識。
-  Aspose.Drawing ライブラリがインストールされています。ダウンロードできます[ここ](https://releases.aspose.com/drawing/net/).
- 吹き出しを追加するドキュメントまたは画像。
## 名前空間のインポート
必要な名前空間がプロジェクトに含まれていることを確認してください。
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## ステップ 1: 画像をロードする
まず、吹き出しを追加する画像をロードします。交換する`"Your Document Directory"`そして`"gears.png"`実際のディレクトリと画像ファイル名を置き換えます。
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    //コードはここにあります
}
```
## ステップ 2: グラフィックス オブジェクトを作成する
を作成します`Graphics`画像からオブジェクトを取得して描画操作を実行します。
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## ステップ 3: 吹き出しの位置を定義する
各コールアウトの開始点と終了点、およびコールアウトの値と単位を定義します。
```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```
## ステップ 4: 吹き出しを描画する
を実装します。`DrawCallOut`画像上に吹き出しを描画するメソッド。
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## ステップ 5: 画像を保存する
吹き出し付きの画像を目的のディレクトリに保存します。
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## 描画コールアウトのソースコード
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```
## 結論

おめでとう！ Aspose.Drawing for .NET を使用して画像に吹き出しを追加することに成功しました。さまざまな位置と値を自由に試して、吹き出しをさらにカスタマイズしてください。

## よくある質問

### Aspose.Drawing を他のタイプのイラストに使用できますか?

はい、Aspose.Drawing は、さまざまなタイプのイラストに対する幅広い描画操作をサポートしています。

### Aspose.Drawing はさまざまな画像形式と互換性がありますか?

絶対に！ Aspose.Drawing は、PNG、JPEG、GIF などの一般的な画像形式をサポートしています。

### 他の例やドキュメントはどこで入手できますか?

包括的なドキュメントを調べる[ここ](https://reference.aspose.com/drawing/net/).

### 問題が発生した場合はどうすればサポートを受けられますか?

訪問[Aspose.Drawing フォーラム](https://forum.aspose.com/c/diagram/17)コミュニティサポートのために。

### 購入する前に Aspose.Drawing を試してみることはできますか?

確かに！無料トライアルを始めてみる[ここ](https://releases.aspose.com/).