---
date: 2025-12-04
description: .NETでAspose.Drawingを使用した画像読み込み、バッチ画像変換、フォーマット変更をマスターしよう。BMPからPNGへの変換やその他の方法を学べます。
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.DrawingでBMPをPNGやその他の形式に変換
url: /ja/net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing を使用した BMP から PNG への変換およびその他のフォーマット

## Introduction

Aspose.Drawing for .NET を使用して **BMP を PNG に変換**（および多数の画像フォーマットへの変換）する手順をご紹介します。単一ファイルの **画像フォーマットの変更** が必要な場合でも、数十枚の画像を対象とした **バッチ画像変換** が必要な場合でも、このチュートリアルでは画像の読み込み、変換、保存をクリーンで保守しやすいコードで実装する方法を示します。

## Quick Answers
- **Aspose.Drawing は BMP を PNG に変換できますか？** はい – BMP を読み込み、拡張子 .png で `Save` を呼び出すだけです。  
- **バッチ変換はサポートされていますか？** もちろんです。ファイルをループし、同じ `LoadAndSave` メソッドを再利用します。  
- **本番環境でライセンスは必要ですか？** 本番利用にはライセンスが必要です。評価用の一時ライセンスが用意されています。  
- **対応している .NET バージョンは？** .NET Framework 4.5 以降、.NET Core 3.1 以降、.NET 5/6/7 で動作します。  
- **ライブラリはどこでダウンロードできますか？** 公式ダウンロードページから最新の Aspose.Drawing パッケージを取得してください。

## What is image format conversion c# with Aspose.Drawing?

Aspose.Drawing は、従来の `System.Drawing.Common` に代わる高性能で完全にマネージドされた .NET ライブラリです。**load image ASP.NET** シナリオをフルコントロールでき、100 以上の画像フォーマットをサポートし、プラットフォーム固有の制限を排除します。

## Why use Aspose.Drawing for batch image conversion?

- **クロスプラットフォームの信頼性** – GDI+ への依存がありません。  
- **豊富なフォーマットサポート** – BMP、GIF、JPG、PNG、TIFF など多数。  
- **一貫した API** – 同一コードが Windows、Linux、macOS で動作します。  
- **パフォーマンス** – 大規模画像処理パイプライン向けに最適化されています。

## Prerequisites

作業を始める前に以下を用意してください。

- **Aspose.Drawing for .NET** – こちらからダウンロード: [here](https://releases.aspose.com/drawing/net/)。  
- 動作する **.NET 開発環境**（Visual Studio、VS Code、または Rider）。

準備が整ったら、必要な名前空間をインポートしてコーディングを開始しましょう。

## Import Namespaces

.NET プロジェクトで必要な名前空間をインポートします。

```csharp
using System.Drawing;
```

これらのクラスが画像の読み込みと保存のコア機能を提供します。

## Step 1: Loading an Image

最初のステップは画像ファイルを読み込むことです。以下のサンプルは BMP を含むさまざまなフォーマットの画像を読み込む方法を示しています。

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## How to convert BMP to PNG with Aspose.Drawing

`LoadAndSave` メソッドは、ソースファイルの読み込みと目的の出力フォーマットへの保存の両方を処理します。引数に `"bmp"` を渡すと、`outputPath` の拡張子を変更した際に自動的に PNG ファイルが生成されます。

### Step 2.1: Load Image

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Step 2.2: Save Image (change image format)

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

各画像フォーマットごとに `LoadAndSave` 呼び出しを繰り返します。`outputPath` の拡張子を調整するだけで **BMP を PNG に変換**、**画像フォーマットを GIF、JPG などに変更** でき、同一メソッドで対応可能です。

## Common Pitfalls & Tips

- **ファイルパスの区切り文字** – 手動で文字列結合する代わりに `Path.Combine` を使用してクロスプラットフォームの安全性を確保してください。  
- **Bitmap の破棄** – `Bitmap` を `using` ブロックでラップし、ネイティブリソースを速やかに解放します。  
- **品質設定** – JPEG を保存する際は `EncoderParameters` オブジェクトで圧縮品質を指定すると便利です。  
- **バッチ処理** – 画像ファイルをフォルダーにまとめ、`Directory.GetFiles` を使って大規模変換を自動化しましょう。

## Frequently Asked Questions

### Q1: Aspose.Drawing はすべての画像フォーマットに対応していますか？

A1: Aspose.Drawing は BMP、GIF、JPG、PNG、TIFF など幅広いフォーマットをサポートしています。

### Q2: Aspose.Drawing の詳細ドキュメントはどこで確認できますか？

A2: 公式ドキュメントは [here](https://reference.aspose.com/drawing/net/) をご覧ください。

### Q3: Aspose.Drawing の一時ライセンスはどのように取得できますか？

A3: 一時ライセンスの詳細は [here](https://purchase.aspose.com/temporary-license/) で確認できます。

### Q4: 実装中に問題が発生したり質問がある場合はどうすればよいですか？

A4: Aspose.Drawing コミュニティは [Aspose Forum](https://forum.aspose.com/c/drawing/44) でサポートしています。

### Q5: Aspose.Drawing ライブラリはどこで購入できますか？

A5: 購入は [here](https://purchase.aspose.com/buy) から可能です。

**Additional Q&A**

**Q: このコードを ASP.NET Web アプリケーションで使用できますか？**  
A: はい – 同じ `LoadAndSave` ロジックは ASP.NET、MVC、Razor Pages でも動作します。ファイルパスが Web プロセスからアクセス可能であることを確認してください。

**Q: バッチ変換を高速化するために画像を並列処理できますか？**  
A: 可能です。`LoadAndSave` 呼び出しを `Parallel.ForEach` ループでラップしてください。ただし、`Bitmap` オブジェクトのスレッドセーフな破棄を忘れずに行う必要があります。

## Conclusion

これで **BMP を PNG に変換** し、**バッチ画像変換** を実行し、**画像フォーマットの変更** を Aspose.Drawing for .NET で行う方法を習得しました。これらのパターンを活用して画像パイプラインを自動化したり、サムネイルを生成したり、Web 配信用のアセットを準備したりしてください。さまざまなフォーマットで実験し、コードをサービスに統合し、完全にマネージドされた描画ライブラリの信頼性を体感しましょう。

---

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}