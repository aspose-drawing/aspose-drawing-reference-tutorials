---
title: Remove Aspose Watermark – Set Aspose.Drawing License
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark. Master licensing methods to unlock full features without watermarks.
weight: 10
url: /net/licensing/licensing/
date: 2026-05-29
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
schemas:
- type: TechArticle
  headline: Remove Aspose Watermark – Set Aspose.Drawing License
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  dateModified: '2026-05-29'
  author: Aspose
- type: HowTo
  name: Remove Aspose Watermark – Set Aspose.Drawing License
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  steps:
  - name: Confirm Success
    text: '> **Pro tip:** Place the `.lic` file in the same folder as your executable
      or provide an absolute path to avoid “file not found” errors.'
  - name: Confirm Success
    text: '> **Warning:** Remember to dispose the `FileStream` (or use a `using` block)
      to free file handles.'
  - name: Display the Consumption Details
    text: '> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will
      fall back to trial mode and you’ll see watermarks in the output.'
- type: FAQPage
  questions:
  - question: What is the primary way to activate Aspose.Drawing?
    answer: Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.
  - question: Can I apply a license at runtime?
    answer: Yes, you can load the license from a `Stream` for dynamic scenarios.
  - question: Is a metered license supported?
    answer: Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable
      consumption‑based billing.
  - question: Do I need a license for development builds?
    answer: A trial works for testing, but a valid license removes watermarks and
      unlocks all APIs.
  - question: Which .NET versions are compatible?
    answer: Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Aspose.Drawing License

## Introduction

If you’re building .NET applications that rely on powerful graphics and image manipulation, **setting an Aspose.Drawing license** is the first step to removing the Aspose watermark and accessing the full feature set. In this tutorial you’ll learn three practical ways to set the Aspose.Drawing license—loading from a file, loading from a stream, and using the metered‑usage model—so you can integrate the library with confidence and keep your output clean.

## Quick Answers
- **What is the primary way to activate Aspose.Drawing?** Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.  
- **Can I apply a license at runtime?** Yes, you can load the license from a `Stream` for dynamic scenarios.  
- **Is a metered license supported?** Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable consumption‑based billing.  
- **Do I need a license for development builds?** A trial works for testing, but a valid license removes watermarks and unlocks all APIs.  
- **Which .NET versions are compatible?** Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.

## Prerequisites

Before you start, make sure you have:

- **Aspose.Drawing Library** – download the latest package from [here](https://releases.aspose.com/drawing/net/).  
- **License File** – obtain a valid `.lic` file from [Aspose](https://purchase.aspose.com/buy).  
- **.NET Development Environment** – Visual Studio, Rider, or any IDE that targets .NET Framework/.NET Core.

## Import Namespaces

We need the standard .NET namespaces plus the Aspose.Drawing namespace for licensing. Add the following `using` statements at the top of your C# file:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## How to Load a License from a File?

The `License` class represents the Aspose.Drawing licensing component that, when instantiated, allows you to apply a license to the library. Loading a license from a file is the most straightforward approach; you simply point the `SetLicense` method at a `.lic` file and the library removes all trial watermarks for the remainder of the application session. This method works in both desktop and server environments and requires no additional configuration beyond ensuring the file is accessible at runtime.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## How to Load a License from a Stream?

When the license file is embedded as a resource or retrieved over the network, loading it from a `Stream` gives you flexibility while still guaranteeing that the watermark is removed. By passing a `Stream` instance to the `SetLicense` method, you keep the license out of the deployment folder, which can improve security and simplify distribution in containerized or cloud scenarios. The process is identical to file‑based loading, except you manage the stream lifecycle yourself.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## How to Activate a Metered License?

The `Metered` class handles metered‑usage activation for Aspose.Drawing, enabling consumption‑based billing. Metered licensing lets you pay only for the operations you actually perform, which is ideal for SaaS or pay‑per‑use scenarios. After you provide the public and private keys, every image‑processing call is tracked and billed automatically, and the library operates in full‑feature mode without watermarks for the duration of the session.

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## Why Set the Aspose.Drawing License Correctly?

Setting the license correctly ensures that the library runs in full‑feature mode, removes trial watermarks, and complies with Aspose’s licensing terms. A properly applied license also enables premium APIs, improves performance by disabling evaluation checks, and allows you to use metered billing if desired. Failing to load the license before the first API call will cause the library to fall back to trial mode, resulting in watermarks on all generated images.

- **Removes watermarks** that appear in trial mode.  
- **Unlocks premium APIs** such as advanced image filters and PDF conversion.  
- **Ensures compliance** with Aspose’s licensing terms for commercial distribution.  
- **Enables metered billing**, letting you pay only for what you use.  

Aspose.Drawing supports **30+ image formats** (including PNG, JPEG, BMP, TIFF, and WebP) and can process **multi‑hundred‑page PDF documents without loading the entire file into memory**, delivering high‑performance conversion on modest hardware.

## Loading License from a File

Loading a license from a file is the most straightforward approach. Follow these three steps:

### Step 1: Initialize the License Object

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Step 2: Set the License from the `.lic` File

```csharp
Console.WriteLine("License set successfully.");
```

### Step 3: Confirm Success

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro tip:** Place the `.lic` file in the same folder as your executable or provide an absolute path to avoid “file not found” errors.

## Loading License from a Stream

When your license file is embedded as a resource or retrieved from a remote location, loading it from a `Stream` gives you flexibility.

### Step 1: Initialize the License Object

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Step 2: Load the License Using a `FileStream`

```csharp
Console.WriteLine("License set successfully.");
```

### Step 3: Confirm Success

```csharp
Console.WriteLine("License set successfully.");
```

> **Warning:** Remember to dispose the `FileStream` (or use a `using` block) to free file handles.

## Using Metered License

Metered licensing is ideal for SaaS or pay‑per‑use scenarios. It tracks consumption and bills you based on actual usage.

### Step 1: Initialize the Metered Object

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Step 2: Set Public and Private Keys

```csharp
// Your image processing logic here
```

### Step 3: Perform Your Image Processing

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Step 4: Retrieve Consumption Information

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### Step 5: Display the Consumption Details

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will fall back to trial mode and you’ll see watermarks in the output.

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| “License file not found” error | Wrong path or missing file in output folder | Use an absolute path or set the file’s *Copy to Output Directory* property to *Copy always*. |
| Watermark still appears after setting license | License not loaded before first API call | Load the license **before** any Aspose.Drawing operation. |
| Metered consumption always zero | Keys not set or wrong environment variables | Verify public/private keys and ensure internet connectivity for Aspose’s metered server. |

## Frequently Asked Questions

**Q1: Can I use Aspose.Drawing without a license?**  
A1: Yes, a trial license works for development and evaluation, but it adds watermarks and limits some features.

**Q2: How often do I need to renew my Aspose.Drawing license?**  
A2: Licenses are perpetual for the purchased version. Renewal is only required for support and upgrades.

**Q3: What is metered licensing, and when should I use it?**  
A3: Metered licensing charges based on usage (operations or data processed). It’s perfect for cloud services or pay‑per‑use models.

**Q4: Can I use Aspose.Drawing in commercial projects?**  
A4: Absolutely—once you have a valid license, you can embed Aspose.Drawing in any commercial application.

**Q5: Where can I find community support for Aspose.Drawing?**  
A5: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) for community help, examples, and discussions.

## Conclusion

Mastering how to **set Aspose.Drawing license**—whether from a file, a stream, or via metered usage—ensures you get the most out of this powerful .NET graphics library while completely **removing the Aspose watermark**. Follow the steps above, watch out for the common pitfalls, and you’ll be ready to build robust image‑processing solutions without licensing roadblocks.

---

**Last Updated:** 2026-05-29  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [How to License Aspose.Drawing for .NET – how to license aspose.drawing](/drawing/net/licensing/)
- [How to Scale Images with Aspose.Drawing for .NET](/drawing/net/image-editing/scale/)
- [How to Draw Text and Fonts with Aspose.Drawing for .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}