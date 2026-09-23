---
date: 2026-09-23
description: C# と Aspose.Drawing を使用して PNG 画像を保存する方法、インストール済みフォントの一覧取得、カスタムフォントでテキストを描画する方法、そして高品質グラフィックのためにビットマップ解像度を調整する方法を学びます。
keywords:
- save png image c#
- installed fonts aspnet
- aspose.drawing bitmap graphics
- c# font collection
- png export .net
lastmod: 2026-09-23
linktitle: C# と Aspose.Drawing を使用して PNG 画像を保存し、インストール済みフォントを利用する
og_description: C# と Aspose.Drawing を使用して PNG 画像を保存します。このガイドでは、インストール済みフォントの一覧取得、テキストの描画、そしてプロフェッショナルなグラフィックのためのビットマップ解像度の制御方法を示します。
og_image_alt: Developer guide showing C# code that creates a bitmap, lists system
  fonts, and saves a PNG file with Aspose.Drawing
og_title: C# と Aspose.Drawing を使用して PNG 画像を保存し、インストール済みフォントを利用する
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  headline: Save PNG image in C# with Aspose.Drawing and installed fonts
  type: TechArticle
- description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  name: Save PNG image in C# with Aspose.Drawing and installed fonts
  steps:
  - name: Create a bitmap (the canvas)
    text: '`Bitmap` is the raster image object that holds pixel data for the canvas.'
  - name: Create graphics from bitmap
    text: '`Graphics` is the object that supplies drawing functions such as drawing
      shapes and text onto a bitmap.'
  - name: Set up brush and font (draw text with fonts)
    text: '`Brush` defines how shapes and text are filled with colour, while `Font`
      specifies the typeface, size, and style for text rendering.'
  - name: List installed fonts and show font families
    text: '`InstalledFontCollection` provides access to all font families installed
      on the host system.'
  - name: Save PNG image
    text: '`bitmap.Save` writes the bitmap to a file in the chosen image format, such
      as PNG. > **Pro tip:** Use `Path.Combine` for building file paths to avoid issues
      with directory separators on different operating systems.'
  type: HowTo
- questions:
  - answer: Yes. Load the font file into a `PrivateFontCollection` and create a `Font`
      from that collection, then draw it the same way as system fonts.
    question: Can I use custom fonts that are not installed on the machine?
  - answer: Wrap font creation in a `try/catch` block and inspect `ArgumentException`
      for missing families; provide a fallback font such as `Arial`.
    question: How do I handle font‑related exceptions?
  - answer: Absolutely. The library works in ASP.NET Core, Azure Functions, and other
      server‑side .NET environments without needing GDI+.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify
      the `FontStyle` enum to apply bold, italic, or underline.
    question: Can I change the text colour or style?
  - answer: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – bitmap graphics and font handling
tags:
- save png
- aspose.drawing
- c# graphics
- installed fonts
- bitmap
title: C# と Aspose.Drawing を使用して PNG 画像を保存し、インストール済みフォントを利用する
url: /ja/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# で PNG 画像を保存し、Aspose.Drawing とインストール済みフォントを使用する

## はじめに

C# で **PNG 画像を保存** し、同時に **ビットマップ グラフィックを作成** したい場合、Aspose.Drawing for .NET はクリーンでクロスプラットフォームな方法を提供します。このチュートリアルでは、インストール済みフォントの一覧取得、フォントファミリーの表示、ビットマップからのグラフィック作成、フォントを使用したテキスト描画を順に解説し、最終的に PNG 画像として保存します。最後まで読むと、Windows、Linux、macOS のいずれでも動作する .NET プロジェクトに組み込める再利用可能なコードスニペットが手に入ります。

## クイック回答
- **このチュートリアルは何を作成しますか？** ホストマシンにインストールされているフォントファミリーの一覧を示す PNG 画像です。  
- **必要なライブラリはどれですか？** Aspose.Drawing for .NET（System.Drawing.Common への依存はありません）。  
- **カスタムフォントを使用できますか？** はい – `InstalledFontCollection` または `PrivateFontCollection` にロードします。  
- **出力解像度は調整可能ですか？** もちろんです – ビットマップのサイズやピクセルフォーマットを変更して解像度を制御できます。  
- **コード実行にライセンスは必要ですか？** 評価用には一時ライセンスで動作しますが、本番環境では正式ライセンスが必要です。

## Aspose.Drawing のコンテキストで「PNG 画像を保存する」とは何ですか？

`Bitmap` は Aspose.Drawing のラスタ画像コンテナで、ピクセルデータを格納します。  
PNG 画像を保存するとは、描画対象である `Bitmap` を `.png` 拡張子のファイルにレンダリングすることです。Aspose.Drawing はロスレス PNG 圧縮を行い、メモリを使い果たすことなく **10 000 × 10 000 ピクセル** までの画像を処理できます。これにより高解像度グラフィックに適しています。生成されたファイルはウェブページ、レポート、またはさらなる画像処理パイプラインで使用できます。

## なぜインストール済みフォントを一覧表示し、フォントファミリーを示すのか？

インストール済みフォントを一覧表示することで、アプリケーションはエンドユーザーの環境に適応し、余分なフォントファイルを配布せずに生成されたグラフィックが企業のブランディングやユーザーの好みに合致することを保証できます。`InstalledFontCollection` は OS にインストールされたフォントを列挙します。これは、レポートの自動生成、証明書、またはシステムのタイポグラフィを尊重すべきあらゆるビジュアルコンテンツに特に有用です。

## Aspose.Drawing を使用して C# でビットマップ グラフィックを作成する方法は？

`Bitmap` は画像キャンバスを表し、`Graphics` はそのキャンバス上で描画するメソッドを提供します。`Font` はテキスト描画に使用する書体を表します。数行のコードで完全な PNG を作成できます：`Bitmap` を作成し、`Graphics` オブジェクトを取得し、インストール済みコレクションから取得した `Font` でテキストを描画し、最後に `bitmap.Save` を呼び出します。以下のステップバイステップガイドで各部分を詳しく解説し、実用的なヒントを追加しています。

## 前提条件

- **Aspose.Drawing ライブラリ** – 最新バージョンは [Aspose Drawing ダウンロードページ](https://releases.aspose.com/drawing/net/) からダウンロードしてください。  
- **IDE** – Visual Studio、Rider、または任意の .NET 対応エディタ。  
- **基本的な C# の知識** – クラス、オブジェクト、簡単なループに慣れている必要があります。  
- **.NET ランタイム** – フルクロスプラットフォームサポートのために .NET 6 以上または .NET Core 3.1 以上を推奨します。

## 名前空間のインポート

C# ファイルの先頭に以下の `using` 文を追加し、コンパイラがグラフィックおよびフォントの型を見つけられるようにします：

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Text;
using System.IO;
```

## ステップバイステップガイド

### ステップ 1: ビットマップ（キャンバス）を作成

`Bitmap` はキャンバスのピクセルデータを保持するラスタ画像オブジェクトです。  

```csharp
using System.Drawing;
using System.Drawing.Text;
```

### ステップ 2: ビットマップから Graphics を作成

`Graphics` はビットマップ上に図形やテキストを描画する機能を提供するオブジェクトです。  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### ステップ 3: ブラシとフォントの設定（フォントでテキストを描画）

`Brush` は図形やテキストの塗りつぶし色を定義し、`Font` はテキスト描画時の書体、サイズ、スタイルを指定します。  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### ステップ 4: インストール済みフォントを一覧表示し、フォントファミリーを示す

`InstalledFontCollection` はホストシステムにインストールされているすべてのフォントファミリーへのアクセスを提供します。  

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### ステップ 5: PNG 画像を保存

`bitmap.Save` はビットマップを PNG などの選択した画像形式でファイルに書き込みます。  

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

> **プロのコツ:** `Path.Combine` を使用してファイルパスを構築すると、異なる OS のディレクトリ区切り文字に起因する問題を回避できます。

## よくある問題と解決策
| 問題 | 原因 | 解決策 |
|-------|-------|-----|
| **フォントが表示されない** | `InstalledFontCollection` が未設定（例: フォントが無いヘッドレスサーバーで実行） | サーバーに必要なフォントをインストールするか、アプリケーションにカスタムフォントを埋め込んでください。 |
| **保存されたファイルが破損している** | ピクセルフォーマットが不正、または書き込み権限がない。 | 対象フォルダーが存在し、アプリが書き込み権限を持っていることを確認してください。`PixelFormat.Format32bppPArgb` を保持します。 |
| **テキストがぼやけて見える** | DPI 設定が低い、またはビットマップサイズが小さい。 | ビットマップのサイズを大きくするか、`graphics.SmoothingMode = SmoothingMode.AntiAlias` を設定してください。 |

## よくある質問

**Q: マシンにインストールされていないカスタムフォントを使用できますか？**  
A: はい。フォントファイルを `PrivateFontCollection` にロードし、そのコレクションから `Font` を作成して、システムフォントと同様に描画できます。

**Q: フォント関連の例外はどう処理すればよいですか？**  
A: フォント作成を `try/catch` ブロックで囲み、`ArgumentException` でフォントファミリーが見つからないか確認し、`Arial` などの代替フォントを提供してください。

**Q: Aspose.Drawing はウェブアプリケーションに適していますか？**  
A: はい。GDI+ を必要とせず、ASP.NET Core、Azure Functions、その他のサーバーサイド .NET 環境で動作します。

**Q: テキストの色やスタイルを変更できますか？**  
A: はい。異なる `Brush` タイプ（例: `LinearGradientBrush`）を使用し、`FontStyle` 列挙体を変更して太字、斜体、下線などを適用できます。

**Q: テスト用の一時ライセンスはどこで入手できますか？**  
A: [Aspose 一時ライセンスページ](https://purchase.aspose.com/temporary-license/) からトライアルライセンスをダウンロードしてください。

## 結論

これらの手順に従うことで、Aspose.Drawing for .NET を使用して **C# で PNG 画像を保存** し、動的に **インストール済みフォントの一覧を表示**、**フォントファミリーを示す**、**ビットマップからグラフィックを作成**、そして **フォントでテキストを描画** する方法を学びました。これで **C# でビットマップ グラフィックを作成** し、ビットマップの解像度を調整し、必要に応じてカスタムフォントを組み込む方法が分かります。プロジェクトのビジュアル要件に合わせて、色、フォントサイズ、ビットマップサイズを試行し、形状描画や画像操作などの他の Aspose.Drawing 機能も活用して、よりリッチなグラフィックを実現してください。

**最終更新日:** 2026-09-23  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

## 関連チュートリアル

- [Aspose.Drawing for .NET でテキストを描画する方法](/drawing/net/text-and-fonts/draw-text/)
- [Aspose.Drawing でアンチエイリアスを使用して画像品質を向上させる](/drawing/net/rendering/antialiasing/)
- [Aspose.Drawing で PNG を保存する方法 – ワールド変換](/drawing/net/coordinate-transformations/world-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}