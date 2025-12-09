---
date: 2025-12-06
description: Scopri come salvare file immagine PNG elencando i font installati, mostrando
  le famiglie di font, creando grafica da bitmap e disegnando testo con i font usando
  Aspose.Drawing per .NET.
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Salva immagine PNG e lavora con i font installati in Aspose.Drawing
url: /it/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva immagine PNG e lavora con i font installati in Aspose.Drawing

## Introduzione

Se hai bisogno di **salvare immagini PNG** che mostrino anche informazioni sui font installati su una macchina, Aspose.Drawing per .NET ti offre un modo pulito e multipiattaforma per farlo. In questo tutorial vedremo come elencare i font installati, mostrare le famiglie di font, creare grafica da un bitmap e disegnare testo con i font—tutto per poi salvare il risultato come immagine PNG. Alla fine avrai uno snippet riutilizzabile da inserire in qualsiasi progetto .NET.

## Risposte rapide
- **Cosa crea questo tutorial?** Un'immagine PNG che elenca le famiglie di font installate.  
- **Quale libreria è necessaria?** Aspose.Drawing per .NET (non è necessario System.Drawing.Common).  
- **Posso usare font personalizzati?** Sì – basta caricarli in una `InstalledFontCollection`.  
- **La risoluzione dell'output è regolabile?** Assolutamente – modifica la dimensione del bitmap o il formato pixel.  
- **È necessaria una licenza per eseguire il codice?** Una licenza temporanea è sufficiente per la valutazione; è necessaria una licenza completa per la produzione.

## Cos'è “salvare immagine PNG” nel contesto di Aspose.Drawing?

Salvare un'immagine PNG significa renderizzare la tua superficie di disegno (un `Bitmap`) in un file con estensione `.png`. Aspose.Drawing gestisce la codifica per te, quindi devi solo chiamare `bitmap.Save(...)` con il percorso desiderato.

## Perché elencare i font installati e mostrare le famiglie di font?

Sapere quali font sono disponibili ti consente di creare grafica dinamica che si adatta all'ambiente dell'utente finale. È particolarmente utile per generare report, certificati o qualsiasi contenuto visivo che deve corrispondere al branding aziendale senza distribuire i file dei font.

## Prerequisiti

- **Libreria Aspose.Drawing** – scarica l'ultima versione dalla [pagina di download di Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider o qualsiasi editor compatibile con .NET.  
- **Conoscenza base di C#** – dovresti sentirti a tuo agio con classi, oggetti e semplici cicli.

## Importare gli spazi dei nomi
Per lavorare con i font e la grafica, importa questi spazi dei nomi all'inizio del tuo file C#:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step‑by‑Step Guide

### Passo 1: Creare un bitmap (la tela)
Prima, creiamo un bitmap che conterrà l'immagine finale. La dimensione del bitmap e il formato pixel determinano la qualità del PNG salvato.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Passo 2: Creare un oggetto Graphics dal bitmap
Successivamente, otteniamo un oggetto `Graphics` dal bitmap. Questo oggetto ci permette di disegnare forme, testo e immagini sulla tela.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Passo 3: Configurare pennello e font (disegnare testo con i font)
Abbiamo bisogno di un pennello per il colore del testo e di un oggetto `Font` che definisce il tipo di carattere, la dimensione e lo stile.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Passo 4: Elencare i font installati e mostrare le famiglie di font
Ora mostriamo il numero di famiglie di font e i primi nomi direttamente sul bitmap. Questo dimostra le funzionalità di **elencare i font installati** e **mostrare le famiglie di font**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Passo 5: Salvare l'immagine PNG
Infine, scriviamo il bitmap su disco come file PNG. Questa è l'operazione principale di **salvare immagine PNG**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Consiglio professionale:** Usa `Path.Combine` per costruire i percorsi dei file e evitare problemi con i separatori di directory su diversi sistemi operativi.

## Problemi comuni e soluzioni
| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **Nessun font visualizzato** | `InstalledFontCollection` non popolato (ad esempio, esecuzione su un server headless senza font). | Installa i font necessari sul server o incorpora font personalizzati nella tua applicazione. |
| **Il file salvato è corrotto** | Formato pixel errato o permessi di scrittura mancanti. | Assicurati che la cartella di destinazione esista e che l'app abbia i permessi di scrittura; mantieni `Format32bppPArgb`. |
| **Il testo appare sfocato** | Impostazioni DPI basse. | Aumenta le dimensioni del bitmap o imposta `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Domande frequenti

**D: Posso usare font personalizzati che non sono installati sulla macchina?**  
R: Sì. Carica il file del font in una `PrivateFontCollection` e crea un `Font` da quella collezione.

**D: Come gestisco le eccezioni legate ai font?**  
R: Avvolgi la creazione del font in un blocco `try/catch` e controlla `ArgumentException` per famiglie mancanti.

**D: Aspose.Drawing è adatto per applicazioni web?**  
R: Assolutamente. La libreria funziona in ASP.NET Core, Azure Functions e altri ambienti server‑side.

**D: Posso cambiare il colore o lo stile del testo?**  
R: Sì. Usa diversi tipi di `Brush` (ad esempio, `LinearGradientBrush`) e modifica l'enumerazione `FontStyle`.

**D: Dove posso ottenere una licenza temporanea per i test?**  
R: Scarica una licenza di prova dalla [pagina di licenza temporanea di Aspose](https://purchase.aspose.com/temporary-license/).

## Conclusione

Seguendo questi passaggi hai imparato a **salvare file PNG** che elencano dinamicamente i **font installati**, **mostrano le famiglie di font**, **creano grafica da un bitmap** e **disegnano testo con i font** usando Aspose.Drawing per .NET. Sentiti libero di sperimentare con altri font, colori e dimensioni del bitmap per soddisfare i requisiti visivi del tuo progetto.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2025-12-06  
**Testato con:** Aspose.Drawing 24.11 for .NET  
**Autore:** Aspose