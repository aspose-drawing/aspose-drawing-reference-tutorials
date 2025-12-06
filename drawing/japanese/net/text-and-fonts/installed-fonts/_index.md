---
date: 2025-12-06
description: Aspose.Drawing for .NET を使用して、インストールされているフォントの一覧表示、フォントファミリーの表示、ビットマップからのグラフィック作成、フォントを使用したテキスト描画、および
  PNG 画像ファイルの保存方法を学びましょう。
language: ja
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.DrawingでPNG画像を保存し、インストール済みフォントを使用する
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG画像を保存し、Aspose.Drawingでインストール済みフォントを使用する

## はじめに

**PNG画像** ファイルを保存し、かつマシンにインストールされているフォント情報も表示したい場合、Aspose.Drawing for .NET がクリーンでクロスプラットフォームな方法を提供します。このチュートリアルでは、インストール済みフォントの一覧取得、フォントファミリの表示、ビットマップからのグラフィック作成、フォントでのテキスト描画を順に解説し、最終的に PNG 画像として保存します。最後まで読むと、任意の .NET プロジェクトに組み込める再利用可能なコードスニペットが手に入ります。

## クイック回答
- **このチュートリアルで作成するものは？** インストール済みフォントファミリを一覧表示した PNG 画像です。  
- **必要なライブラリは？** Aspose.Drawing for .NET（System.Drawing.Common は不要）。  
- **カスタムフォントは使用できる？** はい。`InstalledFontCollection` にロードすれば利用可能です。  
- **出力解像度は調整できる？** もちろんです。ビットマップのサイズやピクセル形式を変更してください。  
- **コード実行にライセンスは必要？** 評価用の一時ライセンスで動作しますが、本番環境では正式ライセンスが必要です。

## Aspose.Drawing における「PNG画像を保存する」とは？
PNG 画像を保存するとは、描画対象（`Bitmap`）を `.png` 拡張子のファイルにエンコードすることです。Aspose.Drawing がエンコード処理を行うので、`bitmap.Save(...)` に保存先パスを指定して呼び出すだけで完了します。

## インストール済みフォントを一覧表示し、フォントファミリを示す理由
利用可能なフォントを把握することで、エンドユーザーの環境に合わせた動的なグラフィックを作成できます。レポートや証明書、企業ブランディングに合わせたビジュアルコンテンツをフォントファイルを配布せずに生成したい場合に特に有用です。

## 前提条件

- **Aspose.Drawing ライブラリ** – 最新バージョンは [Aspose Drawing ダウンロードページ](https://releases.aspose.com/drawing/net/) から取得してください。  
- **IDE** – Visual Studio、Rider、または任意の .NET 対応エディタ。  
- **基本的な C# 知識** – クラス、オブジェクト、簡単なループが扱えること。

## 名前空間のインポート
フォントとグラフィックを扱うために、C# ファイルの先頭で以下の名前空間をインポートします。

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 手順ガイド

### 手順 1: ビットマップ（キャンバス）の作成
まず、最終画像を保持するビットマップを作成します。ビットマップのサイズとピクセル形式が保存する PNG の品質を決定します。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 手順 2: ビットマップから Graphics を取得
次に、ビットマップから `Graphics` オブジェクトを取得します。このオブジェクトを使ってキャンバス上に図形、テキスト、画像を描画します。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### 手順 3: ブラシとフォントの設定（フォントでテキストを描画）
テキストの色を指定するブラシと、フォント名・サイズ・スタイルを定義する `Font` オブジェクトが必要です。

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### 手順 4: インストール済みフォントを一覧表示し、フォントファミリを示す
ここでは、フォントファミリの数と最初の数件の名前をビットマップ上に直接描画します。これにより **インストール済みフォントの一覧取得** と **フォントファミリの表示** が実演できます。

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### 手順 5: PNG 画像を保存
最後に、ビットマップを PNG ファイルとしてディスクに書き出します。これがコアとなる **PNG 画像の保存** 操作です。

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **プロのコツ:** `Path.Combine` を使用してファイルパスを組み立てると、OS 間でのディレクトリ区切り文字の違いによる問題を回避できます。

## よくある問題と対策
| 問題 | 原因 | 対策 |
|------|------|------|
| **フォントが表示されない** | `InstalledFontCollection` が空（例: フォントが無いヘッドレスサーバ上で実行） | サーバに必要なフォントをインストールするか、カスタムフォントをアプリに埋め込む |
| **保存したファイルが破損している** | ピクセル形式が不適切、または書き込み権限がない | 保存先フォルダが存在し、書き込み権限があることを確認。`Format32bppPArgb` を使用し続ける |
| **テキストがぼやけて見える** | DPI が低い | ビットマップのサイズを大きくするか、`graphics.SmoothingMode = SmoothingMode.AntiAlias` を設定する |

## FAQ

**Q: マシンにインストールされていないカスタムフォントは使用できますか？**  
A: はい。フォントファイルを `PrivateFontCollection` にロードし、そのコレクションから `Font` を作成します。

**Q: フォント関連の例外はどう処理すればよいですか？**  
A: フォント作成部分を `try/catch` で囲み、`ArgumentException` で不足しているファミリを確認します。

**Q: Aspose.Drawing は Web アプリケーションでも使えますか？**  
A: 完全に対応しています。ASP.NET Core、Azure Functions などサーバーサイド環境でも動作します。

**Q: テキストの色やスタイルを変更できますか？**  
A: 可能です。`LinearGradientBrush` などの別種ブラシを使用したり、`FontStyle` 列挙体でスタイルを変更したりできます。

**Q: テスト用の一時ライセンスはどこで取得できますか？**  
A: [Aspose 一時ライセンスページ](https://purchase.aspose.com/temporary-license/) からトライアルライセンスをダウンロードしてください。

## 結論

本手順に従うことで、Aspose.Drawing for .NET を利用して **PNG画像を保存** し、動的に **インストール済みフォントを一覧表示**、**フォントファミリを示す**、**ビットマップからグラフィックを作成**、**フォントでテキストを描画** する方法を習得できました。プロジェクトのビジュアル要件に合わせて、フォントや色、ビットマップサイズを自由に試してみてください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2025-12-06  
**テスト環境:** Aspose.Drawing 24.11 for .NET  
**作者:** Aspose