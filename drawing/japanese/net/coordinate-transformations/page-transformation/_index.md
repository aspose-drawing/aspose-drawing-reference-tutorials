---
date: 2025-11-30
description: Aspose.Drawing for .NET を使用して、座標系変換を適用し、矩形ビットマップを描画し、ページを変換する方法を学びます。
language: ja
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: .NET 用 Aspose.Drawing の座標系変換（ページ変換）
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET における座標系変換（ページ変換）

## はじめに

ようこそ！このチュートリアルでは、Aspose.Drawing for .NET を使用して **ページ上で座標系変換を実行する方法** をご紹介します。**矩形ビットマップ** オブジェクトの描画、描画のスケーリング、またはページ単位をデバイス単位にマッピングする必要がある場合でも、以下の手順に従えば、プロジェクトにそのままコピーペーストできる形で簡潔に実装できます。

## クイック回答
- **描画の主要クラスは何ですか？** Aspose.Drawing の `Graphics`。
- **ページ単位はどう設定しますか？** `graphics.PageUnit = GraphicsUnit.Inch;` を使用します。
- **変換されたページに矩形を描画できますか？** はい、`Pen` を作成し `DrawRectangle` を呼び出します。
- **出力はどこに保存されますか？** `bitmap.Save` で指定したフォルダーに保存されます。
- **本番環境でライセンスは必要ですか？** 商用利用には有効な Aspose.Drawing ライセンスが必要です。

## 座標系変換とは？

**座標系変換** とは、論理的なページ座標（インチやミリメートルなど）を物理的なデバイス座標（ピクセル）にマッピングする方法を変更することです。変換を調整することで、スケーリング、回転、平行移動をすべての描画操作に対して制御でき、解像度に依存しないグラフィックの設計が容易になります。

## Aspose.Drawing をページ変換に使用する理由

- **完全な .NET 互換性** – .NET Framework、.NET Core、.NET 5/6 で動作します。
- **豊富なグラフィック API** – System.Drawing.Common と同等の機能を、プラットフォーム制限なしで提供します。
- **シンプルな単位処理** – 1 つのプロパティでインチ、ミリメートル、ポイントなどを切り替えられます。
- **高品質な出力** – PNG、JPEG、BMP などのフォーマットを正確に制御して生成できます。

## 前提条件

始める前に以下を用意してください。

- **Aspose.Drawing ライブラリ** – 公式サイトから最新バージョンをダウンロードしてください [こちら](https://releases.aspose.com/drawing/net/)。
- **開発環境** – Visual Studio（任意のエディション）またはその他の .NET IDE。
- **書き込み権限** – 変換後の画像を保存するフォルダー（コード中の `"Your Document Directory"` を実際のパスに置き換えてください）。

準備ができたら、各ステップを順に見ていきましょう。

## 名前空間のインポート

まず、必要な名前空間をスコープに持ち込みます。

```csharp
using System.Drawing;
```

> *重要ポイント*: `System.Drawing` には、このチュートリアルで使用する `Bitmap`、`Graphics`、`Pen`、および色構造体が含まれています。

## 手順 1: ビットマップの作成

変換された描画をホストする空のキャンバスを作成します。サイズは **1000 × 800 ピクセル**、アルファ透過をサポートするピクセル形式を指定します。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> このビットマップが描画面となります。選択したピクセル形式（`Format32bppPArgb`）は、事前乗算アルファで高品質なレンダリングを実現します。

## 手順 2: Graphics オブジェクトの作成

`Graphics` オブジェクトは描画メソッド（線、形状、テキスト）を提供します。先ほど作成したビットマップから取得します。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> `Graphics` オブジェクトはすべてのレンダリング操作の中心であり、次に適用する変換設定を尊重します。

## 手順 3: キャンバスのクリア

何かを描画する前に、キャンバスを中立的な背景色（この例ではグレー）でクリアします。このステップは、ビットマップ全体を単色で塗りつぶす方法も示しています。

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## 手順 4: 変換の設定（ページ変換の適用）

ここで **ページ変換** を適用し、`PageUnit` をインチに設定します。これにより、以降のすべての座標がピクセルではなくインチとして解釈されます。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *ヒント*: `PageUnit` を変更するだけで、**ページ座標を変換する方法** を手動でピクセル計算せずに実現できます。

## 手順 5: 矩形の描画（draw rectangle bitmap）

次に、**1 インチ × 1 インチ** の矩形を位置 (1, 1) インチに描画します。`Pen` の幅は `0.1f` インチに設定し、細くても見える線にしています。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> これは変換が適用された後の **draw rectangle bitmap** の例です。矩形のサイズがピクセルではなくインチで定義されていることに注目してください。

## 手順 6: 画像の保存

最後に、変換されたビットマップをディスクに永続化します。`"Your Document Directory"` を実際のフォルダー パスに置き換えてください。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> 出力ファイル（`PageTransformation_out.png`）には、先ほど設定した座標系変換を使用して描画された矩形が含まれます。

## よくある問題と解決策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| **画像が空白になる** | キャンバスがクリアされていない、または描画が見えない領域で行われている | `graphics.PageUnit` と座標値を確認し、矩形がビットマップの範囲内に収まっているか確認してください。 |
| **スケーリングが正しくない** | 誤った `GraphicsUnit` を使用している | 使用したい単位（例: `GraphicsUnit.Inch`）と `graphics.PageUnit` が一致しているか再確認してください。 |
| **ファイルパスエラー** | フォルダーが存在しない、または無効な文字が含まれている | 事前に対象フォルダーを作成するか、`Path.Combine` を使用して安全にパスを構築してください。 |

## FAQ

**Q: Aspose.Drawing は無料で使えますか？**  
A: 無料トライアルは [こちら](https://releases.aspose.com/) から利用できます。

**Q: Aspose.Drawing の詳細なドキュメントはどこにありますか？**  
A: ドキュメントは [こちら](https://reference.aspose.com/drawing/net/) にあります。

**Q: Aspose.Drawing のサポートはどこで受けられますか？**  
A: サポートは [Aspose.Drawing フォーラム](https://forum.aspose.com/c/diagram/17) で提供されています。

**Q: Aspose.Drawing の一時ライセンスは入手できますか？**  
A: はい、[こちら](https://purchase.aspose.com/temporary-license/) から取得可能です。

**Q: Aspose.Drawing はどこで購入できますか？**  
A: 購入は [こちら](https://purchase.aspose.com/buy) から行えます。

## 結論

これで **座標系変換の適用**、**draw rectangle bitmap** オブジェクトの描画、そして **結果の保存** 方法を Aspose.Drawing for .NET を使って習得できました。これらの基本ブロックを組み合わせることで、解像度に依存しないグラフィックを作成でき、レポートや UI 要素、正確なサイズ指定が必要なあらゆるシナリオに最適です。`GraphicsUnit` を `Millimeter` や `Point` などに変更して、描画への影響をぜひ試してみてください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2025-11-30  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作成者:** Aspose