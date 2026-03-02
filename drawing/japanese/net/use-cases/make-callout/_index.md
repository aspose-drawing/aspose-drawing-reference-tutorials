---
date: 2026-03-02
description: Aspose.Drawing for .NET を使用して、ドキュメントのイラストを強化しましょう！より明確で情報豊かなビジュアルのために、コールアウトの追加方法をステップバイステップで学びましょう。
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: .NET 用 Aspose.Drawing でコールアウトを追加する方法
url: /ja/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing でコールアウトを作成する

## はじめに
Aspose.Drawing for .NET を使用して画像や図に **コールアウトを追加する方法** をお探しなら、ここが最適な場所です。このチュートリアルでは、画像の読み込みから美しくスタイリングされたコールアウトの描画まで、プロセス全体を順を追って解説します。イラストをより分かりやすく、情報豊かにすることができます。

## クイック回答
- **どのライブラリが必要ですか？** Aspose.Drawing for .NET（公式サイトからダウンロード可能）。  
- **対応している .NET バージョンは？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **ライセンスは必要ですか？** 開発用には無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **実装にどれくらい時間がかかりますか？** 基本的なコールアウトであれば通常 10 分未満です。  
- **色やフォントはカスタマイズできますか？** はい—すべて標準の GDI+ オブジェクト（Pen、Font、Brush）で制御できます。

## Aspose.Drawing でコールアウトを追加する方法
以下は **画像にコールアウトを追加する方法** を示す簡潔なステップバイステップガイドです。コードをコピーして位置を試したり、スタイルをブランドに合わせて調整したりしてください。

## 前提条件
作業を始める前に以下を確認してください。

- C# プログラミング言語の基本的な知識。  
- Aspose.Drawing ライブラリがインストール済み。ダウンロードは [here](https://releases.aspose.com/drawing/net/) から。  
- コールアウトを追加したいドキュメントまたは画像。

## 名前空間のインポート
プロジェクトに必要な名前空間が含まれていることを確認してください。

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## ステップ 1: 画像をロードする
コールアウトを追加したい画像をロードします。`"Your Document Directory"` と `"gears.png"` を実際のディレクトリと画像ファイル名に置き換えてください。

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## ステップ 2: Graphics オブジェクトを作成する
画像から `Graphics` オブジェクトを作成し、描画操作を行えるようにします。

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## ステップ 3: コールアウトの位置を定義する
各コールアウトの開始点と終了点、さらにコールアウトの値と単位を定義します。

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

## ステップ 4: コールアウトを描画する
画像上にコールアウトを描画する `DrawCallOut` メソッドを実装します。

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## ステップ 5: 画像を保存する
コールアウトを付加した画像を希望のディレクトリに保存します。

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## コールアウト描画のソースコード
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

## よくある問題とヒント
- **アンカー座標が正しくない** – 開始点と終了点が画像の範囲内にあることを確認してください。範囲外だとコールアウトが切り取られる可能性があります。  
- **テキストが重なる** – `spaceSize` やフォントサイズを調整し、ラベルが他のグラフィックと衝突しないようにしてください。  
- **パフォーマンス** – 非常に大きな画像を扱う場合、使用後に `Pen`、`Font`、`Brush` オブジェクトを破棄してリソースを解放することを検討してください。

## 結論
おめでとうございます！これで Aspose.Drawing for .NET を使って画像に **コールアウトを追加する方法** が分かりました。さまざまな位置、色、フォントを試して、ビジュアルスタイルに合わせてカスタマイズしてください。

## よくある質問

### Aspose.Drawing を他の種類のイラストに使用できますか？
はい、Aspose.Drawing はさまざまなイラスト向けの描画操作を幅広くサポートしています。

### Aspose.Drawing は異なる画像フォーマットに対応していますか？
もちろんです！Aspose.Drawing は PNG、JPEG、GIF などの一般的な画像フォーマットをサポートしています。

### もっと多くのサンプルやドキュメントはどこで見つけられますか？
包括的なドキュメントは [here](https://reference.aspose.com/drawing/net/) で確認できます。

### 問題が発生した場合、どこでサポートを受けられますか？
コミュニティサポートは [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) で提供されています。

### 購入前に Aspose.Drawing を試すことはできますか？
はい、無料トライアルは [here](https://releases.aspose.com/) から開始できます。

**追加の Q&A**

**Q: コールアウトの線スタイル（破線、点線）を変更できますか？**  
A: はい—線を描画する前に `Pen.DashStyle` プロパティを設定すれば変更できます。

**Q: コールアウトラベルに背景色を付けることは可能ですか？**  
A: 可能です。希望の色で `SolidBrush` を作成し、`DrawString` を呼び出す前にテキストの背後に矩形を塗りつぶしてください。

**Q: 高 DPI ディスプレイでもコールアウトの見た目を同じにするには？**  
A: `graphics.PageUnit = GraphicsUnit.Pixel`（上記コード参照）を設定し、ベクトルベースの測定を使用すればスケーリングが一貫します。

---

**最終更新日:** 2026-03-02  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}